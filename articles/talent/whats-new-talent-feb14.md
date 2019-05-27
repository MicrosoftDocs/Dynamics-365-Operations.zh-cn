---
title: Dynamics 365 for Talent（2019 年 2 月 14 日）中的新增功能或更改
description: 此主题介绍了 Microsoft Dynamics 365 for Talent 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 02/14/2019
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
ms.search.validFrom: 2019-02-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 1db7d032eade3f996e0554e64d6ea0704a347ed8
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517402"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-february-14-2019"></a><span data-ttu-id="46457-103">Dynamics 365 for Talent（2019 年 2 月 14 日）中的新增功能或更改</span><span class="sxs-lookup"><span data-stu-id="46457-103">What's new or changed in Dynamics 365 for Talent (February 14, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="46457-104">此主题介绍了 Talent 中的新增功能和更改的功能。</span><span class="sxs-lookup"><span data-stu-id="46457-104">This topic describes features that are either new or changed in Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="46457-105">Attract 中的更改</span><span class="sxs-lookup"><span data-stu-id="46457-105">Changes in Attract</span></span>
<span data-ttu-id="46457-106">此版本中包含一些小缺陷修复。</span><span class="sxs-lookup"><span data-stu-id="46457-106">There are minor bug fixes included with this release.</span></span>

## <a name="changes-in-onboarding"></a><span data-ttu-id="46457-107">Onboarding 中的更改</span><span class="sxs-lookup"><span data-stu-id="46457-107">Changes in Onboarding</span></span>
<span data-ttu-id="46457-108">此版本中包含一些小缺陷修复。</span><span class="sxs-lookup"><span data-stu-id="46457-108">There are minor bug fixes included with this release.</span></span>
 
## <a name="changes-in-core-hr"></a><span data-ttu-id="46457-109">Core HR 中的更改</span><span class="sxs-lookup"><span data-stu-id="46457-109">Changes in Core HR</span></span> 
<span data-ttu-id="46457-110">**内部版本 8.1.2146**</span><span class="sxs-lookup"><span data-stu-id="46457-110">**Build 8.1.2146**</span></span>

### <a name="employee-fixed-compensation-entity-doesnt-export-all-records"></a><span data-ttu-id="46457-111">员工固定薪酬实体无法导入所有记录</span><span class="sxs-lookup"><span data-stu-id="46457-111">Employee fixed compensation entity doesn't export all records</span></span>
<span data-ttu-id="46457-112">通过此更改，**员工固定薪酬**实体现在可以导入所有记录。</span><span class="sxs-lookup"><span data-stu-id="46457-112">With this change, the **Employee fixed compensation** entity will now export all records.</span></span> <span data-ttu-id="46457-113">此实体可用于为员工创建固定薪酬记录和更新现有固定薪酬记录。</span><span class="sxs-lookup"><span data-stu-id="46457-113">The entity can be used to create and update existing fixed compensation records for employees.</span></span> 

### <a name="employment-end-date-doesnt-honor-employee-preferred-time-zone-settings"></a><span data-ttu-id="46457-114">雇佣结束日期不遵守员工的首选时区设置</span><span class="sxs-lookup"><span data-stu-id="46457-114">Employment end date doesn't honor employee preferred time zone settings</span></span>
<span data-ttu-id="46457-115">创建或终止与公司之间的雇佣时，雇佣结束日期现在遵守用户的首选时区。</span><span class="sxs-lookup"><span data-stu-id="46457-115">Employment end dates are now honoring the user-preferred time zone when creating or ending employment with a company.</span></span>
 
### <a name="uk-addresses-display-in-analytics-as-eastern-switzerland-addresses"></a><span data-ttu-id="46457-116">英国地址在 Analytics 中显示为瑞士东部地区地址</span><span class="sxs-lookup"><span data-stu-id="46457-116">UK addresses display in Analytics as Eastern Switzerland addresses</span></span>
<span data-ttu-id="46457-117">在此版本中，已进行了更改来更正**人员管理**的“按位置分类的人数”报告中的地址不一致。</span><span class="sxs-lookup"><span data-stu-id="46457-117">In this release, a change has been made to correct misalignment in addresses in the **Personnel Management** "Headcount by location" report.</span></span>
 
### <a name="termination-code-is-not-populated-on-the-worker-position-assignment-record-when-ending-the-position"></a><span data-ttu-id="46457-118">终止职位时工作人员职位分配记录中不填充离职代码</span><span class="sxs-lookup"><span data-stu-id="46457-118">Termination code is not populated on the worker position assignment record when ending the position</span></span>
<span data-ttu-id="46457-119">已进行了更改，现在终止员工职位分配时间默认采用“离职原因”代码。</span><span class="sxs-lookup"><span data-stu-id="46457-119">A change has been made to default the "Termination reason" code when ending the employees position assignment.</span></span>

### <a name="new-entity-created-for-job-compensation-levels"></a><span data-ttu-id="46457-120">为工作薪酬级别创建了新实体</span><span class="sxs-lookup"><span data-stu-id="46457-120">New entity created for job compensation levels</span></span>
<span data-ttu-id="46457-121">已经创建了一个新的数据管理框架 (DMF) 实体。</span><span class="sxs-lookup"><span data-stu-id="46457-121">A new data management framework (DMF) entity was created.</span></span> <span data-ttu-id="46457-122">提供该实体是为了为系统中定义的每个工作创建和更新薪酬级别、市场价值和调查信息。</span><span class="sxs-lookup"><span data-stu-id="46457-122">The entity provides for creation and updates to compensation levels, market values, and survey information for each job defined in the system.</span></span>
