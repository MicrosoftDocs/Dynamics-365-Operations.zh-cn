---
title: 开发概述
description: 本开发人员指南提供 API 和自定义字段参考。 另外还提供有关与其他应用集成的信息。
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 5e67749e6f10b1c9202605b26164e30e5d39aa28
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793577"
---
# <a name="development-overview"></a><span data-ttu-id="88e5f-104">开发概述</span><span class="sxs-lookup"><span data-stu-id="88e5f-104">Development overview</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="88e5f-105">本开发人员指南提供 API 和自定义字段参考。</span><span class="sxs-lookup"><span data-stu-id="88e5f-105">This Developer Guide provides an API and custom fields reference.</span></span> <span data-ttu-id="88e5f-106">另外还提供有关与其他应用集成的信息。</span><span class="sxs-lookup"><span data-stu-id="88e5f-106">It also provides information on integrating with other apps.</span></span>

- [<span data-ttu-id="88e5f-107">概览</span><span class="sxs-lookup"><span data-stu-id="88e5f-107">Overview</span></span>](hr-developer-overview.md)

- [<span data-ttu-id="88e5f-108">通过 Power Apps 和 Power Automate 扩展</span><span class="sxs-lookup"><span data-stu-id="88e5f-108">Extend with Power Apps and Power Automate</span></span>](hr-developer-power-apps.md)

- [<span data-ttu-id="88e5f-109">Dataverse 中的 Human Resources 实体</span><span class="sxs-lookup"><span data-stu-id="88e5f-109">Human Resources entities in Dataverse</span></span>](hr-developer-entities.md)

- [<span data-ttu-id="88e5f-110">自定义字段</span><span class="sxs-lookup"><span data-stu-id="88e5f-110">Custom fields</span></span>](hr-developer-custom-fields.md)

- <span data-ttu-id="88e5f-111">设置数据集成</span><span class="sxs-lookup"><span data-stu-id="88e5f-111">Set up data integration</span></span>
  - [<span data-ttu-id="88e5f-112">选择数据集成技术</span><span class="sxs-lookup"><span data-stu-id="88e5f-112">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)
  - [<span data-ttu-id="88e5f-113">配置 Dataverse 集成</span><span class="sxs-lookup"><span data-stu-id="88e5f-113">Configure Dataverse integration</span></span>](hr-admin-integration-common-data-service.md)
  - [<span data-ttu-id="88e5f-114">配置与 Finance 的集成</span><span class="sxs-lookup"><span data-stu-id="88e5f-114">Configure integration with Finance</span></span>](hr-admin-integration-finance.md)
  - [<span data-ttu-id="88e5f-115">配置与 Dayforce 的集成</span><span class="sxs-lookup"><span data-stu-id="88e5f-115">Configure integration with Dayforce</span></span>](hr-admin-integration-dayforce.md)
  - [<span data-ttu-id="88e5f-116">创建定期数据导出应用</span><span class="sxs-lookup"><span data-stu-id="88e5f-116">Create a recurring data export app</span></span>](hr-admin-integration-recurring-data-export.md)
  - <span data-ttu-id="88e5f-117">与 Office 集成</span><span class="sxs-lookup"><span data-stu-id="88e5f-117">Integrate with Office</span></span>
    - [<span data-ttu-id="88e5f-118">Office 集成教程</span><span class="sxs-lookup"><span data-stu-id="88e5f-118">Office integration tutorial</span></span>](../dev-itpro/office-integration/office-integration-tutorial.md?toc=/dynamics365/unified-operations/talent/toc.json)
    - [<span data-ttu-id="88e5f-119">更新 Excel 中的实体数据</span><span class="sxs-lookup"><span data-stu-id="88e5f-119">Update entity data in Excel</span></span>](../dev-itpro/office-integration/use-excel-add-in.md?toc=/dynamics365/unified-operations/talent/toc.json)
    - [<span data-ttu-id="88e5f-120">创建“在 Excel 中打开”体验</span><span class="sxs-lookup"><span data-stu-id="88e5f-120">Create Open in Excel experiences</span></span>](../dev-itpro/office-integration/office-integration-edit-excel.md?toc=/dynamics365/unified-operations/talent/toc.json)
    - [<span data-ttu-id="88e5f-121">解决 Office 集成问题</span><span class="sxs-lookup"><span data-stu-id="88e5f-121">Troubleshoot Office integration</span></span>](../dev-itpro/office-integration/office-integration-troubleshooting.md?toc=/dynamics365/unified-operations/talent/toc.json)

- <span data-ttu-id="88e5f-122">实体 API 引用</span><span class="sxs-lookup"><span data-stu-id="88e5f-122">Entity API reference</span></span>
  - [<span data-ttu-id="88e5f-123">身份验证</span><span class="sxs-lookup"><span data-stu-id="88e5f-123">Authentication</span></span>](hr-developer-api-authentication.md)
  - <span data-ttu-id="88e5f-124">实体</span><span class="sxs-lookup"><span data-stu-id="88e5f-124">Entities</span></span>
    - [<span data-ttu-id="88e5f-125">MyLeaveRequests</span><span class="sxs-lookup"><span data-stu-id="88e5f-125">MyLeaveRequests</span></span>](hr-developer-api-myleaverequests-overview.md)
    - [<span data-ttu-id="88e5f-126">将请假申请提交至工作流</span><span class="sxs-lookup"><span data-stu-id="88e5f-126">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)

## <a name="see-also"></a><span data-ttu-id="88e5f-127">请参阅</span><span class="sxs-lookup"><span data-stu-id="88e5f-127">See also</span></span>

- [<span data-ttu-id="88e5f-128">Human Resources 的新增功能或更改</span><span class="sxs-lookup"><span data-stu-id="88e5f-128">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)
- [<span data-ttu-id="88e5f-129">管理员指南</span><span class="sxs-lookup"><span data-stu-id="88e5f-129">Administrator Guide</span></span>](hr-admin-overview.md)
- [<span data-ttu-id="88e5f-130">用户指南</span><span class="sxs-lookup"><span data-stu-id="88e5f-130">User Guide</span></span>](hr-hrpro-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]