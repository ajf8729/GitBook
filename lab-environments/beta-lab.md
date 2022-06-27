# Summary

- Single Active Directory Forest/Domain (beta.ajf8729.com)
- Synchronized to Azure AD (ajf8729tplab.onmicrosoft.com)
- ConfigMgr Standalone Primary Site
  - Technical Preview Branch
  - HTTPS-Only Mode

# Hosts

## BETADC01A.beta.ajf8729.com

- Windows Server 2022 Datacenter
- 172.30.3.2/24
- Roles
  - Active Directory Domain Services
  - DHCP Server
  - DNS Server

## BETACM01.beta.ajf8729.com

- Windows Server 2022 Datacenter
- 172.30.3.3/24
- Roles
  - ConfigMgr Standalone Primary Site (BTA) - Version 2206 (5.00.9084.1000)
    - Cloud Management Gateway Connection Point
      - CMG: ajf8729betacmg.beta.ajf8729.com
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
    - State Migration Point
  - Patch My PC Publishing Service (2.1.6.0)
  - Power BI Report Server (May 2022)
  - SQL Server 2019 Standard (15.0.4236.7)
  - Windows 11 ADK 22H2 (10.1.22621.1)

## BETAADSYNC01.beta.ajf8729.com

- Windows Server 2022 Datacenter
- 172.30.3.4/24
- Roles
  - Azure AD Connect (2.1.1.0)
  - Intune Connector for Active Directory

## BETACA01.beta.ajf8729.com

- Windows Server 2022 Datacenter
- 172.30.3.5/24
- Alternative Hostnames
  - PKI.beta.ajf8729.com
- Roles
  - Active Directory Certificate Services
    - Enterprise Subordinate Certificate Authority
      - CA Name: "AJF8729 BETA SIGNING CA"
      - CDP/AIA Location: [http://pki.beta.ajf8729.com/CertEnroll/](http://pki.beta.ajf8729.com/CertEnroll/)
    - Certificate Authority Web Enrollment
  - Intune Certificate Connector

## BETADC02.beta.ajf8729.com

- Windows Server vNext Datacenter (25140)
- 172.30.3.6/24
- Roles
  - Active Directory Domain Services
  - DNS Server
