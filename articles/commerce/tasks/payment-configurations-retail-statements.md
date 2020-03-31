---
title: 零售报表的付款配置
description: 此程序会演示 Commerce 商店付款方式的配置（这会影响到如何创建和过帐对帐单）。
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable, RetailStoreTenderTypeTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 72425526a4425eeb5cb7539f9633bda5657ca99e
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/01/2020
ms.locfileid: "3021725"
---
# <a name="payment-configurations-for-retail-statements"></a><span data-ttu-id="b38a6-103">零售报表的付款配置</span><span class="sxs-lookup"><span data-stu-id="b38a6-103">Payment configurations for Retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="b38a6-104">此程序会演示 Commerce 商店付款方式的配置（这会影响到如何创建和过帐对帐单）。</span><span class="sxs-lookup"><span data-stu-id="b38a6-104">This procedure demonstrates configurations for Commerce store payment methods, which affect how statements get created and posted.</span></span>

<span data-ttu-id="b38a6-105">此记录使用 USRT 演示公司。</span><span class="sxs-lookup"><span data-stu-id="b38a6-105">This recording uses the USRT demo company.</span></span>

1. <span data-ttu-id="b38a6-106">转至“Retail 和 Commerce”>“渠道”>“商店”>“所有商店”。</span><span class="sxs-lookup"><span data-stu-id="b38a6-106">Go to Retail and Commerce > Channels > Stores > All stores.</span></span>
2. <span data-ttu-id="b38a6-107">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="b38a6-107">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="b38a6-108">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="b38a6-108">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="b38a6-109">单击“操作窗格”上的“设置”。</span><span class="sxs-lookup"><span data-stu-id="b38a6-109">On the Action Pane, click Set up.</span></span>
5. <span data-ttu-id="b38a6-110">单击“付款方式”。</span><span class="sxs-lookup"><span data-stu-id="b38a6-110">Click Payment methods.</span></span>
6. <span data-ttu-id="b38a6-111">展开或折叠“过帐”部分。</span><span class="sxs-lookup"><span data-stu-id="b38a6-111">Expand or collapse the Posting section.</span></span>
7. <span data-ttu-id="b38a6-112">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="b38a6-112">Click Edit.</span></span>
    * <span data-ttu-id="b38a6-113">选择此付款方式收到的金额是否应过帐到会计科目或银行科目。</span><span class="sxs-lookup"><span data-stu-id="b38a6-113">Select whether the amounts received for this payment method should be posted to a ledger account or bank account.</span></span>  
    * <span data-ttu-id="b38a6-114">选择此付款方式收到的金额应过帐到的科目。</span><span class="sxs-lookup"><span data-stu-id="b38a6-114">Select the account that amounts received for this payment method should be posted to.</span></span>  
    * <span data-ttu-id="b38a6-115">选择一个科目，以过帐收到的总交易金额与用于此付款方式盘点的金额之间的可能差额。</span><span class="sxs-lookup"><span data-stu-id="b38a6-115">Select an account to post possible differences between the total transaction amount received and the amount counted for this payment method.</span></span>  
    * <span data-ttu-id="b38a6-116">在此字段中，您可以输入一个金额，以控制何时将差异金额过帐到其他差额科目。</span><span class="sxs-lookup"><span data-stu-id="b38a6-116">In this field you can enter an amount to control when the difference amount should be posted to another difference account.</span></span> <span data-ttu-id="b38a6-117">您可以使用这个跟踪较大差额。</span><span class="sxs-lookup"><span data-stu-id="b38a6-117">You can use this to track big differences.</span></span>  
    * <span data-ttu-id="b38a6-118">选择一个科目，以便在超过“最大差额”字段中定义的值时，过帐收到的总交易金额与盘点金额之间的可能差额。</span><span class="sxs-lookup"><span data-stu-id="b38a6-118">Select an account to post possible differences between the total transaction amount received and the amount counted, when it exceeds the value that is defined in the "Maximum difference amount" field.</span></span>  
    * <span data-ttu-id="b38a6-119">选择“是”，以将银行投箱金额过帐到单独的科目。</span><span class="sxs-lookup"><span data-stu-id="b38a6-119">Select "Yes" to post bank drop amounts to a separate account.</span></span>  
    * <span data-ttu-id="b38a6-120">在此字段中，您可以选择是否应将收到的银行投箱金额过帐到会计科目或银行科目。</span><span class="sxs-lookup"><span data-stu-id="b38a6-120">In this field you can select whether bank drop amounts should be posted to a ledger account or a bank account.</span></span>  
    * <span data-ttu-id="b38a6-121">选择将银行投箱金额过帐到其中的科目。</span><span class="sxs-lookup"><span data-stu-id="b38a6-121">Select the account to post bank drop amounts into.</span></span>  
    * <span data-ttu-id="b38a6-122">选择在将银行投箱金额过帐到银行科目时使用的银行交易类型。</span><span class="sxs-lookup"><span data-stu-id="b38a6-122">Select the bank transaction type to use when posting bank drop amounts to the bank account.</span></span>  
    * <span data-ttu-id="b38a6-123">选择“是”，以将金库投箱金额过帐到单独的科目。</span><span class="sxs-lookup"><span data-stu-id="b38a6-123">Select "Yes" to post safe drop amounts to a separate account.</span></span>  
    * <span data-ttu-id="b38a6-124">选择是否应将金库投箱金额过帐到会计科目或银行科目。</span><span class="sxs-lookup"><span data-stu-id="b38a6-124">Select whether safe drop amounts should be posted to the ledger account or the bank account.</span></span>  
    * <span data-ttu-id="b38a6-125">选择将金库投箱金额过帐到其中的科目。</span><span class="sxs-lookup"><span data-stu-id="b38a6-125">Select the account to post safe drop amounts into.</span></span>  
8. <span data-ttu-id="b38a6-126">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="b38a6-126">Click Save.</span></span>
