---
title: 集成税务
description: 本主题介绍 Finance and Operations 与 Common Data Service 之间的税务数据集成。
author: robinarh
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ''
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 69521ec8c664a7025050c94105eca58f7f2c5c00
ms.sourcegitcommit: 7d943499f302298c6ff127f56cecc34af6cee289
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/08/2020
ms.locfileid: "3435552"
---
# <a name="integrated-tax"></a>集成税务

[!include [banner](../../includes/banner.md)]



税务设置数据定义间接税（增值税、GST、销售税）和预缴税金的设置。 它描述了税金计算规则、税率、税务核算、结算和其他概念。

## <a name="templates"></a>模板

税务数据包括实体映射的集合，这些映射在数据交互期间协同工作，如下表所示。

Finance and Operations 应用 | Dynamics 365 中的模型驱动应用 | 说明 |
-------------------------|---------------------------------|----|
销售税(物料)组 | msdyn_taxitemgroups |
销售税主管机构 | msdyn_taxauthorities |
免税(销售税)代码实体 CDS | msdyn_taxexemptcodes |
销售税组 | msdyn_taxgroups |
销售税分类帐过帐组 V2 | msdyn_taxpostinggroups |
预缴税金代码 | msdyn_withholdingtaxcodes |
预缴税金组 | msdyn_withholdingtaxgroups | 


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

