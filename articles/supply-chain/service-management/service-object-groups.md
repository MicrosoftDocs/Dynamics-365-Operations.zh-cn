---
title: "服务对象组"
description: "对象组有用于排序和筛选有关报告和统计对象的数据。"
author: YuyuScheller
manager: AnnBe
ms.date: 05/11/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceObjectGroups
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 2ab3ed8a8f36f980473b17b5dfed8cb3d0054253
ms.contentlocale: zh-cn
ms.lasthandoff: 05/08/2018

---

# <a name="service-object-groups"></a><span data-ttu-id="44416-103">服务对象组</span><span class="sxs-lookup"><span data-stu-id="44416-103">Service object groups</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="44416-104">对象组有用于排序和筛选有关报告和统计对象的数据。</span><span class="sxs-lookup"><span data-stu-id="44416-104">Object groups are useful for sorting and filtering the data about objects for reports and statistics.</span></span> <span data-ttu-id="44416-105">例如，您可以按地理位置或按类型对对象进行分组。</span><span class="sxs-lookup"><span data-stu-id="44416-105">For example, you can group objects by geographical location or by type.</span></span>

## <a name="group-by-geographical-location"></a><span data-ttu-id="44416-106">按地理位置分组</span><span class="sxs-lookup"><span data-stu-id="44416-106">Group by geographical location</span></span>

<span data-ttu-id="44416-107">您可以使用此分组方法来显示您的公司服务定位的各种不同对象的位置。</span><span class="sxs-lookup"><span data-stu-id="44416-107">You can use this grouping method to show where the various different objects that your company services are located.</span></span> <span data-ttu-id="44416-108">例如，如果您必须标识在特定国家/地区或区域的您的公司已为其提供服务的对象，则按地理位置对对象进行分组也是有用的。</span><span class="sxs-lookup"><span data-stu-id="44416-108">Grouping objects by geographical location can also be useful if, for example, you must identify the objects that your company already provides services for in a particular country/region.</span></span>

## <a name="example"></a><span data-ttu-id="44416-109">示例</span><span class="sxs-lookup"><span data-stu-id="44416-109">Example</span></span>

<span data-ttu-id="44416-110">比利时的一位客户向您的呼叫中心致电，希望为对象 ABC 创建一个服务协议。</span><span class="sxs-lookup"><span data-stu-id="44416-110">A customer from Belgium calls your service center and wants to create a service agreement for an object, ABC.</span></span> <span data-ttu-id="44416-111">您已将地理位置为比利时的对象组附加到比利时中服务的所有对象。</span><span class="sxs-lookup"><span data-stu-id="44416-111">You have attached an object group for geographical location, Belgium, to all objects that are serviced in Belgium.</span></span> <span data-ttu-id="44416-112">通过使用此组作为筛选器，您可以快速搜索以查看您是否以在计划中拥有 ABC 记录，或您是否必须设置一个新对象。</span><span class="sxs-lookup"><span data-stu-id="44416-112">By using this group as a filter, you can quickly search to see whether you already have a record for ABC in the program, or whether you must set up a new object.</span></span> 

## <a name="group-by-type"></a><span data-ttu-id="44416-113">按类型分组</span><span class="sxs-lookup"><span data-stu-id="44416-113">Group by type</span></span>

<span data-ttu-id="44416-114">您可以使用此分组方法以显示您的公司服务的对象的类型。</span><span class="sxs-lookup"><span data-stu-id="44416-114">You can use this grouping method to show the types of objects that your company services.</span></span> <span data-ttu-id="44416-115">例如，如果您要基于已存在于计划中的类似对象来创建新对象，则按类型对对象进行分组也会很有用。</span><span class="sxs-lookup"><span data-stu-id="44416-115">Grouping objects by type can also be useful if, for example, you want to create a new object based on similar objects that already exist in the program.</span></span>

## <a name="example"></a><span data-ttu-id="44416-116">示例</span><span class="sxs-lookup"><span data-stu-id="44416-116">Example</span></span>

