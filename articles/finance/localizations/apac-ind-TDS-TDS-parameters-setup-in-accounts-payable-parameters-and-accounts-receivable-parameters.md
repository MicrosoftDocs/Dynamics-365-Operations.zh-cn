---
title: 在应付帐款和应收帐款中设置 TDS 参数
description: 本主题说明如何在应付帐款和应收帐款中设置参数以支持从源扣缴税款 (TDS) 扣除。
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
ms.openlocfilehash: 4540cdfff2362d8fb7cc2b4cccf9c340be9750ce
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023058"
---
# <a name="set-tds-parameters-in-accounts-payable-and-accounts-receivable"></a><span data-ttu-id="60f7d-103">在应付帐款和应收帐款中设置 TDS 参数</span><span class="sxs-lookup"><span data-stu-id="60f7d-103">Set TDS parameters in Accounts payable and Accounts receivable</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="60f7d-104">本主题说明如何在应付帐款和应收帐款中设置参数以支持从源扣缴税款 (TDS) 扣除。</span><span class="sxs-lookup"><span data-stu-id="60f7d-104">This topic explains how to set parameters in Accounts payable and Accounts receivable to support Tax Deducted at Source (TDS) deductions.</span></span>

1. <span data-ttu-id="60f7d-105">转到 **税务 \> 设置 \> 参数 \> 应收帐款参数**。</span><span class="sxs-lookup"><span data-stu-id="60f7d-105">Go to **Tax \> Setup \> Parameters \> Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="60f7d-106">在 **更新** 选项卡上，选择 **更新订单行** 以打开 **更新订单行** 对话框。</span><span class="sxs-lookup"><span data-stu-id="60f7d-106">On the **Updates** tab, select **Update order lines** to open the **Update order lines** dialog box.</span></span>
3. <span data-ttu-id="60f7d-107">在 **TDS 组** 部分的 **更新 TDS 组** 字段中，指定用于在行级别更新 TDS 组的方法。</span><span class="sxs-lookup"><span data-stu-id="60f7d-107">In the **TDS group** section, in the **Updating TDS group** field, specify the method to use to update the TDS group at the line level.</span></span> <span data-ttu-id="60f7d-108">在订单头上更新 TDS 组时，将使用此设置。</span><span class="sxs-lookup"><span data-stu-id="60f7d-108">This setting is used when the TDS group is updated on an order header.</span></span> <span data-ttu-id="60f7d-109">选项如下：</span><span class="sxs-lookup"><span data-stu-id="60f7d-109">The following options are available:</span></span>

    - <span data-ttu-id="60f7d-110">**从不** – 当在订单头上更新 TDS 组时，不在订单行上更新它。</span><span class="sxs-lookup"><span data-stu-id="60f7d-110">**Never** – The TDS group isn't updated on the order lines when it's updated on the order header.</span></span>
    - <span data-ttu-id="60f7d-111">**始终** – 当在订单头上更新 TDS 组时，将在订单行上自动更新它。</span><span class="sxs-lookup"><span data-stu-id="60f7d-111">**Always** – The TDS group is automatically updated on the order lines when it's updated on the order header.</span></span>
    - <span data-ttu-id="60f7d-112">**提示** – 用户收到一条消息，提示他们在订单行上更新 TDS 组。</span><span class="sxs-lookup"><span data-stu-id="60f7d-112">**Prompt** – Users receive a message that prompts them to update the TDS group on the order lines.</span></span>
4. <span data-ttu-id="60f7d-113">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="60f7d-113">Select **OK**.</span></span>

    <span data-ttu-id="60f7d-114">[![更新订单行对话框](./media/apac-ind-TDS-26.PNG)](./media/apac-ind-TDS-26.PNG)</span><span class="sxs-lookup"><span data-stu-id="60f7d-114">[![Update order lines dialog box](./media/apac-ind-TDS-26.PNG)](./media/apac-ind-TDS-26.PNG)</span></span>

5. <span data-ttu-id="60f7d-115">转到 **税务 \> 设置 \> 参数 \> 应付帐款参数**。</span><span class="sxs-lookup"><span data-stu-id="60f7d-115">Go to **Tax \> Setup \> Parameters \> Accounts payable parameters**.</span></span>
6. <span data-ttu-id="60f7d-116">在 **常规** 选项卡的 **基于交货信息拆分** 快速选项卡上，将 **产品收据** 设置为 **是**，以过帐和拆分具有不同交货地址和税务帐号 (TAN) 的产品收据。</span><span class="sxs-lookup"><span data-stu-id="60f7d-116">On the **General** tab, on the **Split based on delivery information** FastTab, set the **Product receipt** option to **Yes** to post and split a product receipt that has different delivery addresses and tax account numbers (TANs).</span></span> <span data-ttu-id="60f7d-117">如果此选项设置为 **否**，则不能过帐具有不同交货地址和 TAN 的采购装箱单。</span><span class="sxs-lookup"><span data-stu-id="60f7d-117">If this option is set to **No**, you can't post a purchase packing slip that has different delivery addresses and TANs.</span></span>
7. <span data-ttu-id="60f7d-118">将 **发票** 选项设置为 **是**，以过帐和拆分具有不同交货地址和 TAN 的采购发票。</span><span class="sxs-lookup"><span data-stu-id="60f7d-118">Set the **Invoice** option to **Yes** to post and split a purchase invoice that has different delivery addresses and TANs.</span></span>

    <span data-ttu-id="60f7d-119">[![基于交货信息拆分快速选项卡](./media/apac-ind-TDS-25.png)](./media/apac-ind-TDS-25.png)</span><span class="sxs-lookup"><span data-stu-id="60f7d-119">[![Split based on delivery information FastTab](./media/apac-ind-TDS-25.png)](./media/apac-ind-TDS-25.png)</span></span>

8. <span data-ttu-id="60f7d-120">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="60f7d-120">Close the page.</span></span>
