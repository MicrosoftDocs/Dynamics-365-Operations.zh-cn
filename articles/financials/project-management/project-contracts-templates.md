---
title: 将项目合同和项目直接从 Project Service Automation 同步到 Finance and Operations
description: 此主题介绍用于直接同步 Microsoft Dynamics 365 for Project Service Automation 与 Microsoft Dynamics 365 for Finance and Operations 的项目合同和项目的模板和基础任务。
author: KimANelson
manager: AnnBe
ms.date: 10/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 0889bc233674cb80dd056ac77edb5c936c6633a7
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "312109"
---
# <a name="synchronize-project-contracts-and-projects-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="6f6ce-103">将项目合同和项目直接从 Project Service Automation 同步到 Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="6f6ce-103">Synchronize project contracts and projects directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="6f6ce-104">此主题介绍用于直接同步 Microsoft Dynamics 365 for Project Service Automation 与 Microsoft Dynamics 365 for Finance and Operations 的项目合同和项目的模板和基础任务。</span><span class="sxs-lookup"><span data-stu-id="6f6ce-104">This topic describes the template and underlying tasks that are used to synchronize project contracts and projects directly from Microsoft Dynamics 365 for Project Service Automation to Microsoft Dynamics 365 for Finance and Operations.</span></span>

> [!NOTE] 
> <span data-ttu-id="6f6ce-105">如果在使用 Microsoft Dynamics 365 for Finance and Operations Enterprise edition 7.3.0，则必须安装 KB 4074835。</span><span class="sxs-lookup"><span data-stu-id="6f6ce-105">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, you must install KB 4074835.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="6f6ce-106">Project Service Automation 到 Finance and Operations 的数据传输</span><span class="sxs-lookup"><span data-stu-id="6f6ce-106">Data flow for Project Service Automation to Finance and Operations</span></span>

> [!NOTE]
> <span data-ttu-id="6f6ce-107">应先熟悉 Microsoft Dynamics 365 Data integration 功能，才能使用 Project Service Automation 到 Finance and Operations 集成解决方案。</span><span class="sxs-lookup"><span data-stu-id="6f6ce-107">Before you can use the Project Service Automation to Finance and Operations integration solution, you should be familiar with the Microsoft Dynamics 365 Data integration feature.</span></span>

<span data-ttu-id="6f6ce-108">Project Service Automation 到 Finance and Operations 集成解决方案使用数据集成功能在 Project Service Automation 和 Finance and Operations 的实例之间同步数据。</span><span class="sxs-lookup"><span data-stu-id="6f6ce-108">The Project Service Automation to Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="6f6ce-109">可通过数据集成功能提供的集成模板将有关项目合同、项目、项目合同行和项目合同行里程碑的数据从 Project Service Automation 传输到 Finance and Operations。</span><span class="sxs-lookup"><span data-stu-id="6f6ce-109">The integration template that is available with the Data integration feature enables the flow of data about project contracts, projects, project contract lines, and project contract line milestones from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="6f6ce-110">下图显示 Project Service Automation 与 Finance and Operations 之间中如何同步数据。</span><span class="sxs-lookup"><span data-stu-id="6f6ce-110">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="6f6ce-111">[![Project Service Automation 与 Finance and Operations 集成的数据传输](./media/ProjectsAndContractsFlow.JPG)](./media/ProjectsAndContractsFlow.JPG)</span><span class="sxs-lookup"><span data-stu-id="6f6ce-111">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectsAndContractsFlow.JPG)](./media/ProjectsAndContractsFlow.JPG)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="6f6ce-112">模板和任务</span><span class="sxs-lookup"><span data-stu-id="6f6ce-112">Templates and tasks</span></span>

<span data-ttu-id="6f6ce-113">若要访问可用模板，请在 Microsoft PowerApps 管理员中心中选择**项目**，然后在右上角中选择**新建项目**以选择公共模板。</span><span class="sxs-lookup"><span data-stu-id="6f6ce-113">To access the available templates, in the Microsoft PowerApps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="6f6ce-114">以下模板和基础任务用于将项目合同和项目从 Project Service Automation 同步到 Finance and Operations：</span><span class="sxs-lookup"><span data-stu-id="6f6ce-114">The following template and underlying tasks are used to synchronize project contracts and projects from Project Service Automation to Finance and Operations:</span></span>

