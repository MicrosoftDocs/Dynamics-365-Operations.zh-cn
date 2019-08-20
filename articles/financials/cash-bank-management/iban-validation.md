---
title: 管理国际银行帐号 (IBAN) 帐户验证
description: 此主题介绍如何管理国际银行帐号 (IBAN) 帐户验证。
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 70c497ec575ffcaa6f2fdc3fe77bae7b41dc02fb
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/01/2019
ms.locfileid: "1842417"
---
# <a name="manage-international-bank-account-number-iban-validation"></a><span data-ttu-id="124fd-103">管理国际银行帐号 (IBAN) 验证</span><span class="sxs-lookup"><span data-stu-id="124fd-103">Manage International Bank Account Number (IBAN) validation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="124fd-104">验证国际银行帐号 (IBAN) 可以增加在向银行帐户添加 IBAN 时完成的验证量。</span><span class="sxs-lookup"><span data-stu-id="124fd-104">International Bank Account Number (IBAN) validation increases the amount of validation that is done when you add an IBAN to a bank account.</span></span>

<span data-ttu-id="124fd-105">有关 IBAN 结构的信息存储在 Microsoft Dynamics 365 for Finance and Operations 中。</span><span class="sxs-lookup"><span data-stu-id="124fd-105">Information about the structure of the IBAN is stored in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="124fd-106">当您在银行帐户中首次使用 IBAN 时，该信息将自动加载。</span><span class="sxs-lookup"><span data-stu-id="124fd-106">That information is automatically loaded when you first use the IBAN on bank accounts.</span></span> <span data-ttu-id="124fd-107">它包含 IBAN 的长度，银行帐号和银行代号的开始位置，以及银行帐号和银行代号的长度。</span><span class="sxs-lookup"><span data-stu-id="124fd-107">It contains the length of the IBAN, the starting positions of the bank account number and the routing number, and the length of the bank account number and routing number.</span></span>

## <a name="set-up-iban-structures"></a><span data-ttu-id="124fd-108">设置 IBAN 结构</span><span class="sxs-lookup"><span data-stu-id="124fd-108">Set up IBAN structures</span></span>

1. <span data-ttu-id="124fd-109">转到**现金和银行管理 \> 设置 \> IBAN 结构**。</span><span class="sxs-lookup"><span data-stu-id="124fd-109">Go to **Cash and bank management \> Setup \> IBAN structures**.</span></span>
2. <span data-ttu-id="124fd-110">请注意，已自动设置了每个国家或地区的 IBAN 结构。</span><span class="sxs-lookup"><span data-stu-id="124fd-110">Notice that the IBAN structures for each country or region have been set up automatically.</span></span>
3. <span data-ttu-id="124fd-111">如果想要自定义特定国家或地区的结构，可以进行编辑。</span><span class="sxs-lookup"><span data-stu-id="124fd-111">If you want to customize the structures for a specific country or region, you can edit them.</span></span>
4. <span data-ttu-id="124fd-112">每个新发行版中都有结构定义。</span><span class="sxs-lookup"><span data-stu-id="124fd-112">The structure definitions will be a part of each new release.</span></span> <span data-ttu-id="124fd-113">每次更新之后，可使用**重置结构**菜单加载最新定义。</span><span class="sxs-lookup"><span data-stu-id="124fd-113">You can use the **Reset structures** menu to load the latest definitions after each update.</span></span>

## <a name="validate-the-iban-structure-in-a-bank-account"></a><span data-ttu-id="124fd-114">验证银行帐户中的 IBAN 结构</span><span class="sxs-lookup"><span data-stu-id="124fd-114">Validate the IBAN structure in a bank account</span></span>

1. <span data-ttu-id="124fd-115">转至**现金和银行管理 \> 银行帐户 \> 银行帐户**。</span><span class="sxs-lookup"><span data-stu-id="124fd-115">Go to **Cash and bank management \> Bank accounts \> Bank accounts**.</span></span>
2. <span data-ttu-id="124fd-116">创建银行帐户。</span><span class="sxs-lookup"><span data-stu-id="124fd-116">Create a bank account.</span></span>
3. <span data-ttu-id="124fd-117">在**附加信息**快速选项卡上，输入一个 IBAN。</span><span class="sxs-lookup"><span data-stu-id="124fd-117">On the **Additional information** FastTab, enter an IBAN.</span></span>

    <span data-ttu-id="124fd-118">如果 IBAN 的长度与为每个国家/地区定义的长度不匹配，您将收到一条警告消息。</span><span class="sxs-lookup"><span data-stu-id="124fd-118">If the length of the IBAN doesn't match the length that is defined for each country or region, you will receive a warning message.</span></span> <span data-ttu-id="124fd-119">如果 IBAN 的长度与 IBAN 结构中指定的长度不匹配，则不能继续操作。</span><span class="sxs-lookup"><span data-stu-id="124fd-119">You can't continue if the length of the IBAN doesn't match the length specified in the IBAN structure.</span></span>

    <span data-ttu-id="124fd-120">此项验证还会验证银行帐号是否与表示银行帐号的 IBAN 部分匹配。</span><span class="sxs-lookup"><span data-stu-id="124fd-120">The validation also verifies that the bank account number matches the part of the IBAN that represents the bank account number.</span></span> <span data-ttu-id="124fd-121">如果银行帐号不匹配，将收到警告消息。</span><span class="sxs-lookup"><span data-stu-id="124fd-121">If the bank account number doesn't match, you will receive a warning message.</span></span> <span data-ttu-id="124fd-122">此消息只是警告。</span><span class="sxs-lookup"><span data-stu-id="124fd-122">This message is only a warning.</span></span> <span data-ttu-id="124fd-123">即使银行帐号不匹配，也可以继续操作。</span><span class="sxs-lookup"><span data-stu-id="124fd-123">You can continue even if the bank account number doesn't match.</span></span>

    <span data-ttu-id="124fd-124">此项验证还会验证银行代号是否与表示银行代号的 IBAN 部分匹配。</span><span class="sxs-lookup"><span data-stu-id="124fd-124">The validation also verifies that the bank routing number matches the part of the IBAN that represents the bank routing number.</span></span> <span data-ttu-id="124fd-125">银行代号包含一个银行编号，通常是其他分行。</span><span class="sxs-lookup"><span data-stu-id="124fd-125">The routing number includes a bank number and often an additional bank branch.</span></span> <span data-ttu-id="124fd-126">如果银行代号不匹配，将收到警告消息。</span><span class="sxs-lookup"><span data-stu-id="124fd-126">If the bank routing number doesn't match, you will receive a warning message.</span></span> <span data-ttu-id="124fd-127">此消息只是警告。</span><span class="sxs-lookup"><span data-stu-id="124fd-127">This message is only a warning.</span></span> <span data-ttu-id="124fd-128">即使银行代号不匹配，也可以继续操作。</span><span class="sxs-lookup"><span data-stu-id="124fd-128">You can continue even if the bank routing number doesn't match.</span></span>
