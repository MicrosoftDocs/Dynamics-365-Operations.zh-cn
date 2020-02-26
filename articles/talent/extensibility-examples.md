---
title: 通过 Power Apps 和 Power Automate 扩展 Talent
description: 本文介绍 Microsoft Dynamics 365 Talent - Attract 的一些使用 Microsoft Power Apps 和 Microsoft Power Automate 的可扩展性方案示例。
author: negudava
manager: Annbe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: Dynamics 365 Talent;PowerApps;Flow;Common Data Service
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent;Core;Experience Apps
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 1051fa4db16bb94cc9d60a91fc3637d7e5305cc2
ms.sourcegitcommit: 13c4a6f98ccce243d6befde90992aefcf562bdab
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2020
ms.locfileid: "3029903"
---
# <a name="extend-talent-with-power-apps-and-power-automate"></a>通过 Power Apps 和 Power Automate 扩展 Talent

本文介绍 Microsoft Dynamics 365 Talent: Attract 的一些使用 Microsoft Power Apps 和 Microsoft Power Automate 的可扩展性方案示例。 可以将与各示例关联的解决方案包导入到您的 Power Apps 环境中。 然后可以将这些包用作指南或起点来实施适用于贵组织的方案。

> [!IMPORTANT]
> 如果要“照原样”使用本文中介绍的模板和应用，请务必测试这些模板和应用，以确保其涵盖特定于您的实施的所有方案。


## <a name="prerequisites"></a>先决条件

- 若要导入包，用户必须具有**环境制造者**权限。
- 若要导出或导入应用，用户必须拥有 Power Apps 计划 2 许可证或 Power Apps 计划 2 试用许可证。

## <a name="power-automate--form-connect"></a>Power Automate – 表连接

**Power Automate – 表连接**模板可用于从 Microsoft Forms 读取数据并存储到 Common Data Service 实体中。

可扩展此模板，以使其可用于其他方案。 下面举了一些示例加以说明：

- 捕获应聘者评估。
- 捕获课程调查表的结果。
- 为人力资源 (HR) 管理员编译面试问题库。
- 捕获应聘者的面试流程评估

在 Microsoft Dynamics 365: Attract 中，可以使用应聘者门户中的窗体，应聘者将在其中填写详细信息。 也可以将窗体作为活动嵌入到工作模板中。

应聘者提交窗体时，Microsoft Power Automate 捕获窗体提交，读取数据，然后将其存储到 Common Data Service 实体中。

若要下载 **Power Automate – 表连接**模板和自定义实体结构，请转至 Microsoft 下载中心中的 [Power Automate – 表连接](https://go.microsoft.com/fwlink/?linkid=2081988)。

## <a name="power-automate--sharepoint-integration"></a>Power Automate – SharePoint 集成

**Power Automate – SharePoint 集成**模板可用于从 Microsoft SharePoint 列表读取数据，将该列表与任何 Common Data Service 实体的字段值进行比较，以及将比较结果以通知电子邮件的形式发送。 

组织可能有一组急需的技能。 这些技能可以以 SharePoint 列表的形式存储在 SharePoint 中。 当应聘者申请列出了一组必需技能的任何工作时，如果应聘者的技能与 SharePoint 中存储的技能之间匹配度极高，将发送通知电子邮件。 这有助于更快填充急需职位，因为通知会帮助招聘人员联系应聘者和在整个组织中交叉招聘应聘者。

可扩展此模板，以便其可用于涉及 SharePoint 集成的任何方案。

若要下载 **Power Automate – SharePoint 集成**模板，请转到 Microsoft 下载中心中的 [Power Automate – SharePoint 集成](https://go.microsoft.com/fwlink/?linkid=2082109)。

## <a name="referral-app"></a>Referral 应用

您可以使用 Referral 应用将应聘者添加到共享人才池。 引荐人在提交应聘者时可以输入**名字**、**姓氏**、**电子邮件**和 **LinkedIn URL**。 应聘者源元数据然后会使用引荐人的信息填充。

您可以将此应用嵌入到员工自助服务中来提交引荐，或者可以将其用作企业门户中的超链接，也可以作为独立应用运行。

要下载 **Referral 应用**，在 Microsoft 下载中心转到 [Dynamics 365 Talent 可扩展性解决方案：Referral 应用](https://www.microsoft.com/download/details.aspx?id=58497)。 您可以导入此应用并对其进行自定义来添加其他功能。

## <a name="additional-resources"></a>其他资源

[该 Microsoft Power Platform](https://docs.microsoft.com/power-platform/admin/admin-documentation)</br>
[在租户与环境之间迁移应用](https://docs.microsoft.com/power-platform/admin/environment-and-tenant-migration)
