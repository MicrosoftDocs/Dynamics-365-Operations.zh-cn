---
title: 工作订单和固定资产
description: 本主题介绍资产管理中的工作订单和固定资产。
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 95fe394d22f9fe81511c230a2cf7b8ddf00d896f
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250821"
---
# <a name="work-orders-and-fixed-assets"></a><span data-ttu-id="ae976-103">工作订单和固定资产</span><span class="sxs-lookup"><span data-stu-id="ae976-103">Work orders and fixed assets</span></span>


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="ae976-104">在资产管理中，可将资产与固定资产关联，还可以为这些资产创建工作订单。</span><span class="sxs-lookup"><span data-stu-id="ae976-104">In Asset Management, assets can be related to fixed assets, and you can create work orders for those assets.</span></span> <span data-ttu-id="ae976-105">如果使用此功能，则可在**项目管理与核算**模块和**固定资产**模块中获取固定资产、关联的投资项目和为投资项目登记的所有成本的完整概览。</span><span class="sxs-lookup"><span data-stu-id="ae976-105">If you use this functionality, you can get a complete overview of fixed assets, related investment projects, and the costs registered on the investment projects in the **Project management and accounting** module and the **Fixed assets** module.</span></span>

>[!NOTE]
><span data-ttu-id="ae976-106">仅当选择类型“投资”作为工作订单作业项目的项目类型时，才会填写工作订单作业项目的**固定资产编号**字段。</span><span class="sxs-lookup"><span data-stu-id="ae976-106">The **Fixed asset number** field is only filled out on the work order job project if type "Investment" is selected as the project type on the work order job project.</span></span>

![图 1](media/24-work-orders.png)

<span data-ttu-id="ae976-108">以下过程介绍资产、工作订单、工作订单作业项目和固定资产之间的关系。</span><span class="sxs-lookup"><span data-stu-id="ae976-108">The following procedure describes the relation between assets, work orders, work order job projects, and fixed assets.</span></span>

1. <span data-ttu-id="ae976-109">创建与固定资产关联的资产，如下图中所示。</span><span class="sxs-lookup"><span data-stu-id="ae976-109">You create an asset that you relate to a fixed asset, as shown in the figure below.</span></span>

![图 2](media/25-work-orders.png)

2. <span data-ttu-id="ae976-111">设置工作订单类型（**资产管理** > **设置** > **工作订单** > **工作订单类型**）时，将创建工作订单类型来处理投资。</span><span class="sxs-lookup"><span data-stu-id="ae976-111">When you set up work order types (**Asset management** > **Setup** > **Work orders** > **Work order types**), you create a work order type for handling investments.</span></span> <span data-ttu-id="ae976-112">另请参阅[工作订单类型](../setup-for-work-orders/work-order-types.md)。</span><span class="sxs-lookup"><span data-stu-id="ae976-112">See also [Work order types](../setup-for-work-orders/work-order-types.md).</span></span>

![图 3](media/26-work-orders.png)

3. <span data-ttu-id="ae976-114">设置工作订单项目组（**资产管理** > **设置** > **工作订单** > **项目设置** > **项目组**链接）时，将在**项目管理与核算**模块中创建用于投资的工作订单类型与为投资创建的项目组（**项目管理与核算** > **设置** > **过帐** > **项目组**）之间的关联。</span><span class="sxs-lookup"><span data-stu-id="ae976-114">When you set up work order project groups (**Asset management** > **Setup** > **Work orders** > **Project setup** > **Project group** link), you create a relation between the work order type used for investments and the project group created for investments in the **Project management and accounting** module (**Project management and accounting** > **Setup** > **Posting** > **Project groups**).</span></span>

![图 4](media/27-work-orders.png)

4. <span data-ttu-id="ae976-116">创建与固定资产项目关联的工作订单时，请选择用于处理投资的工作订单类型，如“投资”。</span><span class="sxs-lookup"><span data-stu-id="ae976-116">When you create a work order that relates to a fixed asset object, you select the work order type used for handling investments, for example, "Investment".</span></span>

5. <span data-ttu-id="ae976-117">创建工作订单之后，将在**所有工作订单**中显示关联的工作订单类型。</span><span class="sxs-lookup"><span data-stu-id="ae976-117">When the work order is created, the related work order type is shown in **All work orders**.</span></span>

![图 5](media/28-work-orders.png)

6. <span data-ttu-id="ae976-119">创建工作订单时，将在**项目管理与核算** > **所有项目**中创建与该工作订单关联的项目。</span><span class="sxs-lookup"><span data-stu-id="ae976-119">When the work order is created, the project related to the work order is created in **Project management and accounting** > **All projects**.</span></span> <span data-ttu-id="ae976-120">可查看与项目有关的信息，方法是单击工作订单的**项目 ID** 链接（在**资产管理**的“详细信息视图”中打开工作订单 > **行详细信息**快速选项卡 > **常规**选项卡 > **项目 ID** 字段）。</span><span class="sxs-lookup"><span data-stu-id="ae976-120">You can see project-related information by clicking the **Project ID** link on the work order (in **Asset management**, open the work order in Details view > **Line details** FastTab > **General** tab > **Project ID** field).</span></span>

![图 6](media/29-work-orders.png)

7. <span data-ttu-id="ae976-122">在**固定资产**中，可查看与固定资产关联的项目的概览（**固定资产** > **固定资产** > **固定资产** > 在**固定资产编号**字段中单击固定资产 > 查看**相关信息**窗格 > **关联的项目**部分中的内容）。</span><span class="sxs-lookup"><span data-stu-id="ae976-122">In **Fixed assets**, you are able to see an overview of the projects associated with a fixed asset (**Fixed assets** > **Fixed assets** > **Fixed assets** > click on the fixed asset in the **Fixed asset number** field > view the contents in the **Related information** pane > **Associated projects** section).</span></span>

