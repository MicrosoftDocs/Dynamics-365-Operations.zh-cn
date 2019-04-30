---
title: 使用 PowerApps 和 Microsoft Flow 扩展 Talent - 示例方案
description: 本主题介绍 Microsoft Dynamics 365 for Talent 的一些使用 Microsoft PowerApps 和 Microsoft Flow 的可扩展性方案示例。
author: negudava
manager: Annbe
ms.date: 03/04/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: Dynamics 365 for Talent;PowerApps;Flow;Common Data Service
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent;Core;Experience Apps
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2019-03-04
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 0aa3578047b9397682a7039d0dbcc05cc1b167e4
ms.sourcegitcommit: 9796d022a8abf5c07abcdee6852ee34f06d2eb57
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/12/2019
ms.locfileid: "949912"
---
# <a name="extend-talent-by-using-powerapps-and-microsoft-flow---example-scenarios"></a>使用 PowerApps 和 Microsoft Flow 扩展 Talent - 示例方案

本主题介绍 Microsoft Dynamics 365 for Talent 的一些使用 Microsoft PowerApps 和 Microsoft Flow 的可扩展性方案示例。 可以将与各示例关联的解决方案包导入到您的 PowerApps 环境中。 然后可以将这些包用作指南或起点来实施适用于贵组织的方案。

> [!IMPORTANT]
> 如果要“照原样”使用本主题中介绍的模板和应用，请务必测试这些模板和应用，以确保其涵盖特定于您的实施的所有方案。


## <a name="prerequisites"></a>先决条件

- 若要导入包，用户必须具有**环境制造者**权限。
- 若要导出或导入应用，用户必须拥有 PowerApps 计划 2 许可证或 PowerApps 计划 2 试用许可证。

## <a name="flow--form-connect"></a>流 – 表连接

**流 – 表连接** 模板可用于从 Microsoft Forms 读取数据并存储到 Common Data Service 实体中。

可扩展此模板，以使其可用于其他方案。 下面举了一些示例加以说明：

- 捕获应聘者评估。
- 捕获课程调查表的结果。
- 为人力资源 (HR) 管理员编译面试问题库。
- 捕获应聘者的面试流程评估

在 Microsoft Dynamics 365: Attract 中，可以在应聘者门户中显示窗体，而应聘者可以填写详细信息。 也可以将窗体作为活动嵌入到工作模板中。

应聘者提交窗体时，Microsoft Flow 捕获窗体提交，读取数据，然后将其存储到 Common Data Service 实体中。

若要下载**流 – 表连接**模板和自定义实体结构，请转至 Microsoft 下载中心中的[流 – 表连接](https://go.microsoft.com/fwlink/?linkid=2081988)。

## <a name="initiate-and-extract-parameters-passed-to-powerapps"></a>启动和提取传递到 Powerapps 的参数

**启动和提取传递到 Powerapps 的参数**模板可用作任何特定于 Attract 的 PowerApps 方案的起点。 其中包含 Attract 传递的所有默认参数，如**工作申请**、**应聘者 ID** 和 **工作 ID**。

此模板可用于检索应聘者评估表，这样招聘经理就可以查看应聘者填写的评估。

可在 Attract 中将使用 PowerApps 创建的应用嵌入到工作模板内。

若要下载**启动和提取传递到 Powerapps 的参数**模板和自定义实体结构，请转到 Microsoft 下载中心中的[启动和提取传递到 Powerapps 的参数](https://go.microsoft.com/fwlink/?linkid=2081991)。

## <a name="integration-with-office-365"></a>与 Office 365 的集成

**与 Office 365 的集成**应用可用于从 Microsoft Office 365 为已登录用户提取团队信息。 它在 Talent 中提醒工作人员提取上班打卡和下班打卡详细信息和异常记录。 上班打卡和下班打卡详细信息存储在自定义的 Common Data Service 实体中。 假定这些详细信息是通过集成从第三方系统填写的。

可扩展此应用，以使其可用于其他方案。 例如，可用于显示团队休假信息、日历事件和团队特定的任何事件。

若要下载**与 Office 365 的的集成**应用和自定义实体结构，请转到 Microsoft 下载中心中的[与 Office 365 的集成](https://go.microsoft.com/fwlink/?linkid=2081787)。

## <a name="flow--email-notification"></a>流 – 电子邮件通知

**流 – 电子邮件通知**模板可用于电子邮件通知方案。 可用于在招聘流程任何阶段向招聘团队拒绝的应聘者触发通知电子邮件。

可扩展此模板以在整个招聘流程中跟踪对应聘者阶段的更改，以及向招聘团队和应聘者发送通知。

总之，对于 Common Data Service 中存储的实体，可以设置流程以发送有关 Core HR、Attract 或 Dynamics 365 Talent: Onboard 中发生的事件的通知。

若要下载**流 – 电子邮件通知**模板，请转到 Microsoft 下载中心中的[流 – 电子邮件通知](https://go.microsoft.com/fwlink/?linkid=2082103)。

## <a name="flow--sql-connect-and-execute"></a>流 – SQL 连接和执行

**流 – SQL 连接和执行**模板连接到 Microsoft SQL Server 并让 SQL 查询运行。

尽管此模板设计为读取和更新 SQL 表，但对其进行扩展，以便将其用于其他方案。 例如，可将其用于使用来自 SQL Server 的记录填充 Common Data Service 中的暂存表，以及通过使用来自 SQL Server 的增量推送定期同步暂存表。

若要下载**流 – SQL 连接和执行**模板和自定义实体结构，请转至 Microsoft 下载中心中的[流 – SQL 连接和执行](https://go.microsoft.com/fwlink/?linkid=2081789)。

## <a name="flow--sharepoint-integration"></a>流 – SharePoint 集成

**流 – SharePoint 集成**模板可用于从 Microsoft SharePoint 列表读取数据，将该列表与任何 Common Data Service 实体的字段值进行比较，以及将比较结果以通知电子邮件的形式发送。 

组织可能有一组急需的技能。 这些技能可以以 SharePoint 列表的形式存储在 SharePoint 中。 当应聘者申请列出了一组必需技能的任何工作时，如果应聘者的技能与 SharePoint 中存储的技能之间匹配度极高，将发送通知电子邮件。 这样，将更快填充急需职位，因为通知会帮助招聘人员联系应聘者和在整个组织中交叉招聘应聘者。

可扩展此模板，以便其可用于涉及 SharePoint 集成的任何方案。

若要下载**流 – SharePoint 集成**模板，请转到 Microsoft 下载中心中的[流 – SharePoint 集成](https://go.microsoft.com/fwlink/?linkid=2082109)。



## <a name="additional-resources"></a>其他资源

[该 Microsoft Power Platform](https://docs.microsoft.com/power-platform/admin/admin-documentation)

[在租户与环境之间迁移应用](https://docs.microsoft.com/en-us/power-platform/admin/environment-and-tenant-migration)
