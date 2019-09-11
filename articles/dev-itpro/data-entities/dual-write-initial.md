---
title: Finance and Operations 和 Common Data Service 的初始同步执行顺序
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
ms.openlocfilehash: 1473c3bad55734d5f83ee3e4c1654921b872f3bb
ms.sourcegitcommit: 3f05ede8b8acdf0550240a83a013e093b4ad043d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/13/2019
ms.locfileid: "1873120"
---
# <a name="execution-order-for-initial-synchronization-of-finance-and-operations-and-common-data-service"></a><span data-ttu-id="68120-103">Finance and Operations 和 Common Data Service 的初始同步执行顺序</span><span class="sxs-lookup"><span data-stu-id="68120-103">Execution order for initial synchronization of Finance and Operations and Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="68120-104">使用数据集成之前，必须创建客户、供应商和联系人所需的初始数据。</span><span class="sxs-lookup"><span data-stu-id="68120-104">Before you use data integration, you must create the initial data that is required for customers, vendors, and contacts.</span></span> <span data-ttu-id="68120-105">例如，希望创建新的**供应商组**项，然后将其**付款期限**值设置为 **Net30**。</span><span class="sxs-lookup"><span data-stu-id="68120-105">For example, you want to create a new **Vendor group** item and set its **Terms of Payment** value to **Net30**.</span></span> <span data-ttu-id="68120-106">在此情况下，尝试创建**供应商组**项之前，必须确保 Microsoft Dynamics 365 for Finance and Operations 和 Common Data Service 中都有 **Net30**。</span><span class="sxs-lookup"><span data-stu-id="68120-106">In this case, before you try to create the **Vendor group** item, you must make sure that **Net30** exists in both Microsoft Dynamics 365 for Finance and Operations and Common Data Service.</span></span> <span data-ttu-id="68120-107">（将来，Microsoft 将发布双写入平台功能，称为“初始同步”。该功能将在执行双写入设置期间执行 Finance and Operations 与 Common Data Service 之间的一次性数据同步。）</span><span class="sxs-lookup"><span data-stu-id="68120-107">(In the future, Microsoft will release dual-write platform functionality that is named Initial Sync. This functionality will do a one-time data synchronization between Finance and Operations and Common Data Service as part of the dual-write setup.)</span></span>

> [!TIP]
> <span data-ttu-id="68120-108">Microsoft 将为所有引用数据（包括**付款期限**）发布双写入映射。</span><span class="sxs-lookup"><span data-stu-id="68120-108">Microsoft is releasing a dual-write map for all reference data, including **Terms of Payment** (payment terms).</span></span> <span data-ttu-id="68120-109">如果一个系统中已经有初始数据，对记录执行的小型更新操作可对该记录触发双写入。</span><span class="sxs-lookup"><span data-stu-id="68120-109">If you already have the initial data in one system, a small update operation on a record can trigger dual-write on that record.</span></span>

<span data-ttu-id="68120-110">必须遵守以下过程顺序，并确保 Finance and Operations 和 Common Data Service 中均有初始数据。</span><span class="sxs-lookup"><span data-stu-id="68120-110">You must follow the following order of precedence and make sure that the initial data is available in both Finance and Operations and Common Data Service.</span></span>

## <a name="vendor"></a><span data-ttu-id="68120-111">供应商</span><span class="sxs-lookup"><span data-stu-id="68120-111">Vendor</span></span>

<span data-ttu-id="68120-112">下面是**供应商**实体的执行顺序：</span><span class="sxs-lookup"><span data-stu-id="68120-112">Here is the order of execution for the **Vendor** entity:</span></span>

1. <span data-ttu-id="68120-113">供应商组</span><span class="sxs-lookup"><span data-stu-id="68120-113">Vendor group</span></span>

    1. <span data-ttu-id="68120-114">付款期限</span><span class="sxs-lookup"><span data-stu-id="68120-114">Terms of payment</span></span>

        1. <span data-ttu-id="68120-115">付款日和行</span><span class="sxs-lookup"><span data-stu-id="68120-115">Payment day and lines</span></span>
        2. <span data-ttu-id="68120-116">付款计划</span><span class="sxs-lookup"><span data-stu-id="68120-116">Payment schedule</span></span>

2. <span data-ttu-id="68120-117">供应商付款方式</span><span class="sxs-lookup"><span data-stu-id="68120-117">Vendor payment method</span></span>

## <a name="customer-organization"></a><span data-ttu-id="68120-118">客户（组织）</span><span class="sxs-lookup"><span data-stu-id="68120-118">Customer (Organization)</span></span>

<span data-ttu-id="68120-119">下面是**客户**实体的执行顺序：</span><span class="sxs-lookup"><span data-stu-id="68120-119">Here is the order of execution for the **Customer** entity:</span></span>

1. <span data-ttu-id="68120-120">客户组</span><span class="sxs-lookup"><span data-stu-id="68120-120">Customer group</span></span>

    1. <span data-ttu-id="68120-121">付款期限</span><span class="sxs-lookup"><span data-stu-id="68120-121">Terms of payment</span></span>

        1. <span data-ttu-id="68120-122">付款日和行</span><span class="sxs-lookup"><span data-stu-id="68120-122">Payment day and lines</span></span>
        2. <span data-ttu-id="68120-123">付款</span><span class="sxs-lookup"><span data-stu-id="68120-123">Payment</span></span> 

2. <span data-ttu-id="68120-124">客户付款方式</span><span class="sxs-lookup"><span data-stu-id="68120-124">Customer payment method</span></span>

## <a name="contact-person"></a><span data-ttu-id="68120-125">联系人（个人）</span><span class="sxs-lookup"><span data-stu-id="68120-125">Contact (Person)</span></span>

<span data-ttu-id="68120-126">下面是**联系人**实体的执行顺序：</span><span class="sxs-lookup"><span data-stu-id="68120-126">Here is the order of execution for the **Contact** entity:</span></span>

1. <span data-ttu-id="68120-127">客户</span><span class="sxs-lookup"><span data-stu-id="68120-127">Customer</span></span>
2. <span data-ttu-id="68120-128">供应商</span><span class="sxs-lookup"><span data-stu-id="68120-128">Vendor</span></span>
