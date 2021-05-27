---
title: 更新 TDS 交易的证书编号和日期
description: 本主题说明如何更新从源扣缴税款 (TDS) 的为供应商、客户和分类帐帐户记录的可退税证书编号和日期。
author: kailiang
ms.date: 02/12/2021
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
ms.openlocfilehash: 248de8e12703a84482b67d0899857a6efb33531c
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023054"
---
# <a name="update-certificate-numbers-and-dates-for-tds-transactions"></a><span data-ttu-id="b4df2-103">更新 TDS 交易的证书编号和日期</span><span class="sxs-lookup"><span data-stu-id="b4df2-103">Update certificate numbers and dates for TDS transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b4df2-104">本主题说明如何更新从源扣缴税款 (TDS) 的为供应商、客户和分类帐帐户记录的可退税证书编号和日期。</span><span class="sxs-lookup"><span data-stu-id="b4df2-104">This topic explains how to update the recoverable certificate numbers and dates that were recorded for vendor, customer, and ledger accounts for Tax Deducted at Source (TDS).</span></span> <span data-ttu-id="b4df2-105">您可以在 **可退税证书** 页面上查看 TDS 交易的证书。</span><span class="sxs-lookup"><span data-stu-id="b4df2-105">You can view the certificates for TDS transactions on the **Recoverable certificates** page.</span></span> <span data-ttu-id="b4df2-106">可以使用 **更新证书** 页面更新证书。</span><span class="sxs-lookup"><span data-stu-id="b4df2-106">You can update the certificates by using the **Update Certificates** page.</span></span>

<span data-ttu-id="b4df2-107">按照以下步骤更新 TDS 交易的证书编号和日期。</span><span class="sxs-lookup"><span data-stu-id="b4df2-107">Follow these steps to update certificate numbers and dates for TDS transactions.</span></span>

1. <span data-ttu-id="b4df2-108">转到 **税务 \> 申报 \> 预缴税金 \> 更新证书**。</span><span class="sxs-lookup"><span data-stu-id="b4df2-108">Go to **Tax \> Declarations \> Withholding tax \> Update certificate**.</span></span>

    <span data-ttu-id="b4df2-109">[![更新证书页面](./media/apac-ind-TDS-45.png)](./media/apac-ind-TDS-45.png)</span><span class="sxs-lookup"><span data-stu-id="b4df2-109">[![Update certificate page](./media/apac-ind-TDS-45.png)](./media/apac-ind-TDS-45.png)</span></span>

2. <span data-ttu-id="b4df2-110">在 **更新证书** 页面的 **选择** 部分中，在 **税务类型** 字段中，选择 **TDS**。</span><span class="sxs-lookup"><span data-stu-id="b4df2-110">On the **Update certificate** page, in the **Select** section, in the **Tax type** field, select **TDS**.</span></span>
3. <span data-ttu-id="b4df2-111">在 **证书编号** 字段中，选择客户或供应商的 TDS 证书编号。</span><span class="sxs-lookup"><span data-stu-id="b4df2-111">In the **Certificate number** field, select the customer's or vendor's TDS certificate number.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b4df2-112">**证书编号** 字段仅列出 **可退税证书** 页面上清除了 **已关闭** 复选框的 TDS 证书编号。</span><span class="sxs-lookup"><span data-stu-id="b4df2-112">The **Certificate number** field lists only TDS certificate numbers that the **Closed** check box is cleared for on the **Recoverable certificates** page.</span></span>

    <span data-ttu-id="b4df2-113">**证书日期** 字段显示证书日期。</span><span class="sxs-lookup"><span data-stu-id="b4df2-113">The **Certificate date** field shows the certificate date.</span></span> <span data-ttu-id="b4df2-114">**帐户类型** 字段显示接收了 TDS 证书编号的帐户的类型，**名称** 字段显示帐户的名称。</span><span class="sxs-lookup"><span data-stu-id="b4df2-114">The **Account type** field shows the type of account that the TDS certificate number is received for, and the **Name** field shows the name of the account.</span></span>

