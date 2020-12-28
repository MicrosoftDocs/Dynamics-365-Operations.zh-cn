---
title: 设置主科目类别
description: 本主题说明如何在 Dynamics 365 Finance 中设置主科目类别。
author: aprilolson
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MainAccountCategory, MainAccountCategoryLink
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9e0a015283064af2287013bccc065b4467a308c5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4440679"
---
# <a name="set-up-main-account-categories"></a><span data-ttu-id="3342d-103">设置主科目类别</span><span class="sxs-lookup"><span data-stu-id="3342d-103">Set up main account categories</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3342d-104">本主题说明如何设置主科目类别。</span><span class="sxs-lookup"><span data-stu-id="3342d-104">This topic explains how to set up main account categories.</span></span> <span data-ttu-id="3342d-105">主科目类别用于财务报表和 Power BI 中的默认报表。</span><span class="sxs-lookup"><span data-stu-id="3342d-105">Main account categories are used for the default reports in financial reporting and in Power BI.</span></span> <span data-ttu-id="3342d-106">默认创建的主科目类别可以重命名，但不可删除。</span><span class="sxs-lookup"><span data-stu-id="3342d-106">Main account categories that are created by default can be renamed but not deleted.</span></span> <span data-ttu-id="3342d-107">可创建其他科目类别，并用于报告和分析。</span><span class="sxs-lookup"><span data-stu-id="3342d-107">Additional account categories can be created and used for reporting and analysis purposes.</span></span> <span data-ttu-id="3342d-108">此主题使用演示公司 USMF。</span><span class="sxs-lookup"><span data-stu-id="3342d-108">This topic uses the USMF demo company.</span></span>

## <a name="create-a-main-account-category"></a><span data-ttu-id="3342d-109">创建主科目类别</span><span class="sxs-lookup"><span data-stu-id="3342d-109">Create a main account category</span></span>
1. <span data-ttu-id="3342d-110">在导航窗格中，转到 **模块 > 总帐 > 会计科目表 > 科目 > 主科目类别**。</span><span class="sxs-lookup"><span data-stu-id="3342d-110">In the navigation pane, go to **Modules > General Ledger > Chart of accounts > Accounts > Main account categories**.</span></span>
2. <span data-ttu-id="3342d-111">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="3342d-111">Select **New**.</span></span>
3. <span data-ttu-id="3342d-112">在 **主科目类别** 字段中，输入唯一的名称。</span><span class="sxs-lookup"><span data-stu-id="3342d-112">In the **Main account category** field, enter a unique name.</span></span>
4. <span data-ttu-id="3342d-113">在 **描述** 字段中，输入主科目类别的描述。</span><span class="sxs-lookup"><span data-stu-id="3342d-113">In the **Description field**, enter a description for the main account category.</span></span>
5. <span data-ttu-id="3342d-114">在 **主科目类型** 字段中，选择将链接到类别的主科目类型。</span><span class="sxs-lookup"><span data-stu-id="3342d-114">In the **Main account type** field, select the main account type that will be linked to the category.</span></span>

## <a name="link-main-accounts-to-account-category"></a><span data-ttu-id="3342d-115">链接主科目到科目类别</span><span class="sxs-lookup"><span data-stu-id="3342d-115">Link main accounts to account category</span></span>
1. <span data-ttu-id="3342d-116">单击 **链接主科目**。</span><span class="sxs-lookup"><span data-stu-id="3342d-116">Click **Link main accounts**.</span></span>
2. <span data-ttu-id="3342d-117">在列表中，通过单击 **已链接** 列中的框，选择要分配给主科目类别的主科目。</span><span class="sxs-lookup"><span data-stu-id="3342d-117">In the list, select the main accounts to assign to the main account category by checking the boxes in the **Linked** column.</span></span> <span data-ttu-id="3342d-118">在将类别用于财务报表和分析时，将主科目分配到该主科目类别将汇总科目余额。</span><span class="sxs-lookup"><span data-stu-id="3342d-118">Assigning main accounts to a main account category will aggregate the balances of the accounts when that category is used for financial reporting and analysis.</span></span>  
3. <span data-ttu-id="3342d-119">选择或取消选择 **已链接** 选项，以选择主科目。</span><span class="sxs-lookup"><span data-stu-id="3342d-119">Select or clear the **Linked** option to choose the main accounts.</span></span>
4. <span data-ttu-id="3342d-120">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="3342d-120">Select **OK**.</span></span>
5. <span data-ttu-id="3342d-121">选择 **是**。</span><span class="sxs-lookup"><span data-stu-id="3342d-121">Select **Yes**.</span></span>
