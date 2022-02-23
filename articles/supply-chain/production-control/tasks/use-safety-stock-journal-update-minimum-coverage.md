---
title: 使用安全存货日记帐更新最小覆盖范围
description: 此过程演示如何根据历史交易记录计算最低覆盖范围方案，然后使用这些方案更新物料覆盖范围。
author: ChristianRytt
manager: tfehr
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqItemJournalName, ReqItemJournalSafetyStock, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0d69daf3d307ba72ff6017d91849e3d22bd0bd85
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423228"
---
# <a name="use-the-safety-stock-journal-to-update-minimum-coverage"></a>使用安全存货日记帐更新最小覆盖范围

[!include [banner](../../includes/banner.md)]

此过程演示如何根据历史交易记录计算最低覆盖范围方案，然后使用这些方案更新物料覆盖范围。 方法是使用安全存货日记帐。 创建此任务的演示数据公司是 USMF。 这项任务供生产计划者用于帮助维护最低覆盖范围。


## <a name="create-a-new-safety-stock-journal-name"></a>新建安全存货日记帐名称
1. 在 **导航窗格** 中，转到 **主计划 > 设置 > 安全存货日记帐名称**。
2. 单击 **新建**。
3. 在 **名称** 字段中，键入“材料”。
4. 在 **描述** 字段中，键入“材料”。
5. 关闭该页面。

## <a name="create-a-safety-stock-journal"></a>创建安全库存日记帐
1. 在 **导航窗格** 中，转到 **主计划 > 主计划 > 运行 > 安全存货计算**。
2. 单击 **新建**。
3. 在 **名称** 字段中，输入或选择一个值。 选择您创建的安全存货日记帐名称，如“物料”。  
4. 单击 **创建行**。
5. 在 **开始日期** 字段中输入日期。  
6. 在 **结束日期** 字段中输入日期。
7. 单击 **确定**。 这将为包含库存交易记录的维度创建行。  

## <a name="calculate-proposal"></a>计算方案
1. 单击 **计算方案**。
2. 选择 **使用提前期的平均发货量** 选项。
3. 将 **倍增系数** 设置为“10”。 倍增系数用于调整此方案。 由于演示数据只有少量交易记录，所以您需要设置此系数才能生成切实可行的方案。  
4. 单击 **确定**。 向下滚动找到 M0002 和 M0003。 查看 **计算所得的最低数量** 列。   

## <a name="update-minimum-quantity"></a>更新最小数量
1. 在 **新建最小数量** 字段中，输入一个数字。 更新“新建最小数量”以匹配“计算所得的最低数量”中的值。 如果计算所得的最低数量为零，可以输入所需将来值。 例如，可以在此字段中输入拥有仓库 12 的 M0002 的计算所得最低数量。  
2. 在列表中，找到并选择所需记录。 例如，可以选择拥有仓库 12 的 M0002。  
3. 在 **新建最小数量** 字段中，输入一个数字。 更新“新建最小数量”以匹配“计算所得的最低数量”中的值。 如果计算所得的最低数量为零，可以输入所需将来值。  

## <a name="post-the-new-minimum-quantity-and-validate-the-result"></a>发布新的最小数量和验证结果
1. 单击 **过帐**。
2. 单击 **确定**。
3. 单击并打开 **物料编号** 字段中的链接。
4. 单击并打开 **物料编号** 字段中的链接。
5. 在 **操作窗格** 中，单击“计划”。
6. 单击 **物料覆盖范围**。 请注意，已使用安全存货日记帐中的新最低数量更新了 **最小数量**。  

