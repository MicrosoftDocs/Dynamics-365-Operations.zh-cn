---
title: 未雇用的工作人员
description: 您的组织中没有未来、当前或历史雇用的工作人员会出现在“未雇用工作人员”窗体中。
author: andreabichsel
ms.date: 04/06/2021
ms.topic: ''
ms.prod: ''
ms.technology: ''
ms.search.form: HcmWorkerV2, HRMMassHireProject, HRMMassHireLine, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2021-04-06
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e1a137de25924f4c4ec6f6b1fe70f9d21af591c0
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924563"
---
# <a name="workers-without-employment"></a><span data-ttu-id="3da36-103">未雇用的工作人员</span><span class="sxs-lookup"><span data-stu-id="3da36-103">Workers without employment</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="3da36-104">您的组织中没有未来、当前或历史雇用的工作人员会出现在 **未雇用工作人员** 窗体中。</span><span class="sxs-lookup"><span data-stu-id="3da36-104">Workers with no future, active, or historical employment with your organization appear in the **Workers without employment** form.</span></span> <span data-ttu-id="3da36-105">当您导入没有雇用记录的工作人员时，或者通过 **工作人员 > 雇用历史记录** 删除工作人员的雇用时，会出现具有此状态的工作人员。</span><span class="sxs-lookup"><span data-stu-id="3da36-105">Workers with this status can appear when you import workers without an employment record, or when you delete a worker's employment via **Workers > Employment history**.</span></span>

<span data-ttu-id="3da36-106">默认情况下，**未雇用工作人员** 窗体对以下角色可用：</span><span class="sxs-lookup"><span data-stu-id="3da36-106">By default, the **Workers without employment** form is available to the following roles:</span></span>

- <span data-ttu-id="3da36-107">人力资源助理</span><span class="sxs-lookup"><span data-stu-id="3da36-107">Human Resources Assistant</span></span>
- <span data-ttu-id="3da36-108">人力资源经理</span><span class="sxs-lookup"><span data-stu-id="3da36-108">Human Resources Manager</span></span>
- <span data-ttu-id="3da36-109">招聘人员</span><span class="sxs-lookup"><span data-stu-id="3da36-109">Recruiter</span></span>
- <span data-ttu-id="3da36-110">薪酬福利经理</span><span class="sxs-lookup"><span data-stu-id="3da36-110">Comp and Benefits Manager</span></span>
- <span data-ttu-id="3da36-111">工资管理员</span><span class="sxs-lookup"><span data-stu-id="3da36-111">Payroll Administrator</span></span>
- <span data-ttu-id="3da36-112">工资经理</span><span class="sxs-lookup"><span data-stu-id="3da36-112">Payroll Manager</span></span>
- <span data-ttu-id="3da36-113">培训经理</span><span class="sxs-lookup"><span data-stu-id="3da36-113">Training Manager</span></span>

<span data-ttu-id="3da36-114">在 **未雇用工作人员** 列表中，您可以删除列出的个人。</span><span class="sxs-lookup"><span data-stu-id="3da36-114">In the **Workers without employment** list, you can delete the individuals listed.</span></span> <span data-ttu-id="3da36-115">默认情况下，此特权被授予“人力资源助理”角色。</span><span class="sxs-lookup"><span data-stu-id="3da36-115">By default, this privilege is given to the Human Resources Assistant role.</span></span> <span data-ttu-id="3da36-116">您可以通过以下步骤将此特权授予其他角色：</span><span class="sxs-lookup"><span data-stu-id="3da36-116">You can give this privilege to other roles with the following steps:</span></span>

1. <span data-ttu-id="3da36-117">选择 **系统管理**，然后选择 **安全配置**。</span><span class="sxs-lookup"><span data-stu-id="3da36-117">Select **System administration**, and then select **Security configuration**.</span></span>

2. <span data-ttu-id="3da36-118">在 **特权** 选项卡中，筛选 **特权** 列表以 **维护工作人员**。</span><span class="sxs-lookup"><span data-stu-id="3da36-118">In the **Privileges** tab, filter the **Privileges** list to **Maintain workers**.</span></span>

   <span data-ttu-id="3da36-119">[![筛选特权列表](./media/hr-personnel-workers-without-employment-filter.png)](./media/hr-personnel-workers-without-employment-filter.png)</span><span class="sxs-lookup"><span data-stu-id="3da36-119">[![Filter Privileges list](./media/hr-personnel-workers-without-employment-filter.png)](./media/hr-personnel-workers-without-employment-filter.png)</span></span>

3. <span data-ttu-id="3da36-120">在 **参考** 列中，选择 **显示菜单项**。</span><span class="sxs-lookup"><span data-stu-id="3da36-120">In the **References** column, select **Display menu items**.</span></span>

4. <span data-ttu-id="3da36-121">在 **显示菜单项** 中，选择 **HcmWorkersWithoutEmployment**。</span><span class="sxs-lookup"><span data-stu-id="3da36-121">In **Display menu items**, select **HcmWorkersWithoutEmployment**.</span></span>

   <span data-ttu-id="3da36-122">[![选择窗体](./media/hr-personnel-workers-without-employment-select.png)](./media/hr-personnel-workers-without-employment-select.png)</span><span class="sxs-lookup"><span data-stu-id="3da36-122">[![Select form](./media/hr-personnel-workers-without-employment-select.png)](./media/hr-personnel-workers-without-employment-select.png)</span></span>

5. <span data-ttu-id="3da36-123">将 **删除** 权限设置为 **授权**。</span><span class="sxs-lookup"><span data-stu-id="3da36-123">Set the **Delete** permission to **Grant**.</span></span>

6. <span data-ttu-id="3da36-124">选择 **已取消发布的对象** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="3da36-124">Select the **Unpublished objects** tab.</span></span>

7. <span data-ttu-id="3da36-125">选择 **全部发布**。</span><span class="sxs-lookup"><span data-stu-id="3da36-125">Select **Publish all**.</span></span>

   <span data-ttu-id="3da36-126">[![发布更改](./media/hr-personnel-workers-without-employment-publish.png)](./media/hr-personnel-workers-without-employment-publish.png)</span><span class="sxs-lookup"><span data-stu-id="3da36-126">[![Publish changes](./media/hr-personnel-workers-without-employment-publish.png)](./media/hr-personnel-workers-without-employment-publish.png)</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]