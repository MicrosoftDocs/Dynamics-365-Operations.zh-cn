---
title: 注释集成
description: 本主题介绍双重写入过程中的注释数据集成。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 02/22/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2021-02-22
ms.openlocfilehash: 221be52b4d66aaa47f9a1919d5d0b9f8459b7ff9
ms.sourcegitcommit: db9b35ce6968cad8874b3c13d4c02d84e2617c8b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/11/2021
ms.locfileid: "5577598"
---
# <a name="note-integration"></a><span data-ttu-id="ea363-103">注释集成</span><span class="sxs-lookup"><span data-stu-id="ea363-103">Note integration</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="ea363-104">在业务流程中，Microsoft Dynamics 365 用户经常会收集有关其客户的信息。</span><span class="sxs-lookup"><span data-stu-id="ea363-104">During business processes, Microsoft Dynamics 365 users often gather information about their customers.</span></span> <span data-ttu-id="ea363-105">此信息记录为活动和注释。</span><span class="sxs-lookup"><span data-stu-id="ea363-105">This information is recorded as activities and notes.</span></span> <span data-ttu-id="ea363-106">本主题介绍双重写入过程中的注释数据集成。</span><span class="sxs-lookup"><span data-stu-id="ea363-106">This topic describes the integration of note data in dual-write.</span></span>

<span data-ttu-id="ea363-107">可以通过以下方式对客户信息进行分类：</span><span class="sxs-lookup"><span data-stu-id="ea363-107">Customer information can be classified in the following ways:</span></span>

+ <span data-ttu-id="ea363-108">**Dynamics 365 用户代表客户处理的可操作信息** – 例如，Contoso（Dynamics 365 用户）正在进行游戏节目。</span><span class="sxs-lookup"><span data-stu-id="ea363-108">**Actionable information that a Dynamics 365 user handles on behalf of a customer** – For example, Contoso (a Dynamics 365 user) is conducting a game show.</span></span> <span data-ttu-id="ea363-109">Contoso 的一位客户（一位客户）希望参加游戏节目。</span><span class="sxs-lookup"><span data-stu-id="ea363-109">One of Contoso's customers (a customer) wants to attend the game show.</span></span> <span data-ttu-id="ea363-110">客户要求 Contoso 员工为其预订游戏节目中的广告位。</span><span class="sxs-lookup"><span data-stu-id="ea363-110">The customer asks a Contoso employee to book a slot in the game show for them.</span></span> <span data-ttu-id="ea363-111">预订在 Contoso 的活动参与者日历中进行。</span><span class="sxs-lookup"><span data-stu-id="ea363-111">The booking occurs in Contoso's event attendee's calendar.</span></span>
+ <span data-ttu-id="ea363-112">**Dynamics 365 用户的可操作信息** – 例如，购买 Surface 设备的客户输入特殊说明，指明该设备在交付前应进行礼品包装。</span><span class="sxs-lookup"><span data-stu-id="ea363-112">**Actionable information for a Dynamics 365 user** – For example, a customer who is purchasing a Surface unit enters special instructions that indicate that the device should be gift wrapped before delivery.</span></span> <span data-ttu-id="ea363-113">这些说明是可操作信息，应由负责包装的 Contoso 员工进行处理。</span><span class="sxs-lookup"><span data-stu-id="ea363-113">These instructions are actionable information that should be handled by the Contoso employee who is responsible for packaging.</span></span>
+ <span data-ttu-id="ea363-114">**非可操作性信息** – 例如，客户访问了 Contoso 商店，并且在与售货员交谈期间表达了 *Halo* 游戏和游戏配件方面的兴趣。</span><span class="sxs-lookup"><span data-stu-id="ea363-114">**Non-actionable information** – For example, a customer visits the Contoso store and, during their conversation with a store associate, expresses interest in *Halo* games and gaming accessories.</span></span> <span data-ttu-id="ea363-115">售货员记录了此信息。</span><span class="sxs-lookup"><span data-stu-id="ea363-115">The store associate makes a note of this information.</span></span> <span data-ttu-id="ea363-116">然后，产品推荐引擎使用此信息向客户提供建议。</span><span class="sxs-lookup"><span data-stu-id="ea363-116">The product recommendations engine then uses it to make recommendations to the customer.</span></span>

