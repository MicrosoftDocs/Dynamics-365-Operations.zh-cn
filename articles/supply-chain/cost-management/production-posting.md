---
title: 生产过帐
description: 本文提供有关生产流程中不同过帐类型的信息。
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventItemGroup, ProjCategory, WrkCtrResourceGroup, WrkCtrTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 54591
ms.assetid: 0917fe64-f643-46ae-98ff-5013b266a067
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0b44d57fe89ef7ae3def835865e4da80c260f907
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1547731"
---
# <a name="production-posting"></a>生产过帐

[!include [banner](../includes/banner.md)]

本文提供有关生产流程中不同过帐类型的信息。

生产过帐活动遵循以下各节中描述的生产流程。

## <a name="material-consumption"></a>物料消耗量
在过帐生产领料单日记帐时，将物料登记为在生产中被消耗。 此流程生成扣减现有库存量的发货交易记录。 在生产参数中，您可以指定是否应在分类帐中过帐生产中的原材料（在制品 \[WIP\]）的值。 随后，生产中的原材料 (WIP) 的值将过帐到专用领料单帐户和专用领料单对方科目。

## <a name="time-consumption"></a>时间消耗量
工作人员在生产作业上花费的时间将记录在工艺卡日记帐或作业卡日记帐中。 在过帐这些日记帐时，将处理过帐到生产中 (WIP) 的资源的专用帐户的分类帐。 此过帐表示在生产订单上花费的时间的值。 在将生产订单登记为已结束后，将结算 WIP 帐户。

## <a name="reporting-finished-goods-and-error-quantities"></a>报告成品和残次数量
在生产订单报告为完工入库时，在库存管理中通过完工入库的日记帐更新已完成成品的数量。 如果您在使用 WIP 会计（可在生产参数中设置），则生成分类帐日记帐以减少 WIP 帐户和增加成品库存。 日记帐使用为产品定义的标准成本。

## <a name="ending-the-production-order"></a>结束生产订单
在结束生产订单前，为生成的数量计算实际成本。 物料、人工和开销的所有预估成本都被冲销，并用实际成本替代。 成品的总计成本从库存“收货”帐户中借记，并贷记到库存“发货”帐户。 如果您在运行成本计算时选中**结束作业**复选框，则生产订单的状态将更改为**已结束**。 此状态将阻止将任何额外成本无意中过帐到已完成的生产订单。 您可以指定应将完工入库期间报告的残次数量的值分配到报告为已完工入库的完好数量。 或者，您可以指定应将残次数量的值过帐到专用的报废科目。

## <a name="controlling-the-level-of-ledger-posting"></a>控制分类帐过帐的级别
在**生产控制参数**中，可以使用**分类帐过帐**字段设置生产流程的分类帐过帐级别。 提供以下值：

-   **物料和资源** – 为原材料和成品使用在物料组上设置的会计科目。 从工艺路线工序中的资源或资源组提取时间消耗量的 WIP。
-   **物料和类别** – 为原材料和成品使用在物料组上设置的会计科目。 从与工艺路线工序关联的成本类别提取时间消耗量的 WIP。
-   **生产组** – 为材料和时间消耗量使用在生产组中设置的会计科目。 生产组与已发布产品关联，并会在创建生产订单时复制到这些订单。 随后，对生产订单的过帐将在与生产订单关联的生产组之后进行。

**注意：** 如果使用了计算成品成本的标准方法，则最终交易记录中将反映此情况。 如果实际成本和使用标准方法计算的成本之间存在差别，它将过帐到显示利润或损失的科目中。



