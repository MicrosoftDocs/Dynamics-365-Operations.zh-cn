---
title: 不为 batch-above 物料考虑现有库存
description: 某些时隙模板不为 batch-above 物料考虑当前现有库存。 必须在需求订单上指定批次或序列号。
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: df5642b32f5e053144230eab3dbcf633f526279a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475688"
---
# <a name="slotting-templates-dont-consider-on-hand-inventory-for-batch-above-items"></a>时隙模板不为 batch-above 物料考虑现有库存

## <a name="symptoms"></a>故障特征

具有 *考虑现有* 时隙标准的时隙模板不考虑 *batch-above* 物料的当前现有库存。 它们仅在销售订单行上指定了批号时才考虑。

但是，当您使用 *batch-below* 物料时，将按预期考虑当前的现有库存。

有关详细信息，请参阅[仓库时隙](/dynamics365/supply-chain/warehousing/warehouse-slotting)。

## <a name="resolution"></a>解决方法

可以为 *已订购*、*已预留* 或 *已发放* 需求策略定义时隙模板标题。 对于 *已订购* 需求策略，将应用适用于预留或发放到仓库流程的相同预留层次结构要求。 因此，对于具有 *batch-above* 和 *serial-below* 预留层次结构的物料，必须在需求订单（销售或转移）上指定批号或序列号。

或者，可以使用 *已预留* 需求策略在生成仓库时隙需求之前选择批号或序列号。
