---
title: "服务协议和项目的集成"
description: "在您处理服务协议和服务协议行时，使用在“项目管理与核算”中的区域中设置的数据。"
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjParameters
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
ms.openlocfilehash: 9f2640eae299411d633c68795bc16883dbb5eeaf
ms.contentlocale: zh-cn
ms.lasthandoff: 05/08/2018

---

# <a name="integration-for-service-agreements-and-projects"></a><span data-ttu-id="91238-103">服务协议和项目的集成</span><span class="sxs-lookup"><span data-stu-id="91238-103">Integration for service agreements and projects</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="91238-104">在您处理服务协议和服务协议行时，使用在**项目管理与核算**中的以下区域中设置的数据。</span><span class="sxs-lookup"><span data-stu-id="91238-104">When you work with service agreements and service agreement lines, you use data that is set up in the following areas in **Project management and accounting**.</span></span>

## <a name="project-prices"></a><span data-ttu-id="91238-105">项目价格</span><span class="sxs-lookup"><span data-stu-id="91238-105">Project prices</span></span>

<span data-ttu-id="91238-106">服务协议交易记录的成本和销售价从应用于附加到该服务协议的项目的成本价设置派生。</span><span class="sxs-lookup"><span data-stu-id="91238-106">The cost and the sales price for a service agreement transaction are derived from the cost price setup that applies to the project that is attached to the service agreement.</span></span> <span data-ttu-id="91238-107">可以按项目、员工和类别设置成本价和销售价。</span><span class="sxs-lookup"><span data-stu-id="91238-107">Cost and sales prices can be set up by project, employee, and category.</span></span> 

## <a name="project-validation"></a><span data-ttu-id="91238-108">项目验证</span><span class="sxs-lookup"><span data-stu-id="91238-108">Project validation</span></span>

<span data-ttu-id="91238-109">可通过**项目管理与核算**中的验证设置，限制可用于服务协议行上选定内容的项目、员工和类别。</span><span class="sxs-lookup"><span data-stu-id="91238-109">The projects, employees, and categories that are available for selection on a service agreement line can be limited by the validation setup in **Project management and accounting**.</span></span> <span data-ttu-id="91238-110">使用验证设置，您可以将员工、项目和类别结合起来用于控制访问。</span><span class="sxs-lookup"><span data-stu-id="91238-110">By using the validation setup, you can combine employees, projects, and categories for control access.</span></span> 

## <a name="project-line-properties"></a><span data-ttu-id="91238-111">项目行属性</span><span class="sxs-lookup"><span data-stu-id="91238-111">Project line properties</span></span>

<span data-ttu-id="91238-112">为服务协议行自动输入记录属性。</span><span class="sxs-lookup"><span data-stu-id="91238-112">A line property is entered automatically for a service agreement line.</span></span>

<span data-ttu-id="91238-113">行属性在**项目管理与核算**中的**行属性**窗体中创建。</span><span class="sxs-lookup"><span data-stu-id="91238-113">Line properties are created in the **Line properties** form in **Project management and accounting**.</span></span> <span data-ttu-id="91238-114">记录属性在“”的“”窗体中创建，在某一服务协议上输入的记录属性将附加到为该服务协议选择的项目，并且该记录属性以后将由服务协议行继承。</span><span class="sxs-lookup"><span data-stu-id="91238-114">The line property that is entered on a service agreement is attached to the project that is selected for the service agreement and inherited subsequently by the service agreement line.</span></span> 

## <a name="default-offset-accounts"></a><span data-ttu-id="91238-115">默认对方科目</span><span class="sxs-lookup"><span data-stu-id="91238-115">Default offset accounts</span></span>

<span data-ttu-id="91238-116">如果您输入某一支出交易记录，则自动为该交易记录选择默认的支出对方科目。</span><span class="sxs-lookup"><span data-stu-id="91238-116">If you enter an expense transaction, a default expense offset account is selected automatically for the transaction.</span></span> <span data-ttu-id="91238-117">针对附加到当前服务协议的项目设置默认的支出帐户。</span><span class="sxs-lookup"><span data-stu-id="91238-117">The default expense account is set up for the project that is attached to the current service agreement.</span></span>

## <a name="project-categories"></a><span data-ttu-id="91238-118">项目类别</span><span class="sxs-lookup"><span data-stu-id="91238-118">Project categories</span></span>

