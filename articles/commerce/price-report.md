---
title: 零售价报表
description: 此主题提供可以用于查看分类产品的近期价格变更的价格报表功能的概览。
author: shajain
manager: AnnBe
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: josaw
ms.custom: 16181
ms.assetid: b1b57734-1406-4ed6-8e28-21c705ee17e2
ms.search.region: global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2019-01-18
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: f317b22f2794dc71093068a51c8e9d4e6d7d55ac
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5231144"
---
# <a name="retail-price-reports"></a><span data-ttu-id="fcc85-103">零售价报表</span><span class="sxs-lookup"><span data-stu-id="fcc85-103">Retail price reports</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="fcc85-104">为向客户提供有竞争力的价格，零售商通常会更改产品的价格。</span><span class="sxs-lookup"><span data-stu-id="fcc85-104">In order to provide competitive prices to their customers, retailers often change prices of products.</span></span> <span data-ttu-id="fcc85-105">店长希望能够轻松访问最近或未来的价格变更，以便他们可以计划所需资源来更新显示在商店货位上的价格标签。</span><span class="sxs-lookup"><span data-stu-id="fcc85-105">Store managers want the ability to easily access recent or upcoming price changes so that they can plan for the required resources to update the price labels displayed on the store shelves.</span></span> <span data-ttu-id="fcc85-106">使用 Retail 的版本 10.0，店长可以通过导航到 **所有商店 \> 商店 \> 价格报表** 并查看与商店关联的产品的更新价格来打开 **价格** 报表。</span><span class="sxs-lookup"><span data-stu-id="fcc85-106">With release 10.0 of Retail, a store manager can open the **Price** report by navigating to **All stores \> Store \> Price report** and viewing the updated prices for the products associated to the store.</span></span> 

<span data-ttu-id="fcc85-107">若要启用价格报表，必须打开 **启用商店的价格报表** 参数。</span><span class="sxs-lookup"><span data-stu-id="fcc85-107">To enable the price report, the **Enable price report for store** parameter must be turned on.</span></span> <span data-ttu-id="fcc85-108">此参数位于 **商业参数 \> 折扣 \> 杂项** 选项卡中。打开 **价格报表** 页将显示具有不同配置的对话框。</span><span class="sxs-lookup"><span data-stu-id="fcc85-108">This parameter is located on the **Commerce parameters \> Discounts \> Miscellaneous** tab. Opening the **Price report** page displays a dialog box with various configurations.</span></span> <span data-ttu-id="fcc85-109">可用配置在下面列出。</span><span class="sxs-lookup"><span data-stu-id="fcc85-109">The available configurations are listed below.</span></span>

| <span data-ttu-id="fcc85-110">配置</span><span class="sxs-lookup"><span data-stu-id="fcc85-110">Configuration</span></span> | <span data-ttu-id="fcc85-111">说明</span><span class="sxs-lookup"><span data-stu-id="fcc85-111">Description</span></span> |
|---|---|
| <span data-ttu-id="fcc85-112">开始日期/结束日期</span><span class="sxs-lookup"><span data-stu-id="fcc85-112">From date / To date</span></span>| <span data-ttu-id="fcc85-113">应该生成价格报表的日期范围。</span><span class="sxs-lookup"><span data-stu-id="fcc85-113">The date range for which the price report should be generated.</span></span> <span data-ttu-id="fcc85-114">持续时间当前限定为 7 天。</span><span class="sxs-lookup"><span data-stu-id="fcc85-114">The duration is currently limited to 7 days.</span></span> |
| <span data-ttu-id="fcc85-115">通道</span><span class="sxs-lookup"><span data-stu-id="fcc85-115">Channel</span></span>| <span data-ttu-id="fcc85-116">应该生成价格报表的商店。</span><span class="sxs-lookup"><span data-stu-id="fcc85-116">The store for which the price report should be generated.</span></span> |
| <span data-ttu-id="fcc85-117">显示具有可用库存的产品</span><span class="sxs-lookup"><span data-stu-id="fcc85-117">Display products with available inventory</span></span>| <span data-ttu-id="fcc85-118">将此项设置为 **是** 将只显示当前在商店中有可用的实际库存的那些产品的价格。</span><span class="sxs-lookup"><span data-stu-id="fcc85-118">Setting this to **Yes** will show the prices for only those products which currently have physical inventory available in the store.</span></span> |
| <span data-ttu-id="fcc85-119">显示变型的价格</span><span class="sxs-lookup"><span data-stu-id="fcc85-119">Display prices for variants</span></span> | <span data-ttu-id="fcc85-120">将此项设置为 **是** 将显示变型以及基础产品的价格。</span><span class="sxs-lookup"><span data-stu-id="fcc85-120">Setting this to **Yes** will display the prices of the variants along with the product masters.</span></span> <span data-ttu-id="fcc85-121">这应该仅在您有变型特定价格时再 **打开**，因为行数将变得非常大。</span><span class="sxs-lookup"><span data-stu-id="fcc85-121">This should only be turned **On** if you have variant-specific prices, because the number of rows grows very large.</span></span> <span data-ttu-id="fcc85-122">在将来的版本中，我们将启用基于维度的价格，以便店长可以选择应显示其价格的维度。</span><span class="sxs-lookup"><span data-stu-id="fcc85-122">In future releases, we will enable the dimensions-based prices so that the store manager can choose the dimensions for which the prices should be displayed.</span></span> |
| <span data-ttu-id="fcc85-123">显示具有价格更改的产品</span><span class="sxs-lookup"><span data-stu-id="fcc85-123">Display products with price changes</span></span> | <span data-ttu-id="fcc85-124">将此项设置为 **是** 将仅显示价格已更改的那些日期的价格。</span><span class="sxs-lookup"><span data-stu-id="fcc85-124">Setting this to **Yes** will display the prices for only those dates on which the price has been changed.</span></span> <span data-ttu-id="fcc85-125">**开始日期** 的 *前一天* 的价格将始终显示，以便店长可以轻松识别在整个所选持续时间内未更改价格的产品，并可以查看当前价格。</span><span class="sxs-lookup"><span data-stu-id="fcc85-125">The price for *one day before* the selected **From date** will always be displayed, so that the store manager can easily identity the products which have not changed prices for the entire selected duration, and can also view the current price.</span></span> |

<span data-ttu-id="fcc85-126">生成报表后，Excel 文件可以根据任何其他筛选需要下载。</span><span class="sxs-lookup"><span data-stu-id="fcc85-126">After the report is generated, the Excel file can be downloaded for any additional filtering needs.</span></span> <span data-ttu-id="fcc85-127">价格报表还可以用于检查过去日期的产品的历史价格。</span><span class="sxs-lookup"><span data-stu-id="fcc85-127">The price report can also be used to check the historical prices of products for past dates.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]