5. <span data-ttu-id="b4df2-115">在 **开始日期** 和 **结束日期** 字段中，选择要显示 TDS 交易的期间的开始日期和结束日期。</span><span class="sxs-lookup"><span data-stu-id="b4df2-115">In the **From date** and **To date** fields, select the start and end dates of the period to show the TDS transactions for.</span></span>
6. <span data-ttu-id="b4df2-116">选择 **显示数据** 以查看在选定期间过帐的 TDS 交易。</span><span class="sxs-lookup"><span data-stu-id="b4df2-116">Select **Show data** to view the TDS transactions that were posted during the selected period.</span></span>

    <span data-ttu-id="b4df2-117">在 **概述** 选项卡上，上部窗格中的网格显示有关在选定期间为供应商或客户过帐的每个 TDS 交易的以下信息：</span><span class="sxs-lookup"><span data-stu-id="b4df2-117">On the **Overview** tab, the grid in the upper pane shows the following information about each TDS transaction that was posted for the vendor or customer during the selected period:</span></span>

    - <span data-ttu-id="b4df2-118">**凭证** – TDS 交易的凭证号。</span><span class="sxs-lookup"><span data-stu-id="b4df2-118">**Voucher** – The voucher number of the TDS transaction.</span></span>
    - <span data-ttu-id="b4df2-119">**日期** – TDS 交易的日期。</span><span class="sxs-lookup"><span data-stu-id="b4df2-119">**Date** – The date of the TDS transaction.</span></span>
    - <span data-ttu-id="b4df2-120">**金额** – 计算 TDS 的发票金额。</span><span class="sxs-lookup"><span data-stu-id="b4df2-120">**Amount** – The invoice amount that the TDS was calculated on.</span></span>
    - <span data-ttu-id="b4df2-121">**税额** – 为交易计算的 TDS 税额。</span><span class="sxs-lookup"><span data-stu-id="b4df2-121">**Tax amount** – The TDS tax amount that was calculated for the transaction.</span></span>

7. <span data-ttu-id="b4df2-122">若要将特定 TDS 交易从上部网格移动到下部网格，选择交易，然后选择 **包括**。</span><span class="sxs-lookup"><span data-stu-id="b4df2-122">To move specific TDS transactions from the upper grid to the lower grid, select the transactions, and then select **Include**.</span></span> <span data-ttu-id="b4df2-123">或者，选择 **全部包括** 以将所有 TDS 交易从上部网格移动到下部网格。</span><span class="sxs-lookup"><span data-stu-id="b4df2-123">Alternatively, select **Include all** to move all TDS transactions from the upper grid to the lower grid.</span></span>

    <span data-ttu-id="b4df2-124">若要将特定 TDS 交易或所有 TDS 交易从下部网格移动到上部网格，请使用 **排除** 或 **全部排除** 按钮。</span><span class="sxs-lookup"><span data-stu-id="b4df2-124">To move specific TDS transactions or all TDS transactions from the lower grid to the upper grid, use the **Exclude** or **Exclude all** button.</span></span>

8. <span data-ttu-id="b4df2-125">选择 **更新** 以更新下部网格中 TDS 交易的 **证书编号** 和 **证书日期** 字段。</span><span class="sxs-lookup"><span data-stu-id="b4df2-125">Select **Update** to update the **Certificate number** and **Certificate date** fields for TDS transactions in the lower grid.</span></span>
10. <span data-ttu-id="b4df2-126">转到 **税务 \> 间接税 \> 预缴税金 \> 可退税证书** 并选择 **查询**，以查看在 **证书交易** 页面上具有新证书编号的已更新交易行。</span><span class="sxs-lookup"><span data-stu-id="b4df2-126">Go to **Tax \> Indirect taxes \> Withholding tax \> Recoverable certificate**, and select **Inquiry** to view the updated transaction lines that have the new certificate numbers on the **Certificate transactions** page.</span></span>

    <span data-ttu-id="b4df2-127">[![证书交易页面](./media/apac-ind-TDS-46.png)](./media/apac-ind-TDS-46.png)</span><span class="sxs-lookup"><span data-stu-id="b4df2-127">[![Certificate transactions page](./media/apac-ind-TDS-46.png)](./media/apac-ind-TDS-46.png)</span></span>
