---
title: 打印销售税支付（按代码）报表
description: 此主题介绍按记帐币种或销售税代码币种打印销售税支付（按代码）报表所需设置和操作。
author: anasyash
ms.date: 05/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: anasyash
ms.search.validFrom: 2020-04-08
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: eb3ee4a12d2d29c2769f1ae22e11dc05608b47c1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815444"
---
# <a name="print-the-sales-tax-payment-by-code-report"></a><span data-ttu-id="b6e30-103">打印销售税支付（按代码）报表</span><span class="sxs-lookup"><span data-stu-id="b6e30-103">Print the Sales tax payment by code report</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b6e30-104">若要打开 **销售税支付（按代码）报表** 报表，请转到 **税务** \> **查询和报表** \> **销售税报表** \> **销售税支付（按代码）**。</span><span class="sxs-lookup"><span data-stu-id="b6e30-104">To print the **Sales tax payment by code** report, go to **Tax** \> **Inquiries and reports** \> **Sales tax reports** \> **Sales tax payment by code**.</span></span> <span data-ttu-id="b6e30-105">默认情况下，将使用法人的记帐币种为 **销售税报告代码** 页中设置的所有报告代码生成报表金额。</span><span class="sxs-lookup"><span data-stu-id="b6e30-105">By default, report amounts are generated in the accounting currency of the legal entity for all reporting codes that are set up on the **Sales tax reporting codes** page.</span></span>

<span data-ttu-id="b6e30-106">也可以生成此报表，以使其使用销售税代码的币种为分配给 **销售税代码** 页中的销售税代码的所有报告代码的销售税支付金额。</span><span class="sxs-lookup"><span data-stu-id="b6e30-106">You can also generate this report so that it shows the sales tax payment amounts in the currencies of sales tax codes for all reporting codes that are assigned to sales tax codes on the **Sales tax codes** page.</span></span>

## <a name="turn-on-the-feature"></a><span data-ttu-id="b6e30-107">开启功能</span><span class="sxs-lookup"><span data-stu-id="b6e30-107">Turn on the feature</span></span>

<span data-ttu-id="b6e30-108">在 **功能管理** 工作区中，开启以下功能：**以销售税代码货币生成销售税按代码支付报表**。</span><span class="sxs-lookup"><span data-stu-id="b6e30-108">In the **Feature management** workspace, turn on the following feature: **Generate the Sales tax payment by code report in the sales tax code currency**.</span></span>

## <a name="run-the-report"></a><span data-ttu-id="b6e30-109">运行报表</span><span class="sxs-lookup"><span data-stu-id="b6e30-109">Run the report</span></span>

1. <span data-ttu-id="b6e30-110">转到 **计税** \> **查询和报表** \> **销售税报表** \> **销售税支付（按代码）**。</span><span class="sxs-lookup"><span data-stu-id="b6e30-110">Go to **Tax** \> **Inquiries and reports** \> **Sales tax reports** \> **Sales tax payment by code**.</span></span>
2. <span data-ttu-id="b6e30-111">在 **报表币种** 字段中，选择以下值之一：</span><span class="sxs-lookup"><span data-stu-id="b6e30-111">In the **Report currency** field, select one of the following values:</span></span>

    - <span data-ttu-id="b6e30-112">**记帐币种** – 使用记帐币种打印报表金额。</span><span class="sxs-lookup"><span data-stu-id="b6e30-112">**Accounting currency** – Print the report amounts in the accounting currency.</span></span>
    - <span data-ttu-id="b6e30-113">**销售税代码币种** – 使用销售税代码的币种打印报表金额。</span><span class="sxs-lookup"><span data-stu-id="b6e30-113">**Sales tax code currency** – Print the report amounts in the currencies of sales tax codes.</span></span>

    ![“增值税支付（按代码）”对话框](media/Sales-tax-payment-by-code.png)

<span data-ttu-id="b6e30-115">下图显示生成的报表的示例。</span><span class="sxs-lookup"><span data-stu-id="b6e30-115">The following illustration shows an example of the report that is generated.</span></span> <span data-ttu-id="b6e30-116">如果报告代码分配给的销售税代码的 **销售税币种** 字段设置为 **EUR**，则此报表显示报告代码 **101** 的币种为 **EUR**。</span><span class="sxs-lookup"><span data-stu-id="b6e30-116">The report shows that reporting code **101** has the **EUR** currency if the **Sales tax currency** field is set to **EUR** for the sales tax code that the reporting code is assigned to.</span></span>

![销售税支付（按代码）报表的示例](media/Sales-tax-payment-by-code-2.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]