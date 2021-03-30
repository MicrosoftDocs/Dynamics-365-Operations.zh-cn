---
title: 设置群集领料
description: 此主题介绍如何设置群集领料和如何为群集领料应用物料确认。
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSClusterProfile, WHSRFAutoConfirm, WHSWorkCluster
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2b3df8cf5e63fe97925f17001e836a41c703dfc9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5239222"
---
# <a name="set-up-cluster-picking"></a><span data-ttu-id="5b72a-103">设置群集领料</span><span class="sxs-lookup"><span data-stu-id="5b72a-103">Set up cluster picking</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="5b72a-104">本主题描述了如何是工作人员使用其移动设备将领料工作分组为群集，以便为多个工作订单同时从一个库位领料。</span><span class="sxs-lookup"><span data-stu-id="5b72a-104">This topic describes how to enable workers to use their mobile devices to group picking work into clusters, so that they can pick items from a single location for multiple work orders at the same time.</span></span> <span data-ttu-id="5b72a-105">这被称为 *群集领料*。</span><span class="sxs-lookup"><span data-stu-id="5b72a-105">This is called *cluster picking*.</span></span>

## <a name="about-cluster-picking"></a><span data-ttu-id="5b72a-106">关于群集领料</span><span class="sxs-lookup"><span data-stu-id="5b72a-106">About cluster picking</span></span>

<span data-ttu-id="5b72a-107">在工作订单下达到仓库后，工作人员可以使用移动设备将订单分配到群集。</span><span class="sxs-lookup"><span data-stu-id="5b72a-107">After work orders are released to the warehouse, the worker can use a mobile device to assign the orders to a cluster.</span></span> <span data-ttu-id="5b72a-108">群集将为工作人员组织领料工作。</span><span class="sxs-lookup"><span data-stu-id="5b72a-108">The cluster will organize the picking work for the worker.</span></span> <span data-ttu-id="5b72a-109">在将工作订单分配给集群后，工作人员必须使用群集领料为订单执行领料工作。</span><span class="sxs-lookup"><span data-stu-id="5b72a-109">When a work order is assigned to a cluster, the worker must use cluster picking to perform the picking work for the order.</span></span> <span data-ttu-id="5b72a-110">工作人员不能使用其他领料方法。</span><span class="sxs-lookup"><span data-stu-id="5b72a-110">The worker cannot use other picking methods.</span></span> <span data-ttu-id="5b72a-111">如果将工作订单错误分配到群组，工作人员必须拆分群组，然后重新创建。</span><span class="sxs-lookup"><span data-stu-id="5b72a-111">If a work order is assigned to a cluster by mistake, the worker must break the cluster and then re-create it.</span></span>

<span data-ttu-id="5b72a-112">若有需要，工作人员可以将群集传递给其他工作人员。</span><span class="sxs-lookup"><span data-stu-id="5b72a-112">If needed, a worker can pass a cluster to another worker.</span></span> <span data-ttu-id="5b72a-113">此操作会将群集状态更改为“传递”。</span><span class="sxs-lookup"><span data-stu-id="5b72a-113">This changes the cluster status to Passed.</span></span> <span data-ttu-id="5b72a-114">在工作人员使用移动设备指示领料，并且完成整理后，必须在客户端中确认装运或负荷。</span><span class="sxs-lookup"><span data-stu-id="5b72a-114">When the worker uses a mobile device to indicate that the picking and put away work is completed, the shipment or load must be confirmed in the client.</span></span>

## <a name="enable-cluster-picking"></a><span data-ttu-id="5b72a-115">启用群集领料</span><span class="sxs-lookup"><span data-stu-id="5b72a-115">Enable cluster picking</span></span>

<span data-ttu-id="5b72a-116">若要启用群集领料，则必须设置以下内容：</span><span class="sxs-lookup"><span data-stu-id="5b72a-116">To enable cluster picking, you must set up the following:</span></span>

- <span data-ttu-id="5b72a-117">**群集配置文件** – 指定是否自动生成群集 ID、要使用的库位数量，以及何时拆分群集和如何排序和验证领料工作。</span><span class="sxs-lookup"><span data-stu-id="5b72a-117">**Cluster profiles** – Specify whether to automatically generate cluster   IDs, the number of positions to use, when to break clusters, and how to   sequence and verify the picking work.</span></span>

