---
title: 配置扣缴
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
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
ms.openlocfilehash: 7ee9e8f3bc0e9027e41d3aa91bd097a3f046cbb4
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008244"
---
# <a name="configure-deductions"></a><span data-ttu-id="576db-102">配置扣缴</span><span class="sxs-lookup"><span data-stu-id="576db-102">Configure deductions</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="576db-103">在 Microsoft Dynamics 365 Human Resources 中使用扣缴确定从员工的工资中扣除每种福利的多少（如果有）。</span><span class="sxs-lookup"><span data-stu-id="576db-103">Use deductions in Microsoft Dynamics 365 Human Resources to determine how much, if any, to deduct from an employee’s paycheck for each benefit.</span></span> <span data-ttu-id="576db-104">扣缴是有有效日期的，因此您可以保留扣缴信息的历史记录。</span><span class="sxs-lookup"><span data-stu-id="576db-104">Deductions are date effective, so you can keep a historical record of deduction information.</span></span> 

1. <span data-ttu-id="576db-105">在**福利管理**工作区中，在**设置**下，选择**扣缴**。</span><span class="sxs-lookup"><span data-stu-id="576db-105">In the **Benefits management** workspace, under **Setup**, select **Deductions**.</span></span>

2. <span data-ttu-id="576db-106">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="576db-106">Select **New**.</span></span>

3. <span data-ttu-id="576db-107">为以下字段指定值：</span><span class="sxs-lookup"><span data-stu-id="576db-107">Specify values for the following fields:</span></span>

   | <span data-ttu-id="576db-108">字段</span><span class="sxs-lookup"><span data-stu-id="576db-108">Field</span></span> | <span data-ttu-id="576db-109">说明</span><span class="sxs-lookup"><span data-stu-id="576db-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="576db-110">扣除额</span><span class="sxs-lookup"><span data-stu-id="576db-110">Deduction</span></span> | <span data-ttu-id="576db-111">用于标识福利扣缴的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="576db-111">A unique ID that is used to identify the benefit deduction.</span></span> |
   | <span data-ttu-id="576db-112">说明</span><span class="sxs-lookup"><span data-stu-id="576db-112">Description</span></span> | <span data-ttu-id="576db-113">扣缴的描述。</span><span class="sxs-lookup"><span data-stu-id="576db-113">A description for the deduction.</span></span> |
   | <span data-ttu-id="576db-114">生效</span><span class="sxs-lookup"><span data-stu-id="576db-114">Effective</span></span> | <span data-ttu-id="576db-115">开始日期。</span><span class="sxs-lookup"><span data-stu-id="576db-115">The start date.</span></span> <span data-ttu-id="576db-116">默认值为当前系统日期。</span><span class="sxs-lookup"><span data-stu-id="576db-116">The default value is the current system date.</span></span> |
   | <span data-ttu-id="576db-117">到期</span><span class="sxs-lookup"><span data-stu-id="576db-117">Expiration</span></span> | <span data-ttu-id="576db-118">结束日期。</span><span class="sxs-lookup"><span data-stu-id="576db-118">The end date.</span></span> <span data-ttu-id="576db-119">默认值为 12/31/2154，表示永不。</span><span class="sxs-lookup"><span data-stu-id="576db-119">The default value is 12/31/2154, which signifies never.</span></span> |
   | <span data-ttu-id="576db-120">标题</span><span class="sxs-lookup"><span data-stu-id="576db-120">Heading</span></span> | <span data-ttu-id="576db-121">在处理工资单的福利时，该扣缴针对扣缴中员工部分所使用的工资系统中的标题代码。</span><span class="sxs-lookup"><span data-stu-id="576db-121">The heading code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="576db-122">这在您使用第三方工资单提供程序时会用到。</span><span class="sxs-lookup"><span data-stu-id="576db-122">This is used when you use a third party payroll provider.</span></span> |
   | <span data-ttu-id="576db-123">员工工资扣缴引用</span><span class="sxs-lookup"><span data-stu-id="576db-123">Employee payroll deduction reference</span></span> | <span data-ttu-id="576db-124">在处理工资单的福利时，该扣缴针对扣缴中员工部分所使用的工资系统中的代码。</span><span class="sxs-lookup"><span data-stu-id="576db-124">The deduction code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> |
   | <span data-ttu-id="576db-125">金额标题</span><span class="sxs-lookup"><span data-stu-id="576db-125">Amount heading</span></span> | <span data-ttu-id="576db-126">在处理工资单的福利时，该扣缴金额针对扣缴中员工部分所使用的工资系统中的标题代码。</span><span class="sxs-lookup"><span data-stu-id="576db-126">The heading code from the payroll system that this deduction amount will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="576db-127">这通常在您使用第三方工资单提供程序时会用到。</span><span class="sxs-lookup"><span data-stu-id="576db-127">This is normally used when you use a third party payroll provider.</span></span> |
   | <span data-ttu-id="576db-128">可以删除</span><span class="sxs-lookup"><span data-stu-id="576db-128">Can delete</span></span> | <span data-ttu-id="576db-129">指定从 Dynamics 365 for Finance and Operations 导出的值是否可以让该值在工资系统中删除。</span><span class="sxs-lookup"><span data-stu-id="576db-129">Specifies whether an exported value from Dynamics 365 for Finance and Operations can cause the value to be deleted in the payroll system.</span></span> |
   | <span data-ttu-id="576db-130">已配对的列</span><span class="sxs-lookup"><span data-stu-id="576db-130">Paired columns</span></span> | <span data-ttu-id="576db-131">指定是否将已配对的相邻列中的标题和扣缴金额导出到工资系统。</span><span class="sxs-lookup"><span data-stu-id="576db-131">Specifies whether to export heading and deduction amount in paired adjacent columns to the payroll system.</span></span> |
   | <span data-ttu-id="576db-132">更改生效日期</span><span class="sxs-lookup"><span data-stu-id="576db-132">Change effective date</span></span> | <span data-ttu-id="576db-133">福利扣缴更改的生效日期。</span><span class="sxs-lookup"><span data-stu-id="576db-133">The date when the benefit deduction change will become effective.</span></span> <span data-ttu-id="576db-134">在此日期，只要您运行扣缴更改更新处理，系统将自动更改福利扣缴并更新与此扣缴相关联的所有福利计划。</span><span class="sxs-lookup"><span data-stu-id="576db-134">On this date the system will automatically change the benefit deduction and update all benefit plans associated with this deduction, as long as you run Deduction change update processing.</span></span> |
   | <span data-ttu-id="576db-135">已完成扣缴更改</span><span class="sxs-lookup"><span data-stu-id="576db-135">Deduction change completed</span></span> | <span data-ttu-id="576db-136">在扣缴更新更改处理完成福利扣缴更改后，将自动选中“已完成扣缴更改”复选框。</span><span class="sxs-lookup"><span data-stu-id="576db-136">The Deduction change completed check box will be automatically selected once the benefit deduction changes have been completed by Deduction update change processing.</span></span> |
   
4. <span data-ttu-id="576db-137">要跟踪并维护对福利比率设置的更改，请选择**操作**，然后选择**维护版本**。</span><span class="sxs-lookup"><span data-stu-id="576db-137">To track and maintain changes to the benefit rate setup, select **Actions**, and then select **Maintain versions**.</span></span>

5. <span data-ttu-id="576db-138">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="576db-138">Select **Save**.</span></span> 
