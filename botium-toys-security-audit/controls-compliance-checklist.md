## Controls Assessment Checklist

| Control | Implemented |
|---|---|
| Least Privilege | No |
| Disaster recovery plans | No |
| Password policies | No |
| Separation of duties | No |
| Firewall | Yes |
| Intrusion detection system (IDS) | No |
| Backups | No |
| Antivirus software | Yes |
| Manual monitoring/maintenance for legacy systems | No |
| Encryption | No |
| Password management system | No |
| Locks (offices, storefront, warehouse) | Yes |
| CCTV surveillance | Yes |
| Fire detection/prevention | Yes |

## Compliance Checklist

### PCI DSS
| Best Practice | Met |
|---|---|
| Only authorized users have access to customers' credit card information | No |
| Credit card information is stored, accepted, processed, and transmitted in a secure environment | No |
| Data encryption procedures are implemented for credit card transactions | No |
| Secure password management policies are adopted | No |

### GDPR
| Best Practice | Met |
|---|---|
| E.U. customers' data is kept private/secured | No |
| Plan in place to notify E.U. customers within 72 hours of a breach | Yes |
| Data is properly classified and inventoried | No |
| Privacy policies, procedures, and processes are enforced | Yes |

### SOC (Type 1 / Type 2)
| Best Practice | Met |
|---|---|
| User access policies are established | No |
| Sensitive data (PII/SPII) is confidential/private | No |
| Data integrity is maintained (consistent, complete, accurate, validated) | Yes |
| Data is available to authorized individuals | No |

## Recommendations

To improve Botium Toys' security posture, several best practices should be implemented, such as the principle of least privilege, password policies, encryption, and GDPR compliance.

1. **Least Privilege:** Currently, there are no access restrictions to confidential data, posing a serious security risk. This should be strictly enforced to reduce the risk of misuse of PII/SPII. A role-based access control should be used to restrict certain users from accessing unnecessary data for their role.

2. **Secure Password Policies:** Stronger password policies need to be implemented to reduce the risk of brute force attacks, which could lead to more severe consequences if there is unauthorized entry to the system. Enforce a more complex password requirement, especially for users with access to confidential data.

3. **Encryption:** Customers' data should be encrypted to ensure the confidentiality of their information. Not establishing encryption protocols is against the Payment Card Industry Data Security Standard (PCI DSS). Credit card information needs to be encrypted when stored, accepted, processed, and transmitted. Implement AES-256 for storing data, and TLS 1.3 for data transmission to prioritize confidentiality.

4. **GDPR Compliance:** As of now, E.U. customers' data is not confidential, and Botium Toys is not in compliance. If best practices are not implemented, Botium Toys could face severe consequences. Previous recommendations should be implemented, along with proper classification and inventory of data. Data should be classified based on its sensitivity.
