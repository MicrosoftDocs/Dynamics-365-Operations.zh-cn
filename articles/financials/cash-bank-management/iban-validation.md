---
title: "管理国际银行帐号 (IBAN) 帐户验证"
description: "此主题介绍如何管理国际银行帐号 (IBAN) 帐户验证。"
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.translationtype: HT
ms.sourcegitcommit: 98ed3378ab05c0c69c9e5b2a82310113a81c2264
ms.openlocfilehash: e091aab70a98e0f4b96c41c1ee48926947539105
ms.contentlocale: zh-cn
ms.lasthandoff: 08/31/2018

---

# <a name="manage-international-bank-account-number-iban-account-validation"></a><span data-ttu-id="dd874-103">管理国际银行帐号 (IBAN) 帐户验证</span><span class="sxs-lookup"><span data-stu-id="dd874-103">Manage International Bank Account Number (IBAN) account validation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dd874-104">验证国际银行帐号 (IBAN) 帐户可以增加在向银行帐户添加 IBAN 时完成的验证量。</span><span class="sxs-lookup"><span data-stu-id="dd874-104">International Bank Account Number (IBAN) account validation increases the amount of validation that is done when you add an IBAN to a bank account.</span></span>

<span data-ttu-id="dd874-105">IBAN 的结构存储在 Microsoft Dynamics 365 for Finance and Operation 中，在你首次对银行帐户使用 IBAN 时自动加载。</span><span class="sxs-lookup"><span data-stu-id="dd874-105">The structure of the IBAN is stored in Microsoft Dynamics 365 for Finance and Operation, and is automatically loaded when you first use the IBAN on bank accounts.</span></span> <span data-ttu-id="dd874-106">银行帐号是为 IBAN 号定义的结构的一部分。</span><span class="sxs-lookup"><span data-stu-id="dd874-106">The bank account number is part of the structure defined for an IBAN number.</span></span> <span data-ttu-id="dd874-107">根据该结构，如果 IBAN 中帐号的位置和长度与每个国家或地区的结构中定义的位置不匹配，将收到警告消息。</span><span class="sxs-lookup"><span data-stu-id="dd874-107">Based on that structure, if the position and length of the account number in the IBAN don't match the position that is defined in the structure for each country or region, you will receive warning messages.</span></span>

## <a name="set-up-iban-structures"></a><span data-ttu-id="dd874-108">设置 IBAN 结构</span><span class="sxs-lookup"><span data-stu-id="dd874-108">Set up IBAN structures</span></span>

1. <span data-ttu-id="dd874-109">转到**现金和银行管理 \> 设置 \> IBAN 结构**。</span><span class="sxs-lookup"><span data-stu-id="dd874-109">Go to **Cash and bank management \> Setup \> IBAN structures**.</span></span>
2. <span data-ttu-id="dd874-110">请注意，已自动设置了每个国家或地区的 IBAN 结构。</span><span class="sxs-lookup"><span data-stu-id="dd874-110">Notice that the IBAN structures for each country or region have been set up automatically.</span></span>
3. <span data-ttu-id="dd874-111">如果必须自定义特定国家或地区的结构，可以进行编辑。</span><span class="sxs-lookup"><span data-stu-id="dd874-111">If you must customize the structures for a specific country or region, you can edit them.</span></span>
4. <span data-ttu-id="dd874-112">每个新发行版中都有结构定义。</span><span class="sxs-lookup"><span data-stu-id="dd874-112">The structure definitions will be a part of each new release.</span></span> <span data-ttu-id="dd874-113">每次更新之后，可使用**重置结构**菜单加载最新定义。</span><span class="sxs-lookup"><span data-stu-id="dd874-113">You can use the **Reset structures** menu to load the latest definitions after each update.</span></span>

## <a name="validate-the-iban-structure-in-a-bank-account"></a><span data-ttu-id="dd874-114">验证银行帐户中的 IBAN 结构</span><span class="sxs-lookup"><span data-stu-id="dd874-114">Validate the IBAN structure in a bank account</span></span>

1. <span data-ttu-id="dd874-115">转至**现金和银行管理 \> 银行帐户 \> 银行帐户**。</span><span class="sxs-lookup"><span data-stu-id="dd874-115">Go to **Cash and bank management \> Bank accounts \> Bank accounts**.</span></span>
2. <span data-ttu-id="dd874-116">创建银行帐户。</span><span class="sxs-lookup"><span data-stu-id="dd874-116">Create a bank account.</span></span>
3. <span data-ttu-id="dd874-117">在**附加信息**快速选项卡上，输入一个 IBAN。</span><span class="sxs-lookup"><span data-stu-id="dd874-117">On the **Additional information** FastTab, enter an IBAN.</span></span>

    <span data-ttu-id="dd874-118">如果 IBAN 中帐号的位置和长度与每个国家或地区的结构中定义的位置不匹配，将收到消息。</span><span class="sxs-lookup"><span data-stu-id="dd874-118">If the position and length of the account number in the IBAN don't match the position that is defined in the structure for each country or region, you receive a message.</span></span> <span data-ttu-id="dd874-119">如果 IBAN 的长度与 IBAN 结构中的长度不匹配，则不能继续操作。</span><span class="sxs-lookup"><span data-stu-id="dd874-119">You can't continue if the length of the IBAN doesn't match the length in the IBAN structure.</span></span>

    <span data-ttu-id="dd874-120">此项验证还会验证银行帐号是否与表示银行帐号的 IBAN 部分匹配。</span><span class="sxs-lookup"><span data-stu-id="dd874-120">The validation also verifies that the bank account number matches the part of the IBAN that represents the bank account number.</span></span> <span data-ttu-id="dd874-121">如果银行帐号不匹配，将收到警告消息。</span><span class="sxs-lookup"><span data-stu-id="dd874-121">If the bank account number doesn't match, you receive a warning message.</span></span> <span data-ttu-id="dd874-122">此消息只是警告。</span><span class="sxs-lookup"><span data-stu-id="dd874-122">This message is only a warning.</span></span> <span data-ttu-id="dd874-123">即使银行帐号不匹配，也可以继续操作。</span><span class="sxs-lookup"><span data-stu-id="dd874-123">You can continue even if the bank account number doesn't match.</span></span>

