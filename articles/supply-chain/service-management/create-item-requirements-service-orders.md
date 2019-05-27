---
title: 为服务订单创建物料需求
description: 如果您需要对服务订单预留特定物料，可以创建它的库存物料需求。
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a5a730ae945af15c7bd4020c734bac971d8186e2
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1553407"
---
# <a name="create-item-requirements-for-service-orders"></a><span data-ttu-id="5154c-103">为服务订单创建物料需求</span><span class="sxs-lookup"><span data-stu-id="5154c-103">Create item requirements for service orders</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="5154c-104">您可以创建服务订单跟踪和管理为您的客户提供的服务。</span><span class="sxs-lookup"><span data-stu-id="5154c-104">You can create a service order to track and manage services that you provide to your customers.</span></span> <span data-ttu-id="5154c-105">如果您需要对服务订单预留特定物料，可以创建它的库存物料需求。</span><span class="sxs-lookup"><span data-stu-id="5154c-105">If you need to reserve specific items for a service order, you can create inventory item requirements for it.</span></span> <span data-ttu-id="5154c-106">物料需求可以从库存立即消耗，或可以启动生产订单的物料。</span><span class="sxs-lookup"><span data-stu-id="5154c-106">An item requirement can be immediately consumed from inventory, or it can initiate a production order for the item.</span></span>

<span data-ttu-id="5154c-107">通过使用物料需求来代替物料交易记录，您可以计划刚好在实际使用物料之前交货，创建采购订单，在贸易协议框架中包括物料，以及在生产计划中包括物料需求。</span><span class="sxs-lookup"><span data-stu-id="5154c-107">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span>

<span data-ttu-id="5154c-108">服务订单创建物料需求通过项目进行处理。</span><span class="sxs-lookup"><span data-stu-id="5154c-108">Item requirements for service orders are processed through a project.</span></span> <span data-ttu-id="5154c-109">若要创建服务单物料需求，必须将服务订单附加到项目中去。</span><span class="sxs-lookup"><span data-stu-id="5154c-109">To create an item requirement on a service order, the service order must be assigned to a project.</span></span> <span data-ttu-id="5154c-110">您为服务订单创建物料需求后，可以在**项目**窗体中查看所选项目的物料需求。</span><span class="sxs-lookup"><span data-stu-id="5154c-110">After you create an item requirement for a service order, you can view the item requirement in the **Projects** form for the selected project.</span></span>

## <a name="create-an-item-requirement-for-a-service-order"></a><span data-ttu-id="5154c-111">为服务订单创建物料需求</span><span class="sxs-lookup"><span data-stu-id="5154c-111">Create an item requirement for a service order</span></span>

1.  <span data-ttu-id="5154c-112">单击**服务管理** \> **通用** \> **服务订单** \> **服务订单**。</span><span class="sxs-lookup"><span data-stu-id="5154c-112">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="5154c-113">选择需要创建物料需求的服务订单。</span><span class="sxs-lookup"><span data-stu-id="5154c-113">Select the service order that you want to create an item requirement for.</span></span>

3.  <span data-ttu-id="5154c-114">在**操作窗格**中的**发货**选项卡上单击**物料需求**。</span><span class="sxs-lookup"><span data-stu-id="5154c-114">On the **Action Pane**, on the **Dispatch** tab, click **Item requirement**.</span></span>

4.  <span data-ttu-id="5154c-115">在**物料需求**窗体中输入所需物料的信息。</span><span class="sxs-lookup"><span data-stu-id="5154c-115">In the **Item requirements** form, enter information for the required item.</span></span> <span data-ttu-id="5154c-116">有关特定字段的更多信息，请参阅[物料需求（窗体）](https://technet.microsoft.com/en-us/library/aa552021\(v=ax.60\))。</span><span class="sxs-lookup"><span data-stu-id="5154c-116">For more information about the specific fields, see [Item requirements (form)](https://technet.microsoft.com/en-us/library/aa552021\(v=ax.60\)).</span></span>

## <a name="create-an-item-requirement-for-a-service-agreement"></a><span data-ttu-id="5154c-117">为服务协议创建物料需求</span><span class="sxs-lookup"><span data-stu-id="5154c-117">Create an item requirement for a service agreement</span></span>

1.  <span data-ttu-id="5154c-118">单击**服务管理** \> **常用** \> **服务协议** \> **服务协议**。</span><span class="sxs-lookup"><span data-stu-id="5154c-118">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="5154c-119">打开需要创建物料需求的服务协议。</span><span class="sxs-lookup"><span data-stu-id="5154c-119">Open the service agreement for which you want to create an item requirement.</span></span>

3.  <span data-ttu-id="5154c-120">在**行**快速选项卡上，单击**添加**创建新行。</span><span class="sxs-lookup"><span data-stu-id="5154c-120">On the **Lines** FastTab, click **Add** to create a new line.</span></span>

4.  <span data-ttu-id="5154c-121">在**交易记录类型**字段中选择**物料**。</span><span class="sxs-lookup"><span data-stu-id="5154c-121">In the **Transaction type** field, select **Item**.</span></span>

5.  <span data-ttu-id="5154c-122">在**物料设置**字段中，选择**物料需求**。</span><span class="sxs-lookup"><span data-stu-id="5154c-122">In the **Item setup** field, select **Item requirement**.</span></span>

6.  <span data-ttu-id="5154c-123">在**物料编号**字段中，选择该服务协议所需的物料。</span><span class="sxs-lookup"><span data-stu-id="5154c-123">In the **Item number** field, select the item that is required for the service agreement.</span></span>

7.  <span data-ttu-id="5154c-124">在**行明细**快速选项卡上**产品维度**选项卡中的**站点**字段内，为物料选择库存站点。</span><span class="sxs-lookup"><span data-stu-id="5154c-124">On the **Line details** FastTab, on the **Product dimensions** tab, in the **Site** field, select the inventory site for the item.</span></span>

8.  <span data-ttu-id="5154c-125">若要从协议行中创建服务订单，请在**行**快速选项卡中单击**创建服务订单**，然后将相关信息输入到**创建服务订单**窗体中。</span><span class="sxs-lookup"><span data-stu-id="5154c-125">To create a service order from the agreement line, on the **Lines** FastTab, click **Create service orders**, and then enter the relevant information in the **Create service orders** form.</span></span> 


## <a name="see-also"></a><span data-ttu-id="5154c-126">请参阅</span><span class="sxs-lookup"><span data-stu-id="5154c-126">See also</span></span>

<span data-ttu-id="5154c-127">[自动创建服务订单](create-service-orders-automatically.md)。</span><span class="sxs-lookup"><span data-stu-id="5154c-127">[Create service orders automatically](create-service-orders-automatically.md).</span></span>

  


