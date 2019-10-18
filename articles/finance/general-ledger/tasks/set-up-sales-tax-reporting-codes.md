---
title: 设置销售税申报代码
description: 销售税报表代码指销售税报表上的字段编号。
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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4751256858da417ec9bb1b7d9ccd16fb6bef1cac
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185926"
---
# <a name="set-up-sales-tax-reporting-codes"></a><span data-ttu-id="3eac1-103">设置销售税申报代码</span><span class="sxs-lookup"><span data-stu-id="3eac1-103">Set up sales tax reporting codes</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3eac1-104">销售税报表代码指销售税报表上的字段编号。</span><span class="sxs-lookup"><span data-stu-id="3eac1-104">The Sales tax reporting codes refer to a field number on a sales tax report.</span></span> <span data-ttu-id="3eac1-105">这些代码在国家特定的报表版式上使用，并且根据代码识别的销售税付款按照申报代码，申报打印一定结算期间内的销售税金额。</span><span class="sxs-lookup"><span data-stu-id="3eac1-105">They are used on country specific report layouts and the Sales tax payment by code report to print sales tax amounts for a settlement period summarized per reporting code.</span></span> <span data-ttu-id="3eac1-106">在创建销售税申报代码后，您可以在销售税代码页面的“报告设置”快速选项卡中引用这些代码。</span><span class="sxs-lookup"><span data-stu-id="3eac1-106">After you create Sales tax reporting codes, you can refer to them on the Report setup FastTabs in the Sales tax code page.</span></span> 

<span data-ttu-id="3eac1-107">此记录使用 DEMF 公司演示。</span><span class="sxs-lookup"><span data-stu-id="3eac1-107">This recording uses the DEMF demo company.</span></span>

1. <span data-ttu-id="3eac1-108">在**导航窗格**中，转到**纳税 > 设置 > 销售税 > 销售税申报代码**。</span><span class="sxs-lookup"><span data-stu-id="3eac1-108">In the **Navigation pane**, go to **Tax > Setup > Sales tax > Sales tax reporting codes**.</span></span>
2. <span data-ttu-id="3eac1-109">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="3eac1-109">Click **New**.</span></span>
3. <span data-ttu-id="3eac1-110">选择申报代码所属的报表版式。</span><span class="sxs-lookup"><span data-stu-id="3eac1-110">Select the report layout that the reporting code belongs to.</span></span> <span data-ttu-id="3eac1-111">此版式用于筛选销售税代码的可用申报代码。</span><span class="sxs-lookup"><span data-stu-id="3eac1-111">This layout is used to filter the available reporting codes for a Sales tax code.</span></span> <span data-ttu-id="3eac1-112">每个销售税代码属于使用报表版式的销售税主管机构的结算期间。</span><span class="sxs-lookup"><span data-stu-id="3eac1-112">Each Sales tax code belongs to a settlement period which belongs to a Sales tax authority which uses a Report layout.</span></span>  
4. <span data-ttu-id="3eac1-113">在**申报代码**字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="3eac1-113">In the **Reporting code** field, enter a number.</span></span>
5. <span data-ttu-id="3eac1-114">在**报表文本**字段中，输入在报表中显示的描述。</span><span class="sxs-lookup"><span data-stu-id="3eac1-114">In the **Report text** field, enter a description to display on reports.</span></span>
6. <span data-ttu-id="3eac1-115">在**简单描述**字段中，输入用于内部的描述。</span><span class="sxs-lookup"><span data-stu-id="3eac1-115">In the **Brief description** field, enter a description for internal purposes.</span></span>
7. <span data-ttu-id="3eac1-116">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="3eac1-116">Click **Save**.</span></span>

