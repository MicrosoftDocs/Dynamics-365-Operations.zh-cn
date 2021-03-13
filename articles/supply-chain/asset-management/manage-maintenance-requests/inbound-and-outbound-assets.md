---
title: 入站资产和出站资产
description: 本主题介绍如何在资产管理中登记入站资产和出站资产。
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetOutboundObjectsListPage, EntAssetOutboundObjectsDeliver, EntAssetInboundObjectsListPage, EntAssetInboundObjectsRecieve
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e6dfadf6824c6a3df7be9b3b6f3d9f5dd2749e34
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/16/2021
ms.locfileid: "5018063"
---
# <a name="inbound-and-outbound-assets"></a><span data-ttu-id="1ca08-103">入站资产和出站资产</span><span class="sxs-lookup"><span data-stu-id="1ca08-103">Inbound and outbound assets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="1ca08-104">如果公司对从其他位置或客户收到的资产执行维修作业或维护作业，资产管理同时可跟踪正在前往公司的入站资产和正在退回的出站资产。</span><span class="sxs-lookup"><span data-stu-id="1ca08-104">If your company does repair jobs or maintenance jobs on assets that are received from other locations or customers, Asset Management can track both inbound assets that are on their way to your company and outbound assets that are being returned.</span></span>

> [!NOTE]
> <span data-ttu-id="1ca08-105">如果要使用入站生命周期状态和出站生命周期状态管理正在前来的资产和正在退回的资产，则必须设置维护请求生命周期状态和生命周期模型来支持这些操作。</span><span class="sxs-lookup"><span data-stu-id="1ca08-105">If you want to use inbound and outbound lifecycle states to manage assets that are coming in and being returned, you must set up maintenance request lifecycle states and lifecycle models to support these actions.</span></span> <span data-ttu-id="1ca08-106">有关详细信息，请参阅[维护请求](../setup-for-maintenance-requests/requests.md)。</span><span class="sxs-lookup"><span data-stu-id="1ca08-106">For more information, see [Maintenance requests](../setup-for-maintenance-requests/requests.md).</span></span>

<span data-ttu-id="1ca08-107">资产管理的设置决定是否可以使用入站资产和出站资产。</span><span class="sxs-lookup"><span data-stu-id="1ca08-107">The setup of Asset Management determines whether you can work with inbound and outbound assets.</span></span>

## <a name="register-assets-as-inbound"></a><span data-ttu-id="1ca08-108">将资产登记为入站资产</span><span class="sxs-lookup"><span data-stu-id="1ca08-108">Register assets as inbound</span></span>