- <span data-ttu-id="6f6ce-115">**数据集成中的模板名称：** 项目和合同（PSA 到 Fin and Ops）</span><span class="sxs-lookup"><span data-stu-id="6f6ce-115">**Name of the template in Data integration:** Projects and contracts (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="6f6ce-116">**项目中的任务名称：**</span><span class="sxs-lookup"><span data-stu-id="6f6ce-116">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="6f6ce-117">项目合同（PSA 到 Fin and Ops）</span><span class="sxs-lookup"><span data-stu-id="6f6ce-117">Project contracts PSA to Fin and Ops</span></span>
    - <span data-ttu-id="6f6ce-118">项目（PSA 到 Fin and Ops）</span><span class="sxs-lookup"><span data-stu-id="6f6ce-118">Projects PSA to Fin and Ops</span></span>
    - <span data-ttu-id="6f6ce-119">项目合同行（PSA 到 Fin and Ops）</span><span class="sxs-lookup"><span data-stu-id="6f6ce-119">Project contract lines PSA to Fin and Ops</span></span>
    - <span data-ttu-id="6f6ce-120">项目合同行里程碑（PSA 到 Fin and Ops）</span><span class="sxs-lookup"><span data-stu-id="6f6ce-120">Project contract line milestones PSA to Fin and Ops</span></span>

<span data-ttu-id="6f6ce-121">必须先同步科目，才能同步项目合同和项目。</span><span class="sxs-lookup"><span data-stu-id="6f6ce-121">Before synchronization of project contracts and projects can occur, you must synchronize accounts.</span></span>

## <a name="entity-set"></a><span data-ttu-id="6f6ce-122">实体集</span><span class="sxs-lookup"><span data-stu-id="6f6ce-122">Entity set</span></span>

| <span data-ttu-id="6f6ce-123">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="6f6ce-123">Project Service Automation</span></span>       | <span data-ttu-id="6f6ce-124">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="6f6ce-124">Finance and Operations</span></span>                                 |
|----------------------------------|--------------------------------------------------------|
| <span data-ttu-id="6f6ce-125">订单</span><span class="sxs-lookup"><span data-stu-id="6f6ce-125">Orders</span></span>                           | <span data-ttu-id="6f6ce-126">项目合同集成实体</span><span class="sxs-lookup"><span data-stu-id="6f6ce-126">Integration entity for project contract</span></span>                |
| <span data-ttu-id="6f6ce-127">项目</span><span class="sxs-lookup"><span data-stu-id="6f6ce-127">Projects</span></span>                         | <span data-ttu-id="6f6ce-128">项目的集成实体</span><span class="sxs-lookup"><span data-stu-id="6f6ce-128">Integration entity for project</span></span>                         |
| <span data-ttu-id="6f6ce-129">订单行</span><span class="sxs-lookup"><span data-stu-id="6f6ce-129">Order lines</span></span>                      | <span data-ttu-id="6f6ce-130">项目合同行集成实体</span><span class="sxs-lookup"><span data-stu-id="6f6ce-130">Integration entity for project contract line</span></span>           |
| <span data-ttu-id="6f6ce-131">项目合同行里程碑。</span><span class="sxs-lookup"><span data-stu-id="6f6ce-131">Project contract line milestones</span></span> | <span data-ttu-id="6f6ce-132">项目合同行里程碑集成实体</span><span class="sxs-lookup"><span data-stu-id="6f6ce-132">Integration entity for project contract line milestone</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="6f6ce-133">实体流</span><span class="sxs-lookup"><span data-stu-id="6f6ce-133">Entity flow</span></span>

<span data-ttu-id="6f6ce-134">项目合同在 Project Service Automation 中管理，并同步到 Finance and Operations 中充当项目合同。</span><span class="sxs-lookup"><span data-stu-id="6f6ce-134">Project contracts are managed in Project Service Automation, and they are synchronized to Finance and Operations as project contracts.</span></span> <span data-ttu-id="6f6ce-135">在集成模板中，可在 Finance and Operations 中为项目合同设置集成源。</span><span class="sxs-lookup"><span data-stu-id="6f6ce-135">As part of the integration template, you can set the integration source in Finance and Operations for the project contract.</span></span>

<span data-ttu-id="6f6ce-136">时间和物料项目和固定价格项目在 Project Service Automation 中管理，并同步到 Finance and Operations 中充当项目。</span><span class="sxs-lookup"><span data-stu-id="6f6ce-136">Time and material project and Fixed price projects are managed in Project Service Automation, and they are synchronized to Finance and Operations as projects.</span></span> <span data-ttu-id="6f6ce-137">在模板集成时，可在 Finance and Operations 中为项目设置集成源。</span><span class="sxs-lookup"><span data-stu-id="6f6ce-137">As part of the template integration, you can set the integration source in Finance and Operations for the project.</span></span>

<span data-ttu-id="6f6ce-138">项目合同行在 Project Service Automation 中管理，并同步到 Finance and Operations 中充当项目合同计费规则。</span><span class="sxs-lookup"><span data-stu-id="6f6ce-138">Project contract lines are managed in Project Service Automation, and they are synchronized to Finance and Operations as project contract billing rules.</span></span> <span data-ttu-id="6f6ce-139">如果交付方法与默认项目类型不同，同步将更新合同行项目和项目组的项目类型。</span><span class="sxs-lookup"><span data-stu-id="6f6ce-139">If the billing method differs from the default project type, the synchronization updates the project type for the contract line project and project group.</span></span>

<span data-ttu-id="6f6ce-140">项目合同行里程碑在 Project Service Automation 中管理，并同步到 Finance and Operations 中充当项目合同计费规则里程碑。</span><span class="sxs-lookup"><span data-stu-id="6f6ce-140">Project contract line milestones are managed in Project Service Automation, and they are synchronized to Finance and Operations as project contract billing rule milestones.</span></span>

## <a name="project-service-automation-to-finance-and-operations-integration-solution"></a><span data-ttu-id="6f6ce-141">Project Service Automation 到 Finance and Operations 集成解决方案</span><span class="sxs-lookup"><span data-stu-id="6f6ce-141">Project Service Automation to Finance and Operations integration solution</span></span>

<span data-ttu-id="6f6ce-142">**项目合同**页上有**项目合同 ID** 字段。</span><span class="sxs-lookup"><span data-stu-id="6f6ce-142">The **Project contract ID** field is available on the **Project contracts** page.</span></span> <span data-ttu-id="6f6ce-143">该字段由一个自然唯一密钥组成以支持集成。</span><span class="sxs-lookup"><span data-stu-id="6f6ce-143">This field has been made a natural and unique key to support the integration.</span></span>

<span data-ttu-id="6f6ce-144">新建项目合同时，如果**项目合同 ID**值不存在，则使用编号规则自动生成。</span><span class="sxs-lookup"><span data-stu-id="6f6ce-144">When a new project contract is created, if a **Project contract ID** value doesn't already exist, it's automatically generated by using a number sequence.</span></span> <span data-ttu-id="6f6ce-145">该值由 **ORD** 以及依次紧跟在后面的一个递增编号规则和一个由六个字符组成的后缀构成。</span><span class="sxs-lookup"><span data-stu-id="6f6ce-145">The value consists of **ORD** followed by an incrementing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="6f6ce-146">下面是一个示例：**ORD-01022-Z4M9Q0**。</span><span class="sxs-lookup"><span data-stu-id="6f6ce-146">Here is an example: **ORD-01022-Z4M9Q0**.</span></span>

<span data-ttu-id="6f6ce-147">**项目编号**字段在**项目**页提供。</span><span class="sxs-lookup"><span data-stu-id="6f6ce-147">The **Project Number** field is available on the **Projects** page.</span></span> <span data-ttu-id="6f6ce-148">该字段由一个自然唯一密钥组成以支持集成。</span><span class="sxs-lookup"><span data-stu-id="6f6ce-148">This field has been made a natural and unique key to support the integration.</span></span>

<span data-ttu-id="6f6ce-149">新建项目时，如果**项目编号**值不存在，则使用编号规则自动生成。</span><span class="sxs-lookup"><span data-stu-id="6f6ce-149">When a new project is created, if a **Project Number** value doesn't already exist, it's automatically generated by using a number sequence.</span></span> <span data-ttu-id="6f6ce-150">该值由 **PRJ** 以及依次紧跟在后面的一个递增编号规则和一个由六个字符组成的后缀构成。</span><span class="sxs-lookup"><span data-stu-id="6f6ce-150">The value consists of **PRJ** followed by an incrementing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="6f6ce-151">下面是一个示例：**PRJ-01049-CCNID0**。</span><span class="sxs-lookup"><span data-stu-id="6f6ce-151">Here is an example: **PRJ-01049-CCNID0**.</span></span>

<span data-ttu-id="6f6ce-152">应用 Project Service Automation 到 Finance and Operations 集成解决方案时，<TO DO: link in the top level document link where we will be adding the instructions for applying the PSA solution>升级脚本将在 Project Service Automation 为现有项目合同设置**项目合同 ID**字段，为现有项目设置**项目编号**字段。</span><span class="sxs-lookup"><span data-stu-id="6f6ce-152">When the Project Service Automation to Finance and Operations integration solution is applied<TO DO: link in the top level document link where we will be adding the instructions for applying the PSA solution>, an upgrade script sets the **Project contract ID** field for existing project contracts and the **Project Number** field for existing projects in Project Service Automation.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="6f6ce-153">先决条件和映射设置</span><span class="sxs-lookup"><span data-stu-id="6f6ce-153">Prerequisites and mapping setup</span></span>

- <span data-ttu-id="6f6ce-154">必须先同步科目，才能同步项目合同和项目。</span><span class="sxs-lookup"><span data-stu-id="6f6ce-154">Before synchronization of project contracts and projects can occur, you must synchronize accounts.</span></span>
- <span data-ttu-id="6f6ce-155">在连接集中，向 **msdyn\_name \[Name\]** 添加 **msdyn\_organizationalunits** 的集成密钥字段映射。</span><span class="sxs-lookup"><span data-stu-id="6f6ce-155">In your connection set, add an integration key field mapping for **msdyn\_organizationalunits** to **msdyn\_name \[Name\]**.</span></span> <span data-ttu-id="6f6ce-156">可能首先需要向连接集添加一个项目。</span><span class="sxs-lookup"><span data-stu-id="6f6ce-156">You might first need to add a project to the connection set.</span></span> <span data-ttu-id="6f6ce-157">有关详细信息，请参阅[将数据集成到 Common Data Service for Apps](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator)。</span><span class="sxs-lookup"><span data-stu-id="6f6ce-157">For more information, see [Integrate data into Common Data Service for Apps](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator).</span></span>
- <span data-ttu-id="6f6ce-158">在连接集中，向 **msdynce\_projectnumber \[Project Number\]** 添加 **msdyn\_projects** 的集成密钥字段映射。</span><span class="sxs-lookup"><span data-stu-id="6f6ce-158">In your connection set, add an integration key field mapping for **msdyn\_projects** to **msdynce\_projectnumber \[Project Number\]**.</span></span> <span data-ttu-id="6f6ce-159">可能首先需要向连接集添加一个项目。</span><span class="sxs-lookup"><span data-stu-id="6f6ce-159">You might first need to add a project to the connection set.</span></span> <span data-ttu-id="6f6ce-160">有关详细信息，请参阅[将数据集成到 Common Data Service for Apps](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator)。</span><span class="sxs-lookup"><span data-stu-id="6f6ce-160">For more information, see [Integrate data into Common Data Service for Apps](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator).</span></span>
- <span data-ttu-id="6f6ce-161">可将项目合同和项目的 **SourceDataID** 更新为其他值，也可以将其从映射中移除。</span><span class="sxs-lookup"><span data-stu-id="6f6ce-161">**SourceDataID** for project contracts and projects can be updated to a different value or removed from the mapping.</span></span> <span data-ttu-id="6f6ce-162">默认模板值为 **Project Service Automation**。</span><span class="sxs-lookup"><span data-stu-id="6f6ce-162">The default template value is **Project Service Automation**.</span></span>
- <span data-ttu-id="6f6ce-163">必须更新 **PaymentTerms** 映射，才能在 Finance and Operations 中体现有效的付款期限。</span><span class="sxs-lookup"><span data-stu-id="6f6ce-163">The **PaymentTerms** mapping must be updated so that it reflects valid terms of payment in Finance and Operations.</span></span> <span data-ttu-id="6f6ce-164">也可以从项目任务中移除映射。</span><span class="sxs-lookup"><span data-stu-id="6f6ce-164">You can also remove the mapping from the project task.</span></span> <span data-ttu-id="6f6ce-165">默认值映射具有演示数据的默认值。</span><span class="sxs-lookup"><span data-stu-id="6f6ce-165">The default value map has default values for demo data.</span></span> <span data-ttu-id="6f6ce-166">下表显示 Project Service Automation 中的值。</span><span class="sxs-lookup"><span data-stu-id="6f6ce-166">The following table shows the values in Project Service Automation.</span></span>

    | <span data-ttu-id="6f6ce-167">值</span><span class="sxs-lookup"><span data-stu-id="6f6ce-167">Value</span></span> | <span data-ttu-id="6f6ce-168">说明</span><span class="sxs-lookup"><span data-stu-id="6f6ce-168">Description</span></span>   |
    |-------|---------------|
    | <span data-ttu-id="6f6ce-169">1</span><span class="sxs-lookup"><span data-stu-id="6f6ce-169">1</span></span>     | <span data-ttu-id="6f6ce-170">Net 30</span><span class="sxs-lookup"><span data-stu-id="6f6ce-170">Net 30</span></span>        |
    | <span data-ttu-id="6f6ce-171">2</span><span class="sxs-lookup"><span data-stu-id="6f6ce-171">2</span></span>     | <span data-ttu-id="6f6ce-172">2%10，Net 30</span><span class="sxs-lookup"><span data-stu-id="6f6ce-172">2% 10, Net 30</span></span> |
    | <span data-ttu-id="6f6ce-173">3</span><span class="sxs-lookup"><span data-stu-id="6f6ce-173">3</span></span>     | <span data-ttu-id="6f6ce-174">Net 45</span><span class="sxs-lookup"><span data-stu-id="6f6ce-174">Net 45</span></span>        |
    | <span data-ttu-id="6f6ce-175">4</span><span class="sxs-lookup"><span data-stu-id="6f6ce-175">4</span></span>     | <span data-ttu-id="6f6ce-176">Net 60</span><span class="sxs-lookup"><span data-stu-id="6f6ce-176">Net 60</span></span>        |

## <a name="power-query"></a><span data-ttu-id="6f6ce-177">Power Query</span><span class="sxs-lookup"><span data-stu-id="6f6ce-177">Power Query</span></span>

<span data-ttu-id="6f6ce-178">如果满足以下条件，则必须使用 Microsoft Power Query for Excel：</span><span class="sxs-lookup"><span data-stu-id="6f6ce-178">You must use Microsoft Power Query for Excel to filter data if the following conditions are met:</span></span>

- <span data-ttu-id="6f6ce-179">您在 Microsoft Dynamics 365 for Sales 中有销售订单。</span><span class="sxs-lookup"><span data-stu-id="6f6ce-179">You have sales orders in Microsoft Dynamics 365 for Sales.</span></span>
- <span data-ttu-id="6f6ce-180">您在 Project Service Automation 中有多个组织单位，并且这些组织单位将映射到 Finance and Operations 中的多个法人。</span><span class="sxs-lookup"><span data-stu-id="6f6ce-180">You have multiple organizational units in Project Service Automation, and these organizational units will be mapped to multiple legal entities in Finance and Operations.</span></span>

<span data-ttu-id="6f6ce-181">如果必须使用 Power Query，请遵守以下准则：</span><span class="sxs-lookup"><span data-stu-id="6f6ce-181">If you must use Power Query, follow these guidelines:</span></span>

- <span data-ttu-id="6f6ce-182">项目和合同（PSA 到 Fin and Ops）模板有一个默认筛选器，其中仅包含类型为**工作项 (msdyn\_ordertype = 192350001)** 的销售订单。</span><span class="sxs-lookup"><span data-stu-id="6f6ce-182">The Projects and contracts (PSA to Fin and Ops) template has a default filter that includes only sales orders of the **Work item (msdyn\_ordertype = 192350001)** type.</span></span> <span data-ttu-id="6f6ce-183">此筛选器有助于确保不在 Finance and Operations 中为销售订单创建项目合同。</span><span class="sxs-lookup"><span data-stu-id="6f6ce-183">This filter helps guarantee that project contracts aren't created for sales orders in Finance and Operations.</span></span> <span data-ttu-id="6f6ce-184">如果创建自己的模板，则必须添加这个筛选器。</span><span class="sxs-lookup"><span data-stu-id="6f6ce-184">If you create your own template, you must add this filter.</span></span>
- <span data-ttu-id="6f6ce-185">创建的 Power Query 筛选器必须仅包含应同步到集成连接集的法人的合同组织。</span><span class="sxs-lookup"><span data-stu-id="6f6ce-185">You must create a Power Query filter that includes only the contract organizations that should be synchronized to the legal entity of the integration connection set.</span></span> <span data-ttu-id="6f6ce-186">例如，应将您的包含合同组织单位 Contoso US 的项目合同同步到 USSI 法人，但您的包含合同组织单位 Contoso Global 的项目合同则应同步到 USMF 法人。</span><span class="sxs-lookup"><span data-stu-id="6f6ce-186">For example, project contracts that you have with the contract organizational unit of Contoso US should be synchronized to the USSI legal entity, but project contracts that you have with the contract organizational unit of Contoso Global should be synchronized to the USMF legal entity.</span></span> <span data-ttu-id="6f6ce-187">如果不向任务映射添加此筛选器，则将把所有项目合同同步到为连接集定义的法人，而不考虑合同组织单位。</span><span class="sxs-lookup"><span data-stu-id="6f6ce-187">If you don't add this filter to your task mapping, all project contracts will be synchronized to the legal entity that is defined for the connection set, regardless of the contract organizational unit.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="6f6ce-188">数据集成中的模板映射</span><span class="sxs-lookup"><span data-stu-id="6f6ce-188">Template mapping in Data integration</span></span>

> [!NOTE] 
> <span data-ttu-id="6f6ce-189">项目合同的默认映射中不包含 **CustomerReference**、**AddressCity**、**AddressCountryRegionID**、**AddressDescription**、**AddressLine1**、**AddressLine2**、**AddressState** 和 **AddressZipCode** 字段。</span><span class="sxs-lookup"><span data-stu-id="6f6ce-189">The **CustomerReference**, **AddressCity**, **AddressCountryRegionID**, **AddressDescription**, **AddressLine1**, **AddressLine2**, **AddressState**, and **AddressZipCode** fields aren't included in the default mapping for project contracts.</span></span> <span data-ttu-id="6f6ce-190">如果需要为项目合同同步此数据，可添加这些映射。</span><span class="sxs-lookup"><span data-stu-id="6f6ce-190">You can add the mappings if you require that this data be synchronized for project contracts.</span></span>
>
> <span data-ttu-id="6f6ce-191">项目的默认映射中不包含 **Description**、**ParentID**、**ProjectGroup**、**ProjectManagerPersonnelNumber** 和 **ProjectType** 字段。</span><span class="sxs-lookup"><span data-stu-id="6f6ce-191">The **Description**, **ParentID**, **ProjectGroup**, **ProjectManagerPersonnelNumber**, and **ProjectType** fields aren't included in the default mapping for projects.</span></span> <span data-ttu-id="6f6ce-192">如果需要为项目同步此数据，可添加这些映射。</span><span class="sxs-lookup"><span data-stu-id="6f6ce-192">You can add the mappings if you require that this data be synchronized for projects.</span></span>

<span data-ttu-id="6f6ce-193">下图显示了数据集成中的模板任务映射的示例。</span><span class="sxs-lookup"><span data-stu-id="6f6ce-193">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="6f6ce-194">此映射显示将从 Project Service Automation 同步到 Finance and Operations 的字段信息。</span><span class="sxs-lookup"><span data-stu-id="6f6ce-194">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="6f6ce-195">[![模板映射](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)</span><span class="sxs-lookup"><span data-stu-id="6f6ce-195">[![Template mapping](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)</span></span>

<span data-ttu-id="6f6ce-196">[![模板映射](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)</span><span class="sxs-lookup"><span data-stu-id="6f6ce-196">[![Template mapping](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)</span></span>

<span data-ttu-id="6f6ce-197">[![模板映射](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)</span><span class="sxs-lookup"><span data-stu-id="6f6ce-197">[![Template mapping](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)</span></span>

<span data-ttu-id="6f6ce-198">[![模板映射](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)</span><span class="sxs-lookup"><span data-stu-id="6f6ce-198">[![Template mapping](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)</span></span>
