---
title: 创建销售税支付
description: 结算和过帐销售税作业过程结算销售税帐户的销售税余额，并冲销特定期间内的销售税结算帐户。
author: twheeloc
ms.date: 10/25/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 54132ca4775482b4a06ff7e73125e804aff40cb4
ms.sourcegitcommit: f8b597b09157d934b62bd5fb9a4d05b8f82b5a0e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/26/2021
ms.locfileid: "7700105"
---
# <a name="create-a-sales-tax-payment"></a>创建销售税支付

[!include [banner](../../includes/banner.md)]

结算和过帐销售税作业过程结算销售税帐户的销售税余额，并冲销特定期间内的销售税结算帐户。

1. 转到 **纳税 > 申报 > 销售税 > 结算和过帐销售税**。
2. 在 **结算期间** 字段中，单击下拉按钮以打开查找。
3. 在列表中，单击所选行中的链接。
4. 在 **开始日期** 字段中输入日期。
    - 如果未选择 **总帐参数** 页面的 **包括更正** 选项，会进行不同版本的结算处理。 原始结算为某个期间间隔的首次结算，并且一个期间间隔只能处理一次。 最新更正将结算在原始版本创建后过帐的销售税交易记录。
5. 在 **交易记录日期** 字段中，输入日期。
6. 单击 **确定**。

## <a name="performance-consideration"></a>性能注意事项

完成销售税付款过程可能需要很长时间。 影响过程性能的主要因素是结算期间的发票数，以及必须在销售税结算凭证中过帐的条目数。 要帮助提高性能，您可以选择以绕过流程中不需要的某些功能。

### <a name="enable-the-sales-tax-payment-performance-improvement-feature"></a>启用销售税付款性能改进功能

**销售税付款性能改进** 功能可通过将具有相同主科目、分类帐维度和币种的销售税付款凭证行的记帐币种金额和申报币种金额聚合到一行上，来帮助改进销售税付款过程的性能。

1. 转到 **系统管理** \> **工作区** \> **功能管理**。
2. 在 **全部** 选项卡上，搜索并选择 **销售税付款性能改进**。
3. 选择 **启用**。

### <a name="prevent-generation-of-offset-tax-transactions"></a>防止生成抵消税交易记录

默认情况下，销售税付款凭证根据销售税付款程序中结算的每个销售税交易记录过帐抵消销售税交易记录。 这些抵消销售税交易记录包含在 **销售税/分类帐对帐** 报表中。 它们显示此期间内未结算的销售税交易记录的未付余额。

但是，抵消销售税交易记录可能会增加销售税付款过程的负担。 因此，可以按需激活名为 **TaxReportGenOffsetTaxTransPerRecordSetFlighting** 的外部测试。 此外部测试可以帮助改进除泰国、波兰、匈牙利、立陶宛、马来西亚、印度、意大利、俄罗斯、捷克共和国、爱沙尼亚和拉脱维亚以外的国家和地区的抵消税交易记录的生成性能。

> [!NOTE]
> 如果纳税交易记录表上存在自定义字段，则无法激活外部测试。

由于 **销售税/分类帐对帐** 报表通常仅用于内部控制目的，在很多税制中不需要，因此您可以选择不在销售税付款凭证上生成抵消销售税交易记录。

1. 转到 **纳税** \> **间接税** \> **销售税** \> **销售税结算期间**。
2. 选择结算期间。
3. 在 **常规** 快速选项卡上，将 **防止生成抵消税交易记录** 选项设置为 **是**。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
