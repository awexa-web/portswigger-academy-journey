# Username Enumeration via Different Responses

## Lab Information

* **Platform:** PortSwigger Web Security Academy
* **Category:** Authentication vulnerabilities
* **Difficulty:** PRACTITIONER
* **Vulnerability:** Username Enumeration + Brute Force

---

## Description

This lab demonstrates how an application leaks information through different authentication error messages.

By analyzing the server responses, it is possible to determine whether a username exists and then brute-force the password.

---

## Objective

Identify a valid username, brute-force its password, and log in successfully.

---

## Tools Used

* Burp Suite Community Edition
* Burp Intruder
* Web Browser

---

# Step 1: Capture the Login Request

First, submit invalid credentials and intercept the request using Burp Proxy.

Example request:

```http id="g0d7f3"
POST /login HTTP/1.1
Host: lab-id.web-security-academy.net
Content-Type: application/x-www-form-urlencoded
.
.
.
username=test&password=test
```

Screenshot:

![Login Request](images/login-request.png)

---

# Step 2: Send to Intruder

From HTTP history, send the POST request to Intruder.

Screenshot:

![Intruder Setup](images/intruder-setup.png)

---

# Step 3: Setup Username Enumeration

Highlight the username parameter:

```http id="b8o9zy"
username=§test§&password=test
```

Attack type:

* Sniper

Load the candidate username list.

Screenshot:

![Username Payload Setup](images/username-payload.png)

---

# Step 4: Launch Username Attack

Start the attack.

Burp will test all usernames.

Most responses:

```text id="x3wpm7"
Invalid username
```

One response:

```text id="gq9qsn"
Incorrect password
```

This indicates a valid username.

Screenshot:

![Username Results](images/username-results.png)

---

# Step 5: Identify Valid Username

Sort by Length.

The different response length reveals the valid username.

look at

```text id="rdmbhk"
Username: root
```

Screenshot:

![Valid Username](images/valid-username.png)

---

# Step 6: Setup Password Brute Force

Clear the old payload markers.

Use the valid username:

```http id="ubm2r7"
username=root&password=§test§
```

Load the password list.

Screenshot:

![Password Payload Setup](images/password-payload.png)

---

# Step 7: Launch Password Attack

Start the attack.

Most responses return:

```text id="k0wl5a"
200 OK
```

One response returns:

```text id="sn72ua"
302 OK 
```

This means successful authentication.

Screenshot:

![Password Results](images/password-results.png)

---

# Step 8: Login with Found Credentials

Example credentials:

```text id="y0y4cu"
Username: root
Password: summer
```

Screenshot:

![Successful Login](images/successful-login.png)

---

# Step 9: Lab Solved

After login, access the account page.

Screenshot:

![Lab Solved](images/lab-solved.png)

---

# Why This Works

The application reveals whether usernames exist based on different error messages.

Attack flow:

1. Enumerate usernames
2. Identify valid user
3. Brute-force password
4. Access account

---

# Prevention

Developers should:

* Use generic error messages
* Implement rate limiting
* Add account lockouts
* Use CAPTCHA
* Monitor failed login attempts

---

# Key Takeaways

* Authentication logic can leak sensitive information
* Response length analysis is powerful
* Burp Intruder simplifies brute-force attacks
* Small differences can create big vulnerabilities
