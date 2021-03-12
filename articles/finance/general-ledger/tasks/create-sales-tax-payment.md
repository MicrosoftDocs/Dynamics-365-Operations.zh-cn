---
title: 创建销售税支付
description: 结算和过帐销售税作业过程结算销售税帐户的销售税余额，并冲销特定期间内的销售税结算帐户。
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9b5e3e26e19bd0a9dbf878626328da267b61964f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968696"
---
# <a name="create-a-sales-tax-payment"></a><span data-ttu-id="b4c13-103">创建销售税支付</span><span class="sxs-lookup"><span data-stu-id="b4c13-103">Create a sales tax payment</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b4c13-104">结算和过帐销售税作业过程结算销售税帐户的销售税余额，并冲销特定期间内的销售税结算帐户。</span><span class="sxs-lookup"><span data-stu-id="b4c13-104">The settle and post sales tax job procedure settles sales tax balances on the sales tax accounts, and offsets them to the sales tax settlement account for a given period.</span></span>

1. <span data-ttu-id="b4c13-105">转到 **纳税 > 申报 > 销售税 > 结算和过帐销售税**。</span><span class="sxs-lookup"><span data-stu-id="b4c13-105">Go to **Tax > Declarations > Sales tax > Settle and post sales tax**.</span></span>
2. <span data-ttu-id="b4c13-106">在 **结算期间** 字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="b4c13-106">In the **Settlement period** field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="b4c13-107">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="b4c13-107">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="b4c13-108">在 **开始日期** 字段中输入日期。</span><span class="sxs-lookup"><span data-stu-id="b4c13-108">In the **From date** field, enter a date.</span></span>
    * <span data-ttu-id="b4c13-109">如果未选择 **总帐参数** 页面的 **包括更正** 选项，会进行不同版本的结算处理。</span><span class="sxs-lookup"><span data-stu-id="b4c13-109">If you don't select the **Include corrections** option on the **General ledger parameters** page, the settlement can be processed for different versions.</span></span> <span data-ttu-id="b4c13-110">原始结算为某个期间间隔的首次结算，并且一个期间间隔只能处理一次。</span><span class="sxs-lookup"><span data-stu-id="b4c13-110">Original is the first settlement for a period interval and can be processed only once for a period interval.</span></span> <span data-ttu-id="b4c13-111">最新更正将结算在原始版本创建后过帐的销售税交易记录。</span><span class="sxs-lookup"><span data-stu-id="b4c13-111">The latest corrections will settle sales tax transactions which have been posted after the original version has been created.</span></span>   
5. <span data-ttu-id="b4c13-112">在 **交易记录日期** 字段中，输入日期。</span><span class="sxs-lookup"><span data-stu-id="b4c13-112">In the **Transaction date** field, enter a date.</span></span>
6. <span data-ttu-id="b4c13-113">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="b4c13-113">Click **OK**.</span></span>

