---
title: 配置和使用呼叫中心订单保留
description: 本主题介绍如何使用 Dynamics 365 Commerce 处理保留订单。
author: josaw1
manager: AnnBe
ms.date: 05/14/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: MCRHoldCodeTable, MCRSalesTableOrderHistory, MCRHoldCodeTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 79132
ms.assetid: 7c00dc35-73e5-400a-8587-22f37ddfc0e0
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 08c0eda418af1aa56c6cc71ca1f7f10460651bc9
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/01/2020
ms.locfileid: "3021711"
---
# <a name="configure-and-work-with-call-center-order-holds"></a><span data-ttu-id="3bbb9-103">配置和使用呼叫中心订单保留</span><span class="sxs-lookup"><span data-stu-id="3bbb9-103">Configure and work with call center order holds</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3bbb9-104">本主题介绍 Dynamics 365 Commerce 中针对呼叫中心订单的订单保留功能。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-104">This topic describes the order hold features that Dynamics 365 Commerce has for call center orders.</span></span>

## <a name="configuring-call-center-order-holds"></a><span data-ttu-id="3bbb9-105">配置呼叫中心订单保留</span><span class="sxs-lookup"><span data-stu-id="3bbb9-105">Configuring call center order holds</span></span>

<span data-ttu-id="3bbb9-106">若要使用呼叫中心订单保留功能，首先必须定义保留代码。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-106">To use the call center order hold features, you must first define hold codes.</span></span> <span data-ttu-id="3bbb9-107">若要根据业务需求创建一组用户定义的保留代码，请转至**销售和市场营销** \> **设置** \> **销售订单** \> **订单保留代码**。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-107">To create a set of user-defined hold codes, based on your business requirements, go to **Sales and marketing** \> **Setup** \> **Sales orders** \> **Order hold codes**.</span></span> <span data-ttu-id="3bbb9-108">可选择通过为一个保留代码将**销售订单的默认值**选项设置为**是**，将该保留代码标记为默认保留代码。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-108">You can optionally flag one of the hold codes as the default hold code by setting the **Default for sales order** option to **Yes** for it.</span></span> <span data-ttu-id="3bbb9-109">只要保留销售订单，都将使用这个保留代码。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-109">This hold code will be used any time that a sales order is put on hold.</span></span> <span data-ttu-id="3bbb9-110">如果销售订单有预留库存，并且如果因为特定原因要保留该订单而必须自动删除预留，则为原因代码将**删除库存预留**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-110">If a sales order has reserved inventory, and the reservations must be automatically removed if the order is put on hold for a particular reason, set the **Remove inventory reservations** option to **Yes** for the reason codes.</span></span>

<span data-ttu-id="3bbb9-111">若要指定当保留订单的用户输入可选注释时将捕获的注释类型，请转至**应收帐款** \> **设置** \> **应收帐款参数**，然后在**销售设置**快速选项卡上的**常规**选项卡中，设置**注释类型**字段。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-111">To specify the type of note that will be captured when users who put a sales order on hold enter optional notes, go to **Accounts receivable** \> **Setup** \> **Accounts receivable parameters**, and then, on the **Sales setup** FastTab, on the **General** tab, set the **Note type** field.</span></span> <span data-ttu-id="3bbb9-112">请使用**保留销售订单状态**字段定义当保留的销售订单在**客户服务**页中查看时使用的突出显示颜色。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-112">Use the **On Hold sales order status** field to define the color that will be used to highlight sales orders that are on hold when they are viewed on the **Customer service** page.</span></span>

<span data-ttu-id="3bbb9-113">若要创建一组可选的保留原因代码，请转至 **Retail 和 Commerce** \> **渠道设置** \> **信息代码**。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-113">To create an optional set of hold reason codes, go to **Retail and Commerce** \> **Channel setup** \> **Info codes**.</span></span> <span data-ttu-id="3bbb9-114">这些信息代码可用作辅助原因代码以进一步定义主保留代码。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-114">These info codes can be used as a secondary reason code to further define the main hold code.</span></span> <span data-ttu-id="3bbb9-115">选择**新建**创建原因代码集，然后选择**子代码**定义更多原因的列表。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-115">Select **New** to create a reason code set, and then select **Subcodes** to define the list of additional reasons.</span></span> <span data-ttu-id="3bbb9-116">若要将定义的任何信息代码链接到呼叫中心渠道，请转至 **Retail 和 Commerce** \> **渠道** \> **呼叫中心** \> **所有呼叫中心**。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-116">To link any info codes that you define to the call center channel, go to **Retail and Commerce** \> **Channels** \> **Call centers** \> **All call centers**.</span></span> <span data-ttu-id="3bbb9-117">在**常规**快速选项卡上，设置**保留代码**字段。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-117">On the **General** FastTab, set the **Hold code** field.</span></span>

