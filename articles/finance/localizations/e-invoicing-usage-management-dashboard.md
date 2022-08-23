---
title: 使用情况管理仪表板
description: 本文说明如何通过使用情况管理仪表板监视电子开票服务的使用情况并保持合规性。
author: gionoder
ms.date: 06/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.custom: 97423
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 74f3d88faf192474c177da971a9f7bb0e58e1279
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272200"
---
# <a name="usage-management-dashboard"></a>使用情况管理仪表板

[!include [banner](../includes/banner.md)]

**使用情况管理** 仪表板帮助您监视电子开票服务的使用情况，从而帮助您的组织在其每月使用情况方面保持合规性。 通过计算提交量并将其与获取的提交量进行比较来确定获取量和使用量之间的任何偏差，从而确定合规性。

仪表板包括以下指标：

- 一个成本指标，可用于出于许可合规性目的监视消耗量：

    - 每月使用情况(导出)

- 三个运营指标，可用于出于管理目的跟踪电子开票服务的使用情况：

    - 按功能排列的使用情况
    - 按环境排列的使用情况
    - 每月使用情况(导入)

## <a name="measurement-scope"></a>度量范围

- 度量单位： 

    **使用情况管理** 仪表板计入业务单据的提交和导入的电子发票。

- 组织: 

    计数由您的组织的租户 ID 汇总，而不管 Microsoft Dynamics 365 Finance 或 Dynamics 365 Supply Chain Management 的实例数或启用电子开票服务的法人数。


## <a name="indicator-usage-per-month-export"></a>指标：每月使用情况（导出）

此指标提供有关您的组织在定义期间发出的电子发票的详细信息。

### <a name="scope"></a>范围
- 从 Finance 和 Supply Chain Management 提交到电子开票服务的业务单据数，而不管这些业务单据包含的行数。
- 由电子开票服务成功处理的已提交业务单据数。 当在功能设置中定义的操作流完成时，将单据视为已成功处理。

> [!NOTE]
> 当电子发票提交到外部 Web 服务时，计入与 Web 服务处理的结果（接受、拒绝或架构验证错误）无关。 如果 Web 服务收到并响应来自电子开票服务的请求，将提交视为有效计数。

- **例外：** 如果将业务单据从 Finance 和 Supply Chain Management 重新提交到电子开票服务（例如，在需要重新提交相同的业务单据以更改电子发票状态的情况下），将不计入业务单据。 例如，巴西电子发票（会计单据）的开具将计入为有效，但在请求取消时不计入。


### <a name="calculation"></a>计算

余额的计算方法如下：

余额 = 免费 + 已采购 - 已使用

其中：

- 免费：
  
    客户每月可以免费提交的业务单据量。 它包括可提交给电子开票服务的 100 个业务单据包。 免费量不会累积，任何剩余余额都不会转入下一个期间。
  
- 已采购：
  
    可提交给电子开票服务的 1,000 个业务单据包。 必须每月为您的组织购买此包。 购买量不会累积，任何剩余余额都不会转入下一个期间。
  
- 已使用： 

    根据定义的条件提交到电子开票服务的业务单据的计数。
   
> [!IMPORTANT]
> 如果您的组织计划超过每月的 100 个免费提交量，请购买峰值量以确保您始终遵守 Microsoft 电子开票服务许可策略。
>
> 目前，必须根据购置日期手动输入购买量，以作为 1,000 个提交的多个包。

## <a name="indicator-usage-by-feature"></a>指标：按功能排列的使用情况

该指标显示在定义的时间段内用于开具电子发票的电子开票功能的使用情况。

- 计算：
  
    已使用 = 在向电子开票服务提交业务单据期间使用的每个电子开票功能的次数。

## <a name="indicator-usage-by-environment"></a>指标：按环境排列的使用情况

该指标显示在定义的时间段内电子开票服务环境的使用情况。

- 计算：
    
    已使用 = 在向电子开票服务提交业务单据期间使用的每个电子开票服务环境的次数。

## <a name="indicator-usage-per-month-import"></a>指标：每月使用情况（导入）

该指标显示在定义的时间段内通过电子开票服务将电子发票导入 Finance 和 Supply Chain Management 的数量。

- 范围：

    导入 Finance 和 Supply Chain Management 的电子发票，无论这些电子发票包含多少行。

- 计算：

    已接收 = 导入 Finance 和 Supply Chain Management 中的电子发票计数。

## <a name="functions"></a>功能
### <a name="purchase"></a>采购

在 **每月使用情况（导出）** 选项卡上，选择 **购买** 以手动登记获取的提交量。

对于给定的日期，选择 **新建**，然后输入针对该日期获取的 **包** 数。

按如下所示计算 **数量**：

数量 = 包 * 1.000

计算的 **数量** 反映在指标 **每月使用情况（导出）** 的 **已采购** 中。

### <a name="update"></a>更新

在操作窗格上，选择 **更新** 以刷新计算并更新页面和图表中显示的数据。

### <a name="reset-history-data"></a>重置历史记录数据

在操作窗格上，选择 **重置历史数据** 以刷新从中计算指标的数据库。




> [!NOTE]
> **使用情况管理** 仪表板不显示货币金额。 相反，它仅显示计数的提交和导入的单据的数量。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
