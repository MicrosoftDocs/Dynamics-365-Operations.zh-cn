---
title: 工作订单和固定资产
description: 本主题介绍资产管理中的工作订单和固定资产。
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 65adcd07f1649b2e4eb2e2528507bb15631782ce
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5816716"
---
# <a name="work-orders-and-fixed-assets"></a><span data-ttu-id="c1836-103">工作订单和固定资产</span><span class="sxs-lookup"><span data-stu-id="c1836-103">Work orders and fixed assets</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="c1836-104">在资产管理中，可将资产与固定资产关联，还可以为这些资产创建工作订单。</span><span class="sxs-lookup"><span data-stu-id="c1836-104">In Asset Management, assets can be related to fixed assets, and you can create work orders for those assets.</span></span> <span data-ttu-id="c1836-105">如果使用此功能，则可在 Microsoft Dynamics 365 for Finance and Operations 的 **项目管理与核算** 和 **固定资产** 模块中获取在投资项目中登记的固定资产、关联的投资项目和成本的完整概览。</span><span class="sxs-lookup"><span data-stu-id="c1836-105">If you use this functionality, you can get a complete overview of fixed assets, related investment projects, and the costs that are registered on the investment projects in the **Project management and accounting** and **Fixed assets** modules in Microsoft Dynamics 365 for Finance and Operations.</span></span>

>[!NOTE]
><span data-ttu-id="c1836-106">仅当选择 **投资** 作为工作订单作业项目的项目类型时，才会设置工作订单作业项目的 **固定资产编号** 字段。</span><span class="sxs-lookup"><span data-stu-id="c1836-106">The **Fixed asset number** field on the work order job project is set only if **Investment** is selected as the project type on the work order job project.</span></span>

<span data-ttu-id="c1836-107">下图显示 **项目管理与核算** 模块中的投资项目与工作订单作业项目之间的关系。</span><span class="sxs-lookup"><span data-stu-id="c1836-107">The illustration below shows the relation between an investment project in the **Project management and accounting** module and a work order job project.</span></span>

![图 1](media/24-work-orders.png)

<span data-ttu-id="c1836-109">以下过程介绍资产、工作订单、工作订单作业项目和固定资产之间的关系。</span><span class="sxs-lookup"><span data-stu-id="c1836-109">The following procedure describes the relation between assets, work orders, work order job projects, and fixed assets.</span></span>

1. <span data-ttu-id="c1836-110">您将创建与固定资产相关的资产。</span><span class="sxs-lookup"><span data-stu-id="c1836-110">You create an asset that you relate to a fixed asset.</span></span>

![图 2](media/25-work-orders.png)

2. <span data-ttu-id="c1836-112">在 **工作订单类型** 页面设置工作订单类型（**资产管理** > **设置** > **工作订单** > **工作订单类型**）时，将创建工作订单类型来处理投资。</span><span class="sxs-lookup"><span data-stu-id="c1836-112">When you set up work order types on the **Work order types** page (**Asset management** > **Setup** > **Work orders** > **Work order types**), you create a work order type for handling investments.</span></span> <span data-ttu-id="c1836-113">另请参阅[工作订单类型](../setup-for-work-orders/work-order-types.md)。</span><span class="sxs-lookup"><span data-stu-id="c1836-113">See also [Work order types](../setup-for-work-orders/work-order-types.md).</span></span>

![图 3](media/26-work-orders.png)

3. <span data-ttu-id="c1836-115">在 **工作订单项目设置** 页面的 **项目组** 选项卡上设置工作订单项目组（**资产管理** > **设置** > **工作订单** > **项目设置**）时，将在 **项目管理与核算** 模块中 **项目组** 页面上在用于投资的工作订单类型与为投资创建的项目组之间创建关系（**项目管理与核算** > **设置** > **过帐** > **项目组**）。</span><span class="sxs-lookup"><span data-stu-id="c1836-115">When you set up work order project groups on the **Project group** tab of the **Work order project setup** page (**Asset management** > **Setup** > **Work orders** > **Project setup**), you create a relation between the work order type that is used for investments and the project group that was created for investments on the **Project groups** page in the **Project management and accounting** module (**Project management and accounting** > **Setup** > **Posting** > **Project groups**).</span></span>

![图 4](media/27-work-orders.png)

4. <span data-ttu-id="c1836-117">创建与固定资产项目关联的工作订单时，请选择用于处理投资的工作订单类型，如 **投资**。</span><span class="sxs-lookup"><span data-stu-id="c1836-117">When you create a work order that is related to a fixed asset, you select the work order type that is used to handle investments, such as **Investment**.</span></span>

5. <span data-ttu-id="c1836-118">创建工作订单之后，将在 **所有工作订单** 页面显示关联的工作订单类型。</span><span class="sxs-lookup"><span data-stu-id="c1836-118">When the work order is created, the related work order type is shown on the **All work orders** page.</span></span>

![图 5](media/28-work-orders.png)

6. <span data-ttu-id="c1836-120">创建工作订单后，将在 **项目管理与核算** 模块中的 **所有项目** 页面创建与工作订单关联的项目（**项目管理与核算** > **项目** > **所有项目**）。</span><span class="sxs-lookup"><span data-stu-id="c1836-120">When the work order is created, the project that is related to the work order is created on the **All projects** page in the **Project management and accounting** module (**Project management and accounting** > **Projects** > **All projects**).</span></span> <span data-ttu-id="c1836-121">要查看与项目相关的信息，请在 **资产管理** 模块中 **所有工作订单** 页面的详细信息视图中，在 **行明细** 快速选项卡上的 **常规** 选项卡上，在 **项目 ID** 字段中选择链接（**资产管理** > **公用** > **工作订单** > **所有工作订单**）。</span><span class="sxs-lookup"><span data-stu-id="c1836-121">To view project-related information, select the link in the **Project ID** field on the **General** tab on the **Line details** FastTab in the details view of the **All work orders** page in the **Asset management** module (**Asset management** > **Commom** > **Work orders** > **All work orders**).</span></span>

![图 6](media/29-work-orders.png)

7. <span data-ttu-id="c1836-123">要查看与固定资产关联的项目的概览，请选择 **固定资产** > **固定资产** > **固定资产**，然后在 **固定资产编号** 字段中，选择固定资产的链接打开详细信息视图。</span><span class="sxs-lookup"><span data-stu-id="c1836-123">To see an overview of the projects associated with a fixed asset, select **Fixed assets** > **Fixed assets** > **Fixed assets**, and then, in the **Fixed asset number** field, select the link for the fixed asset to open the details view.</span></span> <span data-ttu-id="c1836-124">展开页面右侧的 **相关信息** 窗格，然后选择 **关联项目** 快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="c1836-124">Expand the **Related information** pane on the right side of the page, and select the **Associated projects** FastTab.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]