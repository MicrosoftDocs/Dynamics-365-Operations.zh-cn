---
title: Dynamics 365 for Talent Core HR（2018 年 11 月 27 日）中的新增功能或更改
description: 此主题介绍了 Microsoft Dynamics 365 for Talent Core HR 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 11/27/2018
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
ms.search.validFrom: 2018-11-27
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 81ea0e4f4878d1967234c597504071ce464a22c5
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/19/2019
ms.locfileid: "857791"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-november-27-2018"></a><span data-ttu-id="06894-103">Dynamics 365 for Talent Core HR（2018 年 11 月 27 日）中的新增功能或更改</span><span class="sxs-lookup"><span data-stu-id="06894-103">What's new or changed in Dynamics 365 for Talent Core HR (November 27, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="06894-104">**内部版本 8.1.2064**</span><span class="sxs-lookup"><span data-stu-id="06894-104">**Build 8.1.2064**</span></span>

<span data-ttu-id="06894-105">此主题介绍了 Core HR 中的新增功能和更改的功能。</span><span class="sxs-lookup"><span data-stu-id="06894-105">This topic describes features that are either new or changed in Core HR.</span></span>


## <a name="changes"></a><span data-ttu-id="06894-106">更改</span><span class="sxs-lookup"><span data-stu-id="06894-106">Changes</span></span>

### <a name="unable-to-create-a-note-in-case-management"></a><span data-ttu-id="06894-107">无法在“案例管理”中创建注释</span><span class="sxs-lookup"><span data-stu-id="06894-107">Unable to create a note in Case Management</span></span>

<span data-ttu-id="06894-108">已进行了更改来解决当尝试在“案例管理”的案例日志中编辑或创建注释时出现的问题。</span><span class="sxs-lookup"><span data-stu-id="06894-108">A change has been made for an issue when attempting to edit or create a note in the case log of Case Management.</span></span>

### <a name="misspelled-word-on-the-analytics-tab-in-the-compensation-workspace"></a><span data-ttu-id="06894-109">薪酬工作区中分析选项卡上拼写错误的字词</span><span class="sxs-lookup"><span data-stu-id="06894-109">Misspelled word on the analytics tab in the compensation workspace</span></span> 

<span data-ttu-id="06894-110">已进行了更改来更正薪酬工作区中薪酬分析图表中“所属种族”的拼写。</span><span class="sxs-lookup"><span data-stu-id="06894-110">A change has been made to correct the spelling of 'Ethnic Origin' in the compensation analytics chart in the compensation workspace.</span></span>

### <a name="employee-self-service-workspace-not-displaying-when-a-user-isnt-assigned-to-a-worker"></a><span data-ttu-id="06894-111">员工自助服务工作区在用户未分配给工作人员时不显示</span><span class="sxs-lookup"><span data-stu-id="06894-111">Employee self-service workspace not displaying when a user isn't assigned to a worker</span></span> 

<span data-ttu-id="06894-112">已对当**员工自助服务**工作区在启动时被选择为分配给工作人员的用户的初始页面进行了更改。</span><span class="sxs-lookup"><span data-stu-id="06894-112">A change has been made when the **Employee self-service** workspace is selected as the initial page on startup for a user who is not assigned to a worker.</span></span> <span data-ttu-id="06894-113">在此情况下，默认仪表板将显示。</span><span class="sxs-lookup"><span data-stu-id="06894-113">In this situation, the default dashboard will be displayed.</span></span>

### <a name="leave-and-absence-error-object-reference-not-set-to-an-instance-of-an-object"></a><span data-ttu-id="06894-114">休假和缺勤错误：对象参考未设置为对象的实例</span><span class="sxs-lookup"><span data-stu-id="06894-114">Leave and Absence error: Object reference not set to an instance of an object</span></span>

<span data-ttu-id="06894-115">已对休假和缺勤进行了更改来更正在**分配给我的工作项**列表中审批休假和缺勤记录之后出现的这个错误。</span><span class="sxs-lookup"><span data-stu-id="06894-115">Changes have been made to Leave and Absence to correct this error after approving leave and absence records in the **Work items assigned to me** list.</span></span>

### <a name="unable-to-recall-an-image-workflow"></a><span data-ttu-id="06894-116">无法撤消图像工作流</span><span class="sxs-lookup"><span data-stu-id="06894-116">Unable to recall an image workflow</span></span>

<span data-ttu-id="06894-117">在撤消图像工作流后，工作流将被设置为“已取消”，现有请求可以在员工自助服务工作区删除。</span><span class="sxs-lookup"><span data-stu-id="06894-117">After recalling an image workflow, the workflow will be set to "cancelled" and the existing request can be deleted in the employee self-service workspace.</span></span>

### <a name="rehired-employees-or-contractors-show-up-multiple-times-after-termination"></a><span data-ttu-id="06894-118">重新雇用的员工或合同工在雇用终止后多次显示</span><span class="sxs-lookup"><span data-stu-id="06894-118">Rehired employees or contractors show up multiple times after termination</span></span> 

<span data-ttu-id="06894-119">通过此更新，重新雇用的离职员工将只在退出列表中显示一次。</span><span class="sxs-lookup"><span data-stu-id="06894-119">With this update, terminated employees that are rehired will only display one time in the exited list.</span></span> 

## <a name="known-issue"></a><span data-ttu-id="06894-120">已知问题</span><span class="sxs-lookup"><span data-stu-id="06894-120">Known issue</span></span>

- <span data-ttu-id="06894-121">**问题**：在将新附件添加到工作人员时，**新建**和**编辑**按钮变灰。</span><span class="sxs-lookup"><span data-stu-id="06894-121">**Issue**: When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out.</span></span> 
- <span data-ttu-id="06894-122">**解决方法：** 打开附件页面之前，确保已关闭**工作人员**页面中的速见表。</span><span class="sxs-lookup"><span data-stu-id="06894-122">**Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="06894-123">如果加载**工作人员**页面时速见表已关闭，将启用附件按钮。</span><span class="sxs-lookup"><span data-stu-id="06894-123">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="06894-124">（下一个平台更新中将解决这个问题。）</span><span class="sxs-lookup"><span data-stu-id="06894-124">(This issue will be fixed in the next platform update.)</span></span>