<span data-ttu-id="ea363-117">通常，可操作性信息在 Finance and Operations 应用和 Customer Engagement 应用中以 *活动* 形式被捕获。</span><span class="sxs-lookup"><span data-stu-id="ea363-117">In general, actionable information is captured as *activities* in Finance and Operations apps and customer engagement apps.</span></span> <span data-ttu-id="ea363-118">非可操作性信息在 Finance and Operations 应用中以 *注释* 形式被捕获，在 Customer Engagement 应用中以 *批注* 形式被捕获。</span><span class="sxs-lookup"><span data-stu-id="ea363-118">Non-actionable information is captured as *notes* in Finance and Operations apps, and as *annotations* in customer engagement apps.</span></span>

> [!TIP]
> <span data-ttu-id="ea363-119">尽管注释适用于非可操作信息，但如果您想使用它们来存储和处理可操作信息，则应用不会阻止您这么做。</span><span class="sxs-lookup"><span data-stu-id="ea363-119">Although notes are intended for non-actionable information, the apps won't prevent you from using them to store and handle actionable information if you want to use them in that way.</span></span>

<span data-ttu-id="ea363-120">Microsoft 当前正在发布注释集成功能。</span><span class="sxs-lookup"><span data-stu-id="ea363-120">Microsoft is currently releasing functionality for note integration.</span></span> <span data-ttu-id="ea363-121">（活动集成功能将在稍后发布。）注释集成适用于客户、供应商、销售订单和采购订单。</span><span class="sxs-lookup"><span data-stu-id="ea363-121">(Functionality for activity integration will be released later.) Note integration is available for customers, vendors, sales orders, and purchase orders.</span></span>

## <a name="create-a-note-in-a-customer-engagement-app"></a><span data-ttu-id="ea363-122">在 Customer Engagement 应用中创建注释</span><span class="sxs-lookup"><span data-stu-id="ea363-122">Create a note in a customer engagement app</span></span>

<span data-ttu-id="ea363-123">要在 Customer Engagement 应用中创建注释，然后将其同步到 Finance and Operations 应用，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="ea363-123">To create a note in a customer engagement app and then sync it to a Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="ea363-124">在 Customer Engagement 应用中，打开客户的帐户记录。</span><span class="sxs-lookup"><span data-stu-id="ea363-124">In the customer engagement app, open the account record for a customer.</span></span>
2. <span data-ttu-id="ea363-125">在 **时间线** 窗格中，选择加号 (**+**)，然后选择 **注释** 以创建注释。</span><span class="sxs-lookup"><span data-stu-id="ea363-125">In the **Timeline** pane, select the plus sign (**+**), and then select **Note** to create a note.</span></span>

    ![在 Customer Engagement 应用中创建注释](media/notes-ce-1.png)

3. <span data-ttu-id="ea363-127">输入标题和描述，然后选择 **添加注释**。</span><span class="sxs-lookup"><span data-stu-id="ea363-127">Enter a title and description, and then select **Add note**.</span></span>

    ![输入标题和描述](media/notes-ce-2.png)

    <span data-ttu-id="ea363-129">新注释将添加到客户时间线中。</span><span class="sxs-lookup"><span data-stu-id="ea363-129">The new note is added to the customer timeline.</span></span>

    ![客户时间线上的新注释](media/notes-ce-3.png)

4. <span data-ttu-id="ea363-131">登录到 Finance and Operations 应用，然后打开相同的客户记录。</span><span class="sxs-lookup"><span data-stu-id="ea363-131">Sign in to the Finance and Operations app, and open the same customer record.</span></span> <span data-ttu-id="ea363-132">请注意右上角的 **附件** 按钮（回形针符号）表示该记录具有附件。</span><span class="sxs-lookup"><span data-stu-id="ea363-132">Notice that the **Attachments** button (paperclip symbol) in the upper-right corner indicates that the record has an attachment.</span></span>

    ![关于附件的通知](media/notes-ce-4.png)

5. <span data-ttu-id="ea363-134">选择 **附件** 按钮以打开 **附件** 页。</span><span class="sxs-lookup"><span data-stu-id="ea363-134">Select the **Attachments** button to open the **Attachments** page.</span></span> <span data-ttu-id="ea363-135">您应该查找在 Customer Engagement 应用中创建的注释。</span><span class="sxs-lookup"><span data-stu-id="ea363-135">You should find the note that you created in the customer engagement app.</span></span>

    ![来自 Customer Engagement 应用的注释](media/notes-ce-5.png)

