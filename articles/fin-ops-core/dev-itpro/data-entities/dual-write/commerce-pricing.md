---
title: 对 Dynamics 365 Sales 使用 Dynamics 365 Commerce 定价引擎
description: 本主题介绍如何在 Dynamics 365 Sales 中使用 Microsoft Dynamics 365 Commerce 定价引擎创建销售报价单。
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: shajain
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-11-03
ms.openlocfilehash: fad5c21d75db62b85efe803f1667dd3f9164a5fc
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/20/2020
ms.locfileid: "4594910"
---
# <a name="use-the-dynamics-365-commerce-pricing-engine-with-dynamics-365-sales"></a>对 Dynamics 365 Sales 使用 Dynamics 365 Commerce 定价引擎

[!include [banner](../../includes/banner.md)]

本主题介绍如何在 Dynamics 365 Sales 中使用 Microsoft Dynamics 365 Commerce 定价引擎创建销售报价单。

Dynamics 365 Commerce 定价引擎支持大多数企业对消费者 (B2C) 定价方案，如商店级定价、基于隶属关系和基于会员制的定价、组合折扣、数量折扣和阈值折扣。 定价引擎使用复杂的规则来确定给定报价单或订单的最佳价格。

使用[双写入](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview)时，您可以根据需要选择三个选项。 您可以使用 Dynamics 365 Sales 中价格列表中的静态定价、Dynamics 365 Supply Chain Management 中的定价引擎或 Dynamics 365 Commerce 中的定价引擎。 在这些选项中，Commerce 定价引擎最适合 B2C 方案。

## <a name="use-the-commerce-pricing-engine-in-sales"></a>在 Sales 中使用 Commerce 定价引擎

> [!NOTE]
> 现在，Commerce 定价引擎只能用于在 Sales 中创建报价单。 销售订单尚不能与 Commerce 定价引擎集成。

当用户在 Sales 中启动报价单时，双写入框架会将报价单详细信息复制到 Commerce。 将把对在 Sales 中现有报价单行或任何新添加的报价单行的任何更改都复制到 Commerce。 当用户要使用 Commerce 定价引擎对报价单定价时，可以选择 **报价单** 根据 Commerce 定价引擎更新报价单的价格。 然后同时在 Sales 和 Commerce 中自动更新价格。

## <a name="prerequisites"></a>先决条件

- 必须先执行[双写入中的目标客户到现金](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-prospect-to-cash/)中的步骤，才能使用 Sales 中的 Commerce 定价引擎。
- 您必须按照以下步骤关闭手动输入的贸易协议评估：

    1. 在 Commerce 环境中，转至 **应收帐款 \> 设置 \> 应收帐款参数**。
    1. 在 **价格** 选项卡上的 **贸易协议评估** 快速选项卡上，清除 **手动输入** 复选框。

## <a name="additional-resources"></a>其他资源

[双写入中的目标客户到现金](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-prospect-to-cash/)
