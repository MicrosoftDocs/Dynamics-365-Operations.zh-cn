---
title: 查看 TDS 结算期间的已过帐 TDS 付款和交易
description: 本主题说明如何查看在结算期间内过帐的从源扣缴税款 (TDS) 付款和交易。
author: kailiang
ms.date: 03/12/2021
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
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 2bada42073e46c69101e6d31f3328a2eeb95f880
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023051"
---
# <a name="view-posted-tds-payments-and-transactions-for-a-tds-settlement-period"></a><span data-ttu-id="ccec9-103">查看 TDS 结算期间的已过帐 TDS 付款和交易</span><span class="sxs-lookup"><span data-stu-id="ccec9-103">View posted TDS payments and transactions for a TDS settlement period</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ccec9-104">本主题说明如何查看在结算期间内过帐的从源扣缴税款 (TDS) 付款和交易。</span><span class="sxs-lookup"><span data-stu-id="ccec9-104">This topic explains how to view the Tax Deducted at Source (TDS) payments and transactions that were posted for a settlement period.</span></span>

1. <span data-ttu-id="ccec9-105">转到 **税 \> 间接税 \> 预缴税金 \> 预缴税金结算期间**。</span><span class="sxs-lookup"><span data-stu-id="ccec9-105">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax settlement periods**.</span></span>

    <span data-ttu-id="ccec9-106">[![预缴税金结算期间页面](./media/apac-ind-TDS-50.png)](./media/apac-ind-TDS-50.png)</span><span class="sxs-lookup"><span data-stu-id="ccec9-106">[![Withholding tax settlement periods page](./media/apac-ind-TDS-50.png)](./media/apac-ind-TDS-50.png)</span></span>

2. <span data-ttu-id="ccec9-107">在 **预缴税金结算期间** 页面上，选择 **预缴税金付款** 打开 **预缴税金付款** 页，您可以在其中查看针对特定 TDS 结算期间进行的 TDS 结算。</span><span class="sxs-lookup"><span data-stu-id="ccec9-107">On the **Withholding tax settlement periods** page, select **Withholding tax payments** to open the **Withholding tax payments** page, where you can view the TDS settlements that were made for a specific TDS settlement period.</span></span>

    <span data-ttu-id="ccec9-108">**概览** 选项卡显示以下信息：</span><span class="sxs-lookup"><span data-stu-id="ccec9-108">The **Overview** tab shows the following information:</span></span>

    - <span data-ttu-id="ccec9-109">**日期** – TDS 结算的日期。</span><span class="sxs-lookup"><span data-stu-id="ccec9-109">**Date** – The date of TDS settlement.</span></span>
    - <span data-ttu-id="ccec9-110">**凭证** – TDS 结算交易的凭证号。</span><span class="sxs-lookup"><span data-stu-id="ccec9-110">**Voucher** – The voucher number of the TDS settlement transaction.</span></span>
    - <span data-ttu-id="ccec9-111">**税务类型** – 运行结算流程的税务类型。</span><span class="sxs-lookup"><span data-stu-id="ccec9-111">**Tax type** – The tax type that the settlement process is run for.</span></span>
    - <span data-ttu-id="ccec9-112">**纳税帐号 (TAN)** – 已结算的 TDS 交易的纳税帐号 (TAN)。</span><span class="sxs-lookup"><span data-stu-id="ccec9-112">**Tax Account Number (TAN)** – The Tax Account Number (TAN) of the settled TDS transaction.</span></span>
    - <span data-ttu-id="ccec9-113">**结算期间** – 运行 TDS 结算流程的结算期间。</span><span class="sxs-lookup"><span data-stu-id="ccec9-113">**Settlement period** – The settlement period that the TDS settlement process is run for.</span></span>
    - <span data-ttu-id="ccec9-114">**开始日期** – 结算期间的开始日期。</span><span class="sxs-lookup"><span data-stu-id="ccec9-114">**From date** – The start date of the settlement period.</span></span>
    - <span data-ttu-id="ccec9-115">**结束日期** – 结算期间的结束日期。</span><span class="sxs-lookup"><span data-stu-id="ccec9-115">**To date** – The end date of the settlement period.</span></span>
    - <span data-ttu-id="ccec9-116">**预缴税金付款版本** – 预缴税金付款的版本：**原始**、**最新更正** 或 **总计清单**。</span><span class="sxs-lookup"><span data-stu-id="ccec9-116">**Withholding tax payment version** – The version of the withholding tax payment: **Original**, **Latest corrections**, or **Total list**.</span></span>

5. <span data-ttu-id="ccec9-117">选择 **凭证** 可以查看 TDS 交易的凭证条目。</span><span class="sxs-lookup"><span data-stu-id="ccec9-117">Select **Voucher** to view the voucher entries for the TDS transaction.</span></span>
6. <span data-ttu-id="ccec9-118">选择 **预缴税金交易** 可以查看在结算期间内为特定期间结算的 TDS 交易的详细信息。</span><span class="sxs-lookup"><span data-stu-id="ccec9-118">Select **Withholding tax transactions** to view the details of the TDS transactions that were settled for a specific period during a settlement period.</span></span> <span data-ttu-id="ccec9-119">选择 **凭证** 可以查看 TDS 交易的凭证条目。</span><span class="sxs-lookup"><span data-stu-id="ccec9-119">Select **Voucher** to view the voucher entries for the TDS transaction.</span></span> <span data-ttu-id="ccec9-120">选择 **预缴税金组分** 可以查看针对特定 TDS 税代码为每个 TDS 税种组分计算的 TDS。</span><span class="sxs-lookup"><span data-stu-id="ccec9-120">Select **Withholding tax components** to view the TDS that was calculated per TDS tax component for a specific TDS tax code.</span></span>
7. <span data-ttu-id="ccec9-121">关闭 **预缴税金付款** 页将返回 **预缴税金结算期间** 页。</span><span class="sxs-lookup"><span data-stu-id="ccec9-121">Close the **Withholding tax payments** page to return to the **Withholding tax settlement periods** page.</span></span>
8. <span data-ttu-id="ccec9-122">选择 **预缴税金交易** 可以查看在结算期间内结算的 TDS 交易的详细信息。</span><span class="sxs-lookup"><span data-stu-id="ccec9-122">Select **Withholding tax transactions** to view the details of the TDS transactions that were settled for the settlement period.</span></span>
