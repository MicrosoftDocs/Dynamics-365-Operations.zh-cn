---
title: 仓库批次和序列预留层次结构故障排除
description: 本主题介绍如何解决在处理使用批次或序列维度的预留层次结构时可能遇到的常见问题。
author: perlynne
ms.date: 3/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 3/12/2021
ms.openlocfilehash: a1abb6f8657484d43d434076e5ee38d1c63fe2ff
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838170"
---
# <a name="troubleshoot-warehouse-batch-and-serial-reservation-hierarchies"></a>仓库批次和序列预留层次结构故障排除

[!include [banner](../includes/banner.md)]

本主题介绍如何解决在处理使用批次或序列维度的预留层次结构时可能遇到的常见问题。

有关详细信息，请参阅[灵活的仓库级维度预留策略](flexible-warehouse-level-dimension-reservation.md)。

物料的预留层次结构指示，必须满足存储维度的要求才能将库位分配到需求订单。 对于在分配库位之前必须满足的所有维度，这些维度可以描述为 *库位上方的维度*；对于可以在库位分配到需求订单之后分配的维度，这些维度可以描述为 *库位下方的维度*。 这些预留层次结构也称为 *batch-above* 和 *batch-below* 预留层次结构，或者 *serial-above* 和 *serial-below* 预留层次结构。

仅在库位上方的维度中没有间隙时才能成功分配库存。 例如，在 *batch-above* 预留层次结构中，您希望在需求订单上指定 **场地**、**仓库** 和 **批号** 维度。 如果缺少其中任何维度，分配流程将失败。 相反，在 *batch-below* 或 *serial-below* 预留层次结构中，可能在需求订单上指定批号或序列号，但分配流程不需要它。

## <a name="i-receive-the-following-error-message-to-be-assigned-to-wave-load-lines-must-specify-the-dimensions-above-the-location-to-assign-these-dimensions-reserve-and-recreate-the-load-line"></a>我收到以下错误消息：“要分配到波次，负荷行必须指定位置以上的维度。 要分配这些维度，请预留并重新创建负荷行。”

### <a name="issue-description"></a>问题描述

当您使用具有 *batch-above* 预留层次结构的物料时，如果尝试发放部分数量的装载，**装载计划工作台** 页面的 **发放到仓库** 命令将不起作用。 您将收到此错误消息，而且不会为部分数量创建工作。

但是，当您使用具有 *batch-below* 预留层次结构的物料时，您可以从 **装载计划工作台** 页面发放部分数量的装载。

### <a name="issue-cause"></a>问题原因

当某个维度在预留层次结构中位于 **库位** 维度上方时，必须在发放到仓库之前指定该维度。 如果未指定一个或多个 **位置** 以上维度，部分数量无法发放。

## <a name="the-auto-reservation-prompt-for-a-batch-number-is-triggered-even-though-there-is-available-inventory"></a>即使有可用库存，也会触发批号的自动预留提示。

### <a name="issue-description"></a>问题描述

当您在未启用仓库流程但启用了自动预留的仓库中使用具有 *batch-above* 预留层次结构的物料时，即使只有一个批次可供领料，也会显示批号的自动预留提示。

但是，当您在启用了仓库流程的仓库中使用同一物料时，不会显示自动预留提示。

### <a name="issue-cause"></a>问题原因

如果预留层次结构定义为 *batch-above* 或 *serial-above* ，必须始终在需求订单上指定引用的维度（**批号** 或 **序列号**）。 如果单个批号或序列号可用，则仓库流程可能能够完成信息。 但是，由于没有为仓库流程启用仓库，因此用户必须始终指定 **库位** 上方的所有维度。

## <a name="slotting-templates-that-have-the-consider-on-hand-slot-criterion-dont-consider-current-on-hand-inventory-for-batch-enabled-items"></a>具有“考虑现有”时隙标准的时隙模板不考虑启用批次的物料的当前现有库存。

有关详细信息，请参阅[仓库时隙](warehouse-slotting.md)。

### <a name="issue-description"></a>问题描述

具有 *考虑现有* 时隙标准的时隙模板不考虑 *batch-above* 物料的当前现有库存。 它们仅在销售订单行上指定了批号时才考虑。

但是，当您使用 *batch-below* 物料时，将按预期考虑当前的现有库存。

### <a name="issue-cause"></a>问题原因

可以为 *已订购*、*已预留* 或 *已发放* 需求策略定义时隙模板标题。 对于 *已订购* 需求策略，将应用适用于预留或发放到仓库流程的相同预留层次结构要求。 因此，对于具有 *batch-above* 和 *serial-below* 预留层次结构的物料，必须在需求订单（销售或转移）上指定批号或序列号。 或者，可以使用 *已预留* 需求策略在生成仓库时隙需求之前选择批号或序列号。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
