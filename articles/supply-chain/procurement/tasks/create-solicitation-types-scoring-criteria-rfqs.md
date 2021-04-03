---
title: 创建询价的申请类型和计分条件
description: 此指南演示如何创建申请类型和将其与计分方法关联。
author: RichardLuan
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQSolicitationType, PurchRFQCaseTableListPage, PurchCreateRFQCase, PurchRFQCaseTable, PurchRFQScoringRFQCaseCriteria, PurchRFQScoringCriteriaCopy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cf196711799b78d7f4106b6693127d7f356b1d4e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5262205"
---
# <a name="create-solicitation-types-and-scoring-criteria-for-rfqs"></a>创建询价的申请类型和计分条件

[!include [banner](../../includes/banner.md)]

此指南演示如何创建申请类型和将其与计分方法关联。 还演示如何在随后将设置默认计分方法的询价 (RFQ) 中使用申请类型。 这些任务通常由采购经理完成。 您可以使用演示数据公司 USMF，也可使用您自己的数据运行该过程。 首先需要有计分方法。


## <a name="create-a-solicitation-type"></a>创建请求类型
1. 转到“采购”>“设置”>“询价”>“申请类型”。
2. 单击“新建”。
3. 在“名称”字段中，键入一个值。
4. 在“描述”字段中，键入一个值。
5. 在“计分方法”字段中，选择要用于此申请类型的计分方法。
6. 单击“保存”。
7. 关闭该页面。

## <a name="use-the-solicitation-type"></a>使用申请类型
1. 转到“采购”>“询价”>“所有询价”。
2. 单击“新建”。
3. 在“申请类型”字段中，选择刚才创建的申请类型。 
    *   
4. 单击“确定”。
5. 单击“计分条件”。
    * 显示的计分条件来自您为申请类型关联的计分方法。 您可以选择在此页中添加或删除条件。 还可以通过从其他计分方法复制条件来添加新条件。  
6. 单击“复制条件”。
7. 在“计分方法”字段中，输入或选择一个值。
8. 单击“确定”。
9. 关闭该页面。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]