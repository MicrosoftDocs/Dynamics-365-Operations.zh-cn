---
title: 创建工作人员福利计划
description: 您可以在 Microsoft Dynamics 365 Human Resources 中创建工作人员福利计划，来为员工选择福利计划并确认福利计划的选择。
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitPlanEmployee, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 27ef56efc39b6cfc605122e499bc249963322ac6
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/18/2021
ms.locfileid: "6059032"
---
# <a name="create-worker-benefit-plans"></a><span data-ttu-id="a5cfe-103">创建工作人员福利计划</span><span class="sxs-lookup"><span data-stu-id="a5cfe-103">Create worker benefit plans</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="a5cfe-104">您可以在 Microsoft Dynamics 365 Human Resources 中创建工作人员福利计划，来为员工选择福利计划并确认福利计划的选择。</span><span class="sxs-lookup"><span data-stu-id="a5cfe-104">You can create worker benefit plans in Microsoft Dynamics 365 Human Resources to select benefit plans for employees and to confirm benefit plan selections.</span></span> <span data-ttu-id="a5cfe-105">通常，员工使用员工自助服务自行选择福利计划，然后福利管理员确认选择。</span><span class="sxs-lookup"><span data-stu-id="a5cfe-105">Typically, employees select benefit plans themselves by using Employee self service, and then a benefits administrator confirms the selections.</span></span> 

1. <span data-ttu-id="a5cfe-106">在 **福利管理** 工作区中，在 **计划** 下，选择 **工作人员福利计划**。</span><span class="sxs-lookup"><span data-stu-id="a5cfe-106">In the **Benefits management** workspace, under **Plans**, select **Worker benefit plans**.</span></span>

2. <span data-ttu-id="a5cfe-107">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="a5cfe-107">Select **New**.</span></span>

