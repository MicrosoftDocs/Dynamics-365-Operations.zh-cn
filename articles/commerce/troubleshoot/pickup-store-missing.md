---
title: 零售店没有出现在要从中提货的商店的列表中
description: 本主题提供了故障排除指南，此指南可以在零售店没有出现在可以从中提货的商店列表中时提供帮助。
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
ms.openlocfilehash: 652f5f1a779a412c21c18814071ba0fb7dd2e155
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585220"
---
# <a name="retail-store-doesnt-appear-in-the-list-of-stores-to-pick-up-from"></a><span data-ttu-id="00139-103">零售店没有出现在要从中提货的商店的列表中</span><span class="sxs-lookup"><span data-stu-id="00139-103">Retail store doesn't appear in the list of stores to pick up from</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="00139-104">本主题提供了故障排除指南，此指南可以在零售店没有出现在可以从中提货的商店列表中时提供帮助。</span><span class="sxs-lookup"><span data-stu-id="00139-104">This topic provides troubleshooting guidance that can help when a retail store doesn't appear in the list of stores where items can be picked up.</span></span>

## <a name="description"></a><span data-ttu-id="00139-105">说明</span><span class="sxs-lookup"><span data-stu-id="00139-105">Description</span></span>

<span data-ttu-id="00139-106">零售店没有出现在可以从中提货的商店的列表中。</span><span class="sxs-lookup"><span data-stu-id="00139-106">A retail store doesn't appear in the list of stores where items can be picked up.</span></span>

## <a name="resolution"></a><span data-ttu-id="00139-107">解决方法</span><span class="sxs-lookup"><span data-stu-id="00139-107">Resolution</span></span>

### <a name="configure-the-longitude-and-latitude-for-the-store-address-in-commerce-headquarters"></a><span data-ttu-id="00139-108">在 Commerce Headquarters 中配置商店地址的经度和纬度</span><span class="sxs-lookup"><span data-stu-id="00139-108">Configure the longitude and latitude for the store address in Commerce headquarters</span></span>

<span data-ttu-id="00139-109">要在 Commerce Headquarters 中配置商店地址的经度和纬度，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="00139-109">To configure the longitude and latitude for the store address in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="00139-110">转至 **Retail 和 Commerce \> 渠道 \> 商店 \> 所有商店**。</span><span class="sxs-lookup"><span data-stu-id="00139-110">Go to **Retail and Commerce \> Channels \> Stores \> All stores**.</span></span>
1. <span data-ttu-id="00139-111">在电子商务站点上查找要出现在提货选项中的商店。</span><span class="sxs-lookup"><span data-stu-id="00139-111">Find the store that you want to appear among the pickup options on the e-commerce site.</span></span> <span data-ttu-id="00139-112">记下其 **运营单位编号** 值。</span><span class="sxs-lookup"><span data-stu-id="00139-112">Make a note of its **Operating unit number** value.</span></span>
1. <span data-ttu-id="00139-113">转到 **组织管理 \> 组织 \> 运营单位**。</span><span class="sxs-lookup"><span data-stu-id="00139-113">Go to **Organization administration \> Organizations \> Operating units**.</span></span>
1. <span data-ttu-id="00139-114">搜索您先前记下的运营单位编号，然后在搜索结果中选择此运营单位。</span><span class="sxs-lookup"><span data-stu-id="00139-114">Search for the operating unit number that you noted earlier, and then select the operating unit in the search results.</span></span>
1. <span data-ttu-id="00139-115">在 **地址** 快速选项卡上，选择 **更多选项**，然后选择 **高级**。</span><span class="sxs-lookup"><span data-stu-id="00139-115">On the **Addresses** FastTab, select **More options**, and then select **Advanced**.</span></span>
1. <span data-ttu-id="00139-116">在 **常规** 快速选项卡上，请确保 **经度** 和 **纬度** 字段设置正确。</span><span class="sxs-lookup"><span data-stu-id="00139-116">On the **General** FastTab, make sure that the **Longitude** and **Latitude** fields are correctly set.</span></span> <span data-ttu-id="00139-117">作为此步骤的一部分，请确保将值正确指定为正数或负数。</span><span class="sxs-lookup"><span data-stu-id="00139-117">As part of this step, make sure that the values are correctly specified as positive or negative numbers.</span></span>

### <a name="configure-fulfillment-groups-in-commerce-headquarters"></a><span data-ttu-id="00139-118">在 Commerce Headquarters 中配置履行组</span><span class="sxs-lookup"><span data-stu-id="00139-118">Configure fulfillment groups in Commerce headquarters</span></span>

<span data-ttu-id="00139-119">要在 Commerce Headquarters 中配置履行组，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="00139-119">To configure fulfillment groups in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="00139-120">转至 **Retail 和 Commerce \> 渠道 \> 在线商店**。</span><span class="sxs-lookup"><span data-stu-id="00139-120">Go to **Retail and Commerce \> Channels \> Online stores**.</span></span>
1. <span data-ttu-id="00139-121">选择要配置的在线商店。</span><span class="sxs-lookup"><span data-stu-id="00139-121">Select the online store to configure.</span></span>
1. <span data-ttu-id="00139-122">在操作窗格上，选择 **设置**，然后选择 **履行组分配**。</span><span class="sxs-lookup"><span data-stu-id="00139-122">On the Action Pane, select **Set up**, and then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="00139-123">在 **履行组分配** 页面上，选择在线商店的履行组。</span><span class="sxs-lookup"><span data-stu-id="00139-123">On the **Fulfillment group assignment** page, select the fulfillment group for the online store.</span></span>
1. <span data-ttu-id="00139-124">在 **设置** 下面，请确保已为履行组正确配置零售店。</span><span class="sxs-lookup"><span data-stu-id="00139-124">Under **Setup**, make sure that the retail store is correctly configured for the fulfillment group.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="00139-125">其他资源</span><span class="sxs-lookup"><span data-stu-id="00139-125">Additional resources</span></span> 

[<span data-ttu-id="00139-126">创建运营单位</span><span class="sxs-lookup"><span data-stu-id="00139-126">Create an operating unit</span></span>](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit)

[<span data-ttu-id="00139-127">设置在线渠道</span><span class="sxs-lookup"><span data-stu-id="00139-127">Set up an online channel</span></span>](../channel-setup-online.md)
