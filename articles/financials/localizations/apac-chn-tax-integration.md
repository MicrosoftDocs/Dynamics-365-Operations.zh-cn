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
ms.search.form: CustParameters, VATInvoiceDescTable_CN, TaxProfileTable_CN
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 265264
ms.assetid: e5dbbbe1-935f-4fb4-a014-447916051628
ms.search.region: China (PRC)
ms.author: leguo
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a523ff097eedf9a4a2cb0341b3be9d05abfa09fa
ms.openlocfilehash: 4e403f29c79286add175724b00803e54ceecdc3b
ms.contentlocale: zh-cn
ms.lasthandoff: 01/23/2018

---

# <a name="configure-tax-integration-for-china"></a><span data-ttu-id="b8b62-103">配置中国的税务集成</span><span class="sxs-lookup"><span data-stu-id="b8b62-103">Configure tax integration for China</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="b8b62-104">本主题描述配置中国的税务集成的流程。</span><span class="sxs-lookup"><span data-stu-id="b8b62-104">This topic describes the process for configuring tax integration for China.</span></span>

## <a name="prerequisite"></a><span data-ttu-id="b8b62-105">必备项</span><span class="sxs-lookup"><span data-stu-id="b8b62-105">Prerequisite</span></span>
<span data-ttu-id="b8b62-106">必须先通过为**应收科目参数**页面（**应收帐款** > **设置** > **应收帐款参数** > **分类帐和销售税** > **常规**选项卡）中的**与税务系统集成**选项选择**是**启用税务集成，才能配置税务集成。</span><span class="sxs-lookup"><span data-stu-id="b8b62-106">Before you can configure tax integration, you must enable tax integration by selecting **Yes** for the **Integration with tax system** option on the **Accounts receivable parameters** page (**Accounts receivable** > **Setup** > **Accounts receivable parameters** > **Ledger and sales tax** > **General** tab).</span></span>

<span data-ttu-id="b8b62-107">若要配置中国的税务集成，请完成以下任务。</span><span class="sxs-lookup"><span data-stu-id="b8b62-107">To configure tax integration for China, complete the following tasks.</span></span>

1.  <span data-ttu-id="b8b62-108">在**增值税发票描述**页中新建一个增值税发票描述。</span><span class="sxs-lookup"><span data-stu-id="b8b62-108">Create a new VAT invoice description on the **VAT invoice description** page.</span></span> <span data-ttu-id="b8b62-109">例如，可能需要设置以下参数：</span><span class="sxs-lookup"><span data-stu-id="b8b62-109">For example, you may need to set  the following parameters:</span></span>
    -   <span data-ttu-id="b8b62-110">将**增值税发票描述 ID** 设置为 InvoiceDescID01</span><span class="sxs-lookup"><span data-stu-id="b8b62-110">**VAT invoice description ID** to InvoiceDescID01</span></span>
    -   <span data-ttu-id="b8b62-111">将**描述**设置为“详见销售清单”</span><span class="sxs-lookup"><span data-stu-id="b8b62-111">**Description** to 详见销售清单</span></span>
    -   <span data-ttu-id="b8b62-112">将**单位**设置为“箱子”</span><span class="sxs-lookup"><span data-stu-id="b8b62-112">**Unit** to Box</span></span>

2.  <span data-ttu-id="b8b62-113">在**税务集成模板**页中创建一个新税务集成模板。</span><span class="sxs-lookup"><span data-stu-id="b8b62-113">Create a new tax integration profile on the **Tax integration profiles** page.</span></span> <span data-ttu-id="b8b62-114">可以设置导入或导出发票时使用的税务集成模板。</span><span class="sxs-lookup"><span data-stu-id="b8b62-114">You can set up tax integration profiles to use when invoices are imported or exported.</span></span> <span data-ttu-id="b8b62-115">在税务集成模板中，可以指定以下信息：</span><span class="sxs-lookup"><span data-stu-id="b8b62-115">In the tax integration profile, you can specify the following:</span></span>
    -   <span data-ttu-id="b8b62-116">增值税代码</span><span class="sxs-lookup"><span data-stu-id="b8b62-116">Sales tax code</span></span>
    -   <span data-ttu-id="b8b62-117">最大发票金额</span><span class="sxs-lookup"><span data-stu-id="b8b62-117">Maximum invoice amount</span></span>
    -   <span data-ttu-id="b8b62-118">金税发票的默认描述和单位</span><span class="sxs-lookup"><span data-stu-id="b8b62-118">Default description and unit for the golden tax invoice</span></span>
    -   <span data-ttu-id="b8b62-119">是否包含普通增值税发票</span><span class="sxs-lookup"><span data-stu-id="b8b62-119">Whether to include non-deductible VAT invoices</span></span>

<span data-ttu-id="b8b62-120">下图是税务集成流程的示例。</span><span class="sxs-lookup"><span data-stu-id="b8b62-120">The tax integration process is illustrated in the following diagram.</span></span>
<span data-ttu-id="b8b62-121">[![IC666469](./media/ic666469.gif)](./media/ic666469.gif)</span><span class="sxs-lookup"><span data-stu-id="b8b62-121">[![IC666469](./media/ic666469.gif)](./media/ic666469.gif)</span></span>

## <a name="see-also"></a><span data-ttu-id="b8b62-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="b8b62-122">See also</span></span>

- [<span data-ttu-id="b8b62-123">导入中国金税数据实体</span><span class="sxs-lookup"><span data-stu-id="b8b62-123">Import the Chinese Golden Tax data entity</span></span>](apac-chn-import-golden-tax-data-entity.md)

- [<span data-ttu-id="b8b62-124">增值税客户发票的中国税务集成修改常见问题</span><span class="sxs-lookup"><span data-stu-id="b8b62-124">Chinese tax integration modification for VAT customer invoices FAQ</span></span>](apac-chn-tax-integration-vat-customer-invoices.md)

- [<span data-ttu-id="b8b62-125">设置中国的基本税务集成</span><span class="sxs-lookup"><span data-stu-id="b8b62-125">Set up basic tax integration for China</span></span>](./tasks/set-up-basic-tax-integration-profile-china.md)



