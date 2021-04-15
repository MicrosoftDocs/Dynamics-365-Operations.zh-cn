---
title: 入站资产和出站资产
description: 本主题介绍如何在资产管理中登记入站资产和出站资产。
author: johanhoffmann
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetOutboundObjectsListPage, EntAssetOutboundObjectsDeliver, EntAssetInboundObjectsListPage, EntAssetInboundObjectsRecieve
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1a2bac914330058400a7e4d7d355bd4a00a4522f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5816788"
---
# <a name="inbound-and-outbound-assets"></a><span data-ttu-id="a7d6f-103">入站资产和出站资产</span><span class="sxs-lookup"><span data-stu-id="a7d6f-103">Inbound and outbound assets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="a7d6f-104">如果公司对从其他位置或客户收到的资产执行维修作业或维护作业，资产管理同时可跟踪正在前往公司的入站资产和正在退回的出站资产。</span><span class="sxs-lookup"><span data-stu-id="a7d6f-104">If your company does repair jobs or maintenance jobs on assets that are received from other locations or customers, Asset Management can track both inbound assets that are on their way to your company and outbound assets that are being returned.</span></span>

> [!NOTE]
> <span data-ttu-id="a7d6f-105">如果要使用入站生命周期状态和出站生命周期状态管理正在前来的资产和正在退回的资产，则必须设置维护请求生命周期状态和生命周期模型来支持这些操作。</span><span class="sxs-lookup"><span data-stu-id="a7d6f-105">If you want to use inbound and outbound lifecycle states to manage assets that are coming in and being returned, you must set up maintenance request lifecycle states and lifecycle models to support these actions.</span></span> <span data-ttu-id="a7d6f-106">有关详细信息，请参阅[维护请求](../setup-for-maintenance-requests/requests.md)。</span><span class="sxs-lookup"><span data-stu-id="a7d6f-106">For more information, see [Maintenance requests](../setup-for-maintenance-requests/requests.md).</span></span>

<span data-ttu-id="a7d6f-107">资产管理的设置决定是否可以使用入站资产和出站资产。</span><span class="sxs-lookup"><span data-stu-id="a7d6f-107">The setup of Asset Management determines whether you can work with inbound and outbound assets.</span></span>

## <a name="register-assets-as-inbound"></a><span data-ttu-id="a7d6f-108">将资产登记为入站资产</span><span class="sxs-lookup"><span data-stu-id="a7d6f-108">Register assets as inbound</span></span>

