---
title: 改进了批量跟踪物料的处理
description: 此主题介绍了对零售对帐单过帐驱动程序流程中批量跟踪物料的批次处理所做的改进。
author: josaw1
manager: AnnBe
ms.date: 05/28/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-28
ms.dyn365.ops.version: 10
ms.openlocfilehash: 4456fc3d5bc4547fa8211642b11ca6df455fa187
ms.sourcegitcommit: aec1dcd44274e9b8d0770836598fde5533b7b569
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2019
ms.locfileid: "1617381"
---
# <a name="improved-handling-of-batch-tracked-items"></a><span data-ttu-id="d46ee-103">改进了批量跟踪物料的处理</span><span class="sxs-lookup"><span data-stu-id="d46ee-103">Improved handling of batch-tracked items</span></span>

<span data-ttu-id="d46ee-104">在 Microsoft Dynamics 365 for Retail 销售点 (POS) 中，无法在销售时捕获批量跟踪物料的批处理号。</span><span class="sxs-lookup"><span data-stu-id="d46ee-104">In Microsoft Dynamics 365 for Retail Point of Sale (POS), batch numbers can't be captured for batch-tracked items at the time of sale.</span></span> <span data-ttu-id="d46ee-105">但是，对于特定配置，在总部通过客户订单或对帐单过帐来过帐销售额时，Microsoft Dynamics 系统要求批量跟踪物料具备有效的批处理号，这些编号在开票流程中使用。</span><span class="sxs-lookup"><span data-stu-id="d46ee-105">However, for specific configurations, when sales are posted in the headquarters through customer orders or statement posting, the Microsoft Dynamics system expects that valid batch numbers for batch-tracked items exist, and that they will be used during the invoicing process.</span></span>

<span data-ttu-id="d46ee-106">如果有效的批处理号对产品可用，则来自对帐单过帐的客户订单开票流程和销售订单开票流程使用这些编号。</span><span class="sxs-lookup"><span data-stu-id="d46ee-106">If valid batch numbers are available for products, the customer order invoicing process and the sales order invoicing process from statement posting use them.</span></span> <span data-ttu-id="d46ee-107">否则，客户订单开票流程无法过帐，POS 用户将收到错误消息。</span><span class="sxs-lookup"><span data-stu-id="d46ee-107">Otherwise, the customer order invoicing process can't post, and the POS user receives an error message.</span></span> <span data-ttu-id="d46ee-108">对帐单过帐随后会进入错误状态。</span><span class="sxs-lookup"><span data-stu-id="d46ee-108">Statement posting then goes into an error state.</span></span> <span data-ttu-id="d46ee-109">即使为产品启用了负库存，也会出现此错误状态。</span><span class="sxs-lookup"><span data-stu-id="d46ee-109">This error state occurs even when negative inventory has been turned on for the products.</span></span>

<span data-ttu-id="d46ee-110">在 Microsoft Dynamics for Retail 版本 10.0.4 和更高版本中进行的改进可帮助确保在为批量跟踪物料启用了负库存时，如果库存为 0（零）或者批处理号不可用，不会阻止这些物料通过对帐单过帐进行客户订单开票和销售订单开票。</span><span class="sxs-lookup"><span data-stu-id="d46ee-110">Improvements that have been made in Microsoft Dynamics for Retail version 10.0.4 and later help guarantee that, when negative inventory is turned on for batch-tracked items, customer order invoicing and sales order invoicing through statement posting aren't blocked for those items if the inventory is 0 (zero) or a batch number isn't available.</span></span> <span data-ttu-id="d46ee-111">批处理号不可用时，新功能会使用销售行的默认批处理 ID。</span><span class="sxs-lookup"><span data-stu-id="d46ee-111">The new functionality uses a default batch ID for the sales lines when batch numbers aren't available.</span></span>

<span data-ttu-id="d46ee-112">要定义为客户订单使用的默认批处理 ID，请在**零售参数**页面的**客户订单**选项卡上，在**订单**快速选项卡中设置**默认批处理 ID** 字段。</span><span class="sxs-lookup"><span data-stu-id="d46ee-112">To define the default batch ID that is used for customer orders, on the **Retail parameters** page, on the **Customer orders** tab, on the **Order** FastTab, set the **Default batch id** field.</span></span>

<span data-ttu-id="d46ee-113">要定义为通过对帐单过帐进行的销售订单开票使用的默认批处理 ID，请在**零售参数**页面的**过帐**选项卡上，在**库存更新**快速选项卡中设置**默认批处理 ID** 字段。</span><span class="sxs-lookup"><span data-stu-id="d46ee-113">To define the default batch ID that is used for sales order invoicing through statement posting, on the **Retail parameters** page, on the **Posting** tab, on the **Inventory update** FastTab, set the **Default batch id** field.</span></span>

> [!NOTE]
> <span data-ttu-id="d46ee-114">只有为特定商店仓库和物料启用了高级仓储时，此功能才可用。</span><span class="sxs-lookup"><span data-stu-id="d46ee-114">This functionality is available only when advanced warehousing is turned on for the specific store warehouse and items.</span></span> <span data-ttu-id="d46ee-115">在以后的版本中，未使用高级仓库管理的方案也将支持此功能。</span><span class="sxs-lookup"><span data-stu-id="d46ee-115">In a later release, the functionality will also be supported for scenarios where advanced warehouse management isn't used.</span></span>
