---
title: 创建 POS 收银机的财务维度并配置收银机上的维度值
description: 此程序会逐步演示如何创建销售点 (POS) 收银机的财务维度，以及演示如何配置收银机的财务维度值。
author: jashanno
manager: AnnBe
ms.date: 11/14/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1e04af04de3d18d375ce3609ab4cd53f652c2fbc
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/01/2020
ms.locfileid: "3021740"
---
# <a name="create-financial-dimensions-for-pos-registers-and-configure-dimension-values-on-registers"></a><span data-ttu-id="1f06c-103">创建 POS 收银机的财务维度并配置收银机上的维度值</span><span class="sxs-lookup"><span data-stu-id="1f06c-103">Create financial dimensions for POS registers and configure dimension values on registers</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="1f06c-104">此程序会逐步演示如何创建销售点 (POS) 收银机的财务维度，以及演示如何配置收银机的财务维度值。</span><span class="sxs-lookup"><span data-stu-id="1f06c-104">This procedure walks through creating financial dimensions for point of sale (POS) registers, and demonstrates how to configure financial dimension values on registers.</span></span> <span data-ttu-id="1f06c-105">此程序不包括其他相关步骤，例如创建维度集和科目结构。</span><span class="sxs-lookup"><span data-stu-id="1f06c-105">This procedure doesn’t include other related steps, such as creating dimension sets and account structures.</span></span> <span data-ttu-id="1f06c-106">这些任务可在其他主题中找到。</span><span class="sxs-lookup"><span data-stu-id="1f06c-106">Those tasks can be found in other topics.</span></span> <span data-ttu-id="1f06c-107">此记录使用 USRT 演示公司。</span><span class="sxs-lookup"><span data-stu-id="1f06c-107">This recording uses USRT demo company.</span></span>

1. <span data-ttu-id="1f06c-108">转到“总帐”>“会计科目表”>“维度”>“财务维度”。</span><span class="sxs-lookup"><span data-stu-id="1f06c-108">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="1f06c-109">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="1f06c-109">Click New.</span></span>
3. <span data-ttu-id="1f06c-110">在“使用以下来源中的值”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="1f06c-110">In the Use values from field, select an option.</span></span>
4. <span data-ttu-id="1f06c-111">在“维度名称”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="1f06c-111">In the Dimension name field, type a value.</span></span>
5. <span data-ttu-id="1f06c-112">单击“启用”。</span><span class="sxs-lookup"><span data-stu-id="1f06c-112">Click Activate.</span></span>
6. <span data-ttu-id="1f06c-113">单击“关闭”。</span><span class="sxs-lookup"><span data-stu-id="1f06c-113">Click Close.</span></span>
7. <span data-ttu-id="1f06c-114">单击“启用”。</span><span class="sxs-lookup"><span data-stu-id="1f06c-114">Click Activate.</span></span>
8. <span data-ttu-id="1f06c-115">单击“维度值”。</span><span class="sxs-lookup"><span data-stu-id="1f06c-115">Click Dimension values.</span></span>
9. <span data-ttu-id="1f06c-116">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="1f06c-116">Close the page.</span></span>
10. <span data-ttu-id="1f06c-117">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="1f06c-117">Click Save.</span></span>
11. <span data-ttu-id="1f06c-118">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="1f06c-118">Close the page.</span></span>
12. <span data-ttu-id="1f06c-119">转至“Retail 和 Commerce”>“渠道设置”>“POS 设置”>“收银机”。</span><span class="sxs-lookup"><span data-stu-id="1f06c-119">Go to Retail and Commerce > Channel setup > POS setup > Registers.</span></span>
13. <span data-ttu-id="1f06c-120">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="1f06c-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="1f06c-121">切换“财务维度”部分的展开项。</span><span class="sxs-lookup"><span data-stu-id="1f06c-121">Toggle the expansion of the Financial dimensions section.</span></span>
15. <span data-ttu-id="1f06c-122">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="1f06c-122">Click Edit.</span></span>
16. <span data-ttu-id="1f06c-123">在“终端”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="1f06c-123">In the Terminal field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="1f06c-124">在列表中，查找并选择正在更新的收银机的维度值。</span><span class="sxs-lookup"><span data-stu-id="1f06c-124">In the list, find and select the dimension value for the register being updated.</span></span>
18. <span data-ttu-id="1f06c-125">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="1f06c-125">Click Save.</span></span>

