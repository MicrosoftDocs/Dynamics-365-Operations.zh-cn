---
title: "虚拟物料"
description: "此主题详细介绍如何在 Microsoft Dynamics 365 for Finance and Operations 中的物料清单 (BOM) 和配方的行中使用虚拟行类型。"
author: ShylaThompson
manager: AnnBe
ms.date: 06/15/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.search.region: Global
ms.author: shylaw
ms.search.validfrom: 
ms.dyn365.ops.version: 8.1
ms.translationtype: HT
ms.sourcegitcommit: c5d4fb53939d88fcb1bd83d70bc361ed9879f298
ms.openlocfilehash: a92dd82f309867586f047e0dfc36e452a44a0f9c
ms.contentlocale: zh-cn
ms.lasthandoff: 10/01/2018

---

# <a name="phantom-items"></a><span data-ttu-id="4111d-103">虚拟物料</span><span class="sxs-lookup"><span data-stu-id="4111d-103">Phantom items</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4111d-104">此主题详细介绍如何在物料清单 (BOM) 和配方的行中使用虚拟行类型。</span><span class="sxs-lookup"><span data-stu-id="4111d-104">This topic describes, in detail, how the Phantom line type can be used for the lines of a bill of materials (BOM) and a formula.</span></span> <span data-ttu-id="4111d-105">在下图中，(a) 是产品 H 和部件 F 和 G 的物料清单，而 (b) 则是产品 H 和部件 F 的工艺路线单。</span><span class="sxs-lookup"><span data-stu-id="4111d-105">In the following illustration, (a) is the BOM for product H and parts F and G, and (b) is the route sheet for products H and part F.</span></span>

![产品 H 和部件 F](media/product-H-part-F.png)


<span data-ttu-id="4111d-107">此图显示的示例为分两个级别的物料清单结构。</span><span class="sxs-lookup"><span data-stu-id="4111d-107">This illustration shows an example of a BOM structure in two levels.</span></span> <span data-ttu-id="4111d-108">成品 H 表示需要进行机器装配的产品。</span><span class="sxs-lookup"><span data-stu-id="4111d-108">Finished product H represents a product for a machine assembly.</span></span> <span data-ttu-id="4111d-109">这个机器装配由两个部件、一个含两种物料（A 和 B）的电子单元 (F)，以及也含两种材料（C 和 D）的一组包装材料构成。</span><span class="sxs-lookup"><span data-stu-id="4111d-109">The machine assembly consists of two parts, an electrical unit (F) that has two materials (A and B) and a group of packaging materials (G) that also has two materials (C and D).</span></span> <span data-ttu-id="4111d-110">另一种材料 (E) 则在常规装配该机器时使用。</span><span class="sxs-lookup"><span data-stu-id="4111d-110">Another material (E) is used during the general assembly of the machine.</span></span>

![产品 H 和部件 F](media/product-H-part-B.png)

<span data-ttu-id="4111d-112">上图表示产品 H 的工程物料清单。此结构很好地囊括了整个机器装配的部件和组件。</span><span class="sxs-lookup"><span data-stu-id="4111d-112">The preceding illustration represents the Engineering BOM for product H. This structure provides a good overview of the parts and components of the overall machine assembly.</span></span> <span data-ttu-id="4111d-113">但是，尽管产品设计师可能希望以这种方式表示物料清单，此结构可能无法正确地表示机器在车间中是如何制造地。</span><span class="sxs-lookup"><span data-stu-id="4111d-113">However, although product designers might prefer to see the BOM represented in this way, this structure might not correctly represent the way that the machine is built on the shop floor.</span></span> 

<span data-ttu-id="4111d-114">例如，上图中的工程物料清单指示电子单元 F 作为单独工作订单中的独立部件进行装配。</span><span class="sxs-lookup"><span data-stu-id="4111d-114">For example, the Engineering BOM in the preceding illustration indicates that electrical unit F is assembled as a separate part on a separate work order.</span></span> <span data-ttu-id="4111d-115">但是在车间中，可能根据判断最好是将该电子单元作为整个机器装配的一部分进行装配，而不是作为单独的工作订单进行装配。</span><span class="sxs-lookup"><span data-stu-id="4111d-115">However, on the shop floor, it might be judged more optimal to assemble the electrical unit as part of the overall machine assembly, not as a separate work order.</span></span>

