---
title: 正在接收混合牌照
description: 此主题描述如何在移动设备上使用混合牌照接收为多个物料登记和创建工作。
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFAutoConfirm, WHSLicensePlate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cc87da5fefde33832fc0be1cfef3aa44b155c0d0
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4423313"
---
# <a name="mixed-license-plate-receiving"></a><span data-ttu-id="1a4e1-103">正在接收混合牌照</span><span class="sxs-lookup"><span data-stu-id="1a4e1-103">Mixed license plate receiving</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1a4e1-104">混合牌照接收允许您在登记和创建入库工作前生成包含多个物料的牌照。</span><span class="sxs-lookup"><span data-stu-id="1a4e1-104">Mixed license plate receiving allows you to build a license plate consisting of multiple items before you register and create put-away work.</span></span> 

<span data-ttu-id="1a4e1-105">包含多个物料的牌照不必在您登记每个物料时在收货台进行拆分。</span><span class="sxs-lookup"><span data-stu-id="1a4e1-105">A license plate that consists of multiple items does not have to be split at the receiving dock for you to register each item.</span></span> 

<span data-ttu-id="1a4e1-106">使用物料相关流确定原始凭证行时，您可以扫描物料控制上的条码。</span><span class="sxs-lookup"><span data-stu-id="1a4e1-106">When using an item-related flow to identify the source document lines, you can scan bar codes on the item control.</span></span> <span data-ttu-id="1a4e1-107">如果条码上配置了一个数量和一个度量单位 (UOM)，该物料和数量将自动添加到混合牌照，且您将返回到屏幕以扫描其他物料。</span><span class="sxs-lookup"><span data-stu-id="1a4e1-107">If the bar code has a quantity and a unit of measure (UOM) configured on it, the item and quantity will automatically be added to the mixed license plate, and you will be returned to the screen to scan another item.</span></span> <span data-ttu-id="1a4e1-108">这可用于快速扫描所有物料，而不必在每个步骤进行确认。</span><span class="sxs-lookup"><span data-stu-id="1a4e1-108">This allows you to quickly scan all the items without having to make a confirmation at each step.</span></span> 

<span data-ttu-id="1a4e1-109">在混合牌照接收流中，您可以显示已经扫描到牌照的物料的列表，并从此处修改或更正物料的数量。</span><span class="sxs-lookup"><span data-stu-id="1a4e1-109">In the flow for mixed license plate receiving, you can display the list of items that are already scanned to the license plate and from here you can modify or correct the quantity of an item.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="1a4e1-110">适用情况</span><span class="sxs-lookup"><span data-stu-id="1a4e1-110">Where it applies</span></span>

<span data-ttu-id="1a4e1-111">混合牌照接收是同时为多个行/物料登记和创建工作的移动设备接收流。</span><span class="sxs-lookup"><span data-stu-id="1a4e1-111">Mixed license plate receiving is a mobile device receiving flow to register and create work for multiple lines/items at the same time.</span></span> <span data-ttu-id="1a4e1-112">这在您收到具有多个物料的传入牌照时很有用。</span><span class="sxs-lookup"><span data-stu-id="1a4e1-112">This is useful if you receive inbound license plates with multiple items.</span></span> 

## <a name="how-to-set-up-mixed-license-plate-receiving"></a><span data-ttu-id="1a4e1-113">如何设置混合牌照接收</span><span class="sxs-lookup"><span data-stu-id="1a4e1-113">How to set up mixed license plate receiving</span></span>
<span data-ttu-id="1a4e1-114">混合牌照接收设置为移动设备菜单项。</span><span class="sxs-lookup"><span data-stu-id="1a4e1-114">Mixed license plate receiving is set up as a mobile device menu item.</span></span>

<span data-ttu-id="1a4e1-115">您需要创建一个使用模式工作的新菜单项，其不使用现有工作，且使用以下其中一种方法：</span><span class="sxs-lookup"><span data-stu-id="1a4e1-115">You need to create a new menu item with mode work that does not use existing work and use one of the following methods:</span></span>

- <span data-ttu-id="1a4e1-116">正在接收混合牌照</span><span class="sxs-lookup"><span data-stu-id="1a4e1-116">Mixed license plate receiving</span></span>
- <span data-ttu-id="1a4e1-117">混合牌照接收和储存</span><span class="sxs-lookup"><span data-stu-id="1a4e1-117">Mixed license plate receiving and put away</span></span>

<span data-ttu-id="1a4e1-118">用于标识原始凭证行的选项为采购订单物料、采购订单行、退货订单、转移单物料和转移单行。</span><span class="sxs-lookup"><span data-stu-id="1a4e1-118">The options to identify the source document lines are purchase order item, purchase order line, return order, transfer order item, and transfer order line.</span></span> <span data-ttu-id="1a4e1-119">这些选项可以更改对单个牌照的接收单。</span><span class="sxs-lookup"><span data-stu-id="1a4e1-119">These options can change the receiving order on a single license plate.</span></span> <span data-ttu-id="1a4e1-120">最后一个选项是按加载物料。</span><span class="sxs-lookup"><span data-stu-id="1a4e1-120">The last option is by load item.</span></span> <span data-ttu-id="1a4e1-121">您可以将多个物料添加到牌照，但不能在多个负荷之间切换。</span><span class="sxs-lookup"><span data-stu-id="1a4e1-121">You can add multiple items to a license plate, but you cannot switch between multiple loads.</span></span>
