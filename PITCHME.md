---?image=assets/img/glasgow.png&position=left&size=55% 100%
@title[Talking Security]

# Talking... Security @fa[lock]

---

# OWASP

- Open Web Application Security Project
- Non-profit 

---

# Programs

Input @fa[fa-arrow-right] <your magic> @fa[fa-arrow-right] Output

---image?https://www.flickr.com/photos/michaelpollak/9880194566/in/photolist-g45zCb-DxGE6-2V1ELY-2uXYSi-9SGxew-4dUMkG-7jSKZw-729nxJ-8j3BGv-qu1r6D-8Cofh7-3eQ6wd-4kwHwD-iZgr-8XYQJ-4U1txC-ae48U-4mJoBF-9qHDHy-7vwvSZ-7cxjtg-2a8Vf7-681xjL-bDs6Ta-dpjZQK-aANxgS-a1k5ZR-2vaj1s-Lg1n-4BR2pv-39G2KH-F68W5-qDUA-j1WcdT-4r7s87-fiuN3v-oNuSF9-8hYJsE-4dUMoS-4Vx5og-JTAxia-9Rzsir-5HXkzh-KtgS9-5rhRFJ-247143Q-dw6wgp-dDtJcM-qZpza-5AVMGj/lightbox/

Instagram

---image?https://www.flickr.com/photos/22695020@N03/4197357363/in/photolist-7oUy7p-dApeZG-6zb4sW-2JGNq-7i6ECt-zkr5LP-dZ8Wyd-6WYRSS-2vSuro-nRnQX-BtfofB-227Yq-dkFREq-enUMLw-2h8YRd-c1XP5-RBY7-2ij8F-9o1VF-cAnv5h-7Z2hZz-7AfAJ-C8PKA-8oeTrS-2JJvzz-dkFPJZ-bVVvzq-AUJSVP-Btg12r-7nTAb8-8kxLVE-9JoEU9-3qAWUb-88CR-227Yo-wHZV7-4JQPD-2UnBJ-xyC4w-4qWMvs-9j4rD-RFNh-4SnfRZ-25EUKr-6HKop8-4JQyC-2bi8S-67TxHp-cjzCn-2FJKMw/lightbox/

vs. Reality

---
## Verification

- Normally it refers to the act of contrasting what was implemented with the requirements.
- In Security, is the act of controlling that input(s) are correct semantically

+++
### Typing

@ul

- In the end there is a typing problem
- The web is a `string`
- But we have different types in our code, and in our DB
- And what about codifications?

@ulend

+++
### Sanitize all inputs

@ul

- All inputs must be sanitized (well, it comes "tainted" ;)
- The resposibility relies on the `sub` that receives the data (this is easier when using MVC)

@ulend

---
### Validation

- Is the act of dinamically execute and test a program, so it conforms with the actual requirements.
- Do you remember, we already did verification!
- Once we have valid type for our data, is it valid in our context?
- If it is some ID, it is valid and the user can access it?

---
## Context and Codification

@ul

- Codification depends on context.
- You cannot codify output as HTML, if you are outputting JS
- Sanitization will depend on context also (see for example Taint mode)

@ulend

---
## OWASP Top Ten

A1:2017 - Injection
A2:2017 - Broken Authentication
A3:2017 - Sensitive Data Exposure
A4:2017 - XML External Entities (XXE)
A5:2017 - Broken Access Control
A6:2017 - Security Misconfiguration
A7:2017 - Cross-Site Scripting (XSS)
A8:2017 - Insecure Deserialization
A9:2017 - Using Components with Known Vulnerabilities
A10:2017 - Insufficient Logging&Monitoring

https://www.owasp.org/images/7/72/OWASP_Top_10-2017_%28en%29.pdf.pdf

---
## OWASP Top Ten Defensive Controls

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

https://www.owasp.org/images/b/bc/OWASP_Top_10_Proactive_Controls_V3.pdf

---
## OWASP ASVS
### Application Security Verification Standard

@snap[east]
V1. Architecture, design and threat modelling
V2.	Authentication
V3.	Session management
V4.	Access control
V5.	Malicious input handling
V7.	Cryptography at rest
V8.	Error handling and logging
V9.	Data protection
V10. Communications
@snapend

@snap[west]
V11. HTTP security configuration
V12. Security configuration verification requirements
V13. Malicious controls
V15. Business logic
V16. File and resources
V17. Mobile
V18. Web services
V19. Configuration
@snapend

Note: One of the best ways to use the Application Security Verification Standard is to use it as blueprint create a Secure Coding Checklist specific to your application, platform or organization. Tailoring the ASVS to your use cases will increase the focus on the security requirements that are most important to your projects and environments. 

---image?assets/img/asvs-levels.jpg
## ASVS Levels


