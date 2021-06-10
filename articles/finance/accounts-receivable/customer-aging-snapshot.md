---
title: 客户帐龄快照
description: 本主题提供有关客户帐龄快照的信息。 帐龄快照计算某个时间点一组客户的帐龄余额。
author: JodiChristiansen
ms.date: 05/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-05-05
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: b88d3fe97d14d3e2f766367de501148063582000
ms.sourcegitcommit: 16376a301a0f121f384d77f9976638f701f8e88e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/28/2021
ms.locfileid: "6123354"
---
# <a name="customer-aging-snapshots"></a><span data-ttu-id="6a9b9-104">客户帐龄快照</span><span class="sxs-lookup"><span data-stu-id="6a9b9-104">Customer aging snapshots</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6a9b9-105">本主题提供有关客户帐龄快照的信息。</span><span class="sxs-lookup"><span data-stu-id="6a9b9-105">This topic provides information about customer aging snapshots.</span></span> <span data-ttu-id="6a9b9-106">帐龄快照计算某个时间点一组客户的帐龄余额。</span><span class="sxs-lookup"><span data-stu-id="6a9b9-106">An aging snapshot calculates aged balances for a group of customers at a point in time.</span></span> <span data-ttu-id="6a9b9-107">您可以为客户池中的所有客户或某些客户创建帐龄快照记录。</span><span class="sxs-lookup"><span data-stu-id="6a9b9-107">You can create aging snapshot records either for all customers or for the customers in a customer pool.</span></span>

<span data-ttu-id="6a9b9-108">帐龄快照中的信息显示在 **帐龄余额** 列表页和 **收款** 页上。</span><span class="sxs-lookup"><span data-stu-id="6a9b9-108">Information from aging snapshots is shown on the **Aged balances** list page and the **Collections** page.</span></span> <span data-ttu-id="6a9b9-109">您必须创建一个帐龄快照，然后才能使用 **帐龄余额** 列表页。</span><span class="sxs-lookup"><span data-stu-id="6a9b9-109">You must create an aging snapshot before you can use the **Aged balances** list page.</span></span> <span data-ttu-id="6a9b9-110">列表页仅列出为其创建了帐龄快照的客户。</span><span class="sxs-lookup"><span data-stu-id="6a9b9-110">The list page lists only customers that an aging snapshot has been created for.</span></span>

<span data-ttu-id="6a9b9-111">**客户信用和收款** 工作区也显示客户帐龄。</span><span class="sxs-lookup"><span data-stu-id="6a9b9-111">The **Customer credit and collections** workspace also shows the customer aging.</span></span> <span data-ttu-id="6a9b9-112">有关详细信息，请参阅[信用和收款管理 Power BI 内容](credit-collections-power-bi.md)。</span><span class="sxs-lookup"><span data-stu-id="6a9b9-112">For more information, see [Credit and collections management Power BI content](credit-collections-power-bi.md).</span></span>

> [!NOTE]
> <span data-ttu-id="6a9b9-113">为了帮助减少创建帐龄快照所需的时间，请在 **功能管理** 工作区打开 **客户帐龄性能增强** 功能。</span><span class="sxs-lookup"><span data-stu-id="6a9b9-113">To help reduce the time that is required to create an aging snapshot, turn on the **Customer aging performance enhancement** feature in the **Feature management** workspace.</span></span> <span data-ttu-id="6a9b9-114">但是，启用此功能后请勿使用客户池。</span><span class="sxs-lookup"><span data-stu-id="6a9b9-114">However, don't use customer pools when this feature is turned on.</span></span> <span data-ttu-id="6a9b9-115">如果选择了客户池，此功能将不起作用，不过您仍然可以创建帐龄快照。</span><span class="sxs-lookup"><span data-stu-id="6a9b9-115">If a customer pool is selected, the feature won't work, but you can still create an aging snapshot.</span></span>

<span data-ttu-id="6a9b9-116">创建客户帐龄快照时，请使用以下字段输入有关它的信息：</span><span class="sxs-lookup"><span data-stu-id="6a9b9-116">When you create a customer aging snapshot, use the following fields to enter information about it:</span></span>

