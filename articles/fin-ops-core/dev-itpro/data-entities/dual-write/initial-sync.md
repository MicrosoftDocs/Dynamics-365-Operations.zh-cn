---
title: Finance and Operations 应用和 Common Data Service 初始同步的执行顺序
description: 本主题指定创建初始数据时必须遵守的同步顺序。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: befe4e12a10f4a39b90bcb4faba6431a063a40e2
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019660"
---
# <a name="execution-order-for-initial-synchronization-of-finance-and-operations-apps-and-common-data-service"></a><span data-ttu-id="6a677-103">Finance and Operations 应用和 Common Data Service 初始同步的执行顺序</span><span class="sxs-lookup"><span data-stu-id="6a677-103">Execution order for initial synchronization of Finance and Operations apps and Common Data Service</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="6a677-104">使用数据集成之前，必须创建客户、供应商和联系人所需的初始数据。</span><span class="sxs-lookup"><span data-stu-id="6a677-104">Before you use data integration, you must create the initial data that is required for customers, vendors, and contacts.</span></span> <span data-ttu-id="6a677-105">例如，希望创建新的**供应商组**项，然后将其**付款期限**值设置为 **Net30**。</span><span class="sxs-lookup"><span data-stu-id="6a677-105">For example, you want to create a new **Vendor group** item and set its **Terms of Payment** value to **Net30**.</span></span> <span data-ttu-id="6a677-106">在此情况下，尝试创建**供应商组**项之前，必须确保应用程序和 Common Data Service 中都有 **Net30**。</span><span class="sxs-lookup"><span data-stu-id="6a677-106">In this case, before you try to create the **Vendor group** item, you must make sure that **Net30** exists in both the application and Common Data Service.</span></span> <span data-ttu-id="6a677-107">（将来，Microsoft 将发布双写入平台功能，称为“初始同步”。该功能将在执行双写入设置期间执行应用程序与 Common Data Service 之间的一次性数据同步。）</span><span class="sxs-lookup"><span data-stu-id="6a677-107">(In the future, Microsoft will release dual-write platform functionality that is named Initial Sync. This functionality will do a one-time data synchronization between the application and Common Data Service as part of the dual-write setup.)</span></span>

> [!TIP]
> <span data-ttu-id="6a677-108">Microsoft 将为所有引用数据（包括**付款期限**）发布双写入映射。</span><span class="sxs-lookup"><span data-stu-id="6a677-108">Microsoft is releasing a dual-write map for all reference data, including **Terms of Payment** (payment terms).</span></span> <span data-ttu-id="6a677-109">如果一个系统中已经有初始数据，对记录执行的小型更新操作可对该记录触发双写入。</span><span class="sxs-lookup"><span data-stu-id="6a677-109">If you already have the initial data in one system, a small update operation on a record can trigger dual-write on that record.</span></span>

<span data-ttu-id="6a677-110">必须遵守以下过程顺序，并确保此应用程序和 Common Data Service 中均有初始数据。</span><span class="sxs-lookup"><span data-stu-id="6a677-110">You must follow the following order of precedence and make sure that the initial data is available in the application and Common Data Service.</span></span>

## <a name="vendor"></a><span data-ttu-id="6a677-111">供应商</span><span class="sxs-lookup"><span data-stu-id="6a677-111">Vendor</span></span>

<span data-ttu-id="6a677-112">下面是**供应商**实体的执行顺序：</span><span class="sxs-lookup"><span data-stu-id="6a677-112">Here is the order of execution for the **Vendor** entity:</span></span>

1. <span data-ttu-id="6a677-113">供应商组</span><span class="sxs-lookup"><span data-stu-id="6a677-113">Vendor group</span></span>

    1. <span data-ttu-id="6a677-114">付款期限</span><span class="sxs-lookup"><span data-stu-id="6a677-114">Terms of payment</span></span>

        1. <span data-ttu-id="6a677-115">付款日和行</span><span class="sxs-lookup"><span data-stu-id="6a677-115">Payment day and lines</span></span>
        2. <span data-ttu-id="6a677-116">付款计划</span><span class="sxs-lookup"><span data-stu-id="6a677-116">Payment schedule</span></span>

2. <span data-ttu-id="6a677-117">供应商付款方式</span><span class="sxs-lookup"><span data-stu-id="6a677-117">Vendor payment method</span></span>

## <a name="customer-organization"></a><span data-ttu-id="6a677-118">客户（组织）</span><span class="sxs-lookup"><span data-stu-id="6a677-118">Customer (Organization)</span></span>

<span data-ttu-id="6a677-119">下面是**客户**实体的执行顺序：</span><span class="sxs-lookup"><span data-stu-id="6a677-119">Here is the order of execution for the **Customer** entity:</span></span>

1. <span data-ttu-id="6a677-120">客户组</span><span class="sxs-lookup"><span data-stu-id="6a677-120">Customer group</span></span>

    1. <span data-ttu-id="6a677-121">付款期限</span><span class="sxs-lookup"><span data-stu-id="6a677-121">Terms of payment</span></span>

        1. <span data-ttu-id="6a677-122">付款日和行</span><span class="sxs-lookup"><span data-stu-id="6a677-122">Payment day and lines</span></span>
        2. <span data-ttu-id="6a677-123">付款</span><span class="sxs-lookup"><span data-stu-id="6a677-123">Payment</span></span> 

2. <span data-ttu-id="6a677-124">客户付款方式</span><span class="sxs-lookup"><span data-stu-id="6a677-124">Customer payment method</span></span>

## <a name="contact-person"></a><span data-ttu-id="6a677-125">联系人（个人）</span><span class="sxs-lookup"><span data-stu-id="6a677-125">Contact (Person)</span></span>

<span data-ttu-id="6a677-126">下面是**联系人**实体的执行顺序：</span><span class="sxs-lookup"><span data-stu-id="6a677-126">Here is the order of execution for the **Contact** entity:</span></span>

1. <span data-ttu-id="6a677-127">客户</span><span class="sxs-lookup"><span data-stu-id="6a677-127">Customer</span></span>
2. <span data-ttu-id="6a677-128">供应商</span><span class="sxs-lookup"><span data-stu-id="6a677-128">Vendor</span></span>
