---
title: 工程更改管理概述（包含视频）
description: 本文概述了工程更改管理，可帮助您计划和管理产品版本控制以及管理产品生命周期和工程更改。
author: t-benebo
ms.date: 08/09/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: a01dfd72428c75d1bb24f32c73c9c799a6c5017e
ms.sourcegitcommit: b3579ac62e1ea15664a114abcc2409cad76d4f19
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/14/2022
ms.locfileid: "9682498"
---
# <a name="engineering-change-management-overview"></a>工程更改管理概述

[!include [banner](../includes/banner.md)]

## <a name="feature-summary"></a>功能汇总

当今的制造商需要强大的产品数据管理、版本控制和工程更改管理，才能在不断缩短的产品生命周期、不断提高的质量和可靠性要求以及日益增加的产品安全关注的世界中取得成功。

工程更改管理为产品数据管理流程带来了结构和规范，让产品能够以工作流支持的受控方式定义、发布和修订。 通过产品版本和工程更改管理，您可以在产品的整个生命周期内记录、评估影响和应用工程更改。

工程更改管理可帮助您计划和管理产品版本控制以及管理产品生命周期和工程更改。 以下是其主要功能的列表：

- 产品版本控制
- 增强的产品发布功能让您可以在一个法人（工程公司）中维护基础产品，然后将完全配置的已发布产品发布到其他法人
- 在产品版本激活之前验证是否输入所需信息的规则（准备情况检查）
- 通过对已发布产品可以在特定业务流程中使用的时间进行细粒度控制，改进了产品生命周期管理
- 工作流支持的工程更改请求
- 工作流支持的工程更改订单

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4HE6B]

前面的视频（[Dynamics 365 Supply Chain Management 中的更改管理功能](https://youtu.be/N313FqvRuBc)）包含在 YouTube 上提供的 [财务和运营播放列表](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW)中。

## <a name="turn-on-the-engineering-change-management-features-for-your-system"></a>为系统开启工程更改管理功能

必须同时启用 *工程更改管理* 功能及其配置密钥，然后才能够使用工程更改管理。 如果您还想要跟踪交易中产品的版本维度（可选），还必须启用 *产品版本维度* 功能及其配置密钥。 根据需要设置这些必备项后，就可以为工程更改管理开启更多可选功能。

### <a name="turn-the-basic-engineering-change-management-features-on-or-off"></a>打开或关闭基本工程更改管理功能

要打开或关闭基本工程更改管理功能，请按照以下步骤操作。 从 Supply Chain Management 版本 10.0.25 开始，*工程更改管理* 功能默认开启。

1. 转到[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)工作区。
1. 检查更新。
1. 根据需要打开或关闭名为 *工程更改管理* 的功能。
1. 如果您还想要跟踪交易中产品的版本维度（可选），打开名为 *产品版本维度* 的功能。

### <a name="turn-the-required-configuration-keys-on-or-off"></a>打开或关闭必需的配置键

接下来，按照以下步骤打开配置密钥。 这些功能默认不打开。

1. 将您的系统置于维护模式下，如[维护模式](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md)中所述。
1. 转到 **系统管理 \> 设置 \> 许可证配置**。
1. 展开 **贸易** 节点。
1. 使用 **工程更改管理** 复选框启用或禁用主要功能的配置键。
1. 展开 **工程更改管理** 节点，根据需要选择或清除以下复选框（取决于您要使用的功能）：

    - **属性搜索** – 选中此复选框将启用[属性搜索功能](engineering-attributes-and-search.md)。 我们建议启用此功能，但是如果您不使用它，可以清除此复选框。
    - **处理制造的更改管理** – 如果要使用工程更改管理功能管理处理制造配方的更改，请选中此复选框。 如果您不必管理配方，可以清除此复选框。 有关详细信息，请参阅[管理配方及其成分的更改](manage-formula-changes.md)。

1. 如果您还想使用版本维度，还要选中 **产品维度 - 版本** 复选框。 （此复选框在列表再下面，不是嵌套在 **工程更改管理** 节点下。）如果您不需要此功能，可以清除此复选框。
1. 关闭维护模式，如[维护模式](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md)中所述。
1. 必须同步数据库以确保正确更新配置键以反映您的更改。 执行以下步骤之一，具体取决于您所使用的环境类型：
    - **对于第 1 层（开发）环境**：在 Microsoft Visual Studio 中打开您的项目，然后选择 **Dynamics 365 \> 同步数据库 \> 同步**。
    - **对于第 2 层（及更高）环境**：将环境置于维护模式和退出维护模式后，数据库会自动同步，因此您可以跳过此步骤。

> [!NOTE]
> 要使用工程更改管理，必须在 **编号规则** 页面将物料清单编号规则和配方编号规则（如果您使用的是配方）设置为 *自动*。

### <a name="turn-on-additional-engineering-change-management-features"></a>开启更多工程更改管理功能

开启基本工程更改管理功能并启用其配置密钥后，将向功能管理添加一些其他和可选的工程更改管理功能。 **工程更改管理** 模块下列出了所有这些功能。 下表介绍各项可选功能，并提供有关详细信息的链接。

| 功能管理中的功能名称 | Description | 功能状态 |
|---|---|---|
| 对现有产品启用更改管理 | <p>利用此功能，您可以将现有产品转换为工程产品，这样就可以通过使用工程更改管理开始管理这些产品。</p><p>有关详细信息，请参阅[对现有产品启用更改管理](change-management-existing-products.md)。</p> | 从版本 10.0.25 开始默认开启。 |
| 面向生产部门的工程通知 | <p>在工程中更改产品时，向生产方通知这些更改可能非常重要。 这样，生产工作人员就可以采取适当的操作，例如，更换组件、替换物料清单 (BOM)，或替换工艺路线。 利用此功能，您可以向生产方通知对正在生产的产品进行的更改。</p><p>有关详细信息，请参阅[管理工程产品的更改](engineering-change-management.md)。</p> |  从版本 10.0.25 开始默认开启。 |
| 工程更改管理的已改进属性继承 | <p>此功能可以简化对成品或中间物料的属性管理。 开启此功能后，可以更轻松地确定属于物料的所有属性，并且可以选择应从该物料传播到其父物料的属性。 此功能非常有用，例如，某个成品的一个组件易碎，有毒或易燃，因为您可以轻松识别易碎、有毒或易燃属性并传播到成品。</p><p>有关详细信息，请参阅[工程属性和工程属性搜索](engineering-attributes-and-search.md)。</p> |  从版本 10.0.25 开始默认开启。 |
| 产品准备情况检查 | <p>此功能允许您为标准（非工程）产品设置就绪情况检查。 产品就绪情况检查用于确保每个产品在提供到交易记录中并使用之前，已完全定义，并且配置了所有必需策略。 如果在使用此功能一段时间后将其禁用，则将删除标准产品的所有现有准备情况检查。</p><p>有关详细信息，请参阅[产品准备](product-readiness.md)。</p> |  从版本 10.0.25 开始默认开启。 |
| 管理对配方及其成分的更改 | <p>利用此功能，您可以跟踪对配方成分、联产品和副产品的更改。</p><p>有关详细信息，请参阅[管理配方及其成分的更改](manage-formula-changes.md)。</p> |  从版本 10.0.25 开始默认开启。 |
| 生成工程产品的变型 | <p>利用此功能，您可以根据可用维度值生成工程产品的变型。</p><p>有关详细信息，请参阅[生成工程产品的变型](engineering-variants.md)。</p> |  从版本 10.0.25 开始默认开启。 |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

