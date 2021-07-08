---
title: 物料不能包含物料清单或配方
description: 当您尝试确认订单时，将在物料验证期间收到一条错误消息。 它指出物料不能包含物料清单 (BOM) 或配方。
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPO
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 6739b8b1e4d080055a2a0501427eac1c2e8a96c5
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294020"
---
# <a name="item-cant-have-a-bom-or-formula"></a><span data-ttu-id="5b952-104">物料不能包含物料清单或配方</span><span class="sxs-lookup"><span data-stu-id="5b952-104">Item can't have a BOM or formula</span></span>

<span data-ttu-id="5b952-105">错误代码：PRO2614</span><span class="sxs-lookup"><span data-stu-id="5b952-105">Error code: PRO2614</span></span>

## <a name="symptoms"></a><span data-ttu-id="5b952-106">故障特征</span><span class="sxs-lookup"><span data-stu-id="5b952-106">Symptoms</span></span>

<span data-ttu-id="5b952-107">当您尝试确认订单时，将在物料验证期间收到以下错误消息：</span><span class="sxs-lookup"><span data-stu-id="5b952-107">When you try to firm an order, you receive the following error message during item validation:</span></span>

> <span data-ttu-id="5b952-108">物料不能包含物料清单或配方</span><span class="sxs-lookup"><span data-stu-id="5b952-108">Item cannot have a BOM or formula</span></span>

## <a name="resolution"></a><span data-ttu-id="5b952-109">解决方法</span><span class="sxs-lookup"><span data-stu-id="5b952-109">Resolution</span></span>

<span data-ttu-id="5b952-110">具有物料清单 (BOM) 或配方的物料必须属于 *计划物料*、*物料清单* 或 *配方* 类型。</span><span class="sxs-lookup"><span data-stu-id="5b952-110">Items that have a bill of materials (BOM) or formula must be of the *Planning item*, *BOM*, or *formula* type.</span></span> <span data-ttu-id="5b952-111">若要更改物料的类型，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="5b952-111">To change the type of an item, follow these steps.</span></span>

1. <span data-ttu-id="5b952-112">转到 **产品信息管理 \> 产品 \> 已发布产品**。</span><span class="sxs-lookup"><span data-stu-id="5b952-112">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="5b952-113">打开相关产品。</span><span class="sxs-lookup"><span data-stu-id="5b952-113">Open the relevant product.</span></span>
1. <span data-ttu-id="5b952-114">在 **工程师** 快速选项卡上，将 **生产类型** 字段设置为 *计划物料*、*物料清单* 或 *配方*。</span><span class="sxs-lookup"><span data-stu-id="5b952-114">On the **Engineer** FastTab, set the **Production type** field to *Planning item*, *BOM*, or *formula*.</span></span>
