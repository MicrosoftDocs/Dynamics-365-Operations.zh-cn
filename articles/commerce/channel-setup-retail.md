---
title: 设置零售渠道
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 中创建新的零售渠道。
author: samjarawan
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 6a8db8bb4b42c7ad6c0c0e0c257bc03e356de7d525f524c22eab46e38c018d49
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6745398"
---
# <a name="set-up-a-retail-channel"></a>设置零售渠道

[!include [banner](includes/banner.md)]

此主题介绍如何在 Microsoft Dynamics 365 Commerce 中创建新的零售渠道。

Dynamics 365 Commerce 支持多种零售渠道。 这些零售渠道包括在线商店、呼叫中心和零售商店（亦称实体商店）。 每个零售商店渠道都可以有自己的付款方式、价格组、销售点 (POS) 收银机、收入帐户和支出帐户以及职员。 您必须先设置所有这些元素，然后才能创建零售商店渠道。 

在创建零售渠道之前，请确保满足[渠道先决条件](channels-prerequisites.md)。

## <a name="create-and-configure-a-new-retail-channel"></a>创建和配置新零售渠道

1. 在导航窗格中，转到 **模块 \> 渠道 \> 商店 \> 所有商店**。
1. 在操作窗格上，选择 **新建**。
1. 在 **名称** 字段中，为新渠道提供名称。
1. 在 **商店编号** 字段中，提供唯一的商店编号。 该编号可以是字母数字，最多 10 个字符。
1. 在 **法人** 下拉列表中，输入适当的法人。
1. 在 **仓库** 下拉列表中，输入适当的仓库。
1. 在 **商店时区** 字段中，选择适当的时区。
1. 在 **销售税组** 下拉列表中，为商店选择适当的销售税组。
1. 在 **货币** 字段中，选择适当的货币。
1. 在 **客户通讯簿** 字段中，提供有效的通讯簿。
1. 在 **默认客户** 字段中，请提供有效的默认客户。
1. 在 **功能配置文件** 字段中，选择功能配置文件（如果适用）。
1. 在 **电子邮件通知配置文件** 字段中，请提供有效的电子邮件通知配置文件。
1. 在操作窗格上，选择 **保存**。

下图显示了新零售渠道的创建过程。

![新零售渠道。](media/channel-setup-retail-1.png)

下图显示了一个零售渠道示例。

![零售渠道示例。](media/channel-setup-retail-2.png)

## <a name="other-settings"></a>其他设置

可以在 **报表/结算** 和 **杂项** 部分中根据零售商店的需求设置许多其他可选设置。

另外，请参阅 [销售点 (POS) 的屏幕布局](pos-screen-layouts.md)，了解有关在 **屏幕布局** 部分中设置默认屏幕布局的信息；参阅 [配置和安装 Retail 硬件工作站](retail-hardware-station-configuration-installation.md)，了解有关 **硬件工作站** 部分的设置信息。

下图显示了一个零售渠道设置配置示例。

![零售渠道配置示例。](media/channel-setup-retail-3.png)

## <a name="additional-channel-set-up"></a>其他渠道设置

可以在操作窗格上 **设置** 部分下找到需要为渠道设置的其他项。

在线渠道设置所需的其他任务包括设置付款方式、现金申报、交货方式、收入/费用帐户、部门、履行组分配和金库。

下图显示了 **设置** 选项卡上的各个其他零售渠道设置选项。

![设置渠道。](media/channel-setup-retail-4.png)

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

### <a name="set-up-cash-declaration"></a>设置现金清点

1. 在操作窗格上，选择 **设置** 选项卡，然后选择 **现金清点**。
1. 在操作窗格上，选择 **新增**，然后创建所有适用的 **硬币** 和 **纸币** 面额。

下图显示了现金清点的示例。

![设置现金清点。](media/channel-setup-retail-6.png)

### <a name="set-up-modes-of-delivery"></a>设置交货模式

您可以从操作窗格上的 **设置** 选项卡中选择 **交货方式** 来查看已配置的交货方式。  

要更改或添加交货方式，请按照下列步骤操作。

1. 在导航窗格中，转到 **模块 \> 库存管理 \> 交货方式**。
1. 在操作窗格上，选择 **新建** 创建新的交货方式，或选择现有方式。
1. 在 **零售渠道** 部分，选择 **添加行** 以添加渠道。 使用组织节点添加渠道而不是单独添加每个渠道可以简化渠道添加操作。

下图显示了交货方式的示例。

![设置交货模式。](media/channel-setup-retail-7.png)