<span data-ttu-id="44416-117">一个客户致电并想要为空调机器 HIJ 设置一个服务协议。</span><span class="sxs-lookup"><span data-stu-id="44416-117">A customer calls and wants to set up a service agreement for an air conditioning machine, HIJ.</span></span> <span data-ttu-id="44416-118">您还没有此机器的记录。</span><span class="sxs-lookup"><span data-stu-id="44416-118">You do not already have a record for this machine.</span></span> <span data-ttu-id="44416-119">但是，您设置了名为“空调”的对象组，而且您已将此组附加到了所有空调对象。</span><span class="sxs-lookup"><span data-stu-id="44416-119">However, you have set up an object group titled Air Conditioners, and you have attached this group to all air conditioning objects.</span></span> <span data-ttu-id="44416-120">因此，您可以快速搜索并标识所有其他空调器并使用来自这些对象的模板信息以为 HIJ 创建服务协议行。</span><span class="sxs-lookup"><span data-stu-id="44416-120">Therefore, you can quickly search for and identify all other air conditioning machines and use the template information from these objects to create service agreement lines for HIJ.</span></span> <span data-ttu-id="44416-121">通过以这种方式使用对象组，您可以迅速设置新对象并确定必须在这些对象上执行的服务任务。</span><span class="sxs-lookup"><span data-stu-id="44416-121">By using object groups in this manner, you can quickly set up new objects and determine the service tasks that must be performed on them.</span></span> 

## <a name="create-service-object-groups"></a><span data-ttu-id="44416-122">创建服务对象组</span><span class="sxs-lookup"><span data-stu-id="44416-122">Create service object groups</span></span>

<span data-ttu-id="44416-123">创建可将服务对象分配给的组。</span><span class="sxs-lookup"><span data-stu-id="44416-123">Create groups that you can assign service objects to.</span></span> <span data-ttu-id="44416-124">服务对象是执行服务的库存物料和其他产品。</span><span class="sxs-lookup"><span data-stu-id="44416-124">Service objects are inventory items and other products for which services are performed.</span></span> <span data-ttu-id="44416-125">通过对服务对象分组，您可以为类似和相关服务对象创建报表。</span><span class="sxs-lookup"><span data-stu-id="44416-125">By grouping service objects, you can create reports for similar and related service objects.</span></span> <span data-ttu-id="44416-126">例如，服务对象组中可包括两个服务对象：一个服务对象是配套件，第二个服务对象是安装配套件的服务。</span><span class="sxs-lookup"><span data-stu-id="44416-126">For example, a service object group might consist of two service objects: One service object is a kit, and the second service object is the service to install the kit.</span></span>

<span data-ttu-id="44416-127">若要创建服务对象组，请执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="44416-127">To create service object groups, follow these steps:</span></span>

1. <span data-ttu-id="44416-128">单击**服务管理 > 设置 > 服务对象 > 服务对象组**。</span><span class="sxs-lookup"><span data-stu-id="44416-128">Click **Service management > Setup > Service objects > Service object groups**.</span></span>

2. <span data-ttu-id="44416-129">单击**新建**创建一个新的服务对象组。</span><span class="sxs-lookup"><span data-stu-id="44416-129">Click **New** to create a new service object group.</span></span>

3. <span data-ttu-id="44416-130">为该服务对象组输入唯一名称和描述（可选）。</span><span class="sxs-lookup"><span data-stu-id="44416-130">Enter a unique name for the service object group and, optionally, a description.</span></span>

<span data-ttu-id="44416-131">通过使用**服务对象**窗体，您可以将服务对象分配给组。</span><span class="sxs-lookup"><span data-stu-id="44416-131">You can assign service objects to the group by using the **Service objects** form.</span></span> 

## <a name="see-also"></a><span data-ttu-id="44416-132">请参阅</span><span class="sxs-lookup"><span data-stu-id="44416-132">See also</span></span>

[<span data-ttu-id="44416-133">创建服务对象</span><span class="sxs-lookup"><span data-stu-id="44416-133">Create service objects</span></span>](create-service-objects.md)



