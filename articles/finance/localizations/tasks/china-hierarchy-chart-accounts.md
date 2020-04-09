---
title: CN-00010 中国会计科目表的层次结构
description: 此过程演示如何通过设置多个会计科目级别在层次结构树状结构中创建会计科目表。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerChartOfAccounts, LedgerChartOfAccountsTreeLevel_CN, LedgerCreateAccount_CN, MainAccount
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: China (PRC)
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c4d11443f6f43bd9664476aeaf9bfb4f727bf42d
ms.sourcegitcommit: c69926b4285cb2ec2d9ce1ad72d1cb852024dd5e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/18/2020
ms.locfileid: "3137961"
---
# <a name="cn-00010-china-hierarchy-of-chart-of-accounts"></a><span data-ttu-id="6b636-103">CN-00010 中国会计科目表的层次结构</span><span class="sxs-lookup"><span data-stu-id="6b636-103">CN-00010 China hierarchy of chart of accounts</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6b636-104">此过程演示如何通过设置多个会计科目级别在层次结构树状结构中创建会计科目表。</span><span class="sxs-lookup"><span data-stu-id="6b636-104">This procedure shows how to create a chart of accounts in a hierarchy tree structure by setting up multiple levels for ledger accounts.</span></span>

<span data-ttu-id="6b636-105">本流程是用演示公司 CNMF 数据生成的。</span><span class="sxs-lookup"><span data-stu-id="6b636-105">This procedure was created using the demo data company CNMF.</span></span> <span data-ttu-id="6b636-106">此过程针对 Dynamics 365 for Operations 版本 1611 中增加的一项功能。</span><span class="sxs-lookup"><span data-stu-id="6b636-106">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="6b636-107">转到“总帐”>“会计科目表”>“科目”>“会计科目表”。</span><span class="sxs-lookup"><span data-stu-id="6b636-107">Go to General ledger > Chart of accounts > Accounts > Chart of accounts.</span></span>
2. <span data-ttu-id="6b636-108">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="6b636-108">Click New.</span></span>
3. <span data-ttu-id="6b636-109">在“会计科目表”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="6b636-109">In the Charts of accounts field, type a value.</span></span>
4. <span data-ttu-id="6b636-110">单击“层次结构设置”。</span><span class="sxs-lookup"><span data-stu-id="6b636-110">Click Hierarchy setup.</span></span>
5. <span data-ttu-id="6b636-111">在“最大级别”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="6b636-111">In the Maximum level field, enter a number.</span></span>
6. <span data-ttu-id="6b636-112">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="6b636-112">Click New.</span></span>
7. <span data-ttu-id="6b636-113">在“长度”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="6b636-113">In the Length field, enter a number.</span></span>
8. <span data-ttu-id="6b636-114">在“水平”字段，输入一个数值。</span><span class="sxs-lookup"><span data-stu-id="6b636-114">In the Level field, enter a number.</span></span>
9. <span data-ttu-id="6b636-115">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="6b636-115">In the Name field, type a value.</span></span>
10. <span data-ttu-id="6b636-116">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="6b636-116">Click New.</span></span>
11. <span data-ttu-id="6b636-117">在“长度”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="6b636-117">In the Length field, enter a number.</span></span>
12. <span data-ttu-id="6b636-118">在“水平”字段，输入一个数值。</span><span class="sxs-lookup"><span data-stu-id="6b636-118">In the Level field, enter a number.</span></span>
    * <span data-ttu-id="6b636-119">根据需要重复前面的三个步骤创建更多科目编号格式。</span><span class="sxs-lookup"><span data-stu-id="6b636-119">Repeat the previous three steps to create additional account number formats as necessary.</span></span>  
13. <span data-ttu-id="6b636-120">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="6b636-120">Click Save.</span></span>
14. <span data-ttu-id="6b636-121">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="6b636-121">Close the page.</span></span>
15. <span data-ttu-id="6b636-122">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="6b636-122">Click New.</span></span>
16. <span data-ttu-id="6b636-123">在“科目名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="6b636-123">In the Account name field, type a value.</span></span>
17. <span data-ttu-id="6b636-124">在“会计科目”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="6b636-124">In the Ledger account field, type a value.</span></span>
18. <span data-ttu-id="6b636-125">在“科目类型”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="6b636-125">In the Account type field, select an option.</span></span>
19. <span data-ttu-id="6b636-126">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="6b636-126">Click OK.</span></span>
20. <span data-ttu-id="6b636-127">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="6b636-127">Click New.</span></span>
21. <span data-ttu-id="6b636-128">在“科目名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="6b636-128">In the Account name field, type a value.</span></span>
22. <span data-ttu-id="6b636-129">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="6b636-129">Click OK.</span></span>
    * <span data-ttu-id="6b636-130">根据需要重复最后三个步骤创建更多下级科目。</span><span class="sxs-lookup"><span data-stu-id="6b636-130">Repeat the last three steps to create additional sub accounts, as necessary.</span></span>  
23. <span data-ttu-id="6b636-131">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="6b636-131">Click Save.</span></span>