## <a name="putting-orders-on-hold"></a><span data-ttu-id="3bbb9-118">保留订单</span><span class="sxs-lookup"><span data-stu-id="3bbb9-118">Putting orders on hold</span></span>

<span data-ttu-id="3bbb9-119">呼叫中心用户在 Commerce 后端程序中创建的订单可手动保留，在特定情况下也可以自动保留。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-119">Orders that call center users create in the back-office Commerce program can be manually put on hold manually or automatically in specific situations.</span></span>

<span data-ttu-id="3bbb9-120">但是在订单录入期间提交和确认订单之前，呼叫中心用户可能希望保留订单，以防下达给仓库进行进一步处理。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-120">During order entry, but before order submission and confirmation, call center users might want to manually put an order on hold to prevent it from being released to the warehouse for further processing.</span></span> <span data-ttu-id="3bbb9-121">例如，下订单的客户可能未准备好提交该订单，或者缺少处理该订单所需关键数据。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-121">For example, the customer who is placing the order might not be ready to commit to it, or critical data that is required in order to process the order might be missing.</span></span>

<span data-ttu-id="3bbb9-122">在订单录入页，呼叫中心用户可通过使用订单录入菜单**销售订单**选项卡上的**订单保留**选项保留订单。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-122">On the order entry page, the call center user can put an order on hold by using the **Order holds** option on the **Sales order** tab of the order entry menu.</span></span> <span data-ttu-id="3bbb9-123">用户还可以在呼叫中心销售订单上选择**完成**时选择**销售订单摘要**页中的**保留**菜单项。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-123">Alternatively, the user can select the **Hold** menu item on the **Sales order summary** page that appears when he or she selects **Complete** on a call center sales order.</span></span>

<span data-ttu-id="3bbb9-124">这两种情况下都将显示**订单保留**页。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-124">In both cases, the **Order holds** page appears.</span></span> <span data-ttu-id="3bbb9-125">然后，用户可选择**新建**为订单创建保留。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-125">The user can then select **New** to create a hold for the order.</span></span> <span data-ttu-id="3bbb9-126">在**保留代码**字段中，用户应选择最能描述保留原因的代码。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-126">In the **Hold code** field, the user should select the code that best describes the reason for the hold.</span></span> <span data-ttu-id="3bbb9-127">（可选）在**原因代码**字段中，用户可以再选择一个代码以进一步说明保留的原因。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-127">In the **Reason code** field, the user can optionally select an additional code to provide a second level of description of the hold.</span></span>

<span data-ttu-id="3bbb9-128">在**注释**快速选项卡上的**保留注释**字段中，用户可输入更多自由格式的注释，以提供更多有关保留的上下文或信息。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-128">On the **Notes** FastTab, in the **Hold Notes** field, the user can enter additional, free-form notes to provide additional context or information about the hold.</span></span> <span data-ttu-id="3bbb9-129">这些注释可以在以后帮助其他查看或处理这个保留订单的用户。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-129">These notes can help other users who review or work with the hold order later.</span></span>

<span data-ttu-id="3bbb9-130">输入并保存保留信息之后，用户可关闭**订单保留**页。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-130">After the hold information is entered and saved, the user can close the **Order holds** page.</span></span> <span data-ttu-id="3bbb9-131">然后，用户将回到销售订单录入页。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-131">The user is then returned to the sales order entry page.</span></span> <span data-ttu-id="3bbb9-132">如果不需要对销售订单执行更多操作，用户可关闭销售订单录入页。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-132">If no further actions are required on the sales order, the user can close the sales order entry page.</span></span>

