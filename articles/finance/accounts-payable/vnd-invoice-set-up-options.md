---
title: 供应商发票自动化的设置选项（预览）
description: 本主题介绍了可用于设置和配置供应商发票自动化的选项。
author: abruer
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-30
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 32da8dc569f4eabfe3d7ddbfac55e827f469d871
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837193"
---
# <a name="setup-options-for-vendor-invoice-automation"></a><span data-ttu-id="3ad7c-103">供应商发票自动化的设置选项</span><span class="sxs-lookup"><span data-stu-id="3ad7c-103">Setup options for vendor invoice automation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3ad7c-104">本主题介绍了可用于设置和配置供应商发票自动化的选项。</span><span class="sxs-lookup"><span data-stu-id="3ad7c-104">This topic describes the options that are available for setting up and configuring vendor invoice automation.</span></span> <span data-ttu-id="3ad7c-105">发票自动化功能使用以下类型的设置参数：</span><span class="sxs-lookup"><span data-stu-id="3ad7c-105">Invoice automation features use the following types of setup parameters:</span></span>

- <span data-ttu-id="3ad7c-106">将导入的供应商发票提交到工作流系统并将过帐的物料收货行与待处理的供应商发票行进行匹配的参数。</span><span class="sxs-lookup"><span data-stu-id="3ad7c-106">Parameters for submitting imported vendor invoices to the workflow system and matching posted product receipt lines to pending vendor invoice lines.</span></span>
- <span data-ttu-id="3ad7c-107">用于处理自动化后台任务的参数。</span><span class="sxs-lookup"><span data-stu-id="3ad7c-107">Parameters for processing automation background tasks.</span></span> <span data-ttu-id="3ad7c-108">流程自动化框架用于将导入的供应商发票提交到工作流系统。</span><span class="sxs-lookup"><span data-stu-id="3ad7c-108">The process automation framework is used to submit imported vendor invoices to the workflow system.</span></span> <span data-ttu-id="3ad7c-109">它还用于自动将过帐的产品收货行与待定的供应商发票行进行匹配，并对自动匹配到产品收货行的手动发票执行发票匹配验证。</span><span class="sxs-lookup"><span data-stu-id="3ad7c-109">It's also used to automatically match posted product receipt lines to pending vendor invoice lines and to perform invoice matching validation for manual invoices that were automatically matched to product receipt lines.</span></span> <span data-ttu-id="3ad7c-110">不同的业务流程使用此框架来定义所选流程的运行频率。</span><span class="sxs-lookup"><span data-stu-id="3ad7c-110">Different business processes use this framework to define how often the selected process is run.</span></span> <span data-ttu-id="3ad7c-111">**将物料收货与发票行进行匹配** 和 **将供应商发票提交到工作流** 后台流程的可用频率包括 **小时** 和 **每日**。</span><span class="sxs-lookup"><span data-stu-id="3ad7c-111">The available frequencies for the **Match product receipt to invoice lines** and **Submit vendor invoices to workflow** background processes include **Hour** and **Daily**.</span></span>

<span data-ttu-id="3ad7c-112">若要设置或查看有关后台任务的信息，请转到 **系统管理 \> 设置 \> 流程自动化**，然后选择 **后台任务** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="3ad7c-112">To set up or view information about a background task, go to **System administration \> Setup \> Process automations**, and select the **Background task** tab.</span></span>

<span data-ttu-id="3ad7c-113">若要通过供应商发票过帐从导入流程中实现非接触式自动化，您必须设置供应商发票工作流。</span><span class="sxs-lookup"><span data-stu-id="3ad7c-113">To achieve touchless automation from the import process through vendor invoice posting, you must set up a Vendor invoice workflow.</span></span> <span data-ttu-id="3ad7c-114">若要设置工作流，请转到 **应付帐款 > 设置 > 应付帐款工作流**。</span><span class="sxs-lookup"><span data-stu-id="3ad7c-114">To set up a workflow, go to **Accounts payable > Setup > Accounts payable workflows**.</span></span> <span data-ttu-id="3ad7c-115">为了确保整个发票处理流程都没有人工干预，您必须在您的工作流配置中包括自动化过帐任务。</span><span class="sxs-lookup"><span data-stu-id="3ad7c-115">To ensure that the invoice can be processed from start to finish without manual intervention, you must include an automated posting task in your workflow configuration.</span></span>

## <a name="parameters-for-submitting-imported-vendor-invoices-to-the-workflow-system"></a><span data-ttu-id="3ad7c-116">用于将导入的供应商发票提交到工作流系统的参数</span><span class="sxs-lookup"><span data-stu-id="3ad7c-116">Parameters for submitting imported vendor invoices to the workflow system</span></span>