1. <span data-ttu-id="a7d6f-109">选择 **资产管理** \> **常用** \> **维护请求** \> **有效维护请求**。</span><span class="sxs-lookup"><span data-stu-id="a7d6f-109">Select **Asset management** \> **Common** \> **Maintenance requests** \> **Active maintenance requests**.</span></span>
2. <span data-ttu-id="a7d6f-110">选择维护请求。</span><span class="sxs-lookup"><span data-stu-id="a7d6f-110">Select the maintenance request.</span></span>
3. <span data-ttu-id="a7d6f-111">选择 **更新维护请求状态**。</span><span class="sxs-lookup"><span data-stu-id="a7d6f-111">Select **Update maintenance request state**.</span></span>
4. <span data-ttu-id="a7d6f-112">选择 **入站**（或已为入站资产创建的其他生命周期状态），然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="a7d6f-112">Select **Inbound** (or another lifecycle state that you've created for inbound assets), and then select **OK**.</span></span>

![将资产登记为入站资产](media/07-manage-maintenance-requests.png)

## <a name="register-inbound-assets-as-received"></a><span data-ttu-id="a7d6f-114">将入站资产登记为接收的资产</span><span class="sxs-lookup"><span data-stu-id="a7d6f-114">Register inbound assets as received</span></span>

1. <span data-ttu-id="a7d6f-115">选择 **资产管理** \> **常用** \> **入站/出站** \> **入站资产**。</span><span class="sxs-lookup"><span data-stu-id="a7d6f-115">Select **Asset management** \> **Common** \> **Inbound/outbound** \> **Inbound assets**.</span></span>
2. <span data-ttu-id="a7d6f-116">选择资产或维护请求。</span><span class="sxs-lookup"><span data-stu-id="a7d6f-116">Select the asset or maintenance request.</span></span>
3. <span data-ttu-id="a7d6f-117">选择 **接收资产**。</span><span class="sxs-lookup"><span data-stu-id="a7d6f-117">Select **Receive assets**.</span></span>
4. <span data-ttu-id="a7d6f-118">在 **接收时间** 字段中，输入日期和时间。</span><span class="sxs-lookup"><span data-stu-id="a7d6f-118">In the **Received** field, enter the date and time.</span></span> <span data-ttu-id="a7d6f-119">然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="a7d6f-119">Then select **OK**.</span></span> <span data-ttu-id="a7d6f-120">将从 **入站资产** 列表页删除记录。</span><span class="sxs-lookup"><span data-stu-id="a7d6f-120">The record is removed from the **Inbound assets** list page.</span></span>

![将入站资产登记为接收的资产](media/08-manage-maintenance-requests.png)

## <a name="register-assets-as-outbound"></a><span data-ttu-id="a7d6f-122">将资产登记为出站资产</span><span class="sxs-lookup"><span data-stu-id="a7d6f-122">Register assets as outbound</span></span>

<span data-ttu-id="a7d6f-123">完成维护作业或修复作业之后，可将资产登记为已返回。</span><span class="sxs-lookup"><span data-stu-id="a7d6f-123">When you've completed the maintenance or repair job, you can register the asset as returned.</span></span>

1. <span data-ttu-id="a7d6f-124">选择 **资产管理** \> **常用** \> **维护请求** \> **有效维护请求**。</span><span class="sxs-lookup"><span data-stu-id="a7d6f-124">Select **Asset management** \> **Common** \> **Maintenance requests** \> **Active maintenance requests**.</span></span>
2. <span data-ttu-id="a7d6f-125">选择维护请求。</span><span class="sxs-lookup"><span data-stu-id="a7d6f-125">Select the maintenance request.</span></span>
3. <span data-ttu-id="a7d6f-126">选择 **更新维护请求状态**。</span><span class="sxs-lookup"><span data-stu-id="a7d6f-126">Select **Update maintenance request state**.</span></span>
4. <span data-ttu-id="a7d6f-127">选择 **出站**（或已为出站资产创建的其他生命周期状态），然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="a7d6f-127">Select **Outbound** (or another lifecycle state that you've created for outbound assets), and then select **OK**.</span></span>

## <a name="register-outbound-assets-as-delivered"></a><span data-ttu-id="a7d6f-128">将出站资产登记为已交付</span><span class="sxs-lookup"><span data-stu-id="a7d6f-128">Register outbound assets as delivered</span></span>

1. <span data-ttu-id="a7d6f-129">选择 **资产管理** \> **常用** \> **入站/出站** \> **出站资产**。</span><span class="sxs-lookup"><span data-stu-id="a7d6f-129">Select **Asset management** \> **Common** \> **Inbound/outbound** \> **Outbound assets**.</span></span>
2. <span data-ttu-id="a7d6f-130">选择资产或维护请求。</span><span class="sxs-lookup"><span data-stu-id="a7d6f-130">Select the asset or maintenance request.</span></span>
3. <span data-ttu-id="a7d6f-131">选择 **交付资产**。</span><span class="sxs-lookup"><span data-stu-id="a7d6f-131">Select **Deliver assets**.</span></span>
4. <span data-ttu-id="a7d6f-132">在 **交付时间** 字段中，输入日期和时间。</span><span class="sxs-lookup"><span data-stu-id="a7d6f-132">In the **Delivered** field, enter the date and time.</span></span> <span data-ttu-id="a7d6f-133">然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="a7d6f-133">Then select **OK**.</span></span> <span data-ttu-id="a7d6f-134">将从 **出站资产** 列表页删除记录。</span><span class="sxs-lookup"><span data-stu-id="a7d6f-134">The record is removed from the **Outbound assets** list page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]