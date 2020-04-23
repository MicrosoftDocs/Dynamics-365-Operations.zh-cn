---
title: 配置扣缴
description: 在 Microsoft Dynamics 365 Human Resources 中使用扣缴确定从员工的工资中扣除每种福利的多少（如果有）。
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5e645c3f098163626cb686aba347897781d7ebc0
ms.sourcegitcommit: a9461650d11d6845e1942865ebf7e35f75f61ad3
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/06/2020
ms.locfileid: "3230054"
---
# <a name="configure-deductions"></a><span data-ttu-id="31717-103">配置扣缴</span><span class="sxs-lookup"><span data-stu-id="31717-103">Configure deductions</span></span>

<span data-ttu-id="31717-104">在 Microsoft Dynamics 365 Human Resources 中使用扣缴确定从员工的工资中扣除每种福利的多少（如果有）。</span><span class="sxs-lookup"><span data-stu-id="31717-104">Use deductions in Microsoft Dynamics 365 Human Resources to determine how much, if any, to deduct from an employee’s paycheck for each benefit.</span></span> <span data-ttu-id="31717-105">扣缴是有有效日期的，因此您可以保留扣缴信息的历史记录。</span><span class="sxs-lookup"><span data-stu-id="31717-105">Deductions are date-effective, so you can keep a historical record of deduction information.</span></span> 

1. <span data-ttu-id="31717-106">在**福利管理**工作区中，在**设置**下，选择**扣缴**。</span><span class="sxs-lookup"><span data-stu-id="31717-106">In the **Benefits management** workspace, under **Setup**, select **Deductions**.</span></span>

2. <span data-ttu-id="31717-107">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="31717-107">Select **New**.</span></span>

