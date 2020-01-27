---
title: Dynamics 365 Talent（2019 年 6 月 25 日）新增功能或更改
description: 此主题介绍了 Microsoft Dynamics 365 Talent 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 06/25/2019
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
ms.search.validFrom: 2019-06-25
ms.dyn365.ops.version: Talent
ms.openlocfilehash: b01033ad52ba8881134d21883e50bc5ccbcdeb33
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/06/2019
ms.locfileid: "2896857"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-june-25-2019"></a>Dynamics 365 Talent（2019 年 6 月 25 日）新增功能或更改

此主题介绍了 Microsoft Dynamics 365 Talent 中的新增功能和更改的功能。

## <a name="changes-in-attract"></a>Attract 中的更改

本版本中包含 Dynamics 365 Talent: Attract 的小缺陷修复。

## <a name="coming-soon-in-attract"></a>Attract 中即将推出

### <a name="job-approvals-appear-on-the-home-page"></a>主页中显示工作审核

仪表板的**审核**部分中将显示审核。 审核人可以在**已分配给您**（其中显示工作 ID、工作头衔、其他审核人和作业的分配日期）下查看自己的审核。 提交待审核工作的用户可以在**您请求的**（其中显示仍然必须审核提交的工作的审核者）下查看自己的工作。

## <a name="changes-in-onboard"></a>Onboard 中的更改
本版本中包含 Dynamics 365 Talent: Onboard 的小缺陷修复。

## <a name="changes-in-core-hr"></a>Core HR 中的更改

本部分中的更改适用于内部版本号 8.1.2357。

### <a name="incorrect-value-displayed-for-primary-position-314266"></a>为主要职位显示的值不正确 (314266)

这些更改将在所有页上一致显示**主要职位**设置。

### <a name="cant-edit-after-recalling-the-workflow-in-review-318180"></a>撤消工作流后不能在“复查”中编辑 (318180)

现在可编辑已通过工作流撤消的复查。

### <a name="final-comments-field-in-reviews-isnt-translated-325921"></a>“复查”中的“最终注释”字段不翻译 (325921)

Talent 中现在将翻译**最终注释**标签。

### <a name="preview-features-will-be-enabled-only-in-sandbox-environments"></a>仅在沙盒环境中才会启用预览功能。

配置新的 Talent 实例时，可指示实例类型为**生产**还是**沙盒**。 **沙盒**实例类型可用于提前测试新功能。 将把所有现有 Talent 实例更新为**生产**实例类型。 如果需要将现有实例之一更新为**沙盒**实例类型，请联系[支持](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support)以发起更改请求。

有关如何发布更改的详细信息，请参阅[配置 Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent)。

## <a name="in-preview"></a>预览模式

### <a name="restrict-the-leave-types-in-time-off-requests"></a>限制请假中的休假类型

组织可以为员工提供多种休假类型。 但是，可能不适合员工提交某些休假类型的请假。 可以改用人力资源 (HR) 管理这些休假类型。 在此版本中，可以配置员工可以提交哪些休假类型的请假。 

## <a name="coming-soon-in-core-hr"></a>Core HR 中即将推出

### <a name="feature-management-area-in-talent"></a>Talent 中的功能管理区域

将从**系统管理**移除**功能管理**，因为此功能有问题。 以后的版本中将重新引入**功能管理**。 

### <a name="common-data-service-entity-support-for-custom-fields"></a>Common Data Service 实体对自定义字段的支持

以下实体将支持自定义字段：**工资单收入代码**、**固定薪酬事件**、**薪酬网格**、**付薪期间**和**薪酬参考点**。 

### <a name="new-common-data-service-entities"></a>新增 Common Data Service 实体

将向 Common Data Service 添加**原因代码**实体。

### <a name="view-performance-information-for-direct-and-extended-reports-in-manager-self-service"></a>在经理自助服务中查看直接报表和扩展报表的性能信息

经理可通过一个新选项查看直接报表和扩展报表的绩效。 现在，职能经理可以分配和更新绩效目标和颁发新审核。 此外，直属经理及其员工可维护和更新绩效日记帐，以帮助确保绩效复查流程顺利进行。 实施此更改后，除了直接报表，经理还可以查看和维护与其扩展报表的绩效有关的信息。

### <a name="print-performance-reviews"></a>打印绩效复查

员工、经理和 HR 可以打印员工的绩效复查。
