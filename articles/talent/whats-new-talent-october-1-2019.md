---
title: Dynamics 365 Talent（2019 年 10 月 1 日）中的新增功能或更改
description: 此主题介绍了 Microsoft Dynamics 365 Talent 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 10/01/2019
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
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 86d8ce59ea67f42bc6e3abea50788bd3bc085e33
ms.sourcegitcommit: 0dd8d0510214f92936a9dd214b404c5c8103587b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/01/2019
ms.locfileid: "2419330"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-01-2019"></a>Dynamics 365 Talent（2019 年 10 月 1 日）中的新增功能或更改

[!include [banner](includes/banner.md)]

此主题介绍了 Dynamics 365 Talent 中的新增功能和更改的功能。

## <a name="changes-in-attract"></a>Attract 中的更改

本版本中包含 Dynamics 365 Talent: Attract 的小缺陷修复。

## <a name="changes-in-onboard"></a>Onboard 中的更改

本版本中包含 Dynamics 365 Talent: Onboard 的小缺陷修复。

## <a name="changes-in-core-hr"></a>Core HR 中的更改

本部分中的更改适用于内部版本号 8.1.2509。 某些标题中括号内的数字是 Microsoft Dynamics Lifecycle Services (LCS) 中的支持号码。

### <a name="streamlined-employee-entry-and-navigation"></a>简化的员工条目和导航

此功能现在可在所有环境中使用。 要打开此功能，请导航至**系统管理 > 链接 > 设置 > 系统参数 > 预览功能**。 选择**增强的工作人员窗体和导航**。 这为所有用户启用了这些更改。 您可以随时关闭此选项。

有关详细信息，请参阅[简化的员工输入和导航](./streamlined-employee-entry.md)。 若要观看这些更改的视频，请参阅 [Dynamics 365 for Talent 2019 发布第 2 波概述](https://aka.ms/ROGT19RW2ROV)。

### <a name="you-can-enable-preview-features-in-sandbox-and-trial-environments"></a>可以在沙盒和试用环境中启用预览功能。

配置新的 Talent 实例时，可指定实例类型为生产还是沙盒。 沙盒类型的实例可用于提前试用新功能。 如果需要将现有实例之一更新为沙盒实例类型，请联系支持以发起更改请求。

有关如何发布更改的详细信息，请参阅[配置 Talent](./provisioning-talent.md)。

### <a name="compensation-date-defaults-to-a-different-date-than-the-position-assignment-337694"></a>薪酬日期默认与职位分配日期不同 (337694)

应用此更改之后，薪酬开始日期默认为职位分配开始日期。

### <a name="not-able-to-end-compensation-along-with-its-position-assignment-328993"></a>无法与职位分配一起结束薪酬 (328993)

应用此更改之后，结束职位分配时，可以在已开启了个人操作的情况下使用**工作人员职位分配**页中的**结束分配**终止薪酬。

### <a name="bank-account-validation-requires-routing-and-account-numbers-in-all-locations-340403"></a>需要所有位置的银行代号和账号，才能验证用户帐户 (340403)

本周的更改已经添加了一个新的配置选项，用于禁用需要**银行代号**和**账号**的验证。 

### <a name="attachments-are-not-enabled-in-mss-performance-journals-for-performance-feedback-341794"></a>MSS 绩效日记帐中不能为绩效反馈启用附件 (341794)

在本周的发布中，将在绩效日记帐页面中为反馈项启用附件。

### <a name="leave-request-details-dont-sync-from-common-data-service-to-talent-369608"></a>无法将请假详细信息从 Common Data Service 同步到 Talent (369608)

应用这些更改之后，Common Data Service 中更新的请假详细信息将同步回 Talent。

### <a name="job-description-doesnt-display-for-the-job-in-the-skill-gap-analysis-page-369398"></a>“技能差距分析”页中不显示工作的工作描述 (369398)

在本周的版本中，在**技能差距分析**页中选择工作时，将显示此描述。

## <a name="coming-soon"></a>即将到期

### <a name="print-performance-reviews"></a>打印绩效复查

员工、经理和 HR 专业人员可以打印员工的绩效复查。
