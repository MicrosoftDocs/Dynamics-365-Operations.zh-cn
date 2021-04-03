---
title: 复制环境后缺少产品和类别
description: 本主题提供故障排除指南，在环境之间或同一环境中复制站点后缺少产品和类别时，本指南可以提供帮助。
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 35f2cbd98a91149395f40bf821c1d5d7e58eaf77
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585221"
---
# <a name="products-and-categories-missing-after-environment-copy"></a><span data-ttu-id="51e7d-103">复制环境后缺少产品和类别</span><span class="sxs-lookup"><span data-stu-id="51e7d-103">Products and categories missing after environment copy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="51e7d-104">本主题提供故障排除指南，在环境之间或同一环境中复制站点后缺少产品和类别时，本指南可以提供帮助。</span><span class="sxs-lookup"><span data-stu-id="51e7d-104">This topic provides troubleshooting guidance that can help when products and categories are missing after a site is copied between environments or within the same environment.</span></span>

## <a name="description"></a><span data-ttu-id="51e7d-105">说明</span><span class="sxs-lookup"><span data-stu-id="51e7d-105">Description</span></span>

<span data-ttu-id="51e7d-106">将站点从一个环境复制到另一环境或在同一环境中复制后，该站点缺少产品和类别。</span><span class="sxs-lookup"><span data-stu-id="51e7d-106">After a site is copied from one environment to another, or within the same environment, the products and categories are missing from the site.</span></span> <span data-ttu-id="51e7d-107">电子商务店面和 Commerce 站点构建器中的 **产品** 选项卡缺少产品和类别。</span><span class="sxs-lookup"><span data-stu-id="51e7d-107">The products and categories will be missing from the e-commerce storefront and from the **Products** tab in Commerce site builder.</span></span>

## <a name="resolution"></a><span data-ttu-id="51e7d-108">解决方法</span><span class="sxs-lookup"><span data-stu-id="51e7d-108">Resolution</span></span>

### <a name="map-the-channel-operating-unit-number-to-a-newly-copied-site-in-commerce-site-builder"></a><span data-ttu-id="51e7d-109">将渠道运营单位编号映射到 Commerce 站点构建器中新复制的站点</span><span class="sxs-lookup"><span data-stu-id="51e7d-109">Map the channel operating unit number to a newly copied site in Commerce site builder</span></span>

<span data-ttu-id="51e7d-110">要将渠道运营单位编号 (OUN) 映射到 Commerce 站点构建器中新复制的站点，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="51e7d-110">To map the channel operating unit number (OUN) to a newly copied site in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="51e7d-111">选择新复制的站点。</span><span class="sxs-lookup"><span data-stu-id="51e7d-111">Select the newly copied site.</span></span>
1. <span data-ttu-id="51e7d-112">在 **站点设置** 下，选择 **渠道**。</span><span class="sxs-lookup"><span data-stu-id="51e7d-112">Under **Site settings**, select **Channels**.</span></span>
1. <span data-ttu-id="51e7d-113">在渠道名称旁边，选择省略号 (**...**)，然后选择 **更改在线商店渠道**。</span><span class="sxs-lookup"><span data-stu-id="51e7d-113">Next to the channel name, select the ellipsis (**...**), and then select **Change online store channel**.</span></span>
1. <span data-ttu-id="51e7d-114">在 **更改在线商店渠道** 对话框中，选择要映射到新复制的站点的渠道，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="51e7d-114">In the **Change online store channel** dialog box, select the channel to map to the newly copied site, and then select **OK**.</span></span>
1. <span data-ttu-id="51e7d-115">选择 **保存并发布**。</span><span class="sxs-lookup"><span data-stu-id="51e7d-115">Select **Save and publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="51e7d-116">其他资源</span><span class="sxs-lookup"><span data-stu-id="51e7d-116">Additional resources</span></span>

[<span data-ttu-id="51e7d-117">将 Dynamics 365 Commerce 站点与在线渠道相关联</span><span class="sxs-lookup"><span data-stu-id="51e7d-117">Associate a Dynamics 365 Commerce site with an online channel</span></span>](../associate-site-online-store.md)
