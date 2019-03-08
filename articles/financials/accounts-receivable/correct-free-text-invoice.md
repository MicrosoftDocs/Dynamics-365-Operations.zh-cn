---
title: 更正普通发票
description: 本文说明如更正已过帐的普通发票，并作为更正发票重新签发该发票。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c8c1b90b7b2c02a53e53cc13d70445a237b126d4
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "364595"
---
# <a name="correct-a-free-text-invoice"></a><span data-ttu-id="8fd11-103">更正普通发票</span><span class="sxs-lookup"><span data-stu-id="8fd11-103">Correct a free text invoice</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8fd11-104">本文说明如更正已过帐的普通发票，并作为更正发票重新签发该发票。</span><span class="sxs-lookup"><span data-stu-id="8fd11-104">This article explains how to correct a free text invoice that has been posted and reissue it as a corrected invoice.</span></span>

<span data-ttu-id="8fd11-105">若要更正已过帐的普通发票，请打开已过帐的普通发票。</span><span class="sxs-lookup"><span data-stu-id="8fd11-105">To correct a free text invoice that has already been posted, open the posted free text invoice.</span></span> <span data-ttu-id="8fd11-106">在**发票**页上，选择**取消**，然后选择**更正发票**。</span><span class="sxs-lookup"><span data-stu-id="8fd11-106">On the **Invoice** page, select **Cancel**, and then select **Correct invoice**.</span></span> <span data-ttu-id="8fd11-107">选择一个原因代码，添加注释，并且为新的已更正发票选择日期。</span><span class="sxs-lookup"><span data-stu-id="8fd11-107">Select a reason code, add comments, and select the date for new corrected invoice.</span></span> <span data-ttu-id="8fd11-108">您可以修改已更正发票并将其过帐。</span><span class="sxs-lookup"><span data-stu-id="8fd11-108">You can modify the corrected invoice, and post it.</span></span> 

<span data-ttu-id="8fd11-109">在您过帐已更正发票时，会为一个等于原始发票金额的贷方金额创建取消发票。</span><span class="sxs-lookup"><span data-stu-id="8fd11-109">When you post the corrected invoice, a canceling invoice is created for a credit amount that equals the original invoice amount.</span></span> <span data-ttu-id="8fd11-110">因此，原始发票和取消发票的组合余额为 0（零）。</span><span class="sxs-lookup"><span data-stu-id="8fd11-110">Therefore, the combined balance of the original invoice and the canceling invoice is 0 (zero).</span></span> <span data-ttu-id="8fd11-111">会比对原始发票结算取消发票。</span><span class="sxs-lookup"><span data-stu-id="8fd11-111">The canceling invoice is settled against the original invoice.</span></span> 

<span data-ttu-id="8fd11-112">在过帐已更正发票后，您将具有三个发票：</span><span class="sxs-lookup"><span data-stu-id="8fd11-112">After you post the corrected invoice, you will have three invoices:</span></span>

-   <span data-ttu-id="8fd11-113">**原始发票** – 包括您正在更改的信息的发票。</span><span class="sxs-lookup"><span data-stu-id="8fd11-113">**Original invoice** – The invoice that includes the information that you're correcting.</span></span>
-   <span data-ttu-id="8fd11-114">**正在取消的发票** – 创建以取消最近更改的发票的系统生成的货方发票。</span><span class="sxs-lookup"><span data-stu-id="8fd11-114">**Canceling invoice** – The system-generated credit invoice that was created to cancel the invoice that was most recently corrected.</span></span>
-   <span data-ttu-id="8fd11-115">**已更正的发票** – 包含已更正发票信息的发票。</span><span class="sxs-lookup"><span data-stu-id="8fd11-115">**Corrected invoice** – The invoice that contains the corrected invoice information.</span></span>

<span data-ttu-id="8fd11-116">您可以通过两种方式标识取消和更正发票：</span><span class="sxs-lookup"><span data-stu-id="8fd11-116">You can identify canceling and correcting invoices in two ways:</span></span>

-   <span data-ttu-id="8fd11-117">**所有普通发票**页包括**更正**列，在其中您可以看到哪些发票是正在取消的发票和已更正的发票。</span><span class="sxs-lookup"><span data-stu-id="8fd11-117">The **All free text invoices** page includes a **Correction** column, where you can see which invoices are canceling invoices and corrected invoices.</span></span>
-   <span data-ttu-id="8fd11-118">普通发票的标题显示状态**正在取消发票‘\[发票编号\]** 或**已更正的发票‘\[发票编号\]**。</span><span class="sxs-lookup"><span data-stu-id="8fd11-118">The header of the free text invoice shows a status of **Cancelling invoice '\[invoice number\]'** or **Corrected invoice '\[invoice number\]'**.</span></span>

> [!NOTE]
> <span data-ttu-id="8fd11-119">只有当选择**普通发票更正**配置键后，此功能才可用。</span><span class="sxs-lookup"><span data-stu-id="8fd11-119">This feature is available only if the **Free text invoice correction** configuration key is selected.</span></span>



