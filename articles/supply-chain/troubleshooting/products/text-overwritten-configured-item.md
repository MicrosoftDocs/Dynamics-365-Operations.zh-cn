---
title: 在销售订单行上配置物料时会覆盖文本
description: 在销售订单行上配置产品时，将使用标准文本覆盖修改后的文本。 请在配置行之前，而不是之后更改文本。
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 20239b9b0eecb355274e909a8b8b39450e468c7e
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475642"
---
# <a name="item-text-is-overwritten-when-a-product-is-configured-on-a-sales-order-line"></a>在销售订单行上配置产品时会覆盖物料文本

## <a name="symptoms"></a>故障特征

当您为可配置物料创建销售订单行，然后修改物料文本时，会发生此问题。 当您配置物料，然后选择 **确定** 时，文本会被标准文本覆盖。

## <a name="resolution"></a>解决方法

此行为是预期的。 文本字段包含变型名称，仅在您配置行后填充。 因此，您必须在配置行之后而不是在之前更改文本。
