---
title: 需求驱动型材料要求计划 (DDMRP) 概述
description: 本文提供有关需求驱动型材料要求计划 (DDMRP) 的信息，这是一种基于供需分离的计划方法。
author: t-benebo
ms.date: 06/30/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-06-30
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 31b45fdb92cf8a590ff77104f0c8015fb4d329d5
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689480"
---
# <a name="demand-driven-material-requirements-planning-ddmrp-overview"></a>需求驱动型材料要求计划 (DDMRP) 概述

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

多年来，公司使用物料需求计划 (MRP) 作为计算制造产品所需的材料和组件的方法。 但是，供应链现在已更改。 部件具有较长的提前期，因为它们越来越多地从海外采购。 因此，许多公司报告说遇到缺货或库存过剩的情况，因为他们不知道要存入多少库存。 还有更多的市场波动（有时预测不准确），客户在短提前期内需要产品。 因此，全世界都存在供应链短缺的问题。 此外，MRP 工具通常会为计划人员提供数千项待办操作。 因此，很难知道要关注的内容。 通常，许多此类问题的解决方案是切换到需求驱动型材料要求计划 (DDMRP)。

DDMRP 是一种基于供应和需求分离的计划方法。 通过设置分离点物料来实现此分离。 对于这些物料，将保留缓冲区以确保保留正确的库存量。 供需分离有助于防止“牛鞭效应”，因为不会通过链来传递可变性。 （*牛鞭效应* 是指零售层面需求的微小波动导致批发、分销商、制造商和原材料供应商层面的需求波动逐渐变大的程度。）每个缓冲区旨在保证部件的平均使用量，也可以进行调整以保证满足峰值需求。

DDMRP 已被证明是一种有价值的规划方法，适用于客户容忍时间短于累积提前期的多变环境。

## <a name="the-five-components-of-ddmrp"></a>DDMRP 的五个组件

DDMRP 具有五个序列组件（步骤）。 前三个组件实质上定义了需求驱动型物料需求计划模型的初始配置和演变配置。 最后两个组件定义方法的日常操作。

1. **[战略库存定位](ddmrp-inventory-positioning.md)** - 标识供应链网络中的分离点。 分离点是供应链中的特定点，您可以在其中放置您将监控和补充的库存缓冲区。
2. **[缓冲区配置文件和级别](ddmrp-buffer-profile-and-levels.md)** - 对于每个分离点，确定缓冲区大小（最小数量、最大数量和再订购点）和再订购数量。
3. **[动态缓冲区调整](ddmrp-buffer-profile-and-levels.md#dynamic-adjustments)** - 根据不同的运行参数或计划的未来事件调整缓冲区级别。
4. **[需求驱动型计划](ddmrp-planning.md)** - 根据需要生成供应订单。 这些供应订单包括制造订单、采购订单和存货转移单
5. **[高度协作和可见执行](ddmrp-visual-and-collaborative-execution.md)** - 借助可视化功能运行供应订单。

DDMRP 通常由具有多级物料清单 (BOM) 的制造商使用。 但是，它也可以应用于分销和零售网络。

## <a name="ddmrp-in-dynamics-365-supply-chain-management"></a>Dynamics 365 Supply Chain Management 中的 DDMRP

DDMRP 包含在 Microsoft Dynamics 365 Supply Chain Management 中，无需其他许可证费用。 在 Supply Chain Management 中，DDMRP 功能已添加到现有 **主计划** 模块。 但是，它要求您使用计划优化加载项。 

DDMRP 与 Supply Chain Management 中的现有计划设置集成，并与这些设置一起使用，以便为您的业务生成正确的计划配置。 它由一个与周期、最小值/最大值、需求等完全不同的新覆盖范围代码控制。 它不是新模块，并且不会替换现有计划功能。 但是，它确实为您提供了更多可使用的功能。
