---
title: (ER) 从 RCS 导入配置
description: 本主题介绍用户如何从 RCS 导入 ER 配置的新版本。
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ea2bfd2514be666d05165410ca27041a86464715
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143215"
---
# <a name="er-import-configurations-from-rcs"></a><span data-ttu-id="49daa-103">(ER) 从 RCS 导入配置</span><span class="sxs-lookup"><span data-stu-id="49daa-103">(ER) Import configurations from RCS</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="49daa-104">以下步骤说明系统管理员或电子报表开发人员角色的用户可如何从 Microsoft Regulatory Configuration Services (RCS) 导入新电子申报 (ER) 配置版本。</span><span class="sxs-lookup"><span data-stu-id="49daa-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can import a new version of an Electronic reporting (ER) configuration from Microsoft Regulatory Configuration Services (RCS).</span></span> <span data-ttu-id="49daa-105">在此示例中，将选择 RCS 中已配置的 ER 配置版本，并将其导入示例公司 Litware, Inc. 的当前实例。可以在任何公司执行这些步骤，因为公司共享 ER 配置。</span><span class="sxs-lookup"><span data-stu-id="49daa-105">In this example, you will select the version of the ER configuration that has been configured in an RCS instance and import it into the current instance for sample company, Litware, Inc. These steps can be performed in any company because ER configurations are shared among companies.</span></span> <span data-ttu-id="49daa-106">为了完成这些步骤，您必须首先完成[创建配置提供程序并标记为当前运行的](er-configuration-provider-mark-it-active-2016-11.md)主题中的步骤。</span><span class="sxs-lookup"><span data-stu-id="49daa-106">To complete these steps, you must first complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="49daa-107">若要完成这些步骤，还必须可以访问其中包含至少一个状态为**已完成**或**共享**的 ER 配置的 RCS 实例。</span><span class="sxs-lookup"><span data-stu-id="49daa-107">To complete these steps, you must also have access to an RCS instance containing at least one ER configuration in either **Completed** or **Shared** status.</span></span>

1. <span data-ttu-id="49daa-108">转到**组织管理** > **工作区** > **电子申报**。</span><span class="sxs-lookup"><span data-stu-id="49daa-108">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span> 
2. <span data-ttu-id="49daa-109">确保示例公司 Litware 公司的配置提供程序可用且标记为**有效**。</span><span class="sxs-lookup"><span data-stu-id="49daa-109">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="49daa-110">如果没有看到此配置提供程序，请首先完成[创建配置提供程序并标记为当前运行的](er-configuration-provider-mark-it-active-2016-11.md)这一主题中的步骤。</span><span class="sxs-lookup"><span data-stu-id="49daa-110">If you don't see this configuration provider, complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 
3. <span data-ttu-id="49daa-111">如果没有为公司设置 RCS 环境，请单击 **Regulatory services – 配置**外部链接，然后按照说明设置 RCS 环境。</span><span class="sxs-lookup"><span data-stu-id="49daa-111">If you have no RCS environment provisioned to your company, click **Regulatory services – Configuration** external link and follow the instructions to provision an RCS environment.</span></span> 
4. <span data-ttu-id="49daa-112">单击**电子申报参数**。</span><span class="sxs-lookup"><span data-stu-id="49daa-112">Click **Electronic reporting parameters**.</span></span> 
5. <span data-ttu-id="49daa-113">单击 **RCS** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="49daa-113">Click the **RCS** tab.</span></span> 
6. <span data-ttu-id="49daa-114">如果已经为您的公司设置了 RCS 环境，请使用页面中提供的 URL 访问。</span><span class="sxs-lookup"><span data-stu-id="49daa-114">If RCS environment has been already provisioned to your company, use presented on the page URLs to access it.</span></span> 
7. <span data-ttu-id="49daa-115">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="49daa-115">Close the page.</span></span> 

## <a name="register-a-new-er-repository"></a><span data-ttu-id="49daa-116">注册新的 ER 存储库。</span><span class="sxs-lookup"><span data-stu-id="49daa-116">Register a new ER repository.</span></span> 
1. <span data-ttu-id="49daa-117">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="49daa-117">In the list, mark the selected row.</span></span> 
2. <span data-ttu-id="49daa-118">选择 Litware, Inc. 提供商。</span><span class="sxs-lookup"><span data-stu-id="49daa-118">Select Litware, Inc. provider.</span></span> 
3. <span data-ttu-id="49daa-119">单击“存储库”。</span><span class="sxs-lookup"><span data-stu-id="49daa-119">Click Repositories.</span></span> 
4. <span data-ttu-id="49daa-120">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="49daa-120">Click Add to open the drop dialog.</span></span> 
5. <span data-ttu-id="49daa-121">在“配置存储库类型”字段中，输入”RCS“。</span><span class="sxs-lookup"><span data-stu-id="49daa-121">In the Configuration repository type field, enter 'RCS'.</span></span> 
6. <span data-ttu-id="49daa-122">单击“创建存储库”。</span><span class="sxs-lookup"><span data-stu-id="49daa-122">Click Create repository.</span></span> 
7. <span data-ttu-id="49daa-123">在 RCS 环境显示名称字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="49daa-123">In the RCS environment display name field, enter or select a value.</span></span> 
8. <span data-ttu-id="49daa-124">选择所需的 RCS 实例。</span><span class="sxs-lookup"><span data-stu-id="49daa-124">Select the desired RCS instance.</span></span> <span data-ttu-id="49daa-125">请注意，可以选择多个。</span><span class="sxs-lookup"><span data-stu-id="49daa-125">Note that you can have several of them.</span></span> 
9. <span data-ttu-id="49daa-126">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="49daa-126">Click OK.</span></span> 

## <a name="import-er-configurations-from-rcs-based-repository"></a><span data-ttu-id="49daa-127">从基于 RCS 的存储库导入 ER 配置</span><span class="sxs-lookup"><span data-stu-id="49daa-127">Import ER configurations from RCS based repository</span></span>
1. <span data-ttu-id="49daa-128">单击**显示筛选器**。</span><span class="sxs-lookup"><span data-stu-id="49daa-128">Click **Show filters**.</span></span> 
2. <span data-ttu-id="49daa-129">使用**开头为**筛选器运算符在**名称**字段中输入筛选器值”RCS“。</span><span class="sxs-lookup"><span data-stu-id="49daa-129">Enter a filter value of "RCS" on the **Name** field using the **begins with** filter operator.</span></span> 
3. <span data-ttu-id="49daa-130">打开所选存储库时，在**连接 Regulatory Configuration Services** 页上，单击**单击此处连接 Regulatory Configuration Services** 链接。</span><span class="sxs-lookup"><span data-stu-id="49daa-130">When you open the selected repository, on the **Connect to Regulatory Configuration Services** page, click **Click here to connect to Regulatory Configuration Services** link.</span></span> 
4. <span data-ttu-id="49daa-131">单击**打开**。</span><span class="sxs-lookup"><span data-stu-id="49daa-131">Click **Open**.</span></span> 
5. <span data-ttu-id="49daa-132">单击**关闭**。</span><span class="sxs-lookup"><span data-stu-id="49daa-132">Click **Close**.</span></span> 
6. <span data-ttu-id="49daa-133">选择所需 ER 配置版本，然后单击**导入**将其导入到当前实例中。</span><span class="sxs-lookup"><span data-stu-id="49daa-133">Select the desired version of ER configuration and click **Import** to bring it in the current instance.</span></span>