<span data-ttu-id="4111d-116">工程物料清单还指示部件 G 是一个单独的部件。</span><span class="sxs-lookup"><span data-stu-id="4111d-116">This Engineering BOM also indicates that part G is a separate part.</span></span> <span data-ttu-id="4111d-117">但是在此结构中，部件 G 表示的不是一个物理部件，而是包装材料的集合。</span><span class="sxs-lookup"><span data-stu-id="4111d-117">However, in this structure, part G doesn’t represent a physical part but a collection of packaging materials.</span></span> 

<span data-ttu-id="4111d-118">因此，尽管工程物料清单对设计产品和保持该设计很有价值，可能并不是最具有逻辑性的产品制造执行过程支持方式。</span><span class="sxs-lookup"><span data-stu-id="4111d-118">Therefore, although an Engineering BOM provides great value for the design of a product and maintenance of that design, it might not be the most logical way to support the manufacturing execution process of the product.</span></span> <span data-ttu-id="4111d-119">相对而言，制造物料清单则最适合制造产品。</span><span class="sxs-lookup"><span data-stu-id="4111d-119">By contrast, a Manufacturing BOM represents the best way to build a product.</span></span>

<span data-ttu-id="4111d-120">下图显示如何将上面的工程物料清单转换为制造物料清单。</span><span class="sxs-lookup"><span data-stu-id="4111d-120">The following illustration shows how the preceding Engineering BOM is transitioned into a Manufacturing BOM.</span></span> <span data-ttu-id="4111d-121">在该图中，(a) 是产品 H 的物料清单，而 b 则是产品 H 的工艺路线单。</span><span class="sxs-lookup"><span data-stu-id="4111d-121">In this illustration, (a) is the BOM for product H, and b is the route sheet for product H.</span></span>

<span data-ttu-id="4111d-122">在此结构中，可看到部件 F 和 G 没有标注，而这些部件所含材料尚未升级到下一个物料清单级别。</span><span class="sxs-lookup"><span data-stu-id="4111d-122">In this structure, you can see that there is no notion of parts F and G, and the materials that these parts consist of have been elevated to the next BOM level.</span></span> 

<span data-ttu-id="4111d-123">与工程物料清单不同（这种清单有两个工序单），制造物料清单只有一个工序单。</span><span class="sxs-lookup"><span data-stu-id="4111d-123">Unlike the Engineering BOM, which had two operations sheets, the Manufacturing BOM has only one operations sheet.</span></span> <span data-ttu-id="4111d-124">链接到部件 G 的包装工序也已升级，现在是产品 H 的工序单的一部分。第一个工序是装配电子单元。</span><span class="sxs-lookup"><span data-stu-id="4111d-124">The packaging operation that was linked to part G has also been elevated and is now part of the operations sheet for product H. The assembly of the electrical unit is the first operation.</span></span> <span data-ttu-id="4111d-125">这个顺序很有道理，因为下一个工序（即机器装配）中将使用该单元。</span><span class="sxs-lookup"><span data-stu-id="4111d-125">This order makes good sense, because this unit is used in the next operation, which is the machine assembly.</span></span> <span data-ttu-id="4111d-126">最后一个工序是包装工序，会用到两种包装材料（C 和 D）。</span><span class="sxs-lookup"><span data-stu-id="4111d-126">The last operation is the packaging operation, which consumes two packing materials (C and D).</span></span>

<span data-ttu-id="4111d-127">在 Microsoft Dynamics 365 for Finance and Operations 中，通过虚拟物料清单行类型实现工程物料清单与制造物料清单之间的转换。</span><span class="sxs-lookup"><span data-stu-id="4111d-127">In Microsoft Dynamics 365 for Finance and Operations, the transition between the Engineering BOM and the Manufacturing BOM is enabled through the Phantom BOM line type.</span></span> <span data-ttu-id="4111d-128">就像术语“虚拟”的含义所示，两种物料清单类型转换期间，部件 F 和 G 已消失。</span><span class="sxs-lookup"><span data-stu-id="4111d-128">As the term “phantom” indicates, parts F and G have disappeared during the transition between the two BOM types.</span></span> <span data-ttu-id="4111d-129">在此示例中，虚拟行类型应用于工程物料清单中部件 F 和 G 的物料清单行。</span><span class="sxs-lookup"><span data-stu-id="4111d-129">In this example, the Phantom line type is applied to the BOM lines for parts F and G in the Engineering BOM.</span></span> <span data-ttu-id="4111d-130">创建生产订单或批处理订单时，将把工程物料清单复制到生产订单或批处理订单。</span><span class="sxs-lookup"><span data-stu-id="4111d-130">When a production or batch order is created, the Engineering BOM is copied to the production or batch order.</span></span> <span data-ttu-id="4111d-131">然后，估计订单时，将从工程物料清单转换为制造物料清单，如上面的图中所示。</span><span class="sxs-lookup"><span data-stu-id="4111d-131">Then, when the order is estimated, the transition from the Engineering BOM to the Manufacturing BOM occurs, as shown in the preceding illustrations.</span></span> <span data-ttu-id="4111d-132">从第二个图中的工序单开始，包装材料 C 和 D 是工序的输入。</span><span class="sxs-lookup"><span data-stu-id="4111d-132">From the operations sheet in the second illustration, packaging materials C and D are input for the operation.</span></span> 

