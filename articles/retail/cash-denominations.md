---
title: "为 POS 配置现金面额"
description: "可以在后端办公系统中定义商店的收银员、销售内勤和经理从 POS 内使用的纸币和硬币的现金面额。"
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 16231
ms.assetid: f28a827c-3a50-4d5e-83eb-e5a768db70a1
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 45e70765c43b93e9d8abab5fbb9de1d67a739a74
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="configure-cash-denominations-for-pos"></a><span data-ttu-id="a495d-103">为 POS 配置现金面额</span><span class="sxs-lookup"><span data-stu-id="a495d-103">Configure cash denominations for POS</span></span>

[!include[banner](includes/banner.md)]

<span data-ttu-id="a495d-104">可以在后端办公系统中定义商店的收银员、销售内勤和经理从 POS 内使用的纸币和硬币的现金面额。</span><span class="sxs-lookup"><span data-stu-id="a495d-104">Cash denominations for notes and coins can be defined in the back office to be used by cashiers, sales associates, and managers at the store from within the POS.</span></span> <span data-ttu-id="a495d-105">这些面额可用于为日结钱币清点或快速清点一笔销售时帮助清点现金。</span><span class="sxs-lookup"><span data-stu-id="a495d-105">These denominations can be used to aid in counting cash for end of day tender declarations or for quickly tendering a sale.</span></span>

## <a name="define-denominations"></a><span data-ttu-id="a495d-106">定义面额</span><span class="sxs-lookup"><span data-stu-id="a495d-106">Define denominations</span></span>
<span data-ttu-id="a495d-107">面额在**设置** > **商店属性中的现金清点选项**页中根据商店设置。</span><span class="sxs-lookup"><span data-stu-id="a495d-107">The denominations are set up per store on the **Set up** > **Cash declaration option from the store property** page.</span></span> 

![现金面额](./media/image1-denomination.png)

<span data-ttu-id="a495d-109">若要定义面额：</span><span class="sxs-lookup"><span data-stu-id="a495d-109">To define a denomination:</span></span>
1. <span data-ttu-id="a495d-110">单击“**新建**”。</span><span class="sxs-lookup"><span data-stu-id="a495d-110">Click **New**.</span></span>
1. <span data-ttu-id="a495d-111">指定类型（硬币还是纸币）。</span><span class="sxs-lookup"><span data-stu-id="a495d-111">Specify the type (coin or note).</span></span>
1. <span data-ttu-id="a495d-112">指定金额（值）。</span><span class="sxs-lookup"><span data-stu-id="a495d-112">Specify the amount (value).</span></span>

![现金面额](./media/image2-denomination.png)

## <a name="configure-the-functionality-profile"></a><span data-ttu-id="a495d-114">配置功能配置文件</span><span class="sxs-lookup"><span data-stu-id="a495d-114">Configure the functionality profile</span></span>
<span data-ttu-id="a495d-115">使用 POS 现金付款时，用户可使用纸币面额快速输入客户支付的金额。</span><span class="sxs-lookup"><span data-stu-id="a495d-115">When paying by cash in POS, the user can use the note denominations to quickly enter the amount paid by the customer.</span></span> <span data-ttu-id="a495d-116">在功能配置文件中，可以配置两种 POS 中的面额显示选项。</span><span class="sxs-lookup"><span data-stu-id="a495d-116">In the functionality profile, you can configure the two options for showing the denomination in POS.</span></span>

<span data-ttu-id="a495d-117">**大于或等于应付款金额**：默认情况下，POS 仅显示大于应付款金额的纸币面额，这样就可以进行一键式付款。</span><span class="sxs-lookup"><span data-stu-id="a495d-117">**Greater or equal to amount due**: By default, POS will only show the note denominations that are greater than the amount due, which allows for one-touch tendering.</span></span> <span data-ttu-id="a495d-118">例如，如果应付款金额为 7.50 美元，POS 将显示以下金额：10 美元、20 美元、50 美元和 100 美元。</span><span class="sxs-lookup"><span data-stu-id="a495d-118">For example, if the amount due is $7.50, POS would show the following denominations: $10, $20, $50, and $100.</span></span> <span data-ttu-id="a495d-119">触摸这些金额中的任何一个都将自动为销售收取这笔金额。</span><span class="sxs-lookup"><span data-stu-id="a495d-119">Touching any of these amounts will automatically tender the sale for that amount.</span></span> <span data-ttu-id="a495d-120">不显示 1 美元和 5 美元纸币，因为这些金额低于应付款金额。</span><span class="sxs-lookup"><span data-stu-id="a495d-120">The $1 and $5 notes are not shown since these amounts are less than the amount due.</span></span>

<span data-ttu-id="a495d-121">**全部面额**：选择此选项将在 POS 中始终显示所有纸币面额，不受应付款金额的影响。</span><span class="sxs-lookup"><span data-stu-id="a495d-121">**All denominations**: Select this option to always show all note denominations in POS, regardless of the amount due.</span></span> <span data-ttu-id="a495d-122">这意味着用户可以使用纸币组合以凑够应付款金额。</span><span class="sxs-lookup"><span data-stu-id="a495d-122">This means that the user can use a combination of notes to reach the amount due.</span></span> <span data-ttu-id="a495d-123">例如，如果应付款金额为 25 美元，则用户可选择 20 美元和 5 美元来完成销售。</span><span class="sxs-lookup"><span data-stu-id="a495d-123">For example, if the amount due is $25.00, the user can choose $20 and $5 to complete the sale.</span></span>

