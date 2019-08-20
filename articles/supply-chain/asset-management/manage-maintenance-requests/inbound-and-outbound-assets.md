---
title: 入站资产和出站资产
description: 本主题介绍如何在资产管理中登记入站资产和出站资产。
author: josaw1
manager: AnnBe
ms.date: 10/01/2019
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 62998da7f541379296d5ac325ae29f24a42f9b7c
ms.sourcegitcommit: 871b76f8808a48d282f151144829323258ffc912
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/02/2019
ms.locfileid: "1847543"
---
# <a name="inbound-and-outbound-assets"></a><span data-ttu-id="60849-103">入站资产和出站资产</span><span class="sxs-lookup"><span data-stu-id="60849-103">Inbound and outbound assets</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="60849-104">如果公司对从其他位置或客户收到的资产执行维修作业或维护作业，资产管理同时可跟踪正在前往公司的入站资产和正在退回的出站资产。</span><span class="sxs-lookup"><span data-stu-id="60849-104">If your company does repair jobs or maintenance jobs on assets that are received from other locations or customers, Asset Management can track both inbound assets that are on their way to your company and outbound assets that are being returned.</span></span>

> [!NOTE]
> <span data-ttu-id="60849-105">如果要使用入站生命周期状态和出站生命周期状态管理正在前来的资产和正在退回的资产，则必须设置维护请求生命周期状态和生命周期模型来支持这些操作。</span><span class="sxs-lookup"><span data-stu-id="60849-105">If you want to use inbound and outbound lifecycle states to manage assets that are coming in and being returned, you must set up maintenance request lifecycle states and lifecycle models to support these actions.</span></span> <span data-ttu-id="60849-106">有关详细信息，请参阅[维护请求的设置](../setup-for-maintenance-requests/requests.md)。</span><span class="sxs-lookup"><span data-stu-id="60849-106">For more information, see [Setup for maintenance requests](../setup-for-maintenance-requests/requests.md).</span></span>

<span data-ttu-id="60849-107">资产管理的设置决定是否可以使用入站资产和出站资产。</span><span class="sxs-lookup"><span data-stu-id="60849-107">The setup of Asset Management determines whether you can work with inbound and outbound assets.</span></span>

## <a name="register-assets-as-inbound"></a><span data-ttu-id="60849-108">将资产登记为入站资产</span><span class="sxs-lookup"><span data-stu-id="60849-108">Register assets as inbound</span></span>

1. <span data-ttu-id="60849-109">选择**资产管理** \> **常用** \> **维护请求** \> **有效维护请求**。</span><span class="sxs-lookup"><span data-stu-id="60849-109">Select **Asset management** \> **Common** \> **Maintenance requests** \> **Active maintenance requests**.</span></span>
2. <span data-ttu-id="60849-110">选择维护请求。</span><span class="sxs-lookup"><span data-stu-id="60849-110">Select the maintenance request.</span></span>
3. <span data-ttu-id="60849-111">选择**更新维护请求状态**。</span><span class="sxs-lookup"><span data-stu-id="60849-111">Select **Update maintenance request state**.</span></span>
4. <span data-ttu-id="60849-112">选择**入站**（或已为入站资产创建的其他生命周期状态），然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="60849-112">Select **Inbound** (or another lifecycle state that you've created for inbound assets), and then select **OK**.</span></span>

![图 1](media/07-manage-maintenance-requests.png)

## <a name="register-inbound-assets-as-received"></a><span data-ttu-id="60849-114">将入站资产登记为接收的资产</span><span class="sxs-lookup"><span data-stu-id="60849-114">Register inbound assets as received</span></span>

1. <span data-ttu-id="60849-115">选择**资产管理** \> **常用** \> **入站/出站** \> **入站资产**。</span><span class="sxs-lookup"><span data-stu-id="60849-115">Select **Asset management** \> **Common** \> **Inbound/outbound** \> **Inbound assets**.</span></span>
2. <span data-ttu-id="60849-116">选择资产或维护请求。</span><span class="sxs-lookup"><span data-stu-id="60849-116">Select the asset or maintenance request.</span></span>
3. <span data-ttu-id="60849-117">选择**接收资产**。</span><span class="sxs-lookup"><span data-stu-id="60849-117">Select **Receive assets**.</span></span>
4. <span data-ttu-id="60849-118">在**接收时间**字段中，输入日期和时间。</span><span class="sxs-lookup"><span data-stu-id="60849-118">In the **Received** field, enter the date and time.</span></span> <span data-ttu-id="60849-119">然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="60849-119">Then select **OK**.</span></span> <span data-ttu-id="60849-120">将从**入站资产**列表页删除记录。</span><span class="sxs-lookup"><span data-stu-id="60849-120">The record is removed from the **Inbound assets** list page.</span></span>

![图 2](media/08-manage-maintenance-requests.png)

## <a name="register-assets-as-outbound"></a><span data-ttu-id="60849-122">将资产登记为出站资产</span><span class="sxs-lookup"><span data-stu-id="60849-122">Register assets as outbound</span></span>

<span data-ttu-id="60849-123">完成维护作业或修复作业之后，可将资产登记为已返回。</span><span class="sxs-lookup"><span data-stu-id="60849-123">When you've completed the maintenance or repair job, you can register the asset as returned.</span></span>

1. <span data-ttu-id="60849-124">选择**资产管理** \> **常用** \> **维护请求** \> **有效维护请求**。</span><span class="sxs-lookup"><span data-stu-id="60849-124">Select **Asset management** \> **Common** \> **Maintenance requests** \> **Active maintenance requests**.</span></span>
2. <span data-ttu-id="60849-125">选择维护请求。</span><span class="sxs-lookup"><span data-stu-id="60849-125">Select the maintenance request.</span></span>
3. <span data-ttu-id="60849-126">选择**更新维护请求状态**。</span><span class="sxs-lookup"><span data-stu-id="60849-126">Select **Update maintenance request state**.</span></span>
4. <span data-ttu-id="60849-127">选择**出站**（或已为出站资产创建的其他生命周期状态），然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="60849-127">Select **Outbound** (or another lifecycle state that you've created for outbound assets), and then select **OK**.</span></span>

## <a name="register-outbound-assets-as-delivered"></a><span data-ttu-id="60849-128">将出站资产登记为已交付</span><span class="sxs-lookup"><span data-stu-id="60849-128">Register outbound assets as delivered</span></span>

1. <span data-ttu-id="60849-129">选择**资产管理** \> **常用** \> **入站/出站** \> **出站资产**。</span><span class="sxs-lookup"><span data-stu-id="60849-129">Select **Asset management** \> **Common** \> **Inbound/outbound** \> **Outbound assets**.</span></span>
2. <span data-ttu-id="60849-130">选择资产或维护请求。</span><span class="sxs-lookup"><span data-stu-id="60849-130">Select the asset or maintenance request.</span></span>
3. <span data-ttu-id="60849-131">选择**交付资产**。</span><span class="sxs-lookup"><span data-stu-id="60849-131">Select **Deliver assets**.</span></span>
4. <span data-ttu-id="60849-132">在**交付时间**字段中，输入日期和时间。</span><span class="sxs-lookup"><span data-stu-id="60849-132">In the **Delivered** field, enter the date and time.</span></span> <span data-ttu-id="60849-133">然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="60849-133">Then select **OK**.</span></span> <span data-ttu-id="60849-134">将从**出站资产**列表页删除记录。</span><span class="sxs-lookup"><span data-stu-id="60849-134">The record is removed from the **Outbound assets** list page.</span></span>
