---
title: 转移仓库内的实际库存
description: 该过程向您介绍创建和过帐库存转移日记帐，以登记物料在仓库内的库位转移。
author: yufeihuang
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cf5a3711cfcd6e5a2ddce09af8569ea26c3502c8
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/29/2021
ms.locfileid: "7580784"
---
# <a name="transfer-physical-inventory-within-the-warehouse"></a>转移仓库内的实际库存

[!include [banner](../../includes/banner.md)]

该过程向您介绍创建和过帐库存转移日记帐，以登记物料在仓库内的库位转移。 在您开始该过程前，您需要为库存转移设置库存日记帐名称。 您可以使用所示的示例值或者使用您自己的数据（如果有产品和库位设置）在该过程中用演示数据公司 USMF 运行。 这些任务通常由仓库员工完成。


## <a name="create-an-inventory-transfer-journal"></a>创建库存转移日记帐
1. 在 **导航窗格** 中，转到 **库存管理 > 日记帐条目 > 物料 > 转移**。
2. 单击 **新建**。
3. 在 **名称** 字段中，输入或选择一个值。
4. 单击 **确定**。 这是指定每一日记帐行的“开始”和“结束”维度的选项。 这些对于日记帐类型十分重要。 您可以使用不同规则将物料转移到库位。 在此示例中，我们将相同仓库内的物料从受牌照控制的库位转移到不受牌照控制的库位。   

## <a name="create-journal-lines"></a>创建日记帐行
1. 在 **日记帐行** 快速选项卡上，单击 **新建**。
2. 在 **物料编号** 字段中，输入或选择一个值。 如果您正在使用 USMF，可以选择“A0001”。  
3. 在 **源站点** 字段中，输入或选择一个值。 如果您正在使用 USMF，可以选择“2”。  
4. 在 **目标站点** 字段中，输入或选择一个值。 如果您正在使用 USMF，可以选择“2”。  
5. 在 **源仓库** 字段中，输入或选择一个值。 如果您正在使用 USMF，可以选择“24”。  
6. 在 **目标仓库** 字段中，输入或选择一个值。 如果您正在使用 USMF，可以选择“24”。  
7. 在 **源库位** 字段中，输入或选择一个值。 如果您正在使用 USMF，可以选择“FL-001”。  
8. 在 **目标库位** 字段中，输入或选择一个值。 如果您正在使用 USMF，可以选择“散装-001”。  
9. 在 **数量** 字段中，输入一个数字。
10. 在 **行明细** 快速选项卡上，单击 **库存维度** 选项卡。
11. 在 **源库存维度** 的 **牌照** 字段中，输入或选择一个值。 如果您正在使用 USMF，可以选择“24”。  
12. 单击 **保存**。

## <a name="post-the-inventory-transfer-journal"></a>过帐库存转移日记帐
1. 在 **操作窗格** 上，单击 **过帐**。
2. 单击 **确定**。

## <a name="view-inventory-transactions"></a>查看库存交易记录
1. 单击 **库存**。
2. 单击 **交易记录**。 在这里，您可以查看过帐日记帐时创建的交易记录。  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]