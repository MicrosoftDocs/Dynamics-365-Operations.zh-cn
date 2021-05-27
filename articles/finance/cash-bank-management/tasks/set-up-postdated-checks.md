---
title: 设置远期支票
description: 本主题说明如何指定是否过帐远期支票的日记帐分录，以及选用哪一个过帐日记帐来清算会计条目和供应商付款。
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankParameters, VendPaymMode, CustPaymMode
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d0d4afd74f9a0f9018629fa92ab6595bfa94f973
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026197"
---
# <a name="set-up-postdated-checks"></a><span data-ttu-id="cc25c-103">设置远期支票</span><span class="sxs-lookup"><span data-stu-id="cc25c-103">Set up postdated checks</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cc25c-104">本主题说明如何指定是否过帐远期支票的日记帐分录，以及选用哪一个过帐日记帐来清算会计条目和供应商付款。</span><span class="sxs-lookup"><span data-stu-id="cc25c-104">This topic explains how to specify whether to post journal entries for postdated checks and which posting journals to use for clearing entries and vendor payments.</span></span> <span data-ttu-id="cc25c-105">您还可以指定已签发支票、已收到支票和预缴税金的清算帐户。</span><span class="sxs-lookup"><span data-stu-id="cc25c-105">You can also specify clearing accounts for issued checks, received checks, and withholding tax.</span></span> <span data-ttu-id="cc25c-106">签发用于在将来时间进行付款和收款的远期支票。</span><span class="sxs-lookup"><span data-stu-id="cc25c-106">Postdated checks that are issued to make and receive payments on a future date.</span></span> <span data-ttu-id="cc25c-107">您可以指定支票是否必须在其到期日期之前反映在会计帐簿中。</span><span class="sxs-lookup"><span data-stu-id="cc25c-107">You can specify whether the check must be reflected in the accounting books before its maturity date.</span></span>



<span data-ttu-id="cc25c-108">本过程由财务主管完成。</span><span class="sxs-lookup"><span data-stu-id="cc25c-108">The role of this procedure is Treasurer.</span></span> <span data-ttu-id="cc25c-109">该程序适用于 USMF 演示公司。</span><span class="sxs-lookup"><span data-stu-id="cc25c-109">This procedure uses the USMF demo company.</span></span>


## <a name="set-up-postdated-checks"></a><span data-ttu-id="cc25c-110">设置远期支票</span><span class="sxs-lookup"><span data-stu-id="cc25c-110">Set up postdated checks</span></span>
1. <span data-ttu-id="cc25c-111">转到“现金和银行管理”>“设置”>“现金和管理银行参数”。</span><span class="sxs-lookup"><span data-stu-id="cc25c-111">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="cc25c-112">单击“远期支票”选项卡。</span><span class="sxs-lookup"><span data-stu-id="cc25c-112">Click the Postdated checks tab.</span></span>
3. <span data-ttu-id="cc25c-113">选择或清除“启用远期支票”复选框。</span><span class="sxs-lookup"><span data-stu-id="cc25c-113">Select or clear the Enable postdated checks check box.</span></span>
4. <span data-ttu-id="cc25c-114">选择或清除“过帐远期支票的日记帐条目”复选框。</span><span class="sxs-lookup"><span data-stu-id="cc25c-114">Select or clear the Post journal entries for postdated checks check box.</span></span>
5. <span data-ttu-id="cc25c-115">在“已签发支票的清算帐户”字段中，指定所需的值。</span><span class="sxs-lookup"><span data-stu-id="cc25c-115">In the Clearing account for issued checks field, specify the desired values.</span></span>
6. <span data-ttu-id="cc25c-116">在“已收到支票的清算帐户”字段中，指定所需的值。</span><span class="sxs-lookup"><span data-stu-id="cc25c-116">In the Clearing account for received checks field, specify the desired values.</span></span>
7. <span data-ttu-id="cc25c-117">在“清算实体的普通日记帐”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="cc25c-117">In the General journal for clearing entries field, type a value.</span></span>
8. <span data-ttu-id="cc25c-118">在“将远期支票转移到此供应商付款日记帐”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="cc25c-118">In the Transfer postdated checks to this vendor payment journal field, type a value.</span></span>
9. <span data-ttu-id="cc25c-119">在“预缴税金清算帐户”字段中，指定所需的值。</span><span class="sxs-lookup"><span data-stu-id="cc25c-119">In the Withholding tax clearing account field, specify the desired values.</span></span>
10. <span data-ttu-id="cc25c-120">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="cc25c-120">Click Save.</span></span>
11. <span data-ttu-id="cc25c-121">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="cc25c-121">Close the page.</span></span>
12. <span data-ttu-id="cc25c-122">转至“应付帐款”>“付款设置”>“付款方式”。</span><span class="sxs-lookup"><span data-stu-id="cc25c-122">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
13. <span data-ttu-id="cc25c-123">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="cc25c-123">Click New.</span></span>
14. <span data-ttu-id="cc25c-124">在“付款方式”字段中，输入值。</span><span class="sxs-lookup"><span data-stu-id="cc25c-124">In the Method of payment field, type a value.</span></span>
15. <span data-ttu-id="cc25c-125">选择“远期支票清算过帐”选项以指明支票金额被过帐到清算帐户中。</span><span class="sxs-lookup"><span data-stu-id="cc25c-125">Select the Postdated check clearing posting option to indicate that the check amount is posted to a clearing account.</span></span>
16. <span data-ttu-id="cc25c-126">在“帐户类型”字段中，选择“银行”。</span><span class="sxs-lookup"><span data-stu-id="cc25c-126">In the Account type field, select 'Bank'.</span></span>
    * <span data-ttu-id="cc25c-127">付款方法的抵消帐户将是银行。</span><span class="sxs-lookup"><span data-stu-id="cc25c-127">The offset account of the payment method will be a bank.</span></span>  
