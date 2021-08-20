---
title: 启用和配置按渠道自动收费
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 中启用和配置按渠道自动收费。
author: gvrmohanreddy
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-03-01
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: d905819d1e0c8223c74509bfb357b3aaa51d20305a2857061eadb0b0ff8f6b9b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6727622"
---
# <a name="enable-and-configure-auto-charges-by-channel"></a>按渠道启用和配置自动费用

此主题介绍如何在 Microsoft Dynamics 365 Commerce 中启用和配置按渠道自动收费。

## <a name="overview"></a>概览

有时可能必须为在特定省/直辖市/自治区州（如加利福尼亚州）所有或部分商店销售的一组产品收取回收费获取其他费用。 可通过 Commerce 中的 **启用按渠道筛选自动收费** 功能指定按渠道自动收费（例如，特定实体店渠道）。 Dynamics 365 Commerce 版本 10.0.10 及更高版本中提供此功能。

若要启用和配置按渠道自动收费，必须完成以下任务：

- 开启 **启用筛选按渠道自动收费** 功能。
- 配置组织层次结构目的。
- 定义按渠道自动收费。

> [!NOTE]
> 只有也开启了高级自动收费功能，**启用筛选按渠道自动收费** 功能才有效。 有关如何开启高级自动收费功能的信息，请参阅[全渠道高级自动收费](omni-auto-charges.md)。

## <a name="turn-on-the-enable-filter-auto-charges-by-channel-feature"></a>开启启用筛选按渠道自动收费功能

若要在 Commerce 中启用按渠道自动收费，请执行以下步骤。

1. 转到 **系统管理员 \> 工作区 \> 功能管理**。
1. 在 **未启用** 选项卡的 **功能名称** 列表中，找到并选中了 **启用筛选按渠道自动收费**。
1. 在右下角，选择 **立即启用**。 此功能在启用之后，将在 **所有** 选项卡中显示。
1. 转到 **Retail 和 Commerce \> Retail 和 Commerce IT \> 分配计划**。
1. 在左窗格中，找到并选择 **1110**（**全局配置**）作业。
1. 在操作窗格上，选择 **立即运行** 传播配置更改。

> [!WARNING]
> 如果要在已使用 **启用筛选按渠道自动收费** 功能之后将其关闭，**自动收费** 下的 **零售渠道关系** 字段将不再显示，而您将失去所有现有配置。 如果删除 **零售渠道关系** 配置导致自动收费规则重复出现，尝试关闭此功能将失败。 关闭此功能之前，请务必检查所有自动收费功能并进行所有必需更改。

## <a name="configure-the-organization-hierarchy-purpose"></a>配置组织层次结构目的

已创建了一个名称为 **零售自动收费** 的新组织层次结构目的，用于管理按渠道自动收费层次结构。

若要在 Commerce 中为组织层次结构目的分配默认层次结构，请执行以下操作。
        
1. 转到 **组织管理 \> 组织 \> 组织层次结构目的**。
1. 在左窗格中，选择 **零售自动收费**。
1. 在 **分配的层次结构** 下，选择 **添加**。
1. 在 **组织层次结构** 对话框中，选择一个组织层次结构（例如，**零售商店(按地区)**），然后选择 **确定**。
1. 在 **分配的层次结构** 下，选择 **设置为默认值**。
1. 转到 **Retail 和 Commerce \> Retail 和 Commerce IT \> 分配计划**。
1. 在左窗格中，找到并选择 **1040**（**产品**）作业。
1. 在操作窗格上，选择 **立即运行**。
1. 重复前两个步骤运行 **1070**（**渠道配置**）和 **1110**（**全局配置**）作业。

![零售自动费用组织层次结构目的的配置。](media/Auto-charges-org-hierarchy-purpose.png)

## <a name="define-auto-charges-by-channel"></a>定义按渠道自动收费

开启 **启用按渠道筛选自动收费** 功能并配置 **零售自动收费** 组织层次结构目的之后，可以按订单头级别或订单行级别定义按渠道自动收费。

若要在 Commerce 中定义按渠道自动收费，请执行以下步骤。

1. 转到 **应收帐款 \> 费用设置 \> 自动费用**。
1. 在左窗格的 **级别** 字段中，选择 **头** 或 **行**，具体取决于您的业务要求。
1. 在 **零售渠道代码** 字段中，选择相应渠道代码（例如，**表** 或 **组**）。 如果使用默认设置 **所有**，则将把费用规则应用于所有渠道。

    - 如果选择 **组**，请确保在 **Retail 和 Commerce \> 渠道设置 \> 费用 \> 零售渠道费用组** 中创建零售渠道费用组。
    - 如果选择 **表**，则可在 **零售渠道关系** 字段中选择特定渠道（如 **San Francisco**）。

1. 转到 **Retail 和 Commerce \> Retail 和 Commerce IT \> 分配计划**。
1. 在左窗格中，找到并选择 **1040**（**产品**）作业。
1. 在操作窗格上，选择 **立即运行**。
1. 重复前两个步骤运行 **1070**（**渠道配置**）和 **1110**（**全局配置**）作业。
    
![按渠道定义的自动费用。](media/Auto-charges-line-charge-by-channel.png)

## <a name="example-scenario"></a>示例场景

以下示例概述配置产品以便在通过 San Francisco 实体店渠道销售产品时收取回收费需要执行的步骤。 此示例还显示自动费用在 Commerce 销售点 (POS) 应用程序中如何显示。

组织定义一个名称为 **RECYCLE** 的费用代码，如下图中所示。

![RECYCLE 费用代码。](media/Auto-charges-charge-code.png)

将在行级别创建一项自动费用。 它具有以下配置：

- **帐户代码** 字段设置为 **所有**。
- **物料代码** 字段设置为 **表**。
- **物料关系** 字段设置为物料 ID **91001**。
- **交货方式代码** 字段设置为 **所有**。
- **零售渠道代码** 字段设置为 **表**。
- **零售渠道关系** 字段设置为 **San Francisco** 商店。

将创建一个自动费用行。 它具有以下配置：

- **货币** 字段设置为 **USD**。
- **费用代码** 字段设置为 **RECYCLE**。
- **类别** 字段将设置为 **固定**。
- **费用** 字段设置为 **$6.25**。

![行级别自动费用和自动费用行的配置。](media/Auto-charges-recyclingfee-line-fee.png)

在 POS 应用程序中，将在 **San Francisco** 商店渠道中创建一个销售订单。 **费用** 行显示回收费为 **$6.25**。

可通过在 POS 应用程序中选择 **交易记录选项 \> 费用 \> 管理费用** 查看这笔回收费的费用代码和说明。

![POS 应用程序中的回收费。](media/pos-auto-charges-recyclingfee-line-fee.png)

## <a name="additional-resources"></a>其他资源

[全渠道高级自动费用](omni-auto-charges.md)

[将标头费用按比例分配给匹配的销售行](pro-rate-charges-matching-lines.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]