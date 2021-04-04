---
title: 登陆成本的采购参数
description: 本主题介绍使用登陆成本模块时如何设置相关的采购参数。
author: sherry-zheng
manager: tfehr
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SrmParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 49e046a1437917cfa866f690511789496fac2c53
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500734"
---
# <a name="procurement-and-sourcing-parameters-for-landed-cost"></a><span data-ttu-id="ef07c-103">登陆成本的采购参数</span><span class="sxs-lookup"><span data-stu-id="ef07c-103">Procurement and sourcing parameters for Landed cost</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="ef07c-104">**采购参数** 页上有一些设置，这些设置在您使用 **登陆成本** 模块时尤为重要。</span><span class="sxs-lookup"><span data-stu-id="ef07c-104">The **Procurement and sourcing parameters** page has a few settings that are especially relevant when you use the **Landed cost** module.</span></span> <span data-ttu-id="ef07c-105">使用从 **采购参数** 页打开的 **更新订单行** 对话框来指定在对采购订单头进行更改时是否应自动更新采购订单行。</span><span class="sxs-lookup"><span data-stu-id="ef07c-105">Use the **Update order lines** dialog box that is opened from the **Procurement and sourcing parameters** page to specify whether purchase order lines should automatically be updated when changes are made on the purchase order header.</span></span>

<span data-ttu-id="ef07c-106">若要完成此设置，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="ef07c-106">To complete this setup, follow these steps.</span></span>

1. <span data-ttu-id="ef07c-107">转至 **采购 \> 设置 \> 采购参数**。</span><span class="sxs-lookup"><span data-stu-id="ef07c-107">Go to **Procurement and sourcing \> Setup \> Procurement and sourcing parameters**.</span></span>
1. <span data-ttu-id="ef07c-108">在 **常规** 选项卡上，选择 **更新订单行** 链接。</span><span class="sxs-lookup"><span data-stu-id="ef07c-108">On the **General** tab, select the **Update order lines** link.</span></span>
1. <span data-ttu-id="ef07c-109">**更新订单行** 对话框将列出订单头上的字段，这些字段还可以将自动更新应用于订单行上的相关字段。</span><span class="sxs-lookup"><span data-stu-id="ef07c-109">The **Update order lines** dialog box lists the fields on the order header that can also apply automatic updates to related fields on the order lines.</span></span> <span data-ttu-id="ef07c-110">将列表中的每个字段设置为以下值之一：</span><span class="sxs-lookup"><span data-stu-id="ef07c-110">Set each field in the list to one of the following values:</span></span>

    - <span data-ttu-id="ef07c-111">**始终** – 更新订单头时，订单行应自动更新。</span><span class="sxs-lookup"><span data-stu-id="ef07c-111">**Always** – The order lines should automatically be updated when the order header is updated.</span></span>
    - <span data-ttu-id="ef07c-112">**从不** – 订单行在订单头更新时应该永远不自动更新。</span><span class="sxs-lookup"><span data-stu-id="ef07c-112">**Never** – The order lines should never be updated when the order header is updated.</span></span>
    - <span data-ttu-id="ef07c-113">**提示** – 将提示用户选择订单行是否应更新。</span><span class="sxs-lookup"><span data-stu-id="ef07c-113">**Prompt** – The user will be prompted to select whether the order lines should be updated.</span></span>
