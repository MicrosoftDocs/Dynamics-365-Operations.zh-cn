---
title: 定义资源功能
description: 资源功能描述了运营资源可执行的内容。
author: sorenva
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WrkCtrCapability
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 072991e7b3844ad3583b7d0c575d426299f74e9f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828698"
---
# <a name="define-resource-capabilities"></a><span data-ttu-id="ad079-103">定义资源功能</span><span class="sxs-lookup"><span data-stu-id="ad079-103">Define resource capabilities</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ad079-104">资源功能描述了运营资源可执行的内容。</span><span class="sxs-lookup"><span data-stu-id="ad079-104">Resource capabilities describe what operations resources can do.</span></span> <span data-ttu-id="ad079-105">在安排期间，每个工作和操作的要求都将与可用资源的功能相匹配。</span><span class="sxs-lookup"><span data-stu-id="ad079-105">During scheduling, the requirements of each job and operation are matched against the capabilities of the available resources.</span></span> <span data-ttu-id="ad079-106">该任务指南将帮助您创建资源功能并其分配给资源。</span><span class="sxs-lookup"><span data-stu-id="ad079-106">This task guide will help you create a resource capability and assign it to a resource.</span></span> <span data-ttu-id="ad079-107">创建此任务的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="ad079-107">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-resource-capability"></a><span data-ttu-id="ad079-108">创建资源功能</span><span class="sxs-lookup"><span data-stu-id="ad079-108">Create a resource capability</span></span>
1. <span data-ttu-id="ad079-109">转到“资源功能”。</span><span class="sxs-lookup"><span data-stu-id="ad079-109">Go to Resource capabilities.</span></span>
2. <span data-ttu-id="ad079-110">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="ad079-110">Click New.</span></span>
3. <span data-ttu-id="ad079-111">在“功能”字段中，键入资源功能的 ID。</span><span class="sxs-lookup"><span data-stu-id="ad079-111">In the Capability field, type the ID of the resource capability.</span></span>
    * <span data-ttu-id="ad079-112">对于特定工序，请使用功能 ID 指定必须具有此功能才能执行操作的资源。</span><span class="sxs-lookup"><span data-stu-id="ad079-112">For a given operation, you use the capability ID to specify that resources must have this capability to perform the operation.</span></span>  
4. <span data-ttu-id="ad079-113">在“描述”字段中，输入功能的描述。</span><span class="sxs-lookup"><span data-stu-id="ad079-113">In the Description field, enter a description of the capability.</span></span>

## <a name="assign-capability-to-a-resource"></a><span data-ttu-id="ad079-114">将功能分配给资源</span><span class="sxs-lookup"><span data-stu-id="ad079-114">Assign capability to a resource</span></span>
1. <span data-ttu-id="ad079-115">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="ad079-115">Click Add.</span></span>
2. <span data-ttu-id="ad079-116">在“资源”字段中，键入资源功能的 ID。</span><span class="sxs-lookup"><span data-stu-id="ad079-116">In the Resource field, type the ID of the resource.</span></span>
    * <span data-ttu-id="ad079-117">资源功能可分配给一个或多个资源。</span><span class="sxs-lookup"><span data-stu-id="ad079-117">A resource capability can be assigned to one or more resources.</span></span>  
3. <span data-ttu-id="ad079-118">在“截止日期”字段，输入日期。</span><span class="sxs-lookup"><span data-stu-id="ad079-118">In the Expiration field, enter a date.</span></span>
    * <span data-ttu-id="ad079-119">您可以使用该字段指定某个资源只在限定时间内具有此功能。</span><span class="sxs-lookup"><span data-stu-id="ad079-119">You can use this field to specify that a resource has the capability for only a limited time.</span></span>  
4. <span data-ttu-id="ad079-120">在“优先”字段，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="ad079-120">In the Priority field, enter a number.</span></span>
    * <span data-ttu-id="ad079-121">在安排工作和操作时，可以指定是否按优先级选择资源。</span><span class="sxs-lookup"><span data-stu-id="ad079-121">When you schedule jobs and operations, you can specify whether to select resources by priority.</span></span> <span data-ttu-id="ad079-122">如果您按优先级选择资源，并且在请求日期之前有多个可执行该工作或操作的资源，则根据所要求的功能选择最低优先级的资源。</span><span class="sxs-lookup"><span data-stu-id="ad079-122">If you choose to do this, and more than one resource can perform the job or operation by the requested date, the resource that has the lowest priority with respect to the required capability is selected.</span></span>  
5. <span data-ttu-id="ad079-123">在“水平”字段，输入一个数值。</span><span class="sxs-lookup"><span data-stu-id="ad079-123">In the Level field, enter a number.</span></span>
    * <span data-ttu-id="ad079-124">当您指定某项工作或操作需要某种特定功能，您还可以指定所需功能的最低水平。</span><span class="sxs-lookup"><span data-stu-id="ad079-124">When you specify that a job or operation requires a particular capability, you can also specify the minimum level that is required.</span></span> <span data-ttu-id="ad079-125">使用功能级别区分资源可以根据不同的速度、力量、大小等执行同类工作。</span><span class="sxs-lookup"><span data-stu-id="ad079-125">Use the capability level to differentiate resources that can perform the same job, but at different speeds, strengths, sizes, and so on.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]