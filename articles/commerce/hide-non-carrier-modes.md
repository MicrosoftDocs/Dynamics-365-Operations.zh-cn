---
title: 在 POS 的装运选项中隐藏非承运人交货方式
description: 本主题介绍一个配置选项，当在销售点 (POS) 应用程序中创建装运订单时，该配置选项可以防止选择中出现非承运人交货方式。
author: hhainesms
manager: annbe
ms.date: 10/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: fcacb4243e78607d19d2c57aff5debe04d85d6f2
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009713"
---
# <a name="hide-non-carrier-delivery-modes-from-the-shipping-options-in-pos"></a><span data-ttu-id="c3b70-103">在 POS 的装运选项中隐藏非承运人交货方式</span><span class="sxs-lookup"><span data-stu-id="c3b70-103">Hide non-carrier delivery modes from the shipping options in POS</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="c3b70-104">本主题介绍可用于销售点 (POS) 应用程序的配置选项。</span><span class="sxs-lookup"><span data-stu-id="c3b70-104">This topic describes a configuration option that is available for the point of sale (POS) application.</span></span> <span data-ttu-id="c3b70-105">此配置选项更改了在 POS 中创建装运订单时，选择交货方式的行为。</span><span class="sxs-lookup"><span data-stu-id="c3b70-105">This configuration option changes the behavior for the selection of a mode of delivery when shipment orders are created in POS.</span></span>

<span data-ttu-id="c3b70-106">用户在 POS 中创建客户装运订单时，他们可以选择装运的交货方式。</span><span class="sxs-lookup"><span data-stu-id="c3b70-106">When users create customer shipment orders in POS, they can select a mode of delivery for the shipment.</span></span> <span data-ttu-id="c3b70-107">无论是装运整个订单还是仅选定的行，此功能都可用。</span><span class="sxs-lookup"><span data-stu-id="c3b70-107">This functionality is available regardless of whether the whole order is being shipped or only selected lines.</span></span>

<span data-ttu-id="c3b70-108">默认情况下，选择了交货方式的对话框将显示渠道、物料和交货地址的组合的所有有效交货方式。</span><span class="sxs-lookup"><span data-stu-id="c3b70-108">By default, the dialog box where a mode of delivery is selected shows all the valid modes of delivery for the combination of a channel, an item, and a delivery address.</span></span> <span data-ttu-id="c3b70-109">这些交货方式在 Headquarters 的 **交货方式** 页面上定义（**销售和市场 \> 设置 \> 配送 \> 交货方式**）。</span><span class="sxs-lookup"><span data-stu-id="c3b70-109">These modes of delivery are defined on the **Modes of delivery** page in Headquarters (**Sales and marketing \> Setup \> Distribution \> Modes of delivery**).</span></span> <span data-ttu-id="c3b70-110">对话框中还会出现供选择的“非承运人”交货方式，如 **Carryout** 或 **Pickup**。</span><span class="sxs-lookup"><span data-stu-id="c3b70-110">"Non-carrier" modes of delivery, such as **Carryout** or **Pickup**, might also appear for selection in the dialog box.</span></span>

<span data-ttu-id="c3b70-111">但是，已增加了一项功能，使您可以在对话框中隐藏非承运人交货方式。</span><span class="sxs-lookup"><span data-stu-id="c3b70-111">However, a feature has been added that lets you hide non-carrier modes of delivery in the dialog box.</span></span> <span data-ttu-id="c3b70-112">要启用此功能，请在 **Commerce 参数** 页面上的 **客户订单** 选项卡上，将 **仅显示装运订单的承运人模式选项** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="c3b70-112">To turn on this feature, on the **Commerce parameters** page, on the **Customer orders** tab, set the **Show only carrier mode options for ship orders** option to **Yes**.</span></span> <span data-ttu-id="c3b70-113">启用此功能并运行适当的配送作业以将信息同步到渠道数据库后，在 POS 中创建装运订单的流程中将不会出现供选择的非承运人交货方式。</span><span class="sxs-lookup"><span data-stu-id="c3b70-113">After you turn on this feature and run the appropriate distribution jobs to sync the information to the channel database, non-carrier modes of delivery won't appear for selection during the process of creating shipment orders in POS.</span></span>
