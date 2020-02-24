---
title: 客户信用管理
description: ''
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
ms.openlocfilehash: 11da8b7fb59bc8f3e2568ada27db753cc815b9c2
ms.sourcegitcommit: 6a70f9ac296158edd065d52a12703b3ce85ce5ee
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/03/2020
ms.locfileid: "3015128"
---
# <a name="customer-credit-management-overview"></a><span data-ttu-id="3d4bf-102">客户信用管理概览</span><span class="sxs-lookup"><span data-stu-id="3d4bf-102">Customer credit management overview</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="3d4bf-103">客户信用管理使您可以根据创建的信用规则通过过帐流程管理信用限额和控制销售订单流程。</span><span class="sxs-lookup"><span data-stu-id="3d4bf-103">Customer credit management allows you to manage credit limits and control the flow of sales orders through the posting process based on credit rules that you create.</span></span> 

<span data-ttu-id="3d4bf-104">信用管理的使用流程可以包括以下部分或所有步骤：</span><span class="sxs-lookup"><span data-stu-id="3d4bf-104">The process for using credit management can include some or all of the following steps:</span></span>
- <span data-ttu-id="3d4bf-105">用信用属性更新客户，这些信用属性提供有关其信用价值的其他信息。</span><span class="sxs-lookup"><span data-stu-id="3d4bf-105">Update customers with credit attributes that provide additional information about their credit worthiness</span></span> 
- <span data-ttu-id="3d4bf-106">使用信用额度调整为客户创建信用额度</span><span class="sxs-lookup"><span data-stu-id="3d4bf-106">Create credit limits for customers using credit limit adjustments</span></span>
- <span data-ttu-id="3d4bf-107">当您要根据业务需求临时增加或减少信用额度时，请使用信用额度调整为客户创建临时信用额度</span><span class="sxs-lookup"><span data-stu-id="3d4bf-107">Create temporary credit limits for customers using credit limit adjustments when you want to increase or decrease their credit limit temporarily based on business needs</span></span>
- <span data-ttu-id="3d4bf-108">添加可能会影响信用额度的其他信息，例如有关保险和担保的信息</span><span class="sxs-lookup"><span data-stu-id="3d4bf-108">Add additional information that can affect the credit limit such as insurance and guarantees</span></span>
- <span data-ttu-id="3d4bf-109">创建将客户联系在一起的客户信用组，以便他们可以共享一个信用额度</span><span class="sxs-lookup"><span data-stu-id="3d4bf-109">Create customer credit groups that link customers together so they can share a single credit limit</span></span>
- <span data-ttu-id="3d4bf-110">为客户分配风险评分，然后使用这些评分通过信用额度调整为客户自动生成信用额度</span><span class="sxs-lookup"><span data-stu-id="3d4bf-110">Assign risk scores to customers and then use those scores to automatically generate credit limits for customers using credit limit adjustments</span></span>
- <span data-ttu-id="3d4bf-111">根据风险、付款条件、信用额度、逾期金额和已用信用额度的百分比等因素，创建阻止规则，以在一个或多个过帐流程中暂停订单</span><span class="sxs-lookup"><span data-stu-id="3d4bf-111">Create blocking rules that will place an order on hold during one or more posting processes based on factors such as risk, payment terms, credit limits, overdue amounts, and percentage of credit limit used</span></span>
- <span data-ttu-id="3d4bf-112">管理暂停的销售订单列表，查看暂停的原因并缓解问题</span><span class="sxs-lookup"><span data-stu-id="3d4bf-112">Manage a list of sales orders that are on hold, review the reasons for the hold, and mitigate the issues</span></span>
- <span data-ttu-id="3d4bf-113">下达销售订单，并允许其继续完成过帐流程</span><span class="sxs-lookup"><span data-stu-id="3d4bf-113">Release sales orders and allow it to continue through the posting process</span></span>
- <span data-ttu-id="3d4bf-114">设置工作流来管理对信用额度更改和销售订单下达的批准</span><span class="sxs-lookup"><span data-stu-id="3d4bf-114">Set up workflow to manage the approval of credit limit changes and sales order releases</span></span>


<a name="additional-resources"></a><span data-ttu-id="3d4bf-115">其他资源</span><span class="sxs-lookup"><span data-stu-id="3d4bf-115">Additional resources</span></span>
--------
[<span data-ttu-id="3d4bf-116">客户信用管理参数设置</span><span class="sxs-lookup"><span data-stu-id="3d4bf-116">Customer credit management parameters setup</span></span>](./cm-credit-mgmt-setup.md)

[<span data-ttu-id="3d4bf-117">客户信用管理设置信息</span><span class="sxs-lookup"><span data-stu-id="3d4bf-117">Customer credit management setup information</span></span>](./cm-setup-information.md)

[<span data-ttu-id="3d4bf-118">为客户添加信用管理信息</span><span class="sxs-lookup"><span data-stu-id="3d4bf-118">Add credit management information for a customer</span></span>](./cm-add-credit-mgmt-information-customer.md)

[<span data-ttu-id="3d4bf-119">客户信用组</span><span class="sxs-lookup"><span data-stu-id="3d4bf-119">Customer credit groups</span></span>](./cm-customer-credit-groups.md)

[<span data-ttu-id="3d4bf-120">客户信用额度调整</span><span class="sxs-lookup"><span data-stu-id="3d4bf-120">Customer credit limit adjustments</span></span>](./cm-credit-limit-adjustments.md)

[<span data-ttu-id="3d4bf-121">销售订单的信用保留</span><span class="sxs-lookup"><span data-stu-id="3d4bf-121">Credit holds for sales orders</span></span>](./cm-sales-order-credit-holds.md)

[<span data-ttu-id="3d4bf-122">客户信用管理定期任务</span><span class="sxs-lookup"><span data-stu-id="3d4bf-122">Customer credit management periodic tasks</span></span>](./cm-periodic-tasks.md)


