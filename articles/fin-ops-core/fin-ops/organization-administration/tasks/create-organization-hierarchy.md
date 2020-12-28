---
title: 创建组织层次结构。
description: 使用以下过程创建组织层次结构。
author: sericks007
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OMHierarchyManager, OMHierarchyPurposeAssociation, OMHierarchySelection, HierarchyDesigner
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 673403680525eff57c5886bb4f430a33efd76250
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/08/2020
ms.locfileid: "4694781"
---
# <a name="create-an-organization-hierarchy"></a><span data-ttu-id="6d7ea-103">创建组织层次结构。</span><span class="sxs-lookup"><span data-stu-id="6d7ea-103">Create an organization hierarchy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6d7ea-104">使用以下过程创建组织层次结构。</span><span class="sxs-lookup"><span data-stu-id="6d7ea-104">Use the following procedure to create an organizational hierarchy.</span></span> <span data-ttu-id="6d7ea-105">可以使用组织层次结构查看和申报来自各种视角的业务。</span><span class="sxs-lookup"><span data-stu-id="6d7ea-105">You can use organizational hierarchies to view and report on your business from various perspectives.</span></span> <span data-ttu-id="6d7ea-106">例如，您可以针对纳税、法律或法定申报设置一种层次结构。</span><span class="sxs-lookup"><span data-stu-id="6d7ea-106">For example, you can set up one hierarchy for tax, legal, or statutory reporting.</span></span> <span data-ttu-id="6d7ea-107">然后，您可以设置另一层次结构，以报告不是法律要求但用于内部报表的财务信息。</span><span class="sxs-lookup"><span data-stu-id="6d7ea-107">You can then set up another hierarchy to report financial information that is not legally required, but that is used for internal reporting.</span></span> 

<span data-ttu-id="6d7ea-108">在创建某一组织层次结构之前，必须先创建组织。</span><span class="sxs-lookup"><span data-stu-id="6d7ea-108">Before you create an organizational hierarchy, you must create organizations.</span></span> <span data-ttu-id="6d7ea-109">有关详细信息，请参阅“创建法人”或“创建运营单位”任务。</span><span class="sxs-lookup"><span data-stu-id="6d7ea-109">For more information, see the "Create a legal entity" or "Create an operating unit" tasks.</span></span> <span data-ttu-id="6d7ea-110">您还可以创建部门和团队。</span><span class="sxs-lookup"><span data-stu-id="6d7ea-110">You can also create departments and teams.</span></span> 

<span data-ttu-id="6d7ea-111">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="6d7ea-111">The demo data company used to create this procedure is USMF.</span></span>

## <a name="create-a-hierarchy"></a><span data-ttu-id="6d7ea-112">创建层次结构</span><span class="sxs-lookup"><span data-stu-id="6d7ea-112">Create a hierarchy</span></span>
1. <span data-ttu-id="6d7ea-113">转到 **导航窗格 > 模块 > 组织管理 > 组织 > 组织层次结构**。</span><span class="sxs-lookup"><span data-stu-id="6d7ea-113">Go to **Navigation pane > Modules > Organization administration > Organizations > Organization hierarchies**.</span></span>
2. <span data-ttu-id="6d7ea-114">在 **操作窗格** 中，单击 **新建**。</span><span class="sxs-lookup"><span data-stu-id="6d7ea-114">On the **Action pane**, click **New**.</span></span>
3. <span data-ttu-id="6d7ea-115">在 **名称** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="6d7ea-115">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="6d7ea-116">在 **用途** 部分中，单击 **分配用途**。</span><span class="sxs-lookup"><span data-stu-id="6d7ea-116">In the **Purpose** section, click **Assign purpose**.</span></span>
5. <span data-ttu-id="6d7ea-117">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="6d7ea-117">In the list, find and select the desired record.</span></span> <span data-ttu-id="6d7ea-118">选择分配给组织层次结构的用途。</span><span class="sxs-lookup"><span data-stu-id="6d7ea-118">Select a purpose to assign to your organization hierarchy.</span></span>  
6. <span data-ttu-id="6d7ea-119">在 **已分配层次结构** 部分中，单击 **添加**。</span><span class="sxs-lookup"><span data-stu-id="6d7ea-119">In the **Assigned hierarchies** sectiom, click **Add**.</span></span>
7. <span data-ttu-id="6d7ea-120">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="6d7ea-120">In the list, mark the selected row.</span></span> <span data-ttu-id="6d7ea-121">查找您刚才创建的层次结构。</span><span class="sxs-lookup"><span data-stu-id="6d7ea-121">Find the hierarchy you just created.</span></span>  
8. <span data-ttu-id="6d7ea-122">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="6d7ea-122">Click **OK**.</span></span>

## <a name="add-organizations-to-the-hierarchy"></a><span data-ttu-id="6d7ea-123">将组织添加到层次结构</span><span class="sxs-lookup"><span data-stu-id="6d7ea-123">Add organizations to the hierarchy</span></span>
1. <span data-ttu-id="6d7ea-124">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="6d7ea-124">In the list, find and select the desired record.</span></span> <span data-ttu-id="6d7ea-125">选择层次结构。</span><span class="sxs-lookup"><span data-stu-id="6d7ea-125">Select your hierarchy.</span></span>  
2. <span data-ttu-id="6d7ea-126">在 **已分配层次结构** 部分中，单击 **查看层次结构**。</span><span class="sxs-lookup"><span data-stu-id="6d7ea-126">In the **Assigned hierarchies** section, click **View hierarchy**.</span></span>
    - <span data-ttu-id="6d7ea-127">根据需要添加组织。</span><span class="sxs-lookup"><span data-stu-id="6d7ea-127">Add organizations, as necessary.</span></span>  
    - <span data-ttu-id="6d7ea-128">若要添加组织，单击 **编辑**，然后单击 **插入** 来添加组织。</span><span class="sxs-lookup"><span data-stu-id="6d7ea-128">To add an organization, click **Edit** and then **Insert** to add the organization.</span></span> <span data-ttu-id="6d7ea-129">在进行更改后，您可以 **保存** 草稿和/或 **发布** 更改。</span><span class="sxs-lookup"><span data-stu-id="6d7ea-129">When you are done making changes you can **Save** a draft and/or **Publish** the changes.</span></span>  

