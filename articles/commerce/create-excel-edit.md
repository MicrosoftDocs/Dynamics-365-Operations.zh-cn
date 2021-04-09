---
title: 创建 Excel 工作簿以编辑零售交易记录
description: 本主题介绍如何创建 Excel 工作簿，以便您可以在 Microsoft Dynamics 365 Commerce 中编辑零售交易记录。
author: josaw1
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: a2d41dd0470a4abae1a8238be8f1549fb094a026
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795731"
---
# <a name="create-an-excel-workbook-to-edit-retail-transactions"></a><span data-ttu-id="c2a43-103">创建 Excel 工作簿以编辑零售交易记录</span><span class="sxs-lookup"><span data-stu-id="c2a43-103">Create an Excel workbook to edit retail transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c2a43-104">本主题介绍如何创建 Excel 工作簿，以便您可以在 Microsoft Dynamics 365 Commerce 中编辑零售交易记录。</span><span class="sxs-lookup"><span data-stu-id="c2a43-104">This topic describes how to create an Excel workbook so that you can edit retail transactions in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c2a43-105">概览</span><span class="sxs-lookup"><span data-stu-id="c2a43-105">Overview</span></span>

<span data-ttu-id="c2a43-106">提供了一个预定义的 Excel 模板，客户可以从系统的不同部分访问该模板，以及将其用于编辑和审计零售交易记录。</span><span class="sxs-lookup"><span data-stu-id="c2a43-106">There is a predefined Excel template that customers can access from different parts of the system and use to edit and audit retail transactions.</span></span> <span data-ttu-id="c2a43-107">但是，客户也可以针对此目的创建一个自定义的 Excel 工作簿。</span><span class="sxs-lookup"><span data-stu-id="c2a43-107">However, customers can also create a custom Excel workbook for this purpose.</span></span>

## <a name="create-and-configure-an-excel-workbook"></a><span data-ttu-id="c2a43-108">创建和配置 Excel 工作簿</span><span class="sxs-lookup"><span data-stu-id="c2a43-108">Create and configure an Excel workbook</span></span>

<span data-ttu-id="c2a43-109">要创建和配置 Excel 工作簿，以便您可以编辑零售交易记录，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="c2a43-109">To create and configure an Excel workbook so that you can edit retail transactions, follow these steps.</span></span>

1. <span data-ttu-id="c2a43-110">打开 Excel，并创建一个空白工作簿。</span><span class="sxs-lookup"><span data-stu-id="c2a43-110">Open Excel, and create a blank workbook.</span></span>
1. <span data-ttu-id="c2a43-111">在 **插入** 选项卡上，选择 **我的加载项**。</span><span class="sxs-lookup"><span data-stu-id="c2a43-111">On the **Insert** tab, select **My add-ins**.</span></span>
1. <span data-ttu-id="c2a43-112">在右侧窗格中，选择 **添加服务器信息** 链接。</span><span class="sxs-lookup"><span data-stu-id="c2a43-112">In the right pane, select the **Add server information** link.</span></span>
1. <span data-ttu-id="c2a43-113">输入服务器 URL，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="c2a43-113">Enter the server URL, and then select **OK**.</span></span>
1. <span data-ttu-id="c2a43-114">如果收到“找不到小程序注册”错误消息，请按照以下步骤操作来解决问题：</span><span class="sxs-lookup"><span data-stu-id="c2a43-114">If you receive a "No applet registrations found" error message, follow these steps to resolve the issue:</span></span>

    1. <span data-ttu-id="c2a43-115">在 Commerce 中，转到 **系统管理 \> 设置 \> Office 应用参数**。</span><span class="sxs-lookup"><span data-stu-id="c2a43-115">In Commerce, go to **System administration \> Setup \> Office app parameters**.</span></span>
    1. <span data-ttu-id="c2a43-116">在 **应用参数** 快速选项卡上，选择 **初始化应用参数**。</span><span class="sxs-lookup"><span data-stu-id="c2a43-116">On the **App parameters** FastTab, select **Initialize app parameters**.</span></span>
    1. <span data-ttu-id="c2a43-117">在确认消息框中，选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="c2a43-117">In the confirmation message box, select **OK**.</span></span>
    1. <span data-ttu-id="c2a43-118">在 **已注册的小程序** 快速选项卡上，选择 **初始化小程序注册**。</span><span class="sxs-lookup"><span data-stu-id="c2a43-118">On the **Registered applets** FastTab, select **Initialize applet registration**.</span></span>
    1. <span data-ttu-id="c2a43-119">根据需要，重复前面的三个步骤。</span><span class="sxs-lookup"><span data-stu-id="c2a43-119">Repeat the previous three steps as required.</span></span>

