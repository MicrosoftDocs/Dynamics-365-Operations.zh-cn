---
title: 库存过帐
description: 本文提供有关战略库存定位的信息，其中涉及识别供应链中的分离点，您可以在供应链中累积现有库存，以帮助缩短提前期并吸收对供应链的冲击。
author: t-benebo
ms.date: 06/30/2022
ms.topic: article
ms.search.form: ReqGroup, EcoResProductDetailsExtended
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-06-30
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 847108575cbf7207282db00d731363c8cfad883a
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689530"
---
# <a name="inventory-positioning"></a>库存过帐

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

战略库存定位涉及标识供应链中的分离点，您可以在供应链中累积现有库存。 此方法主要用于帮助压缩提前期并吸收对供应链的冲击。 这使您可以您减轻“牛鞭效应”，因为需求可变性不会一直传递到供应链。 （*牛鞭效应* 是指零售层面需求的微小波动导致批发、分销商、制造商和原材料供应商层面的需求波动逐渐变大的程度。）

库存定位是需求驱动型材料资源计划 (DDMRP) 的第一步。

## <a name="inventory-positioning-for-manufacturing"></a>制造业的库存定位

本部分提供了一个示例，说明如果您制造典型的枕头产品，那么该如何做出库存定位决策。 枕头具有多级物料清单 (BOM)，如以下说明中所示。

![枕头产品的多级物料清单 (BOM) 示例。](media/ddmrp-bom-example.png "枕头产品的多级物料清单 (BOM) 示例")

### <a name="choose-your-decoupling-points"></a>选择您的分离点

当您选择分离点的放置位置时，请将物料清单中每个物料的以下所有方面视为条件：

- 外部可变性
- 库存利用和灵活性
- 关键运营保护
- 客户容忍时间
- 销售订单可见性区间
- 市场潜在提前期

在枕头示例中，您可能会将第一个分离点放在 *泡沫坯料* 上，原因如下：

- 很难采购用于制造泡沫坯料的材料，而且存货情况不稳定。 因此，满足了 *外部可变性* 条件。
- 除了枕头之外，泡沫坯料还可以切割成许多不同的形状和尺寸，为您制造的其他产品制造泡沫插入物。 因此，满足了 *库存利用和灵活性* 条件。

然后，您可能会将下一个分离点放在 *面料配套件*（即预剪枕头面料）上。 您可能会选择此点，因为您只有一台织物切割机。 因此，满足了 *关键运营保护* 条件。

最后，您可能会将最后一个分离点放在成品枕头产品上。 您可能会选择此点，因为您的销售 *客户容差时间* 非常短，并且您的 *销售订单可见性范围* 相当窄。 因此，您希望确保您拥有满足入站订单的现有库存量。 您还可以通过将提前期保持这么短来设置更高的价格，这是 *市场潜在提前期* 条件所指的内容。

下图根据此分析显示了枕头物料清单的外观。 黄色库存符号突出显示分离点。

![突出显示分离点的物料清单示例。](media/ddmrp-bom-decoupling-example.png "突出显示分离点的物料清单示例")

### <a name="calculate-your-decoupled-lead-time"></a>计算分离的提前期

此节显示在引入分离点后如何计算新的提前期。

在关于上一节中开始的枕头示例的下图中，提前期显示在每个物料清单组件左上角的灰色框中。 具有红色轮廓的框指示推动累计提前期的物料（物料清单每个级别的最长提前期的总和）。 从头开始时，此提前期为 21 天。

![具有提前期的物料清单示例。](media/ddmrp-bom-lead-times-example.png "具有提前期的物料清单示例")

但是，如果您应用以前选择的分离点，则分离的物料将始终有库存。 因此，它们的提前期将为 0（零）。 枕头的新提前期现在只有五天：买线用两天，生产枕头用三天。 此提前期称为 *分离的提前期*。

![分离的提前期示例。](media/ddmrp-bom-decoupled-lead-time-example.png "分离的提前期示例")

## <a name="strategic-inventory-positioning-in-a-retail-model"></a>零售模型中的战略库存定位

由于零售商仅存入成品，因此物料清单不是问题。 但是，通过根据分销网络中的存储位置设置战略库存定位和缓冲水平，零售商仍然可以使用 DDMRP。

下图显示了一个在西雅图拥有配送中心且在马萨诸塞州、亚特兰大和俄勒冈州拥有商店的公司示例。

![零售模型中基于位置的分离点。](media/ddmrp-retail-decoupl-points-example.png "零售模型中基于位置的分离点")

您可能会认为，在配送中心和商店之间移动毛毯产品的转移时间违反了您的 *客户容差时间* 条件，因为您的客户希望在他们访问时毯子有库存。 在这种情况下，您将为三个商店中的每个商店的毛毯产品设置分离点。 根据提前期、需求模式等，每个商店将具有不同的缓冲级别。

## <a name="implement-inventory-positioning-in-dynamics-365-supply-chain-management"></a>在 Dynamics 365 Supply Chain Management 中实施库存定位

本节介绍如何在 Microsoft Dynamics 365 Supply Chain Management 中实施库存定位策略。

### <a name="set-up-item-coverage-groups-that-create-decoupling-points"></a>设置创建分离点的物料覆盖范围组

当物料属于配置有 **分离点** 的 *覆盖范围代码* 值的覆盖范围组时，它们将变为分离点。 因此，DDMRP 设置过程的第一步是决定您必须为您的 DDMRP 策略实施哪些覆盖范围组，然后按照以下步骤创建它们。