<span data-ttu-id="ea363-137">注释的任何更新都会在 Finance and Operations 应用和 Customer Engagement 应用之间来回同步。</span><span class="sxs-lookup"><span data-stu-id="ea363-137">Any updates to the note are synced back and forth between the Finance and Operations app and the customer engagement app.</span></span>

## <a name="create-a-note-in-a-finance-and-operations-app"></a><span data-ttu-id="ea363-138">在 Finance and Operations 应用中创建注释</span><span class="sxs-lookup"><span data-stu-id="ea363-138">Create a note in a Finance and Operations app</span></span>

<span data-ttu-id="ea363-139">您还可以在 Finance and Operations 应用中创建注释，然后它将同步到 Customer Engagement 应用。</span><span class="sxs-lookup"><span data-stu-id="ea363-139">You can also create a note in a Finance and Operations app, and it will be synced to a customer engagement app.</span></span>

<span data-ttu-id="ea363-140">要在 Finance and Operations 应用中创建注释，然后将其同步到 Customer Engagement 应用，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="ea363-140">To create a note in a Finance and Operations app and then sync it to a customer engagement app, follow these steps.</span></span>

1. <span data-ttu-id="ea363-141">在 Finance and Operations 应用中的 **附件** 页面上，选择 **新建**\>**注释**。</span><span class="sxs-lookup"><span data-stu-id="ea363-141">In the Finance and Operations app, on the **Attachments** page, select **New** \> **Note**.</span></span>

    ![在 Finance and Operations 应用中创建注释](media/notes-fo-1.png)

2. <span data-ttu-id="ea363-143">输入标题和一组简要说明，然后选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="ea363-143">Enter a title and a brief set of instructions, and then select **Save**.</span></span>

    ![输入标题和说明](media/notes-fo-2.png)

3. <span data-ttu-id="ea363-145">在 Customer Engagement 应用中，更新记录。</span><span class="sxs-lookup"><span data-stu-id="ea363-145">In the customer engagement app, update the record.</span></span> <span data-ttu-id="ea363-146">您应该会在时间线上找到新注释。</span><span class="sxs-lookup"><span data-stu-id="ea363-146">You should find the new note on the timeline.</span></span>

    ![Customer Engagement 应用中时间线上的新注释](media/notes-fo-3.png)

<span data-ttu-id="ea363-148">您可以将注释归类为内部注释或外部注释。</span><span class="sxs-lookup"><span data-stu-id="ea363-148">You can classify a note as either internal or external.</span></span>

- <span data-ttu-id="ea363-149">在 Finance and Operations 应用的 **附件** 页上，打开注释，然后在 **限制** 字段中，选择 **内部** 或 **外部**。</span><span class="sxs-lookup"><span data-stu-id="ea363-149">In the Finance and Operations app, on the **Attachments** page, open the note, and then, in the **Restriction** field, select **Internal** or **External**.</span></span>

    ![限制字段](media/notes-fo-4.png)

<span data-ttu-id="ea363-151">您还可以创建 URL。</span><span class="sxs-lookup"><span data-stu-id="ea363-151">You can also create a URL.</span></span>

1. <span data-ttu-id="ea363-152">在 Finance and Operations 应用中的 **附件** 页面上，选择 **新建**\>**URL**。</span><span class="sxs-lookup"><span data-stu-id="ea363-152">In the Finance and Operations app, on the **Attachments** page, select **New** \> **URL**.</span></span>
2. <span data-ttu-id="ea363-153">输入标题和 URL。</span><span class="sxs-lookup"><span data-stu-id="ea363-153">Enter a title and the URL.</span></span>
3. <span data-ttu-id="ea363-154">在 **限制** 字段中，选择 **内部** 或 **外部**。</span><span class="sxs-lookup"><span data-stu-id="ea363-154">In the **Restriction** field, select **Internal** or **External**.</span></span>

    ![在 Finance and Operations 应用中创建 URL](media/notes-fo-5.png)

