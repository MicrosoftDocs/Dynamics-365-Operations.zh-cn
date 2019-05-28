---
title: Project Timesheet 移动应用程序
description: 本主题提供有关 Microsoft Dynamics 365 Project Timesheet 移动应用程序的信息。 用户可使用 Project Timesheet 移动应用在自己的移动设备上提交和审核项目的工时单。
author: abruer
manager: AnnBe
ms.date: 04/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: josaw1
ms.dyn365.ops.version: 10
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: a475085001b8fa10814c864ef35129eb6ebfdfef
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/07/2019
ms.locfileid: "1529871"
---
# <a name="microsoft-dynamics-365-project-timesheet-mobile-application"></a>Microsoft Dynamics 365 Project Timesheet 移动应用程序

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>概览

用户可使用 Microsoft Dynamics 365 Project Timesheet 移动应用在自己的移动设备（iPhone 或 Android）上提交和审核项目的工时单。 这款移动应用提供 Microsoft Dynamics 365 for Finance and Operations 的“项目管理与核算”区域中的工时单功能，并可用于及时录入和审核项目工时单。

## <a name="download-and-install-the-mobile-app"></a>下载并安装移动应用

从您的设备的移动商店下载并安装适用于 Android 或 iPhone 的 Microsoft Dynamics 365 Project Timesheet 移动应用。

## <a name="enable-the-app"></a>启用此应用 

必须在 Dynamics 365 for Finance and Operations 中启用 Project Timesheet 移动应用。 若要启用该功能，请转到**项目管理与核算参数 \> 工时单**，然后选择**启用 Microsoft Dynamics 365 Project Timesheet** 参数。

## <a name="sign-in-to-the-app"></a>登录该应用

1.  在移动设备上启动应用程序。

2.  输入您的 Microsoft Dynamics 365 for Finance and Operations URL。

3.  首次登录时，将提示您输入您的用户名和密码。 输入凭据。

4.  您将登录到自己的默认公司。

## <a name="submit-a-project-timesheet"></a>提交项目工时单

可以在该应用中创建和提交项目工时单。 新工时单可以基于以前工时单、保存的行或项目分配中的信息。 如果指定为委托人，则您还可以输入其他工作人员的工时单。 若要以委托人的身份创建工时单，请选择**菜单**按钮，然后选择资源名称。

工时单页面将基于当前日期为工时单期间创建新的工时单。 将显示工作周。 如果工时单阶段包括多个星期，您可以从工作周选项卡选择其他工作周。
如果当前日期有工作单，将显示该工作单。 如果需要在其他工时单期间创建新的工时单，请选择**菜单**按钮，然后选择**新工时单**。

可以通过单击**添加时间**操作或**从以下来源复制时间**操作输入项目信息。 **从以下来源复制时间**操作将复制项目行信息，但不复制工时。 **从以下来源复制时间**菜单包括以下选项：

- **从现有工时单复制** - 从现有的工时单中复制工时单行。

- **从收藏夹复制** – 通过使用工时单设置创建您选中的新工时单行作为收藏夹。

- **从分配复制** -从分配的项目复制新工时单行。

显示的项目信息依赖于在**项目管理与核算参数**页面中定义的移动参数。

在**法人**字段中，选择用于执行项目工作的法人。 **法人**字段仅在为法人启用了内部公司工时单支持时可用。

选择与工时单的项目关联的客户。 Android 上的初始版本不支持客户录入，因为必须先选择项目。 如果先选择了项目，将自动填充**客户**字段。

在**项目**字段中，选择您要为其输入时间的项目。 系统将自动用**客户**字段。

可通过客户和项目查找同时在客户和项目中进行搜索。

根据需要在**类别**、**活动**、**行属性**、**销售税组**和**销售税(物料)组**字段中选择信息。 可以替换这些字段。

将根据项目管理与核算参数把**行属性**字段设置为默认值。 如果启用了项目/类别和项目/资源参数，将把**行属性**值设置为您为此项验证定义的默认值。 如果未启用项目/类别和类别/资源参数，**行属性**值将根据**项目管理与核算参数**页面中的**启用默认行属性**字段采用默认值。 可以替换**行属性**值。

选择一天以添加时间。 输入您每天工作的工时数。

若要添加有关输入的工时的注释，请单击**添加注释**，然后输入内部读者和/或客户读者的注释。
内部注释可以按项目经理查看。 发票中包含客户注释。

若要保存该行作为收藏，请选中复选框，然后单击**另存为收藏夹**。

移动应用程序中不提供财务维度和附件支持。

请根据需要继续添加项目行以完成工时单。

单击**提交**发送工时单到审核工作流。

## <a name="review-timesheets"></a>复查工时单

菜单中将提供需要复查的工时单列表。 仅当已将您指定为工作流审批人，此选项才可用。 同时支持审核标题和行。 可通过行级别审核将一个或多个行设置为要审核。 复查工时单信息之后，单击**审核**、**委托**或**退回**以继续执行工作流。
