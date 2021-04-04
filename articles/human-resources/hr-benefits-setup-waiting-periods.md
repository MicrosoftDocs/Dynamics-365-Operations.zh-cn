---
title: 配置等待时段
description: 在 Microsoft Dynamics 365 Human Resources 中，等待天数建立用于福利计划的里程碑。
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0e08c0c02393506e1e292676c954bdf3850029f7
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/17/2021
ms.locfileid: "5468291"
---
# <a name="configure-waiting-periods"></a><span data-ttu-id="f491c-103">配置等待时段</span><span class="sxs-lookup"><span data-stu-id="f491c-103">Configure waiting periods</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="f491c-104">在 Microsoft Dynamics 365 Human Resources 中，等待天数建立用于福利计划的里程碑。</span><span class="sxs-lookup"><span data-stu-id="f491c-104">In Microsoft Dynamics 365 Human Resources, waiting days establish a milestone to use for benefit plans.</span></span> <span data-ttu-id="f491c-105">例如，从雇用日期起三个月，每个月的第一天，或六个月。</span><span class="sxs-lookup"><span data-stu-id="f491c-105">For example, three months from hire date, the first of each month, or six months.</span></span>   

1. <span data-ttu-id="f491c-106">在 **福利管理** 工作区中，在 **设置** 下，选择 **等待期间**。</span><span class="sxs-lookup"><span data-stu-id="f491c-106">In the **Benefits management** workspace, under **Setup**, select **Waiting periods**.</span></span>

2. <span data-ttu-id="f491c-107">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="f491c-107">Select **New**.</span></span>

3. <span data-ttu-id="f491c-108">为以下字段指定值：</span><span class="sxs-lookup"><span data-stu-id="f491c-108">Specify values for the following fields:</span></span>

   | <span data-ttu-id="f491c-109">字段</span><span class="sxs-lookup"><span data-stu-id="f491c-109">Field</span></span> | <span data-ttu-id="f491c-110">说明</span><span class="sxs-lookup"><span data-stu-id="f491c-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="f491c-111">**等待代码**</span><span class="sxs-lookup"><span data-stu-id="f491c-111">**Waiting code**</span></span> | <span data-ttu-id="f491c-112">等待期间的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="f491c-112">A unique identifier for the waiting period.</span></span> |
   | <span data-ttu-id="f491c-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="f491c-113">**Description**</span></span> | <span data-ttu-id="f491c-114">等待期间的描述。</span><span class="sxs-lookup"><span data-stu-id="f491c-114">A description of the waiting period.</span></span> |
   | <span data-ttu-id="f491c-115">**等待方法**</span><span class="sxs-lookup"><span data-stu-id="f491c-115">**Waiting method**</span></span> | <span data-ttu-id="f491c-116">从值的下拉列表中选择合适的等待方法。</span><span class="sxs-lookup"><span data-stu-id="f491c-116">Select the appropriate waiting method from the drop-down list of values.</span></span> <span data-ttu-id="f491c-117">选项包括“净”、“当前月份”、“当前季度”、“当前年度”和“当前周”。</span><span class="sxs-lookup"><span data-stu-id="f491c-117">Options are Net, Current month, Current quarter, Current year, and Current week.</span></span> |
   | <span data-ttu-id="f491c-118">**月数**</span><span class="sxs-lookup"><span data-stu-id="f491c-118">**Months**</span></span> | <span data-ttu-id="f491c-119">输入要加到等待方法的月数以计算等待日期。</span><span class="sxs-lookup"><span data-stu-id="f491c-119">Enter the number of months to add to the waiting method to calculate the waiting date.</span></span> |
   | <span data-ttu-id="f491c-120">**天数**</span><span class="sxs-lookup"><span data-stu-id="f491c-120">**Days**</span></span> | <span data-ttu-id="f491c-121">输入要加到等待方法的天数以计算等待日期。</span><span class="sxs-lookup"><span data-stu-id="f491c-121">Enter the number of days to add to the waiting method to calculate the waiting date.</span></span> |
   | <span data-ttu-id="f491c-122">**等待天数**</span><span class="sxs-lookup"><span data-stu-id="f491c-122">**Waiting day**</span></span> | <span data-ttu-id="f491c-123">选择要用于计算等待日期的等待天数。</span><span class="sxs-lookup"><span data-stu-id="f491c-123">Select the waiting day to use to calculate the waiting date.</span></span> |

4. <span data-ttu-id="f491c-124">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="f491c-124">Select **Save**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]