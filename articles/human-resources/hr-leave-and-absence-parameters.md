---
title: 配置休假和缺勤参数
description: 在 Dynamics 365 Human Resources 中定义休假和缺勤的人力资源参数。
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2acb8502ebcab122a0a1ff21e9f5e23931026327
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008205"
---
# <a name="configure-leave-and-absence-parameters"></a><span data-ttu-id="dac83-103">配置休假和缺勤参数</span><span class="sxs-lookup"><span data-stu-id="dac83-103">Configure leave and absence parameters</span></span>

<span data-ttu-id="dac83-104">在您在 Dynamics 365 Human Resources 中设置休假和缺勤计划之前，最好先验证所有相关的人力资源参数的设置，包括：</span><span class="sxs-lookup"><span data-stu-id="dac83-104">Before you set up leave and absence plans in Dynamics 365 Human Resources, it's a good idea to verify the settings for all related human resources parameters, including:</span></span>

- <span data-ttu-id="dac83-105">休假请求的编号规则</span><span class="sxs-lookup"><span data-stu-id="dac83-105">Number sequence for leave requests</span></span>
- <span data-ttu-id="dac83-106">家庭医疗休假法 (FMLA) 设置</span><span class="sxs-lookup"><span data-stu-id="dac83-106">Family Medical and Leave Act (FMLA) settings</span></span>
- <span data-ttu-id="dac83-107">休假和缺勤请求的员工自助服务设置</span><span class="sxs-lookup"><span data-stu-id="dac83-107">Employee self service settings for leave and absence requests</span></span>
- <span data-ttu-id="dac83-108">休假和缺勤参数</span><span class="sxs-lookup"><span data-stu-id="dac83-108">Leave and absence parameters</span></span>

## <a name="view-and-change-human-resources-parameters"></a><span data-ttu-id="dac83-109">查看和更改人力资源参数</span><span class="sxs-lookup"><span data-stu-id="dac83-109">View and change human resources parameters</span></span>

1. <span data-ttu-id="dac83-110">在**休假和缺勤**页面，选择**链接**选项卡。</span><span class="sxs-lookup"><span data-stu-id="dac83-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="dac83-111">在**设置**下，选择**人力资源参数**。</span><span class="sxs-lookup"><span data-stu-id="dac83-111">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="dac83-112">在**编号规则**选项卡上，验证**休假请求 ID** 的**编号规则代码**并根据需要进行更改。</span><span class="sxs-lookup"><span data-stu-id="dac83-112">On the **Number sequences** tab, verify the **Number sequence code** for **Leave request ID** and change as necessary.</span></span> <span data-ttu-id="dac83-113">此设置确定用于向休假请求自动分配 ID 的顺序。</span><span class="sxs-lookup"><span data-stu-id="dac83-113">This setting determines the sequence used for automatically assigning IDs to leave requests.</span></span>

4. <span data-ttu-id="dac83-114">在 **FMLA** 选项卡上，验证 FMLA 设置并根据需要进行更改。</span><span class="sxs-lookup"><span data-stu-id="dac83-114">On the **FMLA** tab, verify the FMLA settings and change as necessary.</span></span>

5. <span data-ttu-id="dac83-115">在**员工自助服务**选项卡上，指示经理是否可以代表员工输入休假和缺勤请求。</span><span class="sxs-lookup"><span data-stu-id="dac83-115">On the **Employee self service** tab, indicate whether managers can enter leave and absence requests on behalf of their employees.</span></span>

6. <span data-ttu-id="dac83-116">在**休假和缺勤**选项卡上，验证设置并根据需要进行更改。</span><span class="sxs-lookup"><span data-stu-id="dac83-116">On the **Leave and absence** tab, verify the settings and change as necessary.</span></span>

7. <span data-ttu-id="dac83-117">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="dac83-117">Select **Save**.</span></span>

## <a name="configure-calendar-parameters"></a><span data-ttu-id="dac83-118">配置日历参数</span><span class="sxs-lookup"><span data-stu-id="dac83-118">Configure calendar parameters</span></span>

<span data-ttu-id="dac83-119">如果启用了休假和缺勤日历预览功能，您需要配置其他参数。</span><span class="sxs-lookup"><span data-stu-id="dac83-119">If you have enabled the Leave and absence calendar preview feature, you need to configure additional parameters.</span></span> 

[!include [banner](includes/preview-feature-leave-absence.md)]

> [!NOTE]
> <span data-ttu-id="dac83-120">对于 2020 年 2 月 3 日的预览版本，仅启用了**等待处理的休假请求**。</span><span class="sxs-lookup"><span data-stu-id="dac83-120">For the preview release on February 3, 2020, only **Pending leave requests** are enabled.</span></span>

1. <span data-ttu-id="dac83-121">在**休假和缺勤**页面，选择**链接**选项卡。</span><span class="sxs-lookup"><span data-stu-id="dac83-121">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="dac83-122">在**设置**下，选择**人力资源参数**。</span><span class="sxs-lookup"><span data-stu-id="dac83-122">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="dac83-123">在**日历**选项卡上，根据需要更改日历设置。</span><span class="sxs-lookup"><span data-stu-id="dac83-123">On the **Calendar** tab, change calendar settings as necessary.</span></span>

4. <span data-ttu-id="dac83-124">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="dac83-124">Select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="dac83-125">请参阅</span><span class="sxs-lookup"><span data-stu-id="dac83-125">See also</span></span>

- [<span data-ttu-id="dac83-126">休假和缺勤概览</span><span class="sxs-lookup"><span data-stu-id="dac83-126">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