17. <span data-ttu-id="cc25c-128">在“付款帐户”字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="cc25c-128">In the Payment account field, specify the desired values.</span></span>
    * <span data-ttu-id="cc25c-129">选择用于扣减发票金额的银行帐户。</span><span class="sxs-lookup"><span data-stu-id="cc25c-129">Select the bank account that is used to deduct the invoice amount.</span></span>  
18. <span data-ttu-id="cc25c-130">单击保存。</span><span class="sxs-lookup"><span data-stu-id="cc25c-130">Click Save.</span></span>
19. <span data-ttu-id="cc25c-131">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="cc25c-131">Close the page.</span></span>
> [!NOTE]
> <span data-ttu-id="cc25c-132">要能够在会话日期晚于或等于到期日期时将远期支票过帐到银行帐户，您必须启用功能 **将带有远期支票的付款日记帐过帐到银行帐户的到期日期验证**。</span><span class="sxs-lookup"><span data-stu-id="cc25c-132">To be able to post a postdated check to a bank account when the session date is greater than or equal to the maturity date, you must enable the feature **Maturity date validation of posting payment journal with postdated checks to bank account**.</span></span> <span data-ttu-id="cc25c-133">当会话日期晚于或等于到期日期时，此功能让您可以过帐带有远期支票的供应商或客户的付款日记帐。</span><span class="sxs-lookup"><span data-stu-id="cc25c-133">This feature allows you to post payment journals for vendors or customers with postdated checks, when the session date is greater than or equal to the maturity date.</span></span>
> 
> <span data-ttu-id="cc25c-134">设置 **付款方式**（**应付帐款 > 付款设置 >付款方式**）时，请勿填写 **过渡帐户**。</span><span class="sxs-lookup"><span data-stu-id="cc25c-134">When setting the **Method of payment** (**Accounts payable > Payment setup > Methods of payment**), do not fill in **Bridging account**.</span></span> <span data-ttu-id="cc25c-135">在这种情况下，抵销帐户将填充为 **付款方式** 中设置的银行帐户。</span><span class="sxs-lookup"><span data-stu-id="cc25c-135">In this case, the offset account is filled in with the bank account, which is set up in the **Method of payment**.</span></span>
>  
> <span data-ttu-id="cc25c-136">启用此功能且会话日期早于到期日期时，过帐付款日记帐时将显示以下错误消息：“如果抵销帐户类型为‘银行’，到期日期必须早于或等于会话日期”。</span><span class="sxs-lookup"><span data-stu-id="cc25c-136">When the feature is enabled and the session date is less than the maturity date, the following error message is displayed when posting a payment journal, "Maturity date must be less or equal to the session date if offset account type is Bank".</span></span> <span data-ttu-id="cc25c-137">如果未启用此功能，您可以在会话日期早于到期日期时过帐带有远期支票的付款日记帐。</span><span class="sxs-lookup"><span data-stu-id="cc25c-137">If the feature is not enabled, you can post a payment journal with a postdated check when the session date is less than the maturity date.</span></span>    

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