<span data-ttu-id="3bbb9-133">如果呼叫中心渠道中的**启用订单完成**标志已开启，则不必为已保留的订单应用付款。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-133">If the **Enable order completion** flag is turned on in the call center channel, payment doesn't have to applied to an order that is put on hold.</span></span> <span data-ttu-id="3bbb9-134">相反，对于未保留的销售订单，应用付款之前，用户不能离开销售订单录入页。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-134">By contrast, for a sales order that isn't put on hold, users can't leave the sales order entry page until payment is applied.</span></span> <span data-ttu-id="3bbb9-135">当然，解除订单保留之前，需要付款。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-135">Of course, payment will be required before the order hold is released.</span></span>

<span data-ttu-id="3bbb9-136">此外，呼叫中心用户还可以出于某种原因手动保留可疑订单。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-136">Additionally, call center users can put a manual fraud hold on orders that are suspicious for some reason.</span></span> <span data-ttu-id="3bbb9-137">也可以手动保留匹配有效欺诈条件和规则的订单。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-137">Orders can also be put on hold automatically when they match active fraud criteria and rules.</span></span> <span data-ttu-id="3bbb9-138">有关这种订单保留的详细信息，请参阅[设置欺诈警示](https://docs.microsoft.com/dynamics365/unified-operations/retail/set-up-fraud-alerts)。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-138">For more information on about this type of order hold, see [Set up fraud alerts](https://docs.microsoft.com/dynamics365/unified-operations/retail/set-up-fraud-alerts).</span></span>

## <a name="viewing-and-managing-orders-that-are-on-hold"></a><span data-ttu-id="3bbb9-139">查看和管理保留的订单</span><span class="sxs-lookup"><span data-stu-id="3bbb9-139">Viewing and managing orders that are on hold</span></span>

### <a name="viewing-hold-information-for-a-single-sales-order"></a><span data-ttu-id="3bbb9-140">查看单个销售订单的保留信息</span><span class="sxs-lookup"><span data-stu-id="3bbb9-140">Viewing hold information for a single sales order</span></span>

<span data-ttu-id="3bbb9-141">在**客户服务**页中，用户可目视识别保留的订单，因为这种订单以特定颜色突出显示。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-141">On the **Customer service** page, users can visually identify orders that are on hold, because the order lines are highlighted in a specific color.</span></span> <span data-ttu-id="3bbb9-142">此颜色由**应收帐款参数**页中的**保留销售订单状态**字段定义。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-142">This color is defined by the **On Hold sales order status** field on the **Accounts receivable parameters** page.</span></span>

> [!NOTE]
> <span data-ttu-id="3bbb9-143">如果在页中选中了行，突出显示颜色可能不可见。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-143">If the line is selected on the page, the highlight color isn't visible.</span></span>

<span data-ttu-id="3bbb9-144">用户也可以查看销售订单详细的状态信息以了解是否已保留该订单。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-144">Users can also view detailed status information for a sales order to learn whether the order is on hold.</span></span> <span data-ttu-id="3bbb9-145">可从**所有销售订单**或**客户服务**页访问详细的状态信息。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-145">The detailed status information can be accessed from the **All sales orders** or **Customer service** page.</span></span> <span data-ttu-id="3bbb9-146">如果已保留某个订单，将为其设置**请勿处理**标志，并且**详细状态**字段将显示状态**保留**或**欺诈保留**，具体取决于实际情况。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-146">If an order is on hold, the **Do not process** flag is set for it, and the **Detailed status** field shows a status of either **On Hold** or **Fraud Hold**, depending on the scenario.</span></span>

<span data-ttu-id="3bbb9-147">若要查看单个订单保留的详细信息，用户可从**客户服务**页通过使用所选订单的**选项**菜单打开**订单保留**页的详细视图。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-147">To view the details of an individual order hold, users can open a detailed view of the **Order hold** page from the **Customer service** page, by using the **Options** menu for the selected order.</span></span> <span data-ttu-id="3bbb9-148">用户还可以从**所有销售订单**页访问此视图，方法是选择**销售订单**选项卡上的**订单保留**菜单项。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-148">Users can also access this view from the **All sales order** page, by selecting the **Order holds** menu item on the **Sales order** tab.</span></span>

### <a name="viewing-all-orders-that-are-on-hold"></a><span data-ttu-id="3bbb9-149">查看所有保留的订单</span><span class="sxs-lookup"><span data-stu-id="3bbb9-149">Viewing all orders that are on hold</span></span>

<span data-ttu-id="3bbb9-150">若要查看已手动或自动暂停的所有订单，请转至 **Retail 和 Commerce** \> **客户** \> **订单保留**。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-150">To view all orders that have been put on manual or automatic hold, go to **Retail and Commerce** \> **Customers** \> **Order holds**.</span></span>

<span data-ttu-id="3bbb9-151">**订单保留**工作台提供与手动或欺诈有关的保留操作导致保留的所有订单的列表视图。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-151">The **Order holds** workbench provides a list view of all orders that are on hold because of manual or fraud-related hold actions.</span></span> <span data-ttu-id="3bbb9-152">通过利用页面上的标准筛选和排序选项，用户可以创建视图，以便处理或管理其负责检查的特定保留代码。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-152">By taking advantage of the standard filtering and sorting options on the page, users can create views that let them work with or manage specific hold codes that they are responsible for reviewing.</span></span> <span data-ttu-id="3bbb9-153">**订单保留**工作台也会指示订单已保留的天数。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-153">The **Order holds** workbench also indicates the number of days that an order has been on hold.</span></span> <span data-ttu-id="3bbb9-154">此信息可以帮助用户为队列设置优先级。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-154">This information can help users prioritize the queue.</span></span>

<span data-ttu-id="3bbb9-155">若要获取保留订单更详细的视图，用户可单击菜单中的**订单保留**选项。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-155">To get a more detailed view of the orders that are on hold, users can click the **Order hold** option on the menu.</span></span> <span data-ttu-id="3bbb9-156">此视图提供有关客户的信息，以及已经应用于订单、客户或保留操作的任何注释。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-156">This view providing information about the customer, any notes that have been applied to the order, customer, or hold action.</span></span> <span data-ttu-id="3bbb9-157">如果保留订单是因为该订单匹配欺诈规则，此视图还提供有关自动保留的原因。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-157">The view also provides details about the reason for an automatic hold, if the order was put on hold because it matched a fraud rule.</span></span>

<span data-ttu-id="3bbb9-158">用户从**订单保留**的列表视图和详细视图都可以查看或编辑与订单有关的更多信息，如付款、总额和注释。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-158">From both the list view and the detailed view of the **Order holds** page, users can view or edit additional order-related information, such as payments, totals, and notes.</span></span>

<span data-ttu-id="3bbb9-159">如果贵公司的多位用户同时处理保留队列，**保留签出**选项卡可能很有用。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-159">The options on the **Hold checkout** tab might be useful if multiple users in your company work on the hold queue at the same time.</span></span> <span data-ttu-id="3bbb9-160">通过选择**签出**选项，用户可以指示自己真正查看和调查保留的订单。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-160">By selecting the **Check out** option, users can indicate that they are working to review and investigate the order hold.</span></span> <span data-ttu-id="3bbb9-161">这样，其他用户就不会浪费时间做同样的工作。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-161">In this way, other users don't waste time by trying to do the same work.</span></span> <span data-ttu-id="3bbb9-162">通过**订单保留**的详细视图，用户可查看有关签出日期和时间，以及签出了保留记录的用户的信息。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-162">From the detailed view of the **Order holds** page, users can view information about the checkout date and time, and the user who checked out the hold record.</span></span>

<span data-ttu-id="3bbb9-163">签出保留订单后，只有其签出者才能清除签出。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-163">After a hold record is checked out, only the user who checked it out can clear the checkout.</span></span> <span data-ttu-id="3bbb9-164">此项限制旨在防止用户接手其他用户已在处理的记录。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-164">This restriction is intended to prevent users from taking records that other users are already working on.</span></span> <span data-ttu-id="3bbb9-165">若要将订单放回队列以便其他用户可以处理，需要由记录的签出用户选择**清除签出**选项。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-165">To release an order back to the queue so that other users can work on it, the user who checked out the record selects the **Clear checkout** option.</span></span>

> [!NOTE]
> <span data-ttu-id="3bbb9-166">清除签出时不会解除保留。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-166">The hold isn't released when the checkout is cleared.</span></span>

<span data-ttu-id="3bbb9-167">在某些情况下（如用户因病请假或离职），可能必须将已签出给该用户的记录重新分配给其他用户。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-167">In some situations, such as when a user is out sick or has left the company, records that are checked out to that user might have to be reassigned to another user.</span></span> <span data-ttu-id="3bbb9-168">经理可以通过使用**覆盖签出**选项重新分配记录。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-168">A manager can reassign records by using the **Override checkout** option.</span></span>

## <a name="releasing-orders-that-are-on-hold"></a><span data-ttu-id="3bbb9-169">释放已保留的订单</span><span class="sxs-lookup"><span data-stu-id="3bbb9-169">Releasing orders that are on hold</span></span>

<span data-ttu-id="3bbb9-170">在**订单保留**页的列表视图和详细视图中，**清除保留**选项卡中包含用于解除订单保留的选项。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-170">In both the list view and the detailed view of the **Order holds** page, the **Clear hold** tab contains the options that are used to release an order hold.</span></span> <span data-ttu-id="3bbb9-171">可使用**清除保留**选项从所选保留代码释放订单。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-171">Use the **Clear holds** option to release an order from the selected hold code.</span></span>

<span data-ttu-id="3bbb9-172">呼叫中心订单需要付款。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-172">Call center orders require payment.</span></span> <span data-ttu-id="3bbb9-173">因此，如果尚未为订单应用付款，则不能完全清除保留。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-173">Therefore, a hold can't be fully cleared if payment hasn't been applied to the order.</span></span> <span data-ttu-id="3bbb9-174">在**呼叫中心参数**页中的**保留** 选项卡上，确保**在取消保留时提交**参数已开启。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-174">On the **Call center parameters** page, on the **Holds** tab, make sure that the **Submit when cleared** parameter is turned on.</span></span> <span data-ttu-id="3bbb9-175">此设置有助于保证为已清除保留的订单应用正确的订单提交逻辑以验证和授权付款。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-175">This setting helps guarantee that a cleared hold order goes through the correct order submission logic to validate and authorize payments.</span></span> <span data-ttu-id="3bbb9-176">如果缺少付款，用户将收到错误，并且将不清除保留代码。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-176">If payments are missing, the user receives an error, and the hold code isn't cleared.</span></span>

<span data-ttu-id="3bbb9-177">如果尚未设置**在取消保留时提交**参数，用户应选择**清除保留**菜单中的**清除并提交**选项帮助保证对订单执行所有必需的付款验证。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-177">If the **Submit when cleared** parameter hasn't been set, users should select the **Clear and submit** option on the **Clear hold** menu to help guarantee that the order goes through all the required payment validations.</span></span> <span data-ttu-id="3bbb9-178">如果在呼叫中心渠道内已开启了**启用订单完成**标志的情况下提交订单失败，将解除该订单的保留状态，但是不取消**不处理**标志。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-178">If order submission fails when the **Enable order completion** flag is turned on in the call center channel, the order is released from its hold status, but the **Do not process** flag remains set.</span></span> <span data-ttu-id="3bbb9-179">因此，已应用并验证正确付款之前，不会将该订单下达给仓库。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-179">Therefore, the order isn't released to the warehouse until correct payments have been applied and validated.</span></span>

<span data-ttu-id="3bbb9-180">如果用户希望在解除保留已执行进一步的处理之前清除保留，但是对订单进行更多更改，则可选择**清除并修改**选项。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-180">If users want to clear a hold but make additional changes to the order before it's released for further processing, they can select the **Clear and modify** option.</span></span> <span data-ttu-id="3bbb9-181">此选项将删除保留代码并打开销售订单详细信息，以便用户对订单进行更多更改。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-181">This option removes the hold code and opens the sales order details so that users can make additional changes to the order.</span></span> <span data-ttu-id="3bbb9-182">在呼叫中心渠道内开启了**启用订单完成**时，用户也可以通过付款验证逻辑应用付款和条销售订单。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-182">Users can also apply payment and submit the sales order through payment validation logic when the **Enable order completion** flag is turned on in the call center channel.</span></span>

## <a name="reporting-options"></a><span data-ttu-id="3bbb9-183">报告选项</span><span class="sxs-lookup"><span data-stu-id="3bbb9-183">Reporting options</span></span>

<span data-ttu-id="3bbb9-184">转至 **Retail 和 Commerce** \> **查询和报告** \> **呼叫中心报告** \> **订单保留报告**,以按日期范围、保留代码或其他相关条件运行有关订单保留的报告。</span><span class="sxs-lookup"><span data-stu-id="3bbb9-184">Go to **Retail and Commerce** \> **Inquiries and reports** \> **Call center reports** \> **Order holds report** to run a report about order holds by date range, hold code, or other related criteria.</span></span>