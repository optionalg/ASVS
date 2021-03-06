# V4: Access Control Verification Requirements

## Control Objective

Authorization is the concept of allowing access to resources only to those permitted to use them. Ensure that a verified application satisfies the following high level requirements:

* Persons accessing resources holds valid credentials to do so.
* Users are associated with a well-defined set of roles and privileges.
* Role and permission metadata is protected from replay or tampering.

## Security Verification Requirements

| # | Description | L1 | L2 | L3 | Since |
| --- | --- | --- | --- | -- | -- |
| **4.1** | Verify that the principle of least privilege exists - users should only be able to access functions, data files, URLs, controllers, services, and other resources, for which they possess specific authorization. This implies protection against spoofing and elevation of privilege. | ✓ | ✓ | ✓ | 1.0 |
| **4.4** | Verify that sensitive data and APIs are protected against direct object attacks targeting creation, reading, updating and deletion of records. | ✓ | ✓ | ✓ | 4.0 |
| **4.5** | Verify that directory browsing is disabled unless deliberately desired. Additionally, applications should not allow discovery or disclosure of file or directory metadata, such as Thumbs.db, .DS_Store, .git or .svn folders. | ✓ | ✓ | ✓ | 1.0 |
| **4.8** | Verify that access controls fail securely. | ✓ | ✓ | ✓ | 1.0 |
| **4.9** | Verify that the same access control rules implied by the presentation layer are enforced on the server side. | ✓ | ✓ | ✓ | 1.0 |
| **4.10** | Verify that all user and data attributes and policy information used by access controls cannot be manipulated by end users unless specifically authorized. |  | ✓ | ✓ | 1.0 |
| **4.11** | Verify that there is preferably only one vetted access control mechanism for protecting access to protected data and resources, such that hard coded access control checks are not required throughout the application. |  | ✓ | ✓ | 4.0 |
| **4.12** | Verify that all access control decisions can be logged and all failed decisions are logged. |  | ✓ | ✓ | 2.0 |
| **4.13** | Verify that the application or framework enforces a strong anti-CSRF mechanism any sensitive functionality. | ✓ | ✓ | ✓ | 4.0 |
| **4.14** | Verify the application has sufficient anti-automation to detect and protect against data exfiltration, excessive business logic requests, or denial of service attacks. |  | ✓ | ✓ | 4.0 |
| **4.15** | Verify the application has additional authorization (such as step up or adaptive authentication) for lower value systems, and / or segregation of duties for high value applications to enforce anti-fraud controls as per the risk of application and past fraud. |  | ✓ | ✓ | 3.0 |
| **4.16** | Verify that access control policy is enforced by trusted server-side components.  | ✓ | ✓ | ✓ | 4.0 |
| **4.17** | Verify that data-level access control is implemented such that access to individual records can be managed in a centralized and standard way. | ✓ | ✓ | ✓ | 4.0 |

## References

For more information, see also:

* [OWASP Testing Guide 4.0: Authorization](https://www.owasp.org/index.php/Testing_for_Authorization)
* [OWASP Cheat Sheet: Access Control](https://www.owasp.org/index.php/Access_Control_Cheat_Sheet)
* [OWASP CSRF Cheat Sheet](https://www.owasp.org/index.php/Cross-Site_Request_Forgery_(CSRF)_Prevention_Cheat_Sheet)
* [OWASP REST Cheat Sheet](https://www.owasp.org/index.php/REST_Security_Cheat_Sheet)
* Anti-automation can be achieved in many ways, including the user of [OWASP AppSensor](https://www.owasp.org/index.php/OWASP_AppSensor_Project) and [OWASP Automated Threats to Web Applications](https://www.owasp.org/index.php/OWASP_Automated_Threats_to_Web_Applications)