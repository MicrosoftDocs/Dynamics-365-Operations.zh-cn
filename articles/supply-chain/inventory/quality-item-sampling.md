---
title: 质量管理物料抽样
description: 本主题介绍如何设置物料抽样。
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventItemSampling
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ae8bfd329ca0d7c30adcd93a759ee6bea7b76278
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022220"
---
# <a name="quality-management-item-sampling"></a><span data-ttu-id="9f585-103">质量管理物料抽样</span><span class="sxs-lookup"><span data-stu-id="9f585-103">Quality management item sampling</span></span>

<span data-ttu-id="9f585-104">物料抽样用作质量关联的一部分。</span><span class="sxs-lookup"><span data-stu-id="9f585-104">Item sampling is used as part of a quality association.</span></span> <span data-ttu-id="9f585-105">它定义必须检查的当前实际库存量。</span><span class="sxs-lookup"><span data-stu-id="9f585-105">It defines the amount of current physical inventory that must be inspected.</span></span> <span data-ttu-id="9f585-106">抽样可以基于固定数量、百分比或完整牌照。</span><span class="sxs-lookup"><span data-stu-id="9f585-106">Sampling can be based on fixed quantities, a percentage, or a full license plate.</span></span>

## <a name="set-up-item-sampling"></a><span data-ttu-id="9f585-107">设置物料抽样</span><span class="sxs-lookup"><span data-stu-id="9f585-107">Set up item sampling</span></span>

<span data-ttu-id="9f585-108">请按照以下步骤设置物料抽样。</span><span class="sxs-lookup"><span data-stu-id="9f585-108">Follow these steps to set up item sampling.</span></span>

1. <span data-ttu-id="9f585-109">转到 **库存管理 \> 设置 \> 质量控制 \> 物料抽样**。</span><span class="sxs-lookup"><span data-stu-id="9f585-109">Go to **Inventory management \> Setup \> Quality control \> Item sampling**.</span></span>
1. <span data-ttu-id="9f585-110">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="9f585-110">Select **New**.</span></span>
1. <span data-ttu-id="9f585-111">在 **物料抽样** 字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="9f585-111">In the **Item sampling** field, enter a value.</span></span>
1. <span data-ttu-id="9f585-112">在 **描述** 字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="9f585-112">In the **Description** field, enter a value.</span></span>
1. <span data-ttu-id="9f585-113">在 **值** 字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="9f585-113">In the **Value** field, enter a number.</span></span> <span data-ttu-id="9f585-114">此值与在相邻字段中选择的数量规范值相关。</span><span class="sxs-lookup"><span data-stu-id="9f585-114">This value is related to the quantity specification value that is selected in the adjacent field.</span></span>
1. <span data-ttu-id="9f585-115">如果测试失败，在应锁定全部批次或订单行数量时，在 **流程** 部分选中 **完全锁定** 复选框。</span><span class="sxs-lookup"><span data-stu-id="9f585-115">In the **Process** section, select the **Full blocking** check box if the whole lot or order line quantity should be blocked if a test is failed.</span></span> <span data-ttu-id="9f585-116">如果清除此复选框，测试失败时将仅锁定质检订单中的物料。</span><span class="sxs-lookup"><span data-stu-id="9f585-116">If this check box is cleared, only the items in the quality order will be blocked if a test is failed.</span></span>
1. <span data-ttu-id="9f585-117">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="9f585-117">Select **Save**.</span></span>
1. <span data-ttu-id="9f585-118">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="9f585-118">Close the page.</span></span>

> [!NOTE]
> <span data-ttu-id="9f585-119">*仓库流程质量管理* 功能提供其他的物料抽样功能。</span><span class="sxs-lookup"><span data-stu-id="9f585-119">The *Quality management for warehouse processes* feature provides additional item sampling capabilities.</span></span> <span data-ttu-id="9f585-120">它增加了 *物料抽样范围* 概念，让您可以将完整牌照定义为数量规范。</span><span class="sxs-lookup"><span data-stu-id="9f585-120">It adds the concept of *item sampling scope* and lets you define a full license plate as the quantity specification.</span></span> <span data-ttu-id="9f585-121">如果已启用此功能，请参阅[仓库流程质量管理](quality-management-for-warehouses-processes.md)。</span><span class="sxs-lookup"><span data-stu-id="9f585-121">If you've turned on this feature, see [Quality management for warehouse processes](quality-management-for-warehouses-processes.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