3. <span data-ttu-id="a5cfe-108">为以下字段指定值：</span><span class="sxs-lookup"><span data-stu-id="a5cfe-108">Specify values for the following fields:</span></span>

   | <span data-ttu-id="a5cfe-109">字段</span><span class="sxs-lookup"><span data-stu-id="a5cfe-109">Field</span></span> | <span data-ttu-id="a5cfe-110">说明</span><span class="sxs-lookup"><span data-stu-id="a5cfe-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="a5cfe-111">期间余额</span><span class="sxs-lookup"><span data-stu-id="a5cfe-111">Period</span></span> | <span data-ttu-id="a5cfe-112">在“计划”快速选项卡中指定用于筛选计划的福利期间。筛选计划以帮助您选择所有计划记录的子集，以便可以确认该子集。</span><span class="sxs-lookup"><span data-stu-id="a5cfe-112">Specifies a benefits period to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> <span data-ttu-id="a5cfe-113">例如，选择一个您创建的称为 2015 的期间，来确认 2015 年的所有福利登记选择。</span><span class="sxs-lookup"><span data-stu-id="a5cfe-113">For example, select a period you created called 2015 to confirm all the benefit enrollment selections for 2015.</span></span> |
   | <span data-ttu-id="a5cfe-114">工作人员</span><span class="sxs-lookup"><span data-stu-id="a5cfe-114">Worker</span></span> | <span data-ttu-id="a5cfe-115">在“计划”快速选项卡中指定用于筛选计划的工作人员。筛选计划以帮助您选择所有计划记录的子集，以便可以确认该子集。</span><span class="sxs-lookup"><span data-stu-id="a5cfe-115">Specifies a worker to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="a5cfe-116">法人</span><span class="sxs-lookup"><span data-stu-id="a5cfe-116">Legal entity</span></span> | <span data-ttu-id="a5cfe-117">在“计划”快速选项卡中指定用于筛选计划的法人。筛选计划以帮助您选择所有计划记录的子集，以便可以确认该子集。</span><span class="sxs-lookup"><span data-stu-id="a5cfe-117">Specifies a legal entity to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="a5cfe-118">覆盖范围选项</span><span class="sxs-lookup"><span data-stu-id="a5cfe-118">Coverage option</span></span> | <span data-ttu-id="a5cfe-119">在“计划”快速选项卡中指定用于筛选计划的覆盖范围选项。筛选计划以帮助您选择所有计划记录的子集，以便可以确认该子集。</span><span class="sxs-lookup"><span data-stu-id="a5cfe-119">Specifies a coverage option to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="a5cfe-120">默认</span><span class="sxs-lookup"><span data-stu-id="a5cfe-120">Default</span></span> | <span data-ttu-id="a5cfe-121">根据是否为默认计划来筛选福利计划。</span><span class="sxs-lookup"><span data-stu-id="a5cfe-121">Filters the benefit plans based on whether they are a default plan.</span></span> <span data-ttu-id="a5cfe-122">筛选计划以帮助您选择所有计划记录的子集，以便您可以确认该子集。</span><span class="sxs-lookup"><span data-stu-id="a5cfe-122">Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="a5cfe-123">状态</span><span class="sxs-lookup"><span data-stu-id="a5cfe-123">Status</span></span> | <span data-ttu-id="a5cfe-124">根据状态筛选福利计划。</span><span class="sxs-lookup"><span data-stu-id="a5cfe-124">Filters benefit plans based on their status.</span></span> <span data-ttu-id="a5cfe-125">筛选计划以帮助您选择所有计划记录的子集，以便您可以确认该子集。</span><span class="sxs-lookup"><span data-stu-id="a5cfe-125">Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="a5cfe-126">确认单</span><span class="sxs-lookup"><span data-stu-id="a5cfe-126">Confirmation</span></span> | <span data-ttu-id="a5cfe-127">在“计划”快速选项卡中指定用于筛选计划的确认状态。筛选计划以帮助您选择所有计划记录的子集，以便可以确认该子集。</span><span class="sxs-lookup"><span data-stu-id="a5cfe-127">Specifies the confirmation status to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="a5cfe-128">取消</span><span class="sxs-lookup"><span data-stu-id="a5cfe-128">Cancellation</span></span> | <span data-ttu-id="a5cfe-129">在“计划”快速选项卡中指定用于筛选计划的取消状态。筛选计划以帮助您选择所有计划记录的子集，以便可以确认该子集。</span><span class="sxs-lookup"><span data-stu-id="a5cfe-129">Specifies the cancellation status to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="a5cfe-130">生效日期筛选器</span><span class="sxs-lookup"><span data-stu-id="a5cfe-130">Effective date filter</span></span> | <span data-ttu-id="a5cfe-131">根据计划是已到期、有效还是将来有效来筛选计划。</span><span class="sxs-lookup"><span data-stu-id="a5cfe-131">Filters the plans based on whether they’re expired, active, or will be active in the future.</span></span> <span data-ttu-id="a5cfe-132">在“计划”快速选项卡中选择与您要查看的计划相对应的复选框。</span><span class="sxs-lookup"><span data-stu-id="a5cfe-132">Select the check boxes that correspond to the plans you want to see in the Plans fast tab.</span></span> |
   | <span data-ttu-id="a5cfe-133">计划</span><span class="sxs-lookup"><span data-stu-id="a5cfe-133">Plans</span></span> | <span data-ttu-id="a5cfe-134">“计划”快速选项卡包含符合您指定的筛选条件的计划。</span><span class="sxs-lookup"><span data-stu-id="a5cfe-134">The Plans fast tab contains the plans that meet the filter criteria you specified.</span></span> <span data-ttu-id="a5cfe-135">每行包含 HR 人员设置的相关配置选项和员工选择的登记选择。</span><span class="sxs-lookup"><span data-stu-id="a5cfe-135">The relevant configuration options that were set by HR staff and the enrollment selections that were chosen by employees are included on each line.</span></span> <span data-ttu-id="a5cfe-136">“合格”字段指定计划选择是否存在验证冲突。</span><span class="sxs-lookup"><span data-stu-id="a5cfe-136">The Qualified field specifies whether there is a validation conflict with the plan selection.</span></span> |

4. <span data-ttu-id="a5cfe-137">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="a5cfe-137">Select **Save**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]