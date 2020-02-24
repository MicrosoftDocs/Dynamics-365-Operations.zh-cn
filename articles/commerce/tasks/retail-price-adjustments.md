---
title: 零售价调整
description: 此程序将逐步演示如何创建商业价格调整。
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailDiscountPriceGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fd6459416ca42530401aa439b1b8511657bd9b36
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/01/2020
ms.locfileid: "3021720"
---
# <a name="retail-price-adjustments"></a>零售价调整

[!include[task guide banner](../includes/task-guide-banner.md)]

此程序将逐步演示如何创建商业价格调整。 价格调整可以直接设置某一商品的销售价格，或修改其基础销售价格或贸易协议销售价格。 此程序使用 USRT 演示数据公司。

1. 单击“价格和折扣管理”。
2. 单击“价格调整”选项卡。
3. 单击“新建”。
    * 您可在此创建所有最常用的价格和折扣规则，包括折扣、价格调整、贸易协议日记帐和类别定价规则。  
4. 单击“价格调整”。
5. 在“名称”字段中，键入一个值。
6. 展开“行”部分。
7. 单击“添加”。
    * 在本示例中，在“产品”字段中输入“81126”。 然后，在“折扣百分比”字段中，输入“10.0”。  
    * 折扣百分比类型价格调整将会降低基础销售价格或贸易协议销售价格。  
8. 单击“添加”。
    * 在本示例中，在“产品”字段中输入“81125”。 然后，选择“折扣方法”字段中的“现金折扣金额”。    最后，在“现金折扣金额”字段中输入“5.0”。  
    * 现金折扣金额折扣类型是从基础价或贸易协议价格减去的金额。  
9. 单击“价格组”。
    * 选择“价格组”字段中的“RP-休斯敦”。  
    * 这将价格调整和休斯敦商店关联起来。  
10. 单击“保存”。
11. 关闭该页面。
12. 在“状态”字段中，选择“已启用”。
13. 单击“保存”。
14. 关闭该页面。
15. 刷新该页面。

