---
title: 工程更改管理概述
description: 此主题概述了工程更改管理，可帮助您计划和管理产品版本控制以及管理产品生命周期和工程更改。
author: t-benebo
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 8f2d577d9e48ced9d4c516a66e4f53671417875cbfb51bd6bdc2cb0938d83c01
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6714948"
---
# <a name="engineering-change-management-overview"></a>工程更改管理概述

[!include [banner](../includes/banner.md)]

## <a name="feature-summary"></a>功能汇总

当今的制造商需要强大的产品数据管理、版本控制和工程更改管理，才能在不断缩短的产品生命周期、不断提高的质量和可靠性要求以及日益增加的产品安全关注的世界中取得成功。

工程更改管理为产品数据管理流程带来了结构和规范，让产品能够以工作流支持的受控方式定义、发布和修订。通过产品版本和工程更改管理，您可以在产品的整个生命周期内记录、评估影响和应用工程更改。

工程更改管理可帮助您计划和管理产品版本控制以及管理产品生命周期和工程更改。 以下是其主要功能的列表：

- 产品版本控制
- 增强的产品发布功能让您可以在一个法人（工程公司）中维护基础产品，然后将完全配置的已发布产品发布到其他法人
- 在产品版本激活之前验证是否输入所需信息的规则（准备情况检查）
- 通过对已发布产品可以在特定业务流程中使用的时间进行细粒度控制，改进了产品生命周期管理
- 工作流支持的工程更改请求
- 工作流支持的工程更改订单

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4HE6B]

前面的视频（[Dynamics 365 Supply Chain Management 中的更改管理功能](https://youtu.be/N313FqvRuBc)）包含在 YouTube 上的 [Finance and Operations 播放列表](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW)中。

## <a name="turn-on-the-engineering-change-management-and-version-dimension-features-for-your-system"></a>为系统打开工程更改管理和版本维度功能

必须同时启用 *工程更改管理* 功能及其配置密钥，然后才能够使用工程更改管理。 如果您还想要跟踪交易中产品的版本维度（可选），还必须启用 *产品版本维度* 功能及其配置密钥。

首先，按照以下步骤打开这些功能。

1. 转到[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)工作区。
1. 检查更新。
1. 开启名为 *工程更改管理* 的功能。
1. 如果要使用它，还要打开名为 *产品维度版本* 的功能。

接下来，按照以下步骤打开配置密钥。

1. 将您的系统置于维护模式下，如[维护模式](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md)中所述。
1. 转到 **系统管理 \> 设置 \> 许可证配置**。
1. 展开 **贸易** 节点。
1. 选中 **工程更改管理** 复选框，启用主要功能的 Configuration Key。
1. 展开 **工程更改管理** 节点，根据需要选择或清除以下复选框（取决于您要使用的功能）：

    - **属性搜索** – 选中此复选框将启用[属性搜索功能](engineering-attributes-and-search.md)。 我们建议启用此功能，但是如果您不使用它，可以清除此复选框。
    - **处理制造的更改管理** – 如果要使用工程更改管理功能管理处理制造配方的更改，请选中此复选框。 如果您不必管理配方，可以清除此复选框。 有关详细信息，请参阅[管理配方及其成分的更改](manage-formula-changes.md)。

1. 如果您还想使用版本维度，还要选中 **产品维度 - 版本** 复选框。 （此复选框在列表再下面，不是嵌套在 **工程更改管理** 节点下。）
1. 关闭维护模式，如[维护模式](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md)中所述。

> [!IMPORTANT]
> 从 2022 年 4 月开始，默认情况下，所有新安装的 **工程更改管理** 和 **产品维度 - 版本** 的许可证密钥都将启用，但是如果需要，您仍然可以将其禁用。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
