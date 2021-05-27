---
title: 为供应商和客户设置 TDS 组、PAN 和 TAN 信息
description: 本主题说明如何为供应商和客户设置有关从源扣缴税款 (TDS) 组、永久帐号 (PAN) 和税务帐号 (TAN) 的信息。
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
ms.openlocfilehash: fd33b1775afefed798f1e9bb7601f4112222c430
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023059"
---
# <a name="tds-group-pan-and-tan-information-setup-for-vendors-and-customers"></a><span data-ttu-id="dc7e3-103">为供应商和客户设置的 TDS 组、PAN 和 TAN 信息</span><span class="sxs-lookup"><span data-stu-id="dc7e3-103">TDS group, PAN, and TAN information setup for vendors and customers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dc7e3-104">本主题说明如何为供应商和客户设置有关从源扣缴税款 (TDS) 组、永久帐号 (PAN) 和税务帐号 (TAN) 的信息。</span><span class="sxs-lookup"><span data-stu-id="dc7e3-104">This topic explains how to set up information about the Tax Deducted at Source (TDS) group, permanent account number (PAN), and tax account number (TAN) for vendors and customers.</span></span>

1. <span data-ttu-id="dc7e3-105">转到 **应付帐款 \> 供应商 \> 所有供应商** 或 **应收帐款 \> 客户 \> 所有客户**。</span><span class="sxs-lookup"><span data-stu-id="dc7e3-105">Go to **Accounts payable \> Vendors \> All vendors** or **Accounts receivable \> Customers \> All customers**.</span></span>

    <span data-ttu-id="dc7e3-106">[![所有供应商页面](./media/apac-ind-TDS-55.png)](./media/apac-ind-TDS-55.png)</span><span class="sxs-lookup"><span data-stu-id="dc7e3-106">[![All vendors page](./media/apac-ind-TDS-55.png)](./media/apac-ind-TDS-55.png)</span></span>

2. <span data-ttu-id="dc7e3-107">在操作窗格上，选择 **新建** 以创建供应商或客户，然后输入所需的详细信息。</span><span class="sxs-lookup"><span data-stu-id="dc7e3-107">On the Action Pane, select **New** to create a vendor or customer, and enter the required details.</span></span> <span data-ttu-id="dc7e3-108">或者，选择一个现有供应商或客户。</span><span class="sxs-lookup"><span data-stu-id="dc7e3-108">Alternatively, select an existing vendor or customer.</span></span>
3. <span data-ttu-id="dc7e3-109">在 **发票和交货** 快速选项卡的 **预缴税金** 部分中，将 **计算预缴税金** 选项设置为 **是** 以为供应商或客户计算预缴税金、TDS 或从源征收税款 (TCS)。</span><span class="sxs-lookup"><span data-stu-id="dc7e3-109">On the **Invoice and delivery** FastTab, in the **Withholding tax** section, set the **Calculate withholding tax** option to **Yes** to calculate withholding tax, TDS, or Tax Collected at Source (TCS) for the vendor or customer.</span></span>
4. <span data-ttu-id="dc7e3-110">基于为供应商或客户定义的默认 TDS 组计算采购发票的 TDS。</span><span class="sxs-lookup"><span data-stu-id="dc7e3-110">TDS for a purchase invoice is calculated based on the default TDS group that is defined for the vendor or customer.</span></span> <span data-ttu-id="dc7e3-111">在 **TDS 组** 字段中，选择默认的 TDS 组。</span><span class="sxs-lookup"><span data-stu-id="dc7e3-111">In the **TDS group** field, select the default TDS group.</span></span>

    > [!NOTE]
    > <span data-ttu-id="dc7e3-112">当在 **TDS 组** 字段中选择 TDS 组时，**预缴税金组** 和 **TCS 组** 字段变得不可用。</span><span class="sxs-lookup"><span data-stu-id="dc7e3-112">When you select a TDS group in the **TDS group** field, the **Withholding tax group** and **TCS group** fields become unavailable.</span></span>

5. <span data-ttu-id="dc7e3-113">在 **税务信息** 快速选项卡上，在 **PAN 信息** 部分的 **状态** 字段中，为供应商或客户选择永久帐号的状态。</span><span class="sxs-lookup"><span data-stu-id="dc7e3-113">On the **Tax information** FastTab, in the **PAN information** section, in the **Status** field, select the status of the permanent account number for the vendor or customer:</span></span>

    - <span data-ttu-id="dc7e3-114">**不可用** – 供应商或客户没有 PAN。</span><span class="sxs-lookup"><span data-stu-id="dc7e3-114">**Not available** – The vendor or customer doesn't have a PAN.</span></span>
    - <span data-ttu-id="dc7e3-115">**已收到** – 供应商或客户具有 PAN。</span><span class="sxs-lookup"><span data-stu-id="dc7e3-115">**Received** – The vendor or customer has a PAN.</span></span>
    - <span data-ttu-id="dc7e3-116">**已应用** – 供应商或客户已应用 PAN。</span><span class="sxs-lookup"><span data-stu-id="dc7e3-116">**Applied** – The vendor or customer has applied for a PAN.</span></span>
    - <span data-ttu-id="dc7e3-117">**无效** – 供应商或客户具有 PAN，但无效。</span><span class="sxs-lookup"><span data-stu-id="dc7e3-117">**Invalid** – The vendor or customer has a PAN, but it isn't valid.</span></span>

