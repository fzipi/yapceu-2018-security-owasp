---?image=assets/img/glasgow.png&position=left&size=55% 100%
@title[Talking Security]

# Securing Web Applications using OWASP

---

# OWASP

- OPEN: Everything at OWASP is radically transparent from our finances to our code.
- INNOVATION: OWASP encourages and supports innovation and experiments for solutions to software security challenges.
- GLOBAL: Anyone around the world is encouraged to participate in the OWASP community.
- INTEGRITY: OWASP is an honest and truthful, vendor neutral, global community. 

---

### Program

Input => your magic => Output

---?image=assets/img/unicorn.jpg

## @color[white](Instagram)

---?image=assets/img/garbage.jpg

## @color[red](vs. Reality)

---
## Verification

- Normally it refers to the act of contrasting what was implemented with the requirements.
- In Security, is the act of controlling that input(s) are correct semantically

+++
### Typing

- In the end there is a typing problem
- The web is a `string`
- But we have different types in our code, and in our DB
- And what about codifications?

+++
### Sanitize all inputs

- All inputs must be sanitized (well, it comes "tainted" ;)
- The resposibility relies on the `sub` that receives the data (this is easier when using MVC)

---
### Validation

- Once we have valid type for our data, is it valid in our context?
- If it is a valid ID, do you have permissions?
```perl
  my $id = "12345";
  if (can_access($user, $id)) {
```
@[1](VALID id)
@[2](Does the user has permissions then?)

---
## Context and Codification

- Codification depends on context.
- You cannot codify output as HTML, if your output is JS
- Sanitization will depend on context also (see for example Taint mode)

---

## OWASP

- Top Ten (2017)
- Top Ten Defensive Controls
- Application Security Verification Standard (ASVS)

---

### Top Ten

- A1:2017 - Injection
- A2:2017 - Broken Authentication
- A3:2017 - Sensitive Data Exposure
- A4:2017 - XML External Entities (XXE)
- A5:2017 - Broken Access Control
- A6:2017 - Security Misconfiguration
- A7:2017 - Cross-Site Scripting (XSS)
- A8:2017 - Insecure Deserialization
- A9:2017 - Using Components with Known Vulns
- A10:2017 - Insufficient Logging&Monitoring

---

## Top Ten Defensive Controls

- C1: Define Security Requirements
- C2: Leverage Security Frameworks and Libraries
- C3: Secure Database Access
- C4: Encode and Escape Data
- C5: Validate All Inputs
- C6: Implement Digital Identity
- C7: Enforce Access Controls
- C8: Protect Data Everywhere
- C9: Implement Security Logging and Monitoring
- C10: Handle All Errors and Exceptions

---?image=assets/img/asvs-levels.jpg

---

### ASVS

- V1. Architecture, design and threat modelling
- V2.	Authentication
- V3.	Session management
- V4.	Access control
- V5.	Malicious input handling
- V7.	Cryptography at rest
- V8.	Error handling and logging
- V9.	Data protection
- V10. Communications

---

- V11. HTTP security configuration
- V12. Security configuration verification requirements
- V13. Malicious controls
- V15. Business logic
- V16. File and resources
- V17. Mobile
- V18. Web services
- V19. Configuration

Note: One of the best ways to use the Application Security Verification Standard is to use it as blueprint create a Secure Coding Checklist specific to your application, platform or organization. Tailoring the ASVS to your use cases will increase the focus on the security requirements that are most important to your projects and environments. 

---

# Thanks!