1. 转至 **主计划 \> 设置 \> 覆盖范围 \> 覆盖范围组**。
1. 在“操作窗格”中，选择 **新建** 以创建覆盖范围组。
1. 输入标识覆盖范围组的信息，然后选择要使用的日历。
1. 在 **常规** 选项卡上，将 **覆盖范围代码** 字段设置为 *分离点*。 此设置将导致属于此覆盖范围组的所有物料被视为 DDMRP 的分离点。 它还为此组启用所有 DDMRP 设置，如此过程后面所述。
1. 在 **其他** 选项卡上，在 **DDMRP 参数** 部分，设置以下必填字段：

    - **提前期系数** - 指定一个系数（介于 0 和 1 之间的小数值），以控制在为此覆盖范围组中的物料计算最小和最大库存级别时提前期应产生的影响。 一般来说，物料的提前期越长，其提前期系数应越小。 较小的提前期系数会降低最小和最大库存级别，因此会导致获得更小、更频繁的订单。 DDMRP 方法建议具有长期提前期的物料的值介于 0.20 和 0.40 之间，对于具有中等提前期的物料，建议值介于 0.41 到 0.60 之间，对于具有短提前期的物料，建议值介于 0.61 到 1.00 之间。 有关详细信息，请参阅[缓冲区配置文件和级别](ddmrp-buffer-profile-and-levels.md)。
    - **可见性系数** - 指定一个系数（介于 0 和 1 之间的小数值），以控制在为此覆盖范围组中的物料计算最小库存级别时变化的需求应产生的影响。 一般来说，物料需求变化越大，其可变性系数应越大。 较大的可变性系数会产生更高的最低库存水平。 DDMRP 方法建议具有低可变性提前期的物料的值介于 0.00 和 0.40 之间，对于具有中等可变性的物料，建议值介于 0.41 到 0.60 之间，对于具有高可变性的物料，建议值介于 0.61 到 1.00 之间。 有关详细信息，请参阅[缓冲区配置文件和级别](ddmrp-buffer-profile-and-levels.md)。
    - **最小、最大和再订购点期间** - 指定计算缓冲区值的频率（*每日* 或 *每周*）。

1. 在 **其他** 选项卡上，在 **平均每日使用量** 部分，设置以下必填字段：

    - **平均每日使用量的计算基准** - 选择平均每日使用量 (ADU) 的计算基准。 选择以下值之一：

        - *过去* - 仅查看 **过去期间（天）** 字段中指定天数的过去使用情况。 ADU 的计算方法是计算期间内某一物料的总需求（以库存为单位）除以计算期间中的天数。
        - *将来* - 仅查看 **将来期间（天）** 字段中指定天数的预测将来使用情况（包括预计值）。 ADU 的计算方法是计算期间内某一物料的总需求（以库存为单位）除以计算期间中的天数。 
        - *混合* - 查看过去和将来的使用情况。 **过去期间（天）** 字段、**将来期间（天）** 字段和混合选项的设置均适用。 

            *混合 ADU* =（\[*过去加权值* × *过去的 ADU*\] + \[*将来加权值* × *将来的 ADU*\]）÷（*过去加权值* + *将来加权值*）

    - **过去期间（天）** - 输入系统在计算此覆盖范围组中的物料的 ADU 时应考虑的过去天数（截至并包括今天）。 仅当 **平均每日使用量的计算基准** 字段设置为 *过去* 或 *混合* 时，此设置才适用。
    - **将来期间（天）** - 输入系统在计算此覆盖范围组中的物料的 ADU 时应考虑的将来天数（从今天开始直到指定日）。 仅当 **平均每日使用量的计算基准** 字段设置为 *将来* 或 *混合* 时，此设置才适用。
    - **混合平均每日使用量的过去期间的相对权重** - 输入计算混合 ADU 时要应用于过去期间的权重（百分比）。 仅当 **平均每日使用量的计算基准** 字段设置为 *混合* 时，此设置才适用。
    - **混合平均每日使用量的将来期间的相对权重** - 输入计算混合 ADU 时要应用于将来期间的权重（百分比）。 仅当 **平均每日使用量的计算基准** 字段设置为 *混合* 时，此设置才适用。

1. 对于所有其他选项卡和字段，请输入用于计算与此覆盖范围组相关联的物料需求量的详细设置。

### <a name="set-an-item-as-a-decoupling-point"></a>将物料设置为分离点

若要将物料设置为分离点，请按照以下步骤操作。

1. 转到 **产品信息管理 \> 产品 \> 已发布产品**。
1. 查找并选择要为 DDMRP 设置的已发放物料。
1. 在操作窗格上，在 **计划** 选项卡上，选择 **物料覆盖范围**。
1. 在 **物料覆盖范围** 页面上，可能已列出多个物料覆盖范围记录，每个记录都适用于存储和产品维度的不同组合。 您可以选择适用于要在其中创建分离点的维度的现有物料覆盖范围记录。 或者，您可以在操作窗格上选择 **新建** 来创建新物料覆盖范围记录。
1. 像往常一样设置物料覆盖范围记录。 至少，您必须指定将应用分离点的站点和仓库。
1. 当仍选择适当的记录时，请选择 **常规** 选项卡。
1. 选中 **使用特定设置** 复选框。
1. 将 **覆盖范围组** 字段设置成为创建分离点（如上一节中所述）而设置的覆盖范围组。
1. 此物料现在已配置为分离点。 通常，当您使用 DDMRP 时，您还将在此处配置影响缓冲区大小和再订购数量的设置。 但是，您可以稍后完成该配置。 有关设置的详细信息，请参阅[设置分离点物料的缓冲区](ddmrp-buffer-profile-and-levels.md#set-up-buffers)。

> [!NOTE]
> 若要计划不是分离点的物料，请按照使用标准材料需求计划 (MRP) 时遵循的相同步骤。
