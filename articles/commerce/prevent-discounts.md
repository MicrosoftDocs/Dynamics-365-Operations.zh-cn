---
title: 用于防止为零售产品打折的选项
description: 零售商可能出于多种原因不希望 POS 中某些产品在促销或销售期间不打折。
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.custom: 85183
ms.assetid: e8c5a24f-7edd-4fd6-af80-5e0ac9f03127
ms.search.industry: Retail
ms.search.form: RetailPeriodicDiscount
ms.openlocfilehash: 803279282e98b926ae70351ced39157fa95792d9
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269046"
---
# <a name="options-for-preventing-discounts-for-retail-products"></a>用于防止为零售产品打折的选项

[!include [banner](includes/banner.md)]

零售商可能出于多种原因不希望 POS 中某些产品在促销或销售期间不打折。

可通过以下选项（位于所发布产品的 **商业** 选项卡上）将产品配置为阻止全部折扣或手动折扣。 也可以从类别层次结构的类别级别指定这些设置。

- **阻止所有折扣** – 选择此选项将阻止为此产品应用所有类型的折扣。 包括促销，如组合购买和阈值折扣，以及 POS 用户执行销售期间应用的手动行和交易记录折扣。
- **阻止手动折扣** – 选择此选项将仅阻止 POS 用户执行销售期间应用的手动行和交易记录折扣。 选择了此选项的产品仍然有资格享受促销，如组合购买和数量以及阈值折扣。

> [!NOTE]
> 这些设置不限制价格覆盖操作，因为此操作设置基础价格，不被视为折扣。

[![“阻止折扣”字段。](./media/prevent-discounts.png)](./media/prevent-discounts.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
