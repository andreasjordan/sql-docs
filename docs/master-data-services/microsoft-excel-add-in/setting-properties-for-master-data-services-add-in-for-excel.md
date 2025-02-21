---
title: Setting Properties
description: "Setting Properties for Master Data Services Add-in for Excel"
author: CordeliaGrey
ms.author: jiwang6
ms.date: "03/01/2017"
ms.service: sql
ms.subservice: master-data-services
ms.topic: conceptual
ms.custom: microsoft-excel-add-in
---
# Setting Properties for Master Data Services Add-in for Excel

[!INCLUDE [SQL Server Windows Only - ASDBMI ](../../includes/applies-to-version/sql-windows-only-asdbmi.md)]

  Master Data Services Add-in for Excel settings determine how data is loaded from MDS into the Excel Add-in and how data is published from the Excel Add-in into MDS.  
  
 To make settings for the Excel Add-in, open **Excel**, click the **Master Data** menu, and then click **Settings**. Anyone with access to Excel can change these settings. The settings apply to the computer that Excel is open on.  
  
## Excel Add-in Settings  
  
|Tab and Section|Setting|Description|  
|-|-|-|  
|Settings: Publishing|Show **Publish and Annotate** dialog box when publishing|Select to display the **Publish and Annotate** dialog box after you click **Publish**, enabling you to enter a single annotation for all changes or to enter an annotation for each change.<br /><br /> Deselect to specify that the Publish process is initiated without the **Publish and Annotate** dialog box being displayed. You will not have the opportunity to enter an annotation.|  
|Settings: Version|Version selection|Select the version of the master data that will be loaded into the Excel Add-in. Can be:<br /><br /> **None** to have the version not default to any version<br /><br /> **Oldest** to default to the oldest version **Newest** to default to the most recent version.|  
|Settings: Logging|Turn on detailed logging|Enable logging for the process of loading master data from MDS into the Excel Add-in, such that the  result of every command in the service is logged.|  
|Settings: Telemetry|Turn on telemetry data collection|Enable telemetry to help improve the quality, reliability and performance of [!INCLUDE[ssMDSshort](../../includes/ssmdsshort-md.md)] Excel Add-in.|  
|Settings: Batching size|Number of cells for load|Select a number to indicate how many thousands of cells will be loaded in a batch that is loaded from the MDS server to Excel. The default is 50,000 cells.|  
|Settings: Batching size|Number of cells for publish|Select a number to indicate how many thousands of cells will be published in a batch that is returned from Excel to the server. The default is 50,000 cells.|  
|Settings: Servers Added to Safe List|Clear All|Click to clear the list of connections that were designated as safe when the associated shortcut query file was opened.|  
|Data: Filters|Display filter warning for large data sets|Click to display a warning if the data set being loaded from MDS to Excel exceeds the maximum number of rows or columns.|  
|Data: Filters|Maximum rows|Select the threshold for the number of rows being loaded, beyond which a filter warning will be posted.|  
|Data: Filters|Maximum columns|Select the threshold for the number of columns being loaded, beyond which a filter warning will be posted.|  
|Data: Cell Format|Change the color when: Attribute values change|Click to specify that the color of a cell will be changed if the attribute value in that cell changes when you refresh the Excel Add-in table with new data from the MDS repository.|  
|Data: Cell Format|Change the color when: Members are added|Click to specify that the color of a row's cells will be changed if a new member is added to the row when you refresh the Excel Add-in table with new data from the MDS repository.|  
|Data: Cell Format|Display format|Select the preferred format for displaying values of domain-based attributes. The options are Code {Name}, Code, and Name {Code}.|  
  
  
