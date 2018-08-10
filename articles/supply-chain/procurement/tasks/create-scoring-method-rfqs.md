--- 
title: "创建询价的计分方法"
description: "此过程演示如何创建计分方法。"
author: mkirknel
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6d72678db60254801c6c899f4d405f1c59de8d65
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-scoring-method-for-rfqs"></a>创建询价的计分方法

[!include [task guide banner](../../includes/task-guide-banner.md)]

此过程演示如何创建计分方法。 计分方法是可用于比较在询价 (RFQ) 回复中发送的出价的一组条件。 例如，您可能要根据供应商以往绩效进行评级，或者评判某一公司是否为环境友好型或良好的合作者，或基于价格比较出价。 计分方法可以与申请类型关联，充当该类型的询价的默认计分方法。 这些任务通常由采购经理完成。 您可以使用演示数据公司 USMF，也可使用您自己的数据运行该过程。

1. 转到“采购”>“设置”>“询价”>“计分方法”。
2. 单击“新建”。
3. 在“名称”字段中，键入一个值。
4. 在“描述”字段中，键入一个值。
5. 单击“保存”。
6. 单击“新建”。
7. 在“名称”字段中，键入一个值。
8. 在“描述”字段中，键入一个值。
    * 为询价选择了计分方法时，此描述随计分方法名称一起显示。  
9. 在“范围起始值”字段中，输入一个数字。
    * 此范围限制采购专业人员可输入为分数的内容。 一个询价有多个计分条件时，将把已输入的分数添加到彼此，并提供总分来比较出价。  
10. 在“范围结束值”字段中，输入一个数字。
11. 单击“新建”。
12. 在“名称”字段中，键入一个值。
13. 在“描述”字段中，键入一个值。
14. 在“范围起始值”字段中，输入一个数字。
15. 在“范围结束值”字段中，输入一个数字。


