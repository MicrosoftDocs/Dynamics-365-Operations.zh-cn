---
title: 集成税务
description: 本主题介绍 Finance and Operations 与 Dataverse 之间的税务数据集成。
author: robinarh
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: rhaertle
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: a7992520b57b4c19b6dc8e13bd8e9ffc87b40f5a
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750634"
---
# <a name="integrated-tax"></a><span data-ttu-id="038d9-103">集成税务</span><span class="sxs-lookup"><span data-stu-id="038d9-103">Integrated tax</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="038d9-104">税务设置数据定义间接税（增值税、GST、销售税）和预缴税金的设置。</span><span class="sxs-lookup"><span data-stu-id="038d9-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="038d9-105">它描述了税金计算规则、税率、税务核算、结算和其他概念。</span><span class="sxs-lookup"><span data-stu-id="038d9-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="038d9-106">模板</span><span class="sxs-lookup"><span data-stu-id="038d9-106">Templates</span></span>

<span data-ttu-id="038d9-107">税务数据包括表映射的集合，这些映射在数据交互期间协同工作，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="038d9-107">Tax data includes a collection of table maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="038d9-108">Finance and Operations 应用</span><span class="sxs-lookup"><span data-stu-id="038d9-108">Finance and Operations apps</span></span> | <span data-ttu-id="038d9-109">Dynamics 365 中的模型驱动应用</span><span class="sxs-lookup"><span data-stu-id="038d9-109">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="038d9-110">说明</span><span class="sxs-lookup"><span data-stu-id="038d9-110">Description</span></span> |
-------------------------|---------------------------------|----|
<span data-ttu-id="038d9-111">销售税(物料)组</span><span class="sxs-lookup"><span data-stu-id="038d9-111">Item sales tax group</span></span> | <span data-ttu-id="038d9-112">msdyn_taxitemgroups</span><span class="sxs-lookup"><span data-stu-id="038d9-112">msdyn_taxitemgroups</span></span> |
<span data-ttu-id="038d9-113">销售税主管机构</span><span class="sxs-lookup"><span data-stu-id="038d9-113">Sales tax authorities</span></span> | <span data-ttu-id="038d9-114">msdyn_taxauthorities</span><span class="sxs-lookup"><span data-stu-id="038d9-114">msdyn_taxauthorities</span></span> |
<span data-ttu-id="038d9-115">免税(销售税)代码实体 CDS</span><span class="sxs-lookup"><span data-stu-id="038d9-115">Sales tax exempt code entity CDS</span></span> | <span data-ttu-id="038d9-116">msdyn_taxexemptcodes</span><span class="sxs-lookup"><span data-stu-id="038d9-116">msdyn_taxexemptcodes</span></span> |
<span data-ttu-id="038d9-117">销售税组</span><span class="sxs-lookup"><span data-stu-id="038d9-117">Sales tax groups</span></span> | <span data-ttu-id="038d9-118">msdyn_taxgroups</span><span class="sxs-lookup"><span data-stu-id="038d9-118">msdyn_taxgroups</span></span> |
<span data-ttu-id="038d9-119">销售税分类帐过帐组 V2</span><span class="sxs-lookup"><span data-stu-id="038d9-119">Sales tax ledger posting groups V2</span></span> | <span data-ttu-id="038d9-120">msdyn_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="038d9-120">msdyn_taxpostinggroups</span></span> |
<span data-ttu-id="038d9-121">预缴税金代码</span><span class="sxs-lookup"><span data-stu-id="038d9-121">Withholding tax codes</span></span> | <span data-ttu-id="038d9-122">msdyn_withholdingtaxcodes</span><span class="sxs-lookup"><span data-stu-id="038d9-122">msdyn_withholdingtaxcodes</span></span> |
<span data-ttu-id="038d9-123">预缴税金组</span><span class="sxs-lookup"><span data-stu-id="038d9-123">Withholding tax groups</span></span> | <span data-ttu-id="038d9-124">msdyn_withholdingtaxgroups</span><span class="sxs-lookup"><span data-stu-id="038d9-124">msdyn_withholdingtaxgroups</span></span> | 


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]