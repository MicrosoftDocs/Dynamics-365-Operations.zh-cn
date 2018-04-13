---
title: "防止为零售产品打折"
description: "零售商可能出于多种原因不希望 POS 中某些产品在促销或销售期间不打折。"
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 85183
ms.assetid: e8c5a24f-7edd-4fd6-af80-5e0ac9f03127
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 70139c124486e3e6a01c1c08e71f140dcf1864c0
ms.openlocfilehash: e0d3a16da6a673f9ce6a025a7d4bde9ffb1a9e9b
ms.contentlocale: zh-cn
ms.lasthandoff: 10/23/2017

---

# <a name="prevent-discounts-for-retail-products"></a>防止为零售产品打折

[!INCLUDE [banner](includes/banner.md)]

零售商可能出于多种原因不希望 POS 中某些产品在促销或销售期间不打折。

可通过以下选项（位于所发布产品的**零售**选项卡上）将产品配置为阻止全部折扣或手动折扣。 也可以从零售类别层次结构的类别级别指定这些设置。

**阻止所有折扣**：选择此选项将阻止为此产品应用所有类型的折扣。 包括促销，如组合购买和阈值折扣，以及 POS 用户执行销售期间应用的手动行和交易记录折扣。

**阻止手动折扣**：选择此选项将仅阻止 POS 用户执行销售期间应用的手动行和交易记录折扣。 选择了此选项的产品仍然有资格享受促销，如组合购买和数量以及阈值折扣。

**注意**：这些设置不限制价格覆盖操作，因为此操作设置基础价格，不被视为折扣。  

[![“阻止折扣”字段](./media/prevent discounts.png)](./media/prevent discounts.png)

