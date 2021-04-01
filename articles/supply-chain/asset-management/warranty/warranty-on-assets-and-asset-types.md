---
title: 资产和资产类型的保修
description: 本主题介绍如何在资产管理中为资产和资产类型设置保修。
author: josaw1
manager: tfehr
ms.date: 08/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 78ac93b1e681fca7d7eefd921f282a8496aa9d0a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5245315"
---
# <a name="warranties-on-assets-and-asset-types"></a><span data-ttu-id="86d78-103">资产和资产类型的保修</span><span class="sxs-lookup"><span data-stu-id="86d78-103">Warranties on assets and asset types</span></span>

[!include [banner](../../includes/banner.md)]

 


<span data-ttu-id="86d78-104">本主题介绍如何在资产管理中为资产和资产类型设置保修。</span><span class="sxs-lookup"><span data-stu-id="86d78-104">This topic explains how to set up warranties on assets and asset types in Asset Management.</span></span>

## <a name="set-up-a-warranty-on-an-asset-type"></a><span data-ttu-id="86d78-105">为资产类型设置保修</span><span class="sxs-lookup"><span data-stu-id="86d78-105">Set up a warranty on an asset type</span></span>

1. <span data-ttu-id="86d78-106">选择 **资产管理** \> **设置** \> **资产类型** \> **资产类型**。</span><span class="sxs-lookup"><span data-stu-id="86d78-106">Select **Asset management** \> **Setup** \> **Asset types** \> **Asset types**.</span></span>
2. <span data-ttu-id="86d78-107">在左窗格中，选择要为其附加供应商保修协议的资产类型，然后选择 **资产类型默认**。</span><span class="sxs-lookup"><span data-stu-id="86d78-107">In the left pane, select the asset type to attach a vendor warranty agreement to, and then select **Asset type defaults**.</span></span>
3. <span data-ttu-id="86d78-108">在 **常规** 快速选项卡的 **供应商保修** 字段中，选择协议。</span><span class="sxs-lookup"><span data-stu-id="86d78-108">On the **General** FastTab, in the **Vendor warranty** field, select the agreement.</span></span>

## <a name="set-up-a-warranty-on-an-asset"></a><span data-ttu-id="86d78-109">为资产设置保修</span><span class="sxs-lookup"><span data-stu-id="86d78-109">Set up a warranty on an asset</span></span>

1. <span data-ttu-id="86d78-110">选择 **资产管理** \> **常用** \> **资产** \> **所有资产**。</span><span class="sxs-lookup"><span data-stu-id="86d78-110">Select **Asset management** \> **Common** \> **Assets** \> **All assets**.</span></span>
2. <span data-ttu-id="86d78-111">选择资产，然后选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="86d78-111">Select the asset, and then select **Edit**.</span></span>
3. <span data-ttu-id="86d78-112">在 **供应商** 快速选项卡 **供应商保修** 部分中的 **保修** 字段中，选择保修协议。</span><span class="sxs-lookup"><span data-stu-id="86d78-112">On the **Vendor** FastTab, in the **Vendor warranty** section, in the **Warranty** field, select the warranty agreement.</span></span>
4. <span data-ttu-id="86d78-113">在 **保修开始日期** 和 **保修结束日期** 字段中，选择开始日期和结束日期。</span><span class="sxs-lookup"><span data-stu-id="86d78-113">In the **Warranty start** and **Warranty end** fields, select the start and end dates.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="86d78-114">如果在一个工作订单的 **保修开始日期** 字段中选择了日期，该工作订单的保修将从该日期开始生效。</span><span class="sxs-lookup"><span data-stu-id="86d78-114">If a date is selected in the **Warranty start** field on a work order, the warranty becomes valid for the work order on that date.</span></span> <span data-ttu-id="86d78-115">创建工作订单时，将把 **保修开始日期** 字段自动设置为创建日期。</span><span class="sxs-lookup"><span data-stu-id="86d78-115">When you create a work order, the **Warranty start** field is automatically set to the date of creation.</span></span> <span data-ttu-id="86d78-116">但是，可更改此日期，以使其与保修协议开始日期之类对应。</span><span class="sxs-lookup"><span data-stu-id="86d78-116">However, you can change the date so that it corresponds to, for example, the start date of a warranty agreement.</span></span>
    >
    > ![工作订单页面](media/02-warranty.png)

> [!NOTE]
> <span data-ttu-id="86d78-118">为供应商保修涵盖的资产创建工作订单时，如果该工作订单的预期开始日期在保修期内，您将收到有关保修协议的通知。</span><span class="sxs-lookup"><span data-stu-id="86d78-118">When you create a work order for an asset that is covered by a vendor warranty, if the work order has an expected start date during the warranty period, you receive a notification about the warranty agreement.</span></span> <span data-ttu-id="86d78-119">然后可根据需要取消该工作订单。</span><span class="sxs-lookup"><span data-stu-id="86d78-119">You can then cancel the work order, as you require.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]