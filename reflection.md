\## AWS Cloud Security Reflection



In this lab, I applied core cloud security principles to configure an AWS environment in a secure and controlled way. The main focus was reducing risk through proper access control, secure configurations, and monitoring.



For IAM, I avoided using the root account and instead worked with a restricted user. This follows the principle of least privilege, which limits what a user can do and reduces the potential damage if credentials are compromised. This is critical in cloud environments where misused credentials can lead to full account takeover.



For S3, I enabled "Block all public access" to ensure that no data can be accidentally exposed to the internet. This directly relates to real-world incidents like the Capital One breach, where misconfigured cloud resources contributed to sensitive data exposure. This step protects confidentiality by preventing unauthorized access to stored data.



For EC2, I configured the security group to allow SSH access only from my personal IP address instead of allowing access from anywhere (0.0.0.0/0). This significantly reduces the attack surface and prevents automated attacks or unauthorized login attempts. This improves both confidentiality and integrity by controlling who can access the system.



In terms of availability, these configurations ensure that systems remain usable while still being secure. For example, restricting access does not prevent legitimate use but protects against malicious traffic that could disrupt services.



Finally, I reviewed AWS Billing and CloudTrail to improve visibility. Billing allows detection of unexpected costs that may indicate misuse, while CloudTrail logs all account activity. This supports all three aspects of the CIA triad by helping detect, investigate, and respond to potential security incidents.



This lab demonstrated that cloud security is not about complex tools, but about making correct configuration decisions. Small mistakes, such as overly permissive access or public storage, can lead to major breaches, while simple controls can significantly improve security.

