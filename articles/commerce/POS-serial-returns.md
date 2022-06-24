---
title: 在 POS 中退回序列号控制的产品
description: 本文介绍了在 Microsoft Dynamics 365 Commerce 销售点 (POS) 应用程序中验证序列化物料作为退货流程的一部分的功能。
author: hhainesms
ms.date: 06/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: b2af301180dc2284400b887ce36357660bdd86fa
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860313"
---
# <a name="return-serial-numbercontrolled-products-in-pos"></a>在 POS 中退回序列号控制的产品

[!include [banner](includes/banner.md)]

本文介绍了在 Microsoft Dynamics 365 Commerce 销售点 (POS) 应用程序中验证序列化物料作为退货流程的一部分的功能。

> [!NOTE]
> 在 Commerce 版本 10.0.20 及更高版本中，提供了名为 **POS 中的统一退货处理体验** 的新功能。 若要在 POS 中的退货订单处理期间使用序列号验证，您必须打开此功能。 有关此功能在打开时提供的其他功能的信息，请参阅[在 POS 中创建退货](POS-returns.md)。
>
> 该功能在打开后，无法关闭。

## <a name="options-for-validating-serialized-returns"></a>验证序列化退货的选项

当打开 **POS 中的统一退货处理体验** 功能时，组织可以通过 POS 对序列号控制的物料退货进行验证。 如果返回的序列号与出售的原始序列号不同，此功能可以警告用户。 在 Commerce 版本 10.0.20 及更高版本中，用户收到的消息只是警告消息。 用户可以针对与最初出售的序列号不同的序列号继续处理退货。

若要在打开 **POS 中的统一退货处理体验** 功能后为组织配置序列号验证，请在 Commerce Headquarters 中转到 **Retail 和 Commerce \> Headquarters 设置 \> 参数 \> Commerce 参数**。 在 **库存** 选项卡的 **存储库存操作** 快速选项卡上，将 **对 POS 退货启用序列号验证** 选项设置为 **是**。

## <a name="process-returns-for-serialized-items-in-pos"></a>处理 POS 中序列化物料的退货

如果已将 **对 POS 退货启用序列号验证** 选项设置为 **是**，当通过 POS 退回序列号控制的物料时，用户可以为 **可退货产品** 页面的详细信息窗格中的退货行输入序列号。 如果输入的序列号与为销售交易出售的原始序列号不匹配，用户会收到一条警告消息。 但是，应用程序不会阻止用户继续发布退货。

> [!NOTE]
> 目前，POS 仅支持对原始订购数量不超过 1 的退货行验证序列号。 如果在非 POS 渠道上创建了原始销售订单行，并且如果为给定销售行上的序列化物料订购的数量超过 1，则无法通过 POS 正确退回物料。

## <a name="additional-resources"></a>其他资源

[在 POS 中创建退货](POS-returns.md)
