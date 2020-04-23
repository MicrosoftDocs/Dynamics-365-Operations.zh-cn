---
title: 费用收据处理
description: 本主题提供有关收据的光学字符识别 (OCR) 处理的信息。 此功能适合在 Microsoft Dynamics 365 Finance 中创建费用报表时改善用户体验。
author: stsporen
manager: AnnBe
ms.date: 11/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: efba2faf9428d9b556d74273bc7daadba7211c48
ms.sourcegitcommit: ff6dde637d2f5d2bd18a582eb41573d4c69acdd6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/08/2020
ms.locfileid: "3248955"
---
# <a name="expense-receipt-processing"></a><span data-ttu-id="39355-104">支出收据处理</span><span class="sxs-lookup"><span data-stu-id="39355-104">Expense receipt processing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="39355-105">通过为收据引入光学字符识别 (OCR) 处理，费用录入得到了增强。</span><span class="sxs-lookup"><span data-stu-id="39355-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="39355-106">此功能适合在创建费用报表时改善用户体验。</span><span class="sxs-lookup"><span data-stu-id="39355-106">This feature is designed to improve the user experience when expense reports are created.</span></span>

## <a name="key-features"></a><span data-ttu-id="39355-107">主要功能</span><span class="sxs-lookup"><span data-stu-id="39355-107">Key features</span></span>

- <span data-ttu-id="39355-108">从收据中提取商户名称、日期和总金额。</span><span class="sxs-lookup"><span data-stu-id="39355-108">The merchant name, date, and total amount are extracted from receipts.</span></span>
- <span data-ttu-id="39355-109">该功能尝试将未附加的收据与未附加的费用交易记录匹配。</span><span class="sxs-lookup"><span data-stu-id="39355-109">The feature tries to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="39355-110">用户可以根据收据创建手动输入的费用交易记录。</span><span class="sxs-lookup"><span data-stu-id="39355-110">Users can create manually entered expense transactions from receipts.</span></span>

## <a name="usage-examples"></a><span data-ttu-id="39355-111">用法示例</span><span class="sxs-lookup"><span data-stu-id="39355-111">Usage examples</span></span>

- <span data-ttu-id="39355-112">**自动附加创建费用报表时包括信用卡交易记录的收据。**</span><span class="sxs-lookup"><span data-stu-id="39355-112">**Automatically attach receipts that include credit card transactions when an expense report is created.**</span></span>

    1. <span data-ttu-id="39355-113">打开**费用管理**工作区。</span><span class="sxs-lookup"><span data-stu-id="39355-113">Open the **Expense management** workspace.</span></span>
    2. <span data-ttu-id="39355-114">在**收据**选项卡上，验证是否存在未附加的收据。</span><span class="sxs-lookup"><span data-stu-id="39355-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="39355-115">您也可以在**收据**选项卡上上传收据。</span><span class="sxs-lookup"><span data-stu-id="39355-115">You can also upload receipts on the **Receipts** tab.</span></span>
    3. <span data-ttu-id="39355-116">在**费用**选项卡上，验证是否存在未附加的费用。</span><span class="sxs-lookup"><span data-stu-id="39355-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="39355-117">通常，费用管理员会从信用卡提供商处导入这些费用。</span><span class="sxs-lookup"><span data-stu-id="39355-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
    4. <span data-ttu-id="39355-118">选择**新建费用报表**。</span><span class="sxs-lookup"><span data-stu-id="39355-118">Select **New expense report**.</span></span> <span data-ttu-id="39355-119">请注意，当您创建费用报表时，现在还可以包括费用和收据。</span><span class="sxs-lookup"><span data-stu-id="39355-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="39355-120">如果同时添加费用和收据，则会触发按费用自动匹配收据。</span><span class="sxs-lookup"><span data-stu-id="39355-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

- <span data-ttu-id="39355-121">**创建费用，或匹配收据中的费用。**</span><span class="sxs-lookup"><span data-stu-id="39355-121">**Create an expense, or match an expense from a receipt.**</span></span>

    1. <span data-ttu-id="39355-122">在费用报表中的**收据**选项卡上，选择**添加收据**来附加收据。</span><span class="sxs-lookup"><span data-stu-id="39355-122">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
    2. <span data-ttu-id="39355-123">在上传的收据图像下面，注意**创建**和**匹配**选项。</span><span class="sxs-lookup"><span data-stu-id="39355-123">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

        - <span data-ttu-id="39355-124">选择**创建**以创建手动输入的费用交易记录并填写从收据中提取的值。</span><span class="sxs-lookup"><span data-stu-id="39355-124">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
        - <span data-ttu-id="39355-125">如果选择**匹配**，系统会尝试将现有费用与收据进行匹配。</span><span class="sxs-lookup"><span data-stu-id="39355-125">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="39355-126">安装</span><span class="sxs-lookup"><span data-stu-id="39355-126">Installation</span></span>

<span data-ttu-id="39355-127">此功能与**已重构的费用报表**功能联合使用，有助于简化费用体验。</span><span class="sxs-lookup"><span data-stu-id="39355-127">This feature works in combination with the **Expense reports re-imagined** feature to help simplify the expense experience.</span></span>