- <span data-ttu-id="6a9b9-117">**帐龄期间定义** – 选择帐龄快照的帐龄时间定义。</span><span class="sxs-lookup"><span data-stu-id="6a9b9-117">**Aging period definition** – Select the aging period definition for the aging snapshot.</span></span> <span data-ttu-id="6a9b9-118">每个帐龄期间定义可以有一个帐龄快照。</span><span class="sxs-lookup"><span data-stu-id="6a9b9-118">You can have one aging snapshot for each aging period definition.</span></span> <span data-ttu-id="6a9b9-119">帐龄快照和帐龄期间定义必须分别创建。</span><span class="sxs-lookup"><span data-stu-id="6a9b9-119">The aging snapshot and the aging period definition must be created separately.</span></span>
- <span data-ttu-id="6a9b9-120">**池 ID** – 此字段为可选字段。</span><span class="sxs-lookup"><span data-stu-id="6a9b9-120">**Pool ID** – This field is optional.</span></span> <span data-ttu-id="6a9b9-121">您可以使用池定义应在帐龄快照中处理的客户集。</span><span class="sxs-lookup"><span data-stu-id="6a9b9-121">You can use a pool to define the set of customers that should be processed in the aging snapshot.</span></span> <span data-ttu-id="6a9b9-122">如果在此字段中选择客户池，将仅为属于该客户池的客户帐户创建帐龄快照。</span><span class="sxs-lookup"><span data-stu-id="6a9b9-122">If you select a customer pool in this field, an aging snapshot is created only for the customer accounts that are part of that customer pool.</span></span> <span data-ttu-id="6a9b9-123">所选客户池必须为 **帐龄快照** 类型。</span><span class="sxs-lookup"><span data-stu-id="6a9b9-123">The selected customer pool must be of the **Aging snapshot** type.</span></span> <span data-ttu-id="6a9b9-124">如果将此字段保留为空白，将为所有客户帐户创建帐龄快照。</span><span class="sxs-lookup"><span data-stu-id="6a9b9-124">If you leave this field blank, an aging snapshot is created for all customer accounts.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6a9b9-125">如果 **客户帐龄性能增强** 功能已启用，请勿选择客户池。</span><span class="sxs-lookup"><span data-stu-id="6a9b9-125">If the **Customer aging performance enhancement** feature is turned on, don't select a customer pool.</span></span>

- <span data-ttu-id="6a9b9-126">**条件** – 帐龄快照将根据您选择的日期计算帐龄：</span><span class="sxs-lookup"><span data-stu-id="6a9b9-126">**Criteria** – The aging snapshot will age based on the date that you select:</span></span>

    - <span data-ttu-id="6a9b9-127">**交易日期** – 每项交易根据交易日期计算帐龄。</span><span class="sxs-lookup"><span data-stu-id="6a9b9-127">**Transaction date** – Each transaction is aged based on its transaction date.</span></span>
    - <span data-ttu-id="6a9b9-128">**截止日期** – 每项交易根据截止日期计算帐龄。</span><span class="sxs-lookup"><span data-stu-id="6a9b9-128">**Due date** – Each transaction is aged based on its due date.</span></span>
    - <span data-ttu-id="6a9b9-129">**单据日期** – 每项交易根据单据日期计算帐龄。</span><span class="sxs-lookup"><span data-stu-id="6a9b9-129">**Document date** – Each transaction is aged based on its document date.</span></span>

- <span data-ttu-id="6a9b9-130">**龄截至日期** – 在帐龄快照的 **当前日期** 字段中选择要使用的日期。</span><span class="sxs-lookup"><span data-stu-id="6a9b9-130">**Aging as of** – Select the date to use in the **Current date** field for the aging snapshot.</span></span> <span data-ttu-id="6a9b9-131">然后将根据该日期计算帐龄期间。</span><span class="sxs-lookup"><span data-stu-id="6a9b9-131">Aging periods are then calculated based on that date.</span></span> 

    - <span data-ttu-id="6a9b9-132">**今天的日期** – 使用系统日期。</span><span class="sxs-lookup"><span data-stu-id="6a9b9-132">**Today's date** – Use the system date.</span></span> <span data-ttu-id="6a9b9-133">如果将处理设置为以批处理作业运行，则选择此选项。</span><span class="sxs-lookup"><span data-stu-id="6a9b9-133">Select this option if processing is set up to run in a recurring batch.</span></span> <span data-ttu-id="6a9b9-134">然后，每次运行批处理时，都会使用该运行的系统日期。</span><span class="sxs-lookup"><span data-stu-id="6a9b9-134">Then, every time that the batch is run, the system date of that run is used.</span></span>
    - <span data-ttu-id="6a9b9-135">**选定日期** – 使用您指定的日期。</span><span class="sxs-lookup"><span data-stu-id="6a9b9-135">**Selected date** – Use a date that you specify.</span></span> <span data-ttu-id="6a9b9-136">如果选择此选项，必须输入帐龄日期。</span><span class="sxs-lookup"><span data-stu-id="6a9b9-136">If you select this option, you must enter an aging date.</span></span>

    <span data-ttu-id="6a9b9-137">例如，当前的帐龄期间为 30 天。</span><span class="sxs-lookup"><span data-stu-id="6a9b9-137">For example, the current aging period is 30 days.</span></span> <span data-ttu-id="6a9b9-138">如果您在此字段中选择 **今天的日期**，当前的帐龄期间将从今天的日期开始，然后包括前面 29 天。</span><span class="sxs-lookup"><span data-stu-id="6a9b9-138">If you select **Today's date** in this field, the current aging period starts on today's date and then includes the previous 29 days.</span></span> <span data-ttu-id="6a9b9-139">如果您在此字段中选择 **选定日期** 并输入日期，当前的帐龄期间将从指定日期开始，然后包括前面 29 天。</span><span class="sxs-lookup"><span data-stu-id="6a9b9-139">If you select **Selected date** and enter a date, the current aging period starts on the specified date and then includes the previous 29 days.</span></span>

