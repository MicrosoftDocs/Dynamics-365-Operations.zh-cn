---
title: 位置模板不允许负库存，但允许负现有库存量
description: 位置模板的“允许负库存”选项设置为“否”，但系统仍允许负现有库存量。
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WHSLocationProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: shawan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 356d2dd7853bf93250e14eb9bd28a8a145794584
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026301"
---
# <a name="location-profile-disallows-negative-inventory-but-negative-on-hand-inventory-is-permitted"></a>位置模板不允许负库存，但允许负现有库存量

知识库编号：4613622

## <a name="symptoms"></a>故障特征

位置模板的 **允许负库存** 选项设置为 *否*，但系统仍允许负现有库存量。

## <a name="example-scenario"></a>示例场景

对于政府监管的交易，系统必须能够在帐面亏损中记录负库存。 您希望某个物料能够显示负库存，但只是在指定位置，如油罐。 但是，如果物料模型组允许负库存，您会发现位置是否设置为允许负库存都没有影响。 如果设置了物料，以不允许负库存，如何设置位置模板则无关紧要。

## <a name="resolution"></a>解决方法

位置模板中的 **允许负库存** 设置仅适用于仓库流程，如领料。 但是，设置为允许负库存的物料模型组会影响库存管理和仓库管理模块中的所有流程，位置模板不会替代此设置。

您可以控制是否允许仓库支持负库存。 将物料模型组设置为不允许负实际库存，仅将相关仓库设置为允许负库存。
