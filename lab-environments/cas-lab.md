# Summary

- Single Active Directory Forest/Domain (cas.ajf8729.com)
- Synchronized to Azure AD (afontanez.onmicrosoft.com)
- ConfigMgr Central Administration Site + 2 Child Primary Sites
  - HTTPS-Only Mode

# Hosts

## CASDC01.cas.ajf8729.com

- Windows Server 2022 Datacenter
- 172.30.101.2/24
- Roles
  - Active Directory Domain Services
  - DNS Server

## ADSYNC01.cas.ajf8729.com

- Windows Server 2022 Datacenter
- 172.30.101.3/24
- Roles
  - Azure AD Connect (2.1.1.0)
  - DHCP Server

## CMCAS01.cas.ajf8729.com

- Windows Server 2019 Datacenter
- 172.30.101.4/24
- Roles
  - ConfigMgr Central Administration Site (CAS) - Version 2203 (5.00.9078.1025)
    - Data Warehouse Service Point
    - Endpoint Protection Point
    - Reporting Services Point
    - Service Connection Point
    - Site Database Server
    - Site Server
    - SMS Provider
    - Software Update Point
  - Patch My PC Publishing Service (2.1.6.0)
  - Power BI Report Server (May 2022)
  - SQL Server 2019 Standard (15.0.4236.7)
  - Windows ADK 2004 (10.1.19041.1)

## CMPSA01.cas.ajf8729.com

- Windows Server 2019 Datacenter
- 172.30.101.5/24
- Roles
  - ConfigMgr Primary Site (PSA) - Version 2203 (5.00.9078.1025)
    - Distribution Point
    - Management Point
    - Reporting Services Point
    - Site Database Server
    - Site Server
    - SMS Provider
    - Software Update Point
  - Power BI Report Server (May 2022)
  - SQL Server 2019 Standard (15.0.4236.7)

## CMPSB01.cas.ajf8729.com

- Windows Server 2019 Datacenter
- 172.30.101.6/24
- Roles
  - ConfigMgr Primary Site (PSB) - Version 2203 (5.00.9078.1025)
    - Distribution Point
    - Management Point
    - Reporting Services Point
    - Site Database Server
    - Site Server
    - SMS Provider
    - Software Update Point
  - Power BI Report Server (May 2022)
  - SQL Server 2019 Standard (15.0.4236.7)

## PKI01.cas.ajf8729.com

- Windows Server 2022 Datacenter
- 172.30.101.7/24
- Alternative Hostnames
  - PKI.cas.ajf8729.com
- Roles
  - Active Directory Certificate Services
    - Enterprise Subordinate Certificate Authority
      - CA Name: "AJF8729 CAS LAB SIGNING CA"
      - CDP/AIA Location: [http://pki.cas.ajf8729.com/CertEnroll/](http://pki.cas.ajf8729.com/CertEnroll/)
    - Certificate Authority Web Enrollment
