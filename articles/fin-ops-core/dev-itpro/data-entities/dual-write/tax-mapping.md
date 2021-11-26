---
title: 集成税务
description: 本主题介绍 Finance and Operations 与 Dataverse 之间的税务数据集成。
author: tonyafehr
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: tfehr
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: d1e74bbbeba019ca48dd823b58251643e96edd0c
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/10/2021
ms.locfileid: "7782202"
---
# <a name="integrated-tax"></a>集成税务

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

税务设置数据定义间接税（增值税、GST、销售税）和预缴税金的设置。 它描述了税金计算规则、税率、税务核算、结算和其他概念。

## <a name="templates"></a>模板

税务数据包括表映射的集合，这些映射在数据交互期间协同工作，如下表所示。

| Finance and Operations 应用 | 客户互动应用 | 说明 |
|-----------------------------|-----------------------------------|-------------|
[物料销售税组](mapping-reference.md#196) | msdyn_taxitemgroups | |
[销售税主管机构](mapping-reference.md#193) | msdyn_taxauthorities | |
[免税(销售税)代码实体 CDS](mapping-reference.md#194) | msdyn_taxexemptcodes | |
[销售税组](mapping-reference.md#195) | msdyn_taxgroups | |
[销售税分类帐过帐组 V2](mapping-reference.md#197) | msdyn_taxpostinggroups | |
[预缴税金代码](mapping-reference.md#210) | msdyn_withholdingtaxcodes | |
[预缴税金组](mapping-reference.md#211) | msdyn_withholdingtaxgroups | |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
