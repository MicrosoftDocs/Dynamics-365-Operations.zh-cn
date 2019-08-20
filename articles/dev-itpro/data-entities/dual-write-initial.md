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
ms.openlocfilehash: b74bc2d3133af7e87663a4e6bafb8780e0a6a66f
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797290"
---
# <a name="execution-order-for-initial-sychronization-of-finance-and-operations-and-common-data-service"></a><span data-ttu-id="62ccb-103">Finance and Operations 和 Common Data Service 的初始同步执行顺序</span><span class="sxs-lookup"><span data-stu-id="62ccb-103">Execution order for initial sychronization of Finance and Operations and Common Data Service</span></span>

<span data-ttu-id="62ccb-104">使用数据集成之前，必须创建客户、供应商和联系人所需的初始数据。</span><span class="sxs-lookup"><span data-stu-id="62ccb-104">Before you use data integration, you must create the initial data required for customers, vendors and contacts.</span></span> <span data-ttu-id="62ccb-105">例如，如果要创建新**供应商组**项并将其**付款期限**设置为 **Net30**，则在尝试创建**供应商组**项之前，需要确保 Finance and Operations 和 Common Data Service 中均有 **Net30**。</span><span class="sxs-lookup"><span data-stu-id="62ccb-105">For example, if you want to create a new **Vendor group** item and set its **Terms of Payment** as **Net30**, then before you attempt to create the **Vendor group** item you need to make sure that **Net30** exists in both Finance and Operations and Common Data Service.</span></span> <span data-ttu-id="62ccb-106">（将来，我们将发布双写入平台功能，称为**初始同步**。该功能将在执行双写入设置期间执行 Finance and Operations 与 Common Data Service 之间的一次性数据同步。）</span><span class="sxs-lookup"><span data-stu-id="62ccb-106">(In the future, we will release a  dual-write platform functionality called **Initial Sync**. It will do a one-time data synchronization between Finance and Operations and Common Data Service as part of the dual-write setup.)</span></span>

<span data-ttu-id="62ccb-107">提示：我们将为所有引用数据（包括**付款期限**）发布双写入映射。</span><span class="sxs-lookup"><span data-stu-id="62ccb-107">Tips: We are releasing a dual-write map for all reference data including **Terms of Payment** (Payment Terms).</span></span> <span data-ttu-id="62ccb-108">如果一个系统中已经有初始数据，对记录执行的小型更新操作可对该记录触发双写入。</span><span class="sxs-lookup"><span data-stu-id="62ccb-108">If you already have the initial data in one system, a small update operation on a record can trigger dual-write on that record.</span></span> 

<span data-ttu-id="62ccb-109">必须遵守以下过程顺序，并确保 Finance and Operations 和 Common Data Service 中均有初始数据。</span><span class="sxs-lookup"><span data-stu-id="62ccb-109">You must follow the following order of precedence and make sure that the initial data is available on both Finance and Operations and Common Data Service.</span></span>   

## <a name="vendor"></a><span data-ttu-id="62ccb-110">供应商</span><span class="sxs-lookup"><span data-stu-id="62ccb-110">Vendor</span></span>

<span data-ttu-id="62ccb-111">下面是针对供应商的执行顺序：</span><span class="sxs-lookup"><span data-stu-id="62ccb-111">The order of execution for Vendor is:</span></span>

```
Vendor Group
    Terms of payment
        Payment day & lines
        Payment schedule
Vendor payment method
```

## <a name="customer-organization"></a><span data-ttu-id="62ccb-112">客户（组织）</span><span class="sxs-lookup"><span data-stu-id="62ccb-112">Customer (Organization)</span></span>

<span data-ttu-id="62ccb-113">下面是针对客户的执行顺序：</span><span class="sxs-lookup"><span data-stu-id="62ccb-113">The order of execution for Customer is:</span></span>

```
Customer Group
    Terms of payment
        Payment day & lines
        Payment 
Customer payment method
```

## <a name="contact-person"></a><span data-ttu-id="62ccb-114">联系人（个人）</span><span class="sxs-lookup"><span data-stu-id="62ccb-114">Contact (Person)</span></span>

<span data-ttu-id="62ccb-115">下面是针对联系人的执行顺序：</span><span class="sxs-lookup"><span data-stu-id="62ccb-115">The order of execution for Contact is:</span></span>

```
Customer
Vendor               
```
