# PortSwigger Web Security Academy - Solved Labs

![Total Labs](https://img.shields.io/badge/Total%20Labs-%2034-blue) ![Last Updated](https://img.shields.io/badge/Last%20Updated-%20SQL-injection-attack-listing-the-database-contents-on-non-Oracle-databases-lightgrey)

This repository tracks progress through PortSwigger Web Security Academy labs. It is structured as a solved labs tracker with an empty table ready for future updates and writeup links.

## Level progress
- **Apprentice**: 27 of 61
- **Practitioner**: 33 of 174
- **Expert**: 0 of 39

## Categories Covered
- **Web cache deception**: 5/5 lab
- **Server-side request forgery (SSRF)**: 4/5 lab
- **Authentication vulnerabilities**: 11/11 lab
- **Clickjacking**: 5/5 lab
- **API Testing**: 0/0 lab
- **Access control**: 0/0 lab
- **SQL injection**: 0/0 lab
- **Cross-site scripting**: 0/0 lab
- **Server-side template injection**: 0/0 lab
- **JWT attacks**: 0/0 lab
- **OAuth authentication**: 0/0 lab
- **GraphQL API vulnerabilities**: 0/0 lab
- **Insecure deserialization**: 0/0 lab
- **XXE injection**: 0/0 lab
- **NoSQL injection**: 0/0 lab
- **Request smuggling**: 0/0 lab

## Notes
- Full writeups are reserved for significant lab findings and technique notes.
- Tools used: Burp Suite, browser developer tools, HTTP proxy.

## How to Read
- `No`: Sequential lab number.
- `Date`: When the lab was solved.
- `Topic`: Vulnerability category.
- `Lab Title`: Exact lab name.
- `Difficulty`: Apprentice, Practitioner, or Expert.
- `Writeup Link`: Link to detailed notes or `N/A`.

## Solved Labs

| No | Date    | Topic                 | Lab Title | Difficulty | Writeup Link |
|----|---------|-----------------------|-----------|------------|--------------|
| 1  |2025-6-10  | Web cache deception   |Exploiting path mapping for web cache deception     | APPRENTICE   | N/A          |
| 2  |2025-6-10  | Web cache deception   |Exploiting path delimiters for web cache deception    |PRACTITIONER | N/A  |
| 3 |2025-6-10  | Web cache deception   |Exploiting origin server normalization for web cache deception     |PRACTITIONER | N/A  |
| 4 |2025-6-10  | Web cache deception   |Exploiting cache server normalization for web cache deception  |PRACTITIONER | N/A |
| 5 | 2025-6-11 |  Server-side request forgery (SSRF) |Basic SSRF against the local server |APPRENTICE     |N/A|
| 6 | 2025-6-11 |  Server-side request forgery (SSRF) |Basic SSRF against another back-end system |   APPRENTICE     |N/A|
| 7 | 2025-6-11 |  Server-side request forgery (SSRF) |SSRF with blacklist-based input filter |   PRACTITIONER     |N/A|
| 8 | 2025-6-11 |  Server-side request forgery (SSRF) | SSRF with filter bypass via open redirection vulnerability|   PRACTITIONER     |N/A|
| 9 | 2025-6-11 |  Server-side request forgery (SSRF) |Blind SSRF with out-of-band detection  |   PRACTITIONER     |N/A|
| 10 | 2025-6-12 |  Authentication vulnerabilities |Username enumeration via different responses |   APPRENTICE |[writeup](https://medium.com/@awela1499/username-enumeration-via-different-responses-portswigger-lab-17dd6255e1bb)|
| 11 | 2025-6-12 |  Authentication vulnerabilities |Username enumeration via subtly different responses|   PRACTITIONER |N/A|
| 12| 2025-6-12 |  Authentication vulnerabilities |Username enumeration via response timing|   PRACTITIONER |N/A|
| 13 | 2025-6-12 |  Authentication vulnerabilities |Broken brute-force protection, IP block  |   PRACTITIONER |N/A|
| 14 | 2025-6-13 |  Authentication vulnerabilities |   2FA simple bypass  |   APPRENTICE |N/A|
| 15 | 2025-6-13 |  Authentication vulnerabilities |2FA broken logic  |   PRACTITIONER |N/A|
| 16 | 2025-6-13 |  Authentication vulnerabilities |Brute-forcing a stay-logged-in cookie  |   PRACTITIONER |N/A|
| 17 | 2025-6-13 |  Authentication vulnerabilities | Offline password cracking |   PRACTITIONER |N/A|
| 18 | 2025-6-13 |  Authentication vulnerabilities |Password reset broken logic  |   APPRENTICE |N/A|
| 19| 2025-6-13 |  Authentication vulnerabilities |Password reset poisoning via middleware |   PRACTITIONER |N/A|
| 20 | 2025-6-13 |  Authentication vulnerabilities | Password brute-force via password change|   PRACTITIONER |N/A|
| 21  | 2025-6-14 |Clickjacking (UI redressing)    |Basic clickjacking with CSRF token protection |   APPRENTICE     |N/A|
| 22  | 2025-6-14 |Clickjacking (UI redressing)    |Clickjacking with form input data prefilled from a URL parameter |APPRENTICE |N/A|
| 23 | 2025-6-14 |Clickjacking (UI redressing)    |Clickjacking with a frame buster script |APPRENTICE   |N/A|
| 24  | 2025-6-14 |Clickjacking (UI redressing)    |Exploiting clickjacking vulnerability to trigger DOM-based XSS |   PRACTITIONER     |N/A|
| 25  | 2025-6-14 |Clickjacking (UI redressing)    |Multistep clickjacking|   PRACTITIONER     |N/A|
| 26  | 2025-6-16 |SQL injection|SQL injection vulnerability in WHERE clause allowing retrieval of hidden data|APPRENTICE|N/A|
| 27  | 2025-6-16 |SQL injection| SQL injection vulnerability allowing login bypass|APPRENTICE|N/A|
| 28  | 2025-6-16 |SQL injection| SQL injection UNION attack, determining the number of columns returned by the query|   PRACTITIONER     |N/A|
| 29  | 2025-6-16 |SQL injection|SQL injection UNION attack, finding a column containing text|   PRACTITIONER |N/A|
| 30  | 2025-6-16 |SQL injection| SQL injection UNION attack, retrieving data from other tables|   PRACTITIONER |N/A|
| 31  | 2025-6-16 |SQL injection| SQL injection UNION attack, retrieving multiple values in a single column|PRACTITIONER|N/A|
| 32  | 2025-6-17 |SQL injection| SQL injection attack, querying the database type and version on MySQL and Microsoft| PRACTITIONER|N/A|
| 33  | 2025-6-17 |SQL injection| SQL injection attack, listing the database contents on non-Oracle databases|PRACTITIONER|N/A|
