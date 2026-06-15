**Secret-manager-lab**
This project demonstrates the implementation of Google Cloud Secret Manager for securely storing, managing, and retrieving sensitive information such as database passwords and API keys. 
The lab covers secret creation, version management, secure access patterns, and enterprise security best practices

**Architecture Diagram**
Application
      │
      ▼
Service Account
      │
      ▼
Secret Manager
   │         │
   ▼         ▼
db-password  api-key

**Services Used**

Google Cloud Secret Manager
Secure secret storage
Secret versioning
Secret rotation
Access control

**IAM (Identity and Access Management)**

User authorization
Access management
Least privilege principle

**Service Accounts**

Application identity
Secure access to secrets

**Objectives**

Understand Secret Manager architecture
Create and manage secrets
Learn secret versioning
Securely retrieve secrets
Understand application authentication patterns
Learn enterprise security best practices

**Secret Creation**
Secret 1
Secret Name: db-password
Value: MySecurePassword123!

**Purpose:**
Stores database credentials securely.

Secret 2
Secret Name: api-key
Value: sample-api-key-123

**Purpose:**
Stores API credentials securely.
Secret Versioning

**Secret Manager automatically creates versions for each secret.**

Example:
db-password
     │
     ├── Version 1
     ├── Version 2
     └── Version 3

**Benefits:**

Secret rotation
Rollback capability
Compliance support
Auditing and tracking

**During this lab:**
Version 1
Status: Enabled was successfully created and verified.

**Secure Retrieval**
Secret retrieval workflow:

Application
      ↓
Service Account
      ↓
Secret Manager
      ↓
Retrieve Secret

**Verified Secret: MySecurePassword123!**

**Benefits:**

No hardcoded credentials
Centralized management
Secure access control
Improved security posture

**Secret Manager vs KMS**

| Feature                | Secret Manager | Cloud KMS      |
| ---------------------- | -------------- | -------------- |
| Stores Passwords       | Yes            | No             |
| Stores API Keys        | Yes            | No             |
| Stores Tokens          | Yes            | No             |
| Stores Encryption Keys | No             | Yes            |
| Key Rotation           | No             | Yes            |
| CMEK Support           | No             | Yes            |
| Primary Use            | Secret Storage | Key Management |

**Quick Rule**
Password → Secret Manager
Encryption Key → Cloud KMS

**Production Improvements**

Implement least-privilege IAM roles
Use Service Accounts instead of user credentials
Enable audit logging
Implement secret rotation policies
Use customer-managed encryption keys (CMEK) where required
Regularly review access permissions
Monitor secret access events

**Key Learnings**

Secret Manager securely stores sensitive information
Secret versioning supports rotation and rollback
Service Accounts provide secure application identity
IAM controls access to secrets
Hardcoded credentials should be avoided
Secret Manager improves security and compliance

**Final Outcome**

Successfully implemented Google Cloud Secret Manager to securely store and retrieve sensitive information. 
Created secrets for database credentials and API keys, explored secret versioning, verified secure retrieval, and 
learned enterprise-grade security practices for cloud-native applications.

