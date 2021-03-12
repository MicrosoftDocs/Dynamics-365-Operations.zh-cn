---
title: 创建零售渠道的财务维度并配置商店上的维度值
description: 此程序会逐步演示如何创建带有维度值的商业渠道财务维度，以及配置商店的财务维度值的步骤。
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 86fc9c9a400bee1280b32f10b1e8f55e581e1984
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4964737"
---
# <a name="create-financial-dimensions-for-retail-channels-and-configure-dimension-values-on-stores"></a><span data-ttu-id="362a3-103">创建零售渠道的财务维度并配置商店上的维度值</span><span class="sxs-lookup"><span data-stu-id="362a3-103">Create financial dimensions for retail channels and configure dimension values on stores</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="362a3-104">此程序会逐步演示如何创建带有维度值的商业渠道财务维度，以及配置商店的财务维度值的步骤。</span><span class="sxs-lookup"><span data-stu-id="362a3-104">This procedure walks through creating a commerce channel financial dimension with dimension values and steps to configure financial dimension values on stores.</span></span> <span data-ttu-id="362a3-105">该主题不包括其他相关步骤，例如创建维度集和科目结构。</span><span class="sxs-lookup"><span data-stu-id="362a3-105">The topic does not include other related steps, such as creating dimension sets and account structures.</span></span> <span data-ttu-id="362a3-106">此程序使用 USRT 演示数据公司。</span><span class="sxs-lookup"><span data-stu-id="362a3-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="362a3-107">转到“总帐”>“会计科目表”>“维度”>“财务维度”。</span><span class="sxs-lookup"><span data-stu-id="362a3-107">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="362a3-108">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="362a3-108">Click New.</span></span>
3. <span data-ttu-id="362a3-109">在“使用以下来源中的值”字段中，选择“商业渠道”。</span><span class="sxs-lookup"><span data-stu-id="362a3-109">In the Use values from field, select 'Commerce channels'.</span></span>
4. <span data-ttu-id="362a3-110">在“维度名称”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="362a3-110">In the Dimension name field, type a value.</span></span>
5. <span data-ttu-id="362a3-111">单击“启用”。</span><span class="sxs-lookup"><span data-stu-id="362a3-111">Click Activate.</span></span>
6. <span data-ttu-id="362a3-112">单击“关闭”。</span><span class="sxs-lookup"><span data-stu-id="362a3-112">Click Close.</span></span>
7. <span data-ttu-id="362a3-113">单击“启用”。</span><span class="sxs-lookup"><span data-stu-id="362a3-113">Click Activate.</span></span>
8. <span data-ttu-id="362a3-114">单击“维度值”。</span><span class="sxs-lookup"><span data-stu-id="362a3-114">Click Dimension values.</span></span>
9. <span data-ttu-id="362a3-115">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="362a3-115">Close the page.</span></span>
10. <span data-ttu-id="362a3-116">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="362a3-116">Click Save.</span></span>
11. <span data-ttu-id="362a3-117">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="362a3-117">Close the page.</span></span>
12. <span data-ttu-id="362a3-118">转至“Retail 和 Commerce”>“渠道”>“商店”>“所有商店”。</span><span class="sxs-lookup"><span data-stu-id="362a3-118">Go to Retail and Commerce > Channels > Stores > All stores.</span></span>
13. <span data-ttu-id="362a3-119">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="362a3-119">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="362a3-120">切换“财务维度”部分的展开项。</span><span class="sxs-lookup"><span data-stu-id="362a3-120">Toggle the expansion of the Financial dimensions section.</span></span>
15. <span data-ttu-id="362a3-121">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="362a3-121">Click Edit.</span></span>
16. <span data-ttu-id="362a3-122">在“商业渠道”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="362a3-122">In the Commerce channel field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="362a3-123">在列表中，查找并选择正在更新的商店的维度值。</span><span class="sxs-lookup"><span data-stu-id="362a3-123">In the list, find and select the dimension value for the store being updated.</span></span>
18. <span data-ttu-id="362a3-124">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="362a3-124">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="362a3-125">在“成本中心”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="362a3-125">In the CostCenter field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="362a3-126">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="362a3-126">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="362a3-127">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="362a3-127">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="362a3-128">在“部门”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="362a3-128">In the Department field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="362a3-129">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="362a3-129">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="362a3-130">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="362a3-130">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="362a3-131">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="362a3-131">Click Save.</span></span>

