#### ADR-6: Sensitive data access

**Date**
2021-10-29

**Status**
Proposed

**Context**
Based on the requirements provided by Product Owner, Farmacy Family System stores personally identifiable dietary and nutritional information about U.S. citizens and may share this information with 3d-party medical service providers which falls under the purview of Health Insurance Portability and Accountability Act (HIPAA). 

HIPAA requires data at rest to be secured according to NIST 800-111 and data in motion to be secured by NIST 800-52, 800-77, or FIPS140-2, and that legally binding customer authorisation to be provided for 3d-party access to personally identifiable medical data. Farmacy Family System is AWS-based.

**Decision**
The Farmacy Family System must comply with legal requirements. Standards-based Transport Layer Security (TLS) adequately secures data in motion at little or no cost. AWS services eligible for HIPAA ([HIPAA Eligible Services Reference](https://aws.amazon.com/compliance/hipaa-eligible-services-reference/)) must be used to store or process sensitive data in the manner recommended by AWS in a relevant whitepaper ([Architecting for HIPAA Security and Compliance on Amazon Web Services - AWS Whitepaper](https://docs.aws.amazon.com/whitepapers/latest/architecting-hipaa-security-and-compliance-on-aws/architecting-hipaa-security-and-compliance-on-aws.pdf)). 

Customer authorisation form processing may be handled by a 3d-party service provider ([https://www.jotform.com/hipaa/](https://www.jotform.com/hipaa/)) or developed in-house, but given development complexity caused by the variety of methods by which legally binding customer authorisation may be obtained (e.g. [How do HIPAA authorizations apply to an electronic health information exchange environment?](https://www.hhs.gov/hipaa/for-professionals/faq/554/how-do-hipaa-authorizations-apply-to-electronic-health-information/index.html) or  [Is a copy, facsimile, or electronically transmitted version of a signed authorization valid under the Privacy Rule?](https://www.hhs.gov/hipaa/for-professionals/faq/475/is-a-copy-of-a-signed-authorization-valid/index.html)) certain fluidity of relevant legislation and seriousness of consequences of non-compliance with HIPAA requirements 3d-party service is the obvious choice as being faster and cheaper to implement and because it transfers the risks of non-compliance to a service provider.