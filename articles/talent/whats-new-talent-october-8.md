---
title: Dynamics 365 for Talent Core HR（2018 年 10 月 1 日）中的新增功能或更改
description: 此主题介绍了 Microsoft Dynamics 365 for Talent Core HR 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 10/07/2018
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
ms.search.validFrom: 2018-10-07
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 92eb1508905309294e17b770829b1c5a22be1316
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "303461"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-october-8-2018"></a><span data-ttu-id="0180b-103">Dynamics 365 for Talent Core HR（2018 年 10 月 8 日）中的新增功能或更改</span><span class="sxs-lookup"><span data-stu-id="0180b-103">What's new or changed in Dynamics 365 for Talent Core HR (October 8, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0180b-104">**内部版本 8.1.1050.0**</span><span class="sxs-lookup"><span data-stu-id="0180b-104">**Build 8.1.1050.0**</span></span>

<span data-ttu-id="0180b-105">此主题介绍了 Core HR 中的新增功能和更改的功能。</span><span class="sxs-lookup"><span data-stu-id="0180b-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="allow-other-dates-to-be-used-on-leave-tier-basis-leave-management"></a><span data-ttu-id="0180b-106">允许要在休假层基础使用的其他日期（休假管理）</span><span class="sxs-lookup"><span data-stu-id="0180b-106">Allow other dates to be used on leave tier basis (Leave Management)</span></span>

<span data-ttu-id="0180b-107">在向员工奖励休假时，奖励层基础确定员工应计的休假时间。</span><span class="sxs-lookup"><span data-stu-id="0180b-107">When awarding leave to employees, the award tier basis determines how much time off an employee accrues.</span></span> <span data-ttu-id="0180b-108">目前，这些层基于员工开始日期和受聘日期。</span><span class="sxs-lookup"><span data-stu-id="0180b-108">Currently, these tiers are based on employee start date and seniority date.</span></span> <span data-ttu-id="0180b-109">在某些情况下，组织需要这些层基于其他日期，如周年纪念日日期或原始雇用日期。</span><span class="sxs-lookup"><span data-stu-id="0180b-109">In some scenarios, organizations need these tiers to be based on other dates, like anniversary date or original hire date.</span></span> <span data-ttu-id="0180b-110">这些日期已用于休假计划来确定应计何时发生，当员工在计划中登记时使用这些相同日期的功能已添加以确定应计金额。</span><span class="sxs-lookup"><span data-stu-id="0180b-110">These dates are already used on the leave plan to determine when accruals happen, the ability for these same dates to be used when an employee is enrolled in a plan have been added to determine the accrual amount.</span></span> 

## <a name="other-changes"></a><span data-ttu-id="0180b-111">其他更改</span><span class="sxs-lookup"><span data-stu-id="0180b-111">Other changes</span></span>
<span data-ttu-id="0180b-112">杂项修复已包含在此版本中。</span><span class="sxs-lookup"><span data-stu-id="0180b-112">Miscellanous fixes have been included in this release.</span></span>

## <a name="known-issue"></a><span data-ttu-id="0180b-113">已知问题</span><span class="sxs-lookup"><span data-stu-id="0180b-113">Known issue</span></span>

<span data-ttu-id="0180b-114">**问题：** 向工作人员添加新附件时，**新建**和**编辑**按钮灰显。**解决方法：** 打开附件页面之前，确保已关闭**工作人员**页面中的速见表。</span><span class="sxs-lookup"><span data-stu-id="0180b-114">**Issue:** When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out. **Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="0180b-115">如果加载**工作人员**页面时速见表已关闭，将启用附件按钮。</span><span class="sxs-lookup"><span data-stu-id="0180b-115">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="0180b-116">（下一个平台更新中将解决这个问题。）</span><span class="sxs-lookup"><span data-stu-id="0180b-116">(This issue will be fixed in the next platform update.)</span></span>
