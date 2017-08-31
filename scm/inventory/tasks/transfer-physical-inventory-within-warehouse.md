--- 
title: "转移仓库内的实际库存"
description: "该过程向您介绍创建和过帐库存转移日记帐，以登记物料在仓库内的库位转移。"
author: MarkusFogelberg
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: fedb209ab111ed1fb6281fda2f4dea345e0905ef
ms.contentlocale: zh-cn
ms.lasthandoff: 07/27/2017

---
# <a name="transfer-physical-inventory-within-the-warehouse"></a>转移仓库内的实际库存

[!include[task guide banner](../../includes/task-guide-banner.md)]

该过程向您介绍创建和过帐库存转移日记帐，以登记物料在仓库内的库位转移。 在您开始该过程前，您需要为库存转移设置库存日记帐名称。 您可以使用所示的示例值或者使用您自己的数据（如果有产品和库位设置）在该过程中用演示数据公司 USMF 运行。 这些任务通常由仓库员工完成。


## <a name="create-an-inventory-transfer-journal"></a>创建库存转移日记帐
1. 转到“转移”。
2. 单击“新建”。
3. 在“名称”字段中，输入或选择一个值。
4. 单击“确定”。
    * 这是指定每一日记帐行的“开始”和“结束”维度的选项。 这些对于日记帐类型十分重要。 您可以使用不同规则将物料转移到库位。 在此示例中，我们将相同仓库内的物料从受牌照控制的库位转移到不受牌照控制的库位。   

## <a name="create-journal-lines"></a>创建日记帐行
1. 单击“新建”。
2. 在“物料编号”字段中，输入或选择一个值。
    * 如果您正在使用 USMF，可以选择“A0001”。  
3. 在“源站点”字段中，输入或选择一个值。
    * 如果您正在使用 USMF，可以选择“2”。  
4. 在“目标站点”字段中，输入或选择一个值。
    * 如果您正在使用 USMF，可以选择“2”。  
5. 在“源仓库”字段中，输入或选择一个值。
    * 如果您正在使用 USMF，可以选择“24”。  
6. 在“目标仓库”字段中，输入或选择一个值。
    * 如果您正在使用 USMF，可以选择“24”。  
7. 在“源库位”字段中，输入或选择一个值。
    * 如果您正在使用 USMF，可以选择“FL-001”。  
8. 在“目标库位”字段中，输入或选择一个值。
    * 如果您正在使用 USMF，可以选择“散装-001”。  
9. 在“数量”字段中，输入一个数字。
10. 单击“库存维度”选项卡。
11. 在“牌照”字段中，输入或选择一个值。
    * 如果您正在使用 USMF，可以选择“24”。  
12. 单击“保存”。

## <a name="post-the-inventory-transfer-journal"></a>过帐库存转移日记帐
1. 单击“过帐”。
2. 单击“确定”。

## <a name="view-inventory-transactions"></a>查看库存交易记录
1. 单击“库存”。
2. 单击“交易记录”。
    * 在这里，您可以查看过帐日记帐时创建的交易记录。  


