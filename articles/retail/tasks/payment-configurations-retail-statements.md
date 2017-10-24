--- 
title: "零售报表的付款配置"
description: "此程序会演示零售商店付款方式的配置（这会影响到如何创建和过帐零售报表）。"
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: f12d8ac9be11b92eaef4acce094ae183906278d4
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="payment-configurations-for-retail-statements"></a><span data-ttu-id="195e7-103">零售报表的付款配置</span><span class="sxs-lookup"><span data-stu-id="195e7-103">Payment configurations for Retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="195e7-104">此程序会演示零售商店付款方式的配置（这会影响到如何创建和过帐零售报表）。</span><span class="sxs-lookup"><span data-stu-id="195e7-104">This procedure demonstrates configurations for Retail store payment methods, which affect how Retail statements get created and posted.</span></span>

<span data-ttu-id="195e7-105">此记录使用 USRT 演示公司。</span><span class="sxs-lookup"><span data-stu-id="195e7-105">This recording uses the USRT demo company.</span></span>

1. <span data-ttu-id="195e7-106">转至“零售和商业”>“渠道”>“零售商店”>“所有零售商店”。</span><span class="sxs-lookup"><span data-stu-id="195e7-106">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
2. <span data-ttu-id="195e7-107">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="195e7-107">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="195e7-108">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="195e7-108">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="195e7-109">单击“操作窗格”上的“设置”。</span><span class="sxs-lookup"><span data-stu-id="195e7-109">On the Action Pane, click Set up.</span></span>
5. <span data-ttu-id="195e7-110">单击“付款方式”。</span><span class="sxs-lookup"><span data-stu-id="195e7-110">Click Payment methods.</span></span>
6. <span data-ttu-id="195e7-111">展开或折叠“过帐”部分。</span><span class="sxs-lookup"><span data-stu-id="195e7-111">Expand or collapse the Posting section.</span></span>
7. <span data-ttu-id="195e7-112">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="195e7-112">Click Edit.</span></span>
    * <span data-ttu-id="195e7-113">选择此付款方式收到的金额是否应过帐到会计科目或银行科目。</span><span class="sxs-lookup"><span data-stu-id="195e7-113">Select whether the amounts received for this payment method should be posted to a ledger account or bank account.</span></span>  
    * <span data-ttu-id="195e7-114">选择此付款方式收到的金额应过帐到的科目。</span><span class="sxs-lookup"><span data-stu-id="195e7-114">Select the account that amounts received for this payment method should be posted to.</span></span>  
    * <span data-ttu-id="195e7-115">选择一个科目，以过帐收到的总交易金额与用于此付款方式盘点的金额之间的可能差额。</span><span class="sxs-lookup"><span data-stu-id="195e7-115">Select an account to post possible differences between the total transaction amount received and the amount counted for this payment method.</span></span>  
    * <span data-ttu-id="195e7-116">在此字段中，您可以输入一个金额，以控制何时将差异金额过帐到其他差额科目。</span><span class="sxs-lookup"><span data-stu-id="195e7-116">In this field you can enter an amount to control when the difference amount should be posted to another difference account.</span></span> <span data-ttu-id="195e7-117">您可以使用这个跟踪较大差额。</span><span class="sxs-lookup"><span data-stu-id="195e7-117">You can use this to track big differences.</span></span>  
    * <span data-ttu-id="195e7-118">选择一个科目，以便在超过“最大差额”字段中定义的值时，过帐收到的总交易金额与盘点金额之间的可能差额。</span><span class="sxs-lookup"><span data-stu-id="195e7-118">Select an account to post possible differences between the total transaction amount received and the amount counted, when it exceeds the value that is defined in the "Maximum difference amount" field.</span></span>  
    * <span data-ttu-id="195e7-119">选择“是”，以将银行投箱金额过帐到单独的科目。</span><span class="sxs-lookup"><span data-stu-id="195e7-119">Select "Yes" to post bank drop amounts to a seperate account.</span></span>  
    * <span data-ttu-id="195e7-120">在此字段中，您可以选择是否应将收到的银行投箱金额过帐到会计科目或银行科目。</span><span class="sxs-lookup"><span data-stu-id="195e7-120">In this field you can select whether bank drop amounts should be posted to a ledger account or a bank account.</span></span>  
    * <span data-ttu-id="195e7-121">选择将银行投箱金额过帐到其中的科目。</span><span class="sxs-lookup"><span data-stu-id="195e7-121">Select the account to post bank drop amounts into.</span></span>  
    * <span data-ttu-id="195e7-122">选择在将银行投箱金额过帐到银行科目时使用的银行交易类型。</span><span class="sxs-lookup"><span data-stu-id="195e7-122">Select the bank transaction type to use when posting bank drop amounts to the bank account.</span></span>  
    * <span data-ttu-id="195e7-123">选择“是”，以将金库投箱金额过帐到单独的科目。</span><span class="sxs-lookup"><span data-stu-id="195e7-123">Select "Yes" to post safe drop amounts to a seperate account.</span></span>  
    * <span data-ttu-id="195e7-124">选择是否应将金库投箱金额过帐到会计科目或银行科目。</span><span class="sxs-lookup"><span data-stu-id="195e7-124">Select whether safe drop amounts should be posted to the ledger account or the bank account.</span></span>  
    * <span data-ttu-id="195e7-125">选择将金库投箱金额过帐到其中的科目。</span><span class="sxs-lookup"><span data-stu-id="195e7-125">Select the account to post safe drop amounts into.</span></span>  
8. <span data-ttu-id="195e7-126">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="195e7-126">Click Save.</span></span>


