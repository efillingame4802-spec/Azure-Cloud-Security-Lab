Week 2 - Identity Security Lab

Controls Implemented

    Cloud-Native Administrative Account
    Microsoft Entra ID P2
    Microsoft Authenticator MFA
    Security Groups
    Azure RBAC
    Conditional Access
    Privileged Identity Management (PIM)

Administrative Model

    Break Glass Account
    Cloud Administrator
    Standard User
Identity Architecture

    Cloud Administrator:
        Member of Azure-Security-Admins

    Azure-Security-Admins:
        Assigned Owner Role

    Edward User:
        Assigned Reader Role
Security Improvements

    Implemented cloud-native administrative account
    Configured Microsoft Authenticator MFA
    Implemented group-based access control
    Assigned Azure permissions through security groups
    Created Conditional Access policy in Report-Only mode
    Configured Privileged Identity Management at subscription scope

Lessons Learned

    Native cloud accounts simplify Microsoft 365 administration.
    Microsoft Authenticator provides stronger authentication than passwords alone.
    Security groups simplify access management and improve scalability.
    RBAC allows implementation of the least privilege principle.
    Conditional Access supports Zero Trust security models.
    PIM enables just-in-time privilege management.
Future Improvements

    Enable Conditional Access policy
    Implement eligible Owner assignments through PIM
    Configure Defender for Cloud
    Deploy Microsoft Sentinel
    Implement KQL threat hunting
    Create automated response playbooks
    Terraform infrastructure deployment
