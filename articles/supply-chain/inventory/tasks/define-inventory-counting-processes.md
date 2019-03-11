---
title: 定义库存盘点流程
description: 此过程向您介绍，通过创建一个盘点组和盘点日记帐，配置基本存货盘点过程。
author: MarkusFogelberg
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCountGroup, InventJournalName, InventParameters, EcoResProductDetailsExtended, InventItemLocation, InventLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 707d4fab58a9c689f32d9e881ecacbe8e64b517c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "345321"
---
# <a name="define-inventory-counting-processes"></a>定义库存盘点流程

[!include [task guide banner](../../includes/task-guide-banner.md)]

此过程向您介绍，通过创建一个盘点组和盘点日记帐，配置基本存货盘点过程。 它也将向您展示如何在仓库和物料级别启用盘点策略。 这些任务通常由仓库主管执行。 它是某些现有发布产品和仓库的先决条件。 如果您使用演示数据公司，您可以在 USMF 公司中对任何库存物料执行此过程。


## <a name="create-a-counting-group"></a>创建一个盘点组
1. 转到“库存管理”>“设置”>“库存”>“盘点组”。
2. 单击“新建”。
3. 在“盘点组”字段中，键入一个值。
4. 在“名称”字段中，键入一个值。
5. 在“盘点代码”字段中，选择一个选项。
    * 手动 – 每次运行作业时包括行。 换言之，由您决定盘点组的计数间隔。  期间 – 期间间隔过期时在盘点日志中包括此期间的行。   零库存 – 如果现有库存量变为零 (0)，则在运行作业时在盘点日志中生成行。 如果一次计数后现有库存量变为 0，则下次开始计数时生成行。   最小值 – 如果现有库存量等于或低于指定的最小值，则在盘点日志中插入行。  
    * 可选：如果您在“盘点代码”字段中指定了“期间”，则您必须在“盘点期间”字段中键入期间间隔。 间隔单位是天。  
    * 当您在盘点日记帐创建新行时运行作业，无论您运行同一作业的频率是多少，新行将在“特定的间隔”字段中得到创建。 例如，若盘点期间设置为 7，且盘点日记帐行在 1 月 1 日最终生成，而另一作业在 1 月 5 日开始，并未经过 7 日，因而在该期间间隔内日记帐中不会生成行。 如果您在 1 月 8 日再次开始作业，因为已过 7 天，则在盘点日记帐中能够生成此期间的行。  
6. 单击“保存”。

## <a name="create-a-counting-journal-name"></a>创建一个盘点日记帐名称
1. 单击“库存管理”>“设置”>“日记帐名称”>“库存”。
2. 单击“新建”。
3. 在“名称”字段中，键入一个值。
4. 在“描述”字段中，键入一个值。
5. 在“日记帐类型”字段中，选择“盘点”。
    * 可选：当在创建盘点日记帐时，如果您想要为凭证 ID 生成特定的编号规则，您可以选择不同的凭证系列 ID。 在“编号规则”页设置凭证系列。  
6. 在“细节级别”字段中，选择一个选项。
    * 在日记帐过帐时，应用的合计级别。  
    * 可选：您可以更改“预留”字段中的值。 这就是在盘点期间，预留物料的方法。   
    * 手动 - 物料应在“预留”窗体中手动预留。   自动 - 订单数量将从物料的可用、现有库存量中保留。    分解 - 预留为交易主计划的一部分。  
7. 单击“保存”。

## <a name="set-standard-counting-journal-name"></a>设置标准盘点日记帐名称
1. 转到“库存管理”>“设置”>“库存和仓库管理参数”。
2. 单击“日记帐”选项卡。
3. 在“盘点”字段中，单击下拉按钮以打开查找。
4. 选择您之前创建的日记帐。
    * 该日记帐将为“盘点类型”的库存日记帐的默认日记帐名称。  
5. 单击“常规”选项卡。
    * 可选：选择此选项以在盘点过程中锁定某物料，以避免更新装箱单、领料单或进行领料单登记等。  

## <a name="set-the-counting-policy-for-an-item"></a>设置物料的盘点策略
1. 转到“产品信息管理”>“产品”>“已发布产品”。
2. 在该列表中，单击您想为其设置盘点策略产品的物料编号的链接。
    * 请注意：您需要选择进行库存跟踪的物料。 不能盘点非库存产品。 如果您正使用 USMF 演示数据，您可以选择物料 A0001。  
3. 单击“编辑”。
4. 切换“库存管理”部分的扩展。
5. 在“盘点组”字段中，单击下拉按钮以打开查找。
6. 在该列表中，单击您之前创建的盘点组。
    * 此产品将包含在使用此盘点组创建库存盘点日记帐行之中。  
7. 单击“保存”。

## <a name="set-the-counting-policy-for-an-item-in-a-specific-warehouse"></a>为特定仓库中的物料设置盘点策略
1. 在“操作窗格”上，单击“库存管理”。
2. 单击“仓库物料”。
3. 单击“新建”。
4. 在“仓库”字段，单击下拉按钮以打开查找。
5. 在该列表中，选择您想设置特定盘点的策略的仓库。
6. 在“盘点组”字段中，单击下拉按钮以打开查找。
7. 在列表中，选择一个盘点组。
    * 您可以选择一个应用于您所选择的特定仓库的物料的特定盘点组。 在该仓库执行盘点时，此盘点策略将覆盖物料的常规盘点策略。  
8. 单击“保存”。