- <span data-ttu-id="5b72a-118">**工作模板** – 定义如何为群集领料创建领料工作。</span><span class="sxs-lookup"><span data-stu-id="5b72a-118">**Work templates** – Define how to create the picking work for cluster   picking.</span></span>

- <span data-ttu-id="5b72a-119">**位置指令** – 指定从哪儿领料和物料的放置位置。</span><span class="sxs-lookup"><span data-stu-id="5b72a-119">**Location directives** – Specify where to pick items from, and where to put   them.</span></span>

- <span data-ttu-id="5b72a-120">**移动设备菜单项** – 配置移动设备菜单使用群集领料主导的现有工作。</span><span class="sxs-lookup"><span data-stu-id="5b72a-120">**Mobile device menu items** – Configure a mobile device menu item to use existing work that is directed by cluster picking.</span></span> <span data-ttu-id="5b72a-121">您必须将菜单项添加到移动菜单以便在移动设备上显示。</span><span class="sxs-lookup"><span data-stu-id="5b72a-121">You must then add the menu item to a mobile device menu so that it is displayed on mobile devices.</span></span>

- <span data-ttu-id="5b72a-122">**仓库管理参数** – 若要生成群集的标识符，请指定编号顺序。</span><span class="sxs-lookup"><span data-stu-id="5b72a-122">**Warehouse management parameters** – Specify the number sequence to use if   you want to generate identifiers for clusters.</span></span>

## <a name="set-up-a-cluster-profile"></a><span data-ttu-id="5b72a-123">设置群集配置文件</span><span class="sxs-lookup"><span data-stu-id="5b72a-123">Set up a cluster profile</span></span>

<span data-ttu-id="5b72a-124">若要设置群集配置文件，请按以下步骤进行操作：</span><span class="sxs-lookup"><span data-stu-id="5b72a-124">To set up a cluster profile, follow these steps:</span></span>

1. <span data-ttu-id="5b72a-125">单击 **仓库管理** \> **设置** \> **移动设备** \> **群集配置文件**。</span><span class="sxs-lookup"><span data-stu-id="5b72a-125">Click **Warehouse management** \> **Setup** \> **Mobile device** \>  **Cluster profiles**.</span></span>

1. <span data-ttu-id="5b72a-126">单击 **新建** 创建一个新的配置文件。</span><span class="sxs-lookup"><span data-stu-id="5b72a-126">Click **New** to create a new profile.</span></span>

1. <span data-ttu-id="5b72a-127">单击 **创建群集**，然后在 **群集排序** 下，单击 **新建** 设置群集的排序条件。</span><span class="sxs-lookup"><span data-stu-id="5b72a-127">Click **Create cluster** and, under **Cluster sorting**, click **New** to set up the sorting criteria for the cluster.</span></span> <span data-ttu-id="5b72a-128">排序条件控制工作人员执行领料工作的订单。</span><span class="sxs-lookup"><span data-stu-id="5b72a-128">The sorting criteria control the order in which the worker will perform the picking work.</span></span> <span data-ttu-id="5b72a-129">您可以根据需要添加任意多的条件。</span><span class="sxs-lookup"><span data-stu-id="5b72a-129">You can add as many criteria as needed.</span></span>

1. <span data-ttu-id="5b72a-130">在 **序列号** 字段中，输入编号以定义排序条件的处理顺序。</span><span class="sxs-lookup"><span data-stu-id="5b72a-130">In the **Sequence number** field, enter a number to define the order in  which the sorting criteria are processed.</span></span>

1. <span data-ttu-id="5b72a-131">在 **字段名称** 字段中，选择决定排序的字段。</span><span class="sxs-lookup"><span data-stu-id="5b72a-131">In the **Field name** field, select the field that will determine the sorting.</span></span> <span data-ttu-id="5b72a-132">例如，如果您选择 **WMSLocationId** 字段，则工作将按库位排序。</span><span class="sxs-lookup"><span data-stu-id="5b72a-132">For example, if you select the **WMSLocationId** field, the work will be sorted by location.</span></span>

1. <span data-ttu-id="5b72a-133">在 **排序** 字段中，选择下列选项之一。</span><span class="sxs-lookup"><span data-stu-id="5b72a-133">In the **Sorting** field, select one of the following options.</span></span>