- <span data-ttu-id="6a9b9-140">**更新收款状态** – 将此选项设置为 **是**，可以在帐龄日期超过 **承诺付款日期** 字段中的日期时，将 **收款** 页上的交易收款状态从 **承诺付款** 更改为 **未实现付款承诺**。</span><span class="sxs-lookup"><span data-stu-id="6a9b9-140">**Update collection status** – Set this option to **Yes** to update the collection status of transactions on the **Collections** page from **Promise to pay** to **Promise to pay broken** if the aging date is beyond the date in the **Promise to pay date** field.</span></span> <span data-ttu-id="6a9b9-141">将此选项设置为 **否**，**收款** 页上的收款状态保持不变。</span><span class="sxs-lookup"><span data-stu-id="6a9b9-141">Set this option to **No** to leave the collection status unchanged on the **Collections** page.</span></span>
- <span data-ttu-id="6a9b9-142">**包括余额为零的客户** – 将此选项设置为 **是** 将包括所有客户，无论他们的余额是多少。</span><span class="sxs-lookup"><span data-stu-id="6a9b9-142">**Include customers with zero balance** – Set this option to **Yes** to include all customers, regardless of their balance.</span></span> <span data-ttu-id="6a9b9-143">如果您包括所有客户，我们建议您打开 **客户帐龄性能增强** 功能，并且不要使用客户池。</span><span class="sxs-lookup"><span data-stu-id="6a9b9-143">If you include all customers, we recommend that you to turn on the **Customer aging performance enhancement** feature, and that you not use customer pools.</span></span> <span data-ttu-id="6a9b9-144">将此选项设置为 **否** 将仅包括有余额的客户。</span><span class="sxs-lookup"><span data-stu-id="6a9b9-144">Set this option to **No** to include only customers that have a balance.</span></span> <span data-ttu-id="6a9b9-145">此设置有助于提高性能，因为会跳过没有余额的客户。</span><span class="sxs-lookup"><span data-stu-id="6a9b9-145">This setting helps speed up performance, because customers that don't have a balance are skipped.</span></span>
- <span data-ttu-id="6a9b9-146">**公司范围** – 在 **公司范围** 选项卡中，选择要包括在帐龄快照中的法人（公司）。</span><span class="sxs-lookup"><span data-stu-id="6a9b9-146">**Company range** – On the **Company range** tab, select the legal entities (companies) to include in the aging snapshot.</span></span> <span data-ttu-id="6a9b9-147">仅设置了集中付款的法人可供选择。</span><span class="sxs-lookup"><span data-stu-id="6a9b9-147">Only legal entities that are set up for centralized payments are available for selection.</span></span> <span data-ttu-id="6a9b9-148">然后，来自所选法人的交易将包括在所有这些法人中具有相同当事方 ID 的客户的帐龄期间内。</span><span class="sxs-lookup"><span data-stu-id="6a9b9-148">Transactions from the selected legal entities are then included in the aging periods for customers that have the same party ID in all those legal entities.</span></span> <span data-ttu-id="6a9b9-149">货币金额将转换为您创建帐龄快照时登录的法人的货币。</span><span class="sxs-lookup"><span data-stu-id="6a9b9-149">Currency amounts are converted to the currency of the legal entity that you're signed in to when you create the aging snapshot.</span></span>

<span data-ttu-id="6a9b9-150">我们建议您将此流程计划为批量运行。</span><span class="sxs-lookup"><span data-stu-id="6a9b9-150">We recommend that you schedule this process to run in a batch.</span></span>

> [!NOTE]
> <span data-ttu-id="6a9b9-151">为帮助在创建帐龄快照时提高批处理性能，在 **应收帐款参数** 页上 **收款** 选项卡上的 **收款默认值** 快速选项卡上的 **最大批处理任务数** 字段中输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="6a9b9-151">To help improve batch performance when aging snapshots are created, enter a number in the **Maximum number of batch tasks** field on the **Collections defaults** FastTab on the **Collections** tab of the **Accounts receivable parameters** page.</span></span> <span data-ttu-id="6a9b9-152">在 **帐龄客户余额** 字段中，我们建议您从默认值 **100** 开始，然后根据您的情况调整值来优化处理。</span><span class="sxs-lookup"><span data-stu-id="6a9b9-152">In the **Age customer balances** field, we recommend that you start with the default value of **100** and then adjust the value to optimize processing for your situation.</span></span>

