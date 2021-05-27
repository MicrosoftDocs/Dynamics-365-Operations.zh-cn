---
title: 记录 TDS 可退税证书编号
description: 本主题说明如何使用可退税证书页面，记录特定供应商、客户或分类帐收到的从源扣缴税款 (TDS) 证书的证书编号和日期。
author: kailiang
mms.date: 02/12/2021
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
ms.openlocfilehash: b501c331cccc6d030f36d0a13ba0a6a13c08c733
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023044"
---
# <a name="record-tds-recoverable-certificate-numbers"></a><span data-ttu-id="c2d84-103">记录 TDS 可退税证书编号</span><span class="sxs-lookup"><span data-stu-id="c2d84-103">Record TDS recoverable certificate numbers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c2d84-104">本主题说明如何使用 **可退税证书** 页面，记录特定供应商、客户或分类帐收到的从源扣缴税款 (TDS) 证书的证书编号和日期。</span><span class="sxs-lookup"><span data-stu-id="c2d84-104">This topic explains how to use the **Recoverable certificates** page to record the certificate numbers and dates for Tax Deducted at Source (TDS) certificates that are received for a specific vendor, customer, or ledger.</span></span> <span data-ttu-id="c2d84-105">若要更新在此页面上为 TDS 交易记录的 TDS 证书编号和日期，请使用 **更新证书** 页面（**总帐 \> 定期 \> 预缴税款 \> 更新证书**）。</span><span class="sxs-lookup"><span data-stu-id="c2d84-105">To update the TDS certificate numbers and dates that are recorded for TDS transactions on this page, use the **Update certificate** page (**General ledger \> Periodic \> Withholding tax \> Update certificate**).</span></span> <span data-ttu-id="c2d84-106">更新完 TDS 证书编号后，请关闭它们。</span><span class="sxs-lookup"><span data-stu-id="c2d84-106">After you've finished updating TDS certificate numbers, close them.</span></span>

<span data-ttu-id="c2d84-107">按照以下步骤记录 TDS 证书编号和日期。</span><span class="sxs-lookup"><span data-stu-id="c2d84-107">Follow these steps to record the TDS certificate numbers and dates.</span></span>

1. <span data-ttu-id="c2d84-108">转到 **税务 \> 间接税 \> 预缴税金 \> 可退税证书**。</span><span class="sxs-lookup"><span data-stu-id="c2d84-108">Go to **Tax \> Indirect tax \> Withholding tax \> Recoverable certificates**.</span></span>

    <span data-ttu-id="c2d84-109">[![可退税证书页面](./media/apac-ind-TDS-49.png)](./media/apac-ind-TDS-49.png)</span><span class="sxs-lookup"><span data-stu-id="c2d84-109">[![Recoverable certificates page](./media/apac-ind-TDS-49.png)](./media/apac-ind-TDS-49.png)</span></span> 

