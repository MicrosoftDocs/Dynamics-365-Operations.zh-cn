---
title: 将地址添加到服务订单
description: 此主题描述如何将客户地址添加到服务订单。
author: ShylaThompson
manager: tfehr
ms.date: 05/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 41497eacae8bcc0e57df8062f7f318a39c2b4909
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/10/2020
ms.locfileid: "3978765"
---
# <a name="add-an-address-to-a-service-order"></a><span data-ttu-id="f5fb4-103">将地址添加到服务订单</span><span class="sxs-lookup"><span data-stu-id="f5fb4-103">Add an address to a service order</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="f5fb4-104">此主题描述如何将客户地址添加到服务订单。</span><span class="sxs-lookup"><span data-stu-id="f5fb4-104">This topic describes how to add a customer address to a service order.</span></span> <span data-ttu-id="f5fb4-105">在您创建某一服务订单时，地址信息将从该服务订单附加到的项目转移。</span><span class="sxs-lookup"><span data-stu-id="f5fb4-105">When you create a service order, the address information is transferred from the project that the service order is attached to.</span></span> <span data-ttu-id="f5fb4-106">但是，您可以从已在 Microsoft Dynamics AX 中输入的客户、供应商、站点、仓库、服务订单和项目的地址，选择备选位置。</span><span class="sxs-lookup"><span data-stu-id="f5fb4-106">However, you can select an alternative location from addresses that are already entered in Microsoft Dynamics AX for customers, vendors, sites, warehouses, service orders, and projects.</span></span>

<span data-ttu-id="f5fb4-107">您还可以创建新地址。</span><span class="sxs-lookup"><span data-stu-id="f5fb4-107">You can also create a new address.</span></span> <span data-ttu-id="f5fb4-108">默认情况下，将新地址转移到项目。</span><span class="sxs-lookup"><span data-stu-id="f5fb4-108">By default, the new address is transferred to the project.</span></span> <span data-ttu-id="f5fb4-109">但是，您可以指定新地址仅与该服务实例相关。</span><span class="sxs-lookup"><span data-stu-id="f5fb4-109">However, you can specify that the new address is only relevant for this instance of the service.</span></span> <span data-ttu-id="f5fb4-110">如果您执行此操作，则新地址不会转移到项目。</span><span class="sxs-lookup"><span data-stu-id="f5fb4-110">If you do, the new address is not transferred to the project.</span></span>

## <a name="create-a-customer-address-for-a-service-order"></a><span data-ttu-id="f5fb4-111">为服务订单创建客户地址</span><span class="sxs-lookup"><span data-stu-id="f5fb4-111">Create a customer address for a service order</span></span>

<span data-ttu-id="f5fb4-112">若要添加地址到销售订单，请执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="f5fb4-112">To add an address to a service order, follow these steps:</span></span>

1.  <span data-ttu-id="f5fb4-113">单击**服务管理** \> **通用** \> **服务订单** \> **服务订单**。</span><span class="sxs-lookup"><span data-stu-id="f5fb4-113">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="f5fb4-114">打开想要为其创建地址的服务订单。</span><span class="sxs-lookup"><span data-stu-id="f5fb4-114">Open the service order that you want to create an address for.</span></span>

3.  <span data-ttu-id="f5fb4-115">在**操作窗格**上，单击**编辑**，然后单击**标头视图**。</span><span class="sxs-lookup"><span data-stu-id="f5fb4-115">On the **Action Pane**, click **Edit**, and then click **Header view**.</span></span>

4.  <span data-ttu-id="f5fb4-116">在**地址**快速选项卡，单击**添加地址**。</span><span class="sxs-lookup"><span data-stu-id="f5fb4-116">On the **Address** FastTab, click **Add address**.</span></span>

5.  <span data-ttu-id="f5fb4-117">在**新地址**窗体中，输入地址的唯一名称并完成其余的字段。</span><span class="sxs-lookup"><span data-stu-id="f5fb4-117">In the **New address** form, enter a unique name for the address and complete the remaining fields.</span></span> 
    

    > [!WARNING]
    > <P><span data-ttu-id="f5fb4-118">如果输入与现有地址相同的名称，则您在剩余字段中输入的信息将覆盖现有地址信息。</span><span class="sxs-lookup"><span data-stu-id="f5fb4-118">If you enter the same name as an existing address, the information that you enter in the remaining fields will overwrite information for the existing address.</span></span></P>


6.  <span data-ttu-id="f5fb4-119">单击 **确定**以将新地址复制到您的服务订单中。</span><span class="sxs-lookup"><span data-stu-id="f5fb4-119">Click **OK** to copy the new address to your service order.</span></span>

## <a name="specify-an-alternative-address-on-a-service-order"></a><span data-ttu-id="f5fb4-120">在服务订单上指定备选地址</span><span class="sxs-lookup"><span data-stu-id="f5fb4-120">Specify an alternative address on a service order</span></span>

<span data-ttu-id="f5fb4-121">若要将备选地址添加到服务订单，请执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="f5fb4-121">To add an alternative address to a service order, follow these steps:</span></span>

1.  <span data-ttu-id="f5fb4-122">单击**服务管理** \> **通用** \> **服务订单** \> **服务订单**。</span><span class="sxs-lookup"><span data-stu-id="f5fb4-122">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="f5fb4-123">打开您想要为其输入备选地址的服务订单。</span><span class="sxs-lookup"><span data-stu-id="f5fb4-123">Open the service order that you want to enter an alternative address for.</span></span>

3.  <span data-ttu-id="f5fb4-124">在**操作窗格**上，单击**编辑**，然后单击**标头视图**。</span><span class="sxs-lookup"><span data-stu-id="f5fb4-124">On the **Action Pane**, click **Edit**, and then click **Header view**.</span></span>

4.  <span data-ttu-id="f5fb4-125">在**地址**快速选项卡，单击**其他地址**。</span><span class="sxs-lookup"><span data-stu-id="f5fb4-125">On the **Address** FastTab, click **Other address**.</span></span>

5.  <span data-ttu-id="f5fb4-126">在**地址选择**窗体**记录类型**字段中，选择**服务订单**。</span><span class="sxs-lookup"><span data-stu-id="f5fb4-126">In the **Address selection** form, in the **Record type** field, select **Service orders**.</span></span>

6.  <span data-ttu-id="f5fb4-127">选择地址，然后单击**确定**以将其复制到您的服务订单中。</span><span class="sxs-lookup"><span data-stu-id="f5fb4-127">Select an address, and then click **OK** to copy it to your service order.</span></span>


  


