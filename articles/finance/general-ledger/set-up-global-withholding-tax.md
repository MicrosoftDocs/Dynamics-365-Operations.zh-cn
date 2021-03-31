---
title: 设置全球预缴税金
description: 本主题列出了为销售和购买设置全球预缴税金的步骤。
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
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 00c472e90f4926c52ffe9b19661e68cbfa6bd493
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5204825"
---
# <a name="set-up-global-withholding-tax"></a><span data-ttu-id="c028c-103">设置全球预缴税金</span><span class="sxs-lookup"><span data-stu-id="c028c-103">Set up global withholding tax</span></span>

<span data-ttu-id="c028c-104">本主题列出了为销售和购买设置全球预缴税金的步骤。</span><span class="sxs-lookup"><span data-stu-id="c028c-104">This topic lists the steps for setting up global withholding tax for sales and purchases.</span></span> 

1. <span data-ttu-id="c028c-105">在 **预缴税金主管机构** 页上设置预缴税金主管机构。</span><span class="sxs-lookup"><span data-stu-id="c028c-105">Set up withholding tax authorities on the **Withholding tax authorities** page.</span></span>

2. <span data-ttu-id="c028c-106">在 **预缴税金结算期间** 页上设置预缴结算期间。</span><span class="sxs-lookup"><span data-stu-id="c028c-106">Set up withholding settlement periods on the **Withholding tax settlement periods** page.</span></span>

3. <span data-ttu-id="c028c-107">在 **预缴税金 > 分类帐过帐组** 页上设置预缴分类帐过帐组。</span><span class="sxs-lookup"><span data-stu-id="c028c-107">Set up withholding ledger posting group on the **Withholding tax > ledger posting group** page.</span></span>

   > [!Note] 
   >
   > <span data-ttu-id="c028c-108">**预缴税金** 科目将被分配一个 **过帐类型** 为预缴税金的主科目。</span><span class="sxs-lookup"><span data-stu-id="c028c-108">**Withholding tax** account will be assigned with a main account with **Posting type** of Withholding tax.</span></span> <span data-ttu-id="c028c-109">**预缴税金冲销** 科目也将被分配一个 **过帐类型** 为“预缴税金冲销”的主科目。</span><span class="sxs-lookup"><span data-stu-id="c028c-109">**Withholding tax offset** account will also be assigned with a main account with **Posting type** "Withholding tax offset".</span></span> <span data-ttu-id="c028c-110">转到 **总帐 > 会计科目表 > 科目 > 主科目**，在主科目的 **过帐验证** 子窗体中设置 **过帐类型**。</span><span class="sxs-lookup"><span data-stu-id="c028c-110">Go to **General ledger > Chart of accounts > Accounts > Main accounts**, set up the **Posting type** in the **Posting validation** sub-form for the main accounts.</span></span>

4. <span data-ttu-id="c028c-111">在 **预缴税金代码** 页上设置预缴税金代码。</span><span class="sxs-lookup"><span data-stu-id="c028c-111">Set up withholding tax codes on the **Withholding tax codes** page.</span></span>

5. <span data-ttu-id="c028c-112">在 **预缴税金组** 页上设置预缴税金组。</span><span class="sxs-lookup"><span data-stu-id="c028c-112">Set up withholding tax groups on the **Withholding tax groups** page.</span></span>

6. <span data-ttu-id="c028c-113">在 **预缴税金** 收入 **类型** 页上设置预缴税金收入类型。</span><span class="sxs-lookup"><span data-stu-id="c028c-113">Set up withholding tax revenue types on the **Withholding tax revenue** **types** page.</span></span>

7. <span data-ttu-id="c028c-114">在 **物料预缴税金组** 页上为物料或服务设置预缴税金组。</span><span class="sxs-lookup"><span data-stu-id="c028c-114">Set up withholding tax groups on the **Item withholding tax groups** page for an item or service.</span></span>

8. <span data-ttu-id="c028c-115">在 **总帐参数 > 预缴税金** 页上设置 **最小发票金额**。</span><span class="sxs-lookup"><span data-stu-id="c028c-115">Set up **Minimum invoice amount** on the **General ledger parameters > Withholding tax** page.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]