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
ms.openlocfilehash: 0d32a5f7859f0200da823a73d94b9a6b2a9c8e7d
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019656"
---
# <a name="integrated-tax"></a><span data-ttu-id="43d21-103">集成税务</span><span class="sxs-lookup"><span data-stu-id="43d21-103">Integrated tax</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="43d21-104">税务设置数据定义间接税（增值税、GST、销售税）和预缴税金的设置。</span><span class="sxs-lookup"><span data-stu-id="43d21-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="43d21-105">它描述了税金计算规则、税率、税务核算、结算和其他概念。</span><span class="sxs-lookup"><span data-stu-id="43d21-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="43d21-106">模板</span><span class="sxs-lookup"><span data-stu-id="43d21-106">Templates</span></span>

<span data-ttu-id="43d21-107">税务数据包括实体映射的集合，这些映射在数据交互期间协同工作，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="43d21-107">Tax data includes a collection of entity maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="43d21-108">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="43d21-108">Finance and Operations</span></span>   | <span data-ttu-id="43d21-109">其他 Dynamics 365 应用</span><span class="sxs-lookup"><span data-stu-id="43d21-109">Other Dynamics 365 apps</span></span>
-------------------------|---------------------------------
<span data-ttu-id="43d21-110">税码</span><span class="sxs-lookup"><span data-stu-id="43d21-110">Tax codes</span></span>                  | <span data-ttu-id="43d21-111">msdyn\_taxcodes.md</span><span class="sxs-lookup"><span data-stu-id="43d21-111">msdyn\_taxcodes.md</span></span>
<span data-ttu-id="43d21-112">税务组</span><span class="sxs-lookup"><span data-stu-id="43d21-112">Tax groups</span></span>               | <span data-ttu-id="43d21-113">msdyn\_taxgroups.md</span><span class="sxs-lookup"><span data-stu-id="43d21-113">msdyn\_taxgroups.md</span></span>
<span data-ttu-id="43d21-114">税务(物料)组</span><span class="sxs-lookup"><span data-stu-id="43d21-114">Tax item groups</span></span>          | <span data-ttu-id="43d21-115">msdyn\_taxitemgroups.md</span><span class="sxs-lookup"><span data-stu-id="43d21-115">msdyn\_taxitemgroups.md</span></span>
<span data-ttu-id="43d21-116">免税</span><span class="sxs-lookup"><span data-stu-id="43d21-116">Tax Exemptions</span></span>           | <span data-ttu-id="43d21-117">msdyn\_taxexemptcodes.md</span><span class="sxs-lookup"><span data-stu-id="43d21-117">msdyn\_taxexemptcodes.md</span></span>
<span data-ttu-id="43d21-118">税务主管机构</span><span class="sxs-lookup"><span data-stu-id="43d21-118">Tax Authorities</span></span>          | <span data-ttu-id="43d21-119">msdyn\_taxauthorities.md</span><span class="sxs-lookup"><span data-stu-id="43d21-119">msdyn\_taxauthorities.md</span></span>
<span data-ttu-id="43d21-120">预缴税金代码</span><span class="sxs-lookup"><span data-stu-id="43d21-120">Withholding tax codes</span></span>      | <span data-ttu-id="43d21-121">msdyn\_withholdingtaxcodes.md</span><span class="sxs-lookup"><span data-stu-id="43d21-121">msdyn\_withholdingtaxcodes.md</span></span>
<span data-ttu-id="43d21-122">预缴税金组</span><span class="sxs-lookup"><span data-stu-id="43d21-122">Withholding tax groups</span></span>   | <span data-ttu-id="43d21-123">msdyn\_withholdingtaxgroups.md</span><span class="sxs-lookup"><span data-stu-id="43d21-123">msdyn\_withholdingtaxgroups.md</span></span>
<span data-ttu-id="43d21-124">税会计科目组</span><span class="sxs-lookup"><span data-stu-id="43d21-124">Tax Ledger Account Group</span></span> | <span data-ttu-id="43d21-125">msdyn\_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="43d21-125">msdyn\_taxpostinggroups</span></span>  

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

