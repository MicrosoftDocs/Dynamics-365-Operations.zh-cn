--- 
title: "针对电子申报 (ER) 创建一个配置提供程序，并标记其为当前运行的"
description: "以下步骤说明了用户如何指派“系统管理员”或者“电子电子报表开发人员”为“电子申报 (ER)”新建一个配置提供程序。"
author: NickSelin
manager: AnnBe
ms.date: 10/18/2016
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: bdb3a3857a7293828a7766b6988c123a43e0673c
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-configuration-providand-mark-it-as-active-for-electronic-reporting-er"></a><span data-ttu-id="ef7c9-103">针对电子申报 (ER) 创建一个配置提供程序，并标记其为当前运行的</span><span class="sxs-lookup"><span data-stu-id="ef7c9-103">Create a configuration providand mark it as active for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ef7c9-104">以下步骤说明了用户如何指派“系统管理员”或者“电子电子报表开发人员”为“电子申报 (ER)”新建一个配置提供程序。</span><span class="sxs-lookup"><span data-stu-id="ef7c9-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can create a configuration provider for Electronic reporting (ER).</span></span> <span data-ttu-id="ef7c9-105">每个 ER 配置都将把该提供程序归类为其作者。</span><span class="sxs-lookup"><span data-stu-id="ef7c9-105">Each ER configuration will refer to the provider as the author of the configuration.</span></span> <span data-ttu-id="ef7c9-106">以样本公司 Litware，Inc. 为例，新建一个配置提供程序。这些步骤适用于所有公司，因为所有公司都共享 ER 配置提供程序。</span><span class="sxs-lookup"><span data-stu-id="ef7c9-106">In this example, you will create a configuration provider for sample company, Litware, Inc. These steps can be performed in any company as ER configuration providers are shared among all companies.</span></span>


## <a name="create-a-provider"></a><span data-ttu-id="ef7c9-107">新建一个提供程序</span><span class="sxs-lookup"><span data-stu-id="ef7c9-107">Create a provider</span></span>
1. <span data-ttu-id="ef7c9-108">转到“组织管理”>“工作区”>“电子申报”。</span><span class="sxs-lookup"><span data-stu-id="ef7c9-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="ef7c9-109">单击“配置提供程序”。</span><span class="sxs-lookup"><span data-stu-id="ef7c9-109">Click Configuration providers.</span></span>
3. <span data-ttu-id="ef7c9-110">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="ef7c9-110">Click New.</span></span>
    * <span data-ttu-id="ef7c9-111">提供程序具有唯一名称和 URL。</span><span class="sxs-lookup"><span data-stu-id="ef7c9-111">A provider record has a unique name and URL.</span></span> <span data-ttu-id="ef7c9-112">如果 Litware 公司的记录 (http://www.litware.com) 已存在，则查看此页内容并跳过此过程。</span><span class="sxs-lookup"><span data-stu-id="ef7c9-112">Review the content of this page and skip this procedure if a record for Litware, Inc. (http://www.litware.com) already exists.</span></span>  
4. <span data-ttu-id="ef7c9-113">在“名称”字段中，键入 'Litware, Inc.'。</span><span class="sxs-lookup"><span data-stu-id="ef7c9-113">In the Name field, type 'Litware, Inc.'.</span></span>
    * <span data-ttu-id="ef7c9-114">Litware 公司</span><span class="sxs-lookup"><span data-stu-id="ef7c9-114">Litware, Inc.</span></span>  
5. <span data-ttu-id="ef7c9-115">在“网址”字段中，键入 'http://www.litware.com'。</span><span class="sxs-lookup"><span data-stu-id="ef7c9-115">In the Internet address field, type 'http://www.litware.com'.</span></span>
    * <span data-ttu-id="ef7c9-116">http://www.litware.com</span><span class="sxs-lookup"><span data-stu-id="ef7c9-116">http://www.litware.com</span></span>  
6. <span data-ttu-id="ef7c9-117">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="ef7c9-117">Click Save.</span></span>
7. <span data-ttu-id="ef7c9-118">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="ef7c9-118">Close the page.</span></span>

## <a name="select-as-an-active-provider"></a><span data-ttu-id="ef7c9-119">选择为当前运行的提供程序</span><span class="sxs-lookup"><span data-stu-id="ef7c9-119">Select as an active provider</span></span>
1. <span data-ttu-id="ef7c9-120">选择 Litware 提供商。</span><span class="sxs-lookup"><span data-stu-id="ef7c9-120">Select the Litware, Inc. provider.</span></span>
2. <span data-ttu-id="ef7c9-121">单击“设置有效”。</span><span class="sxs-lookup"><span data-stu-id="ef7c9-121">Click Set active.</span></span>