| <span data-ttu-id="5b72a-134">**选项**</span><span class="sxs-lookup"><span data-stu-id="5b72a-134">**Option**</span></span>     | <span data-ttu-id="5b72a-135">**说明**</span><span class="sxs-lookup"><span data-stu-id="5b72a-135">**Description**</span></span>                                                                                                                                                                                                                    |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b72a-136">**升序**</span><span class="sxs-lookup"><span data-stu-id="5b72a-136">**Ascending**</span></span>  | <span data-ttu-id="5b72a-137">基于排序条件，领料工作按升序排序。</span><span class="sxs-lookup"><span data-stu-id="5b72a-137">Picking work is sequenced in ascending order based on the sorting criteria.</span></span> <span data-ttu-id="5b72a-138">例如，如果您使用 **WMSLocationId** 字段作为排序条件，您的位置 ID 是 1、2、3 和 4，则您需首先从库位 4 中领料。</span><span class="sxs-lookup"><span data-stu-id="5b72a-138">For example, if you use the **WMSLocationId** field as sorting criteria, and your location IDs are 1, 2, 3, and 4, you will pick from location 4 first.</span></span> |
| <span data-ttu-id="5b72a-139">**降序**</span><span class="sxs-lookup"><span data-stu-id="5b72a-139">**Descending**</span></span> | <span data-ttu-id="5b72a-140">基于排序条件，领料工作按降序排序。</span><span class="sxs-lookup"><span data-stu-id="5b72a-140">Picking work is sequenced in descending order based on the sorting criteria.</span></span> <span data-ttu-id="5b72a-141">例如，如果您使用 **WMSLocationId** 字段作为排序条件，您的位置 ID 是 1、2、3 和 4，则您需首先从库位 1 中领料。</span><span class="sxs-lookup"><span data-stu-id="5b72a-141">For example, if you use the **WMSLocationId** field as sorting criteria, and your location IDs are 1, 2, 3, and 4, you will pick from location 1 first.</span></span> |

## <a name="item-confirmation"></a><span data-ttu-id="5b72a-142">物料配置</span><span class="sxs-lookup"><span data-stu-id="5b72a-142">Item confirmation</span></span>

<span data-ttu-id="5b72a-143">应用群集领料时，物料确认是验证添加到群集的物料的关键。</span><span class="sxs-lookup"><span data-stu-id="5b72a-143">When cluster picking is applied, item confirmation is crucial to verify the items that are added to clusters.</span></span> <span data-ttu-id="5b72a-144">您可以在群集领料流程中验证群集领料中的物料。</span><span class="sxs-lookup"><span data-stu-id="5b72a-144">You can verify items in cluster picking during the cluster picking process.</span></span> <span data-ttu-id="5b72a-145">设置基于产品条码设置。</span><span class="sxs-lookup"><span data-stu-id="5b72a-145">The setup is based on the product bar code setup.</span></span>

### <a name="set-up-item-verification-with-cluster-picking"></a><span data-ttu-id="5b72a-146">设置群集领料的物料验证</span><span class="sxs-lookup"><span data-stu-id="5b72a-146">Set up item verification with cluster picking</span></span>

1. <span data-ttu-id="5b72a-147">在移动设备菜单项上，打开工作确认的设置窗体：**仓库管理** \> **仓库管理** \> **设置** \> **移动设备** \> **移动设备菜单项**。</span><span class="sxs-lookup"><span data-stu-id="5b72a-147">On a mobile device menu item, open the setup form for work confirmation:  **Warehouse management** \> **Warehouse management** \> **Setup** \>  **Mobile device** \> **Mobile device menu items**.</span></span>

1. <span data-ttu-id="5b72a-148">从移动设备菜单项打开 **工作确认设置**。</span><span class="sxs-lookup"><span data-stu-id="5b72a-148">From the mobile device menu item, open **Work confirmation setup**.</span></span> <span data-ttu-id="5b72a-149">**产品确认** 选项允许您在扫描时从移动设备验证每件库存。</span><span class="sxs-lookup"><span data-stu-id="5b72a-149">The **Product confirmation** option allows you to verify each piece of inventory from the mobile device when scanned.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]