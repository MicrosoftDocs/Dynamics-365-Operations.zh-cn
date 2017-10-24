---
title: "为本地部署配置 SQL Server Reporting Services"
description: "本主题提供有关为本地部署配置 SQL Server Reporting Services (SSRS) 的信息。"
author: sarvanisathish
manager: AnnBe
ms.date: 06/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, UnifiedOperations
ms.custom: 55651
ms.assetid: 
ms.search.region: Global
ms.author: sarvanis
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 5ee1b93b92516e14e9581c3b2fe6a2527403ae1e
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="configure-sql-server-reporting-services-for-an-on-premises-deployment"></a>为本地部署配置 SQL Server Reporting Services

使用本主题中的步骤为你的 Microsoft Dynamics 365 for Finance and Operations Enterprise 版本（本地）部署配置 SQL Server Reporting Services (SSRS)。

1. 打开 Reporting Services 配置管理器应用程序。
2. 保留默认的**服务器名称**（这应是当前计算机的名称）和**报表服务器实例**，**MSSQLSERVER**。 
3. 单击**连接**。
   
   [![报表服务配置连接](./media/ssrs-config-manager-01.png)](./media/ssrs-config-manager-01.png)
   
4. 单击**服务帐户**选项卡并验证设置是否与以下图形匹配。

    [![服务帐户选项卡](./media/ssrs-config-manager-02.png)](./media/ssrs-config-manager-02.png)
    
5. 单击 **Web 服务 URL** 选项卡并验证设置是否与以下图形匹配。 

    [![Web 服务 URL 选项卡](./media/ssrs-config-manager-03.png)](./media/ssrs-config-manager-03.png) 
    
6. 单击**数据库**选项卡并验证**数据库名称**和**凭据设置**是否与以下图形匹配。 **注意：**你需要创建一个新的数据库。 为此，请单击**更改数据库**，然后验证新的数据库名称是否为：**DynamicsAxReportServer**。

    [![数据库选项卡](./media/ssrs-config-manager-04.png)](./media/ssrs-config-manager-04.png)
    
7. 单击 **Web 门户 URL** 选项卡并验证设置是否与以下图形匹配。 **注意：**你必须单击**应用**以创建和正确配置门户。

    [![Web 门户 URL 选项卡](./media/ssrs-config-manager-05.png)](./media/ssrs-config-manager-05.png)
    
  配置门户后，**Web 门户**选项卡将与以下图形匹配。
    [![Web 门户选项卡](./media/ssrs-config-manager-06.png)](./media/ssrs-config-manager-06.png)
    
8. 单击报表 URL 以查看 SQL Server Reporting Services Web 门户。 
9.  当你在该门户时，创建名为 **Dynamics** 的新文件夹。

    [![Dynamics 文件夹](./media/ssrs-config-manager-07.png)](./media/ssrs-config-manager-07.png)
    
10. 在 **Reporting Services 配置管理器**中，单击**电子邮件设置**选项卡并验证设置是否与以下图形匹配。

    [![电子邮件设置选项卡](./media/ssrs-config-manager-08.png)](./media/ssrs-config-manager-08.png)
    
11. 单击**执行帐户**选项卡并验证设置是否与以下图形匹配。

    [![执行帐户选项卡](./media/ssrs-config-manager-09.png)](./media/ssrs-config-manager-09.png)
    
  不要更改**加密密钥**选项卡上的默认设置。[![加密密钥选项卡](./media/ssrs-config-manager-10.png)](./media/ssrs-config-manager-10.png)
    
12. 单击**订阅设置**选项卡，并验证设置是否与以下图形匹配。

    [![订阅设置选项卡](./media/ssrs-config-manager-11.png)](./media/ssrs-config-manager-11.png)
    
  不要更改**扩大部署**选项卡上的默认设置。[![扩大部署选项卡](./media/ssrs-config-manager-12.png)](./media/ssrs-config-manager-12.png)
    
  不要更改 **Power BI 集成**选项卡上的默认设置。[![Power BI 集成选项卡](./media/ssrs-config-manager-13.png)](./media/ssrs-config-manager-13.png) 
    
13. 单击**退出**以关闭 **Reporting Services 配置管理器**。

    [![关闭 Reporting Services 配置管理器](./media/ssrs-config-manager-14.png)](./media/ssrs-config-manager-14.png)
    


