---
title: "配置规则"
description: "本文提供有关配置规则的一般信息。 配置规则定义使用基于维度的配置技术的产品的物料清单 (BOM) 中物料之间的关系。"
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMConfigRule
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19761
ms.assetid: e4c6622d-1e2d-4a4d-8047-c553a25d4f87
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 74c8ffe4ab00e7afa1235e24327e18a65061636a
ms.contentlocale: zh-cn
ms.lasthandoff: 05/25/2017

---

# <a name="configuration-rules"></a>配置规则

[!include[banner](../includes/banner.md)]


本文提供有关配置规则的一般信息。 配置规则定义使用基于维度的配置技术的产品的物料清单 (BOM) 中物料之间的关系。

在您定义基于维度的配置模型时，配置规则可用。 配置规则用于强制或禁止物料清单 (BOM) 的特定物料组合。 在物料清单创建后，并且相关物料分配给其各自配置组，一个或多个配置规则可以定义。 如果两个物料合成整体，**选择**运算符用于确保包含。 如果两个物料相互排斥，**取消选择**运算符用于确保排除。  

**注意：**此信息仅适用于使用基于维度的配置技术的基础产品。  

现有配置为不受配置规则后续更改的影响。 但是，在您定义新配置之前，且如果您认为规则在检查时已更改，设置规则十分重要。  

**注意：**对于**选择**方法，将自动选择派生的配置组、物料编号和配置。 对于**取消选择**方法，将不能选择派生的配置组、物料编号和配置。

<a name="see-also"></a>请参阅
--------

[基于维度的产品配置](dimension-based-product-configuration.md)




