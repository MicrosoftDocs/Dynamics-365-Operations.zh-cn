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
ms.openlocfilehash: b6be53e9a2065373ca37c2791568a8161823803f
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772402"
---
## <a name="integrated-tax"></a><span data-ttu-id="65f0e-103">集成税务</span><span class="sxs-lookup"><span data-stu-id="65f0e-103">Integrated tax</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="65f0e-104">税务设置数据定义间接税（增值税、GST、销售税）和预缴税金的设置。</span><span class="sxs-lookup"><span data-stu-id="65f0e-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="65f0e-105">它描述了税金计算规则、税率、税务核算、结算和其他概念。</span><span class="sxs-lookup"><span data-stu-id="65f0e-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="65f0e-106">模板</span><span class="sxs-lookup"><span data-stu-id="65f0e-106">Templates</span></span>

<span data-ttu-id="65f0e-107">税务数据包括实体映射的集合，这些映射在数据交互期间协同工作，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="65f0e-107">Tax data includes a collection of entity maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="65f0e-108">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="65f0e-108">Finance and Operations</span></span>   | <span data-ttu-id="65f0e-109">Customer Engagement 应用程序</span><span class="sxs-lookup"><span data-stu-id="65f0e-109">Customer Engagement application</span></span>
-------------------------|---------------------------------
<span data-ttu-id="65f0e-110">税码</span><span class="sxs-lookup"><span data-stu-id="65f0e-110">Tax codes</span></span>                  | <span data-ttu-id="65f0e-111">msdyn\_taxcodes.md</span><span class="sxs-lookup"><span data-stu-id="65f0e-111">msdyn\_taxcodes.md</span></span>
<span data-ttu-id="65f0e-112">税务组</span><span class="sxs-lookup"><span data-stu-id="65f0e-112">Tax groups</span></span>               | <span data-ttu-id="65f0e-113">msdyn\_taxgroups.md</span><span class="sxs-lookup"><span data-stu-id="65f0e-113">msdyn\_taxgroups.md</span></span>
<span data-ttu-id="65f0e-114">税务(物料)组</span><span class="sxs-lookup"><span data-stu-id="65f0e-114">Tax item groups</span></span>          | <span data-ttu-id="65f0e-115">msdyn\_taxitemgroups.md</span><span class="sxs-lookup"><span data-stu-id="65f0e-115">msdyn\_taxitemgroups.md</span></span>
<span data-ttu-id="65f0e-116">免税</span><span class="sxs-lookup"><span data-stu-id="65f0e-116">Tax Exemptions</span></span>           | <span data-ttu-id="65f0e-117">msdyn\_taxexemptcodes.md</span><span class="sxs-lookup"><span data-stu-id="65f0e-117">msdyn\_taxexemptcodes.md</span></span>
<span data-ttu-id="65f0e-118">税务主管机构</span><span class="sxs-lookup"><span data-stu-id="65f0e-118">Tax Authorities</span></span>          | <span data-ttu-id="65f0e-119">msdyn\_taxauthorities.md</span><span class="sxs-lookup"><span data-stu-id="65f0e-119">msdyn\_taxauthorities.md</span></span>
<span data-ttu-id="65f0e-120">预缴税金代码</span><span class="sxs-lookup"><span data-stu-id="65f0e-120">Withholding tax codes</span></span>      | <span data-ttu-id="65f0e-121">msdyn\_withholdingtaxcodes.md</span><span class="sxs-lookup"><span data-stu-id="65f0e-121">msdyn\_withholdingtaxcodes.md</span></span>
<span data-ttu-id="65f0e-122">预缴税金组</span><span class="sxs-lookup"><span data-stu-id="65f0e-122">Withholding tax groups</span></span>   | <span data-ttu-id="65f0e-123">msdyn\_withholdingtaxgroups.md</span><span class="sxs-lookup"><span data-stu-id="65f0e-123">msdyn\_withholdingtaxgroups.md</span></span>
<span data-ttu-id="65f0e-124">税会计科目组</span><span class="sxs-lookup"><span data-stu-id="65f0e-124">Tax Ledger Account Group</span></span> | <span data-ttu-id="65f0e-125">msdyn\_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="65f0e-125">msdyn\_taxpostinggroups</span></span>  

[!include [banner](../includes/dual-write-symbols.md)]

[!include [Tax groups](dual-write/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax item groups](dual-write/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Exemptions](dual-write/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax Authorities](dual-write/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Withholding tax codes](dual-write/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](dual-write/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

[!include [Tax Ledger Account Group](dual-write/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

