---
title: 设置主科目类别
description: 本主题说明如何在 Dynamics 365 for Finance and Operations 中设置主科目类别。
author: aprilolson
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MainAccountCategory, MainAccountCategoryLink
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4d37deb0bda225abb111375d8a00ae22d9e0c4fe
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916060"
---
# <a name="set-up-main-account-categories"></a><span data-ttu-id="b96de-103">设置主科目类别</span><span class="sxs-lookup"><span data-stu-id="b96de-103">Set up main account categories</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b96de-104">本主题说明如何在 Dynamics 365 for Finance and Operations 中设置主科目类别。</span><span class="sxs-lookup"><span data-stu-id="b96de-104">This topic explains how to set up main account categories in Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="b96de-105">主科目类别用于财务报表和 Power BI 中的默认报表。</span><span class="sxs-lookup"><span data-stu-id="b96de-105">Main account categories are used for the default reports in financial reporting and in Power BI.</span></span> <span data-ttu-id="b96de-106">默认创建的主科目类别可以重命名，但不可删除。</span><span class="sxs-lookup"><span data-stu-id="b96de-106">Main account categories that are created by default can be renamed but not deleted.</span></span> <span data-ttu-id="b96de-107">可创建其他科目类别，并用于报告和分析。</span><span class="sxs-lookup"><span data-stu-id="b96de-107">Additional account categories can be created and used for reporting and analysis purposes.</span></span> <span data-ttu-id="b96de-108">此主题使用演示公司 USMF。</span><span class="sxs-lookup"><span data-stu-id="b96de-108">This topic uses the USMF demo company.</span></span>

## <a name="create-a-main-account-category"></a><span data-ttu-id="b96de-109">创建主科目类别</span><span class="sxs-lookup"><span data-stu-id="b96de-109">Create a main account category</span></span>
1. <span data-ttu-id="b96de-110">在导航窗格中，转到**模块 > 总帐 > 会计科目表 > 科目 > 主科目类别**。</span><span class="sxs-lookup"><span data-stu-id="b96de-110">In the navigation pane, go to **Modules > General Ledger > Chart of accounts > Accounts > Main account categories**.</span></span>
2. <span data-ttu-id="b96de-111">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="b96de-111">Select **New**.</span></span>
3. <span data-ttu-id="b96de-112">在**主科目类别**字段中，输入唯一的名称。</span><span class="sxs-lookup"><span data-stu-id="b96de-112">In the **Main account category** field, enter a unique name.</span></span>
4. <span data-ttu-id="b96de-113">在**描述**字段中，输入主科目类别的描述。</span><span class="sxs-lookup"><span data-stu-id="b96de-113">In the **Description field**, enter a description for the main account category.</span></span>
5. <span data-ttu-id="b96de-114">在**主科目类型**字段中，选择将链接到类别的主科目类型。</span><span class="sxs-lookup"><span data-stu-id="b96de-114">In the **Main account type** field, select the main account type that will be linked to the category.</span></span>

## <a name="link-main-accounts-to-account-category"></a><span data-ttu-id="b96de-115">链接主科目到科目类别</span><span class="sxs-lookup"><span data-stu-id="b96de-115">Link main accounts to account category</span></span>
1. <span data-ttu-id="b96de-116">单击**链接主科目**。</span><span class="sxs-lookup"><span data-stu-id="b96de-116">Click **Link main accounts**.</span></span>
2. <span data-ttu-id="b96de-117">在列表中，通过单击**已链接**列中的框，选择要分配给主科目类别的主科目。</span><span class="sxs-lookup"><span data-stu-id="b96de-117">In the list, select the main accounts to assign to the main account category by checking the boxes in the **Linked** column.</span></span> <span data-ttu-id="b96de-118">在将类别用于财务报表和分析时，将主科目分配到该主科目类别将汇总科目余额。</span><span class="sxs-lookup"><span data-stu-id="b96de-118">Assigning main accounts to a main account category will aggregate the balances of the accounts when that category is used for financial reporting and analysis.</span></span>  
3. <span data-ttu-id="b96de-119">选择或取消选择**已链接**选项，以选择主科目。</span><span class="sxs-lookup"><span data-stu-id="b96de-119">Select or clear the **Linked** option to choose the main accounts.</span></span>
4. <span data-ttu-id="b96de-120">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="b96de-120">Select **OK**.</span></span>
5. <span data-ttu-id="b96de-121">选择**是**。</span><span class="sxs-lookup"><span data-stu-id="b96de-121">Select **Yes**.</span></span>
