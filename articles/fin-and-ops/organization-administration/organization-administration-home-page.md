---
title: 组织管理主页
description: 此主题指向可帮助您在组织中使用 Microsoft Dynamics 365 for Finance and Operations 的资源。
author: sericks007
manager: AnnBe
ms.date: 08/18/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 20421
ms.assetid: 7aa24a03-d172-47e9-81f8-ebd39e80bc60
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0a693529b55b66eb940f8215a336d5c4ae0acedd
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545848"
---
# <a name="organization-administration-home-page"></a>组织管理主页

[!include [banner](../includes/banner.md)]

此主题指向可帮助高级用户和管理员配置 Microsoft Dynamics 365 for Finance and Operations 的内容。 此内容将帮助他们配置系统，使其顺畅有效地为您的组织和业务工作。

此处列出的许多内容适用于在**组织管理**模块中的功能。 但是，有一些任务，如创建和使用记录模板，可以在任何模块中执行以帮助您的组织更加有效地运行。

## <a name="number-sequences"></a>编号规则

编号规则用于为需要标识符的主数据记录和交易记录生成可读的唯一标识符。 需要标识符的主数据记录或交易记录称为 *“参考”*。 在您能为一个参考创建新记录之前，您必须设置编号规则并将其与参考相关联。

- [编号规则概览](number-sequence-overview.md)
- [通过使用向导设置编号规则](tasks/set-up-number-sequences-wizard.md)（任务指南）
- [单个设置编号规则](tasks/set-up-number-sequences-individual-basis.md)（任务指南）

## <a name="organizations"></a>组织

组织是共同工作以执行业务流程的群体。 组织层次结构表示构成您的公司的组织之间的关系。

在 Finance and Operations 中设置组织和组织层次结构之前，请确保您已计划好您的业务将如何建模。 组织模型对 Finance and Operations 实施和业务流程有重大影响。

- [组织和组织层次结构](organizations-organizational-hierarchies.md)
- [规划组织层次结构](plan-organizational-hierarchy.md)
- [创建组织层次结构](tasks/create-organization-hierarchy.md)（任务指南）
- [创建法人](tasks/create-legal-entity.md)（任务指南）
- [创建运营单位](tasks/create-operating-unit.md)（任务指南）

## <a name="address-books"></a>通讯簿

全球通讯簿是必须为所有内部和外部人员及与公司往来的组织存储的主数据的集中存储库。 与当事方记录关联的数据包括当事方的名称、地址和联系信息。

在创建全球通讯簿后，您可以根据需要在您的组织中创建附加通讯簿，如组织中每个公司一个单独的通讯簿或每个经营范围一个单独的通讯簿。

- [全球通讯簿](overview-global-address-book.md)
- [计划如何配置全局通讯簿和附加通讯簿](plan-configuration-global-address-book-additional-address-books.md)
- [配置全球通讯簿](tasks/configure-global-address-book.md)
- [通讯簿常见问题](qa-address-books.md)

## <a name="workflow"></a>工作流

“工作流”是随 Finance and Operations 一起安装的系统，可以用于创建单独的“工作流”或业务流程。 当您创建工作流时，您通过显示谁必须完成任务、制定决策或批准文档指定单据如何在系统中流动或移动。

- [工作流概览](overview-workflow-system.md)
- [工作流元素](workflow-elements.md)
- [工作流操作](workflow-actions.md)
- [创建工作流](create-workflow.md)

## <a name="electronic-signatures"></a>电子签名

电子签名确认要启动或审核计算流程的人员的身份。 在一些行业中，电子签名与手写签名在法律上具有相同效力。 电子签名是一些受管制行业（如制药业、食品和饮料业以及航空和国防）的法规遵从性要求。

在 Finance and Operations 中，可以对关键业务流程使用电子签名。 一些流程具有内置电子签名功能。 还可以为任意数据库表和字段创建自定义签名要求。

- [电子签名概览](electronic-signature-overview.md)
- [设置电子签名](tasks/set-up-electronic-signatures.md)（任务指南）

## <a name="case-management"></a>案例管理

通过计划、跟踪和分析案例，您可以提出可用于类似问题的有效解决方案。 例如，当客户服务代表或人力资源通才创建案例时，他们可在知识文章中查找帮助他们更有效地处理或解决案例的信息。

- [案例管理概览](cases.md)
- [配置案例安全、流程和类别](plan-case-management.md)

## <a name="record-templates"></a>记录模板

记录模板有助于您更快捷地创建记录。 您可以创建报表模板，以便不必明确为每条记录输入常用字段值。

- [记录模板](record-templates.md)
- [创建记录模板以加快数据输入](../../dev-itpro/data-entities/tasks/create-record-template-facilitate-data-entry.md)（任务指南）
- [使用记录模板创建新记录](../../dev-itpro/data-entities/tasks/use-record-template-new-record.md)（任务指南）

## <a name="general-organization-administration"></a>常规组织管理

- [更改横幅或形象标识](../get-started/tasks/change-banner-or-logo.md)（任务指南）
- [配置文档管理](configure-document-management.md)
- [配置和发送电子邮件](configure-email.md)
- [日期/时间数据和时区](date-time-zones.md)
