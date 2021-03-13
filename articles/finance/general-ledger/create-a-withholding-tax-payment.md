---
title: 创建预缴税金支付
description: 预缴税金支付作业过程结算预缴税金帐户中应付帐款中的预缴税金余额，并冲销特定期间内的预缴税金结算帐户。 本主题列出了设置预缴税金支付的步骤。
author: roschlom
manager: AnnBe
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: e522711340b663bd849825b3d4dd2b7e78e4737c
ms.sourcegitcommit: 630a0b3f800f36ced49b79156dd52132904fef75
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/25/2021
ms.locfileid: "5060707"
---
# <a name="create-a-withholding-tax-payment"></a><span data-ttu-id="38761-104">创建预缴税金支付</span><span class="sxs-lookup"><span data-stu-id="38761-104">Create a withholding tax payment</span></span>

<span data-ttu-id="38761-105">预缴税金支付作业过程结算预缴税金帐户中应付帐款中的预缴税金余额，并冲销特定期间内的预缴税金结算帐户。</span><span class="sxs-lookup"><span data-stu-id="38761-105">The Withholding tax payment job procedure settles withholding tax balances from Accounts payable on withholding tax accounts, and offsets them to the withholding tax settlement account for a given period.</span></span> <span data-ttu-id="38761-106">本主题列出了设置预缴税金支付的步骤。</span><span class="sxs-lookup"><span data-stu-id="38761-106">This topic lists the steps for setting up a withholding tax payment.</span></span>

> [!NOTE] 
> <span data-ttu-id="38761-107">计算预缴税金支付时，不考虑预缴税金冲销（来自应收帐款）。</span><span class="sxs-lookup"><span data-stu-id="38761-107">Withholding tax offset (from accounts receivable) is not taken into account when a withholding tax payment is calculated.</span></span>

1. <span data-ttu-id="38761-108">转到 **导航窗格 > 模块 > 纳税 > 申报 > 预缴税金 > 预缴税金支付**。</span><span class="sxs-lookup"><span data-stu-id="38761-108">Go to **Navigation pane > Modules > Tax > Declarations > Withholding tax > Withholding tax payment**.</span></span>
2. <span data-ttu-id="38761-109">在 **结算期间** 字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="38761-109">In the **Settlement period** field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="38761-110">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="38761-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="38761-111">在 **开始日期** 字段中输入日期。</span><span class="sxs-lookup"><span data-stu-id="38761-111">In the **From date** field, enter a date.</span></span>
5. <span data-ttu-id="38761-112">在 **交易记录日期** 字段中，输入日期。</span><span class="sxs-lookup"><span data-stu-id="38761-112">In the **Transaction date** field, enter a date.</span></span>
6. <span data-ttu-id="38761-113">选择 **更新** 将预缴税金支付凭证过帐到预缴税金结算帐户。</span><span class="sxs-lookup"><span data-stu-id="38761-113">Select **Update** to post withholding tax payment voucher to the withholding tax settlement account.</span></span>
7. <span data-ttu-id="38761-114">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="38761-114">Click **OK**.</span></span>

![预缴税金支付的参数](media/withholding-tax-payment.png)
