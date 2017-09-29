---
title: "配置中国的税务集成"
description: "本主题描述配置中国的税务集成的流程。"
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 265264
ms.assetid: e5dbbbe1-935f-4fb4-a014-447916051628
ms.search.region: China (PRC)
ms.author: leguo
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: cb5ab0e64b2a663af627d4d46e3a74aa526058b8
ms.openlocfilehash: 69ab2dde3051ac95b3025a3f78c85db296203d7f
ms.contentlocale: zh-cn
ms.lasthandoff: 07/28/2017

---

# <a name="configure-tax-integration-for-china"></a><span data-ttu-id="db071-103">配置中国的税务集成</span><span class="sxs-lookup"><span data-stu-id="db071-103">Configure tax integration for China</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="db071-104">本主题描述配置中国的税务集成的流程。</span><span class="sxs-lookup"><span data-stu-id="db071-104">This topic describes the process for configuring tax integration for China.</span></span>

<span data-ttu-id="db071-105">若要配置中国的税务集成，请完成以下任务。</span><span class="sxs-lookup"><span data-stu-id="db071-105">To configure tax integration for China, complete the following tasks.</span></span>

1.  <span data-ttu-id="db071-106">在**增值税发票描述**页中新建一个增值税发票描述。</span><span class="sxs-lookup"><span data-stu-id="db071-106">Create a new VAT invoice description on the **VAT invoice description** page.</span></span> <span data-ttu-id="db071-107">例如，可能需要设置以下参数：</span><span class="sxs-lookup"><span data-stu-id="db071-107">For example, you may need to set  the following parameters:</span></span>
    -   <span data-ttu-id="db071-108">将**增值税发票描述 ID** 设置为 InvoiceDescID01</span><span class="sxs-lookup"><span data-stu-id="db071-108">**VAT invoice description ID** to InvoiceDescID01</span></span>
    -   <span data-ttu-id="db071-109">将**描述**设置为“详见销售清单”</span><span class="sxs-lookup"><span data-stu-id="db071-109">**Description** to 详见销售清单</span></span>
    -   <span data-ttu-id="db071-110">将**单位**设置为“箱子”</span><span class="sxs-lookup"><span data-stu-id="db071-110">**Unit** to Box</span></span>

2.  <span data-ttu-id="db071-111">在**税务集成模板**页中创建一个新税务集成模板。</span><span class="sxs-lookup"><span data-stu-id="db071-111">Create a new tax integration profile on the **Tax integration profiles** page.</span></span> <span data-ttu-id="db071-112">可以设置导入或导出发票时使用的税务集成模板。</span><span class="sxs-lookup"><span data-stu-id="db071-112">You can set up tax integration profiles to use when invoices are imported or exported.</span></span> <span data-ttu-id="db071-113">在税务集成模板中，可以指定以下信息：</span><span class="sxs-lookup"><span data-stu-id="db071-113">In the tax integration profile, you can specify the following:</span></span>
    -   <span data-ttu-id="db071-114">增值税代码</span><span class="sxs-lookup"><span data-stu-id="db071-114">Sales tax code</span></span>
    -   <span data-ttu-id="db071-115">最大发票金额</span><span class="sxs-lookup"><span data-stu-id="db071-115">Maximum invoice amount</span></span>
    -   <span data-ttu-id="db071-116">金税发票的默认描述和单位</span><span class="sxs-lookup"><span data-stu-id="db071-116">Default description and unit for the golden tax invoice</span></span>
    -   <span data-ttu-id="db071-117">是否包含普通增值税发票</span><span class="sxs-lookup"><span data-stu-id="db071-117">Whether to include non-deductible VAT invoices</span></span>

<span data-ttu-id="db071-118">下图是税务集成流程的示例。</span><span class="sxs-lookup"><span data-stu-id="db071-118">The tax integration process is illustrated in the following diagram.</span></span>
<span data-ttu-id="db071-119">[![IC666469](./media/ic666469.gif)](./media/ic666469.gif)</span><span class="sxs-lookup"><span data-stu-id="db071-119">[![IC666469](./media/ic666469.gif)](./media/ic666469.gif)</span></span>

## <a name="see-also"></a><span data-ttu-id="db071-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="db071-120">See also</span></span>

- [<span data-ttu-id="db071-121">导入中国金税数据实体</span><span class="sxs-lookup"><span data-stu-id="db071-121">Import the Chinese Golden Tax data entity</span></span>](apac-chn-import-golden-tax-data-entity.md)

- [<span data-ttu-id="db071-122">增值税客户发票的中国税务集成修改常见问题</span><span class="sxs-lookup"><span data-stu-id="db071-122">Chinese tax integration modification for VAT customer invoices FAQ</span></span>](apac-chn-tax-integration-vat-customer-invoices.md)

- [<span data-ttu-id="db071-123">设置中国的基本税务集成</span><span class="sxs-lookup"><span data-stu-id="db071-123">Set up basic tax integration for China</span></span>](./tasks/set-up-basic-tax-integration-profile-china.md)



