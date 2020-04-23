---
title: 用于群集领料的产品确认
description: 此主题描述如何设置物料验证和群集领料。
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFAutoConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7e6493afb64acb4d7644aac8dad71a0917c76549
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205774"
---
[!include [banner](../includes/banner.md)]

# <a name="product-confirmation-for-cluster-picking"></a><span data-ttu-id="cd720-103">用于群集领料的产品确认</span><span class="sxs-lookup"><span data-stu-id="cd720-103">Product confirmation for cluster picking</span></span>
<span data-ttu-id="cd720-104">群集领料让您能够同时领取多个订单的物料。</span><span class="sxs-lookup"><span data-stu-id="cd720-104">Cluster picking allows you to pick items for several orders at the same time.</span></span> <span data-ttu-id="cd720-105">应用群集领料时，物料确认是验证添加到群集的物料的关键。</span><span class="sxs-lookup"><span data-stu-id="cd720-105">When cluster picking is applied, item confirmation is crucial to verify the items that are added to clusters.</span></span> <span data-ttu-id="cd720-106">您可以在群集领料流程中验证群集领料中的物料。</span><span class="sxs-lookup"><span data-stu-id="cd720-106">You can verify items in cluster picking during the cluster picking process.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="cd720-107">适用情况</span><span class="sxs-lookup"><span data-stu-id="cd720-107">Where it applies</span></span>
<span data-ttu-id="cd720-108">群集领料物料验证与您在非群集领料流程中验证物料的工作方式相同。</span><span class="sxs-lookup"><span data-stu-id="cd720-108">Item verification for cluster picking works the same way as when you verify items in a non-cluster picking processes.</span></span> <span data-ttu-id="cd720-109">设置基于产品条码设置。</span><span class="sxs-lookup"><span data-stu-id="cd720-109">The setup is based on the product bar code setup.</span></span>

## <a name="set-up-item-verification-with-cluster-picking"></a><span data-ttu-id="cd720-110">设置群集领料的物料验证</span><span class="sxs-lookup"><span data-stu-id="cd720-110">Set up item verification with cluster picking</span></span>
1.  <span data-ttu-id="cd720-111">在移动设备菜单项上，打开工作确认的设置窗体：**仓库管理** > **仓库管理** > **设置** > **移动设备** > **移动设备菜单项**。</span><span class="sxs-lookup"><span data-stu-id="cd720-111">On a mobile device menu item, open the setup form for work confirmation: **Warehouse management** > **Warehouse management** > **Setup** > **Mobile device** > **Mobile device menu items**.</span></span>
2.  <span data-ttu-id="cd720-112">从移动设备菜单项打开**工作确认设置**。</span><span class="sxs-lookup"><span data-stu-id="cd720-112">From the mobile device menu item, open **Work confirmation setup**.</span></span>

|        <span data-ttu-id="cd720-113">选项</span><span class="sxs-lookup"><span data-stu-id="cd720-113">Option</span></span>        |                                    <span data-ttu-id="cd720-114">说明</span><span class="sxs-lookup"><span data-stu-id="cd720-114">Description</span></span>                                    |
|----------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="cd720-115">产品确认</span><span class="sxs-lookup"><span data-stu-id="cd720-115">Product confirmation</span></span> | <span data-ttu-id="cd720-116">允许您在扫描时从移动设备验证每件库存。</span><span class="sxs-lookup"><span data-stu-id="cd720-116">Allows you to verify each piece of inventory from the mobile device when scanned.</span></span> |

