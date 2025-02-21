---
title: "URL Reservations for Multi-Instance Report Server Deployments"
description: "URL Reservations for Multi-Instance Report Server Deployments"
author: maggiesMSFT
ms.author: maggies
ms.date: 05/18/2016
ms.service: reporting-services
ms.topic: conceptual
helpviewer_keywords:
  - "URL reservations"
---
# URL Reservations for Multi-Instance Report Server Deployments
  If you install multiple instances of [!INCLUDE[ssRSnoversion](../../includes/ssrsnoversion-md.md)] on the same computer, you must consider how you will define the URL reservations for each instance. Within each instance, the Report Server Web service and the [!INCLUDE[ssRSWebPortal](../../includes/ssrswebportal.md)] must have at least one URL reservation each. The entire set of reservations must be unique in HTTP.SYS.  
  
 Duplicate URLs are detected during URL registration, which occurs when the service starts. If you create URL reservations that are not unique, the name conflict might not be detected until you start the service. For this reason, make sure that you follow naming conventions or rules to ensure all values are unique.  
  
## Default Naming Conventions  
 [!INCLUDE[ssRSnoversion](../../includes/ssrsnoversion-md.md)] can be installed within a [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] named instance. When you install or configure a report server within a named instance, the instance name is automatically included in the virtual directory in the default URL reservation that [!INCLUDE[ssRSnoversion](../../includes/ssrsnoversion-md.md)] provides. The following table shows the URL reservations for a default instance and a named instance.  
  
|SQL Server Instance|Default URL Reservation|  
|-------------------------|-----------------------------|  
|Default (MSSQLServer)|`https://+:80/reportserver`|  
|Named (MynamedInstance)|`https://+:80/reportserver_MyNamedInstance`|  
  
 For the named instance, the virtual directory includes the instance name. Both the default instance and the named instance listen on the same port, but the unique virtual directory names determine which report server gets the request.  
  
 Best practice recommendations are to use the virtual directory name to distinguish among the report server instance. It provides a clear correspondence between a URL and the target instance, and ensures that the application names are unique across the whole system.  
  
## Custom Naming Conventions  
 Although using the instance name is recommended, you can use the URL syntax and your own naming conventions to meet the unique name constraints for URL reservations. The following examples illustrate different approaches for creating unique URLs for each instance.  
  
|Report Server default instance (MSSQLSERVER)|ReportServer_MyNamedInstance|Uniqueness|  
|----------------------------------------------------|-----------------------------------|----------------|  
|`https://+:80/reportserver`|`https://+:8888/reportserver`|Each instance listens on a different port.|  
|`https://www.contoso.com/reportserver`|`https://SRVR-46/reportserver`|Each instance responds to different server names (fully qualified domain name, and machine name).|  
  
## Uniqueness Requirements  
 The underlying technologies used by [!INCLUDE[ssRSnoversion](../../includes/ssrsnoversion-md.md)] impose requirements around unique names. HTTP.SYS requires that all URLs within its repository be unique. You can vary the port, host name, or virtual directory name to create a unique URL. [!INCLUDE[vstecasp](../../includes/vstecasp-md.md)] requires that application identities be unique within the same process. This requirement affects the virtual directory names. It specifies that you cannot duplicate a virtual directory name within the same report server instance.  
  
## See Also  
 [Configure Report Server URLs  &#40;Report Server Configuration Manager&#41;](../../reporting-services/install-windows/configure-report-server-urls-ssrs-configuration-manager.md)   
 [Configure a URL  &#40;Report Server Configuration Manager&#41;](../../reporting-services/install-windows/configure-a-url-ssrs-configuration-manager.md)  
  
  
