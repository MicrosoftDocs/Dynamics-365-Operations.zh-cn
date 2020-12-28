---
title: Dynamics 365 Talent 的新增功能或更改（2019 年 7 月 30 日）
description: 此主题介绍了 Microsoft Dynamics 365 Talent 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 07/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 311042caf6a391a06c7e2d8c4c2c2f6e1f855437
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460482"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-july-30-2019"></a>Dynamics 365 Talent 的新增功能或更改（2019 年 7 月 30 日）

此主题介绍了 Dynamics 365 Talent 中的新增功能和更改的功能。

## <a name="changes-in-attract"></a>Attract 中的更改
本版本中包含 Dynamics 365 Talent: Attract 的小缺陷修复。

## <a name="changes-in-onboard"></a>Onboard 中的更改
本版本中包含 Dynamics 365 Talent: Onboard 的小缺陷修复。

## <a name="changes-in-core-hr"></a>Core HR 中的更改
本部分中的更改适用于内部版本号 8.1.2409。


### <a name="region-support-for-canada-and-southeast-asia"></a>加拿大和东南亚的地区支持

我们很高兴地宣布，加拿大和东南亚地区将于 2019 年 8 月 1 日推出 Talent。 通过此更改，您可以在加拿大和亚洲地区创建环境，并且所有 Talent 数据将仅在这些位置内维护。 您可以通过在“新建环境”对话框中选择位置来在这些新地区创建环境，并使用该环境在 LCS 中配置 Talent，如[配置 Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent) 中所述。

不支持将现有项目的数据从其他地区迁移到加拿大和亚洲地区。 仅新项目可以配置到这些新的支持地区。

### <a name="new-active-positions-list-page"></a>新的有效职位列表页

基于位置的列表的选项现在包括：**所有职位**、**有效职位**、**空缺职位** 和 **无效职位**。 新的 **有效职位** 列表页面仅显示截至当前日期的有效位置（空缺或已填补）。 

### <a name="allow-course-participants-to-be-added-to-open-courses"></a>允许课程参与者被添加到开设的课程

本周的更改更正了仅直接下属可以注册开设的课程的问题。

### <a name="fte-analysis-displaying-incorrect-fte-number"></a>FTE 分析显示不正确的 FTE 编号

**FTE 分析** 已在 **人事管理** 的 **分析** 选项卡中得到更正。

### <a name="final-comments-label-translation"></a>最终注释标签翻译

**最终注释** 标签现在在审核窗体中翻译。

## <a name="in-preview"></a>预览模式

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>只有沙盒实例中才会启用预览功能

配置新的 Talent 实例时，可指定实例类型为 **生产** 还是 **沙盒**。 **沙盒** 类型的实例可用于提前测试新功能。 将把所有现有 Talent 实例更新为 **生产** 实例类型。 如果需要将现有实例之一更新为 **沙盒** 实例类型，请联系[支持](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support)以发起更改请求。

有关如何发布更改的详细信息，请参阅[配置 Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent)。

### <a name="view-extended-information-for-performance-in-manager-self-service"></a>在经理自助服务中查看绩效的更多信息

经理可通过一个新选项查看直接报表和扩展报表的绩效。 现在，职能经理可以分配和更新绩效目标和颁发新审核。 此外，直属经理及其员工可维护和更新绩效日记帐，以帮助确保绩效复查流程顺利进行。 实施此更改后，除了直接报表，经理还可以查看和维护与其扩展报表的绩效有关的信息。
