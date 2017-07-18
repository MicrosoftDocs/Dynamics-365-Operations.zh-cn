---
title: "包装材料和费用"
description: "定期向回收公司支付包装材料费用。 为包装单位中包含的每种材料支付每个单位重量的金额。 程序将计算和报告包装材料费用，但是不过帐分录，因为没有将这些费用视为要向主管机构缴纳的税款。"
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventPackagingGroup, InventPackagingMaterialCode, InventPackagingMaterialFee, InventPackagingMaterialTrans, InventPackagingMaterialTransPurch, InventPackagingUnit
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2194
ms.assetid: 040b65dc-43c9-4256-b69f-b2d6e736fbe9
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: e07ed8d8344576f96d2439051255d0e58555c30f
ms.contentlocale: zh-cn
ms.lasthandoff: 05/25/2017

---

# <a name="packing-materials-and-fees"></a>包装材料和费用

[!include[banner](../includes/banner.md)]


定期向回收公司支付包装材料费用。 为包装单位中包含的每种材料支付每个单位重量的金额。 程序将计算和报告包装材料费用，但是不过帐分录，因为没有将这些费用视为要向主管机构缴纳的税款。

程序将为销售订单行和采购订单行计算包装材料重量和费用。

可以为一种物料、一个物料包装组或所有物料定义一个或多个包装单位。 包装单位包含包装材料、其重量和该包装单位中包括的物料数量。 将包装材料代码分配给定义的包装材料的每种类型。 根据包装材料代码，您可以指定指定期间的价格。 基于此信息计算包装材料费用。

| **注意**                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------|
| 即使您的公司不支付包装材料费用，您也可以使用此功能来计算包装材料重量的统计。 |

## <a name="setup-requirements-for-packing-material-fees"></a>包装材料费用的设置要求
在计算包装材料重量和/或费用之前，必须创建下列基础数据：

-   包装组 – 创建要分配到物料的包装组。
-   包装材料代码 – 为定义的包装材料的每种类型创建包装材料代码。
-   包装单位 – 为一种物料、一个包装组或所有物料指定包装单位。 对于每个包装单位，定义要包含的包装材料、分配重量，并在“包装单位因子”字段中，从库存单位输入换算系数。
-   包装材料费用 – 按照包装材料代码指定包装材料费用。 为每种类型的材料定义有效期、每种材料的价格、币种和单位。

## <a name="packing-units-on-sales-order-lines"></a>销售订单行的包装单位
当您创建销售订单行时，检查系统以查看是否为物料指定了包装单位。 如果指定了包装单位，系统会使用指定的包装单位和包装单位数量更新销售订单行。 包装单位数量基于订购数量除以选定包装单位中的物料数量。 如果没有指定包装单位，您可以在销售订单行上手动输入包装单位和包装单位数量。 当您过帐销售订单行时，也可以更改包装单位和包装单位数量。 如果销售订单行部分交货或一部分开发票，将用到这一操作。 当您为销售订单开发票时，将创建包装材料交易记录。 包装材料交易记录包含销售订单行的包装材料的重量。 还可以在开票后修改交易记录，然后创建新的交易记录。

## <a name="packing-units-on-purchase-order-lines"></a>采购订单行的包装单位
采购订单行的包装材料交易记录不是由系统创建的。 您将手动在**“包装材料交易记录”**页中为已开票采购订单行创建交易记录。

## <a name="set-up-customer-packagingmaterialfee-license-numbers"></a>设置客户的包装材料费用许可证编号
如果客户支付包装材料费用，请在**“客户”**页中指定客户的包装材料费用许可证编号。 如果为客户指定了许可证编号，则对销售订单开票时将自动计算包装材料费用。 开票后，**“计算费用”**复选框将在**“包装材料交易记录”**页中被取消选中，因为您不必计算和打印报表。 您可以在发票上打印包装材料重量并告知客户由他们支付该费用。 

如果您的公司支付包装材料费用，请不要指定客户许可证编号。 开票后，**“计算费用”**复选框在**“包装材料交易记录”**页中被选中。 这表示创建报表时计算费用。 您可以在发票上打印重量并指明由您的公司支付费用。

## <a name="print-packaging-material-weights-on-invoices"></a>在发票上打印包装材料重量
可以在发票上打印包装材料重量并指明由谁来支付包装材料费用。 重量按包装代码来汇总。
 





