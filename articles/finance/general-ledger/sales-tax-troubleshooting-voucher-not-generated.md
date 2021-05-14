---
title: 未生成凭证
description: 本主题提供可以在凭证应生成但未生成时提供帮助的故障排除信息。
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
ms.openlocfilehash: eafc9110ec58be5083569188d59b67a62e86c85d
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947604"
---
# <a name="voucher-isnt-generated"></a><span data-ttu-id="b057b-103">未生成凭证</span><span class="sxs-lookup"><span data-stu-id="b057b-103">Voucher isn't generated</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b057b-104">如果应生成凭证，但 **凭证交易** 页未显示任何凭证，请根据需要按照以下各节中的步骤解决此问题。</span><span class="sxs-lookup"><span data-stu-id="b057b-104">If a voucher should be generated, but the **Voucher transactions** page doesn't show any vouchers, follow the steps in the following sections as required to troubleshoot this issue.</span></span>

<span data-ttu-id="b057b-105">[![没有凭证的“凭证交易”页](./media/voucher-not-generated-Picture1.png)](./media/voucher-not-generated-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="b057b-105">[![Voucher transactions page that has no vouchers](./media/voucher-not-generated-Picture1.png)](./media/voucher-not-generated-Picture1.png)</span></span>

## <a name="check-the-tax-applicability"></a><span data-ttu-id="b057b-106">检查税适用性</span><span class="sxs-lookup"><span data-stu-id="b057b-106">Check the tax applicability</span></span>

1. <span data-ttu-id="b057b-107">转到 **税** \> **定期任务** \> **未转移的子分类日记帐分录**。</span><span class="sxs-lookup"><span data-stu-id="b057b-107">Go to **Tax** \> **Periodic tasks** \> **Subledger journal entries not yet transferred**.</span></span>
2. <span data-ttu-id="b057b-108">如果有日记帐记录，选择它，然后选择 **立即转移**。</span><span class="sxs-lookup"><span data-stu-id="b057b-108">If there is a journal record, select it, and then select **Transfer now**.</span></span>

    <span data-ttu-id="b057b-109">[![“未转移的子分类日记帐分录”页上的“立即转移”按钮](./media/voucher-not-generated-Picture2.png)](./media/voucher-not-generated-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="b057b-109">[![Transfer now button on the Subledger journal entries not yet transferred page](./media/voucher-not-generated-Picture2.png)](./media/voucher-not-generated-Picture2.png)</span></span>

3. <span data-ttu-id="b057b-110">再次打开 **凭证交易** 页，查看是否生成了凭证。</span><span class="sxs-lookup"><span data-stu-id="b057b-110">Open the **Voucher transactions** page again to see whether the voucher was generated.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="b057b-111">确定是否存在自定义</span><span class="sxs-lookup"><span data-stu-id="b057b-111">Determine whether customization exists</span></span>

<span data-ttu-id="b057b-112">如果您已经完成了上一节中的步骤，但未发现问题，请确定是否存在自定义。</span><span class="sxs-lookup"><span data-stu-id="b057b-112">If you've completed the steps in the previous section but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="b057b-113">如果不存在自定义，请创建 Microsoft 服务请求寻求进一步支持。</span><span class="sxs-lookup"><span data-stu-id="b057b-113">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
