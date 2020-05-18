---
title: Dynamics 365 Human Resources 中的新增功能或更改（2020 年 5 月 1 日）
description: 本文介绍 Microsoft Dynamics 365 Human Resources 中的新增功能或更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 05/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f1a0cfd1c1b0dcc9defaad7e4cce22ebe1e91fae
ms.sourcegitcommit: cc5dc0bd90277f1ba684dd310da3274886ce573c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/29/2020
ms.locfileid: "3320911"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-1-2020"></a>Dynamics 365 Human Resources 中的新增功能或更改（2020 年 5 月 1 日）

本文介绍 Dynamics 365 Human Resources 中的新增功能或更改的功能。 更改适用于内部版本号 8.1.3196。 某些标题中括号内的数字是 LCS 支持号码，供您参考。

## <a name="new-performance-management-entities-available-in-data-management-framework-dmf"></a>数据管理框架 (DMF) 中提供了新的绩效管理实体

以下实体现在可用。 如果发现实体列表中未列出这些实体，请使用**框架参数 > 实体设置 > 刷新实体列表**中的**刷新实体**选项。

- **讨论资格**
- **讨论目标**
- **讨论度量**
- **讨论主题**
- **绩效日记帐**
- **量化指标**
- **目标度量**

此外，**总分**和**平均分数**已添加到**讨论**实体中。

## <a name="increase-length-of-leave-request-comments-275641"></a>增加休假请求长度注释 (275641)

现在，关于休假请求的注释可以超过 100 个字符。

## <a name="final-comments-on-reviews-dont-appear-when-the-manager-or-employee-is-signed-into-a-different-company-431688"></a>当经理或员工登录到其他公司后，不会出现对审核的最终注释 (431688)

现在，在查看审核时将显示所有注释。

## <a name="user-defined-links-arent-supported-on-new-worker-form-390374"></a>新的工作人员窗体不支持用户定义的链接 (390374)

现在，简化的**工作人员**窗体支持用户定义的链接。

## <a name="hcmratinglevelentity-causes-odata-api-crash-439476"></a>HcmRatingLevelEntity 导致 OData API 崩溃 (439476)

此更改可更正 API 崩溃错误。 重复的名称引起了此错误。

## <a name="in-preview"></a>预览模式

## <a name="leave-suspension"></a>休假暂停

可在 Human Resources 中暂停员工的休假和缺勤。 暂停休假将停止所选休假类型的休假应计。 如果处理了应计后发生暂停，暂停休假将为员工的休假余额创建按比例调整。 有关详细信息，请参阅[暂停休假](hr-leave-and-absence-suspend-leave.md)。

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a>更新用户体验以表明应计已暂停 (429550)

用户体验现在表明计划已暂停应计。

## <a name="suspend-leave-accrual-for-specified-leave-types-272447"></a>暂停指定休假类型的休假应计 (272447)

在此版本中，HR 可以创建一个规则，以针对输入了无薪假休假请求的员工暂停休假应计。 无薪假可以是一种类型，但不是必须的。 您可以根据其他休假类型暂停任何休假。

## <a name="dmf-entity-available-for-accrual-suspensions-429549"></a>可用于暂停应计的 DMF 实体 (429549)

DMF 实体现在可用于暂停应计。

## <a name="add-reason-code-to-accrual-suspensions-429547"></a>将原因代码添加到应计暂停 (429547)

原因代码已添加到应计暂停。

## <a name="begin-transitioning-from-human-resources-parameters-to-leave-and-absence-parameters"></a>开始从人力资源参数转换到休假和缺勤参数

此版本开始将人力资源参数与休假和缺勤参数进行合并。

## <a name="carry-forward-rules"></a>结转规则

可为转移了结转调整的结转余额指定结转休假类型。 例如，如果员工结转 10 天，则可为这 10 天选择其他休假类型。 有关详细信息，请参阅[配置休假和缺勤类型](hr-leave-and-absence-types.md)。

## <a name="known-issues"></a>已知问题

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a>SharePoint 预览在某些环境下不起作用

如果 SharePoint 中存储的文档的文档预览不起作用，请尝试以下过程：

1. 验证管理员用户帐户是否具有与用户记录关联的电子邮件。 可在**用户**页面查看这些信息。 如果未设置电子邮件，则需要使用 OData Excel 加载项添加电子邮件和提供程序。 默认情况下，Excel 设计中不显示电子邮件地址。 您需要编辑 Excel 设计，添加所有字段，然后应用并刷新。 完成这些步骤后，您可以更新管理员帐户。

2. 管理员帐户具有关联的电子邮件帐户后，使用管理员凭据登录到 Human Resources。

3. 访问 SharePoint 中的附件启动文档预览。

4. 使用有权访问附件的另一个用户帐户登录，然后验证预览是否按预期工作。