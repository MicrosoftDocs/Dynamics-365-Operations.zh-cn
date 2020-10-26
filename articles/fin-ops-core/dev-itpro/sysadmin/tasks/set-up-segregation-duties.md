---
title: 设置职责划分
description: 您可以设置规则，以分离必须由不同用户执行的任务。
author: maertenm
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 47747cba7f83d0b43a284750cff232824e00053a
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982398"
---
# <a name="set-up-segregation-of-duties"></a><span data-ttu-id="caa22-103">设置职责划分</span><span class="sxs-lookup"><span data-stu-id="caa22-103">Set up segregation of duties</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="caa22-104">您可以设置规则，以分离必须由不同用户执行的任务。</span><span class="sxs-lookup"><span data-stu-id="caa22-104">You can set up rules to separate tasks that must be performed by different users.</span></span> <span data-ttu-id="caa22-105">此概念被称作职责划分。</span><span class="sxs-lookup"><span data-stu-id="caa22-105">This concept is named segregation of duties.</span></span> <span data-ttu-id="caa22-106">例如，您可能不希望由同一人确认收到货物和处理向供应商付款的事宜。</span><span class="sxs-lookup"><span data-stu-id="caa22-106">For example, you might not want the same person both to acknowledge the receipt of goods and to process payment to the vendor.</span></span> <span data-ttu-id="caa22-107">职责划分有助于您减少欺骗风险，并且它还有助于您检测错误或违规。</span><span class="sxs-lookup"><span data-stu-id="caa22-107">Segregation of duties helps you reduce the risk of fraud, and it also helps you detect errors or irregularities.</span></span> <span data-ttu-id="caa22-108">您还可以使用职责划分来执行内部控制策略。</span><span class="sxs-lookup"><span data-stu-id="caa22-108">You can also use segregation of duties to enforce internal control policies.</span></span> <span data-ttu-id="caa22-109">完成以下过程以创建规则。</span><span class="sxs-lookup"><span data-stu-id="caa22-109">Complete the following procedure to create a rule.</span></span> <span data-ttu-id="caa22-110">您必须是系统管理员，才能完成该过程。</span><span class="sxs-lookup"><span data-stu-id="caa22-110">You must be a system administrator to complete the procedure.</span></span> <span data-ttu-id="caa22-111">用于创建该过程的演示数据公司是 DAT。</span><span class="sxs-lookup"><span data-stu-id="caa22-111">The demo data company used to create this procedure is DAT.</span></span> 

1. <span data-ttu-id="caa22-112">转到**导航窗格 > 模块 > 系统管理 > 安全 > 职责划分 > 职责划分规则**。</span><span class="sxs-lookup"><span data-stu-id="caa22-112">Go to **Navigation pane > Modules > System administration > Security > Segregation of duties > Segregation of duties rules**.</span></span>
2. <span data-ttu-id="caa22-113">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="caa22-113">Click **New**.</span></span>
3. <span data-ttu-id="caa22-114">在**名称**字段中，为规则输入一个值。</span><span class="sxs-lookup"><span data-stu-id="caa22-114">In the **Name** field, type a value for the rule.</span></span>
4. <span data-ttu-id="caa22-115">在**第一个职责**字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="caa22-115">In the **First duty** field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="caa22-116">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="caa22-116">In the list, find and select the desired record.</span></span> <span data-ttu-id="caa22-117">选择由规则控制的第一个职责。</span><span class="sxs-lookup"><span data-stu-id="caa22-117">Select the first duty that is controlled by the rule.</span></span>
6. <span data-ttu-id="caa22-118">在**第二个职责**字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="caa22-118">In the **Second duty** field, click the drop-down button to open the lookup.</span></span> 
7. <span data-ttu-id="caa22-119">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="caa22-119">In the list, find and select the desired record.</span></span> <span data-ttu-id="caa22-120">选择由规则控制的第二个职责。</span><span class="sxs-lookup"><span data-stu-id="caa22-120">Select the second duty that is controlled by the rule.</span></span>
10. <span data-ttu-id="caa22-121">在**严重性**字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="caa22-121">In the **Severity** field, select an option.</span></span> <span data-ttu-id="caa22-122">选择在同一用户或角色同时履行两个职责时发生风险的严重性。</span><span class="sxs-lookup"><span data-stu-id="caa22-122">Select the severity of the risk that occurs when the same user or role performs both duties.</span></span>  
11. <span data-ttu-id="caa22-123">在**安全风险**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="caa22-123">In the **Security risk** field, type a value.</span></span> <span data-ttu-id="caa22-124">输入安全风险的描述。</span><span class="sxs-lookup"><span data-stu-id="caa22-124">Enter a description of the security risk.</span></span>  
12. <span data-ttu-id="caa22-125">在**安全降低**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="caa22-125">In the **Security mitigation** field, type a value.</span></span> <span data-ttu-id="caa22-126">输入您为减少安全风险而采取的行动的描述。</span><span class="sxs-lookup"><span data-stu-id="caa22-126">Enter a description of the actions that you take to mitigate the security risk.</span></span> <span data-ttu-id="caa22-127">例如，您可以通过更详细地审查流程，通过进行阅读管理审查，或者通过与其他部门共享资源，减少风险。</span><span class="sxs-lookup"><span data-stu-id="caa22-127">For example, you can mitigate the risk by conducting more detailed reviews of the process, by conducting a monthly managerial review, or by sharing resources with other departments.</span></span>     
13. <span data-ttu-id="caa22-128">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="caa22-128">Click **Save**.</span></span>

