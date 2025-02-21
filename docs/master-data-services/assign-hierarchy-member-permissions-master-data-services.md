---
title: Assign Hierarchy Member Permissions
description: "Assign Hierarchy Member Permissions (Master Data Services)"
author: CordeliaGrey
ms.author: jiwang6
ms.date: "03/01/2017"
ms.service: sql
ms.subservice: master-data-services
ms.topic: conceptual
helpviewer_keywords:
  - "permissions [Master Data Services], assigning member permissions"
  - "members [Master Data Services], assigning permissions"
---
# Assign Hierarchy Member Permissions (Master Data Services)

[!INCLUDE [SQL Server - Windows only ASDBMI  ](../includes/applies-to-version/sql-windows-only-asdbmi.md)]

  Assign permissions to hierarchy members to give users or groups access to view data in the **Explorer** functional area of [!INCLUDE[ssMDSmdm](../includes/ssmdsmdm-md.md)].  
  
 Hierarchy member permissions are optional. They provide added granularity to model object permissions, which are required.  
  
## Prerequisites  
 To perform this procedure:  
  
-   You must have permission to access the **Users and Group Permissions** functional area.  
  
-   You must be a model administrator. For more information, see [Administrators &#40;Master Data Services&#41;](../master-data-services/administrators-master-data-services.md).  
  
### To assign hierarchy member permissions  
  
1.  In [!INCLUDE[ssMDSmdm](../includes/ssmdsmdm-md.md)], click **User and Group Permissions**.  
  
2.  On the **Users** or **Groups** page, select the row for the user or group that you want to edit.  
  
3.  Click **Edit selected user**.  
  
4.  Click the **Hierarchy Members** tab.  
  
5.  From the **Model** list, select a model.  
  
6.  From the **Version** list, select a version.  
  
7.  From the **Hierarchy** list, select a hierarchy.  
  
8.  Click **Edit**.  
  
9. Expand the tree, and click the hierarchy node you want to assign permissions to.  
  
10. From the menu, select a combination of **Create**, **Read,Update** and **Delete** permissions, or **Deny** permissions.  
  
11. Click **Save**.  
  
    > [!NOTE]  
    >  Hierarchy member permissions do not take effect immediately. See [Immediately Apply Member Permissions &#40;Master Data Services&#41;](../master-data-services/immediately-apply-member-permissions-master-data-services.md) for more information.  
  
## See Also  
 [Delete Hierarchy Member Permissions &#40;Master Data Services&#41;](../master-data-services/delete-hierarchy-member-permissions-master-data-services.md)   
 [Assign Model Object Permissions &#40;Master Data Services&#41;](../master-data-services/assign-model-object-permissions-master-data-services.md)   
 [Hierarchy Member Permissions &#40;Master Data Services&#41;](../master-data-services/hierarchy-member-permissions-master-data-services.md)  
  
  