1. <span data-ttu-id="1ca08-109">选择 **资产管理** \> **常用** \> **维护请求** \> **有效维护请求**。</span><span class="sxs-lookup"><span data-stu-id="1ca08-109">Select **Asset management** \> **Common** \> **Maintenance requests** \> **Active maintenance requests**.</span></span>
2. <span data-ttu-id="1ca08-110">选择维护请求。</span><span class="sxs-lookup"><span data-stu-id="1ca08-110">Select the maintenance request.</span></span>
3. <span data-ttu-id="1ca08-111">选择 **更新维护请求状态**。</span><span class="sxs-lookup"><span data-stu-id="1ca08-111">Select **Update maintenance request state**.</span></span>
4. <span data-ttu-id="1ca08-112">选择 **入站**（或已为入站资产创建的其他生命周期状态），然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="1ca08-112">Select **Inbound** (or another lifecycle state that you've created for inbound assets), and then select **OK**.</span></span>

![将资产登记为入站资产](media/07-manage-maintenance-requests.png)

## <a name="register-inbound-assets-as-received"></a><span data-ttu-id="1ca08-114">将入站资产登记为接收的资产</span><span class="sxs-lookup"><span data-stu-id="1ca08-114">Register inbound assets as received</span></span>

1. <span data-ttu-id="1ca08-115">选择 **资产管理** \> **常用** \> **入站/出站** \> **入站资产**。</span><span class="sxs-lookup"><span data-stu-id="1ca08-115">Select **Asset management** \> **Common** \> **Inbound/outbound** \> **Inbound assets**.</span></span>
2. <span data-ttu-id="1ca08-116">选择资产或维护请求。</span><span class="sxs-lookup"><span data-stu-id="1ca08-116">Select the asset or maintenance request.</span></span>
3. <span data-ttu-id="1ca08-117">选择 **接收资产**。</span><span class="sxs-lookup"><span data-stu-id="1ca08-117">Select **Receive assets**.</span></span>
4. <span data-ttu-id="1ca08-118">在 **接收时间** 字段中，输入日期和时间。</span><span class="sxs-lookup"><span data-stu-id="1ca08-118">In the **Received** field, enter the date and time.</span></span> <span data-ttu-id="1ca08-119">然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="1ca08-119">Then select **OK**.</span></span> <span data-ttu-id="1ca08-120">将从 **入站资产** 列表页删除记录。</span><span class="sxs-lookup"><span data-stu-id="1ca08-120">The record is removed from the **Inbound assets** list page.</span></span>

![将入站资产登记为接收的资产](media/08-manage-maintenance-requests.png)

## <a name="register-assets-as-outbound"></a><span data-ttu-id="1ca08-122">将资产登记为出站资产</span><span class="sxs-lookup"><span data-stu-id="1ca08-122">Register assets as outbound</span></span>

<span data-ttu-id="1ca08-123">完成维护作业或修复作业之后，可将资产登记为已返回。</span><span class="sxs-lookup"><span data-stu-id="1ca08-123">When you've completed the maintenance or repair job, you can register the asset as returned.</span></span>

1. <span data-ttu-id="1ca08-124">选择 **资产管理** \> **常用** \> **维护请求** \> **有效维护请求**。</span><span class="sxs-lookup"><span data-stu-id="1ca08-124">Select **Asset management** \> **Common** \> **Maintenance requests** \> **Active maintenance requests**.</span></span>
2. <span data-ttu-id="1ca08-125">选择维护请求。</span><span class="sxs-lookup"><span data-stu-id="1ca08-125">Select the maintenance request.</span></span>
3. <span data-ttu-id="1ca08-126">选择 **更新维护请求状态**。</span><span class="sxs-lookup"><span data-stu-id="1ca08-126">Select **Update maintenance request state**.</span></span>
4. <span data-ttu-id="1ca08-127">选择 **出站**（或已为出站资产创建的其他生命周期状态），然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="1ca08-127">Select **Outbound** (or another lifecycle state that you've created for outbound assets), and then select **OK**.</span></span>

## <a name="register-outbound-assets-as-delivered"></a><span data-ttu-id="1ca08-128">将出站资产登记为已交付</span><span class="sxs-lookup"><span data-stu-id="1ca08-128">Register outbound assets as delivered</span></span>

1. <span data-ttu-id="1ca08-129">选择 **资产管理** \> **常用** \> **入站/出站** \> **出站资产**。</span><span class="sxs-lookup"><span data-stu-id="1ca08-129">Select **Asset management** \> **Common** \> **Inbound/outbound** \> **Outbound assets**.</span></span>
2. <span data-ttu-id="1ca08-130">选择资产或维护请求。</span><span class="sxs-lookup"><span data-stu-id="1ca08-130">Select the asset or maintenance request.</span></span>
3. <span data-ttu-id="1ca08-131">选择 **交付资产**。</span><span class="sxs-lookup"><span data-stu-id="1ca08-131">Select **Deliver assets**.</span></span>
4. <span data-ttu-id="1ca08-132">在 **交付时间** 字段中，输入日期和时间。</span><span class="sxs-lookup"><span data-stu-id="1ca08-132">In the **Delivered** field, enter the date and time.</span></span> <span data-ttu-id="1ca08-133">然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="1ca08-133">Then select **OK**.</span></span> <span data-ttu-id="1ca08-134">将从 **出站资产** 列表页删除记录。</span><span class="sxs-lookup"><span data-stu-id="1ca08-134">The record is removed from the **Outbound assets** list page.</span></span>
