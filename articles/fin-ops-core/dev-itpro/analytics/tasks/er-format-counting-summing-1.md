---
title: ER 配置格式以执行盘点和合计（第 1 部分 - 创建格式）
description: 本主题介绍如何配置电子报告格式以基于已经生成的文本输出的数据执行盘点和合计。 （第 1 部分）
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 64bf9f48319029e835f9e3fe2b888625100cc408
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565134"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-1---create-format"></a><span data-ttu-id="25436-104">ER 配置格式以执行盘点和合计（第 1 部分 - 创建格式）</span><span class="sxs-lookup"><span data-stu-id="25436-104">ER Configure format to do counting and summing (Part 1 - Create format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="25436-105">以下步骤介绍指定为系统管理或电子申报开发人员角色的用户如何配置电子申报 (ER) 格式，以便基于已生成的文本输出的数据执行盘点和合计。</span><span class="sxs-lookup"><span data-stu-id="25436-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="25436-106">这些步骤可以在任何公司执行。</span><span class="sxs-lookup"><span data-stu-id="25436-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="25436-107">为了完成这些步骤，您必须首先完成“创建配置提供商并标记为有效”这一过程中的步骤。</span><span class="sxs-lookup"><span data-stu-id="25436-107">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>

<span data-ttu-id="25436-108">此过程针对 Dynamics 365 for Operations 版本 1611 中增加的一项功能。</span><span class="sxs-lookup"><span data-stu-id="25436-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="25436-109">访问 Microsoft 提供的配置列表</span><span class="sxs-lookup"><span data-stu-id="25436-109">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="25436-110">转到“组织管理”>“工作区”>“电子申报”。</span><span class="sxs-lookup"><span data-stu-id="25436-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="25436-111">确保“Litware 公司”</span><span class="sxs-lookup"><span data-stu-id="25436-111">Make sure that the "Litware, Inc."</span></span> <span data-ttu-id="25436-112">提供程序可用且标记为有效。</span><span class="sxs-lookup"><span data-stu-id="25436-112">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="25436-113">选择“Litware 公司”</span><span class="sxs-lookup"><span data-stu-id="25436-113">Select the "Litware, Inc."</span></span> <span data-ttu-id="25436-114">提供程序。</span><span class="sxs-lookup"><span data-stu-id="25436-114">provider.</span></span>
3. <span data-ttu-id="25436-115">单击“存储库”。</span><span class="sxs-lookup"><span data-stu-id="25436-115">Click Repositories.</span></span>
    * <span data-ttu-id="25436-116">如果已存在“运营资源”的存储库，请跳过当前子任务的其余步骤。</span><span class="sxs-lookup"><span data-stu-id="25436-116">If a repository of the "Operations resources" type already exists, skip the remaining steps of the current sub-task.</span></span>  
4. <span data-ttu-id="25436-117">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="25436-117">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="25436-118">在“配置存储库类型”字段中，输入“运营资源”。</span><span class="sxs-lookup"><span data-stu-id="25436-118">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="25436-119">单击“创建存储库”。</span><span class="sxs-lookup"><span data-stu-id="25436-119">Click Create repository.</span></span>
7. <span data-ttu-id="25436-120">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="25436-120">Click OK.</span></span>

## <a name="get-the-intrastat-configurations-provided-by-microsoft"></a><span data-ttu-id="25436-121">获取 Microsoft 提供的内部统计配置</span><span class="sxs-lookup"><span data-stu-id="25436-121">Get the Intrastat configurations provided by Microsoft</span></span>
1. <span data-ttu-id="25436-122">单击“打开”。</span><span class="sxs-lookup"><span data-stu-id="25436-122">Click Open.</span></span>
2. <span data-ttu-id="25436-123">在树中，选择“内部统计模型\内部统计 (DE)”。</span><span class="sxs-lookup"><span data-stu-id="25436-123">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
3. <span data-ttu-id="25436-124">单击“导入”。</span><span class="sxs-lookup"><span data-stu-id="25436-124">Click Import.</span></span>
    * <span data-ttu-id="25436-125">单击所选配置的版本 1.1 的“导入”。</span><span class="sxs-lookup"><span data-stu-id="25436-125">Click Import for version 1.1 of the selected configuration.</span></span>  
4. <span data-ttu-id="25436-126">单击“是”。</span><span class="sxs-lookup"><span data-stu-id="25436-126">Click Yes.</span></span>
5. <span data-ttu-id="25436-127">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="25436-127">Close the page.</span></span>
6. <span data-ttu-id="25436-128">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="25436-128">Close the page.</span></span>
7. <span data-ttu-id="25436-129">单击“申报配置”。</span><span class="sxs-lookup"><span data-stu-id="25436-129">Click Reporting configurations.</span></span>
8. <span data-ttu-id="25436-130">在树中，展开“内部统计模型”。</span><span class="sxs-lookup"><span data-stu-id="25436-130">In the tree, expand 'Intrastat model'.</span></span>
9. <span data-ttu-id="25436-131">在树中，选择“内部统计模型\内部统计 (DE)”。</span><span class="sxs-lookup"><span data-stu-id="25436-131">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]