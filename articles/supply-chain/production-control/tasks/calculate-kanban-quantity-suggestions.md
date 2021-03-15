---
title: 计算看板数量建议
description: 此过程重点是通过使用看板数量计算，优化特定看板规则的看板大小和数量。
author: ChristianRytt
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3e7343d0a9ea3082a3fad90bdcbb8962e56c70a4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4981373"
---
# <a name="calculate-kanban-quantity-suggestions"></a>计算看板数量建议

[!include [banner](../../includes/banner.md)]

此过程重点是通过使用看板数量计算，优化特定看板规则的看板大小和数量。 创建此程序的演示数据公司是 USMF。 此程序是专为价值流经理设计的。 这是您完成“添加新看板数量计算策略到看到规则”这一过程的先决条件。


## <a name="create-a-kanban-quantity-calculation"></a>创建看板数量计算
1. 转到“生产控制”>“定期任务”>“看板数量计算”>“计算看板数量”。
2. 单击“新建”。
3. 在“名称”字段中，键入“Speaker2016”。
4. 在“名称”字段中，单击下拉按钮以打开查找。
    * 选择您在“添加新看板数量计算策略到看板规则”这一过程中创建的策略。 例如，Speaker2016。  
5. 在列表中，单击所选行中的链接。
6. 在“规则有效截止日期”字段，设置日期和时间为“2012-12-17T08:00:00”。
    * 此日期用作确定要包括在看板数量计算中的固定看板规则基础。  
7. 在“已履行需求期间开始日期”字段，设置日期和时间为“2012-11-17T09:00:00”。
    * 包括过去需求交易记录以计算看板数量的开始日期。  
8. 在“已履行需求期间结束日期”字段，设置日期和时间为“2012-12-17T07:59:59”。
    * 包括过去需求交易记录以计算看板数量的截止日期。  
9. 在“需求期间开始日期”字段，设置日期和时间为“2012-12-17T08:00:00”。
    * 包括当前需求交易记录以计算固定看板数量的开始日期。  
10. 在“需求期间结束日期”字段，设置日期和时间为“2013-01-16T07:59:59”。
    * 包括当前需求交易记录以计算看板数量的截止日期。  

## <a name="generate-kanban-quantity-proposal"></a>生成看板数量方案
1. 单击“保存”。
2. 单击“生成”。
    * 这将生成 000020 看板规则的看板数量方案行。  

## <a name="run-kanban-quantity-calculation"></a>运行看板数量计算
1. 单击“计算”。
    * 此计算看板数量方案。  
2. 单击“确定”。
3. 在列表中，标记所选的行。
    * 请注意，建议的看板数量为 2。  

## <a name="change-product-quantity-and-calculate-again"></a>更改产品数量并重新计算
1. 将产品数量设置为“5”。
2. 单击“计算”。
3. 单击“确定”。
    * 请注意，如果看板数量为 5，建议更改为 4。  
    * 这由实际产品数量低引起，我们需要更多看板来满足需求。  

## <a name="update-kanban-rule"></a>更新看板规则
1. 在“规则生效日期”字段中，输入日期和时间。
    * 将“规则有效截止日期”设置为未来日期。 例如，今天 + 一年。  
2. 单击“更新”。
3. 单击“确定”。
4. 关闭该页面。

## <a name="validate-change-on-kanban-rule"></a>验证看板规则的更改
1. 转到“产品信息管理”>“Lean manufacturing”>“看板规则”。
2. 在列表中，单击所选行中的链接。
    * 选择在上一子任务中创建的看板规则。 这应该是按编号排序的列表中的第一个看板规则。  
3. 切换“详细信息”部分的展开项。
    * 请注意，生效日期指规则在此日期前未生效。  
4. 切换“数量”部分的展开项。
    * 请注意，这是您在看板数量计算中输入的默认数量。  
    * 请注意，这是来自看板数量计算的固定看板数量 4.  
5. 单击“列表面板”选项卡。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]