# ☁️ Cloud Security Implementation on AWS  
**Internship Project | Codetech IT Solutions**  
**Domain:** Cloud Computing | **Duration:** 4 Weeks  

---

## 📌 Objective

The objective of this project is to implement key **cloud security measures** on the **Amazon Web Services (AWS)** platform. These include:

- Creating secure and controlled access using **IAM (Identity and Access Management)**.
- Ensuring **data confidentiality** and **integrity** through **encryption**.
- Leveraging **AWS S3 and KMS (Key Management Service)** for secure storage and cryptographic key management.

This implementation demonstrates a real-world approach to managing cloud resources securely using IAM roles, policies, S3 storage encryption, and KMS.

---

## 🔐 Identity and Access Management (IAM)

**IAM** is a core AWS security service that enables administrators to control access to AWS services and resources securely.

### 🔧 Implementation Steps:
1. **Created an IAM user** to simulate a secondary user login for AWS Console access.
2. Designed a **custom IAM policy** that allows the IAM user to access **only Amazon S3 services**.
3. Attached the policy to the user, enforcing **principle of least privilege**.
4. Verified access by logging in as the IAM user and confirming access was restricted only to S3, as defined in the policy.

IAM policies are written in JSON and define explicit **Allow** or **Deny** permissions on actions and resources. This helps in granular access control and audit-friendly configurations.

### 📸 Output – IAM Policy Applied:
![IAM Policy Screenshot](https://github.com/user-attachments/assets/4fb6d758-6303-46e6-8826-b62c6350bd44)

---

## 🔒 Secure Storage & Data Encryption

To ensure secure storage of data in the cloud, **Amazon S3** was used in conjunction with **AWS KMS (Key Management Service)** to encrypt data at rest.

### 🔧 Implementation Steps:
1. **Created a KMS Key** named `task-4-s3-kms-key` for encryption operations.
2. **Created a new S3 bucket** to store sensitive data.
3. Enabled **default encryption** on the S3 bucket using the custom KMS key.
4. Uploaded files to the S3 bucket and verified they were encrypted using the specified key.
5. Verified encryption status using the AWS S3 object properties to ensure **KMS key association**.

This setup guarantees that any data uploaded to the bucket is encrypted automatically, and access to the key is managed securely via IAM.

### 🛡️ Benefits:
- Protection against unauthorized data access.
- Fine-grained control over who can use or manage the encryption keys.
- Easy compliance with regulatory requirements like GDPR, HIPAA, etc.

### 📸 Output – Secure Storage & Encryption Enabled:
![Secure Storage Screenshot](https://github.com/user-attachments/assets/bee7e990-0f46-403c-b927-d40aa7cbb169)

---

## ⚙️ Tools & Technologies Used

| Technology | Purpose |
|------------|---------|
| **AWS IAM** | Identity and access control |
| **Amazon S3** | Scalable cloud storage |
| **AWS KMS** | Encryption key management |
| **AWS Console** | User interface for configuration and testing |

---

## ✅ Key Takeaways

- Learned how to set up IAM users and restrict permissions using custom policies.
- Understood how AWS KMS integrates with S3 for automatic encryption of data.
- Gained hands-on experience with core AWS security services.
- Practiced the **least privilege access model** to protect cloud environments.

---

## 📚 Additional Notes

- IAM policies can be further extended to support multiple services and conditional permissions.
- KMS supports key rotation and logging via AWS CloudTrail for auditability.
- S3 supports both **server-side encryption (SSE)** with KMS and **client-side encryption** – in this project, **SSE-KMS** was used.

---

## 🧠 Conclusion

This project highlights the importance of implementing security at both the **access control** and **data protection** layers of a cloud environment. Using AWS IAM and KMS together provides a scalable and secure architecture to manage resources and sensitive information effectively. These configurations align with best practices for **cloud security architecture** and are foundational for building secure cloud-native applications.

---

