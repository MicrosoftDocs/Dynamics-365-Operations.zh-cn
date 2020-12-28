---
title: 设置租赁日记帐名称
description: 本主题说明如何定义租赁日记帐名称。 租赁日记帐名称指定资产租赁中源于的条目过帐到的日记帐。
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e8b1b908dfd6d1d6072b6efa83f13ae5784c85c1
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4440944"
---
# <a name="set-up-lease-journal-names"></a><span data-ttu-id="a99ee-104">设置租赁日记帐名称</span><span class="sxs-lookup"><span data-stu-id="a99ee-104">Set up lease journal names</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a99ee-105">租赁日记帐名称指定资产租赁交易过帐到的日记帐。</span><span class="sxs-lookup"><span data-stu-id="a99ee-105">Lease journal names specify the journals that Asset leasing transactions are posted to.</span></span> <span data-ttu-id="a99ee-106">**资产租赁参数** 页面中的 **初始确认** 和 **月日记帐名称** 字段中显示分配给 **资产租赁** 日记帐类型的日记帐名称。</span><span class="sxs-lookup"><span data-stu-id="a99ee-106">Only journal names that are assigned to the **Asset leasing** journal type appear in the **Initial Recognition** and **Monthly Journal Name** fields on the **Asset leasing parameters** page.</span></span> <span data-ttu-id="a99ee-107">只能将 **供应商发票记录** 日记帐类型分配给 **发票日记帐名称** 字段。</span><span class="sxs-lookup"><span data-stu-id="a99ee-107">Only **vendor invoice recording** journal type can be assigned to the **Invoice journal name** field.</span></span>

<span data-ttu-id="a99ee-108">要配置租赁日记帐名称，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="a99ee-108">To configure lease journal names, follow these steps.</span></span>

1. <span data-ttu-id="a99ee-109">转到 **资产租赁 \> 设置 \> 资产租赁参数**。</span><span class="sxs-lookup"><span data-stu-id="a99ee-109">Go to **Asset leasing \> Setup \> Asset leasing parameters**.</span></span>
2. <span data-ttu-id="a99ee-110">在 **常规** 选项卡的 **初始确认日记帐名称** 字段中，选择日记帐。</span><span class="sxs-lookup"><span data-stu-id="a99ee-110">On the **General** tab, in the **Initial recognition journal name** field, and select a journal.</span></span> <span data-ttu-id="a99ee-111">将把所有初始确认日记帐条目过帐到该日记帐名称。</span><span class="sxs-lookup"><span data-stu-id="a99ee-111">All initial recognition journal entries will be posted to this journal name.</span></span>
3. <span data-ttu-id="a99ee-112">在 **发票日记帐名称** 字段中，选择日记帐。</span><span class="sxs-lookup"><span data-stu-id="a99ee-112">In the **Invoice journal name** field, select a journal.</span></span> <span data-ttu-id="a99ee-113">如果为租赁帐簿将 **向供应商付款** 选项设置为 **是**，将把租赁和费用付款发票过帐到该日记帐名称。</span><span class="sxs-lookup"><span data-stu-id="a99ee-113">If the **Pay to vendor** option is set to **Yes** for the lease book, lease and expense payment invoices will be posted to this journal name.</span></span>
4. <span data-ttu-id="a99ee-114">在 **租赁日记帐名称** 字段中，选择日记帐。</span><span class="sxs-lookup"><span data-stu-id="a99ee-114">In the **Lease journal name** field, select a journal.</span></span> <span data-ttu-id="a99ee-115">所有折旧、利息和短期重新分类条目都将过帐到该日记帐名称。</span><span class="sxs-lookup"><span data-stu-id="a99ee-115">All depreciation, interest, and short-term reclassification entries will be posted to this journal name.</span></span> <span data-ttu-id="a99ee-116">如果为租赁帐簿将 **向供应商付款** 选项设置为 **否**，将把租赁付款和费用付款条目也过帐到该日记帐名称。</span><span class="sxs-lookup"><span data-stu-id="a99ee-116">If the **Pay to vendor** option is set to **No** for the lease book, lease payments and expense payment entries will also be posted to this journal name.</span></span>
