---
title: "创建一个部门并将该部门与部门层次结构关联"
description: "部门是一个运营单位，表示组织的类别或功能区域。 部门负责组织的特定区域，例如，销售、会计或人力资源。 您可以在功能区中使用要上报的部门。 部门可能具有损益职责。"
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HierarchyDesigner, OMOperatingUnit
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 812db9f1d319e4d16f83700a7153a0a3b318963e
ms.openlocfilehash: 3fc30669bf7a16616484bf7115cb121ce463840f
ms.contentlocale: zh-cn
ms.lasthandoff: 03/23/2018

---

# <a name="create-a-department-and-associate-it-with-the-department-hierarchy"></a><span data-ttu-id="fa005-106">创建一个部门并将该部门与部门层次结构关联</span><span class="sxs-lookup"><span data-stu-id="fa005-106">Create a department and associate it with the department hierarchy</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="fa005-107">部门是一个运营单位，表示组织的类别或功能区域。</span><span class="sxs-lookup"><span data-stu-id="fa005-107">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="fa005-108">部门负责组织的特定区域，例如，销售、会计或人力资源。</span><span class="sxs-lookup"><span data-stu-id="fa005-108">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="fa005-109">您可以在功能区中使用要上报的部门。</span><span class="sxs-lookup"><span data-stu-id="fa005-109">You can use departments to report on functional areas.</span></span> <span data-ttu-id="fa005-110">部门可能具有损益职责。</span><span class="sxs-lookup"><span data-stu-id="fa005-110">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="fa005-111">部门还可能包括成本中心组。</span><span class="sxs-lookup"><span data-stu-id="fa005-111">A department might include a group of cost centers.</span></span> <span data-ttu-id="fa005-112">可以向部门分配位置。</span><span class="sxs-lookup"><span data-stu-id="fa005-112">Positions can be assigned to departments.</span></span> <span data-ttu-id="fa005-113">要创建部门，请单击**人力资源** &gt; **部门** &gt; **部门**。</span><span class="sxs-lookup"><span data-stu-id="fa005-113">To create a department, click **Human Resources** &gt; **Departments** &gt; **Department**.</span></span> <span data-ttu-id="fa005-114">下表说明可用的字段。</span><span class="sxs-lookup"><span data-stu-id="fa005-114">The following table describes the fields that are available.</span></span>

| <span data-ttu-id="fa005-115">字段</span><span class="sxs-lookup"><span data-stu-id="fa005-115">Field</span></span>               | <span data-ttu-id="fa005-116">描述</span><span class="sxs-lookup"><span data-stu-id="fa005-116">Description</span></span>                                                                                                                                                                                                       |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa005-117">姓名</span><span class="sxs-lookup"><span data-stu-id="fa005-117">Name</span></span>                | <span data-ttu-id="fa005-118">输入部门名称。</span><span class="sxs-lookup"><span data-stu-id="fa005-118">Enter a name for the department.</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="fa005-119">部门编号</span><span class="sxs-lookup"><span data-stu-id="fa005-119">Department number</span></span>   | <span data-ttu-id="fa005-120">如果向**“编号规则”**页上的**“组织编号”**引用分配编号规则代码，则可能会自动生成默认值。</span><span class="sxs-lookup"><span data-stu-id="fa005-120">A default value might be generated automatically if a number sequence code is assigned to the **Organization number** reference on the **Number sequences** page.</span></span>                                                 |
| <span data-ttu-id="fa005-121">搜索名称</span><span class="sxs-lookup"><span data-stu-id="fa005-121">Search name</span></span>         | <span data-ttu-id="fa005-122">输入可用于搜索部门的名称或缩写。</span><span class="sxs-lookup"><span data-stu-id="fa005-122">Enter a name or acronym that can be used to search for the department.</span></span>                                                                                                                                            |
| <span data-ttu-id="fa005-123">备忘录</span><span class="sxs-lookup"><span data-stu-id="fa005-123">Memo</span></span>                | <span data-ttu-id="fa005-124">在此处输入任何附加信息。</span><span class="sxs-lookup"><span data-stu-id="fa005-124">Enter any additional information here.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="fa005-125">在层次结构中</span><span class="sxs-lookup"><span data-stu-id="fa005-125">In hierarchy</span></span>        | <span data-ttu-id="fa005-126">选中的复选框表示部门已包含在部门层次结构中。</span><span class="sxs-lookup"><span data-stu-id="fa005-126">A selected check box indicates that the department is included in the department hierarchy.</span></span> <span data-ttu-id="fa005-127">有关如何将部门添加到部门层次结构的信息，请参阅本文中后面的信息。</span><span class="sxs-lookup"><span data-stu-id="fa005-127">For information about how to add a department to the department hierarchy, see the information later in this article.</span></span> |
| <span data-ttu-id="fa005-128">DUNS 编号</span><span class="sxs-lookup"><span data-stu-id="fa005-128">DUNS number</span></span>         | <span data-ttu-id="fa005-129">DUNS 代表数据统一编码系统。</span><span class="sxs-lookup"><span data-stu-id="fa005-129">DUNS stands for Data Universal Number System.</span></span> <span data-ttu-id="fa005-130">这是由 Dun & Bradstreet 发布的 9 位数编号。</span><span class="sxs-lookup"><span data-stu-id="fa005-130">This is a nine-digit number that is issued by Dun & Bradstreet.</span></span>                                                                                                     |
| <span data-ttu-id="fa005-131">经理</span><span class="sxs-lookup"><span data-stu-id="fa005-131">Manager</span></span>             | <span data-ttu-id="fa005-132">输入管理部门的人员。</span><span class="sxs-lookup"><span data-stu-id="fa005-132">Enter the persona that manages the department.</span></span>                                                                                                                                                                    |
| <span data-ttu-id="fa005-133">地址</span><span class="sxs-lookup"><span data-stu-id="fa005-133">Addresses</span></span>           | <span data-ttu-id="fa005-134">添加部门的地址信息。</span><span class="sxs-lookup"><span data-stu-id="fa005-134">Add the address information for the department.</span></span> <span data-ttu-id="fa005-135">例如，添加部门所在的建筑物邮寄地址。</span><span class="sxs-lookup"><span data-stu-id="fa005-135">For example, add the mailing address for the building that the department is located in.</span></span>                                                                          |
| <span data-ttu-id="fa005-136">联系人信息</span><span class="sxs-lookup"><span data-stu-id="fa005-136">Contact information</span></span> | <span data-ttu-id="fa005-137">添加部门的联系人信息。</span><span class="sxs-lookup"><span data-stu-id="fa005-137">Add contact information for the department.</span></span> <span data-ttu-id="fa005-138">例如，添加部门服务台的电话号码。</span><span class="sxs-lookup"><span data-stu-id="fa005-138">For example, add a telephone number for the service desk in the department.</span></span>                                                                                           |

