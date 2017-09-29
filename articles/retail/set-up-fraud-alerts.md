---
title: "设置欺诈预警"
description: "此主题说明在订单处理过程中，如何设置预警规则来通知客户服务代表潜在的欺诈信息。 您可以定义特别的代码用以自动或手动地暂停可疑订单。"
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 79103
ms.assetid: e342af8d-7498-4d20-8483-ab368429c578
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: 09d80015298c3d0219b6ffb290dc456990536a62
ms.contentlocale: zh-cn
ms.lasthandoff: 06/29/2017



---

# <a name="set-up-fraud-alerts"></a><span data-ttu-id="80414-104">设置欺诈预警</span><span class="sxs-lookup"><span data-stu-id="80414-104">Set up fraud alerts</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="80414-105">此主题说明在订单处理过程中，如何设置预警规则来通知客户服务代表潜在的欺诈信息。</span><span class="sxs-lookup"><span data-stu-id="80414-105">This topic explains how to set up rules to alert customer service representatives of potentially fraudulent information when orders are processed.</span></span> <span data-ttu-id="80414-106">您可以定义特别的代码用以自动或手动地暂停可疑订单。</span><span class="sxs-lookup"><span data-stu-id="80414-106">You can define specific codes to use to automatically or manually put suspicious orders on hold.</span></span> 

<span data-ttu-id="80414-107">在设置和使用欺诈检查规则之前，您必须启用欺诈检查并在呼叫中心参数中定义基本欺诈检查值。</span><span class="sxs-lookup"><span data-stu-id="80414-107">Before you set up and use fraud checking rules, you must enable fraud checking and define the basic fraud checking values in the call center parameters.</span></span> <span data-ttu-id="80414-108">有以下两种类型的欺诈规则：</span><span class="sxs-lookup"><span data-stu-id="80414-108">There are two types of fraud rules:</span></span>

-   <span data-ttu-id="80414-109">**静态规则** 使用特定的值，例如已列入黑名单的电话号码。</span><span class="sxs-lookup"><span data-stu-id="80414-109">**Static rules** use a specific value, such as a phone number that has been blacklisted.</span></span>
-   <span data-ttu-id="80414-110">**动态规则** 可由变量和条件构成。</span><span class="sxs-lookup"><span data-stu-id="80414-110">**Dynamic rules** can be composed from variables and conditions.</span></span>

<span data-ttu-id="80414-111">在创建动态规则之前，您需创建变量和条件，它们定义了规则适用对象以及适用场合。</span><span class="sxs-lookup"><span data-stu-id="80414-111">Before you create a dynamic rule, you must create the variables and conditions that define who the rule applies to and when the rule should be applied.</span></span> <span data-ttu-id="80414-112">例如，您需要创建一个规则以要求将客户 1202 下达的价值 1,000.00 或更高的任何销售订单置于暂停状态，直到客户付款被确认。</span><span class="sxs-lookup"><span data-stu-id="80414-112">For example, you want to create a rule to require that any sales order that customer 1202 places that is worth 1,000.00 or more be put on hold until the customer payment can be verified.</span></span> <span data-ttu-id="80414-113">在此情况下，变量为客户 1202 和订单总和 1,000.00。</span><span class="sxs-lookup"><span data-stu-id="80414-113">In this case, the variables are customer 1202 and an order total of 1,000.00.</span></span> <span data-ttu-id="80414-114">此条件指定，如果客户 1202 下达了订单且订单的总金额大于或等于 1,000.00，则必须将销售订单置于暂停状态，直到客户付款被确认。</span><span class="sxs-lookup"><span data-stu-id="80414-114">The condition specifies that if customer 1202 places an order, and the total amount of the order is equal to or more than 1,000.00, the sales order must be put on hold until the customer payment can be verified.</span></span>




