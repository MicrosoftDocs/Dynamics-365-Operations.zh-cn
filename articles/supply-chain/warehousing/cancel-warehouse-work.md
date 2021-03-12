---
title: 取消仓库工作以进行异常处理
description: 本主题介绍“取消工作”功能，该功能使仓库主管可以处理被阻止的工作。
author: omulvad
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSTroubIeshootingSeIfService, WHSTroubleshootingSelfService
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2019-10-1
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ae4062401cd5be2371c45642b78bf3708b04f664
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001185"
---
# <a name="cancel-warehouse-work-for-exception-handling"></a><span data-ttu-id="675ad-103">取消仓库工作以进行异常处理</span><span class="sxs-lookup"><span data-stu-id="675ad-103">Cancel warehouse work for exception handling</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="675ad-104">Microsoft Dynamics 365 Supply Chain Management 中的“取消工作”功能使管理员用户可以取消当前正在进行的特定仓库工作，但是由于特殊情况，该工作已被系统阻止或无法完成。</span><span class="sxs-lookup"><span data-stu-id="675ad-104">The Cancel work functionality in Microsoft Dynamics 365 Supply Chain Management lets the admin user cancel specific warehouse work that is currently in progress, but that is blocked by the system or can't be completed because of exceptional circumstances.</span></span> <span data-ttu-id="675ad-105">此功能是修复不一致数据的 SQL 纠正脚本的一种有吸引力且安全的替代方法。</span><span class="sxs-lookup"><span data-stu-id="675ad-105">This functionality is an attractive and secure alternative to SQL corrective scripts that fix inconsistent data.</span></span> <span data-ttu-id="675ad-106">不过，尽管这些脚本通常是从 IT 专业人员那里索要的，但具有管理员权限的公司中的用户可以使用“取消工作”功能。</span><span class="sxs-lookup"><span data-stu-id="675ad-106">However, whereas these scripts are typically requested from IT professionals, the Cancel work functionality can be used by users in the company who have admin rights.</span></span>

<span data-ttu-id="675ad-107">您可以在 **仓库管理** \> **定期任务** \> **清除 \> 取消工作** 中访问“取消工作”功能。</span><span class="sxs-lookup"><span data-stu-id="675ad-107">You can access the Cancel work functionality at **Warehouse management** \> **Periodic tasks** \> **Clean up \> Cancel work**.</span></span> <span data-ttu-id="675ad-108">在 **取消工作** 对话框中，指定要取消的工作的工作 ID，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="675ad-108">In the **Cancel work** dialog box, specify the work ID of the work to cancel, and then select **OK**.</span></span>

## <a name="warehouse-work-that-can-be-canceled"></a><span data-ttu-id="675ad-109">可以取消的仓库工作</span><span class="sxs-lookup"><span data-stu-id="675ad-109">Warehouse work that can be canceled</span></span>

<span data-ttu-id="675ad-110">在仓库领料工序期间，工作人员可能会遇到这样的情况，即他们已经将从存储位置领取的数量登记到用户位置，但是他们无法登记放置操作。</span><span class="sxs-lookup"><span data-stu-id="675ad-110">During warehouse picking operations, a worker might encounter situations where they have registered quantities as picked from a storage location to their user location, but then they can't register the put operation.</span></span> <span data-ttu-id="675ad-111">仓库数据不一致通常是（但并非总是）造成工作被阻止的原因。</span><span class="sxs-lookup"><span data-stu-id="675ad-111">Inconsistent warehouse data is often, but not always, the reason why work is blocked.</span></span>

<span data-ttu-id="675ad-112">与可以使用工作标题上的 **取消** 按钮访问的常规“取消”功能不同，“取消工作”功能不需要最后完成的工作行是 **放置** 类型的工作行。</span><span class="sxs-lookup"><span data-stu-id="675ad-112">Unlike the regular Cancel functionality that can be accessed by using the **Cancel** button on the work header, the Cancel work functionality doesn't require that the last completed work line be a work line of the **put** type.</span></span> <span data-ttu-id="675ad-113">换言之，对于“取消工作”功能，即使工作行上的物料数量在用户位置，也可以运行取消逻辑。</span><span class="sxs-lookup"><span data-stu-id="675ad-113">In other words, for the Cancel work functionality, cancellation logic can be run even if the item quantity on a work line is in a user location.</span></span>

> [!NOTE]
> <span data-ttu-id="675ad-114">对于由于操作原因必须取消的工作，仓库用户必须继续使用工作页面上的常规“取消”功能。</span><span class="sxs-lookup"><span data-stu-id="675ad-114">For work that must be canceled for operational reasons, warehouse users must continue to use the regular Cancel functionality on the work page.</span></span>

<span data-ttu-id="675ad-115">使用“取消工作”功能只能取消 **销售**、**转移发货**、**原材料领料** 或 **补货** 类型的工作。</span><span class="sxs-lookup"><span data-stu-id="675ad-115">Only work of the **Sales**, **Transfer issue**, **Raw material picking**, or **Replenishment** type can be canceled by using the Cancel work functionality.</span></span> <span data-ttu-id="675ad-116">对于锁定的原材料领料工作或可以使用常规“取消”功能取消的工作，不会运行取消逻辑（请参见前面的说明）。</span><span class="sxs-lookup"><span data-stu-id="675ad-116">Cancellation logic won't be run for frozen raw material picking work or work that can be canceled by using the regular Cancel functionality (see the preceding note).</span></span>

<span data-ttu-id="675ad-117">要取消阻止工作，系统会取消所有其余工作行并修复与用户指定的工作 ID 关联的仓库数据。</span><span class="sxs-lookup"><span data-stu-id="675ad-117">To unblock the work, the system cancels any remaining work lines and fixes the warehouse data that is associated with the work ID that the user specified.</span></span> <span data-ttu-id="675ad-118">然后可以恢复涉及受影响物料数量的任何常规仓库处理操作。</span><span class="sxs-lookup"><span data-stu-id="675ad-118">Any regular warehouse-handling operations that involve the affected item quantity can then resume.</span></span>

<span data-ttu-id="675ad-119">要在取消工作后将受影响的物料放置在特定位置，用户必须在移动设备上使用库存变动或数量调整操作。</span><span class="sxs-lookup"><span data-stu-id="675ad-119">To put the affected item in a specific location after the work is canceled, the user must use an inventory movement or quantity adjustment operation on a mobile device.</span></span>
