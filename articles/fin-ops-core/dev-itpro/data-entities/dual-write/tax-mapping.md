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
# <a name="integrated-tax"></a><span data-ttu-id="bb6aa-103">集成税务</span><span class="sxs-lookup"><span data-stu-id="bb6aa-103">Integrated tax</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="bb6aa-104">税务设置数据定义间接税（增值税、GST、销售税）和预缴税金的设置。</span><span class="sxs-lookup"><span data-stu-id="bb6aa-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="bb6aa-105">它描述了税金计算规则、税率、税务核算、结算和其他概念。</span><span class="sxs-lookup"><span data-stu-id="bb6aa-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="bb6aa-106">模板</span><span class="sxs-lookup"><span data-stu-id="bb6aa-106">Templates</span></span>

<span data-ttu-id="bb6aa-107">税务数据包括实体映射的集合，这些映射在数据交互期间协同工作，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="bb6aa-107">Tax data includes a collection of entity maps that work together during data interaction, as shown in the following table.</span></span>

| <span data-ttu-id="bb6aa-108">Finance and Operations 应用</span><span class="sxs-lookup"><span data-stu-id="bb6aa-108">Finance and Operations apps</span></span> | <span data-ttu-id="bb6aa-109">Dynamics 365 中的模型驱动应用</span><span class="sxs-lookup"><span data-stu-id="bb6aa-109">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="bb6aa-110">说明</span><span class="sxs-lookup"><span data-stu-id="bb6aa-110">Description</span></span> |
-------------------------|---------------------------------
<span data-ttu-id="bb6aa-111">税码</span><span class="sxs-lookup"><span data-stu-id="bb6aa-111">Tax codes</span></span>                   | <span data-ttu-id="bb6aa-112">msdyn\_taxcodes.md</span><span class="sxs-lookup"><span data-stu-id="bb6aa-112">msdyn\_taxcodes.md</span></span> | 
<span data-ttu-id="bb6aa-113">税务组</span><span class="sxs-lookup"><span data-stu-id="bb6aa-113">Tax groups</span></span>                 | <span data-ttu-id="bb6aa-114">msdyn\_taxgroups.md</span><span class="sxs-lookup"><span data-stu-id="bb6aa-114">msdyn\_taxgroups.md</span></span> | 
<span data-ttu-id="bb6aa-115">税务(物料)组</span><span class="sxs-lookup"><span data-stu-id="bb6aa-115">Tax item groups</span></span>             | <span data-ttu-id="bb6aa-116">msdyn\_taxitemgroups.md</span><span class="sxs-lookup"><span data-stu-id="bb6aa-116">msdyn\_taxitemgroups.md</span></span> | 
<span data-ttu-id="bb6aa-117">免税</span><span class="sxs-lookup"><span data-stu-id="bb6aa-117">Tax Exemptions</span></span>             | <span data-ttu-id="bb6aa-118">msdyn\_taxexemptcodes.md</span><span class="sxs-lookup"><span data-stu-id="bb6aa-118">msdyn\_taxexemptcodes.md</span></span> | 
<span data-ttu-id="bb6aa-119">税务主管机构</span><span class="sxs-lookup"><span data-stu-id="bb6aa-119">Tax Authorities</span></span>             | <span data-ttu-id="bb6aa-120">msdyn\_taxauthorities.md</span><span class="sxs-lookup"><span data-stu-id="bb6aa-120">msdyn\_taxauthorities.md</span></span> | 
<span data-ttu-id="bb6aa-121">预缴税金代码</span><span class="sxs-lookup"><span data-stu-id="bb6aa-121">Withholding tax codes</span></span>       | <span data-ttu-id="bb6aa-122">msdyn\_withholdingtaxcodes.md</span><span class="sxs-lookup"><span data-stu-id="bb6aa-122">msdyn\_withholdingtaxcodes.md</span></span> | 
<span data-ttu-id="bb6aa-123">预缴税金组</span><span class="sxs-lookup"><span data-stu-id="bb6aa-123">Withholding tax groups</span></span>     | <span data-ttu-id="bb6aa-124">msdyn\_withholdingtaxgroups.md</span><span class="sxs-lookup"><span data-stu-id="bb6aa-124">msdyn\_withholdingtaxgroups.md</span></span> | 
<span data-ttu-id="bb6aa-125">税会计科目组</span><span class="sxs-lookup"><span data-stu-id="bb6aa-125">Tax Ledger Account Group</span></span> | <span data-ttu-id="bb6aa-126">msdyn\_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="bb6aa-126">msdyn\_taxpostinggroups</span></span>     | 

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

