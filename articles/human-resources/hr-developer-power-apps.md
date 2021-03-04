---
title: 通过 Power Apps 和 Power Automate 扩展 Talent
description: 本文介绍 Microsoft Dynamics 365 Human Resources 的一些使用 Microsoft Power Apps 和 Microsoft Power Automate 的可扩展性方案示例。
author: negudava
manager: Annbe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core;Experience Apps;Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2e89347829ccd6569d568db42c79b5fea2316ba3
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527018"
---
# <a name="extend-with-power-apps-and-power-automate"></a>通过 Power Apps 和 Power Automate 扩展

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

本文介绍 Microsoft Dynamics 365 Human Resources 的一些使用 Microsoft Power Apps 和 Microsoft Power Automate 的可扩展性方案示例。 可以将与各示例关联的解决方案包导入到您的 Power Apps 环境中。 然后可以将这些包用作指南或起点来实施适用于贵组织的方案。

> [!IMPORTANT]
> 如果要“照原样”使用本主题中介绍的模板和应用，请务必测试这些模板和应用，以确保其涵盖特定于您的实施的所有方案。

## <a name="prerequisites"></a>先决条件

- 若要导入包，用户必须具有 **环境制造者** 权限。
- 若要导出或导入应用，用户必须拥有 Power Apps 计划 2 许可证或 Power Apps 计划 2 试用许可证。

## <a name="integration-with-microsoft-365-power-automate"></a>与 Microsoft 365 Power Automate 集成

**与 Microsoft 365 集成** 应用可用于从 Microsoft 365 为已登录用户提取团队信息。 它引用 Human Resources 中的工作人员来提取员工身份证明类型。 经理可以检查员工 ID 类型的到期日期。 如果员工 ID 类型即将到期，他们还可以发送电子邮件提醒。 Power Automate 与 Power Apps 集成来发送此提醒。 发送提醒后，确认将从 Power Automate 发送回 Power Apps。 身份证明类型包括驾照、护照和其他可接受的 ID 形式。

您可以扩展此应用来处理其他场景。 例如，可以使用它来显示团队休假信息、日历事件和团队特定的任何事件。

若要下载 **与 Microsoft 365 Power Automate 集成** 应用，请转到 Microsoft 下载中心中的[与 Microsoft 365 集成](https://go.microsoft.com/fwlink/?linkid=2081787)。

## <a name="power-automate--sql-connect-and-execute"></a>Power Automate – SQL 连接和执行

**Power Automate – SQL 连接和执行** 模板连接到 Microsoft SQL Server 并让 SQL 查询运行。

虽然此模板读取和更新 SQL 表，但是您可以对其进行扩展，然后将其用于其他场景。 例如，可将其用于使用来自 SQL Server 的记录填充 Common Data Service 中的暂存表，以及通过使用来自 SQL Server 的增量推送定期同步暂存表。

“高级查询”已与 Flow 集成，以实现数据转换和增量推送。

若要下载 **Power Automate – SQL 连接和执行** 模板和自定义实体结构，请转至 Microsoft 下载中心中的 [Power Automate – SQL 连接和执行](https://go.microsoft.com/fwlink/?linkid=2081789)。

## <a name="additional-resources"></a>其他资源

[该 Microsoft Power Platform](https://docs.microsoft.com/power-platform/admin/admin-documentation)</br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]