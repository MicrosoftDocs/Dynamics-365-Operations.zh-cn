---
title: 任务录制的安全诊断
description: 本主题提供有关如何根据任务录制来分析和管理安全许可要求的信息。
author: Peakerbl
manager: AnnBe
ms.date: 05/05/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: ''
ms.dyn365.ops.version: Version 10.0.9
ms.openlocfilehash: 88eb90b35f1a9754cc4daa01d8f40cdf712db4f8
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679782"
---
# <a name="security-diagnostics-for-task-recordings"></a><span data-ttu-id="fc444-103">任务录制的安全诊断</span><span class="sxs-lookup"><span data-stu-id="fc444-103">Security diagnostics for task recordings</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="before-you-begin"></a><span data-ttu-id="fc444-104">开始之前</span><span class="sxs-lookup"><span data-stu-id="fc444-104">Before you begin</span></span>

<span data-ttu-id="fc444-105">本主题提供有关如何根据任务录制来分析和管理安全许可要求的信息。</span><span class="sxs-lookup"><span data-stu-id="fc444-105">This topic provides information about how to analyze and manage security permission requirements based on a task recording.</span></span> <span data-ttu-id="fc444-106">在完成本主题中的步骤之前，您必须具有要分析的业务流程的任务录制。</span><span class="sxs-lookup"><span data-stu-id="fc444-106">Before you complete the steps in this topic, you must have a task recording of the business process that you want to analyze.</span></span> <span data-ttu-id="fc444-107">要录制业务流程，请参阅[任务录制器资源](../../user-interface/task-recorder.md)。</span><span class="sxs-lookup"><span data-stu-id="fc444-107">To record a business process, see [Task recorder resources](../../user-interface/task-recorder.md).</span></span> 

## <a name="manage-security-for-a-task-recording"></a><span data-ttu-id="fc444-108">管理任务录制的安全性</span><span class="sxs-lookup"><span data-stu-id="fc444-108">Manage security for a task recording</span></span>

1. <span data-ttu-id="fc444-109">转到 **系统管理** > **安全** > **任务录制的安全诊断**。</span><span class="sxs-lookup"><span data-stu-id="fc444-109">Go to **System administration** > **Security** > **Security diagnostic for task recording**.</span></span>
2. <span data-ttu-id="fc444-110">从其位置打开任务录制。</span><span class="sxs-lookup"><span data-stu-id="fc444-110">Open the task recording from its location.</span></span> <span data-ttu-id="fc444-111">选择 **从此 PC 中打开** 或 **从 Lifecycle Services 中打开**，然后选择 **关闭**。</span><span class="sxs-lookup"><span data-stu-id="fc444-111">Select **Open from this PC** or **Open from Lifecycle Services**, and then select **Close**.</span></span>
3. <span data-ttu-id="fc444-112">这将打开 **安全菜单项详细信息** 页面，其中列出了该流程所需的安全对象。</span><span class="sxs-lookup"><span data-stu-id="fc444-112">This will open the **Security menu item details** page that lists the security objects required for the process.</span></span>

 > [!NOTE]
 > <span data-ttu-id="fc444-113">列表中不包括 **操作** 和 **输出** 菜单项。</span><span class="sxs-lookup"><span data-stu-id="fc444-113">The **Action** and **Output** menu items are not included in the list.</span></span>

4. <span data-ttu-id="fc444-114">在 **用户 ID** 字段中，选择一个用户。</span><span class="sxs-lookup"><span data-stu-id="fc444-114">In the **User ID** field, select a user.</span></span> <span data-ttu-id="fc444-115">如果用户没有某些菜单项的权限，则 **缺少权限** 字段将更新为 **是**。</span><span class="sxs-lookup"><span data-stu-id="fc444-115">If the user does not have permissions for some menu items, the **Missing permissions** field will update to **Yes**.</span></span>
  
  ![安全菜单项详细信息页面](../media/Security-Menu-Item-Details.png)

5. <span data-ttu-id="fc444-117">选择 **添加引用** 以查看安全对象的列表，包括授予缺少的权限的角色、职责和特权。</span><span class="sxs-lookup"><span data-stu-id="fc444-117">Select **Add Reference** to see a list of the security objects, including roles, duties, and privileges that grant the missing permission.</span></span>
6. <span data-ttu-id="fc444-118">从列表中选择安全对象：</span><span class="sxs-lookup"><span data-stu-id="fc444-118">Select a security object from the list:</span></span>

    - <span data-ttu-id="fc444-119">如果选择了 **角色**，请选择 **为用户添加角色**。</span><span class="sxs-lookup"><span data-stu-id="fc444-119">If **Role** is selected, select **Add role to user**.</span></span> <span data-ttu-id="fc444-120">这会打开 **将用户分派给角色** 页。</span><span class="sxs-lookup"><span data-stu-id="fc444-120">This will open the **Assign users to roles** page.</span></span> <span data-ttu-id="fc444-121">有关详细信息，请参阅[将用户分派给安全角色](assign-users-security-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="fc444-121">For more information, see [Assign users to security roles](assign-users-security-roles.md) page.</span></span>
    - <span data-ttu-id="fc444-122">如果选择了 **职责**，请选择 **将职责添加到角色**，选择应将职责添加到的角色，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="fc444-122">If **Duty** is selected, select **Add duty to role**, select the roles that the duty should be added to, and then select **OK**.</span></span>
    - <span data-ttu-id="fc444-123">如果选择了 **特权**，请选择 **将特权添加到职责**，选择应将职责添加到的角色，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="fc444-123">If **Privilege** is selected, select **Add privilege to duties**, select the roles that the duty should be added to, and then select **OK**.</span></span>
