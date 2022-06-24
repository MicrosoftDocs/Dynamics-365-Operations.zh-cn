---
title: 2021 年 11 月 19 日 Dynamics 365 Human Resources 中的新增功能或更改
description: 本文介绍 2021 年 11 月 19 日独立 Microsoft Dynamics 365 Human Resources 中的新增或更改的功能。
author: marcelbf
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-12-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d3e08432a4ce4d73cd67ad839191abe9f6e691a6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886064"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-november-19-2021"></a>2021 年 11 月 19 日 Dynamics 365 Human Resources 中的新增功能或更改

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本文介绍 Microsoft Dynamics 365 Human Resources 中的新增、更改或即将推出的功能。

有关更新流程和计划的详细信息，请参阅[更新流程](hr-admin-setup-update-process.md)。

有关新功能及其预计的正式发布日期的详细信息，请参阅 [Dynamics 365 Human Resources 2021 年发布第 2 波](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)。

## <a name="in-this-release"></a>在此发布中

此版本中包含以下 bug 修复。 更改适用于内部版本号 8.1.4591。

### <a name="bug-fixes"></a>缺陷修复

此发布中包含以下缺陷修复。

> [!NOTE]
> 我们的目标是尽快为您提供此信息。 我们可能会更新本文，以包含在最初发布本文之后将其纳入内部版本的缺陷修复。

| 问题编号 | 问题 | Description |
|---|---|---|
| 626178 | **经理自助服务** 中的工作人员磁贴缺少导航 | 此问题现已修复。 导航已可用，可在 **经理自助服务** 中查看报表详细信息。 |
| 632573 | 保存 **课程** 时没有验证错误 | 此问题现已修复。 当创建 **最小参与者人数** 大于 0 的课程时，即使 **最大参与者人数** 为 0，仍然允许保存。 |
| 615955 | 创建新的招聘请求位置时，出现错误“必须填写 **目的** 字段”。 | 为新的招聘请求位置创建地址时，您会收到错误：“必须填写‘目的’字段。” 但是，页面上没有 **目的** 字段。 |
| 620797 | 空白 **性别** 字段错误具有误导性 | 如果没有为个人联系人输入性别，报表会显示“单击或点击此处输入文本”– 这是一种误导，因为此字段中无法输入任何内容。 |
| 620800 | 福利报表链接被隐藏 | 默认情况下，在 **员工自助服务** 中无法查看福利报表。  已在 **链接** 部分下的 **员工自助服务** 右侧添加了一个链接 |
| 629778 | CDS 集成的性能问题。 | 与授权相关的请求导致性能问题。 |

## <a name="in-preview"></a>预览模式

以下新功能处于预览状态。 有关如何开启或关闭的详细信息，请参阅[管理功能](hr-admin-manage-features.md)。

| 功能 | 发布计划 | 文档 |
|---|---|---|
| 福利管理工作区 | [福利管理工作区（预览）](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [福利管理工作区](hr-benefits-management-workspace.md) |


## <a name="coming-soon"></a>即将推出
有关计划功能及其计划发布的完整列表，请参阅 [Dynamics 365 和行业云：2021 年发布第 2 波](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)。

[!INCLUDE[footer-include](../includes/footer-banner.md)]
