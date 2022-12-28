---
title: 优化年终结算
description: 本文介绍可用于总帐年终结算流程的优化年终结算服务加载项。
author: moaamer
ms.date: 12/02/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerClosingSheet
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2022-11-28
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: bc6ab7e36f37707442f8d5d5b6e0d5f5d42e2171
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831521"
---
# <a name="optimize-year-end-close"></a>优化年终结算 

Microsoft Dynamics 365 Finance 的优化年终结算服务加载项让年终结算处理能够在 Dynamics 365 Finance 资源的应用程序对象服务器 (AOS) 实例之外运行。 它使用微服务技术。 与优化年终结算功能相关的好处包括提高了性能，并将年终结算处理期间对 SQL 数据库的影响降到最低。

>[!NOTE]
> Microsoft Dynamics 365 Finance 10.0.31 版本提供优化年终结算功能。 此功能已反向移植到 Dynamics Finance 版本 10.0.30 和 10.0.29，您需要进行最新的质量更新。   

要使用优化年终结算功能，您必须完成以下任务：

1. 在 Microsoft Dynamics Lifecycle Service 中的项目中安装优化年终结算服务加载项。
2. 在功能管理中启用 **优化年终结算** 功能。

> [!NOTE]
> 在功能管理中禁用 **优化年终结算** 功能后，您仍然可以对 Finance 使用当前的年终结算功能。

## <a name="improved-performance"></a>性能提升

**优化年终结算** 功能用于加快年终结算处理，特别是对于有大量数据的客户。 在服务上运行年终结算时，繁重的处理将从 Finance 资源卸载，以帮助减少处理时间，释放可能影响其他用户日常运营的资源。

**优化年终结算** 功能可以帮助您实现以下目标：

- 通过减少运行时来提高年终结算的性能。
- 减少年终结算运行期间对其他流程的影响。
- 改进年终结果的报告和调整，因为年终结算运行所需的时间更少。

## <a name="new-options-and-visibility"></a>新选项和可见性

启用 **优化年终结算** 功能时，将在以下位置添加 **结果** 和 **状态** 两个新列：

- 在 **年终结算** 页面
- 在 **年终结算结果** 对话框中
- 在 **年末结算模板** 页面上的 **资产负债表财务维度转移** 选项中

下图显示了 **年终结算** 页面上 **结果** 和 **状态** 列的示例。 您可以在 **结果** 列中选择 **查看结果** 链接打开年终结算的结果。 **状态** 列显示年终结算流程的当前状态。 因此，新列提供了对年终结算流程进度的可见性。

[![年终结算页面上的结果和状态列。](./media/Optimize-year-end-close-Image3.png)](./media/Optimize-year-end-close-Image3.png)

此外，当启用 **优化年终结算** 功能时，**资产负债表财务维度** 快速选项卡将在 **年终结算模板** 页面上可用。 进行年终结算时，您可以使用此快速选项卡详细指定资产负债表财务维度。 此功能与已经对损益帐户可用的功能类似。

[![资产负债表财务维度快速选项卡。](./media/Optimize-year-end-close-Image4.png)](./media/Optimize-year-end-close-Image4.png)

## <a name="architecture-and-data-flow"></a>体系结构和数据流

要使用 **优化年终结算** 功能并在微服务上运行年终结算，您必须从 Lifecycle Services 安装 **优化年终结算服务加载项**，然后在功能管理中启用 **优化年终结算** 功能。

如下图所示，年终结算处理验证加载项是否已安装，以及功能是否已启用。 如果这两个先决条件均满足，将在微服务上运行年终结算。

[![数据流图。](./media/Optimize-year-end-close-Image5.png)](./media/Optimize-year-end-close-Image5.png)

## <a name="high-level-flow-for-year-end-close-processing"></a>年终结算处理的高级流

1. 年终结算流程从 Finance 中开始，请转到 **总帐 \> 期间结算 \> 年终结算**。 此流程为正在结算的法人创建结算批处理作业和任务。
2. 年终结算确定年终结算是应该在微服务上运行还是按照当前结算逻辑运行。

    - 如果在 Lifecycle Services 中安装了 **优化年终结算服务加载项**，并且在功能管理中启用了 **优化年终结算** 功能，年终结算将在微服务上运行。

        1. 优化年终结算功能为每个正在结算的法人创建年终结算服务作业，然后运行年终结算逻辑。 微服务执行年终结算。
        2. Finance 会侦听微服务上的年终结算，以确定微服务何时完成。 年终结算结果随后会在 Finance 中的 **年终结算** 页面更新。

    - 否则，年终结算将按照当前结算逻辑运行。
