---
title: "组织和组织层次结构"
description: "组织是共同工作以执行业务流程的群体。 组织层次结构表示构成您的公司的组织之间的关系。"
author: sericks007
manager: AnnBe
ms.date: 08/18/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 17291
ms.assetid: 76b7ca45-93d4-45cc-b191-66ee63afa1fd
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 563aaea1d565df1e82fb0e5dafe268f0d0838528
ms.openlocfilehash: 21dae54c91b699f402c5c7a7105dc36e7ee5bb52
ms.contentlocale: zh-cn
ms.lasthandoff: 08/18/2017

---

# <a name="organizations-and-organizational-hierarchies"></a><span data-ttu-id="1cad2-104">组织和组织层次结构</span><span class="sxs-lookup"><span data-stu-id="1cad2-104">Organizations and organizational hierarchies</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="1cad2-105">组织是共同工作以执行业务流程的群体。</span><span class="sxs-lookup"><span data-stu-id="1cad2-105">An organization is a group of people who are working together to carry out a business process or achieve a goal.</span></span> <span data-ttu-id="1cad2-106">组织层次结构表示构成您的公司的组织之间的关系。</span><span class="sxs-lookup"><span data-stu-id="1cad2-106">Organizational hierarchies represent the relationships between the organizations that make up your business.</span></span>

<a name="organizations"></a><span data-ttu-id="1cad2-107">组织</span><span class="sxs-lookup"><span data-stu-id="1cad2-107">Organizations</span></span>
-------------

<span data-ttu-id="1cad2-108">在 Microsoft Dynamics 365 for Finance and Operations 中，您可以定义以下类型的内部组织：法人、运营单位和团队。</span><span class="sxs-lookup"><span data-stu-id="1cad2-108">In Microsoft Dynamics 365 for Finance and Operations, you can define the following types of internal organizations: legal entities, operating units, and teams.</span></span>

<span data-ttu-id="1cad2-109">所有内部组织都为“**聚会**”实体的类型。</span><span class="sxs-lookup"><span data-stu-id="1cad2-109">All internal organizations are types of the **Party** entity.</span></span> <span data-ttu-id="1cad2-110">因此，这些组织使用通讯簿功能储存地址和联系信息。</span><span class="sxs-lookup"><span data-stu-id="1cad2-110">Therefore, these organizations use the address book to store address and contact information.</span></span> <span data-ttu-id="1cad2-111">当事人（可以是人员或组织）可以属于一个或多个通讯簿。</span><span class="sxs-lookup"><span data-stu-id="1cad2-111">A party, which can be either a person or an organization, can belong to one or more address books.</span></span>
### <a name="legal-entities"></a><span data-ttu-id="1cad2-112">法人</span><span class="sxs-lookup"><span data-stu-id="1cad2-112">Legal entities</span></span>

<span data-ttu-id="1cad2-113">法人是具有已登记的或法律允许的法律结构的组织。</span><span class="sxs-lookup"><span data-stu-id="1cad2-113">A legal entity is an organization that has a registered or legislated legal structure.</span></span> <span data-ttu-id="1cad2-114">法人可以输入到法律合同，并需要准备报告它们的业绩的报表。</span><span class="sxs-lookup"><span data-stu-id="1cad2-114">Legal entities can enter into legal contracts and are required to prepare statements that report on their performance.</span></span> 

<span data-ttu-id="1cad2-115">公司是法人的一种类型。</span><span class="sxs-lookup"><span data-stu-id="1cad2-115">A company is a type of legal entity.</span></span> <span data-ttu-id="1cad2-116">在 Microsoft Dynamics 365 for Finance and Operations 的此版本中，公司只能是您能创建的这类法人，每个法人与公司 ID 相关联。</span><span class="sxs-lookup"><span data-stu-id="1cad2-116">In this release of Microsoft Dynamics 365 for Finance and Operations, companies are the only kind of legal entity that you can create, and every legal entity is associated with a company ID.</span></span> <span data-ttu-id="1cad2-117">因为程序中的某些功能区域在它们的数据模型中使用了公司 ID 或 DataAreaId，所以此关联存在。</span><span class="sxs-lookup"><span data-stu-id="1cad2-117">This association exists because some functional areas in the program use a company ID, or DataAreaId, in their data models.</span></span> <span data-ttu-id="1cad2-118">在这些功能区域中，公司用作了数据安全性的边界。</span><span class="sxs-lookup"><span data-stu-id="1cad2-118">In these functional areas, companies are used as a boundary for data security.</span></span> <span data-ttu-id="1cad2-119">用户只能访问他们当前登录到的公司的数据。</span><span class="sxs-lookup"><span data-stu-id="1cad2-119">Users can access data only for the company that they are currently logged on to.</span></span>