4. <span data-ttu-id="ea363-156">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="ea363-156">Select **Save**.</span></span>

    <span data-ttu-id="ea363-157">由于 Customer Engagement 应用没有 URL 类型，因此该 URL 已与双重写入功能集成为注释。</span><span class="sxs-lookup"><span data-stu-id="ea363-157">Because customer engagement apps don't have a URL type, the URL is integrated with dual-write as a note.</span></span>

    ![Customer Engagement 应用中显示为注释的 URL](media/notes-ce-6.png)

> [!NOTE]
> <span data-ttu-id="ea363-159">不支持文件附件。</span><span class="sxs-lookup"><span data-stu-id="ea363-159">File attachments aren't supported.</span></span>

## <a name="templates"></a><span data-ttu-id="ea363-160">模板</span><span class="sxs-lookup"><span data-stu-id="ea363-160">Templates</span></span>

<span data-ttu-id="ea363-161">注释集成包括表映射的集合，这些映射在数据交互期间协同工作，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="ea363-161">Note integration includes a collection of table maps that work together during data interaction, as shown in the following table.</span></span>

| <span data-ttu-id="ea363-162">Finance and Operations 应用</span><span class="sxs-lookup"><span data-stu-id="ea363-162">Finance and Operations app</span></span> | <span data-ttu-id="ea363-163">Customer engagement 应用</span><span class="sxs-lookup"><span data-stu-id="ea363-163">Customer engagement app</span></span> | <span data-ttu-id="ea363-164">说明</span><span class="sxs-lookup"><span data-stu-id="ea363-164">Description</span></span> |
|----------------------------|-------------------------|-------------|
| [<span data-ttu-id="ea363-165">客户附件</span><span class="sxs-lookup"><span data-stu-id="ea363-165">Customer Attachments</span></span>](mapping-reference.md#230) | <span data-ttu-id="ea363-166">批注</span><span class="sxs-lookup"><span data-stu-id="ea363-166">Annotations</span></span> | <span data-ttu-id="ea363-167">使用纯文本和 URL 来捕获客户特定信息的企业（针对组织和个人）。</span><span class="sxs-lookup"><span data-stu-id="ea363-167">Businesses that use plain text and URLs to capture customer-specific information (for both organizations and persons).</span></span> |
| [<span data-ttu-id="ea363-168">供应商单据附件</span><span class="sxs-lookup"><span data-stu-id="ea363-168">Vendor document attachments</span></span>](mapping-reference.md#231) | <span data-ttu-id="ea363-169">批注</span><span class="sxs-lookup"><span data-stu-id="ea363-169">Annotations</span></span> | <span data-ttu-id="ea363-170">使用纯文本和 URL 来捕获供应商特定信息的企业（针对组织和个人）。</span><span class="sxs-lookup"><span data-stu-id="ea363-170">Businesses that use plain text and URLs to capture vendor-specific information (for both organizations and persons).</span></span> |
| [<span data-ttu-id="ea363-171">销售订单头文档附件</span><span class="sxs-lookup"><span data-stu-id="ea363-171">Sales order header document attachments</span></span>](mapping-reference.md#229) | <span data-ttu-id="ea363-172">批注</span><span class="sxs-lookup"><span data-stu-id="ea363-172">Annotations</span></span> | <span data-ttu-id="ea363-173">使用纯文本和 URL 来捕获销售订单特定信息的企业。</span><span class="sxs-lookup"><span data-stu-id="ea363-173">Businesses that use plain text and URLs to capture sales order–specific information.</span></span> |
| [<span data-ttu-id="ea363-174">采购订单头文档附件</span><span class="sxs-lookup"><span data-stu-id="ea363-174">Purchase order header document attachments</span></span>](mapping-reference.md#232) | <span data-ttu-id="ea363-175">批注</span><span class="sxs-lookup"><span data-stu-id="ea363-175">Annotations</span></span> | <span data-ttu-id="ea363-176">使用纯文本和 URL 来捕获采购订单特定信息的企业。</span><span class="sxs-lookup"><span data-stu-id="ea363-176">Businesses that use plain text and URLs to capture purchase order–specific information.</span></span> |

<span data-ttu-id="ea363-177">有关更多信息，请参见[双重写入映射参考](mapping-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="ea363-177">For more information, see [Dual-write mapping reference](mapping-reference.md).</span></span>
