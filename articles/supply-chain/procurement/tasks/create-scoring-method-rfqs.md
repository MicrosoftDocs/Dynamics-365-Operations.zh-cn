---
title: 创建询价的计分方法
description: 此过程演示如何创建计分方法。
author: GalynaFedorova
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchRFQScoringMethod
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2a6b715caa57d8ceb2e91af88538fa735568a997
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/03/2022
ms.locfileid: "8671050"
---
# <a name="create-a-scoring-method-for-rfqs"></a>创建询价的计分方法

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]