### <a name="operating-units"></a><span data-ttu-id="1cad2-120">运营单位</span><span class="sxs-lookup"><span data-stu-id="1cad2-120">Operating units</span></span>

<span data-ttu-id="1cad2-121">运营单位是用来拆分企业中的经济资源和运营流程的控件的组织。</span><span class="sxs-lookup"><span data-stu-id="1cad2-121">An operating unit is an organization that is used to divide the control of economic resources and operational processes in a business.</span></span> <span data-ttu-id="1cad2-122">运营单位中的人有义务最大化对稀有资源的使用、改进流程和记录他们的业绩。</span><span class="sxs-lookup"><span data-stu-id="1cad2-122">People in an operating unit have a duty to maximize the use of scarce resources, improve processes, and account for their performance.</span></span> 

<span data-ttu-id="1cad2-123">在 Microsoft Dynamics 365 for Finance and Operations 中，运营单位的类型包括成本中心、业务单位、价值流、部门和零售渠道。</span><span class="sxs-lookup"><span data-stu-id="1cad2-123">In Microsoft Dynamics 365 for Finance and Operations, the types of operating units include cost centers, business units, value streams, departments, and retail channels.</span></span> <span data-ttu-id="1cad2-124">下表提供了有关每个类型的运营单位的详细信息。</span><span class="sxs-lookup"><span data-stu-id="1cad2-124">The following table provides more information about each type of operating unit.</span></span>

| <span data-ttu-id="1cad2-125">运营单位类型</span><span class="sxs-lookup"><span data-stu-id="1cad2-125">Operating unit type</span></span> | <span data-ttu-id="1cad2-126">描述</span><span class="sxs-lookup"><span data-stu-id="1cad2-126">Description</span></span>         | <span data-ttu-id="1cad2-127">用途</span><span class="sxs-lookup"><span data-stu-id="1cad2-127">Purpose</span></span>      |
|---------------------|---------------------|--------------|
| <span data-ttu-id="1cad2-128">成本中心</span><span class="sxs-lookup"><span data-stu-id="1cad2-128">Cost center</span></span>         | <span data-ttu-id="1cad2-129">经理对预算的和实际支出负问责性的工序运营单位。</span><span class="sxs-lookup"><span data-stu-id="1cad2-129">An operating unit in which managers are accountable for budgeted and actual expenditures.</span></span>                                                      | <span data-ttu-id="1cad2-130">用于跨法人的业务流程的管理和运营控制。</span><span class="sxs-lookup"><span data-stu-id="1cad2-130">Used for the management and operational control of business processes that span legal entities.</span></span>                                         |
| <span data-ttu-id="1cad2-131">业务单位</span><span class="sxs-lookup"><span data-stu-id="1cad2-131">Business unit</span></span>       | <span data-ttu-id="1cad2-132">创建来满足战略业务目标的一个半自主运营单位。</span><span class="sxs-lookup"><span data-stu-id="1cad2-132">A semi-autonomous operating unit that is created to meet strategic business objectives.</span></span>                                                        | <span data-ttu-id="1cad2-133">用于基于组织单独服务的法人的工厂或产品行的财务报表。</span><span class="sxs-lookup"><span data-stu-id="1cad2-133">Used for financial reporting that is based on industries or product lines that the organization serves independently of legal entities.</span></span> |
| <span data-ttu-id="1cad2-134">价值流</span><span class="sxs-lookup"><span data-stu-id="1cad2-134">Value stream</span></span>        | <span data-ttu-id="1cad2-135">控制一个或多个生产流的工序单位。</span><span class="sxs-lookup"><span data-stu-id="1cad2-135">An operating unit that controls one or more production flows.</span></span>                                                                                  | <span data-ttu-id="1cad2-136">通常在控制产品或服务要求提供给客户的活动和流的精益制造中。</span><span class="sxs-lookup"><span data-stu-id="1cad2-136">Commonly used in lean manufacturing to control the activities and flows that are required to supply a product or service to consumers.</span></span>  |
| <span data-ttu-id="1cad2-137">部门</span><span class="sxs-lookup"><span data-stu-id="1cad2-137">Department</span></span>          | <span data-ttu-id="1cad2-138">表示执行销售或记账等特定任务的组织的类别或功能部分的运营单位。</span><span class="sxs-lookup"><span data-stu-id="1cad2-138">An operating unit that represents a category or functional part of an organization that performs a specific task, such as sales or accounting.</span></span> | <span data-ttu-id="1cad2-139">用于申报功能区域。</span><span class="sxs-lookup"><span data-stu-id="1cad2-139">Used to report on functional areas.</span></span> <span data-ttu-id="1cad2-140">某部分可能具有损益责任，而且可能是由一组成本中心构成的。</span><span class="sxs-lookup"><span data-stu-id="1cad2-140">A department may have profit and loss responsibility, and may consist of a group of cost centers.</span></span>   |
| <span data-ttu-id="1cad2-141">零售渠道</span><span class="sxs-lookup"><span data-stu-id="1cad2-141">Retail channel</span></span>      | <span data-ttu-id="1cad2-142">应用单位表示传统实体店、在线商店或联机市场。</span><span class="sxs-lookup"><span data-stu-id="1cad2-142">An operating unit that represents a brick and mortar store, an online store or an online marketplace.</span></span>                                          | <span data-ttu-id="1cad2-143">用于法人内或跨法人的一个或多个商店的管理和运营控制。</span><span class="sxs-lookup"><span data-stu-id="1cad2-143">Used for the management and operational control of one or more stores within or across legal entities.</span></span>                                  |

