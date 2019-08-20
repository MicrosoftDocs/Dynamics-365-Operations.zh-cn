---
title: 设置职责划分
description: 您可以设置规则，以分离必须由不同用户执行的任务。
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e3682dbcb72588633fb6b3fe4cbda99f422163a3
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/02/2019
ms.locfileid: "1851253"
---
# <a name="set-up-segregation-of-duties"></a><span data-ttu-id="3f5a2-103">设置职责划分</span><span class="sxs-lookup"><span data-stu-id="3f5a2-103">Set up segregation of duties</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3f5a2-104">您可以设置规则，以分离必须由不同用户执行的任务。</span><span class="sxs-lookup"><span data-stu-id="3f5a2-104">You can set up rules to separate tasks that must be performed by different users.</span></span> <span data-ttu-id="3f5a2-105">此概念被称作职责划分。</span><span class="sxs-lookup"><span data-stu-id="3f5a2-105">This concept is named segregation of duties.</span></span> <span data-ttu-id="3f5a2-106">例如，您可能不希望由同一人确认收到货物和处理向供应商付款的事宜。</span><span class="sxs-lookup"><span data-stu-id="3f5a2-106">For example, you might not want the same person both to acknowledge the receipt of goods and to process payment to the vendor.</span></span> <span data-ttu-id="3f5a2-107">职责划分有助于您减少欺骗风险，并且它还有助于您检测错误或违规。</span><span class="sxs-lookup"><span data-stu-id="3f5a2-107">Segregation of duties helps you reduce the risk of fraud, and it also helps you detect errors or irregularities.</span></span> <span data-ttu-id="3f5a2-108">您还可以使用职责划分来执行内部控制策略。</span><span class="sxs-lookup"><span data-stu-id="3f5a2-108">You can also use segregation of duties to enforce internal control policies.</span></span> <span data-ttu-id="3f5a2-109">完成以下过程以创建规则。</span><span class="sxs-lookup"><span data-stu-id="3f5a2-109">Complete the following procedure to create a rule.</span></span> <span data-ttu-id="3f5a2-110">您必须是系统管理员，才能完成该过程。</span><span class="sxs-lookup"><span data-stu-id="3f5a2-110">You must be a system administrator to complete the procedure.</span></span> <span data-ttu-id="3f5a2-111">用于创建该过程的演示数据公司是 DAT。</span><span class="sxs-lookup"><span data-stu-id="3f5a2-111">The demo data company used to create this procedure is DAT.</span></span> 

1. <span data-ttu-id="3f5a2-112">转到“系统管理”>“安全”>“职责划分”>“职责划分规则”。</span><span class="sxs-lookup"><span data-stu-id="3f5a2-112">Go to System administration > Security > Segregation of duties > Segregation of duties rules.</span></span>
2. <span data-ttu-id="3f5a2-113">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="3f5a2-113">Click New.</span></span>
3. <span data-ttu-id="3f5a2-114">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="3f5a2-114">In the Name field, type a value.</span></span>
    * <span data-ttu-id="3f5a2-115">输入规则的名称。</span><span class="sxs-lookup"><span data-stu-id="3f5a2-115">Enter a name for the rule.</span></span>  
4. <span data-ttu-id="3f5a2-116">在“第一个职责”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="3f5a2-116">In the First duty field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="3f5a2-117">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="3f5a2-117">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="3f5a2-118">选择由规则控制的第一个职责。</span><span class="sxs-lookup"><span data-stu-id="3f5a2-118">Select the first duty that is controlled by the rule.</span></span>  
6. <span data-ttu-id="3f5a2-119">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="3f5a2-119">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="3f5a2-120">在“第二个职责”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="3f5a2-120">In the Second duty field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="3f5a2-121">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="3f5a2-121">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="3f5a2-122">选择由规则控制的第二个职责。</span><span class="sxs-lookup"><span data-stu-id="3f5a2-122">Select the second duty that is controlled by the rule.</span></span>  
9. <span data-ttu-id="3f5a2-123">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="3f5a2-123">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="3f5a2-124">在“严重性”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="3f5a2-124">In the Severity field, select an option.</span></span>
    * <span data-ttu-id="3f5a2-125">选择在同一用户或角色同时履行两个职责时发生风险的严重性。</span><span class="sxs-lookup"><span data-stu-id="3f5a2-125">Select the severity of the risk that occurs when the same user or role performs both duties.</span></span>  
11. <span data-ttu-id="3f5a2-126">在“安全风险”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="3f5a2-126">In the Security risk field, type a value.</span></span>
    * <span data-ttu-id="3f5a2-127">输入安全风险的描述。</span><span class="sxs-lookup"><span data-stu-id="3f5a2-127">Enter a description of the security risk.</span></span>  
12. <span data-ttu-id="3f5a2-128">在“安全降低”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="3f5a2-128">In the Security mitigation field, type a value.</span></span>
    * <span data-ttu-id="3f5a2-129">输入您为减少安全风险而采取的行动的描述。</span><span class="sxs-lookup"><span data-stu-id="3f5a2-129">Enter a description of the actions that you take to mitigate the security risk.</span></span> <span data-ttu-id="3f5a2-130">例如，您可以通过更详细地审查流程，通过进行阅读管理审查，或者通过与其他部门共享资源，减少风险。</span><span class="sxs-lookup"><span data-stu-id="3f5a2-130">For example, you can mitigate the risk by conducting more detailed reviews of the process, by conducting a monthly managerial review, or by sharing resources with other departments.</span></span>  
13. <span data-ttu-id="3f5a2-131">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="3f5a2-131">Click Save.</span></span>

