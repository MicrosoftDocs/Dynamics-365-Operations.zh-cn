---
title: Dynamics 365 Talent 的新增功能或更改（2019 年 7 月 23 日）
description: 此主题介绍了 Microsoft Dynamics 365 Talent 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 07/23/2019
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
ms.search.validFrom: 2019-07-23
ms.dyn365.ops.version: Talent
ms.openlocfilehash: ffbb29fb89ed6a3fd6db11f2c8d656ab565c43f3
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897641"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-july-23-2019"></a>Dynamics 365 Talent 的新增功能或更改（2019 年 7 月 23 日）

此主题介绍了 Dynamics 365 Talent 中的新增功能和更改的功能。

## <a name="changes-in-attract"></a>Attract 中的更改

### <a name="pdf-renderer-for-candidate-documents"></a>应聘者文档的 PDF 渲染器

Attract 用户现在可以在文档查看器中查看应聘者的 PDF 附件，而不是下载附件。

### <a name="signing-up-for-attract-user-research-group"></a>注册加入 Attract 用户研究组 

在我们规划新产品功能或发布预览功能时，我们也在寻找能够帮助指引我们的方向的用户。 感兴趣的用户现在可以使用我们应用中的注册链接注册成为我们用户研究组的成员。

### <a name="job-approvals-appear-on-the-home-page"></a>主页中显示工作审核

仪表板的**审核**部分中将显示审核。 审核人可以在**已分配给您**（其中显示工作 ID、工作头衔、其他审核人和作业的分配日期）下查看自己的审核。 提交待审核工作的用户可以在**您请求的**（其中显示仍然必须审核提交的工作的审核者）下查看自己的工作。

## <a name="changes-in-onboard"></a>Onboard 中的更改
本版本中包含 Dynamics 365 Talent: Onboard 的小缺陷修复。

## <a name="changes-in-core-hr"></a>Core HR 中的更改
本部分中的更改适用于内部版本号 8.1.2394。

### <a name="entity-support-for-custom-fields-in-common-data-service"></a>Common Data Service 中自定义字段的实体支持 

在此版本中，**工作日历**和**工作日历**天现在在 Common Data Service 中支持自定义字段。

### <a name="restrict-leave-types-in-time-off-requests"></a>限制请假中的休假类型

组织可以为员工提供多种不同的休假类型。 但是，可能不适合员工提交某些休假类型的请假。 可以改用 HR 管理这些休假类型。 在此版本中，可以配置员工可以提交哪些休假类型的请假。 

## <a name="in-preview"></a>预览模式

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>只有沙盒实例中才会启用预览功能

配置新的 Talent 实例时，可指定实例类型为**生产**还是**沙盒**。 **沙盒**类型的实例可用于提前测试新功能。 将把所有现有 Talent 实例更新为**生产**实例类型。 如果需要将现有实例之一更新为**沙盒**实例类型，请联系[支持](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support)以发起更改请求。

有关如何发布更改的详细信息，请参阅[配置 Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent)。

### <a name="view-extended-information-for-performance-in-manager-self-service"></a>在经理自助服务中查看绩效的更多信息

经理可通过一个新选项查看直接报表和扩展报表的绩效。 现在，职能经理可以分配和更新绩效目标和颁发新审核，与其员工一起管理。 此外，直属经理及其员工可维护和更新绩效日记帐，以帮助确保绩效复查流程顺利进行。 实施此更改后，除了直接报表，经理还可以查看和维护与其扩展报表的绩效有关的信息。 

## <a name="coming-soon"></a>即将到期

### <a name="region-support-for-canada-and-southeast-asia"></a>加拿大和东南亚的地区支持

我们很高兴地宣布，加拿大和东南亚地区将于 2019 年 8 月 1 日推出 Talent。 通过此更改，您可以在加拿大和亚洲地区创建环境，并且所有 Talent 数据将仅在这些位置内维护。 您可以通过在“新建环境”对话框中选择位置来在这些新地区创建环境，并使用该环境在 LCS 中配置 Talent，如[配置 Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent) 中所述。

不支持将现有项目的数据从其他地区迁移到加拿大和亚洲地区。 仅新项目可以配置到这些新的支持地区。
