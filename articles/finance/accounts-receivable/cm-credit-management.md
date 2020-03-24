---
title: 客户信用管理
description: 客户信用管理使您可以根据创建的信用规则通过过帐流程管理信用限额和控制销售订单流程。
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1e7d3325587d7cfc876e8f8c7b9207d44046ccd4
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124269"
---
# <a name="customer-credit-management-overview"></a><span data-ttu-id="e6833-103">客户信用管理概览</span><span class="sxs-lookup"><span data-stu-id="e6833-103">Customer credit management overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e6833-104">客户信用管理使您可以根据创建的信用规则通过过帐流程管理信用限额和控制销售订单流程。</span><span class="sxs-lookup"><span data-stu-id="e6833-104">Customer credit management allows you to manage credit limits and control the flow of sales orders through the posting process based on credit rules that you create.</span></span> 

<span data-ttu-id="e6833-105">信用管理的使用流程可以包括以下部分或所有步骤：</span><span class="sxs-lookup"><span data-stu-id="e6833-105">The process for using credit management can include some or all of the following steps:</span></span>
- <span data-ttu-id="e6833-106">用信用属性更新客户，这些信用属性提供有关其信用价值的其他信息。</span><span class="sxs-lookup"><span data-stu-id="e6833-106">Update customers with credit attributes that provide additional information about their credit worthiness</span></span> 
- <span data-ttu-id="e6833-107">使用信用额度调整为客户创建信用额度</span><span class="sxs-lookup"><span data-stu-id="e6833-107">Create credit limits for customers using credit limit adjustments</span></span>
- <span data-ttu-id="e6833-108">当您要根据业务需求临时增加或减少信用额度时，请使用信用额度调整为客户创建临时信用额度</span><span class="sxs-lookup"><span data-stu-id="e6833-108">Create temporary credit limits for customers using credit limit adjustments when you want to increase or decrease their credit limit temporarily based on business needs</span></span>
- <span data-ttu-id="e6833-109">添加可能会影响信用额度的其他信息，例如有关保险和担保的信息</span><span class="sxs-lookup"><span data-stu-id="e6833-109">Add additional information that can affect the credit limit such as insurance and guarantees</span></span>
- <span data-ttu-id="e6833-110">创建将客户联系在一起的客户信用组，以便他们可以共享一个信用额度</span><span class="sxs-lookup"><span data-stu-id="e6833-110">Create customer credit groups that link customers together so they can share a single credit limit</span></span>
- <span data-ttu-id="e6833-111">为客户分配风险评分，然后使用这些评分通过信用额度调整为客户自动生成信用额度</span><span class="sxs-lookup"><span data-stu-id="e6833-111">Assign risk scores to customers and then use those scores to automatically generate credit limits for customers using credit limit adjustments</span></span>
- <span data-ttu-id="e6833-112">根据风险、付款条件、信用额度、逾期金额和已用信用额度的百分比等因素，创建阻止规则，以在一个或多个过帐流程中暂停订单</span><span class="sxs-lookup"><span data-stu-id="e6833-112">Create blocking rules that will place an order on hold during one or more posting processes based on factors such as risk, payment terms, credit limits, overdue amounts, and percentage of credit limit used</span></span>
- <span data-ttu-id="e6833-113">管理暂停的销售订单列表，查看暂停的原因并缓解问题</span><span class="sxs-lookup"><span data-stu-id="e6833-113">Manage a list of sales orders that are on hold, review the reasons for the hold, and mitigate the issues</span></span>
- <span data-ttu-id="e6833-114">下达销售订单，并允许其继续完成过帐流程</span><span class="sxs-lookup"><span data-stu-id="e6833-114">Release sales orders and allow it to continue through the posting process</span></span>
- <span data-ttu-id="e6833-115">设置工作流来管理对信用额度更改和销售订单下达的批准</span><span class="sxs-lookup"><span data-stu-id="e6833-115">Set up workflow to manage the approval of credit limit changes and sales order releases</span></span>


<a name="additional-resources"></a><span data-ttu-id="e6833-116">其他资源</span><span class="sxs-lookup"><span data-stu-id="e6833-116">Additional resources</span></span>
--------
[<span data-ttu-id="e6833-117">客户信用管理参数设置</span><span class="sxs-lookup"><span data-stu-id="e6833-117">Customer credit management parameters setup</span></span>](./cm-credit-mgmt-setup.md)

[<span data-ttu-id="e6833-118">客户信用管理设置信息</span><span class="sxs-lookup"><span data-stu-id="e6833-118">Customer credit management setup information</span></span>](./cm-setup-information.md)

[<span data-ttu-id="e6833-119">为客户添加信用管理信息</span><span class="sxs-lookup"><span data-stu-id="e6833-119">Add credit management information for a customer</span></span>](./cm-add-credit-mgmt-information-customer.md)

[<span data-ttu-id="e6833-120">客户信用组</span><span class="sxs-lookup"><span data-stu-id="e6833-120">Customer credit groups</span></span>](./cm-customer-credit-groups.md)

[<span data-ttu-id="e6833-121">客户信用额度调整</span><span class="sxs-lookup"><span data-stu-id="e6833-121">Customer credit limit adjustments</span></span>](./cm-credit-limit-adjustments.md)

[<span data-ttu-id="e6833-122">销售订单的信用保留</span><span class="sxs-lookup"><span data-stu-id="e6833-122">Credit holds for sales orders</span></span>](./cm-sales-order-credit-holds.md)

[<span data-ttu-id="e6833-123">客户信用管理定期任务</span><span class="sxs-lookup"><span data-stu-id="e6833-123">Customer credit management periodic tasks</span></span>](./cm-periodic-tasks.md)


