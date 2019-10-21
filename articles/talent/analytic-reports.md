---
title: 使用 Microsoft Dynamics 365 Talent - Attract 中的分析报表
description: 本主题介绍了 Microsoft Dynamics 365 Talent - Attract 中招聘流程见解的分析报表
author: fewatson
manager: AnnBe
ms.date: 04/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: fewatson
ms.search.validFrom: 2019-04-30
ms.dyn365.ops.version: Talent April 2019 update
ms.openlocfilehash: be62fe9a5021cfa83a465d316b182c0a154c0c50
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/23/2019
ms.locfileid: "2009996"
---
# <a name="use-analytic-reports"></a>使用分析报告

Microsoft Dynamics 365 Talent: Attract 中的分析报表提供现成的 (OOTB) 解决方案以获取招聘流程见解。 可用功能包括：

- **工作分析：** 单击工作类的**分析**选项卡可查看该工作的申请人的指标。
- **分析中心：** 单击左侧导航中的**分析**可查看工作的聚合指标。
- **用户特定安全性：** 对报表的访问由 Attract [角色](security-attract.md) 和工作参与者角色控制。
- **交叉筛选：** 单击报表内的视觉对象可查看按所选数据筛选的其他指标。

>[!NOTE] 
>- 此功能现在处于[预览](access-preview-feature.md)阶段。 若要尝试，必须安装[**综合招聘加载项**](attract-comprehensive-hiring.md)。
>- 所有公共预览报表均以英语显示。
>- 报表每隔 3 小时刷新。 上次刷新时间（本地时区内）位于报表顶部。 刷新次数为近似值，由数据量和您所在地区的资源负荷决定。

## <a name="job-analytics"></a>工作分析

工作分析报表提供工作招聘流程的快照。  关键指标包括：

- 有效申请人（按阶段）
- 申请人来源
- 申请人类型（内部或外部）

## <a name="analytics-hub"></a>分析中心

分析中心报表聚合工作数据以展示招聘流程的趋势。 Attract 中包含两种 OOTB 报表：管道汇总和漏斗图分析。

### <a name="pipeline-summary"></a>管道汇总

管道汇总报表聚合开放工作的数据。 关键指标包括：

- 所有工作的申请人（按阶段）
- 申请人来源
- 开放工作（按资历级别）

### <a name="funnel-analysis"></a>漏斗图分析

漏斗图分析报表聚合已作为已填充而关闭的工作的数据。 关键指标包括：

- 聘用时间
- 转换指标（不确定）
- 聘约接受率

注意：若需最精确的聘用时间报告，建议使用[聘约管理](offer-setup.md)，这是一项综合招聘加载项的一项功能。

>[!TIP] 
>可尝试将光标悬停在视觉对象上方以查看更多信息。 例如，将光标悬停在**有效的申请人**视觉对象上方将显示平均阶段天数。 分析此信息可提供对减少招聘时间至关重要的见解，并让招聘人员重点关注减少各阶段所用时间的方法。

## <a name="user-specific-security"></a>用户特定安全性

Attract 报表可供管理员、全部阅读、招聘人员和招聘经理[角色](security-attract.md)访问。 未分配的用户不能访问分析报表页面（工作分析或分析中心）。

工作分析报表显示所选工作的数据。 分析中心报表聚合用户可查看的所有工作的数据。 可查看“工作”页面上的“我的工作”和“所有工作”的用户在分析中心内的可用视图相同。

## <a name="cross-filter"></a>交叉筛选

Power BI 其中一项重要功能是报表页面中的所有视觉对象的互连方式。 如果选择其中一个视觉对象上的数据点，页面中包含该数据的其他所有视觉对象将根据所选内容变化。 有关详细信息及示例，请参阅 [Power BI 报告中视觉对象如何相互交叉筛选](https://docs.microsoft.com/power-bi/consumer/end-user-interactions)。

## <a name="export-to-excel"></a>导出至 Excel

若要使用 Excel 查看报表数据，可单击视觉对象上的选项菜单（三个点），然后选择**导出基础数据**。 导出的数据将按照 Attract 中的用户权限进行筛选。 有关详细信息，请参阅[从可视化项导出数据](https://docs.microsoft.com/power-bi/visuals/power-bi-visualization-export-data)。