<span data-ttu-id="3ad7c-117">用于将导入的供应商发票提交到工作流系统的特定参数。</span><span class="sxs-lookup"><span data-stu-id="3ad7c-117">Specific parameters are used to submit imported vendor invoices to the workflow system.</span></span> <span data-ttu-id="3ad7c-118">此外，某些参数还用于将过帐的物料收货行与待处理的供应商发票行进行匹配。</span><span class="sxs-lookup"><span data-stu-id="3ad7c-118">Additionally, some parameters are used to match posted product receipt lines to pending vendor invoice lines.</span></span> <span data-ttu-id="3ad7c-119">在 **应付帐款参数** 页面的 **供应商发票自动化** 选项卡上，必须设置的参数分为以下几个部分：</span><span class="sxs-lookup"><span data-stu-id="3ad7c-119">On the **Vendor invoice automation** tab of the **Accounts payable parameters** page, the parameters that you must set are divided between the following sections:</span></span>

- <span data-ttu-id="3ad7c-120">供应商发票工作流</span><span class="sxs-lookup"><span data-stu-id="3ad7c-120">Vendor invoices workflow</span></span>
- <span data-ttu-id="3ad7c-121">自动匹配物料收货</span><span class="sxs-lookup"><span data-stu-id="3ad7c-121">Match product receipts automatically</span></span>

<span data-ttu-id="3ad7c-122">提供了以下参数：</span><span class="sxs-lookup"><span data-stu-id="3ad7c-122">The following parameters are available:</span></span>

- <span data-ttu-id="3ad7c-123">**自动将导入的发票提交到工作流** – 如果将此选项设置为 **是**，导入的发票将自动提交到工作流系统。</span><span class="sxs-lookup"><span data-stu-id="3ad7c-123">**Automatically submit imported invoices to workflow** – If you set this option to **Yes**, imported invoices are automatically submitted to the workflow system.</span></span> <span data-ttu-id="3ad7c-124">如果将此选项设置为 **否**，必须手动提交发票。</span><span class="sxs-lookup"><span data-stu-id="3ad7c-124">If this option is set to **No**, invoices must be manually submitted.</span></span> <span data-ttu-id="3ad7c-125">通过将此选项设置为 **是**，您可以通过过帐从导入结果中启用非接触式流程。</span><span class="sxs-lookup"><span data-stu-id="3ad7c-125">By setting this option to **Yes**, you enable a touchless process from the import results through posting.</span></span>

    <span data-ttu-id="3ad7c-126">仅在为您的法人设置了有效的供应商发票工作流时，才可以将此选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="3ad7c-126">You can set this option to **Yes** only if an active vendor invoice workflow is set up for your legal entity.</span></span> <span data-ttu-id="3ad7c-127">若要设置工作流，请转到 **应付帐款 \> 设置 \> 应付帐款工作流**。</span><span class="sxs-lookup"><span data-stu-id="3ad7c-127">To set up a workflow, go to **Accounts payable \> Setup \> Accounts payable workflow**.</span></span>

- <span data-ttu-id="3ad7c-128">**在自动提交之前将物料收货与发票行进行匹配** – 如果将此选项设置为 **是**，直到匹配的物料收货数量等于发票数量，导入的发票才能自动提交到工作流系统。</span><span class="sxs-lookup"><span data-stu-id="3ad7c-128">**Match product receipts to invoice lines prior to automatically submitting** – If you set this option to **Yes**, the imported invoice can't automatically be submitted to the workflow system until the matched product receipt quantity equals the invoice quantity.</span></span> <span data-ttu-id="3ad7c-129">通过将此选项设置为 **是**，您可以自动将已过帐的物料收货与为其定义了三向匹配政策的发票行进行匹配。</span><span class="sxs-lookup"><span data-stu-id="3ad7c-129">By setting this option to **Yes**, you enable automatic matching of posted product receipts to invoice lines that a three-way matching policy is defined for.</span></span> <span data-ttu-id="3ad7c-130">该流程将一直运行，直到匹配的物料收货数量等于发票数量。</span><span class="sxs-lookup"><span data-stu-id="3ad7c-130">That process will run until the matched product receipt quantity equals the invoice quantity.</span></span> <span data-ttu-id="3ad7c-131">此时，发票将自动提交到工作流系统。</span><span class="sxs-lookup"><span data-stu-id="3ad7c-131">At that point, the invoice is automatically submitted to the workflow system.</span></span>

    <span data-ttu-id="3ad7c-132">只有在选择 **启用发票匹配验证** 选项时，“在自动提交之前将物料收货与发票行进行匹配”选项才可用。</span><span class="sxs-lookup"><span data-stu-id="3ad7c-132">The 'Match product receipts to invoice lines prior to automatically submitting option is available only if the **Enable invoice matching validation** option is selected.</span></span> <span data-ttu-id="3ad7c-133">选择此选项后，将自动选择 **自动将物料收货与发票行进行匹配** 选项。</span><span class="sxs-lookup"><span data-stu-id="3ad7c-133">When this option is selected, the **Automatically match product receipts to invoice lines** option is automatically selected.</span></span>

