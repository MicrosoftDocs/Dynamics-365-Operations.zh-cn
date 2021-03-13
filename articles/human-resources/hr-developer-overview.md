---
title: 开发概述
description: 本开发人员指南提供 API 和自定义字段参考。 另外还提供有关与其他应用集成的信息。
author: andreabichsel
manager: tfehr
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
ms.openlocfilehash: 517febd7967350956a28dfd9d11e4042456c7da0
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115382"
---
# <a name="development-overview"></a><span data-ttu-id="f6314-104">开发概述</span><span class="sxs-lookup"><span data-stu-id="f6314-104">Development overview</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="f6314-105">本开发人员指南提供 API 和自定义字段参考。</span><span class="sxs-lookup"><span data-stu-id="f6314-105">This Developer Guide provides an API and custom fields reference.</span></span> <span data-ttu-id="f6314-106">另外还提供有关与其他应用集成的信息。</span><span class="sxs-lookup"><span data-stu-id="f6314-106">It also provides information on integrating with other apps.</span></span>

- [<span data-ttu-id="f6314-107">概览</span><span class="sxs-lookup"><span data-stu-id="f6314-107">Overview</span></span>](hr-developer-overview.md)

- [<span data-ttu-id="f6314-108">通过 Power Apps 和 Power Automate 扩展</span><span class="sxs-lookup"><span data-stu-id="f6314-108">Extend with Power Apps and Power Automate</span></span>](hr-developer-power-apps.md)

- [<span data-ttu-id="f6314-109">Dataverse 中的 Human Resources 实体</span><span class="sxs-lookup"><span data-stu-id="f6314-109">Human Resources entities in Dataverse</span></span>](hr-developer-entities.md)

- [<span data-ttu-id="f6314-110">自定义字段</span><span class="sxs-lookup"><span data-stu-id="f6314-110">Custom fields</span></span>](hr-developer-custom-fields.md)

- <span data-ttu-id="f6314-111">设置数据集成</span><span class="sxs-lookup"><span data-stu-id="f6314-111">Set up data integration</span></span>
  - [<span data-ttu-id="f6314-112">选择数据集成技术</span><span class="sxs-lookup"><span data-stu-id="f6314-112">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)
  - [<span data-ttu-id="f6314-113">配置 Dataverse 集成</span><span class="sxs-lookup"><span data-stu-id="f6314-113">Configure Dataverse integration</span></span>](hr-admin-integration-common-data-service.md)
  - [<span data-ttu-id="f6314-114">配置与 Finance 的集成</span><span class="sxs-lookup"><span data-stu-id="f6314-114">Configure integration with Finance</span></span>](hr-admin-integration-finance.md)
  - [<span data-ttu-id="f6314-115">配置与 Dayforce 的集成</span><span class="sxs-lookup"><span data-stu-id="f6314-115">Configure integration with Dayforce</span></span>](hr-admin-integration-dayforce.md)
  - [<span data-ttu-id="f6314-116">创建定期数据导出应用</span><span class="sxs-lookup"><span data-stu-id="f6314-116">Create a recurring data export app</span></span>](hr-admin-integration-recurring-data-export.md)
  - <span data-ttu-id="f6314-117">与 Office 集成</span><span class="sxs-lookup"><span data-stu-id="f6314-117">Integrate with Office</span></span>
    - [<span data-ttu-id="f6314-118">Office 集成教程</span><span class="sxs-lookup"><span data-stu-id="f6314-118">Office integration tutorial</span></span>](../dev-itpro/office-integration/office-integration-tutorial.md?toc=/dynamics365/unified-operations/talent/toc.json)
    - [<span data-ttu-id="f6314-119">更新 Excel 中的实体数据</span><span class="sxs-lookup"><span data-stu-id="f6314-119">Update entity data in Excel</span></span>](../dev-itpro/office-integration/use-excel-add-in.md?toc=/dynamics365/unified-operations/talent/toc.json)
    - [<span data-ttu-id="f6314-120">创建“在 Excel 中打开”体验</span><span class="sxs-lookup"><span data-stu-id="f6314-120">Create Open in Excel experiences</span></span>](../dev-itpro/office-integration/office-integration-edit-excel.md?toc=/dynamics365/unified-operations/talent/toc.json)
    - [<span data-ttu-id="f6314-121">解决 Office 集成问题</span><span class="sxs-lookup"><span data-stu-id="f6314-121">Troubleshoot Office integration</span></span>](../dev-itpro/office-integration/office-integration-troubleshooting.md?toc=/dynamics365/unified-operations/talent/toc.json)

- <span data-ttu-id="f6314-122">实体 API 引用</span><span class="sxs-lookup"><span data-stu-id="f6314-122">Entity API reference</span></span>
  - [<span data-ttu-id="f6314-123">身份验证</span><span class="sxs-lookup"><span data-stu-id="f6314-123">Authentication</span></span>](hr-developer-api-authentication.md)
  - <span data-ttu-id="f6314-124">实体</span><span class="sxs-lookup"><span data-stu-id="f6314-124">Entities</span></span>
    - [<span data-ttu-id="f6314-125">MyLeaveRequests</span><span class="sxs-lookup"><span data-stu-id="f6314-125">MyLeaveRequests</span></span>](hr-developer-api-myleaverequests-overview.md)
    - [<span data-ttu-id="f6314-126">将请假申请提交至工作流</span><span class="sxs-lookup"><span data-stu-id="f6314-126">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)

## <a name="see-also"></a><span data-ttu-id="f6314-127">请参阅</span><span class="sxs-lookup"><span data-stu-id="f6314-127">See also</span></span>

- [<span data-ttu-id="f6314-128">Human Resources 的新增功能或更改</span><span class="sxs-lookup"><span data-stu-id="f6314-128">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)
- [<span data-ttu-id="f6314-129">管理员指南</span><span class="sxs-lookup"><span data-stu-id="f6314-129">Administrator Guide</span></span>](hr-admin-overview.md)
- [<span data-ttu-id="f6314-130">用户指南</span><span class="sxs-lookup"><span data-stu-id="f6314-130">User Guide</span></span>](hr-hrpro-overview.md)
