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
ms.openlocfilehash: a4da37d45698290b40f6c72148f1500bef72127a
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173077"
---
# <a name="integrated-tax"></a>集成税务

[!include [banner](../../includes/banner.md)]



税务设置数据定义间接税（增值税、GST、销售税）和预缴税金的设置。 它描述了税金计算规则、税率、税务核算、结算和其他概念。

## <a name="templates"></a>模板

税务数据包括实体映射的集合，这些映射在数据交互期间协同工作，如下表所示。

| Finance and Operations 应用 | Dynamics 365 中的模型驱动应用 | 说明 |
-------------------------|---------------------------------
税码                   | msdyn\_taxcodes.md | 
税务组                 | msdyn\_taxgroups.md | 
税务(物料)组             | msdyn\_taxitemgroups.md | 
免税             | msdyn\_taxexemptcodes.md | 
税务主管机构             | msdyn\_taxauthorities.md | 
预缴税金代码       | msdyn\_withholdingtaxcodes.md | 
预缴税金组     | msdyn\_withholdingtaxgroups.md | 
税会计科目组 | msdyn\_taxpostinggroups     | 

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

