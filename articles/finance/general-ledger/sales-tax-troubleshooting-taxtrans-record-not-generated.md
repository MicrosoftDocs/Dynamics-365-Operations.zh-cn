---
title: 未生成 TaxTrans 记录
description: 本主题提供可以在未生成 TaxTrans 记录时提供帮助的故障排除信息。
author: qire
manager: beya
ms.date: 04/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 0c7414cc39198ff4d5be9b4c41ca62f9c78c9250
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947601"
---
# <a name="taxtrans-record-isnt-generated"></a><span data-ttu-id="54ba9-103">未生成 TaxTrans 记录</span><span class="sxs-lookup"><span data-stu-id="54ba9-103">TaxTrans record isn't generated</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="54ba9-104">如果您为交易选择 **已过帐销售税**，但是 **已过帐销售税** 页上未显示税务行或缺少税务行，有可能是未生成 **TaxTrans** 记录。</span><span class="sxs-lookup"><span data-stu-id="54ba9-104">If you select **Posted sales tax** for a transaction, but the **Posted sales tax** page either shows no tax lines or is missing a tax line, the **TaxTrans** record might not have been generated.</span></span>

<span data-ttu-id="54ba9-105">[![没有行项的“已过帐销售税”页](./media/taxtrans-is-not-generated-Picture1.png)](./media/taxtrans-is-not-generated-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="54ba9-105">[![Posted sales tax page that has no line items](./media/taxtrans-is-not-generated-Picture1.png)](./media/taxtrans-is-not-generated-Picture1.png)</span></span>

<span data-ttu-id="54ba9-106">要解决此问题，请根据需要按照以下各节中的步骤操作。</span><span class="sxs-lookup"><span data-stu-id="54ba9-106">To troubleshoot this issue, follow the steps in the following sections as required.</span></span>

## <a name="check-the-sales-tax-before-you-post-the-transaction"></a><span data-ttu-id="54ba9-107">过帐交易前检查销售税</span><span class="sxs-lookup"><span data-stu-id="54ba9-107">Check the sales tax before you post the transaction</span></span>

1. <span data-ttu-id="54ba9-108">在过帐交易之前，在 **过帐发票** 页上，选择 **销售税** 检查计算。</span><span class="sxs-lookup"><span data-stu-id="54ba9-108">Before you post the transaction, on the **Posting invoice** page, select **Sales tax** to check the calculation.</span></span>

    <span data-ttu-id="54ba9-109">[![“过帐发票”页上的“销售税”按钮](./media/taxtrans-is-not-generated-Picture2.png)](./media/taxtrans-is-not-generated-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="54ba9-109">[![Sales tax button on the Posting invoice page](./media/taxtrans-is-not-generated-Picture2.png)](./media/taxtrans-is-not-generated-Picture2.png)</span></span>

2. <span data-ttu-id="54ba9-110">在 **临时销售税交易** 页上，查看计算结果。</span><span class="sxs-lookup"><span data-stu-id="54ba9-110">On the **Temporary sales tax transactions** page, review the result of the calculation.</span></span> <span data-ttu-id="54ba9-111">如果未计算税款，请参阅[未计算税款或税额为零](sales-tax-troubleshooting-tax-not-calculated-amount-zero.md)。</span><span class="sxs-lookup"><span data-stu-id="54ba9-111">If no tax is calculated, see [Tax isn't calculated or the tax amount is zero](sales-tax-troubleshooting-tax-not-calculated-amount-zero.md).</span></span>

## <a name="find-the-taxtrans-record-in-all-posted-sales-tax"></a><span data-ttu-id="54ba9-112">在所有过帐的销售税中查找 TaxTrans 记录</span><span class="sxs-lookup"><span data-stu-id="54ba9-112">Find the TaxTrans record in all posted sales tax</span></span>

1. <span data-ttu-id="54ba9-113">转到 **税** \> **查询和申报** \> **销售税查询** > **已过帐销售税**。</span><span class="sxs-lookup"><span data-stu-id="54ba9-113">Go to **Tax** \> **Inquiries and reports** \> **Sales tax inquiries** > **Posted sales tax**.</span></span>
2. <span data-ttu-id="54ba9-114">在 **凭证** 列标题中，选择筛选符号查找 **TaxTrans** 记录。</span><span class="sxs-lookup"><span data-stu-id="54ba9-114">In the **Voucher** column heading, select the filter symbol to find the **TaxTrans** record.</span></span>
3. <span data-ttu-id="54ba9-115">如果找到了所需的销售税记录，请检查日期。</span><span class="sxs-lookup"><span data-stu-id="54ba9-115">If you find the sales tax records that you're looking for, check the date.</span></span> <span data-ttu-id="54ba9-116">如果日期不同于日记帐标头的日期，请创建 Microsoft 服务请求寻求其他支持。</span><span class="sxs-lookup"><span data-stu-id="54ba9-116">If the date differs from the date of the journal header, create a Microsoft service request for additional support.</span></span>

    <span data-ttu-id="54ba9-117">[![已过帐的销售税页面](./media/taxtrans-is-not-generated-Picture4.png)](./media/taxtrans-is-not-generated-Picture4.png)</span><span class="sxs-lookup"><span data-stu-id="54ba9-117">[![Posted sales tax page](./media/taxtrans-is-not-generated-Picture4.png)](./media/taxtrans-is-not-generated-Picture4.png)</span></span>

## <a name="debug-to-check-details"></a><span data-ttu-id="54ba9-118">调试以检查详细信息</span><span class="sxs-lookup"><span data-stu-id="54ba9-118">Debug to check details</span></span>

1. <span data-ttu-id="54ba9-119">有关如何调试和确定是否正确生成了 **TmpTaxWorkTrans** 和 **TaxUncommitted** 的信息，请参阅 [TaxTrans 中的字段值不正确](sales-tax-troubleshooting-field-value-taxtrans-incorrect.md)。</span><span class="sxs-lookup"><span data-stu-id="54ba9-119">For information about how to debug and determine whether **TmpTaxWorkTrans** and **TaxUncommitted** are correctly generated, see [Field value in TaxTrans is incorrect](sales-tax-troubleshooting-field-value-taxtrans-incorrect.md).</span></span>
2. <span data-ttu-id="54ba9-120">如果正确生成了 **TaxTmpWorkTrans** 或 **TaxUncommitted**，在 **TaxPost::SaveAndPost()** 和 **Tax::SaveAndPost** 处添加中断点来调试未插入 **TaxTrans** 的原因。</span><span class="sxs-lookup"><span data-stu-id="54ba9-120">If **TaxTmpWorkTrans** or **TaxUncommitted** is correctly generated, add a breakpoint at **TaxPost::SaveAndPost()** and **Tax::SaveAndPost** to debug the reason why **TaxTrans** isn't inserted.</span></span>

    <span data-ttu-id="54ba9-121">[![在代码中添加的中断点](./media/taxtrans-is-not-generated-Picture5.png)](./media/taxtrans-is-not-generated-Picture5.png)</span><span class="sxs-lookup"><span data-stu-id="54ba9-121">[![Breakpoints added in code](./media/taxtrans-is-not-generated-Picture5.png)](./media/taxtrans-is-not-generated-Picture5.png)</span></span>

    <span data-ttu-id="54ba9-122">[![添加的中断点的结果](./media/taxtrans-is-not-generated-Picture6.png)](./media/taxtrans-is-not-generated-Picture6.png)</span><span class="sxs-lookup"><span data-stu-id="54ba9-122">[![Results of added breakpoints](./media/taxtrans-is-not-generated-Picture6.png)](./media/taxtrans-is-not-generated-Picture6.png)</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="54ba9-123">确定是否存在自定义</span><span class="sxs-lookup"><span data-stu-id="54ba9-123">Determine whether customization exists</span></span>

<span data-ttu-id="54ba9-124">如果您已经完成了前面几节中的步骤，但未发现问题，请确定是否存在自定义。</span><span class="sxs-lookup"><span data-stu-id="54ba9-124">If you've completed the steps in the previous sections but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="54ba9-125">如果不存在自定义，请创建 Microsoft 服务请求寻求进一步支持。</span><span class="sxs-lookup"><span data-stu-id="54ba9-125">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
