---
title: Dynamics 365 Talent - Core HR（2018 年 9 月 24 日）中的新增功能或更改
description: 此主题介绍了 Microsoft Dynamics 365 Talent - Core HR 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 09/21/2018
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
ms.search.validFrom: 2018-09-30
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e0c1a3bf7613db4887e0943a70ad6262a70997f0
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898958"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-september-24-2018"></a><span data-ttu-id="0f0e6-103">Dynamics 365 Talent - Core HR（2018 年 9 月 24 日）中的新增功能或更改</span><span class="sxs-lookup"><span data-stu-id="0f0e6-103">What's new or changed in Dynamics 365 Talent - Core HR (September 24, 2018)</span></span>

<span data-ttu-id="0f0e6-104">**内部版本 8.1.1015.0**</span><span class="sxs-lookup"><span data-stu-id="0f0e6-104">**Build 8.1.1015.0**</span></span>

<span data-ttu-id="0f0e6-105">此主题介绍了 Core HR 中的新增功能和更改的功能。</span><span class="sxs-lookup"><span data-stu-id="0f0e6-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="currency-added-to-benefits"></a><span data-ttu-id="0f0e6-106">为福利添加的币种</span><span class="sxs-lookup"><span data-stu-id="0f0e6-106">Currency added to Benefits</span></span>

<span data-ttu-id="0f0e6-107">福利计划已经过更新，现在包含福利币种。</span><span class="sxs-lookup"><span data-stu-id="0f0e6-107">Benefit plans have been updated to include the currency of the benefit.</span></span> <span data-ttu-id="0f0e6-108">工作人员登记福利中也有这个新字段。</span><span class="sxs-lookup"><span data-stu-id="0f0e6-108">This new field is also available on worker enrolled benefits.</span></span> <span data-ttu-id="0f0e6-109">这个新字段是“维护权益”和“查看权益列表”安全权限的一部分。</span><span class="sxs-lookup"><span data-stu-id="0f0e6-109">This new field is part of the Maintain benefits and View a list of benefits security privilege.</span></span>

## <a name="update-proration-process--leave-and-absence"></a><span data-ttu-id="0f0e6-110">更新按比例分配过程 – 休假和缺勤</span><span class="sxs-lookup"><span data-stu-id="0f0e6-110">Update proration process – Leave and Absence</span></span>

<span data-ttu-id="0f0e6-111">组织根据员工加入和离开公司的时间以不同的方式奖励休假。</span><span class="sxs-lookup"><span data-stu-id="0f0e6-111">Organizations award time off differently based on when employees join and leave the company.</span></span> <span data-ttu-id="0f0e6-112">有些离开组织的员工可能需要在解除雇用日期结束奖励，而其他用户则根据最后工作日停止累积过程。</span><span class="sxs-lookup"><span data-stu-id="0f0e6-112">For employees leaving the organization, some may need to end the award on the termination date, while others rely on the last day worked to stop the accrual process.</span></span> <span data-ttu-id="0f0e6-113">这些更改让组织可以在组织解除雇用过程中选择何时结束登记。</span><span class="sxs-lookup"><span data-stu-id="0f0e6-113">These changes provide organizations the ability to choose when to end enrollment during the termination process.</span></span> <span data-ttu-id="0f0e6-114">这些选项是经理自助服务中“解除雇用工作人员”权限的一部分。</span><span class="sxs-lookup"><span data-stu-id="0f0e6-114">These new options are part of the privileges for Terminate a worker and Terminate a worker from manager self service.</span></span> 

## <a name="other-changes"></a><span data-ttu-id="0f0e6-115">其他更改</span><span class="sxs-lookup"><span data-stu-id="0f0e6-115">Other changes</span></span>

<span data-ttu-id="0f0e6-116">此版本中还包含若干缺陷修复。</span><span class="sxs-lookup"><span data-stu-id="0f0e6-116">This release includes several additional bug fixes.</span></span>

## <a name="known-issue"></a><span data-ttu-id="0f0e6-117">已知问题</span><span class="sxs-lookup"><span data-stu-id="0f0e6-117">Known Issue</span></span>

-   <span data-ttu-id="0f0e6-118">**问题：** 向工作人员添加新附件时，**新建**和**编辑**按钮灰显。**解决方法：** 打开附件页面之前，确保已关闭**工作人员**页面中的速见表。</span><span class="sxs-lookup"><span data-stu-id="0f0e6-118">**Issue:** When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out. **Workaround:** Before opening the attachment page, make sure that the fact boxes on the **Worker** page are closed.</span></span> <span data-ttu-id="0f0e6-119">如果加载**工作人员**页面时速见表已关闭，将启用附件按钮。</span><span class="sxs-lookup"><span data-stu-id="0f0e6-119">If the fact boxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="0f0e6-120">（下一个平台更新中将解决这个问题。）</span><span class="sxs-lookup"><span data-stu-id="0f0e6-120">(This issue will be fixed in the next platform update.)</span></span>
