# 🔐 Authentication Vulnerabilities


## What is authentication?

Authentication is the process of verifying the identity of a user.

Authentication usually works on three factors:
1. **Knowledge factor** – something the user knows (like a password)
2. **Possession factor** – something the user has (like an OTP or token)
3. **Inherence factor** – something the user is (like biometrics)


## Difference between authentication and authorization

- **Authentication** is the process of verifying if the user is who they claim to be.
- **Authorization** is the process of verifying if the authenticated user has permission to perform specific operations.

> _Permissions define what an authenticated user is allowed to do._


## How do authentication vulnerabilities arise?

- Weak protection against brute-force attacks
- Poorly implemented authentication mechanisms that can be bypassed
- Lack of proper rate limiting, CAPTCHA, or account lockout features


## Impact of vulnerable authentication

- If a user's account is compromised, the attacker gains access to their data and functionality.
- This may open the door to **privilege escalation** or **lateral movement**, eventually compromising admin accounts or internal infrastructure.
- Attackers can take over the system entirely and access sensitive areas of the web application.


## Vulnerabilities in Password-Based Login

Password-based logins are still the most common form of authentication. Either a user creates an account or an admin provides them with a username and password. If an attacker is able to guess both, they gain access.

### a. Brute-Force Attacks

Attackers use tools to rapidly try different combinations of usernames and passwords until they succeed.

- They often don't guess randomly – instead, they use:
  - Common passwords
  - Leaked password lists
  - Patterns based on public user information

#### Brute-forcing usernames:
- Usernames are often **exposed publicly**.
- Many systems use **email addresses** for login, which are easy to find.

#### Brute-forcing passwords:
- Even though users are told to keep passwords safe, common passwords like `12345678` are still used.
- Attackers can use lists of such weak passwords to attempt access.

> That's why websites enforce password complexity requirements:
- A minimum number of characters
- A mix of upper and lowercase letters
- At least one special character

But even with that, if the password is:
- Based on public or personal info
- Easy to guess
- Reused across sites

It can still be broken.

And even when users create "strong" passwords, they often follow memorable patterns – making them predictable again.
