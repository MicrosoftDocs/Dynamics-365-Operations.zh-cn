---
title: 创建配置提供程序并标记为当前运行的
description: 以下步骤说明了用户如何指派“系统管理员”或者“电子电子报表开发人员”为“电子申报 (ER)”新建一个配置提供程序。
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERVendorTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 13a27c2fec2a2b226e9ae8d5b8f9a61e8b79ceb0
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "362226"
---
# <a name="create-configuration-providers-and-mark-them-as-active"></a><span data-ttu-id="e1149-103">创建配置提供程序并标记为当前运行的</span><span class="sxs-lookup"><span data-stu-id="e1149-103">Create configuration providers and mark them as active</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e1149-104">以下步骤说明了用户如何指派“系统管理员”或者“电子电子报表开发人员”为“电子申报 (ER)”新建一个配置提供程序。</span><span class="sxs-lookup"><span data-stu-id="e1149-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can create a configuration provider for Electronic reporting (ER).</span></span> <span data-ttu-id="e1149-105">每个 ER 配置都将把该提供程序归类为其作者。</span><span class="sxs-lookup"><span data-stu-id="e1149-105">Each ER configuration will refer to the provider as the author of the configuration.</span></span> <span data-ttu-id="e1149-106">以样本公司 Litware，Inc. 为例，新建一个配置提供程序。这些步骤适用于所有公司，因为所有公司都共享 ER 配置提供程序。</span><span class="sxs-lookup"><span data-stu-id="e1149-106">In this example, you will create a configuration provider for sample company, Litware, Inc. These steps can be performed in any company as ER configuration providers are shared among all companies.</span></span>


## <a name="create-a-provider"></a><span data-ttu-id="e1149-107">新建一个提供程序</span><span class="sxs-lookup"><span data-stu-id="e1149-107">Create a provider</span></span>
1. <span data-ttu-id="e1149-108">转到“组织管理”>“工作区”>“电子申报”。</span><span class="sxs-lookup"><span data-stu-id="e1149-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="e1149-109">单击“配置提供程序”。</span><span class="sxs-lookup"><span data-stu-id="e1149-109">Click Configuration providers.</span></span>
3. <span data-ttu-id="e1149-110">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="e1149-110">Click New.</span></span>
    * <span data-ttu-id="e1149-111">提供程序具有唯一名称和 URL。</span><span class="sxs-lookup"><span data-stu-id="e1149-111">A provider record has a unique name and URL.</span></span> <span data-ttu-id="e1149-112">如果已存在 Litware 公司 (http://www.litware.com) 的记录，则查看此页内容并跳过此步骤。</span><span class="sxs-lookup"><span data-stu-id="e1149-112">Review the content of this page and skip this procedure if a record for Litware, Inc. (http://www.litware.com) already exists.</span></span>  
4. <span data-ttu-id="e1149-113">在“名称”字段中，键入 'Litware, Inc.'。</span><span class="sxs-lookup"><span data-stu-id="e1149-113">In the Name field, type 'Litware, Inc.'.</span></span>
    * <span data-ttu-id="e1149-114">Litware 公司</span><span class="sxs-lookup"><span data-stu-id="e1149-114">Litware, Inc.</span></span>  
5. <span data-ttu-id="e1149-115">在”Internet 地址“字段中，键入“http://www.litware.com”。</span><span class="sxs-lookup"><span data-stu-id="e1149-115">In the Internet address field, type 'http://www.litware.com'.</span></span>
    * http://www.litware.com  
6. <span data-ttu-id="e1149-116">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="e1149-116">Click Save.</span></span>
7. <span data-ttu-id="e1149-117">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="e1149-117">Close the page.</span></span>

## <a name="select-as-an-active-provider"></a><span data-ttu-id="e1149-118">选择为当前运行的提供程序</span><span class="sxs-lookup"><span data-stu-id="e1149-118">Select as an active provider</span></span>
1. <span data-ttu-id="e1149-119">选择 Litware 提供商。</span><span class="sxs-lookup"><span data-stu-id="e1149-119">Select the Litware, Inc. provider.</span></span>
2. <span data-ttu-id="e1149-120">单击“设置有效”。</span><span class="sxs-lookup"><span data-stu-id="e1149-120">Click Set active.</span></span>

