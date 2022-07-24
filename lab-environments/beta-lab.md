# Summary

- Single Active Directory Forest/Domain (beta.ajf8729.com)
- Synchronized to Azure AD (ajf8729tplab.onmicrosoft.com)
- ConfigMgr Standalone Primary Site
  - Technical Preview Branch
  - HTTPS-Only Mode

# Hosts

## BETADC01.beta.ajf8729.com

- Windows Server vNext 25128 Datacenter
- 172.30.3.2/24
- Alternative Hostnames
  - PKI.beta.ajf8729.com
- Roles
  - Active Directory Certificate Services
    - Enterprise Subordinate Certificate Authority
      - CA Name: "AJF8729 BETA LAB SIGNING CA"
      - CDP/AIA Location: [http://pki.beta.ajf8729.com/CertEnroll/](http://pki.beta.ajf8729.com/CertEnroll/)
    - Certificate Authority Web Enrollment
  - Active Directory Domain Services
  - Azure AD Connect (2.1.15.0)
  - DHCP Server
  - DNS Server

## CM01.beta.ajf8729.com

- Windows Server 2022 Datacenter
- 172.30.3.3/24
- Roles
  - ConfigMgr Standalone Primary Site (TP1) - Version 2207 (5.00.9085.1000)
    - Data Warehouse Service Point
    - Distribution Point
    - Endpoint Protection Point
    - Fallback Status Point
    - Management Point
    - Reporting Services Point
    - Service Connection Point
    - Site Database Server
    - SMS Provider
    - Software Update Point
  - Patch My PC Publishing Service (2.1.6.0)
  - Power BI Report Server (May 2022)
  - SQL Server 2019 Standard (15.0.4236.7)
  - Windows 11 ADK 21H2 (10.1.22000.1)