<span data-ttu-id="fa005-139">要将部门添加到部门层次结构，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="fa005-139">To add a department to the department hierarchy, follow these steps.</span></span>

1.  <span data-ttu-id="fa005-140">单击**人力资源** &gt; **部门** &gt; **部门层次结构**。</span><span class="sxs-lookup"><span data-stu-id="fa005-140">Click **Human Resources** &gt; **Departments** &gt; **Department hierarchy**.</span></span>
2.  <span data-ttu-id="fa005-141">单击**“编辑”**，然后选择部门应在其下方的组织。</span><span class="sxs-lookup"><span data-stu-id="fa005-141">Click **Edit**, and then select the organization that the department should be under.</span></span>
3.  <span data-ttu-id="fa005-142">单击**“插入”**，然后在列表中选择**“部门”**。</span><span class="sxs-lookup"><span data-stu-id="fa005-142">Click **Insert**, and select **Department** in the list.</span></span>
4.  <span data-ttu-id="fa005-143">在显示的部门列表中，选择要添加到层次结构的部门。</span><span class="sxs-lookup"><span data-stu-id="fa005-143">In the list of departments that appears, select the department to add to the hierarchy.</span></span>
5.  <span data-ttu-id="fa005-144">保存所做的更改。</span><span class="sxs-lookup"><span data-stu-id="fa005-144">Save your changes.</span></span> <span data-ttu-id="fa005-145">您会收到一条消息，表示已创建层次结构的草稿版本。</span><span class="sxs-lookup"><span data-stu-id="fa005-145">You receive a message that a draft version of the hierarchy has been created.</span></span>
6.  <span data-ttu-id="fa005-146">准备好后，单击层次结构设计器中的**发布**。</span><span class="sxs-lookup"><span data-stu-id="fa005-146">When you're ready, click **Publish** in the hierarchy designer.</span></span> <span data-ttu-id="fa005-147">您可以输入一个指示何时应发布层次结构的生效日期。</span><span class="sxs-lookup"><span data-stu-id="fa005-147">You can enter an effective date that indicates when the hierarchy should be published.</span></span> <span data-ttu-id="fa005-148">例如，要在下一个日历年的年初添加新部门，请将生效日期设置为新日历年的 1 月 1 日。</span><span class="sxs-lookup"><span data-stu-id="fa005-148">For example, to add a new department at the beginning of the next calendar year, set the effective date to January 1 of the new calendar year.</span></span> <span data-ttu-id="fa005-149">对层次结构进行的更改将在该日期生效。</span><span class="sxs-lookup"><span data-stu-id="fa005-149">The changes to the hierarchy will take effect on that date.</span></span>

## <a name="steps-for-creating-a-department"></a><span data-ttu-id="fa005-150">部门创建步骤</span><span class="sxs-lookup"><span data-stu-id="fa005-150">Steps for creating a department</span></span>
<span data-ttu-id="fa005-151">请参阅[定义新部门](../fin-and-ops/hr/tasks/define-new-departments.md)主题了解创建新部门的分步过程。</span><span class="sxs-lookup"><span data-stu-id="fa005-151">Refer to the [Define new departments](../fin-and-ops/hr/tasks/define-new-departments.md) topic for the step-by-step procedure for creating a new department.</span></span> 

