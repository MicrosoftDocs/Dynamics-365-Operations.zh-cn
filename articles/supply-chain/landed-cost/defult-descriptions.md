---
title: 总帐的默认描述
description: 可以使用默认描述将凭证过帐中的“描述”字段更新为总帐。
author: sherry-zheng
manager: tfehr
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TransactionTexts
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 47c5c9e71dba7a0cb7c798c167208faebeb5af6c
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500372"
---
# <a name="default-descriptions-for-the-general-ledger"></a><span data-ttu-id="23631-103">总帐的默认描述</span><span class="sxs-lookup"><span data-stu-id="23631-103">Default descriptions for the general ledger</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="23631-104">可以使用默认描述将凭证过帐中的 **描述** 字段更新为总帐。</span><span class="sxs-lookup"><span data-stu-id="23631-104">Default descriptions can be used to update the **Description** field in voucher postings to the general ledger.</span></span> <span data-ttu-id="23631-105">此功能已得到增强，可以处理登陆成本。</span><span class="sxs-lookup"><span data-stu-id="23631-105">This functionality has been enhanced to work with Landed cost.</span></span>

<span data-ttu-id="23631-106">要设置分类帐过帐的默认描述，请转到 **组织管理 \> 设置 \> 默认描述**。</span><span class="sxs-lookup"><span data-stu-id="23631-106">To set up default descriptions for ledger postings, go to **Organizational administration \> Setup \> Default descriptions**.</span></span>

<span data-ttu-id="23631-107">下表列出了为支持登陆成本在 **默认描述** 页上为 **描述** 字段添加的新值。</span><span class="sxs-lookup"><span data-stu-id="23631-107">The following table lists the new values that have been added for the **Description** field on the **Default descriptions** page to support Landed cost.</span></span>

| <span data-ttu-id="23631-108">描述类型</span><span class="sxs-lookup"><span data-stu-id="23631-108">Description type</span></span> | <span data-ttu-id="23631-109">说明</span><span class="sxs-lookup"><span data-stu-id="23631-109">Notes</span></span> |
|---|---|
| <span data-ttu-id="23631-110">进口成本计算 – 成本应计</span><span class="sxs-lookup"><span data-stu-id="23631-110">Import costing – Cost accrual</span></span> | <span data-ttu-id="23631-111">过帐采购订单发票时，将处理估计航行成本的成本应计。</span><span class="sxs-lookup"><span data-stu-id="23631-111">When a purchase order invoice is posted, a cost accrual is processed for estimate voyage costs.</span></span> <span data-ttu-id="23631-112">可以将默认描述指定为将航行编号添加到描述中。</span><span class="sxs-lookup"><span data-stu-id="23631-112">Default descriptions can be specified to add the voyage number to the description.</span></span> <span data-ttu-id="23631-113">使用 *%4* 作为装运编号。</span><span class="sxs-lookup"><span data-stu-id="23631-113">Use *%4* for the shipment number.</span></span> |
| <span data-ttu-id="23631-114">进口成本计算 – 在途货物订单</span><span class="sxs-lookup"><span data-stu-id="23631-114">Import costing – Goods in transit order</span></span> | <span data-ttu-id="23631-115">如果您使用的是在途处理，采购订单发票将过帐，货物将过帐到在途货物帐户。</span><span class="sxs-lookup"><span data-stu-id="23631-115">If you're using in-transit processing, the purchase order invoice is posted, and the goods are posted to a goods in transit account.</span></span> <span data-ttu-id="23631-116">可以将默认描述指定为将在途订单编号添加到描述中。</span><span class="sxs-lookup"><span data-stu-id="23631-116">Default descriptions can be specified to add the in-transit order number to the description.</span></span> <span data-ttu-id="23631-117">使用 *%4* 作为在途订单编号。</span><span class="sxs-lookup"><span data-stu-id="23631-117">Use *%4* for the in-transit order number.</span></span> |
| <span data-ttu-id="23631-118">库存 – 结转 – 调整</span><span class="sxs-lookup"><span data-stu-id="23631-118">Inventory – close – adjustment</span></span> | <span data-ttu-id="23631-119">为航行成本处理应付帐款 (AP) 发票时，将处理库存调整以估计航行成本。</span><span class="sxs-lookup"><span data-stu-id="23631-119">When the accounts payable (AP) invoice is processed for a voyage cost, an inventory adjustment is processed to estimate voyage costs.</span></span> <span data-ttu-id="23631-120">可以将默认描述指定为将航行编号添加到描述中。</span><span class="sxs-lookup"><span data-stu-id="23631-120">Default descriptions can be specified to add the voyage number to the description.</span></span> <span data-ttu-id="23631-121">使用 *%4* 作为装运编号。</span><span class="sxs-lookup"><span data-stu-id="23631-121">Use *%4* for the shipment number.</span></span> |

<span data-ttu-id="23631-122">有关如何使用 **默认描述** 页的详细信息，请参阅[设置自动过帐的默认描述](../../finance/general-ledger/set-up-default-descriptions-for-automatic-posting.md)。</span><span class="sxs-lookup"><span data-stu-id="23631-122">For more information about how to work with the **Default descriptions** page, see [Set up default descriptions for automatic posting](../../finance/general-ledger/set-up-default-descriptions-for-automatic-posting.md).</span></span>
