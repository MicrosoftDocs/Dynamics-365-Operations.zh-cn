---
title: 根据维护请求创建工作订单
description: 本主题说明如何在资产管理中根据维护请求创建工作订单。
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b6bd98796140ab7aa3e7813ff1526413504554c5
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205199"
---
# <a name="create-work-orders-from-maintenance-requests"></a><span data-ttu-id="c4dbc-103">根据维护请求创建工作订单</span><span class="sxs-lookup"><span data-stu-id="c4dbc-103">Create work orders from maintenance requests</span></span>

[!include [banner](../../includes/banner.md)]

 


<span data-ttu-id="c4dbc-104">创建了维护请求之后，可将其轻松转化为工作订单。</span><span class="sxs-lookup"><span data-stu-id="c4dbc-104">After you've created maintenance requests, you can easily convert them to work orders.</span></span> <span data-ttu-id="c4dbc-105">本主题介绍处理维护请求，同时更新多个维护请求，然后同时为多个维护请求创建一个工作订单的最快方法。</span><span class="sxs-lookup"><span data-stu-id="c4dbc-105">This topic describes the quickest way to work with maintenance requests, update several maintenance requests at the same time, and then create a work order for several maintenance requests at the same time.</span></span> <span data-ttu-id="c4dbc-106">在**有效维护请求**或**我的功能位置维护请求**页，也可以一次处理一个维护请求，并将一个维护请求转化为工作订单。</span><span class="sxs-lookup"><span data-stu-id="c4dbc-106">On the **Active maintenance requests** or **My functional location maintenance requests** page, you can also work with one maintenance request at a time and convert one maintenance request to a work order.</span></span>

> [!NOTE]
> <span data-ttu-id="c4dbc-107">每个维护请求只能与一个工作订单关联。</span><span class="sxs-lookup"><span data-stu-id="c4dbc-107">Every maintenance request can be related to only one work order.</span></span> <span data-ttu-id="c4dbc-108">但是，一个工作订单中可以包含多个维护请求，即使这些维护请求具有不同资产也不例外。</span><span class="sxs-lookup"><span data-stu-id="c4dbc-108">However, multiple maintenance requests can be included in one work order, even if the maintenance requests have different assets.</span></span>

1. <span data-ttu-id="c4dbc-109">选择**资产管理** \> **常用** \> **维护请求** \> **所有维护请求**。</span><span class="sxs-lookup"><span data-stu-id="c4dbc-109">Select **Asset management** \> **Common** \> **maintenance requests** \> **All maintenance requests**.</span></span>
2. <span data-ttu-id="c4dbc-110">必须为维护请求先至少选择一个维护作业类型，并且还选择维护作业类型变体和交易（如果此信息相关），才能基于维护请求创建工作订单。</span><span class="sxs-lookup"><span data-stu-id="c4dbc-110">Before you can create a work order from maintenance requests, you must select, at a minimum, a maintenance job type for the maintenance requests, and also a maintenance job type variant and trade, if this information is relevant.</span></span> <span data-ttu-id="c4dbc-111">在网格视图中，可以轻松更新维护请求的信息。</span><span class="sxs-lookup"><span data-stu-id="c4dbc-111">In the grid view, you can easily update information for a maintenance request.</span></span>
3. <span data-ttu-id="c4dbc-112">准备好创建工作订单时，选择要在其中包含的维护请求。</span><span class="sxs-lookup"><span data-stu-id="c4dbc-112">When you're ready to create a work order, select the maintenance requests to include in it.</span></span>

    - <span data-ttu-id="c4dbc-113">如果选择多个要转化为工作订单的维护请求，则必须先设置**资产**字段和**维护作业类型**字段，才能创建工作订单。</span><span class="sxs-lookup"><span data-stu-id="c4dbc-113">If you select several maintenance requests to convert to a work order, both the **Asset** field and the **Maintenance job type** field must be set before you create the work order.</span></span>
    - <span data-ttu-id="c4dbc-114">如果选择一个要转化为工作订单的维护请求，则必须先仅设置**资产**字段，才能创建工作订单。</span><span class="sxs-lookup"><span data-stu-id="c4dbc-114">If you select one maintenance request to convert to a work order, only the **Asset** field must be set before you create the work order.</span></span> <span data-ttu-id="c4dbc-115">但是，创建工作订单时，可以在**创建工作订单**对话框中选择维护作业类型（如果此信息相关，则还需要选择关联的维护作业类型变体和交易）。</span><span class="sxs-lookup"><span data-stu-id="c4dbc-115">However, when you create the work order, you can select a maintenance job type (and a related maintenance job type variant and trade, if this information is relevant) in the **Create work order** dialog box.</span></span>

4. <span data-ttu-id="c4dbc-116">选择**工作订单**。</span><span class="sxs-lookup"><span data-stu-id="c4dbc-116">Select **Work order**.</span></span>
5. <span data-ttu-id="c4dbc-117">在**创建工作订单**对话框中，设置字段，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="c4dbc-117">In the **Create work order** dialog box, set the fields, and then select **OK**.</span></span>

    <span data-ttu-id="c4dbc-118">可能会通过消息栏通知您已创建了新工作订单。</span><span class="sxs-lookup"><span data-stu-id="c4dbc-118">A message bar might notify you that a new work order has been created.</span></span>

    <span data-ttu-id="c4dbc-119">此外，创建基于维护请求的工作订单时，如果一个保修协议中涵盖与该维护请求关联的资产，则会通过消息栏告知您这个保修协议。</span><span class="sxs-lookup"><span data-stu-id="c4dbc-119">Additionally, when you create a work order that is based on a maintenance request, if the asset that is related to the maintenance request is included in a warranty agreement, a message bar notifies you about the warranty agreement.</span></span>

6. <span data-ttu-id="c4dbc-120">选择**资产管理** \> **常用** \> **工作订单** \> **所有工作订单**，然后打开新工作订单。</span><span class="sxs-lookup"><span data-stu-id="c4dbc-120">Select **Asset management** \> **Common** \> **Work orders** \> **All work orders**, and open the new work order.</span></span>

    ![打开新工作订单](media/05-manage-maintenance-requests.png)