### <a name="set-up-incomeexpense-account"></a>设置收入/支出帐户

要设置收入/支出帐户，请执行以下步骤。

1. 在操作窗格上，选择 **设置** 选项卡，然后选择 **收入/支出帐户**。
1. 在操作窗格上，选择 **新建**。
1. 在 **名称** 下面，输入名称。
1. 在 **搜索名称** 下面，输入搜索名称。
1. 在 **帐户类型** 下面，输入帐户类型。
1. 根据需要在 **消息行 1**、**消息行 2**、**票单文本 1** 和 **票单文本 2** 中输入文字。
1. 在 **过帐** 下面，输入过帐信息。
1. 在操作窗格上，选择 **保存**。

下图显示了收入/支出帐户的示例。

![设置收入/支出帐户。](media/channel-setup-retail-8.png)

### <a name="set-up-sections"></a>设置部门

要设置部门，请按照以下步骤操作。

1. 在操作窗格上，选择 **设置** 选项卡，然后单击 **部门**。
1. 在操作窗格上，选择 **新建**。
1. 在 **部门编号** 下面，输入部门编号。
1. 在 **描述** 下面，输入描述。
1. 在 **部门规模** 下面，输入部门规模。
1. 根据需要针对 **常规** 和 **销售统计** 配置其他设置。
1. 在操作窗格上，选择 **保存**。

### <a name="set-up-a-fulfillment-group-assignment"></a>设置履行组分配

若要设置履行组分配，请执行以下步骤。

1. 在操作窗格上，选择 **设置** 选项卡，然后选择 **履行组分配**。
1. 在操作窗格上，选择 **新建**。
1. 在 **履行组** 下拉列表中，选择一个履行组。
1. 在 **描述** 下拉列表中，输入描述。
1. 在操作窗格上，选择 **保存**

下图显示了履行组分配设置的示例。

![设置履行组分配。](media/channel-setup-retail-9.png)

### <a name="set-up-safes"></a>设置金库

要设置金库，请按照以下步骤操作。

1. 在操作窗格上，选择 **设置** 选项卡，然后单击 **金库**。
1. 在操作窗格上，选择 **新建**。
1. 输入金库的名称
1. 在操作窗格上，选择 **保存**。

### <a name="ensure-unique-transaction-ids"></a>确保交易 ID 是唯一的

从 Commerce 版本 10.0.18 开始，为销售点 (POS) 生成的交易 ID 采用序列形式，包括以下部分：

- 固定部分，商店 ID 和终端 ID 的串联。 
- 序列部分，一个数字序列。 

具体来说，格式为 *{store}-{terminal}-{numbersequence}*。 

由于可以在脱机和联机模式下生成交易 ID，因此已经存在生成重复交易 ID 的情况。 消除重复的交易 ID 需要进行大量的手动数据修复。 

在 Commerce 版本 10.0.19 中，交易 ID 格式已更新，删除了序列部分，改为使用通过计算自 1970 年以来的时间（以毫秒为单位）生成的 13 位数字。 进行此更改后，新的交易 ID 格式为 *{store}-{terminal}-{millisecondsSince1970}*。 此更新使交易 ID 不再序列化，确保交易 ID 始终是唯一的。 

> [!NOTE]
> 交易 ID 仅用于内部系统，因此不需要序列化。 但是，很多国家/地区要求收据 ID 采用序列形式。

可以从 **功能管理** 工作区启用新交易 ID 格式功能。 

若要启用新的交易 ID，请按照下列步骤操作：

1. 在 Commerce Headquarters 中，转到 **系统管理 \> 工作区 \> 功能管理**。
1. 筛选“retail 和 commerce”模块。
1. 搜索 **启用新交易 ID 以避免交易 ID 重复** 功能名称。
1. 选择该功能，然后在右窗格中选择 **立即启用**。  
1. 转到 **Retail 和 Commerce \> Retail 和 Commerce IT \> 分配计划**。
1. 运行 **1070 渠道配置** 和 **1170 POS 任务录制器** 作业，将已启用的功能同步到商店。
1. 将更改发送到商店后，必须关闭 POS 终端，然后重新打开才能使用新交易 ID 格式。 

> [!NOTE]
> 启用新交易 ID 格式功能后，您将无法禁用此功能。 如果必须禁用，请联系 Commerce 支持。

## <a name="additional-resources"></a>其他资源

[渠道概览](channels-overview.md)

[渠道设置先决条件](channels-prerequisites.md)

[设置在线渠道](channel-setup-online.md)

[设置呼叫中心渠道](channel-setup-callcenter.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
