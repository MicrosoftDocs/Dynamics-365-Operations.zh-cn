---
title: Dynamics 365 for Talent（2019 年 9 月 17 日）中的新增功能或更改
description: 此主题介绍了 Microsoft Dynamics 365 for Talent 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 9/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-09-17
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 97e55919309e3e95d21b4fdb14f913cf511280eb
ms.sourcegitcommit: f853c8d46ffc8e578387bac4cd48a948916983ef
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/19/2019
ms.locfileid: "2002565"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-september-17-2019"></a><span data-ttu-id="82262-103">Dynamics 365 for Talent（2019 年 9 月 17 日）中的新增功能或更改</span><span class="sxs-lookup"><span data-stu-id="82262-103">What's new or changed in Dynamics 365 for Talent (September 17, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="82262-104">此主题介绍了 Dynamics 365 for Talent 中的新增功能和更改的功能。</span><span class="sxs-lookup"><span data-stu-id="82262-104">This topic describes features that are either new or changed in Dynamics 365 for Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="82262-105">Attract 中的更改</span><span class="sxs-lookup"><span data-stu-id="82262-105">Changes in Attract</span></span>
<span data-ttu-id="82262-106">本版本中包含 Dynamics 365 Talent: Attract 的小缺陷修复。</span><span class="sxs-lookup"><span data-stu-id="82262-106">This release includes minor bug fixes for Dynamics 365 Talent: Attract.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="82262-107">Onboard 中的更改</span><span class="sxs-lookup"><span data-stu-id="82262-107">Changes in Onboard</span></span>
<span data-ttu-id="82262-108">本版本中包含 Dynamics 365 Talent: Onboard 的小缺陷修复。</span><span class="sxs-lookup"><span data-stu-id="82262-108">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="82262-109">Core HR 中的更改</span><span class="sxs-lookup"><span data-stu-id="82262-109">Changes in Core HR</span></span>
<span data-ttu-id="82262-110">本部分中的更改适用于内部版本号 8.1.2492。</span><span class="sxs-lookup"><span data-stu-id="82262-110">Changes described in this section apply to build number 8.1.2492.</span></span> <span data-ttu-id="82262-111">某些标题中括号内的数字是 Microsoft Dynamics Lifecycle Services (LCS) 中的支持号码。</span><span class="sxs-lookup"><span data-stu-id="82262-111">The numbers in parentheses in some headings refer to support numbers in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

### <a name="you-can-enable-preview-features-in-sandbox-and-trial-environments"></a><span data-ttu-id="82262-112">可以在沙盒和试用环境中启用预览功能。</span><span class="sxs-lookup"><span data-stu-id="82262-112">You can enable preview features in Sandbox and Trial environments</span></span>

<span data-ttu-id="82262-113">配置新的 Talent 实例时，可指定实例类型为生产还是沙盒。</span><span class="sxs-lookup"><span data-stu-id="82262-113">When you provision a new instance of Talent, you can specify whether the instance type is Production or Sandbox.</span></span> <span data-ttu-id="82262-114">沙盒类型的实例可用于提前试用新功能。</span><span class="sxs-lookup"><span data-stu-id="82262-114">Instances of the Sandbox type allow for early trial of new features.</span></span> <span data-ttu-id="82262-115">如果需要将现有实例之一更新为沙盒实例类型，请联系支持以发起更改请求。</span><span class="sxs-lookup"><span data-stu-id="82262-115">If you want one of your existing instances to be updated to the Sandbox instance type, contact Support to initiate the change request.</span></span>

<span data-ttu-id="82262-116">有关如何发布更改的详细信息，请参阅[配置 Talent](./provisioning-talent.md)。</span><span class="sxs-lookup"><span data-stu-id="82262-116">For more information about how changes are published, see [Provision Talent](./provisioning-talent.md).</span></span>

### <a name="human-resources-staff-cant-see-performance-review-details-once-assigned-to-them-by-workflow-370308"></a><span data-ttu-id="82262-117">人力资源员工无法查看工作流为其分配的绩效审核详细信息 (370308)</span><span class="sxs-lookup"><span data-stu-id="82262-117">Human Resources staff can't see performance review details once assigned to them by workflow (370308)</span></span>

<span data-ttu-id="82262-118">应用本周的更新之后，HR 专业人员可以查看已经通过工作流处理为其分配的绩效审核详细信息。</span><span class="sxs-lookup"><span data-stu-id="82262-118">With this week's update, HR professionals will be able to see performance review details that have been assigned to them through workflow processing.</span></span> <span data-ttu-id="82262-119">若要查看审核，请导航到**员工自助服务 > 分配给我的工作项**。</span><span class="sxs-lookup"><span data-stu-id="82262-119">To view reviews, navigate to **Employee self-service > Work items assigned to me**.</span></span>

### <a name="job-family-field-missing-in-the-manage-changes-page-for-job-details-346031"></a><span data-ttu-id="82262-120">缺少工作详细信息的“管理更改”页面中缺少工作系列字段 (346031)</span><span class="sxs-lookup"><span data-stu-id="82262-120">Job family field missing in the Manage changes page for job details (346031)</span></span>

<span data-ttu-id="82262-121">在此版本中，已向工作详细信息的**管理更改**页面添加了工作系列字段。</span><span class="sxs-lookup"><span data-stu-id="82262-121">In this release, the job family field has been added to the **Manage changes** page for job details.</span></span>

## <a name="in-preview"></a><span data-ttu-id="82262-122">预览模式</span><span class="sxs-lookup"><span data-stu-id="82262-122">In preview</span></span>

### <a name="streamlined-employee-entry-and-navigation"></a><span data-ttu-id="82262-123">简化的员工条目和导航</span><span class="sxs-lookup"><span data-stu-id="82262-123">Streamlined employee entry and navigation</span></span>

<span data-ttu-id="82262-124">此功能现在可在沙盒环境中使用。</span><span class="sxs-lookup"><span data-stu-id="82262-124">This functionality is now available in sandbox environments.</span></span> <span data-ttu-id="82262-125">要打开此功能，请导航至**系统管理 > 链接 > 设置 > 系统参数 > 预览功能**。</span><span class="sxs-lookup"><span data-stu-id="82262-125">To turn this feature on, navigate to **System administration > Links > Setup > System parameters > Preview features**.</span></span> <span data-ttu-id="82262-126">选择**增强的工作人员窗体和导航**。</span><span class="sxs-lookup"><span data-stu-id="82262-126">Select **Enhanced worker form and navigation**.</span></span> <span data-ttu-id="82262-127">这将为所有用户启用这些更改。</span><span class="sxs-lookup"><span data-stu-id="82262-127">This will enable these changes for all users.</span></span> <span data-ttu-id="82262-128">您可以随时关闭此选项。</span><span class="sxs-lookup"><span data-stu-id="82262-128">You can turn this option off at any time.</span></span>

<span data-ttu-id="82262-129">有关详细信息，请参阅[简化的员工输入和导航](./streamlined-employee-entry.md)。</span><span class="sxs-lookup"><span data-stu-id="82262-129">For more information, see [Streamlined employee entry and navigation](./streamlined-employee-entry.md).</span></span> <span data-ttu-id="82262-130">若要查看这些更改，请观看视频 [Dynamics 365 for Talent 2019 发布第 2 波概述](https://aka.ms/ROGT19RW2ROV)。</span><span class="sxs-lookup"><span data-stu-id="82262-130">To see the changes, watch the video [Dynamics 365 for Talent 2019 release wave 2 overview](https://aka.ms/ROGT19RW2ROV).</span></span>
