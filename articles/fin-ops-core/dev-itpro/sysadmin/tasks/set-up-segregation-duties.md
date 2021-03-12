---
title: 设置职责划分
description: 您可以设置规则，以分离必须由不同用户执行的任务。
author: peakerbl
manager: AnnBe
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bcbd32131f9980a4f55e91b9d7ad48171069f72e
ms.sourcegitcommit: 316200579dd5b04ad76f276a2ed6b0f55fa8c812
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/05/2021
ms.locfileid: "4826386"
---
# <a name="set-up-segregation-of-duties"></a><span data-ttu-id="d513a-103">设置职责划分</span><span class="sxs-lookup"><span data-stu-id="d513a-103">Set up segregation of duties</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d513a-104">您可以设置规则，以分离必须由不同用户执行的任务。</span><span class="sxs-lookup"><span data-stu-id="d513a-104">You can set up rules to separate tasks that must be performed by different users.</span></span> <span data-ttu-id="d513a-105">此概念被称作职责划分。</span><span class="sxs-lookup"><span data-stu-id="d513a-105">This concept is named segregation of duties.</span></span> <span data-ttu-id="d513a-106">例如，您可能不希望由同一人确认收到货物和处理向供应商付款的事宜。</span><span class="sxs-lookup"><span data-stu-id="d513a-106">For example, you might not want the same person to acknowledge the receipt of goods and to process payment to the vendor.</span></span> <span data-ttu-id="d513a-107">职责划分有助于您减少欺骗风险，并且它还有助于您检测错误或违规。</span><span class="sxs-lookup"><span data-stu-id="d513a-107">Segregation of duties helps you reduce the risk of fraud, and it also helps you detect errors or irregularities.</span></span> <span data-ttu-id="d513a-108">您还可以使用职责划分来执行内部控制策略。</span><span class="sxs-lookup"><span data-stu-id="d513a-108">You can also use segregation of duties to enforce internal control policies.</span></span> <span data-ttu-id="d513a-109">完成以下过程以创建规则。</span><span class="sxs-lookup"><span data-stu-id="d513a-109">Complete the following procedure to create a rule.</span></span> <span data-ttu-id="d513a-110">您必须是系统管理员，才能完成该过程。</span><span class="sxs-lookup"><span data-stu-id="d513a-110">You must be a system administrator to complete the procedure.</span></span>

1. <span data-ttu-id="d513a-111">转到 **系统管理** > **安全** > **职责划分** > **职责划分规则**。</span><span class="sxs-lookup"><span data-stu-id="d513a-111">Go to **System administration** > **Security** > **Segregation of duties** > **Segregation of duties rules**.</span></span>
2. <span data-ttu-id="d513a-112">单击 **新建**。</span><span class="sxs-lookup"><span data-stu-id="d513a-112">Click **New**.</span></span>
3. <span data-ttu-id="d513a-113">在 **名称** 字段中，为规则输入一个值。</span><span class="sxs-lookup"><span data-stu-id="d513a-113">In the **Name** field, type a value for the rule.</span></span>
4. <span data-ttu-id="d513a-114">在 **第一个职责** 字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="d513a-114">In the **First duty** field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="d513a-115">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="d513a-115">In the list, find and select the desired record.</span></span> <span data-ttu-id="d513a-116">选择由规则控制的第一个职责。</span><span class="sxs-lookup"><span data-stu-id="d513a-116">Select the first duty that is controlled by the rule.</span></span>
6. <span data-ttu-id="d513a-117">在 **第二个职责** 字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="d513a-117">In the **Second duty** field, click the drop-down button to open the lookup.</span></span> 
7. <span data-ttu-id="d513a-118">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="d513a-118">In the list, find and select the desired record.</span></span> <span data-ttu-id="d513a-119">选择由规则控制的第二个职责。</span><span class="sxs-lookup"><span data-stu-id="d513a-119">Select the second duty that is controlled by the rule.</span></span>
10. <span data-ttu-id="d513a-120">在 **严重性** 字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="d513a-120">In the **Severity** field, select an option.</span></span> <span data-ttu-id="d513a-121">选择在同一用户或角色同时履行两个职责时发生风险的严重性。</span><span class="sxs-lookup"><span data-stu-id="d513a-121">Select the severity of the risk that occurs when the same user or role performs both duties.</span></span>  
11. <span data-ttu-id="d513a-122">在 **安全风险** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="d513a-122">In the **Security risk** field, type a value.</span></span> <span data-ttu-id="d513a-123">输入安全风险的描述。</span><span class="sxs-lookup"><span data-stu-id="d513a-123">Enter a description of the security risk.</span></span>  
12. <span data-ttu-id="d513a-124">在 **安全降低** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="d513a-124">In the **Security mitigation** field, type a value.</span></span> <span data-ttu-id="d513a-125">输入您为减少安全风险而采取的行动的描述。</span><span class="sxs-lookup"><span data-stu-id="d513a-125">Enter a description of the actions that you take to mitigate the security risk.</span></span> <span data-ttu-id="d513a-126">例如，您可以通过更详细地审查流程，通过进行阅读管理审查，或者通过与其他部门共享资源，减少风险。</span><span class="sxs-lookup"><span data-stu-id="d513a-126">For example, you can mitigate the risk by conducting more detailed reviews of the process, by conducting a monthly managerial review, or by sharing resources with other departments.</span></span>     
13. <span data-ttu-id="d513a-127">单击 **保存**。</span><span class="sxs-lookup"><span data-stu-id="d513a-127">Click **Save**.</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="d513a-128">创建规则时，不会验证是否符合职责划分规则。</span><span class="sxs-lookup"><span data-stu-id="d513a-128">Compliance with the rules for segregation of duties is not verified when you create a rule.</span></span> <span data-ttu-id="d513a-129">您可以创建一个为现有角色创建冲突的规则。</span><span class="sxs-lookup"><span data-stu-id="d513a-129">You can create a rule that creates a conflict for existing roles.</span></span> <span data-ttu-id="d513a-130">现有用户角色分配也可能与新规则冲突。</span><span class="sxs-lookup"><span data-stu-id="d513a-130">Existing user role assignments can also be in conflict with the new rule.</span></span> <span data-ttu-id="d513a-131">创建或修改规则后，您必须验证合规性。</span><span class="sxs-lookup"><span data-stu-id="d513a-131">You must validate compliance after you create or modify a rule.</span></span> <span data-ttu-id="d513a-132">有关详细信息，请参阅[确定和解决职责划分冲突](identify-resolve-conflicts-segregation-duties.md)</span><span class="sxs-lookup"><span data-stu-id="d513a-132">For more information, see [Identify and resolve conflicts in segregation of duties](identify-resolve-conflicts-segregation-duties.md)</span></span>