<span data-ttu-id="91238-119">可用于服务协议行的类别在**项目管理与核算**中的**项目类别**窗体中设置。</span><span class="sxs-lookup"><span data-stu-id="91238-119">The categories that are available for service agreement lines are set up in the **Project categories** form in **Project management and accounting**.</span></span> 

> [!NOTE]
> <P><span data-ttu-id="91238-120">在<STRONG>项目类别</STRONG>窗体<STRONG>项目</STRONG>选项卡中选中了<STRONG>在日记帐中有效</STRONG>复选框的类别可供选择。</span><span class="sxs-lookup"><span data-stu-id="91238-120">Categories that have the <STRONG>Active in journals</STRONG> check box selected on the <STRONG>Project</STRONG> tab in the <STRONG>Project categories</STRONG> form are available for selection.</span></span> <span data-ttu-id="91238-121">但是，如果选中了<STRONG>项目管理与核算参数</STRONG>窗体<STRONG>日记帐</STRONG>选项卡中的<STRONG>无效类别</STRONG>复选框，则所有类别均可供选择。</span><span class="sxs-lookup"><span data-stu-id="91238-121">However, if the <STRONG>Inactive categories</STRONG> check box is selected on the <STRONG>Journals</STRONG> tab in the <STRONG>Project management and accounting parameters</STRONG> form, all categories are available for selection.</span></span></P>

## <a name="project-parameters"></a><span data-ttu-id="91238-122">项目参数</span><span class="sxs-lookup"><span data-stu-id="91238-122">Project parameters</span></span>

<span data-ttu-id="91238-123">如果选中了**项目管理与核算参数**窗体**日记帐**选项卡中的**已离职工作人员**字段，则可在**服务协议**和**服务订单**窗体中选择已离职员工和有效员工。</span><span class="sxs-lookup"><span data-stu-id="91238-123">If the **Terminated workers** field on the **Journals** tab in the **Project management and accounting parameters** form is selected, you can select inactive employees and active employees in the **Service agreements** and **Service orders** forms.</span></span>

<span data-ttu-id="91238-124">此外，您可以在**服务订单**中的**项目**选项卡上启用**开始时间**和**结束时间**字段，以便针对服务订单行输入开始时间和结束时间。</span><span class="sxs-lookup"><span data-stu-id="91238-124">Also, you can enable the **Start time** and **End time** fields on the **Project** tab in the **Service orders** form to enter starting and ending times on service order lines.</span></span>

## <a name="enable-the-starting-and-ending-time-feature-for-service-orders"></a><span data-ttu-id="91238-125">启用服务订单的开始和结束时间功能</span><span class="sxs-lookup"><span data-stu-id="91238-125">Enable the starting and ending time feature for service orders</span></span>

1.  <span data-ttu-id="91238-126">单击**项目管理与核算** \> **设置** \> **项目管理与核算参数**。</span><span class="sxs-lookup"><span data-stu-id="91238-126">Click **Project management and accounting** \> **Setup** \> **Project management and accounting parameters**.</span></span>

2.  <span data-ttu-id="91238-127">单击**日记帐**选项卡，然后选中**显示开始/结束时间**复选框。</span><span class="sxs-lookup"><span data-stu-id="91238-127">Click the **Journals** tab, and then select the **Show start/end times** check box.</span></span>

3.  <span data-ttu-id="91238-128">单击**项目管理与核算** \> **设置** \> **日记帐** \> **日记帐名称**。</span><span class="sxs-lookup"><span data-stu-id="91238-128">Click **Project management and accounting** \> **Setup** \> **Journals** \> **Journal names**.</span></span>

4.  <span data-ttu-id="91238-129">选择附加到该服务订单的日志名称。</span><span class="sxs-lookup"><span data-stu-id="91238-129">Select the journal name that is attached to the service order.</span></span>

5.  <span data-ttu-id="91238-130">单击**常规**选项卡，然后选中**显示开始/结束时间**复选框。</span><span class="sxs-lookup"><span data-stu-id="91238-130">Click the **General** tab, and then select the **Show start/end times** check box.</span></span>


> [!NOTE]
> <P><span data-ttu-id="91238-131">在<STRONG>服务管理参数</STRONG>窗体<STRONG>日记帐</STRONG>选项卡上的<STRONG>工时</STRONG>字段中，为该服务订单选择日志名称。</span><span class="sxs-lookup"><span data-stu-id="91238-131">Select the journal name for the service order in the <STRONG>Hour</STRONG> field on the <STRONG>Journals</STRONG> tab in the <STRONG>Service management parameters</STRONG> form.</span></span></P>






