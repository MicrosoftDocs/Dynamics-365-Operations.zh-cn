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
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4042fb9da0fe38de50ad7e0c8e64b98925ea1188
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5265951"
---
# <a name="create-financial-dimensions-for-pos-registers-and-configure-dimension-values-on-registers"></a><span data-ttu-id="52c17-103">创建 POS 收银机的财务维度并配置收银机上的维度值</span><span class="sxs-lookup"><span data-stu-id="52c17-103">Create financial dimensions for POS registers and configure dimension values on registers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="52c17-104">此程序会逐步演示如何创建销售点 (POS) 收银机的财务维度，以及演示如何配置收银机的财务维度值。</span><span class="sxs-lookup"><span data-stu-id="52c17-104">This procedure walks through creating financial dimensions for point of sale (POS) registers, and demonstrates how to configure financial dimension values on registers.</span></span> <span data-ttu-id="52c17-105">此程序不包括其他相关步骤，例如创建维度集和科目结构。</span><span class="sxs-lookup"><span data-stu-id="52c17-105">This procedure doesn't include other related steps, such as creating dimension sets and account structures.</span></span> <span data-ttu-id="52c17-106">这些任务可在其他主题中找到。</span><span class="sxs-lookup"><span data-stu-id="52c17-106">Those tasks can be found in other topics.</span></span> <span data-ttu-id="52c17-107">此记录使用 USRT 演示公司。</span><span class="sxs-lookup"><span data-stu-id="52c17-107">This recording uses USRT demo company.</span></span>

1. <span data-ttu-id="52c17-108">转到“总帐”>“会计科目表”>“维度”>“财务维度”。</span><span class="sxs-lookup"><span data-stu-id="52c17-108">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="52c17-109">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="52c17-109">Click New.</span></span>
3. <span data-ttu-id="52c17-110">在“使用以下来源中的值”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="52c17-110">In the Use values from field, select an option.</span></span>
4. <span data-ttu-id="52c17-111">在“维度名称”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="52c17-111">In the Dimension name field, type a value.</span></span>
5. <span data-ttu-id="52c17-112">单击“启用”。</span><span class="sxs-lookup"><span data-stu-id="52c17-112">Click Activate.</span></span>
6. <span data-ttu-id="52c17-113">单击“关闭”。</span><span class="sxs-lookup"><span data-stu-id="52c17-113">Click Close.</span></span>
7. <span data-ttu-id="52c17-114">单击“启用”。</span><span class="sxs-lookup"><span data-stu-id="52c17-114">Click Activate.</span></span>
8. <span data-ttu-id="52c17-115">单击“维度值”。</span><span class="sxs-lookup"><span data-stu-id="52c17-115">Click Dimension values.</span></span>
9. <span data-ttu-id="52c17-116">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="52c17-116">Close the page.</span></span>
10. <span data-ttu-id="52c17-117">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="52c17-117">Click Save.</span></span>
11. <span data-ttu-id="52c17-118">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="52c17-118">Close the page.</span></span>
12. <span data-ttu-id="52c17-119">转至“Retail 和 Commerce”>“渠道设置”>“POS 设置”>“收银机”。</span><span class="sxs-lookup"><span data-stu-id="52c17-119">Go to Retail and Commerce > Channel setup > POS setup > Registers.</span></span>
13. <span data-ttu-id="52c17-120">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="52c17-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="52c17-121">切换“财务维度”部分的展开项。</span><span class="sxs-lookup"><span data-stu-id="52c17-121">Toggle the expansion of the Financial dimensions section.</span></span>
15. <span data-ttu-id="52c17-122">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="52c17-122">Click Edit.</span></span>
16. <span data-ttu-id="52c17-123">在“终端”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="52c17-123">In the Terminal field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="52c17-124">在列表中，查找并选择正在更新的收银机的维度值。</span><span class="sxs-lookup"><span data-stu-id="52c17-124">In the list, find and select the dimension value for the register being updated.</span></span>
18. <span data-ttu-id="52c17-125">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="52c17-125">Click Save.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]