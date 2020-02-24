---
title: Dynamics 365 Talent（2020 年 1 月 7 日）中的新增功能或更改的功能
description: 本文介绍 Microsoft Dynamics 365 Talent 中的新增功能或更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-01-07
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e227c614fdbfe6f3dd410f1a533c593979abf1ec
ms.sourcegitcommit: 615ed3e4260192ba36826e128f1afa1588e94845
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/21/2020
ms.locfileid: "2974422"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-7-2020"></a><span data-ttu-id="2bc43-103">Dynamics 365 Talent（2020 年 1 月 7 日）中的新增功能或更改的功能</span><span class="sxs-lookup"><span data-stu-id="2bc43-103">What's new or changed in Dynamics 365 Talent (January 7, 2020)</span></span>

<span data-ttu-id="2bc43-104">本文介绍 Dynamics 365 Talent 中的新增功能或更改的功能。</span><span class="sxs-lookup"><span data-stu-id="2bc43-104">This article describes features that are either new or changed in Dynamics 365 Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="2bc43-105">Attract 中的更改</span><span class="sxs-lookup"><span data-stu-id="2bc43-105">Changes in Attract</span></span>

<span data-ttu-id="2bc43-106">本版本中包含 Dynamics 365 Talent: Attract 的小缺陷修复。</span><span class="sxs-lookup"><span data-stu-id="2bc43-106">This release includes minor bug fixes for Dynamics 365 Talent: Attract.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="2bc43-107">Onboard 中的更改</span><span class="sxs-lookup"><span data-stu-id="2bc43-107">Changes in Onboard</span></span>

<span data-ttu-id="2bc43-108">本版本中包含 Dynamics 365 Talent: Onboard 的小缺陷修复。</span><span class="sxs-lookup"><span data-stu-id="2bc43-108">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="2bc43-109">Core HR 中的更改</span><span class="sxs-lookup"><span data-stu-id="2bc43-109">Changes in Core HR</span></span>

<span data-ttu-id="2bc43-110">本部分中的更改适用于内部版本号 8.1.2697。</span><span class="sxs-lookup"><span data-stu-id="2bc43-110">Changes described in this section apply to build number 8.1.2697.</span></span> <span data-ttu-id="2bc43-111">某些标题中括号内的数字是 Microsoft Dynamics Lifecycle Services (LCS) 中的支持号码。</span><span class="sxs-lookup"><span data-stu-id="2bc43-111">The numbers in parentheses in some headings refer to support numbers in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

 
### <a name="cant-delete-workers-that-dont-have-employment-records---386157"></a><span data-ttu-id="2bc43-112">无法删除没有就业记录的工作人员 - (386157)</span><span class="sxs-lookup"><span data-stu-id="2bc43-112">Can't delete workers that don't have employment records - (386157)</span></span>

<span data-ttu-id="2bc43-113">此更改会在**失业工作人员**窗体中添加删除选项。</span><span class="sxs-lookup"><span data-stu-id="2bc43-113">This change adds a delete option in the **Workers without employment** form.</span></span> <span data-ttu-id="2bc43-114">当工作人员没有未来、当前或过去的工作时，此窗体中将出现工作人员。</span><span class="sxs-lookup"><span data-stu-id="2bc43-114">Workers appear in this form when no future, active, or historical employments exist for the worker.</span></span> <span data-ttu-id="2bc43-115">在此版本中，仅对系统管理员启用了删除功能。</span><span class="sxs-lookup"><span data-stu-id="2bc43-115">In this release, delete is only enabled for System Administrators.</span></span> <span data-ttu-id="2bc43-116">但是，在下周的版本中，安全性将得到更新，以允许具有 HR 助手角色的所有用户删除没有工作的工作人员。</span><span class="sxs-lookup"><span data-stu-id="2bc43-116">However, in next week's release, security will be updated to allow all users with the HR assistant role to remove employees without employments.</span></span> <span data-ttu-id="2bc43-117">您还可以按照以下步骤手动进行这些更改。</span><span class="sxs-lookup"><span data-stu-id="2bc43-117">You can also make these changes manually by following the following steps.</span></span>

1. <span data-ttu-id="2bc43-118">转到**安全配置**。</span><span class="sxs-lookup"><span data-stu-id="2bc43-118">Go to **Security configuration**.</span></span>
2. <span data-ttu-id="2bc43-119">在**特权**选项卡中，筛选**特权**列表以**维护工作人员**。</span><span class="sxs-lookup"><span data-stu-id="2bc43-119">In the **Privileges** tab, filter the **Privileges** list to **Maintain workers**.</span></span>
3. <span data-ttu-id="2bc43-120">在**参考**列中，选择**显示菜单项**。</span><span class="sxs-lookup"><span data-stu-id="2bc43-120">In the **References** column, select **Display menu items**.</span></span>
4. <span data-ttu-id="2bc43-121">在**显示菜单项**中，选择 **HcmWOrkersWithoutEmployment**。</span><span class="sxs-lookup"><span data-stu-id="2bc43-121">In **Display menu items**, select **HcmWOrkersWithoutEmployment**.</span></span>
5. <span data-ttu-id="2bc43-122">将**删除**权限设置为“授予”。</span><span class="sxs-lookup"><span data-stu-id="2bc43-122">Set the **Delete** permission to Grant.</span></span>
6. <span data-ttu-id="2bc43-123">选择**已取消发布的对象**选项卡。</span><span class="sxs-lookup"><span data-stu-id="2bc43-123">Select the **Unpublished objects** tab.</span></span>
7. <span data-ttu-id="2bc43-124">选择**全部发布**。</span><span class="sxs-lookup"><span data-stu-id="2bc43-124">Select **Publish all**.</span></span>
