---
title: 分析报告疑难解答
description: 本文说明如果客户的数据更改不出现在任何客户的工作区时该怎么做。
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d4e76f3b6231b6f307173fa176360daf775c8a7950bc4ab2f2162c768102c369
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6717406"
---
# <a name="troubleshoot-analytic-reports"></a>分析报告疑难解答

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**发货**

客户的数据更改不出现在任何客户的工作区的 **分析** 选项卡。

**原因**

默认情况下，Microsoft Power BI 报表根据部署度量批处理作业的计划每四小时刷新一次。

**分辨率**

此问题可能只是时间问题。 请执行以下步骤开始批处理作业并更新分析工作区。

1. 在 **系统管理 \> 链接 \> 批处理作业 \> 批处理作业** 打开 **批处理作业** 页。 或者，使用“搜索”，输入 **批处理作业**。
1. 在列表中查找 **部署度量** 作业。
1. 选择该页顶部的 **编辑**，将计划的开始日期/时间设置为将刷新更接近当前时间的分析的值。

![批处理作业。](media/batch-jobs.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]