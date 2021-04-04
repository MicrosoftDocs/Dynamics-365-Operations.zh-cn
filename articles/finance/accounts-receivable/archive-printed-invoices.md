---
title: 使用哈希编号存档打印的客户账单
description: 本主题说明如何启用存档以存储带有哈希编号的打印客户发票。
author: ilyako
manager: AnnBe
ms.date: 03/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: d502ec5d286573c72e207419b66f283183009c09
ms.sourcegitcommit: 08ac570bece3e4ee4a0f632f51623e328536dfcf
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/08/2021
ms.locfileid: "5557472"
---
# <a name="archive-printed-customer-invoices-with-hash-numbers"></a><span data-ttu-id="66758-103">使用哈希编号存档打印的客户账单</span><span class="sxs-lookup"><span data-stu-id="66758-103">Archive printed customer invoices with hash numbers</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="66758-104">在某些国家/地区，法律要求将计算出的哈希编号与某些文档的打印输出一起存储在系统中。</span><span class="sxs-lookup"><span data-stu-id="66758-104">In some countries, there is a legal requirement to store calculated hash numbers in the system together with printouts of some documents.</span></span> <span data-ttu-id="66758-105">哈希编号可用于向权威机构报告以及在审核期间报告。</span><span class="sxs-lookup"><span data-stu-id="66758-105">Hash numbers can be used for reporting to authorities and during audits.</span></span>

<span data-ttu-id="66758-106">本主题说明如何配置存档以存储带有哈希编号的打印客户发票。</span><span class="sxs-lookup"><span data-stu-id="66758-106">This topic explains how to configure archiving in order to store printed customer invoices with hash numbers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="66758-107">先决条件</span><span class="sxs-lookup"><span data-stu-id="66758-107">Prerequisites</span></span>

- <span data-ttu-id="66758-108">在 **功能管理** 工作区，打开 **存档带有哈希编号的打印客户发票** 功能。</span><span class="sxs-lookup"><span data-stu-id="66758-108">In the **Feature management** workspace, turn on the feature, **Archive printed customer invoices with hash numbers**.</span></span> <span data-ttu-id="66758-109">有关更多信息，请参见[功能管理概述](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="66758-109">For more information, see [Feature management overview](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>
- <span data-ttu-id="66758-110">在 **打印管理** 中配置所需文档的可打印格式。</span><span class="sxs-lookup"><span data-stu-id="66758-110">Configure the printable formats of required documents in **Print management**.</span></span>

<span data-ttu-id="66758-111">此功能适用于以下文档。</span><span class="sxs-lookup"><span data-stu-id="66758-111">This functionality is applicable to the following documents.</span></span>

<span data-ttu-id="66758-112">**应收账款**</span><span class="sxs-lookup"><span data-stu-id="66758-112">**Accounts receivable**</span></span>
- <span data-ttu-id="66758-113">客户账单</span><span class="sxs-lookup"><span data-stu-id="66758-113">Customer invoice</span></span>
- <span data-ttu-id="66758-114">客户贷方通知单</span><span class="sxs-lookup"><span data-stu-id="66758-114">Customer credit note</span></span>
- <span data-ttu-id="66758-115">普通账单</span><span class="sxs-lookup"><span data-stu-id="66758-115">Free text invoice</span></span>
- <span data-ttu-id="66758-116">普通贷方通知单</span><span class="sxs-lookup"><span data-stu-id="66758-116">Free text credit note</span></span>

<span data-ttu-id="66758-117">**项目管理与核算**</span><span class="sxs-lookup"><span data-stu-id="66758-117">**Project management and accounting**</span></span>
- <span data-ttu-id="66758-118">项目账单</span><span class="sxs-lookup"><span data-stu-id="66758-118">Project invoice</span></span>
- <span data-ttu-id="66758-119">项目贷方通知单</span><span class="sxs-lookup"><span data-stu-id="66758-119">Project credit note</span></span>

## <a name="configure-customer-master-data"></a><span data-ttu-id="66758-120">配置客户主数据</span><span class="sxs-lookup"><span data-stu-id="66758-120">Configure customer master data</span></span>
<span data-ttu-id="66758-121">完成以下步骤以配置客户数据，并启用自动将打印发票另存为附件的功能。</span><span class="sxs-lookup"><span data-stu-id="66758-121">Complete the following steps to configure customer data and turn on the ability to automatically save printed invoices as attachments.</span></span>

1. <span data-ttu-id="66758-122">转到 **应付帐款** > **所有客户**。</span><span class="sxs-lookup"><span data-stu-id="66758-122">Go to **Accounts receivable** > **All customers**.</span></span> 
2. <span data-ttu-id="66758-123">选择客户，然后在 **发票和交货** 快速选项卡上的 **电子发票** 部分，在 **电子发票附件** 字段中，选择 **是**。</span><span class="sxs-lookup"><span data-stu-id="66758-123">Select a customer, and on the **Invoice and delivery** FastTab, in the **E-INVOCE** section, in the **eInvoice attachment** field, select **Yes**.</span></span>

## <a name="print-invoices"></a><span data-ttu-id="66758-124">打印发票</span><span class="sxs-lookup"><span data-stu-id="66758-124">Print invoices</span></span>
<span data-ttu-id="66758-125">您可以为上一过程中配置的客户过帐和打印任何自由文本形式的客户和项目发票或贷方通知单。</span><span class="sxs-lookup"><span data-stu-id="66758-125">You can post and print any free text, customer, and project invoice or credit note for the customer configured in the previous procedure.</span></span>

<span data-ttu-id="66758-126">针对打印的发票打开 **附件** 页面。</span><span class="sxs-lookup"><span data-stu-id="66758-126">Open the **Attachments** page for the printed invoice.</span></span> <span data-ttu-id="66758-127">在 **附件** 快速选项卡上 **其他详细信息** 字段组内的 **文件哈希编号** 字段中，查找为打印发票计算的已存储哈希编号。</span><span class="sxs-lookup"><span data-stu-id="66758-127">On the **Attachment** FastTab, in the **Additional details** field group, in **Document hash number** field, find the stored hash number calculated for the printed invoice.</span></span>

![附件哈希编号](media/attach-hash-num.jpg)

