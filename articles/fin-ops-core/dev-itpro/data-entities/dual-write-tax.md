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
ms.openlocfilehash: 86e74086a5a74c7af5f2572d1a653a1658d729c0
ms.sourcegitcommit: d0322d1ed6c798301058e44dae76227a0e1f49ac
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2019
ms.locfileid: "2853851"
---
# <a name="integrated-tax"></a><span data-ttu-id="80b7d-103">集成税务</span><span class="sxs-lookup"><span data-stu-id="80b7d-103">Integrated tax</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="80b7d-104">税务设置数据定义间接税（增值税、GST、销售税）和预缴税金的设置。</span><span class="sxs-lookup"><span data-stu-id="80b7d-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="80b7d-105">它描述了税金计算规则、税率、税务核算、结算和其他概念。</span><span class="sxs-lookup"><span data-stu-id="80b7d-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="80b7d-106">模板</span><span class="sxs-lookup"><span data-stu-id="80b7d-106">Templates</span></span>

<span data-ttu-id="80b7d-107">税务数据包括实体映射的集合，这些映射在数据交互期间协同工作，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="80b7d-107">Tax data includes a collection of entity maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="80b7d-108">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="80b7d-108">Finance and Operations</span></span>   | <span data-ttu-id="80b7d-109">其他 Dynamics 365 应用</span><span class="sxs-lookup"><span data-stu-id="80b7d-109">Other Dynamics 365 apps</span></span>
-------------------------|---------------------------------
<span data-ttu-id="80b7d-110">税码</span><span class="sxs-lookup"><span data-stu-id="80b7d-110">Tax codes</span></span>                  | <span data-ttu-id="80b7d-111">msdyn\_taxcodes.md</span><span class="sxs-lookup"><span data-stu-id="80b7d-111">msdyn\_taxcodes.md</span></span>
<span data-ttu-id="80b7d-112">税务组</span><span class="sxs-lookup"><span data-stu-id="80b7d-112">Tax groups</span></span>               | <span data-ttu-id="80b7d-113">msdyn\_taxgroups.md</span><span class="sxs-lookup"><span data-stu-id="80b7d-113">msdyn\_taxgroups.md</span></span>
<span data-ttu-id="80b7d-114">税务(物料)组</span><span class="sxs-lookup"><span data-stu-id="80b7d-114">Tax item groups</span></span>          | <span data-ttu-id="80b7d-115">msdyn\_taxitemgroups.md</span><span class="sxs-lookup"><span data-stu-id="80b7d-115">msdyn\_taxitemgroups.md</span></span>
<span data-ttu-id="80b7d-116">免税</span><span class="sxs-lookup"><span data-stu-id="80b7d-116">Tax Exemptions</span></span>           | <span data-ttu-id="80b7d-117">msdyn\_taxexemptcodes.md</span><span class="sxs-lookup"><span data-stu-id="80b7d-117">msdyn\_taxexemptcodes.md</span></span>
<span data-ttu-id="80b7d-118">税务主管机构</span><span class="sxs-lookup"><span data-stu-id="80b7d-118">Tax Authorities</span></span>          | <span data-ttu-id="80b7d-119">msdyn\_taxauthorities.md</span><span class="sxs-lookup"><span data-stu-id="80b7d-119">msdyn\_taxauthorities.md</span></span>
<span data-ttu-id="80b7d-120">预缴税金代码</span><span class="sxs-lookup"><span data-stu-id="80b7d-120">Withholding tax codes</span></span>      | <span data-ttu-id="80b7d-121">msdyn\_withholdingtaxcodes.md</span><span class="sxs-lookup"><span data-stu-id="80b7d-121">msdyn\_withholdingtaxcodes.md</span></span>
<span data-ttu-id="80b7d-122">预缴税金组</span><span class="sxs-lookup"><span data-stu-id="80b7d-122">Withholding tax groups</span></span>   | <span data-ttu-id="80b7d-123">msdyn\_withholdingtaxgroups.md</span><span class="sxs-lookup"><span data-stu-id="80b7d-123">msdyn\_withholdingtaxgroups.md</span></span>
<span data-ttu-id="80b7d-124">税会计科目组</span><span class="sxs-lookup"><span data-stu-id="80b7d-124">Tax Ledger Account Group</span></span> | <span data-ttu-id="80b7d-125">msdyn\_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="80b7d-125">msdyn\_taxpostinggroups</span></span>  

[!include [banner](../includes/dual-write-symbols.md)]

[!include [Tax groups](dual-write/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax item groups](dual-write/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Exemptions](dual-write/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax Authorities](dual-write/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Withholding tax codes](dual-write/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](dual-write/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

[!include [Tax Ledger Account Group](dual-write/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

