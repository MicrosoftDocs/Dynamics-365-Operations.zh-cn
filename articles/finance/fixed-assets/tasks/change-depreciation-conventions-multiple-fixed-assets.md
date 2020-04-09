---
title: 更改多项固定资产的折旧惯例
description: 此任务更新特定固定资产组的折旧惯例。
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysQueryForm, SrsReportViewerForm
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 39930134782b40de05a92a6ad51c4f628f304a78
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142884"
---
# <a name="change-depreciation-conventions-for-multiple-fixed-assets"></a><span data-ttu-id="6737e-103">更改多项固定资产的折旧惯例</span><span class="sxs-lookup"><span data-stu-id="6737e-103">Change depreciation conventions for multiple fixed assets</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6737e-104">此任务更新特定固定资产组的折旧惯例。</span><span class="sxs-lookup"><span data-stu-id="6737e-104">This task updates the depreciation convention for a specified fixed asset group.</span></span> <span data-ttu-id="6737e-105">此任务指南使用 USMF 公司演示。</span><span class="sxs-lookup"><span data-stu-id="6737e-105">This task guide uses the USMF demo company.</span></span>

1. <span data-ttu-id="6737e-106">转到“固定资产”>“定期任务”>“成批更新”</span><span class="sxs-lookup"><span data-stu-id="6737e-106">Go to Fixed assets > Periodic tasks > Mass update</span></span>
2. <span data-ttu-id="6737e-107">在“折旧帐簿”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="6737e-107">In the Depreciation book field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="6737e-108">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="6737e-108">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="6737e-109">在“开始投入使用”字段，输入日期。</span><span class="sxs-lookup"><span data-stu-id="6737e-109">In the Placed in service start field, enter a date.</span></span>
5. <span data-ttu-id="6737e-110">在“投入使用结束”字段，输入日期。</span><span class="sxs-lookup"><span data-stu-id="6737e-110">In the Placed in service end field, enter a date.</span></span>
    * <span data-ttu-id="6737e-111">仅所选折旧帐簿中的且在该等日期之间投入使用的资产才会更新。</span><span class="sxs-lookup"><span data-stu-id="6737e-111">Only assets that are a part of the select depreciation book and that have been placed in service between these dates will be updated.</span></span>  
6. <span data-ttu-id="6737e-112">在“当前折旧惯例”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="6737e-112">In the Current depreciation convention field, select an option.</span></span>
    * <span data-ttu-id="6737e-113">仅属于当前折旧惯例的资产才会更新。</span><span class="sxs-lookup"><span data-stu-id="6737e-113">Only assets that have the current depreciation convention will be updated.</span></span>  
7. <span data-ttu-id="6737e-114">在“新折旧惯例”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="6737e-114">In the New depreciation convention field, select an option.</span></span>
    * <span data-ttu-id="6737e-115">验证报表将打印给所选目标。</span><span class="sxs-lookup"><span data-stu-id="6737e-115">Verify the report will print to the desired destination.</span></span>  
8. <span data-ttu-id="6737e-116">扩展“要包括的记录”部分。</span><span class="sxs-lookup"><span data-stu-id="6737e-116">Expand the Records to include section.</span></span>
9. <span data-ttu-id="6737e-117">单击“筛选器”。</span><span class="sxs-lookup"><span data-stu-id="6737e-117">Click Filter.</span></span>
10. <span data-ttu-id="6737e-118">在列表中选择固定资产组。</span><span class="sxs-lookup"><span data-stu-id="6737e-118">In the list, select the Fixed asset group.</span></span>
11. <span data-ttu-id="6737e-119">在“标准”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="6737e-119">In the Criteria field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="6737e-120">选择期望的固定资产组。</span><span class="sxs-lookup"><span data-stu-id="6737e-120">Select the desired Fixed asset group.</span></span>
13. <span data-ttu-id="6737e-121">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="6737e-121">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="6737e-122">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="6737e-122">Click OK.</span></span>
15. <span data-ttu-id="6737e-123">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="6737e-123">Click OK.</span></span>
    *  <span data-ttu-id="6737e-124">流程结果将在成批更新报表中显示。</span><span class="sxs-lookup"><span data-stu-id="6737e-124">Results of the process are shown on the Mass update report.</span></span>     