<span data-ttu-id="39355-128">要使用这些高级费用功能，请安装 Microsoft Dynamics 365 Finance 费用管理服务加载项，然后在实例中打开这些功能。</span><span class="sxs-lookup"><span data-stu-id="39355-128">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="39355-129">您可以在 Microsoft Dynamics Lifecycle Services (LCS) 中从您的项目访问加载项。</span><span class="sxs-lookup"><span data-stu-id="39355-129">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="39355-130">登录到 LCS，然后打开所需的环境。</span><span class="sxs-lookup"><span data-stu-id="39355-130">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="39355-131">转到**完整详细信息**。</span><span class="sxs-lookup"><span data-stu-id="39355-131">Go to **Full details**.</span></span>
3. <span data-ttu-id="39355-132">选择**维护**，或向下滚动到**环境加载项**快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="39355-132">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="39355-133">选择**安装新加载项**。</span><span class="sxs-lookup"><span data-stu-id="39355-133">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="39355-134">选择**费用管理服务**。</span><span class="sxs-lookup"><span data-stu-id="39355-134">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="39355-135">按照安装指南操作，并同意条款和条件。</span><span class="sxs-lookup"><span data-stu-id="39355-135">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="39355-136">选择**安装**。</span><span class="sxs-lookup"><span data-stu-id="39355-136">Select **Install**.</span></span>

<span data-ttu-id="39355-137">在**功能管理**工作区中，开启以下功能：</span><span class="sxs-lookup"><span data-stu-id="39355-137">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="39355-138">已重构的费用报表</span><span class="sxs-lookup"><span data-stu-id="39355-138">Expense reports re-imagined</span></span>
- <span data-ttu-id="39355-139">自动匹配并从收据创建支出</span><span class="sxs-lookup"><span data-stu-id="39355-139">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="39355-140">开启这些功能时，将执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="39355-140">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="39355-141">现有**费用管理**工作区已替换为新工作区。</span><span class="sxs-lookup"><span data-stu-id="39355-141">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="39355-142">为费用字段可见性添加一个新菜单项。</span><span class="sxs-lookup"><span data-stu-id="39355-142">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="39355-143">您仍然可以打开以前的**费用报告**页面，方法是转到**费用管理 > 我的费用 > 费用报告**。</span><span class="sxs-lookup"><span data-stu-id="39355-143">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="39355-144">工作流和所有审核仍然会将您带到现有费用报表页。</span><span class="sxs-lookup"><span data-stu-id="39355-144">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="39355-145">收据将通过 Microsoft Azure Cognitive Services 务得到处理，并且将提取和添加元数据。</span><span class="sxs-lookup"><span data-stu-id="39355-145">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="39355-146">添加了一个选项，使您可以创建一个包含匹配的未附加收据的费用报表。</span><span class="sxs-lookup"><span data-stu-id="39355-146">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="39355-147">添加到费用报告中的选项使您可以从收据创建费用行，或尝试将现有收据与现有费用行进行匹配。</span><span class="sxs-lookup"><span data-stu-id="39355-147">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

<span data-ttu-id="39355-148">有关已重构的费用报表功能的更多信息，请参见[已重构的费用报表](ExpenseWorkspaceNew.md)。</span><span class="sxs-lookup"><span data-stu-id="39355-148">For more information about the Expense reports re-imagined feature, see [Expense reports reimagined](ExpenseWorkspaceNew.md).</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="39355-149">常见问题</span><span class="sxs-lookup"><span data-stu-id="39355-149">Frequently asked questions</span></span>

<span data-ttu-id="39355-150">**Microsoft 是否将我的数据用于其模型？**</span><span class="sxs-lookup"><span data-stu-id="39355-150">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="39355-151">否，Microsoft 已经为其收据处理服务建立了通用机器学习模型。</span><span class="sxs-lookup"><span data-stu-id="39355-151">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="39355-152">此模型并不基于您上传的收据。</span><span class="sxs-lookup"><span data-stu-id="39355-152">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="39355-153">**在哪里可以使用和处理此功能？**</span><span class="sxs-lookup"><span data-stu-id="39355-153">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="39355-154">目前，支持在美国使用。</span><span class="sxs-lookup"><span data-stu-id="39355-154">Currently, the United States is supported.</span></span>

<span data-ttu-id="39355-155">**我的收据去哪里了？**</span><span class="sxs-lookup"><span data-stu-id="39355-155">**Where do my receipts go?**</span></span>

<span data-ttu-id="39355-156">Finance 将与 Cognitive Services 联系以提取字段数据。</span><span class="sxs-lookup"><span data-stu-id="39355-156">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="39355-157">进行处理时，Cognitive Services 将您的收据副本最多保留 24 小时。</span><span class="sxs-lookup"><span data-stu-id="39355-157">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="39355-158">处理完成后，Cognitive Services 将删除收据。</span><span class="sxs-lookup"><span data-stu-id="39355-158">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="39355-159">收据仍存储在 Finance 中。</span><span class="sxs-lookup"><span data-stu-id="39355-159">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="39355-160">有关更多信息，请参见[使用 Form Recognizer 的新功能实现收据了解](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/)。</span><span class="sxs-lookup"><span data-stu-id="39355-160">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>
