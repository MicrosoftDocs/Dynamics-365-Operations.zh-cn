---
title: "创建生产订单"
description: "在创建生产订单时，将发起开始生产物料的请求。 生产订单包含与将生产的产品、生产数量和计划完工日期有关的信息。 它还包含要消耗的物料以及要用于生产物料的流程的信息。"
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdTable, ProdTableCreate
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19741
ms.assetid: bbb6e69d-479c-45fc-a0a8-66da5df16c7f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: d6b35c347aad64a44e827ecb86273f4767d8afd3
ms.contentlocale: zh-cn
ms.lasthandoff: 05/08/2018

---

# <a name="create-production-orders"></a><span data-ttu-id="62663-105">创建生产订单</span><span class="sxs-lookup"><span data-stu-id="62663-105">Create production orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="62663-106">在创建生产订单时，将发起开始生产物料的请求。</span><span class="sxs-lookup"><span data-stu-id="62663-106">When a production order is created, a request is initiated to start producing an item.</span></span> <span data-ttu-id="62663-107">生产订单包含与将生产的产品、生产数量和计划完工日期有关的信息。</span><span class="sxs-lookup"><span data-stu-id="62663-107">The production order contains information about what will be produced, the quantity to produce, and the planned finish date.</span></span> <span data-ttu-id="62663-108">它还包含要消耗的物料以及要用于生产物料的流程的信息。</span><span class="sxs-lookup"><span data-stu-id="62663-108">It also contains information about which materials to consume and which process to follow to produce the item.</span></span>

<span data-ttu-id="62663-109">生产订单在生产生命周期的各个阶段中传递。</span><span class="sxs-lookup"><span data-stu-id="62663-109">A production order passes through stages of the production life cycle.</span></span> <span data-ttu-id="62663-110">在创建一个订单后，会将状态**“已创建”**分配给该订单。</span><span class="sxs-lookup"><span data-stu-id="62663-110">When an order is created, it is assigned the status **Created**.</span></span> <span data-ttu-id="62663-111">在完成一个订单后，会将状态**“已结束”**分配给该订单。</span><span class="sxs-lookup"><span data-stu-id="62663-111">When an order is finished, it is assigned the status **Ended**.</span></span> <span data-ttu-id="62663-112">每个阶段中的参数设置允许用户配置每个步骤。</span><span class="sxs-lookup"><span data-stu-id="62663-112">A parameter setting in each stage allows a user to configure each step.</span></span> <span data-ttu-id="62663-113">可以为单个用户或为所有用户指定该设置。</span><span class="sxs-lookup"><span data-stu-id="62663-113">The setting can be set up for a single user or for all users.</span></span>

<span data-ttu-id="62663-114">生产物料清单和生产工艺路线是生产订单的主要实体。</span><span class="sxs-lookup"><span data-stu-id="62663-114">The production bill of material and the production route are the main entities of the production order.</span></span> <span data-ttu-id="62663-115">它们基于要生产的选定物料和数量复制到生产订单。</span><span class="sxs-lookup"><span data-stu-id="62663-115">They are copied to the production order based on the selected item and quantity that are going to be produced.</span></span> <span data-ttu-id="62663-116">在启动生产订单之前，生产物料清单和工艺路线是可以编辑的。</span><span class="sxs-lookup"><span data-stu-id="62663-116">Before the production order is started, the production bill of material and route can be edited.</span></span>

<span data-ttu-id="62663-117">在以下情况下可以创建生产订单：</span><span class="sxs-lookup"><span data-stu-id="62663-117">A production order can be created in the following scenarios:</span></span>

-   <span data-ttu-id="62663-118">由主规划执行基于物料需求创建。</span><span class="sxs-lookup"><span data-stu-id="62663-118">Created by master planning execution based on material demand.</span></span>
-   <span data-ttu-id="62663-119">从销售订单行直接创建，或在创建和估计更高级别的生产订单（限定供应）时创建。</span><span class="sxs-lookup"><span data-stu-id="62663-119">Created directly from a sales order line or when a higher-level production order is created and estimated (pegged supply).</span></span>
-   <span data-ttu-id="62663-120">手动创建。</span><span class="sxs-lookup"><span data-stu-id="62663-120">Created manually.</span></span>





