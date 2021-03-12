---
title: 更正库存跟踪信息
description: 该过程让您了解创建和过帐库存转移日志的流程，以纠正库存跟踪信息。
author: MarkusFogelberg
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventBatchIdLookup, InventLocationIdLookup, InventDimTracking, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7c70dba7d21eab372cec235efa5a4be19587a409
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000126"
---
# <a name="correct-inventory-tracking-information"></a>更正库存跟踪信息

[!include [banner](../../includes/banner.md)]

该过程让您了解创建和过帐库存转移日志的流程，以纠正库存跟踪信息。 在此示例中，我们通过将不正确登记的批更新为其他批，来更新批控制物料的信息。 您可以使用演示数据公司 USPI 或您自己的数据了解该过程。 如果您使用您自己的数据，需启用可以批处理的物料；并且它不能是位置控制。 您还需要有一个为库存转移而设置的库存日记帐名称。 这些任务通常由仓库员工完成。


## <a name="create-an-inventory-transfer-journal"></a>创建库存转移日记帐
1. 转到“转移”。
2. 单击“新建”。
3. 在“名称”字段中，输入或选择一个值。
4. 单击“确定”。

## <a name="create-journal-lines"></a>创建日记帐行
1. 单击“新建”。
2. 在“物料编号”字段中，输入或选择一个值。
    * 如果您正在使用 USPI，请选择物料 M5003。  
3. 在“数量”字段中，输入一个数字。
4. 单击“库存维度”选项卡。
5. 在“批号”字段中，输入或选择一个值。
6. 在“站点”字段中，输入或选择一个值。
7. 在“仓库”字段中，输入或选择一个值。
8. 在“批号”字段中，输入或选择一个值。

## <a name="post-the-journal"></a>过帐日记帐
1. 单击“过帐”。
2. 单击“确定”。

## <a name="check-tracing-information"></a>检查跟踪信息
1. 单击“库存”。
2. 单击“跟踪“。
3. 单击“确定”。
    * 使用此跟踪信息，您可以返回跟踪您从哪个批中更正库存。  您还可以使用“物料跟踪页”以查看此信息。  
4. 关闭该页面。

## <a name="check-inventory-transactions"></a>检查库存交易记录
1. 单击“库存”。
2. 单击“交易记录”。
    * 在这里，您可以查看过帐日记帐时创建的交易记录。   

