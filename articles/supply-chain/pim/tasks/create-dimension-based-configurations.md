---
title: 创建基于维度的配置
description: 此过程显示如何定义基于维度的产品的配置。
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, EcoResDimensionBasedConfiguration, ConfigChooseFromRoute, ConfigChooseFromGroup, ConfigChoiceApprove
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c3e5cd2677480b14739f963cf4a74efaa7f2bd2a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423003"
---
# <a name="create-dimension-based-configurations"></a><span data-ttu-id="a04fb-103">创建基于维度的配置</span><span class="sxs-lookup"><span data-stu-id="a04fb-103">Create dimension-based configurations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a04fb-104">此过程显示如何定义基于维度的产品的配置。</span><span class="sxs-lookup"><span data-stu-id="a04fb-104">This procedure shows how to define a configuration for a dimension-based product.</span></span> <span data-ttu-id="a04fb-105">这是此系列中最后一个说明如何构建基于维度的配置组合的过程。</span><span class="sxs-lookup"><span data-stu-id="a04fb-105">This is the last procedure in the series that explains how to build combinations for dimension-based configuration.</span></span> <span data-ttu-id="a04fb-106">此过程的执行取决于在前七个记录中创建的数据。</span><span class="sxs-lookup"><span data-stu-id="a04fb-106">The execution of this procedure is dependent on the data created in the previous seven recordings.</span></span> <span data-ttu-id="a04fb-107">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="a04fb-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="find-the-dimension-based-product-master"></a><span data-ttu-id="a04fb-108">查找基于维度的基础产品</span><span class="sxs-lookup"><span data-stu-id="a04fb-108">Find the dimension-based product master</span></span>
1. <span data-ttu-id="a04fb-109">单击“已发布产品的维护”。</span><span class="sxs-lookup"><span data-stu-id="a04fb-109">Click Released product maintenance.</span></span>
2. <span data-ttu-id="a04fb-110">单击“已发布产品”。</span><span class="sxs-lookup"><span data-stu-id="a04fb-110">Click Released products.</span></span>
3. <span data-ttu-id="a04fb-111">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="a04fb-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="a04fb-112">选择您以 8 个记录的此顺序在第一个记录中创建的基于维度的基础产品。</span><span class="sxs-lookup"><span data-stu-id="a04fb-112">Select the dimension-based product master that you created in the first recording in this sequence of 8 recordings.</span></span>  

## <a name="create-configurations"></a><span data-ttu-id="a04fb-113">创建配置</span><span class="sxs-lookup"><span data-stu-id="a04fb-113">Create configurations</span></span>
1. <span data-ttu-id="a04fb-114">在“工程操作窗格”上单击“维护配置”。</span><span class="sxs-lookup"><span data-stu-id="a04fb-114">On the Engineering Action Pane, click Maintain configurations.</span></span>
2. <span data-ttu-id="a04fb-115">单击“配置”。</span><span class="sxs-lookup"><span data-stu-id="a04fb-115">Click Configure.</span></span>
3. <span data-ttu-id="a04fb-116">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="a04fb-116">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="a04fb-117">在“物料编号”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="a04fb-117">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="a04fb-118">选择第一个配置组中的任意物料。</span><span class="sxs-lookup"><span data-stu-id="a04fb-118">Select any of the items in the first configuration group.</span></span>  
5. <span data-ttu-id="a04fb-119">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="a04fb-119">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="a04fb-120">在“物料编号”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="a04fb-120">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="a04fb-121">从第二个配置组中选择任意物料。</span><span class="sxs-lookup"><span data-stu-id="a04fb-121">Select any item from the second configuration group.</span></span>  
7. <span data-ttu-id="a04fb-122">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="a04fb-122">Click OK.</span></span>
8. <span data-ttu-id="a04fb-123">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="a04fb-123">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="a04fb-124">在“配置”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="a04fb-124">In the Configuration field, type a value.</span></span>
    * <span data-ttu-id="a04fb-125">输入将便于标识配置的名称。</span><span class="sxs-lookup"><span data-stu-id="a04fb-125">Enter a configuration name that will make it easy to identify the configuration.</span></span>  
10. <span data-ttu-id="a04fb-126">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="a04fb-126">In the Description field, type a value.</span></span>
    * <span data-ttu-id="a04fb-127">输入说明配置包含的内容的配置描述。</span><span class="sxs-lookup"><span data-stu-id="a04fb-127">Enter a description of the configuration to explain what it contains.</span></span>  
11. <span data-ttu-id="a04fb-128">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="a04fb-128">Click OK.</span></span>

