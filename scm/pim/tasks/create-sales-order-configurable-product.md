--- 
title: "创建可配置产品的销售订单"
description: "此过程显示如何将配置模板应用于销售订单中的一个产品。"
author: BibiSp
manager: AnnBe
ms.date: 10/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 6546d504a2fda255cb5183408dfe84a3074543ab
ms.contentlocale: zh-cn
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-sales-order-for-a-configurable-product"></a>创建可配置产品的销售订单

[!include[task guide banner](../../includes/task-guide-banner.md)]

此过程显示如何将配置模板应用于销售订单中的一个产品。 此示例使用 USMF 演示数据公司中的 D0006 扬声器模型。 通常，销售订单处理人员使用此过程。


## <a name="create-a-sales-order"></a>创建销售订单
1. 点击“销售订单处理和查询”。
2. 单击“新建”。
3. 单击“销售订单”。
4. 在“客户帐户”字段中选择“US-001”。 
5. 单击“确定”。
6. 在“物料编号”字段中，选择 D0006。
    * 对于此任务，必须选择一个可配置产品。  
7. 单击“产品和供应”。
8. 单击“配置行”。
    * 请注意，已根据选择的配置更改了价格，并且“含电缆”字段现在已设置为 True。  
    * 记下为电缆选择的默认价格和设置。  
9. 单击“加载模板”。
    * 此示例显示如何应用模板以选择预定义的配置。 如果将此过程用作任务指南并希望查看可用的其他属性值，必须单击“解锁”按钮。  
10. 单击“确定”。
11. 单击“确定”。
12. 展开“行明细”部分。
13. 单击“产品”选项卡。
    * 此物料的配置现在在产品维度下列出。  
14. 关闭该页面。

## <a name="select-the-product-configuration"></a>选择产品配置


