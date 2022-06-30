# Summary

- Single Active Directory Forest/Domain (ad.ajf8729.com)
- Synchronized to Azure AD (ajf8729.onmicrosoft.com)
- ConfigMgr Standalone Primary Site
  - HTTPS-Only Mode

# Hosts

## ADDC01A.ad.ajf8729.com

- Windows Server 2022 Datacenter
- 172.30.1.2/24
- Roles
  - Active Directory Domain Services
  - DFS Namespace Server
  - DNS Server

## ADDC02.ad.ajf8729.com

- Windows Server 2022 Datacenter
- 172.30.1.3/24
- Roles
  - Active Directory Domain Services
  - Azure AD Application Proxy Connector
  - Azure AD Connect (2.1.1.0)
  - DFS Namespace Server
  - DNS Server
  - DHCP Server
  - Intune Connector for Active Directory

## ADCM01.ad.ajf8729.com

- Windows Server 2019 Datacenter
- 172.30.1.5/24
- Roles
  - ConfigMgr Primary Site (PS1) - Version 2203 (5.00.9078.1025)
    - Data Warehouse Service Point
    - Endpoint Protection Point
    - Service Connection Point
    - Site Database Server
    - Site Server
    - SMS Provider
  - SQL Server 2019 Standard (15.0.4236.7)
  - Windows 11 ADK 22H2 (10.1.22621.1)

## ADCA02.ad.ajf8729.com

- Windows Server 2022 Datacenter
- 172.30.1.7/24
- Alternative Hostnames
  - PKI.ad.ajf8729.com
- Roles
  - Active Directory Certificate Services
    - Enterprise Subordinate Certificate Authority
      - CA Name: "AJF8729 AD SIGNING CA"
      - CDP/AIA Location: [http://pki.ad.ajf8729.com/CertEnroll/](http://pki.ad.ajf8729.com/CertEnroll/)
    - Certificate Authority Web Enrollment
  - Intune Certificate Connector

## ADCM02.ad.ajf8729.com

- Windows Server 2019 Datacenter
- 172.30.1.10/24
- Roles
  - ConfigMgr Primary Site (PS1) - Version 2203 (5.00.9078.1025)
    - Cloud Management Gateway Connection Point
      - CMG: ajf8729cmg.ajf8729.com
    - Distribution Point
    - Fallback Status Point
    - Management Point
    - Reporting Services Point
    - Software Update Point
    - State Migration Point
  - Patch My PC Publishing Service (2.1.6.0)
  - Power BI Report Server (May 2022)
