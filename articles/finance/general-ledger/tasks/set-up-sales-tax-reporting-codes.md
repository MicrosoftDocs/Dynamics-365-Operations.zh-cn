---
title: 设置销售税申报代码
description: 销售税报表代码指销售税报表上列出的字段编号。
author: twheeloc
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxReportCollection
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: be24e18da63d1a613c3c6e72f7c767c7af9b6656
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222135"
---
# <a name="set-up-sales-tax-reporting-codes"></a><span data-ttu-id="89aa9-103">设置销售税申报代码</span><span class="sxs-lookup"><span data-stu-id="89aa9-103">Set up sales tax reporting codes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="89aa9-104">销售税报表代码指销售税报表上列出的字段编号。</span><span class="sxs-lookup"><span data-stu-id="89aa9-104">The Sales tax reporting codes refer to a field number that's listed on a sales tax report.</span></span> <span data-ttu-id="89aa9-105">它们用于国家/地区特定的报表布局。</span><span class="sxs-lookup"><span data-stu-id="89aa9-105">They are used on country-specific report layouts.</span></span> <span data-ttu-id="89aa9-106">也用于按代码报告打印增值税支付。</span><span class="sxs-lookup"><span data-stu-id="89aa9-106">They're also used on the Sales tax payment by code report.</span></span> <span data-ttu-id="89aa9-107">该报表显示为每个申报代码汇总的结算期的销售税金额。</span><span class="sxs-lookup"><span data-stu-id="89aa9-107">That report shows sales tax amounts for a settlement period summarized for each reporting code.</span></span> <span data-ttu-id="89aa9-108">在创建销售税申报代码后，您可以在销售税代码页面的“报告设置”快速选项卡（可以从 **销售税代码** 访问该快速选项卡）中引用这些代码。</span><span class="sxs-lookup"><span data-stu-id="89aa9-108">After you create Sales tax reporting codes, you can refer to those codes on the Report setup FastTabs, which you can access from the **Sales tax code** page.</span></span> 

<span data-ttu-id="89aa9-109">此记录使用 DEMF 公司演示。</span><span class="sxs-lookup"><span data-stu-id="89aa9-109">This recording uses the DEMF demo company.</span></span>

1. <span data-ttu-id="89aa9-110">在 **导航窗格** 中，转到 **纳税 > 设置 > 销售税 > 销售税申报代码**。</span><span class="sxs-lookup"><span data-stu-id="89aa9-110">In the **Navigation pane**, go to **Tax > Setup > Sales tax > Sales tax reporting codes**.</span></span>
2. <span data-ttu-id="89aa9-111">单击 **新建**。</span><span class="sxs-lookup"><span data-stu-id="89aa9-111">Click **New**.</span></span>
3. <span data-ttu-id="89aa9-112">选择申报代码所属的报表版式。</span><span class="sxs-lookup"><span data-stu-id="89aa9-112">Select the report layout that the reporting code belongs to.</span></span> <span data-ttu-id="89aa9-113">此版式用于筛选销售税代码的可用申报代码。</span><span class="sxs-lookup"><span data-stu-id="89aa9-113">This layout is used to filter the available reporting codes for a sales tax code.</span></span> <span data-ttu-id="89aa9-114">每个销售税代码属于使用报表版式的销售税主管机构的结算期间。</span><span class="sxs-lookup"><span data-stu-id="89aa9-114">Each sales tax code belongs to a settlement period, which belongs to a Sales tax authority, which uses a report layout.</span></span>  
4. <span data-ttu-id="89aa9-115">在 **申报代码** 字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="89aa9-115">In the **Reporting code** field, enter a number.</span></span>
5. <span data-ttu-id="89aa9-116">在 **报表文本** 字段中，输入在报表中显示的描述。</span><span class="sxs-lookup"><span data-stu-id="89aa9-116">In the **Report text** field, enter a description to display on reports.</span></span>
6. <span data-ttu-id="89aa9-117">在 **简单描述** 字段中，输入用于内部的描述。</span><span class="sxs-lookup"><span data-stu-id="89aa9-117">In the **Brief description** field, enter a description for internal purposes.</span></span>
7. <span data-ttu-id="89aa9-118">单击 **保存**。</span><span class="sxs-lookup"><span data-stu-id="89aa9-118">Click **Save**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]