## <a name="multilevel-phantom-bom-structures"></a><span data-ttu-id="4111d-133">多级虚拟物料清单结构</span><span class="sxs-lookup"><span data-stu-id="4111d-133">Multilevel phantom BOM structures</span></span>
<span data-ttu-id="4111d-134">可以在多级虚拟物料清单结构中使用虚拟行类型，如下图中所示。</span><span class="sxs-lookup"><span data-stu-id="4111d-134">The Phantom line type can be used in multilevel BOM structures, as shown in the following illustration.</span></span> <span data-ttu-id="4111d-135">在该图中，(a) 是产品 G 的物料清单，而 (b) 则是部件 E 和 F 及产品 G 的工艺路线单。</span><span class="sxs-lookup"><span data-stu-id="4111d-135">In this illustration, (a) is the BOM for product G, and (b) is the route sheet for parts E and F and product G.</span></span> 

![带工艺路线单的产品 G 和部件 F](media/product-G-route-sheet-G.png)


<span data-ttu-id="4111d-137">下图显示配置了部件 E 和 F 的物料清单行以便让行类型为虚拟时生成的制造物料清单和工艺路线单。</span><span class="sxs-lookup"><span data-stu-id="4111d-137">The following illustration shows the resulting Manufacturing BOM and route sheet if the BOM lines for parts E and F are configured so that the line type is Phantom.</span></span> <span data-ttu-id="4111d-138">在该图中，(a) 是产品 G 的物料清单，而 (b) 则是产品 G 的工艺路线单。</span><span class="sxs-lookup"><span data-stu-id="4111d-138">In this illustration, (a) is the BOM for product G, and (b) is the route sheet for product G.</span></span>

![产品 G](media/product-G.png)


## <a name="phantom-and-route-network"></a><span data-ttu-id="4111d-140">虚拟和工艺路线网络</span><span class="sxs-lookup"><span data-stu-id="4111d-140">Phantom and route network</span></span>
<span data-ttu-id="4111d-141">也可以将虚拟物料清单用于具有工艺路线网络的物料清单。</span><span class="sxs-lookup"><span data-stu-id="4111d-141">Phantom BOMs can also be used for a BOM that has a route network.</span></span> <span data-ttu-id="4111d-142">在工艺路线网络中，一个或多个工序同时运行。</span><span class="sxs-lookup"><span data-stu-id="4111d-142">In a route network, one or more operations run in parallel.</span></span> <span data-ttu-id="4111d-143">下图显示多级物料清单中使用的工艺路线网络的示例。</span><span class="sxs-lookup"><span data-stu-id="4111d-143">The following illustration shows an example of a route network that is used in a multilevel BOM.</span></span> <span data-ttu-id="4111d-144">在该图中，(a) 是产品 G 和部件 F 的物料清单，而 (b) 则是产品 G 和部件 F 的工艺路线单，后者具有工艺路线网络。</span><span class="sxs-lookup"><span data-stu-id="4111d-144">In this illustration, (a) is the BOM for product G and part F, and (b) is the route sheet for product G and part F, which has a route network.</span></span>

![产品 G 和部件 F](media/product-G-part-F.png)


<span data-ttu-id="4111d-146">在下图中，(a) 是产品 G 和部件 F 的物料清单，而 (b) 则是产品 G 和部件 F 的工艺路线单。</span><span class="sxs-lookup"><span data-stu-id="4111d-146">In the following illustration, (a) is the BOM for product G and part F, and (b) is the route sheet for product G and part F.</span></span>

![带工艺路线单的产品 G 和部件 F](media/product-G-part-F-with-route-sheet.png)