1. <span data-ttu-id="c2a43-120">选择 **设计**，然后选择 **添加表**。</span><span class="sxs-lookup"><span data-stu-id="c2a43-120">Select **Design**, and then select **Add table**.</span></span>
1. <span data-ttu-id="c2a43-121">根据必须修改的数据，选择必须添加到 Excel 工作簿中以进行编辑的实体。</span><span class="sxs-lookup"><span data-stu-id="c2a43-121">Based on the data that has to be modified, select the entities that must be added to the Excel workbook for editing.</span></span> <span data-ttu-id="c2a43-122">使用下表作为参考。</span><span class="sxs-lookup"><span data-stu-id="c2a43-122">Use the following table as a reference.</span></span>

    | <span data-ttu-id="c2a43-123">交易记录类型</span><span class="sxs-lookup"><span data-stu-id="c2a43-123">Transaction type</span></span> | <span data-ttu-id="c2a43-124">要使用的数据实体</span><span class="sxs-lookup"><span data-stu-id="c2a43-124">Data entities to use</span></span> |
    |------------------|----------------------|
    | <span data-ttu-id="c2a43-125">现金和结转交易、在线订单、异步客户订单、异步客户报价</span><span class="sxs-lookup"><span data-stu-id="c2a43-125">Cash and carry transactions, Online orders, Async customer orders, Async customer quotes</span></span> | <span data-ttu-id="c2a43-126">交易记录（可审计）、销售交易记录（可审计）、付款交易记录（可审计）、纳税交易记录（可审计）、折扣交易记录（可审计）、费用交易记录（可审计）</span><span class="sxs-lookup"><span data-stu-id="c2a43-126">Transaction (auditable), Sales transaction (auditable), Payment transactions (auditable), Tax transactions (auditable), Discount transactions (auditable), Charge transactions (auditable)</span></span> |
    | <span data-ttu-id="c2a43-127">银行投箱</span><span class="sxs-lookup"><span data-stu-id="c2a43-127">Bank drop</span></span> | <span data-ttu-id="c2a43-128">交易记录（可审计）、银行支付交易记录（可审计）</span><span class="sxs-lookup"><span data-stu-id="c2a43-128">Transaction (auditable), Banked tender transactions (auditable)</span></span> |
    | <span data-ttu-id="c2a43-129">金库投箱</span><span class="sxs-lookup"><span data-stu-id="c2a43-129">Safe drop</span></span> | <span data-ttu-id="c2a43-130">交易记录（可审计）、金库支付交易记录（可审计）</span><span class="sxs-lookup"><span data-stu-id="c2a43-130">Transaction (auditable), Safe tender transactions (auditable)</span></span> |
    | <span data-ttu-id="c2a43-131">钱币清点</span><span class="sxs-lookup"><span data-stu-id="c2a43-131">Tender declaration</span></span> | <span data-ttu-id="c2a43-132">交易记录（可审计）、钱币清点交易记录（可审计）</span><span class="sxs-lookup"><span data-stu-id="c2a43-132">Transaction (auditable), Tender declaration transactions (auditable)</span></span> |
    | <span data-ttu-id="c2a43-133">收入、支出</span><span class="sxs-lookup"><span data-stu-id="c2a43-133">Income, Expense</span></span> | <span data-ttu-id="c2a43-134">交易记录（可审计）、收入/支出交易记录（可审计）、付款交易记录（可审计）</span><span class="sxs-lookup"><span data-stu-id="c2a43-134">Transaction (auditable), Income/Expense transactions (auditable), Payment transactions (auditable)</span></span> |
    | <span data-ttu-id="c2a43-135">清点起始金额、支付方式删除、浮动条目、找零支付方式、账单付款、客户存款</span><span class="sxs-lookup"><span data-stu-id="c2a43-135">Declare starting amount, Tender removal, Float entry, Change tender, Invoice payment, Customer deposit</span></span> | <span data-ttu-id="c2a43-136">交易记录（可审计）、付款交易记录（可审计）</span><span class="sxs-lookup"><span data-stu-id="c2a43-136">Transaction (auditable), Payment transactions (auditable)</span></span> |

    > [!NOTE]
    > <span data-ttu-id="c2a43-137">务必注意，只能向每个 Excel 工作簿添加一个数据实体。</span><span class="sxs-lookup"><span data-stu-id="c2a43-137">It's important that you add only one data entity to each Excel workbook.</span></span> <span data-ttu-id="c2a43-138">此外，必须将钥匙符号标记的所有字段都添加到相关工作簿中。</span><span class="sxs-lookup"><span data-stu-id="c2a43-138">Additionally, all fields that are marked by a key symbol must be added to the relevant workbook.</span></span>

