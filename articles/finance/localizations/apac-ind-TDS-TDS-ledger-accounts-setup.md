---
title: 设置 TDS 分类帐帐户
description: 本主题说明如何为从源扣缴税款 (TDS) 设置分类帐帐户功能。
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
ms.openlocfilehash: 93d4cb54488ec0eeee40ca56f3e46f30012f54f5
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023057"
---
# <a name="set-up-tds-ledger-accounts"></a><span data-ttu-id="1a44b-103">设置 TDS 分类帐帐户</span><span class="sxs-lookup"><span data-stu-id="1a44b-103">Set up TDS ledger accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1a44b-104">本主题说明如何为从源扣缴税款 (TDS) 设置分类帐帐户功能。</span><span class="sxs-lookup"><span data-stu-id="1a44b-104">This topic explains how to set up ledger accounts for the Tax Deducted at Source (TDS) feature.</span></span> <span data-ttu-id="1a44b-105">使用 **会计科目表** 页面以为 TDS 设置分类帐帐户。</span><span class="sxs-lookup"><span data-stu-id="1a44b-105">You use the **Chart of accounts** page to set up ledger accounts for TDS.</span></span>

1. <span data-ttu-id="1a44b-106">转到 **总帐 \> 会计科目表 \> 帐户 \> 主帐户**。</span><span class="sxs-lookup"><span data-stu-id="1a44b-106">Go to **General ledger \> Chart of accounts \> Accounts \> Main accounts**.</span></span>
2. <span data-ttu-id="1a44b-107">在 **概述** 选项卡上，选择 **Alt+N** 以创建 TDS 分类帐帐户，然后输入所需的详细信息。</span><span class="sxs-lookup"><span data-stu-id="1a44b-107">On the **Overview** tab, select **Alt+N** to create a TDS ledger account, and enter the required details.</span></span>
3. <span data-ttu-id="1a44b-108">在 **设置** 选项卡的 **过帐类型** 字段中，选择 **预缴税金**。</span><span class="sxs-lookup"><span data-stu-id="1a44b-108">On the **Setup** tab, in the **Posting type** field, select **Withholding tax**.</span></span>     

    > [!NOTE]
    > <span data-ttu-id="1a44b-109">过帐类型为 **预缴税金** 的分类帐帐户仅可以定义为应收帐款，用于过帐 TDS 税码的 TDS 应收金额。</span><span class="sxs-lookup"><span data-stu-id="1a44b-109">Ledger accounts that have a posting type of **Withholding tax** can be defined only as receivable accounts that are used to post the TDS receivable amount for a TDS tax code.</span></span>

4. <span data-ttu-id="1a44b-110">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="1a44b-110">Close the page.</span></span>