### <a name="teams"></a><span data-ttu-id="1cad2-144">团队</span><span class="sxs-lookup"><span data-stu-id="1cad2-144">Teams</span></span>

<span data-ttu-id="1cad2-145">团队是一个组织，该组织的成员共享公共责任、利益或目标。</span><span class="sxs-lookup"><span data-stu-id="1cad2-145">A team is an organization in which the members share a common responsibility, interest, or objective.</span></span> <span data-ttu-id="1cad2-146">团队不能用于组织层次结构。</span><span class="sxs-lookup"><span data-stu-id="1cad2-146">Teams cannot be used in organizational hierarchies.</span></span>

<a name="organizational-hierarchies"></a><span data-ttu-id="1cad2-147">组织的层次结构</span><span class="sxs-lookup"><span data-stu-id="1cad2-147">Organizational hierarchies</span></span>
--------------------------

<span data-ttu-id="1cad2-148">设置组织的层次结构以查看和申报来自不同视角的业务。</span><span class="sxs-lookup"><span data-stu-id="1cad2-148">Set up organizational hierarchies to view and report on your business from different perspectives.</span></span> <span data-ttu-id="1cad2-149">例如，您可以针对纳税、法律或法定申报设置法人的层次结构。</span><span class="sxs-lookup"><span data-stu-id="1cad2-149">For example, you can set up a hierarchy of legal entities for tax, legal, or statutory reporting.</span></span> <span data-ttu-id="1cad2-150">设置基于运营单位的层次结构以报告不是法律要求但用于内部控制的财务信息。</span><span class="sxs-lookup"><span data-stu-id="1cad2-150">Set up a hierarchy that is based on operating units to report financial information that is not legally required, but that is used for internal control.</span></span> <span data-ttu-id="1cad2-151">例如，您可以创建一个采购层次结构以控制采购策略、规则和义务流程。</span><span class="sxs-lookup"><span data-stu-id="1cad2-151">For example, you can create a purchasing hierarchy to control purchasing policies, rules, and business processes.</span></span> 

<span data-ttu-id="1cad2-152">每个层次结构都将分配 Microsoft Dynamics 365 for Finance and Operations 的用途。</span><span class="sxs-lookup"><span data-stu-id="1cad2-152">Each hierarchy is assigned a purpose in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="1cad2-153">层次结构用途确定可以包括在层次结构中的组织的类型。</span><span class="sxs-lookup"><span data-stu-id="1cad2-153">The purpose of a hierarchy determines the types of organizations that can be included in the hierarchy.</span></span> <span data-ttu-id="1cad2-154">该用途还决定着哪些应用程序方案能够在该层次结构中使用。</span><span class="sxs-lookup"><span data-stu-id="1cad2-154">The purpose also determines which application scenarios a hierarchy can be used in.</span></span> 

<span data-ttu-id="1cad2-155">层次结构中的组织可以共享参数、策略和交易记录。</span><span class="sxs-lookup"><span data-stu-id="1cad2-155">Organizations in a hierarchy can share parameters, policies, and transactions.</span></span> <span data-ttu-id="1cad2-156">组织可以继承或覆盖其父级组织的参数。</span><span class="sxs-lookup"><span data-stu-id="1cad2-156">An organization can inherit or override the parameters of its parent organization.</span></span> <span data-ttu-id="1cad2-157">但是，产品和地址簿等共享的主数据适用于整个组织，但是不能被单个组织覆盖。</span><span class="sxs-lookup"><span data-stu-id="1cad2-157">However, shared master data, such as products and address books, applies to the whole organization and cannot be overridden for individual organizations.</span></span> <span data-ttu-id="1cad2-158">创建组织和层次结构要求详细计划。</span><span class="sxs-lookup"><span data-stu-id="1cad2-158">Creating organizations and hierarchies requires careful planning.</span></span> <span data-ttu-id="1cad2-159">有关详细信息，请参阅[计划组织层次结构](plan-organizational-hierarchy.md)。</span><span class="sxs-lookup"><span data-stu-id="1cad2-159">For more information, see [Plan the organizational hierarchy](plan-organizational-hierarchy.md).</span></span>






