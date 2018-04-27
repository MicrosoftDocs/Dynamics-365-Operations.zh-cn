---
title: "固定资产管理工作区"
description: "此主题提供有关固定资产管理工作区的信息。 此工作区显示与在系统中输入的固定资产有关的信息。 它包含一个汇总视图和一个分析视图。"
author: saraschi2
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetWorkspace
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.assetid: 
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 8425387d4004e02e9b8adf9ba3b31a0b4e02b6e9
ms.contentlocale: zh-cn
ms.lasthandoff: 02/07/2018

---

# <a name="fixed-asset-management-workspace"></a>固定资产管理工作区

[!INCLUDE [banner](../includes/banner.md)]

**固定资产管理**工作区显示与在系统中输入的固定资产有关的信息。 该工作区包括一个汇总视图和一个分析视图。 **我的工作**选项卡显示汇总磁贴、固定资产详细信息和与当前公司中的固定资产有关的信息。 您还可以直接将分析添加到工作区中的 Power BI 分析部分。 **分析 - 所有公司**选项卡使用 Microsoft Power BI 的功能显示与所有公司中的固定资产有关的视觉对象。

## <a name="my-work"></a>我的工作

### <a name="summary"></a>汇总

**汇总**部分的磁贴提供您的固定资产的概览。 该信息包括与尚未购置的资产有关的指标、在当前年度期间购置的资产以及在当前年度期间已处置的资产。 **汇总**部分还可以快速导航到**固定资产**列表页、批次折旧方案和固定资产日记帐。

### <a name="find-fixed-assets"></a>查找固定资产

**查找固定资产**部分允许您通过提供固定资产编号、组、名称、位置或负责人快速搜索资产。 符合搜索条件的所有资产将显示在列表中。

从列表中，您可以查看以下页面：

 - 用于固定资产的**详细信息**页。
 - 用于与固定资产关联的所有帐簿的**帐簿**页
 - **估计资产估价**页

### <a name="valuations"></a>估价

**固定资产估价**页让您能够在一个页面上查看与固定资产有关的最重要的信息以及与固定资产关联的所有帐簿的详细信息。 页面左上方的**余额**选项显示与固定资产关联的每个帐簿的当前估价。 您可以从估值钻取以查看构成汇总值的详细的交易记录。 页面左上方的**模板**选项显示与固定资产关联的每个帐簿的折旧方案。

您可以从**固定资产管理**工作区或**固定资产**列表页访问**固定资产估价**页。

### <a name="related-information"></a>相关信息

您可以使用工作区**相关信息**部分中的链接直接导航到**帐簿设置**页、**固定资产交易记录查询**页和多个报表。

### <a name="analytics--all-companies"></a>分析 - 所有公司

**分析**页提供与系统中的所有法人中的固定资产有关的关键指标。 对此选项卡的访问权限受“查看所有公司安全权限的固定资产分析”的控制。

下表显示在每个报表页上可用的可视化项。

| 报表页            | 可视化        |
|------------------------|----------------------|
| 固定资产估价 | 帐面净值总计 |
| 固定资产估价 | 帐面净值（按固定资产组） |
| 固定资产估价 | 购置价格 |
| 固定资产估价 | 处置值 |
| 固定资产估价 | 固定资产明细 |
| 估价地图        | 帐面净值总计 |
| 估价地图        | 固定资产位置 |
| 估价地图        | 固定资产明细 |

若要查看带数据的分析，必须先刷新**实体商店**页的 AssetTransactionMeasure 聚合度量。

