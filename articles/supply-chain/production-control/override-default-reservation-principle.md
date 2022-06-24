---
title: 替代生产中的默认材料预留原则
description: 本文介绍如何为每个物料模型组设置默认的预留原则，以可以将不同的预留原则自动应用于作为生产物料清单 (BOM) 或批次订单配方一部分的每个物料。
author: johanhoffmann
ms.date: 12/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-10
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 381b7fa5046df8f2734e4b242058eb9a673388cf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8907223"
---
# <a name="override-the-default-reservation-principle-for-materials-in-production"></a>替代生产中的默认材料预留原则

[!include [banner](../includes/banner.md)]

*替代默认生产预留* 功能可让您为每个物料模型组设置默认的预留原则。 因此，可以将不同预留原则自动应用于属于生产物料清单 (BOM) 或批次订单配方的一部分的每个物料。 您可以选择是否每个物料模型组都应替代为订单设置的默认预留原则，以及应改为为使用哪个预留原则（*手动*、*估计*、*计划*、*下达* 或 *开始*）。

创建新生产订单或批次订单时，系统会提示您选择应该应用于该订单及其所有 BOM 行或配方行的预留原则。 使用 *替代默认生产预留* 功能时，部分或全部 BOM 行或配方行可以替代该预留原则，改为使用为相关物料模型组设置的预留原则。

例如，如果您有需要执行领料工作的原材料或成分，为这些产品创建的 BOM 行或配方行将需要实际预留，因为实际预留是生成仓库工作的先决条件。 通常，如果希望预留自动执行，请选择以下预留原则之一：*估计*、*计划*、*下达* 或 *开始*。 另一方面，如果您有不需要领料的材料或成分，由于它们是直接从某个位置消耗，因此通常选择 *手动* 预留原则，这不会进行任何实际预留或产生任何领料工作。

## <a name="turn-the-override-default-production-reservation-feature-on-or-off"></a>打开或关闭替代默认生产预留功能

从 Supply Chain Management 版本 10.0.25 开始，此功能默认开启。 管理员可以通过在 [功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)工作区搜索 *替代默认生产预留* 功能来打开或关闭此功能。

## <a name="assign-a-production-reservation-policy-to-an-item-model-group"></a>将生产预留策略分配给物料模型组

1. 转到 **成本管理 \> 库存会计政策设置 \> 物料模型组**。
1. 创建或选择一个物料模型组。
1. 在 **库存策略** 快速选项卡上，选中 **替代物料生产预留** 复选框。
1. 在 **预留** 字段中，为属于所选模型组的物料选择预留原则。 （这些物料包括 BOM 行或配方行上的物料。）

    - **手动** – 模型组中的物料不会自动进行实际预留来用于生产。 但是，它们仍然可以根据需要手动预留。
    - **估计** – 在估计生产订单期间，模型组中的物料将被实际预留。
    - **计划** – 在计划生产订单期间，模型组中的物料将被实际预留。
    - **下达** – 在生产订单下达后，模型组中的物料将被实际预留。
    - **开始** – 模型组中的物料将在生产订单开始时进行实际预留。

## <a name="example-using-reservation-principles-in-a-bulkpack-scenario"></a>示例：在散装/包装场景中使用预留原则

在 1,000 升混合器中生产了大量润滑材料。 散装材料准备好后，被泵送到几个灌装站，在那里灌入不同大小的瓶子。 灌装完成后，瓶子使用箱子进行包装。 这些箱子然后再经过包装放到托盘上。

在此场景中，将创建批次订单来生产 1,000 升散装材料。 （此订单为批次订单。）此批次订单完成后，将被报告为完工入库到灌装站的材料输入位置。 然后创建灌装和包装每种瓶子尺寸的批次订单。 （这些订单是包装订单。）包装订单具有由散装材料、空瓶、标签和其他包装材料组成的配方。 由于散装材料直接从混合罐流向灌装站，因此无需执行仓库工作来选择此成分，而且散装材料直接从输入位置消耗。 所以，预留原则设置为 *手动*。 其他材料通过领料工作分批进入灌装站。 因此，这些行的预留原则设置为 *下达*，以实现在下达包装订单时自动进行预留等目的。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]