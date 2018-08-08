---
title: "成本对象维度"
description: "在分析成本时，使用成本元素维度确定成本流向。 您可以使用成本对象维度确定应在何处分配成本。。 本主题提供了有关成本对象维度的信息。"
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMDimensionMember
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 223174
ms.assetid: 2a1cdd35-30cb-41e7-9506-67fd04a537c5
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 60a6575387a6ebe3b349a61368a7561d78dc69f3
ms.contentlocale: zh-cn
ms.lasthandoff: 08/07/2018

---

# <a name="cost-object-dimensions"></a><span data-ttu-id="bd33b-105">成本对象维度</span><span class="sxs-lookup"><span data-stu-id="bd33b-105">Cost object dimensions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bd33b-106">在分析成本时，使用成本元素维度确定成本流向。</span><span class="sxs-lookup"><span data-stu-id="bd33b-106">When you analyze costs, you use cost element dimensions to determine where costs flow to.</span></span> <span data-ttu-id="bd33b-107">您可以使用成本对象维度确定应在何处分配成本。。</span><span class="sxs-lookup"><span data-stu-id="bd33b-107">You use cost object dimensions to determine where you should assign costs.</span></span> <span data-ttu-id="bd33b-108">本主题提供了有关成本对象维度的信息。</span><span class="sxs-lookup"><span data-stu-id="bd33b-108">This topic provides information about cost object dimensions.</span></span>

<span data-ttu-id="bd33b-109">成本对象可以是您要估计、分配成本或直接衡量的任何对象类型。</span><span class="sxs-lookup"><span data-stu-id="bd33b-109">A cost object can be any type of object that you want to estimate, allocate costs to, or measure directly.</span></span> <span data-ttu-id="bd33b-110">典型的成本对象包括产品、项目、资源、部门、成本中心和地理区域。</span><span class="sxs-lookup"><span data-stu-id="bd33b-110">Typical cost objects include products, projects, resources, departments, cost centers, and geographical regions.</span></span> <span data-ttu-id="bd33b-111">管理层使用成本对象量化成本，也推动盈利分析。</span><span class="sxs-lookup"><span data-stu-id="bd33b-111">Management uses cost objects to quantify costs and also to drive profitability analysis.</span></span>

## <a name="cost-object-dimensions-and-cost-object-dimension-members"></a><span data-ttu-id="bd33b-112">成本对象维度和成本对象维度成员</span><span class="sxs-lookup"><span data-stu-id="bd33b-112">Cost object dimensions and cost object dimension members</span></span>
<span data-ttu-id="bd33b-113">成本对象被称为“*成本对象维度*”。</span><span class="sxs-lookup"><span data-stu-id="bd33b-113">Cost objects are known as *cost object dimensions*.</span></span> <span data-ttu-id="bd33b-114">在您决定成本对象维度应引用哪个实体后，您必须指定单独的维度值或者将它们从其他源系统导入到成本核算中。</span><span class="sxs-lookup"><span data-stu-id="bd33b-114">After you’ve decided which entity the cost object dimension should refer to, you must specify the individual dimension values or import them into Cost accounting from other source systems.</span></span> <span data-ttu-id="bd33b-115">这些单独的维度值被称为“*成本对象维度成员*”。</span><span class="sxs-lookup"><span data-stu-id="bd33b-115">These individual dimension values are known as *cost object dimension members*.</span></span> <span data-ttu-id="bd33b-116">例如，您要使用名为“成本中心”的财务维度作为成本对象维度。</span><span class="sxs-lookup"><span data-stu-id="bd33b-116">For example, you want to use the financial dimension that is named Cost center as the cost object dimension.</span></span> <span data-ttu-id="bd33b-117">要查看成本如何流向各个成本中心，您必须导入成本对象维度成员。</span><span class="sxs-lookup"><span data-stu-id="bd33b-117">To see how costs flow to the individual cost centers, you must import the cost object dimension members.</span></span> <span data-ttu-id="bd33b-118">在这种情况下，成本对象维度成员是实际成本中心，例如销售、生产、管理和地理位置。</span><span class="sxs-lookup"><span data-stu-id="bd33b-118">In this case, the cost object dimension members are the actual cost centers, such as Sales, Production, Administration, and Geographic locations.</span></span> <span data-ttu-id="bd33b-119">以下屏幕截图举例说明了作为成本对象维度的成本中心及其作为成本对象维度成员的实际成本中心。</span><span class="sxs-lookup"><span data-stu-id="bd33b-119">The following screenshot shows an example of Cost Centers as the cost object dimension with its actual cost centers as cost object dimension members.</span></span> 

<span data-ttu-id="bd33b-120">[![成本对象维度](./media/cost-object-dimensions.png)](./media/cost-object-dimensions.png)</span><span class="sxs-lookup"><span data-stu-id="bd33b-120">[![cost-object-dimensions](./media/cost-object-dimensions.png)](./media/cost-object-dimensions.png)</span></span>

## <a name="import-cost-object-dimension-members-through-data-connectors"></a><span data-ttu-id="bd33b-121">通过数据连接器导入成本对象维度成员</span><span class="sxs-lookup"><span data-stu-id="bd33b-121">Import cost object dimension members through data connectors</span></span>
<span data-ttu-id="bd33b-122">要更加轻松地导入成本对象维度成员，您可以使用数据连接器从您要作为成本对象维度使用的实体中检索值。</span><span class="sxs-lookup"><span data-stu-id="bd33b-122">To make the import of cost object dimension members easier, you use data connectors to retrieve the values from the entities that you want to use as cost object dimensions.</span></span> <span data-ttu-id="bd33b-123">您可以使用预构建的数据连接器或您构建的自定义数据连接器。</span><span class="sxs-lookup"><span data-stu-id="bd33b-123">You can use either the pre-built data connectors or custom data connectors that you build.</span></span>




