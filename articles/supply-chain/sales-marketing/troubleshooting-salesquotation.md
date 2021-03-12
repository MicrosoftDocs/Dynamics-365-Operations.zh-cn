---
title: 销售报价单故障排除
description: 本主题介绍如何解决在使用销售报价单时可能遇到的问题。
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesQuotationTable, SalesQuotationTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 98011dbf22ff55b7651ce63557fa4a360130b6af
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974752"
---
# <a name="troubleshoot-sales-quotations"></a><span data-ttu-id="ebe94-103">销售报价单故障排除</span><span class="sxs-lookup"><span data-stu-id="ebe94-103">Troubleshoot sales quotations</span></span>

<span data-ttu-id="ebe94-104">本主题介绍如何解决在使用销售报价单时可能遇到的问题。</span><span class="sxs-lookup"><span data-stu-id="ebe94-104">This topic describes how to fix issues that you might encounter while you work with sales quotations.</span></span>

## <a name="i-cant-change-the-sales-quantity-of-a-sales-quotation-for-a-service-item"></a><span data-ttu-id="ebe94-105">我无法更改服务物料的销售报价单的销售数量。</span><span class="sxs-lookup"><span data-stu-id="ebe94-105">I can't change the sales quantity of a sales quotation for a service item.</span></span>

### <a name="issue-description"></a><span data-ttu-id="ebe94-106">问题描述</span><span class="sxs-lookup"><span data-stu-id="ebe94-106">Issue description</span></span>

<span data-ttu-id="ebe94-107">如果您尝试在销售报价单行上为 *服务* 类型的物料设置销售数量（**SalesQty** 字段），您将收到以下消息：“不允许更新“数量”字段”。</span><span class="sxs-lookup"><span data-stu-id="ebe94-107">If you try to set a sales quantity (**SalesQty** field) for an item of the *Service* type on a sales quotation line, you will receive the following message: "Update not allowed for field Quantity."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="ebe94-108">解决问题</span><span class="sxs-lookup"><span data-stu-id="ebe94-108">Issue resolution</span></span>

<span data-ttu-id="ebe94-109">您不能为属于服务物料的产品设置销售数量。</span><span class="sxs-lookup"><span data-stu-id="ebe94-109">You can't set a sales quantity for products that are service items.</span></span> <span data-ttu-id="ebe94-110">例如，如果您提供安装物料的服务，那么记录数量是没有意义的，因为没有实际物料。</span><span class="sxs-lookup"><span data-stu-id="ebe94-110">For example, if you offer a service to install an item, it doesn't make sense to record a quantity, because there is no physical item.</span></span> <span data-ttu-id="ebe94-111">只有服务。</span><span class="sxs-lookup"><span data-stu-id="ebe94-111">There is only a service.</span></span>