3. <span data-ttu-id="31717-108">为以下字段指定值：</span><span class="sxs-lookup"><span data-stu-id="31717-108">Specify values for the following fields:</span></span>

   | <span data-ttu-id="31717-109">字段</span><span class="sxs-lookup"><span data-stu-id="31717-109">Field</span></span> | <span data-ttu-id="31717-110">说明</span><span class="sxs-lookup"><span data-stu-id="31717-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="31717-111">**扣除额**</span><span class="sxs-lookup"><span data-stu-id="31717-111">**Deduction**</span></span> | <span data-ttu-id="31717-112">用于标识福利扣缴的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="31717-112">A unique ID that is used to identify the benefit deduction.</span></span> |
   | <span data-ttu-id="31717-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="31717-113">**Description**</span></span> | <span data-ttu-id="31717-114">扣缴的描述。</span><span class="sxs-lookup"><span data-stu-id="31717-114">A description for the deduction.</span></span> |
   | <span data-ttu-id="31717-115">**生效**</span><span class="sxs-lookup"><span data-stu-id="31717-115">**Effective**</span></span> | <span data-ttu-id="31717-116">开始日期。</span><span class="sxs-lookup"><span data-stu-id="31717-116">The start date.</span></span> <span data-ttu-id="31717-117">默认值为当前系统日期。</span><span class="sxs-lookup"><span data-stu-id="31717-117">The default value is the current system date.</span></span> |
   | <span data-ttu-id="31717-118">**到期**</span><span class="sxs-lookup"><span data-stu-id="31717-118">**Expiration**</span></span> | <span data-ttu-id="31717-119">结束日期。</span><span class="sxs-lookup"><span data-stu-id="31717-119">The end date.</span></span> <span data-ttu-id="31717-120">默认值为 12/31/2154，表示永不。</span><span class="sxs-lookup"><span data-stu-id="31717-120">The default value is 12/31/2154, which signifies never.</span></span> |
   | <span data-ttu-id="31717-121">**标题**</span><span class="sxs-lookup"><span data-stu-id="31717-121">**Heading**</span></span> | <span data-ttu-id="31717-122">在处理工资单的福利时，该扣缴针对扣缴中员工部分所使用的工资系统中的标题代码。</span><span class="sxs-lookup"><span data-stu-id="31717-122">The heading code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="31717-123">这在您使用第三方工资单提供程序时会用到。</span><span class="sxs-lookup"><span data-stu-id="31717-123">This is used when you use a third-party payroll provider.</span></span> |
   | <span data-ttu-id="31717-124">**员工工资扣缴引用**</span><span class="sxs-lookup"><span data-stu-id="31717-124">**Employee payroll deduction reference**</span></span> | <span data-ttu-id="31717-125">在处理工资单的福利时，该扣缴针对扣缴中员工部分所使用的工资系统中的代码。</span><span class="sxs-lookup"><span data-stu-id="31717-125">The deduction code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> |
   | <span data-ttu-id="31717-126">**金额标题**</span><span class="sxs-lookup"><span data-stu-id="31717-126">**Amount heading**</span></span> | <span data-ttu-id="31717-127">在处理工资单的福利时，该扣缴金额针对扣缴中员工部分所使用的工资系统中的标题代码。</span><span class="sxs-lookup"><span data-stu-id="31717-127">The heading code from the payroll system that this deduction amount will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="31717-128">这通常在您使用第三方工资单提供程序时会用到。</span><span class="sxs-lookup"><span data-stu-id="31717-128">This is normally used when you use a third-party payroll provider.</span></span> |
   | <span data-ttu-id="31717-129">**可以删除**</span><span class="sxs-lookup"><span data-stu-id="31717-129">**Can delete**</span></span> | <span data-ttu-id="31717-130">指定从 Dynamics 365 for Finance and Operations 导出的值是否可以让该值在工资系统中删除。</span><span class="sxs-lookup"><span data-stu-id="31717-130">Specifies whether an exported value from Dynamics 365 for Finance and Operations can cause the value to be deleted in the payroll system.</span></span> |
   | <span data-ttu-id="31717-131">**已配对的列**</span><span class="sxs-lookup"><span data-stu-id="31717-131">**Paired columns**</span></span> | <span data-ttu-id="31717-132">指定是否将已配对的相邻列中的标题和扣缴金额导出到工资系统。</span><span class="sxs-lookup"><span data-stu-id="31717-132">Specifies whether to export heading and deduction amount in paired adjacent columns to the payroll system.</span></span> |
   | <span data-ttu-id="31717-133">**更改生效日期**</span><span class="sxs-lookup"><span data-stu-id="31717-133">**Change effective date**</span></span> | <span data-ttu-id="31717-134">福利扣缴更改的生效日期。</span><span class="sxs-lookup"><span data-stu-id="31717-134">The date when the benefit deduction change will become effective.</span></span> <span data-ttu-id="31717-135">在此日期，只要您运行**扣缴更改更新**处理，系统将自动更改福利扣缴并更新与此扣缴相关联的所有福利计划。</span><span class="sxs-lookup"><span data-stu-id="31717-135">On this date, the system automatically changes the benefit deduction and updates all benefit plans associated with this deduction, as long as you run **Deduction change update** processing.</span></span> |
   | <span data-ttu-id="31717-136">**已完成扣缴更改**</span><span class="sxs-lookup"><span data-stu-id="31717-136">**Deduction change completed**</span></span> | <span data-ttu-id="31717-137">在扣缴更新更改处理完成福利扣缴更改后，将自动选中**已完成扣缴更改**复选框。</span><span class="sxs-lookup"><span data-stu-id="31717-137">The **Deduction change completed** check box will be automatically selected once the benefit deduction changes have been completed by Deduction update change processing.</span></span> |
   
4. <span data-ttu-id="31717-138">要跟踪并维护对福利比率设置的更改，请选择**操作**，然后选择**维护版本**。</span><span class="sxs-lookup"><span data-stu-id="31717-138">To track and maintain changes to the benefit rate setup, select **Actions**, and then select **Maintain versions**.</span></span>

5. <span data-ttu-id="31717-139">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="31717-139">Select **Save**.</span></span> 