- <span data-ttu-id="3ad7c-134">**要求计算合计等于导入合计才能进行自动化工作流提交** – 如果将此选项设置为 **是**，直到发票的计算合计等于导入合计，才能将发票自动提交到工作流系统。</span><span class="sxs-lookup"><span data-stu-id="3ad7c-134">**Require the calculated totals to equal the imported totals for automatic workflow submission** – If you set this option to **Yes**, the invoice can't automatically be submitted to the workflow system until the totals that are calculated for the invoice equal the imported totals.</span></span> <span data-ttu-id="3ad7c-135">如果此选项设置为 **否**，发票可以自动提交到工作流系统，但是只有在对计算合计进行更正以使其与导入合计匹配之后才能将其过帐。</span><span class="sxs-lookup"><span data-stu-id="3ad7c-135">If this option is set to **No**, the invoice can automatically be submitted to the workflow system, but it can't be posted until the calculated totals are corrected so that they match the imported totals.</span></span> <span data-ttu-id="3ad7c-136">如果您不导入发票金额或销售税金额，则此选项应设置为 **否**。</span><span class="sxs-lookup"><span data-stu-id="3ad7c-136">If you don't import the invoice amount or the sales tax amount, this option should be set to **No**.</span></span>
- <span data-ttu-id="3ad7c-137">**自动将物料收货与发票行进行匹配** – 如果将此选项设置为 **是**，后台处理可用于自动将已过帐的物料收货与为其定义了三向匹配政策的发票行进行匹配。</span><span class="sxs-lookup"><span data-stu-id="3ad7c-137">**Automatically match product receipts to invoice lines** – If you set this option to **Yes**, background processing can be used to do automatic matching of posted product receipts to invoice lines that a three-way matching policy is defined for.</span></span> <span data-ttu-id="3ad7c-138">该流程将一直运行，直到匹配的物料收货数量等于发票数量，或者直到达到 **尝试自动匹配的次数** 字段的值。</span><span class="sxs-lookup"><span data-stu-id="3ad7c-138">That process will run until the matched product receipt quantity equals the invoice quantity, or until the value of the **Number of times to attempt automatic matching** field is reached.</span></span> <span data-ttu-id="3ad7c-139">可以运行该流程，直到发票已提交到工作流系统。</span><span class="sxs-lookup"><span data-stu-id="3ad7c-139">The process can be run until the invoice has been submitted to the workflow system.</span></span>

    <span data-ttu-id="3ad7c-140">只有在选择 **启用发票匹配验证** 选项后，此选项才可用。</span><span class="sxs-lookup"><span data-stu-id="3ad7c-140">This option is available only if the **Enable invoice matching validation** option is selected.</span></span>

    <span data-ttu-id="3ad7c-141">如果您将 **在自动匹配之前将物料收货与发票行进行匹配** 选项设置为 **是**，此选项不能设置为 **否**。</span><span class="sxs-lookup"><span data-stu-id="3ad7c-141">If you set the **Match product receipts to invoice lines prior to automatically matching** option to **Yes**, this option can't be set to **No**.</span></span> <span data-ttu-id="3ad7c-142">若要将此选项设置为 **否**，您必须首先将 **在自动匹配之前将物料收货与发票行进行匹配** 选项设置为 **否**。</span><span class="sxs-lookup"><span data-stu-id="3ad7c-142">To set this option to **No**, you must first set the **Match product receipts to invoice lines prior to automatically matching** option to **No**.</span></span>

- <span data-ttu-id="3ad7c-143">**尝试自动匹配的次数** – 选择系统在得出流程失败的结论之前应尝试将物料收货与发票行进行匹配的次数。</span><span class="sxs-lookup"><span data-stu-id="3ad7c-143">**Number of times to attempt automatic matching** – Select the number of times that the system should try to match product receipts to an invoice line before it concludes that the process failed.</span></span> <span data-ttu-id="3ad7c-144">达到指定的尝试次数后，发票将从自动化处理中删除。</span><span class="sxs-lookup"><span data-stu-id="3ad7c-144">When the specified number of attempts is reached, the invoice is removed from automation processing.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]