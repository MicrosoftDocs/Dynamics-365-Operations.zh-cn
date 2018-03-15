---
title: "服务对象组"
description: "对象组有用于排序和筛选有关报告和统计对象的数据。"
author: YuyuScheller
manager: AnnBe
ms.date: 02/21/2018
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
ms.sourcegitcommit: 221b9dae7e83e7f4a535ac60f2a2011533d7861c
ms.openlocfilehash: fa503ac82286099a0eafc7034d169e165b538e2c
ms.contentlocale: zh-cn
ms.lasthandoff: 02/21/2018

---

# <a name="service-object-groups"></a><span data-ttu-id="e6164-103">服务对象组</span><span class="sxs-lookup"><span data-stu-id="e6164-103">Service object groups</span></span> 

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e6164-104">对象组有用于排序和筛选有关报告和统计对象的数据。</span><span class="sxs-lookup"><span data-stu-id="e6164-104">Object groups are useful for sorting and filtering the data about objects for reports and statistics.</span></span> <span data-ttu-id="e6164-105">例如，您可以按地理位置或按类型对对象进行分组。</span><span class="sxs-lookup"><span data-stu-id="e6164-105">For example, you can group objects by geographical location or by type.</span></span>

## <a name="group-by-geographical-location"></a><span data-ttu-id="e6164-106">按地理位置分组</span><span class="sxs-lookup"><span data-stu-id="e6164-106">Group by geographical location</span></span>

<span data-ttu-id="e6164-107">您可以使用此分组方法来显示您的公司服务定位的各种不同对象的位置。</span><span class="sxs-lookup"><span data-stu-id="e6164-107">You can use this grouping method to show where the various different objects that your company services are located.</span></span> <span data-ttu-id="e6164-108">例如，如果您必须标识在特定国家/地区或区域的您的公司已为其提供服务的对象，则按地理位置对对象进行分组也是有用的。</span><span class="sxs-lookup"><span data-stu-id="e6164-108">Grouping objects by geographical location can also be useful if, for example, you must identify the objects that your company already provides services for in a particular country/region.</span></span>

## <a name="example"></a><span data-ttu-id="e6164-109">示例</span><span class="sxs-lookup"><span data-stu-id="e6164-109">Example</span></span>

<span data-ttu-id="e6164-110">比利时的一位客户向您的呼叫中心致电，希望为对象 ABC 创建一个服务协议。</span><span class="sxs-lookup"><span data-stu-id="e6164-110">A customer from Belgium calls your service center and wants to create a service agreement for an object, ABC.</span></span> <span data-ttu-id="e6164-111">您已将地理位置为比利时的对象组附加到比利时中服务的所有对象。</span><span class="sxs-lookup"><span data-stu-id="e6164-111">You have attached an object group for geographical location, Belgium, to all objects that are serviced in Belgium.</span></span> <span data-ttu-id="e6164-112">通过使用此组作为筛选器，您可以快速搜索以查看您是否以在计划中拥有 ABC 记录，或您是否必须设置一个新对象。</span><span class="sxs-lookup"><span data-stu-id="e6164-112">By using this group as a filter, you can quickly search to see whether you already have a record for ABC in the program, or whether you must set up a new object.</span></span> 

## <a name="group-by-type"></a><span data-ttu-id="e6164-113">按类型分组</span><span class="sxs-lookup"><span data-stu-id="e6164-113">Group by type</span></span>

<span data-ttu-id="e6164-114">您可以使用此分组方法以显示您的公司服务的对象的类型。</span><span class="sxs-lookup"><span data-stu-id="e6164-114">You can use this grouping method to show the types of objects that your company services.</span></span> <span data-ttu-id="e6164-115">例如，如果您要基于已存在于计划中的类似对象来创建新对象，则按类型对对象进行分组也会很有用。</span><span class="sxs-lookup"><span data-stu-id="e6164-115">Grouping objects by type can also be useful if, for example, you want to create a new object based on similar objects that already exist in the program.</span></span>

## <a name="example"></a><span data-ttu-id="e6164-116">示例</span><span class="sxs-lookup"><span data-stu-id="e6164-116">Example</span></span>

<span data-ttu-id="e6164-117">一个客户致电并想要为空调机器 HIJ 设置一个服务协议。</span><span class="sxs-lookup"><span data-stu-id="e6164-117">A customer calls and wants to set up a service agreement for an air conditioning machine, HIJ.</span></span> <span data-ttu-id="e6164-118">您还没有此机器的记录。</span><span class="sxs-lookup"><span data-stu-id="e6164-118">You do not already have a record for this machine.</span></span> <span data-ttu-id="e6164-119">但是，您设置了名为“空调”的对象组，而且您已将此组附加到了所有空调对象。</span><span class="sxs-lookup"><span data-stu-id="e6164-119">However, you have set up an object group titled Air Conditioners, and you have attached this group to all air conditioning objects.</span></span> <span data-ttu-id="e6164-120">因此，您可以快速搜索并标识所有其他空调器并使用来自这些对象的模板信息以为 HIJ 创建服务协议行。</span><span class="sxs-lookup"><span data-stu-id="e6164-120">Therefore, you can quickly search for and identify all other air conditioning machines and use the template information from these objects to create service agreement lines for HIJ.</span></span> <span data-ttu-id="e6164-121">通过以这种方式使用对象组，您可以迅速设置新对象并确定必须在这些对象上执行的服务任务。</span><span class="sxs-lookup"><span data-stu-id="e6164-121">By using object groups in this manner, you can quickly set up new objects and determine the service tasks that must be performed on them.</span></span> 