2. <span data-ttu-id="c2d84-110">在 **可退税证书** 页面上，在 **税务类型** 字段中，选择 **TDS**。</span><span class="sxs-lookup"><span data-stu-id="c2d84-110">On the **Recoverable certificates** page, in the **Tax type** field, select **TDS**.</span></span>
3. <span data-ttu-id="c2d84-111">选择 **新建** 创建记录。</span><span class="sxs-lookup"><span data-stu-id="c2d84-111">Select **New** to create a record.</span></span>
4. <span data-ttu-id="c2d84-112">在 **证书编号** 字段中，输入 TDS 证书编号。</span><span class="sxs-lookup"><span data-stu-id="c2d84-112">In the **Certificate number** field, enter the TDS certificate number.</span></span>
5. <span data-ttu-id="c2d84-113">在 **帐户类型** 字段中，选择收到 TDS 证书的帐户类型：**供应商**、**客户** 或 **分类帐**。</span><span class="sxs-lookup"><span data-stu-id="c2d84-113">In the **Account type** field, select the type of account that the TDS certificate is received for: **Vendor**, **Customer**, or **Ledger**.</span></span>
6. <span data-ttu-id="c2d84-114">在 **帐户** 字段中，选择供应商、客户或分类帐帐号，具体取决于所选的帐户类型。</span><span class="sxs-lookup"><span data-stu-id="c2d84-114">In the **Account** field, select the vendor, customer, or ledger account number, depending on the account type that you selected.</span></span> <span data-ttu-id="c2d84-115">**名称** 字段显示供应商、客户或分类帐帐户的名称。</span><span class="sxs-lookup"><span data-stu-id="c2d84-115">The **Name** field shows the name of the vendor, customer, or ledger account.</span></span>
7. <span data-ttu-id="c2d84-116">在 **证书金额** 字段中，输入 TDS 证书的金额。</span><span class="sxs-lookup"><span data-stu-id="c2d84-116">In the **Certificate amount** field, enter the amount of the TDS certificate.</span></span>
8. <span data-ttu-id="c2d84-117">在 **日期** 字段中，输入证书编号的证书日期。</span><span class="sxs-lookup"><span data-stu-id="c2d84-117">In the **Date** field, enter the certificate date for the certificate number.</span></span>
9. <span data-ttu-id="c2d84-118">选择 **查询** 以打开 **证书交易** 页面，您可以在该页面中查看更新了 TDS 证书编号和日期的 TDS 交易。</span><span class="sxs-lookup"><span data-stu-id="c2d84-118">Select **Inquiries** to open the **Certificate transactions** page, where you can view the TDS transactions that the TDS certificate number and date are updated for.</span></span> <span data-ttu-id="c2d84-119">可以在 **更新证书** 页面上更新此信息（**税务 \> 申报 \> 预缴税金 \> 更新证书**）。</span><span class="sxs-lookup"><span data-stu-id="c2d84-119">This information can be updated on the **Update certificate** page (**Tax \> Declarations \> Withholding tax \> Update certificate**).</span></span>

    <span data-ttu-id="c2d84-120">**更新证书** 页面显示每个 TDS 交易的以下信息。</span><span class="sxs-lookup"><span data-stu-id="c2d84-120">The **Update certificate** page shows the following information for each TDS transaction:</span></span>

    - <span data-ttu-id="c2d84-121">**日期** – TDS 交易的过帐日期。</span><span class="sxs-lookup"><span data-stu-id="c2d84-121">**Date** – The posting date of the TDS transaction.</span></span>
    - <span data-ttu-id="c2d84-122">**凭证** – TDS 交易的凭证号。</span><span class="sxs-lookup"><span data-stu-id="c2d84-122">**Voucher** – The voucher number of the TDS transaction.</span></span>
    - <span data-ttu-id="c2d84-123">**来源** – 用于创建 TDS 交易的模块。</span><span class="sxs-lookup"><span data-stu-id="c2d84-123">**Source** – The module that the TDS transaction was created in.</span></span>
    - <span data-ttu-id="c2d84-124">**帐户** – 为其创建了 TDS 交易的供应商、客户或分类帐帐号。</span><span class="sxs-lookup"><span data-stu-id="c2d84-124">**Account** – The vendor, customer, or ledger account number that the TDS transaction was created for.</span></span>
    - <span data-ttu-id="c2d84-125">**名称** – 为其创建了 TDS 交易的供应商、客户或分类帐帐户的名称。</span><span class="sxs-lookup"><span data-stu-id="c2d84-125">**Name** – The name of the vendor, customer, or ledger account that the TDS transaction was created for.</span></span>
    - <span data-ttu-id="c2d84-126">**金额** – 计算 TDS 的发票金额。</span><span class="sxs-lookup"><span data-stu-id="c2d84-126">**Amount** – The invoice amount that the TDS was calculated on.</span></span>
    - <span data-ttu-id="c2d84-127">**税额** – 为交易计算的 TDS 税额。</span><span class="sxs-lookup"><span data-stu-id="c2d84-127">**Tax amount** – The TDS tax amount that was calculated for the transaction.</span></span>
    - <span data-ttu-id="c2d84-128">**证书日期** – 为 TDS 交易更新的 TDS 证书日期。</span><span class="sxs-lookup"><span data-stu-id="c2d84-128">**Certificate date** – The TDS certificate date that was updated for the TDS transaction.</span></span>
    - <span data-ttu-id="c2d84-129">**证书编号** – 为 TDS 交易更新的 TDS 证书编号。</span><span class="sxs-lookup"><span data-stu-id="c2d84-129">**Certificate number** – TDS certificate number that was updated for the TDS transaction.</span></span>

10. <span data-ttu-id="c2d84-130">在 **可退税证书** 页面上，选中 **已关闭** 复选框，以便在 **更新证书** 页面上为 TDS 交易更新完它后，关闭 TDS 证书编号。</span><span class="sxs-lookup"><span data-stu-id="c2d84-130">On the **Recoverable certificates** page, select the **Closed** check box to close the TDS certificate number after you've finished updating it for TDS transactions on the **Update certificate** page.</span></span>

    <span data-ttu-id="c2d84-131">若要针对页面上的所有记录选中 **已关闭** 复选框，请选择 **全部标记**。</span><span class="sxs-lookup"><span data-stu-id="c2d84-131">To select the **Closed** check box for all records on the page, select **Mark all**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c2d84-132">为其选中 **已关闭** 复选框的 TDS 证书编号在 **更新证书** 页面上都不可用。</span><span class="sxs-lookup"><span data-stu-id="c2d84-132">TDS certificate numbers that the **Closed** check box is selected for aren't available on the **Update certificate** page.</span></span>
