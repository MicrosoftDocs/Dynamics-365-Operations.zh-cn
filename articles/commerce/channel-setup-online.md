---
title: 设置在线渠道
description: 本文介绍如何在 Microsoft Dynamics 365 Commerce 中创建新的在线渠道。
author: samjarawan
ms.date: 02/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: be9fafe8ece771ad6577db1cdb70af6f48e054cc
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272872"
---
# <a name="set-up-an-online-channel"></a>设置在线渠道

[!include [banner](includes/banner.md)]

本文介绍如何在 Microsoft Dynamics 365 Commerce 中创建新的在线渠道。

Dynamics 365 Commerce 支持多种零售渠道。 这些零售渠道包括在线商店、呼叫中心和零售商店（亦称实体商店）。 除了在其零售商店中购买外，在线商店还使客户可以选择从零售商的在线商店中购买产品。

要在 Commerce 中创建在线商店，必须首先创建在线渠道。 在创建新在线渠道之前，请确保已完成[渠道设置先决条件](channels-prerequisites.md)。

必须至少在 Commerce 中创建一个在线商店，才能创建新站点。 有关详细信息，请参阅[创建电子商务站点](create-ecommerce-site.md)。

## <a name="create-and-configure-a-new-online-channel"></a>创建和配置新在线渠道

要创建和配置新在线渠道，请按照以下步骤操作。

1. 在导航窗格中，转到 **模块 \> 渠道 \> 在线商店**。
1. 在操作窗格上，选择 **新建**。
1. 在 **名称** 字段中，为新渠道提供名称。
1. 在 **法人** 下拉列表中，输入适当的法人。
1. 在 **仓库** 下拉列表中，输入适当的仓库。
1. 在 **商店时区** 字段中，选择适当的时区。
1. 在 **货币** 字段中，选择适当的货币。
1. 在 **默认客户** 字段中，请提供有效的默认客户。
1. 在 **客户通讯簿** 字段中，提供有效的通讯簿。
1. 在 **功能配置文件** 字段中，选择功能配置文件（如果适用）。
1. 在 **电子邮件通知配置文件** 字段中，请提供有效的电子邮件通知配置文件。
1. 在操作窗格上，选择 **保存**。

下图显示了新在线渠道的创建过程。

![新在线渠道。](media/channel-setup-online-1.png)

下图显示了一个在线渠道示例。

![在线渠道示例。](media/channel-setup-online-2.png)

## <a name="assign-the-channel-to-a-commerce-scale-unit"></a>将渠道分配给 Commerce Scale Unit

您的新渠道必须分配给 Commerce Scale Unit。 有关说明，请参阅[配置渠道以使用 Commerce Scale Unit](../fin-ops-core/dev-itpro/deployment/initialize-retail-channels.md#configure-channels-to-use-commerce-scale-unit)。

## <a name="set-up-languages"></a>设置语言

如果您的电子商务站点将支持多种语言，请展开 **语言** 部分，并根据需要添加其他语言。

## <a name="set-up-payment-account"></a>设置付款帐户

从 **付款帐户** 部分中，您可以添加第三方付款提供商。 有关设置 Adyen Payment Connector 的信息，请参阅[适用于 Adyen 的 Dynamics 365 Payment Connector](./dev-itpro/adyen-connector.md)。

## <a name="additional-channel-setup"></a>其他渠道设置

在线渠道设置所需的其他任务包括设置付款方式、交货方式和履行组分配。

下图显示了 **设置** 选项卡上的 **交货方式**、**付款方式** 和 **履行组分配** 设置选项。

![其他在线渠道设置操作。](media/channel-setup-online-3.png)

### <a name="set-up-payment-methods"></a>设置付款方式

要设置付款方式，请针对此渠道支持的每种付款类型执行这些步骤。

1. 在操作窗格上，选择 **设置** 选项卡，然后选择 **付款方式**。
1. 在操作窗格上，选择 **新建**。
1. 在导航窗格中，选择所需的付款方式。
1. 在 **常规** 部分，提供 **操作名称** 并配置任何其他所需的设置。
1. 根据付款类型的要求配置任何其他设置。
1. 在操作窗格上，选择 **保存**。

下图显示了现金支付方式的示例。

![付款方式示例。](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a>设置交货模式

您可以从 **操作窗格** 上的 **设置** 选项卡中选择 **交货方式** 来查看已配置的交货方式。  

要更改或添加交货方式，请按照下列步骤操作。

1. 在导航窗格中，转到 **模块 \> 库存管理 \> 交货方式**。
1. 在操作窗格上，选择 **新增** 以创建新的交货方式，或选择现有方式。
1. 在 **零售渠道** 部分，选择 **添加行** 以添加渠道。 使用组织节点添加渠道而不是单独添加每个渠道可以简化渠道添加操作。

下图显示了交货方式的示例。

![设置交货模式。](media/channel-setup-retail-7.png)

### <a name="set-up-a-fulfillment-group-assignment"></a>设置履行组分配

若要设置履行组分配，请执行以下步骤。

1. 在操作窗格上，选择 **设置** 选项卡，然后选择 **履行组分配**。
1. 在操作窗格上，选择 **新建**。
1. 在 **履行组** 下拉列表中，选择一个履行组。
1. 在 **描述** 下拉列表中，输入描述。
1. 在操作窗格上，选择 **保存**。

下图显示了履行组分配设置的示例。

![设置履行组分配。](media/channel-setup-retail-9.png)

## <a name="additional-resources"></a>其他资源

[渠道概览](channels-overview.md)

[渠道设置先决条件](channels-prerequisites.md)

[设置零售渠道](channel-setup-retail.md)

[设置呼叫中心渠道](channel-setup-callcenter.md)

[适用于 Adyen 的 Dynamics 365 付款连接器](./dev-itpro/adyen-connector.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
