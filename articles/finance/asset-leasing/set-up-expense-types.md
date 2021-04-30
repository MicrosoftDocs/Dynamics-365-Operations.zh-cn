---
title: 设置费用类型
description: 本主题介绍如何在资产租赁中设置费用类型。
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseExpenseTypeTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2019-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a1d6667a7c6fe1cd44196f2e753ca72b2ca97649
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880976"
---
# <a name="set-up-expense-types"></a><span data-ttu-id="fd82e-103">设置费用类型</span><span class="sxs-lookup"><span data-stu-id="fd82e-103">Set up expense types</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fd82e-104">本主题介绍如何在资产租赁中设置费用类型。</span><span class="sxs-lookup"><span data-stu-id="fd82e-104">This topic explains how to set up expense types in Asset leasing.</span></span> <span data-ttu-id="fd82e-105">付款计划中未包含的费用称为 *费用成本*。</span><span class="sxs-lookup"><span data-stu-id="fd82e-105">Costs that aren't represented by the payment schedule are known as *expense costs*.</span></span> <span data-ttu-id="fd82e-106">这些成本的示例包括财产税、公共区域维护成本和保险费用。</span><span class="sxs-lookup"><span data-stu-id="fd82e-106">Examples of these costs include property taxes, common area maintenance costs, and insurance expenses.</span></span>

## <a name="add-an-administrative-expense-type"></a><span data-ttu-id="fd82e-107">添加管理费用类型</span><span class="sxs-lookup"><span data-stu-id="fd82e-107">Add an administrative expense type</span></span>

1. <span data-ttu-id="fd82e-108">转到 **资产租赁 \> 设置 \> 费用类型**。</span><span class="sxs-lookup"><span data-stu-id="fd82e-108">Go to **Asset leasing \> Setup \> Expense types**.</span></span>
2. <span data-ttu-id="fd82e-109">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="fd82e-109">Select **New**.</span></span>
3. <span data-ttu-id="fd82e-110">在相应字段中，输入新的费用类型和说明。</span><span class="sxs-lookup"><span data-stu-id="fd82e-110">In the appropriate fields, enter the new expense type and a description.</span></span>

## <a name="assign-accounts-to-administrative-costs"></a><span data-ttu-id="fd82e-111">将科目分配给管理费用</span><span class="sxs-lookup"><span data-stu-id="fd82e-111">Assign accounts to administrative costs</span></span>

<span data-ttu-id="fd82e-112">接下来，您应该将科目与费用类型关联。</span><span class="sxs-lookup"><span data-stu-id="fd82e-112">Next, you should associate accounts with the expense types.</span></span> <span data-ttu-id="fd82e-113">过帐费用计划条目时，将借记这些科目。</span><span class="sxs-lookup"><span data-stu-id="fd82e-113">These accounts will be debited when expense schedule entries are posted.</span></span> <span data-ttu-id="fd82e-114">对方科目在每个租赁的 **执行费用付款计划** 行中指定。</span><span class="sxs-lookup"><span data-stu-id="fd82e-114">The offset account is specified on the **Executory costs payment schedule** lines on each lease.</span></span>

1. <span data-ttu-id="fd82e-115">转到 **资产租赁 \> 设置 \> 资产租赁参数**。</span><span class="sxs-lookup"><span data-stu-id="fd82e-115">Go to **Asset leasing \> Setup \> Asset leasing parameters**.</span></span>
2. <span data-ttu-id="fd82e-116">在 **科目** 选项卡的 **执行成本** 快速选项卡上 **费用类型** 字段中，选择费用类型。</span><span class="sxs-lookup"><span data-stu-id="fd82e-116">On the **Accounts** tab, on the **Executory costs** FastTab, in the **Expense type** field, select the expense type.</span></span>
3. <span data-ttu-id="fd82e-117">选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="fd82e-117">Select **Add**.</span></span>
4. <span data-ttu-id="fd82e-118">在 **帐簿类型** 字段中，选择要链接到管理费用的帐簿类型。</span><span class="sxs-lookup"><span data-stu-id="fd82e-118">In the **Book type** field, select the book type to link to the administrative costs.</span></span>

    > [!NOTE]
    > <span data-ttu-id="fd82e-119">可以将多种帐簿类型链接到同一个费用科目。</span><span class="sxs-lookup"><span data-stu-id="fd82e-119">Multiple book types can be linked to the same expense account.</span></span>

5. <span data-ttu-id="fd82e-120">在 **科目代码** 字段中，指定帐簿应该应用于的租赁：</span><span class="sxs-lookup"><span data-stu-id="fd82e-120">In the **Account code** field, specify which leases the book should be applied to:</span></span>

    - <span data-ttu-id="fd82e-121">**所有** – 将帐簿应用于所有租赁。</span><span class="sxs-lookup"><span data-stu-id="fd82e-121">**All** – Apply the book to all leases.</span></span>
    - <span data-ttu-id="fd82e-122">**组** – 将帐簿应用于特定租赁组。</span><span class="sxs-lookup"><span data-stu-id="fd82e-122">**Group** – Apply the book to a specific group of leases.</span></span>
    - <span data-ttu-id="fd82e-123">**表** – 将帐簿应用于特定租赁。</span><span class="sxs-lookup"><span data-stu-id="fd82e-123">**Table** – Apply the book to specific leases.</span></span>

6. <span data-ttu-id="fd82e-124">如果在 **帐户编码** 字段中选择了 **组** 或 **表**，请在 **科目/组编号** 字段中选择科目编号或组编号。</span><span class="sxs-lookup"><span data-stu-id="fd82e-124">If you selected **Group** or **Table** in the **Account code** field, select an account number or group number in the **Account/Group number** field.</span></span>
7. <span data-ttu-id="fd82e-125">在相应字段中，选择金融租赁主科目和经营性租赁主科目。</span><span class="sxs-lookup"><span data-stu-id="fd82e-125">In the appropriate fields, select the finance lease main account and the operating lease main account.</span></span>

<span data-ttu-id="fd82e-126">完成这些步骤后，您可以通过所选租赁的 **租赁详细信息** 页上的 **执行成本付款计划** 行添加费用。</span><span class="sxs-lookup"><span data-stu-id="fd82e-126">When you've completed these steps, you can add expenses through the **Executory costs payment schedule** lines on the **Lease details** page of a selected lease.</span></span> <span data-ttu-id="fd82e-127">或者，也可以在创建新租赁时增加费用。</span><span class="sxs-lookup"><span data-stu-id="fd82e-127">Alternatively, you can add expenses when you create a new lease.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