1. <span data-ttu-id="c2a43-139">配置工作簿后，应用所需的筛选器。</span><span class="sxs-lookup"><span data-stu-id="c2a43-139">After the workbook is configured, apply the required filters.</span></span> <span data-ttu-id="c2a43-140">请确保对文件中的所有工作表应用相同的筛选器。</span><span class="sxs-lookup"><span data-stu-id="c2a43-140">Be sure to apply the same filters to all the worksheets in the file.</span></span> <span data-ttu-id="c2a43-141">避免将大量数据加载到 Excel 文件中。</span><span class="sxs-lookup"><span data-stu-id="c2a43-141">Avoid loading very large amounts of data into the Excel file.</span></span> <span data-ttu-id="c2a43-142">否则，可能会影响性能，并且 Excel 和您的系统运行速度可能会变慢。</span><span class="sxs-lookup"><span data-stu-id="c2a43-142">Otherwise, performance might be affected, and Excel and your system might slow down.</span></span> <span data-ttu-id="c2a43-143">我们建议您始终使用“公司”和“报表编号”或“交易记录编号”作为文件的筛选器。</span><span class="sxs-lookup"><span data-stu-id="c2a43-143">We recommend that you always use "Company" and either "Statement Number" or "Transaction Number" as filters for your file.</span></span>
1. <span data-ttu-id="c2a43-144">配置筛选器后，选择 **刷新** 以加载数据。</span><span class="sxs-lookup"><span data-stu-id="c2a43-144">After the filters are configured, select **Refresh** to load the data.</span></span>
1. <span data-ttu-id="c2a43-145">编辑所需的数据，然后将其发布。</span><span class="sxs-lookup"><span data-stu-id="c2a43-145">Edit the required data, and then publish it.</span></span> <span data-ttu-id="c2a43-146">如果 **发布** 按钮不可用，原因可能是某些关键字段未添加到 Excel 工作簿中。</span><span class="sxs-lookup"><span data-stu-id="c2a43-146">If the **Publish** button is unavailable, some key fields probably weren't added to the Excel workbook.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c2a43-147">其他资源</span><span class="sxs-lookup"><span data-stu-id="c2a43-147">Additional resources</span></span>

[<span data-ttu-id="c2a43-148">编辑并审计现金和结转及现金管理交易记录</span><span class="sxs-lookup"><span data-stu-id="c2a43-148">Edit and audit cash and carry and cash management transactions</span></span>](edit-cash-trans.md)

[<span data-ttu-id="c2a43-149">编辑并审计在线订单和异步客户订单交易记录</span><span class="sxs-lookup"><span data-stu-id="c2a43-149">Edit and audit online order and asynchronous customer order transactions</span></span>](edit-order-trans.md)

[<span data-ttu-id="c2a43-150">编辑零售交易记录的财务维度</span><span class="sxs-lookup"><span data-stu-id="c2a43-150">Edit financial dimensions for retail transactions</span></span>](edit-financial-dim.md)

[<span data-ttu-id="c2a43-151">将字段添加到 Excel 工作簿以编辑零售交易记录</span><span class="sxs-lookup"><span data-stu-id="c2a43-151">Add fields to an Excel workbook to edit retail transactions</span></span>](add-fields-excel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]