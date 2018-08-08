--- 
title: "创建销售税支付"
description: "结算和过帐销售税作业结算销售税帐户的销售税余额，并冲销特定期间内的销售税结算帐户。"
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 9b6e60ff6465ef0bddda2e93b07f41e47f2e1ddd
ms.contentlocale: zh-cn
ms.lasthandoff: 08/07/2018

---
# <a name="create-a-sales-tax-payment"></a><span data-ttu-id="98a08-103">创建销售税支付</span><span class="sxs-lookup"><span data-stu-id="98a08-103">Create a sales tax payment</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="98a08-104">结算和过帐销售税作业结算销售税帐户的销售税余额，并冲销特定期间内的销售税结算帐户。</span><span class="sxs-lookup"><span data-stu-id="98a08-104">The settle and post sales tax job settles sales tax balances on the sales tax accounts and offsets them to the sales tax settlement account for a given period.</span></span>

1. <span data-ttu-id="98a08-105">转到“纳税”>“申报”>“销售税”>“结算和过帐销售税”。</span><span class="sxs-lookup"><span data-stu-id="98a08-105">Go to Tax > Declarations > Sales tax > Settle and post sales tax.</span></span>
2. <span data-ttu-id="98a08-106">在“结算期间”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="98a08-106">In the Settlement period field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="98a08-107">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="98a08-107">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="98a08-108">在“开始日期”字段中输入日期。</span><span class="sxs-lookup"><span data-stu-id="98a08-108">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="98a08-109">如果未选择总帐参数页面的“包括更正”选项，会进行不同版本的结算处理。</span><span class="sxs-lookup"><span data-stu-id="98a08-109">If the Include corrections option is not selected on the General ledger parameters page, the settlement can be processed for different versions.</span></span> <span data-ttu-id="98a08-110">原始结算为某个期间间隔的首次结算，并且一个期间间隔只能处理一次。</span><span class="sxs-lookup"><span data-stu-id="98a08-110">Original is the first settlement for a period interval and can only processed once for a period interval.</span></span> <span data-ttu-id="98a08-111">最新更正将结算在原始版本创建后过帐的销售税交易记录。</span><span class="sxs-lookup"><span data-stu-id="98a08-111">Latest corrections will settle sales tax transactions which have been posted after the original version has been created.</span></span>   
5. <span data-ttu-id="98a08-112">在“交易记录日期”字段中，输入日期。</span><span class="sxs-lookup"><span data-stu-id="98a08-112">In the Transaction date field, enter a date.</span></span>
6. <span data-ttu-id="98a08-113">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="98a08-113">Click OK.</span></span>


