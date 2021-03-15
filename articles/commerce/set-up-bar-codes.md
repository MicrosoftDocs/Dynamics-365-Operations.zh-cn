---
title: 设置条码
description: 本文介绍如何在 Dynamics 365 Commerce 中使用条码。
author: jblucher
manager: AnnBe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailBarcodeMaskCharacter, RetailBarcodeMaskSetup
audience: Application User
ms.reviewer: josaw
ms.custom: 15971
ms.assetid: 6b4b2ac2-0344-41aa-8818-62c30017d5ac
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 86a29935974fbe30947c089d161f024428230b51
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969768"
---
# <a name="set-up-bar-codes"></a>设置条码

[!include [banner](includes/banner.md)]

本文介绍如何在 Dynamics 365 Commerce 中使用条码。

您可以使用条码采购和销售产品、跟踪产品变型和设置客户和员工。 您还可以使用条码发货和批准优惠券、礼品卡和贷方通知单。 您可以设置产品，以便具有标准条码或自定义公司内部条码。 产品可以有多个条码。 例如，如果来自不同的制造商，则产品可能具有多个条码，或者，如果基于大小、样式或颜色的变量它具有款式。 条码可以包含产品的重量或价格。 条码掩码是用于创建条码的模板。

> [!NOTE]
> 如果您为每个变型组合分配唯一条码，您可以在收银机上扫描条码，让程序确定出售的是哪种产品款式。 可以按款式收集和查看有关销售的统计。 可以为每个大小、颜色和样式组都分配一个可在条码中标识该组的唯一编号。 Commerce 使用条码掩码来自动为每种款式组合生成条码。 如果存在多种大小、颜色和样式的情况下功能很有用，因为不断添加款式代码将显著增加组合的数量。 如果不使用此功能，必须手动将条码分配给表示产品变型的每个组合。

可以通过手动方式或自动方式来创建条码。 若要创建条码，请按照其列出的顺序完成以下任务。

1. [设置条码掩码字符](set-up-bar-code-masks.md)。
2. [设置条码掩码](set-up-bar-code-masks.md)。
3. 配置条码设置。
4. [为产品创建条码](../supply-chain/pim/tasks/create-bar-code-product.md)。

## <a name="additional-resources"></a>其他资源

[设置条码掩码](set-up-bar-code-masks.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]