--- 
title: "创建工作类"
description: "该过程会显示如何设置工作类。"
author: BibiSp
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 9a775366bdaecb59a375f245f7a4d17a659cab11
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-work-class"></a><span data-ttu-id="501f7-103">创建工作类</span><span class="sxs-lookup"><span data-stu-id="501f7-103">Create a work class</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="501f7-104">该过程会显示如何设置工作类。</span><span class="sxs-lookup"><span data-stu-id="501f7-104">This procedure shows you how to set up a work class.</span></span> <span data-ttu-id="501f7-105">工作类用于处理和/或限制工作指令行的类型，以便仓库工作人员可以在移动设备上进行处理。</span><span class="sxs-lookup"><span data-stu-id="501f7-105">Work classes are used to direct and/or limit the type of work order lines that a warehouse worker can process on a mobile device.</span></span> <span data-ttu-id="501f7-106">可以藉由仓库工作人员可以访问的移动设备菜单项上的工作类和工作行上指定的工作类，确定工作人员可以处理的行。</span><span class="sxs-lookup"><span data-stu-id="501f7-106">The lines that a worker can process are determined from the work classes on the mobile device menu items that the warehouse worker has access to and the work class that’s specified on the work lines.</span></span> <span data-ttu-id="501f7-107">工作类还可用于验证工作指令行的存放位置。</span><span class="sxs-lookup"><span data-stu-id="501f7-107">Work classes can also be used to validate the put location for a work order line.</span></span> <span data-ttu-id="501f7-108">您可以使用 USMF 公司演示数据，也可使用您自己的数据运行该过程。</span><span class="sxs-lookup"><span data-stu-id="501f7-108">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="501f7-109">该过程专门面向仓库经理。</span><span class="sxs-lookup"><span data-stu-id="501f7-109">This procedure is intended for the warehouse manager.</span></span>

1. <span data-ttu-id="501f7-110">转到“仓库管理”>“设置”>“工作”>“工作类”。</span><span class="sxs-lookup"><span data-stu-id="501f7-110">Go to Warehouse management > Setup > Work > Work classes.</span></span>
2. <span data-ttu-id="501f7-111">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="501f7-111">Click New.</span></span>
3. <span data-ttu-id="501f7-112">在“工作类 ID”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="501f7-112">In the Work class ID field, type a value.</span></span>
4. <span data-ttu-id="501f7-113">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="501f7-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="501f7-114">在“工作订单类型”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="501f7-114">In the Work order type field, select an option.</span></span>
6. <span data-ttu-id="501f7-115">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="501f7-115">Click New.</span></span>
7. <span data-ttu-id="501f7-116">在“位置类型”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="501f7-116">In the Location type field, type a value.</span></span>
    * <span data-ttu-id="501f7-117">如果您选择某一位置类型，即会限制物料在领取后的存放位置。</span><span class="sxs-lookup"><span data-stu-id="501f7-117">If you select a location type, this sets a restriction on where items can be put after they’ve been picked.</span></span> <span data-ttu-id="501f7-118">在位置指令尝试决定位置时，使用该设置，或者如果仓管人员手动提供移动设备菜单项的位置。</span><span class="sxs-lookup"><span data-stu-id="501f7-118">This setting is used when a location directive tries to resolve the location, or if a warehouse worker manually provides the location for the mobile device menu item.</span></span>  
8. <span data-ttu-id="501f7-119">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="501f7-119">Close the page.</span></span>

