--- 
title: "配置机器学习支持的产品建议"
description: "此过程刷新实体商店中为生产建议提供支持的机器学习系统使用的数据，然后启用有关 POS 客户端的产品建议。"
author: ashishmsft
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 277ffb879b80fe57deeaa2b52c1543baaf820274
ms.contentlocale: zh-cn
ms.lasthandoff: 02/07/2018

---
# <a name="configure-machine-learning-powered-product-recommendations"></a><span data-ttu-id="9b6dd-103">配置机器学习支持的产品建议</span><span class="sxs-lookup"><span data-stu-id="9b6dd-103">Configure machine learning-powered product recommendations</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="9b6dd-104">此过程刷新实体商店中为生产建议提供支持的机器学习系统使用的数据，然后启用有关 POS 客户端的产品建议。</span><span class="sxs-lookup"><span data-stu-id="9b6dd-104">This procedure refreshes the data in the Entity store that is used by the machine learning system that powers product recommendations, and then enables product recommendations on POS clients.</span></span> <span data-ttu-id="9b6dd-105">此程序使用 USRT 演示数据公司。</span><span class="sxs-lookup"><span data-stu-id="9b6dd-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="9b6dd-106">转到“系统管理”>“设置”>“实体商店”。</span><span class="sxs-lookup"><span data-stu-id="9b6dd-106">Go to System administration > Setup > Entity Store.</span></span>
2. <span data-ttu-id="9b6dd-107">在列表中，找到并选择记录“RetailSales”。</span><span class="sxs-lookup"><span data-stu-id="9b6dd-107">In the list, find and select the record 'RetailSales'.</span></span>
3. <span data-ttu-id="9b6dd-108">单击“刷新”。</span><span class="sxs-lookup"><span data-stu-id="9b6dd-108">Click Refresh.</span></span>
4. <span data-ttu-id="9b6dd-109">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="9b6dd-109">Click OK.</span></span>
5. <span data-ttu-id="9b6dd-110">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="9b6dd-110">Close the page.</span></span>
6. <span data-ttu-id="9b6dd-111">转到“零售和商业”>“总部设置”>“参数”>“零售参数”。</span><span class="sxs-lookup"><span data-stu-id="9b6dd-111">Go to Retail and commerce > Headquarters setup > Parameters > Retail parameters.</span></span>
7. <span data-ttu-id="9b6dd-112">单击“机器学习”选项卡。</span><span class="sxs-lookup"><span data-stu-id="9b6dd-112">Click the Machine learning tab.</span></span>
8. <span data-ttu-id="9b6dd-113">在“启用产品建议”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="9b6dd-113">Select 'Yes' in the Enable product recommendations field.</span></span>
    * <span data-ttu-id="9b6dd-114">如果收到消息“无法检索建议模型”，这是因为您最近刷新了实体商店，并且系统可能尚未完成新数据的吸收。</span><span class="sxs-lookup"><span data-stu-id="9b6dd-114">If you receive the message "The recommendation models couldn't be retrieved", it’s because you refreshed the Entity Store very recently and the system may not have finished assimilating the new data.</span></span> <span data-ttu-id="9b6dd-115">等待 2-3 小时再重试。</span><span class="sxs-lookup"><span data-stu-id="9b6dd-115">Wait 2-3 hours and try again.</span></span>  
9. <span data-ttu-id="9b6dd-116">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="9b6dd-116">Click Save.</span></span>
10. <span data-ttu-id="9b6dd-117">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="9b6dd-117">Close the page.</span></span>


