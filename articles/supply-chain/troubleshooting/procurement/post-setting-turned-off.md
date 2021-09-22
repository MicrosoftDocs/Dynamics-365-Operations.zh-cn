---
title: 不能打开“过帐到分类帐中的费用帐户”设置
description: 为采购订单开票时，如果启用“应付帐款参数”页面的“发票”选项卡上的“过帐到分类帐中的费用帐户”选项，将发生此问题
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 592444958dad4624fdc9098dc58df0a2e49e63de
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475708"
---
# <a name="the-post-to-charge-account-in-ledger-setting-isnt-turned-on"></a>不能打开“过帐到分类帐中的费用帐户”设置

## <a name="symptoms"></a>故障特征

为采购订单开票时，如果将 **应付帐款参数** 的 **发票** 选项卡上的 **过帐到分类帐中的费用帐户** 选项设置为 *是*，将发生此问题。

## <a name="reproduce-the-issue"></a>重现问题

以下过程显示了一种重现此问题的方法。

1. 转到 **应付帐款 \>设置 \> 应付帐款参数**。
1. 在 **发票** 选项卡上，将 **过帐到分类帐中的费用帐户** 选项设置为 *是*。
1. 转到 **库存管理 \> 设置 \> 过帐 \> 过帐**。
1. 在 **采购订单** 选项卡上，确保已删除产品的采购支出中的所有行。
1. 转到 **应付帐款 \> 采购订单 \> 所有采购订单**。
1. 创建采购订单。 在 **供应商帐户** 字段中，选择 *1001 Acme 办公设备*。
1. 添加具有以下设置的采购订单行：

    - **物料编号**：*D0011 激光投影仪*
    - **站点**：*1*
    - **仓库**：*11*
    - **数量：** *4*

1. 在操作窗格的 **采购** 选项卡上，在 **操作** 组中，选择 **确认**。
1. 在操作窗格的 **接收** 选项卡上，在 **生成** 组中，选择 **产品收货**。
1. 在 **过帐产品收货** 对话框中的 **产品收货** 字段中，输入任意数字，然后选择 **确定**。
1. 在操作窗格 **发票** 选项卡的 **常规** 组中，选择 **发票**。
1. 在 **编号** 字段中，输入任意数字作为发票编号。
1. 更新匹配状态，然后过帐。
1. 请注意，现在从采购订单生成发票时会收到以下错误：“产品的“采购支出”交易类型的科目编号不存在。”

## <a name="resolution"></a>解决方法

这取决于发票和发票组的参数设置。 有关详细信息，请参阅以下博客文章：[采购费用和库存变化的会计](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/12/15/accounting-for-purchase-charge-and-stock-variation/)。
