---
title: 全球预缴税金
description: 本主题提供有关全球预缴税金功能及其设置方法的信息。 全球预缴税金功能针对供应商和客户交易进行了增强，让预缴税金在物料级别计算。
author: roschlom
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: 9a73d34fb4fbf007cbb5a996cfa6e9719532869c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826658"
---
# <a name="global-withholding-tax"></a><span data-ttu-id="3e26b-104">全球预缴税金</span><span class="sxs-lookup"><span data-stu-id="3e26b-104">Global withholding tax</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3e26b-105">本主题提供有关全球预缴税金功能，并说明了设置方法。</span><span class="sxs-lookup"><span data-stu-id="3e26b-105">This topic provides information about global withholding tax functionality and explains how to set it up.</span></span> <span data-ttu-id="3e26b-106">版本 10.0.17 及更高版本中提供此新功能。</span><span class="sxs-lookup"><span data-stu-id="3e26b-106">The new functionality is available in version 10.0.17 and later.</span></span>

<span data-ttu-id="3e26b-107">全球预缴税金功能针对供应商和客户交易进行了增强，让预缴税金在物料级别计算。</span><span class="sxs-lookup"><span data-stu-id="3e26b-107">Global withholding tax functionality is enhanced for vendor and customer transactions, so that withholding tax is calculated at the item level.</span></span> <span data-ttu-id="3e26b-108">购买交易中预缴税金帐户中的余额可以通过对预缴税金结算帐户运行预缴税金支付作业来结算。</span><span class="sxs-lookup"><span data-stu-id="3e26b-108">The balance in the withholding tax account from purchase transactions can be settled by running the withholding tax payment job against the withholding tax settlement account.</span></span>

> [!NOTE]
> <span data-ttu-id="3e26b-109">全球预缴税金在采购订单、供应商发票和销售订单页上不支持 **维护费用** 功能。</span><span class="sxs-lookup"><span data-stu-id="3e26b-109">Global withholding tax doesn't support the **Maintain charges** function on the purchase order, vendor invoice, and sales order pages.</span></span>

## <a name="turn-on-global-withholding-tax"></a><span data-ttu-id="3e26b-110">打开全球预缴税金</span><span class="sxs-lookup"><span data-stu-id="3e26b-110">Turn on global withholding tax</span></span>

1. <span data-ttu-id="3e26b-111">在 **功能管理** 工作区，选择 **全球预缴税金**，然后选择 **立即启用**。</span><span class="sxs-lookup"><span data-stu-id="3e26b-111">In the **Feature management** workspace, select **Global withholding tax**, and then select **Enable now**.</span></span>
2. <span data-ttu-id="3e26b-112">转到 **税 \> 设置 \> 参数 \> 总帐参数**，然后在 **预缴税金** 选项卡上，将 **启用全球预缴税金** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="3e26b-112">Go to **Tax \> Setup \> Parameters \> General ledger parameters**, and then, on the **Withholding tax** tab, set the **Enable global withholding tax** option to **Yes**.</span></span>
3. <span data-ttu-id="3e26b-113">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="3e26b-113">Select **Save**.</span></span>
4. <span data-ttu-id="3e26b-114">在 Web 浏览器中刷新页面。</span><span class="sxs-lookup"><span data-stu-id="3e26b-114">Refresh the page in your web browser.</span></span>

> [!NOTE]
> <span data-ttu-id="3e26b-115">对于已经存在本地化的预缴税金解决方案的国家/地区，无法启用全球预缴税金功能。</span><span class="sxs-lookup"><span data-stu-id="3e26b-115">Global withholding tax functionality can’t be turned on for countries/regions where localized withholding tax solutions already exist.</span></span> <span data-ttu-id="3e26b-116">这些区域包括但不限于印度、巴西、泰国、沙特阿拉伯、爱尔兰、英国和美国。</span><span class="sxs-lookup"><span data-stu-id="3e26b-116">These areas include but are not restricted to India, Brazil, Thailand, Saudi Arabia, Ireland, Great Britain and the United States.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]