6. <span data-ttu-id="dc7e3-118">如果在 **状态** 字段中选择了 **已收到** 来指示供应商或客户具有 PAN，则在 **编号** 字段中输入 PAN。</span><span class="sxs-lookup"><span data-stu-id="dc7e3-118">If you selected **Received** in the **Status** field to indicate that the vendor or customer has a PAN, enter the PAN in the **Number** field.</span></span> <span data-ttu-id="dc7e3-119">PAN 必须包含五个字母字符、四个数字字符和一个字母字符。</span><span class="sxs-lookup"><span data-stu-id="dc7e3-119">The PAN must consist of five alphabetic characters, then four numeric characters, and then one alphabetic character.</span></span> <span data-ttu-id="dc7e3-120">下面是一个示例：**ABCDE1260A**。</span><span class="sxs-lookup"><span data-stu-id="dc7e3-120">Here is an example: **ABCDE1260A**.</span></span>
7. <span data-ttu-id="dc7e3-121">如果在 **状态** 字段中选择了 **已应用** 来指示供应商或客户已应用 PAN，则在 **参考编号** 字段中输入参考编号。</span><span class="sxs-lookup"><span data-stu-id="dc7e3-121">If you selected **Applied** in the **Status** field to indicate that the vendor or customer has applied for PAN, enter the reference number in the **Reference number** field.</span></span>
8. <span data-ttu-id="dc7e3-122">在 **评估对象的性质** 字段中，选择供应商或客户所属的评估对象类别的性质：</span><span class="sxs-lookup"><span data-stu-id="dc7e3-122">In the **Nature of assessee** field, select the nature of assessee category that the vendor or customer belongs to:</span></span>

    - <span data-ttu-id="dc7e3-123">公司</span><span class="sxs-lookup"><span data-stu-id="dc7e3-123">Company</span></span>
    - <span data-ttu-id="dc7e3-124">HUF</span><span class="sxs-lookup"><span data-stu-id="dc7e3-124">HUF</span></span>
    - <span data-ttu-id="dc7e3-125">确认</span><span class="sxs-lookup"><span data-stu-id="dc7e3-125">Firm</span></span>
    - <span data-ttu-id="dc7e3-126">个人</span><span class="sxs-lookup"><span data-stu-id="dc7e3-126">Individual</span></span>
    - <span data-ttu-id="dc7e3-127">AOP</span><span class="sxs-lookup"><span data-stu-id="dc7e3-127">AOP</span></span>
    - <span data-ttu-id="dc7e3-128">BOI</span><span class="sxs-lookup"><span data-stu-id="dc7e3-128">BOI</span></span>
    - <span data-ttu-id="dc7e3-129">本地主管机构</span><span class="sxs-lookup"><span data-stu-id="dc7e3-129">Local authority</span></span>
    - <span data-ttu-id="dc7e3-130">其他</span><span class="sxs-lookup"><span data-stu-id="dc7e3-130">Others</span></span>

    <span data-ttu-id="dc7e3-131">[![税务信息快速选项卡](./media/apac-ind-TDS-56.png)](./media/apac-ind-TDS-56.png)</span><span class="sxs-lookup"><span data-stu-id="dc7e3-131">[![Tax information FastTab](./media/apac-ind-TDS-56.png)](./media/apac-ind-TDS-56.png)</span></span>

9. <span data-ttu-id="dc7e3-132">在操作窗格上的 **供应商** 选项卡上，在 **登记** 组中，选择 **登记 ID** 以打开 **管理地址** 页面。</span><span class="sxs-lookup"><span data-stu-id="dc7e3-132">On the Action Pane, on the **Vendor** tab, in the **Registration** group, select **Registration IDs** to open the **Manage addresses** page.</span></span>
10. <span data-ttu-id="dc7e3-133">在 **管理地址** 页面的 **税务信息** 快速选项卡上，选择 **添加** 或 **编辑** 以打开 **管理税务信息** 页面，您可以在该页面中维护税务登记条目。</span><span class="sxs-lookup"><span data-stu-id="dc7e3-133">On the **Manage addresses** page, on the **Tax information** FastTab, select **Add** or **Edit** to open the **Manage tax information** page, where you can maintain the tax registration entry.</span></span>
11. <span data-ttu-id="dc7e3-134">在 **管理税务信息** 页面的 **预缴税金** 快速选项卡上，在 **税务帐号 (TAN)** 字段中，输入 TAN。</span><span class="sxs-lookup"><span data-stu-id="dc7e3-134">On the **Manage tax information** page, on the **Withholding tax** FastTab, in the **Tax Account Number (TAN)** field, enter the TAN.</span></span> <span data-ttu-id="dc7e3-135">TAN 必须包含四个字母字符、五个数字字符和一个字母字符。</span><span class="sxs-lookup"><span data-stu-id="dc7e3-135">The TAN must consist of four alphabetic characters, then five numeric characters, and then one alphabetic character.</span></span> <span data-ttu-id="dc7e3-136">下面是一个示例：**AFGH54821T**。</span><span class="sxs-lookup"><span data-stu-id="dc7e3-136">Here is an example: **AFGH54821T**.</span></span>
12. <span data-ttu-id="dc7e3-137">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="dc7e3-137">Close the page.</span></span>
