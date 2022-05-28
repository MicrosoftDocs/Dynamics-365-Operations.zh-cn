---
title: 通过 Power Apps 和 Power Automate 扩展 Talent
description: 本文介绍 Microsoft Dynamics 365 Human Resources 的一些使用 Microsoft Power Apps 和 Microsoft Power Automate 的可扩展性方案示例。
author: negudava
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4036378ca70089a9978a9bf5fb48c058a2064cdc
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2022
ms.locfileid: "8689485"
---
# <a name="extend-with-power-apps-and-power-automate"></a>通过 Power Apps 和 Power Automate 扩展


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



本文介绍 Microsoft Dynamics 365 Human Resources 的一些使用 Microsoft Power Apps 和 Microsoft Power Automate 的可扩展性方案示例。 可以将与各示例关联的解决方案包导入到您的 Power Apps 环境中。 然后可以将这些包用作指南或起点来实施适用于贵组织的方案。

> [!IMPORTANT]
> 如果要“照原样”使用本主题中介绍的模板和应用，请务必测试这些模板和应用，以确保其涵盖特定于您的实施的所有方案。

## <a name="prerequisites"></a>先决条件

- 若要导入包，用户必须具有 **环境制造者** 权限。
- 若要导出或导入应用，用户必须拥有 Power Apps 计划 2 许可证或 Power Apps 计划 2 试用许可证。

## <a name="integration-with-microsoft-365-power-automate"></a>与 Microsoft 365 的集成 Power Automate

**与 Microsoft 365 的集成** 应用可用于从 Microsoft 365 为已登录用户提取团队信息。 它引用 Human Resources 中的工作人员来提取员工身份证明类型。 经理可以检查员工 ID 类型的到期日期。 如果员工 ID 类型即将到期，他们还可以发送电子邮件提醒。 Power Automate 与 Power Apps 集成来发送此提醒。 发送提醒后，确认将从 Power Automate 发送回 Power Apps。 身份证明类型包括驾照、护照和其他可接受的 ID 形式。

您可以扩展此应用来处理其他场景。 例如，可以使用它来显示团队休假信息、日历事件和团队特定的任何事件。

若要下载 **与 Microsoft 365 的集成 Power Automate** 应用，请转到 Microsoft 下载中心中的[与 Microsoft 365 的集成](https://go.microsoft.com/fwlink/?linkid=2081787)。

## <a name="power-automate--sql-connect-and-execute"></a>Power Automate – SQL 连接和执行

**Power Automate – SQL 连接和执行** 模板连接到 Microsoft SQL Server 并让 SQL 查询运行。

虽然此模板读取和更新 SQL 表，但是您可以对其进行扩展，然后将其用于其他场景。 例如，可将其用于使用来自 SQL Server 的记录填充 Dataverse 中的暂存表，以及通过使用来自 SQL Server 的增量推送定期同步暂存表。

“高级查询”已与 Flow 集成，以实现数据转换和增量推送。

若要下载 **Power Automate – SQL 连接和执行** 模板和自定义实体结构，请转至 Microsoft 下载中心中的 [Power Automate – SQL 连接和执行](https://go.microsoft.com/fwlink/?linkid=2081789)。

## <a name="additional-resources"></a>其他资源

[该 Microsoft Power Platform](/power-platform/admin/admin-documentation)</br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
