--- 
title: "创建盘点和合计的格式"
description: "以下步骤介绍指定为系统管理或电子申报开发人员角色的用户如何配置电子申报 (ER) 格式，以便基于已生成的文本输出的数据执行盘点和合计。"
author: NickSelin
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: c20f2190e6480b6586d8102c489633d748d85a95
ms.contentlocale: zh-cn
ms.lasthandoff: 05/08/2018

---
# <a name="create-format-for-counting-and-summing"></a><span data-ttu-id="e4dd5-103">创建盘点和合计的格式</span><span class="sxs-lookup"><span data-stu-id="e4dd5-103">Create format for counting and summing</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e4dd5-104">以下步骤介绍指定为系统管理或电子申报开发人员角色的用户如何配置电子申报 (ER) 格式，以便基于已生成的文本输出的数据执行盘点和合计。</span><span class="sxs-lookup"><span data-stu-id="e4dd5-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="e4dd5-105">这些步骤可以在任何公司执行。</span><span class="sxs-lookup"><span data-stu-id="e4dd5-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="e4dd5-106">为了完成这些步骤，您必须首先完成“创建配置提供商并标记为有效”这一过程中的步骤。</span><span class="sxs-lookup"><span data-stu-id="e4dd5-106">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>

<span data-ttu-id="e4dd5-107">此过程针对 Dynamics 365 for Operations 版本 1611 中增加的一项功能。</span><span class="sxs-lookup"><span data-stu-id="e4dd5-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="e4dd5-108">访问 Microsoft 提供的配置列表</span><span class="sxs-lookup"><span data-stu-id="e4dd5-108">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="e4dd5-109">转到“组织管理”>“工作区”>“电子申报”。</span><span class="sxs-lookup"><span data-stu-id="e4dd5-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="e4dd5-110">确保“Litware 公司”</span><span class="sxs-lookup"><span data-stu-id="e4dd5-110">Make sure that the “Litware, Inc.”</span></span> <span data-ttu-id="e4dd5-111">提供程序可用且标记为有效。</span><span class="sxs-lookup"><span data-stu-id="e4dd5-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="e4dd5-112">选择“Litware 公司”</span><span class="sxs-lookup"><span data-stu-id="e4dd5-112">Select the “Litware, Inc.”</span></span> <span data-ttu-id="e4dd5-113">提供程序。</span><span class="sxs-lookup"><span data-stu-id="e4dd5-113">provider.</span></span>
3. <span data-ttu-id="e4dd5-114">单击“存储库”。</span><span class="sxs-lookup"><span data-stu-id="e4dd5-114">Click Repositories.</span></span>
    * <span data-ttu-id="e4dd5-115">如果已存在“运营资源”的存储库，请跳过当前子任务的其余步骤。</span><span class="sxs-lookup"><span data-stu-id="e4dd5-115">If a repository of the "Operations resources" type already exists, skip the remaining steps of the current sub-task.</span></span>  
4. <span data-ttu-id="e4dd5-116">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="e4dd5-116">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="e4dd5-117">在“配置存储库类型”字段中，输入“运营资源”。</span><span class="sxs-lookup"><span data-stu-id="e4dd5-117">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="e4dd5-118">单击“创建存储库”。</span><span class="sxs-lookup"><span data-stu-id="e4dd5-118">Click Create repository.</span></span>
7. <span data-ttu-id="e4dd5-119">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="e4dd5-119">Click OK.</span></span>

## <a name="get-the-intrastat-configurations-provided-by-microsoft"></a><span data-ttu-id="e4dd5-120">获取 Microsoft 提供的内部统计配置</span><span class="sxs-lookup"><span data-stu-id="e4dd5-120">Get the Intrastat configurations provided by Microsoft</span></span>
1. <span data-ttu-id="e4dd5-121">单击“打开”。</span><span class="sxs-lookup"><span data-stu-id="e4dd5-121">Click Open.</span></span>
2. <span data-ttu-id="e4dd5-122">在树中，选择“内部统计模型\内部统计 (DE)”。</span><span class="sxs-lookup"><span data-stu-id="e4dd5-122">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
3. <span data-ttu-id="e4dd5-123">单击“导入”。</span><span class="sxs-lookup"><span data-stu-id="e4dd5-123">Click Import.</span></span>
    * <span data-ttu-id="e4dd5-124">单击所选配置的版本 1.1 的“导入”。</span><span class="sxs-lookup"><span data-stu-id="e4dd5-124">Click Import for version 1.1 of the selected configuration.</span></span>  
4. <span data-ttu-id="e4dd5-125">单击“是”。</span><span class="sxs-lookup"><span data-stu-id="e4dd5-125">Click Yes.</span></span>
5. <span data-ttu-id="e4dd5-126">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="e4dd5-126">Close the page.</span></span>
6. <span data-ttu-id="e4dd5-127">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="e4dd5-127">Close the page.</span></span>
7. <span data-ttu-id="e4dd5-128">单击“申报配置”。</span><span class="sxs-lookup"><span data-stu-id="e4dd5-128">Click Reporting configurations.</span></span>
8. <span data-ttu-id="e4dd5-129">在树中，展开“内部统计模型”。</span><span class="sxs-lookup"><span data-stu-id="e4dd5-129">In the tree, expand 'Intrastat model'.</span></span>
9. <span data-ttu-id="e4dd5-130">在树中，选择“内部统计模型\内部统计 (DE)”。</span><span class="sxs-lookup"><span data-stu-id="e4dd5-130">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>


