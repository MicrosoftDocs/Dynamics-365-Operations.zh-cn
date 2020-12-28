---
title: 客户信用组
description: 本主题提供有关客户信用组的信息。
author: mikefalkner
manager: AnnBe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1ddf41d88d085b102a7d69eeeff0ec463d8b4137
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4440718"
---
# <a name="customer-credit-groups"></a><span data-ttu-id="f758a-103">客户信用组</span><span class="sxs-lookup"><span data-stu-id="f758a-103">Customer credit groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f758a-104">您可以定义具有共享信用额度的客户组。</span><span class="sxs-lookup"><span data-stu-id="f758a-104">You can define groups of customers who have a shared credit limit.</span></span> <span data-ttu-id="f758a-105">还考虑了在客户发票帐户上定义的个人信用额度。</span><span class="sxs-lookup"><span data-stu-id="f758a-105">The individual credit limit that is defined on the customer invoice account is also considered.</span></span>

<span data-ttu-id="f758a-106">可以从不同的法人中选择客户信用组的成员。</span><span class="sxs-lookup"><span data-stu-id="f758a-106">Members of a customer credit group can be selected from different legal entities.</span></span> <span data-ttu-id="f758a-107">当您将一个客户添加到客户信用组中的客户列表时，每个客户的信用额度的到期日期将更改为分配给该组的到期日期。</span><span class="sxs-lookup"><span data-stu-id="f758a-107">When you add a customer to the list of customers in the customer credit group, the expiration date of the credit limit for each customer is changed to the expiration date that is assigned to the group.</span></span>

<span data-ttu-id="f758a-108">您可以在 **客户信用组** 页（**信用管理 \> 客户信用组 \> 客户信用组**）上设置客户信用组。</span><span class="sxs-lookup"><span data-stu-id="f758a-108">You can set up customer credit groups on the **Customer credit groups** page (**Credit management \> Customer credit groups \> Customer credit groups**).</span></span>

1. <span data-ttu-id="f758a-109">在 **组号** 和 **描述** 字段中，输入组的标识符和描述。</span><span class="sxs-lookup"><span data-stu-id="f758a-109">In the **Group number** and **Description** fields, enter an identifier and description for the group.</span></span>
2. <span data-ttu-id="f758a-110">在 **信用额度** 和 **货币** 字段中，输入系统检查组中任何成员的信用额度时应使用的信用额度和货币。</span><span class="sxs-lookup"><span data-stu-id="f758a-110">In the **Credit limit** and **Currency** fields, enter the credit limit and currency that should be used when the system checks the credit limit for any member of the group.</span></span>
3. <span data-ttu-id="f758a-111">在 **信用额度结束日期** 字段中，输入信用额度的到期日期。</span><span class="sxs-lookup"><span data-stu-id="f758a-111">In the **Credit limit to date** field, enter the date when the credit limit expires.</span></span> <span data-ttu-id="f758a-112">客户信用组必须具有到期日期。</span><span class="sxs-lookup"><span data-stu-id="f758a-112">Customer credit groups must have an expiration date.</span></span>

<span data-ttu-id="f758a-113">设置完客户信用组后，您可以通过指定其法人和客户帐户 ID 将客户添加到该组中。</span><span class="sxs-lookup"><span data-stu-id="f758a-113">After you've finished setting up a customer credit group, you can add customers to it by specifying their legal entity and customer account ID.</span></span> <span data-ttu-id="f758a-114">当您将新客户添加到客户信用组时，系统会在所有法人中搜索相同的客户帐户，并提示您将其添加到客户信用组中。</span><span class="sxs-lookup"><span data-stu-id="f758a-114">When you add a new customer to a customer credit group, the system searches for the same customer account across all legal entities and prompts you to add it to the customer credit group.</span></span>

<span data-ttu-id="f758a-115">使用 **帐龄余额** 菜单查看客户信用组中所有发票客户的帐龄余额详细信息。</span><span class="sxs-lookup"><span data-stu-id="f758a-115">Use the **Aged balances** menu to view the details of the aging balance for all invoice customers in a customer credit group.</span></span> <span data-ttu-id="f758a-116">**帐龄余额** 页显示了发票客户帐户的帐龄余额摘要。</span><span class="sxs-lookup"><span data-stu-id="f758a-116">The **Aging balance** page shows a summary of the aged balances for the invoice customer accounts.</span></span>
