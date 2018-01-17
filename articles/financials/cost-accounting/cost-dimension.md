---
title: "创建维度并导入维度成员"
description: "成本核算是一个独立的模块，需要来自其他模块的主数据。"
author: YuyuScheller
manager: AnnBe
ms.date: 09/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 256254
ms.assetid: e1b0a6e3-0c72-4a7d-90e1-20f870c6dbad
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: dbf39ee7f64305596bdc57e9f63fe7a71bb5ecb0
ms.contentlocale: zh-cn
ms.lasthandoff: 01/17/2018

---

# <a name="create-dimensions-and-import-dimension-members"></a><span data-ttu-id="a42aa-103">创建维度并导入维度成员</span><span class="sxs-lookup"><span data-stu-id="a42aa-103">Create dimensions and import dimension members</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a42aa-104">成本核算是一个独立的模块，需要来自其他模块的数据。</span><span class="sxs-lookup"><span data-stu-id="a42aa-104">Cost accounting is an independent module that requires data from other modules.</span></span> <span data-ttu-id="a42aa-105">该数据分为以下类别：</span><span class="sxs-lookup"><span data-stu-id="a42aa-105">This data is categorized into the following:</span></span>

-  <span data-ttu-id="a42aa-106">成本元素</span><span class="sxs-lookup"><span data-stu-id="a42aa-106">Cost elements</span></span>
-  <span data-ttu-id="a42aa-107">成本对象</span><span class="sxs-lookup"><span data-stu-id="a42aa-107">Cost objects</span></span>
-  <span data-ttu-id="a42aa-108">统计维度</span><span class="sxs-lookup"><span data-stu-id="a42aa-108">Statistical dimensions</span></span>

<span data-ttu-id="a42aa-109">一个**成本元素**对应于会计科目表的成本相关物料。</span><span class="sxs-lookup"><span data-stu-id="a42aa-109">A **Cost element** corresponds to a cost-relevant item in the chart of accounts.</span></span> <span data-ttu-id="a42aa-110">**成本对象**对应于任何类型的财务维度，例如您要估算、分配成本或直接衡量的产品、成本中心和项目。</span><span class="sxs-lookup"><span data-stu-id="a42aa-110">A **Cost object** corresponds to any type of financial dimension, such as products, cost centers, and projects that you want to estimate, allocate costs to, or measure directly.</span></span> <span data-ttu-id="a42aa-111">**统计维度**及其成员用于登记非货币条目。</span><span class="sxs-lookup"><span data-stu-id="a42aa-111">A **Statistical dimension** and its members are used to register non-monetary entries.</span></span> <span data-ttu-id="a42aa-112">统计维度成员可用作成本分配和成本分摊中的分配基础</span><span class="sxs-lookup"><span data-stu-id="a42aa-112">Statistical dimension members can be used as an allocation base in cost distribution and allocation</span></span> 

<span data-ttu-id="a42aa-113">下图说明在成本核算中使用的维度。</span><span class="sxs-lookup"><span data-stu-id="a42aa-113">The following diagram illustrates the dimensions that are used in Cost accounting.</span></span>

<span data-ttu-id="a42aa-114">[![成本会计维度](./media/cost-eos-dimensions.png)](./media/cost-eos-dimensions.png)</span><span class="sxs-lookup"><span data-stu-id="a42aa-114">[![Cost accounting dimensions](./media/cost-eos-dimensions.png)](./media/cost-eos-dimensions.png)</span></span>

<span data-ttu-id="a42aa-115">在数据导入到成本核算后，您可以使用它生成各种视角，为组织中的所有级别的经理提供见解。</span><span class="sxs-lookup"><span data-stu-id="a42aa-115">After the data is imported into Cost accounting, you can use it to build various perspectives that provide insights to managers at all levels of the organization.</span></span> <span data-ttu-id="a42aa-116">以下主题提供有关创建维度和导入维度成员的信息。</span><span class="sxs-lookup"><span data-stu-id="a42aa-116">The following topics provide information about creating dimensions and importing dimension members.</span></span> 

-  [<span data-ttu-id="a42aa-117">成本元素维度</span><span class="sxs-lookup"><span data-stu-id="a42aa-117">Cost element dimensions</span></span>](cost-elements.md)
-  [<span data-ttu-id="a42aa-118">创建成本元素（任务指南）</span><span class="sxs-lookup"><span data-stu-id="a42aa-118">Create cost elements (Task guide)</span></span>](./tasks/create-cost-elements.md)
-  [<span data-ttu-id="a42aa-119">成本对象维度</span><span class="sxs-lookup"><span data-stu-id="a42aa-119">Cost object dimensions</span></span>](cost-objects.md)
-  [<span data-ttu-id="a42aa-120">创建成本元素（任务指南）</span><span class="sxs-lookup"><span data-stu-id="a42aa-120">Create cost elements (Task guide)</span></span>](./tasks/create-cost-objects.md)
-  [<span data-ttu-id="a42aa-121">将成本元素维度成员映射到一组常用维度成员</span><span class="sxs-lookup"><span data-stu-id="a42aa-121">Map cost element dimension members to a common set of dimension members</span></span>](map-cost-elements-dimension-members.md)
-  [<span data-ttu-id="a42aa-122">映射成本元素维度（任务指南）</span><span class="sxs-lookup"><span data-stu-id="a42aa-122">Map a cost element dimension (Task guide)</span></span>](./tasks/map-cost-element-dimension.md)
-  [<span data-ttu-id="a42aa-123">统计维度成员和统计度量提供方模板</span><span class="sxs-lookup"><span data-stu-id="a42aa-123">Statistical dimension members and statistical measure provider templates</span></span>](statistical-measure-provider-template.md)







