---
title: Dynamics 365 for Talent（2019 年 2 月 7 日）中的新增功能或更改
description: 此主题介绍了 Microsoft Dynamics 365 for Talent 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 02/07/2019
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
ms.search.validFrom: 2019-02-07
ms.dyn365.ops.version: Talent
ms.openlocfilehash: b89fc15130755a80b56f26cf7c61674a26f43e36
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517400"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-february-7-2019"></a>Dynamics 365 for Talent（2019 年 2 月 7 日）中的新增功能或更改

[!include [banner](includes/banner.md)]

此主题介绍了 Talent 中的新增功能和更改的功能。

## <a name="changes-in-attract"></a>Attract 中的更改

### <a name="interview-scheduling-enhancements"></a>面试计划增强
端对端面试计划体验已改进。 现在可查看内部应聘者的日历可用日期，并可以使用内部应聘者的日历来获取计划建议。 有关详细信息，请参阅[面试计划和反馈](interview-scheduling-feedback.md)。

### <a name="job-posting-to-linkedin--company-mismatch-issue-fixed"></a>工作发布到 LinkedIn – 已解决了公司不匹配问题
已解决了从 Attract 发布到LinkedIn 的工作在错误的公司名下显示这一问题。 有关详细信息，请参阅[在 Attract 中创建、审核和发布工作](creating-jobs-attract.md)。

### <a name="career-site-url-displayed-in-admin-settings"></a>求职站点 URL 在“管理员设置”中显示
求职站点主页 URL 现在在**求职站点管理**下的**管理员设置**中显示。

## <a name="changes-in-core-hr"></a>Core HR 中的更改

**内部版本 8.1.2134**

### <a name="multiple-compensation-levels-supported-on-jobs"></a>工作支持多个薪酬级别
可通过此更改为某个工作定义多个薪酬级别，从而在使用该工作时支持计划之间可能不同的员工固定薪酬范围。 

例如:    
*工作* - 客户经理*关联的薪酬级别：* B1 和 B2 - 每个级别都有一个定义的值范围。 B1 = 最低为 50,000，中等为 60,000，最高为 75,000，B2 = 最低为 65,000，中等为 74,000，最高为 85,000。 根据定义的资格规则为员工创建固定薪酬时，每个固定计划现在可指向同一个工作和该工作的不同级别。 这样就可以在不同区域/国家或地区中定义计划，并且计划可指向不含重复工作但范围不同的同一个工作，以考虑这些差异。

### <a name="compensation-level-field-has-been-added-to-the-employee-fixed-compensation-entity"></a>已向员工固定薪酬实体添加了薪酬级别字段。 
通过此更新，已将员工固定薪酬实体更新为包含**薪酬级别**字段。 通过添加此项功能，可以更轻松地更新员工固定薪酬计划。 

### <a name="update-job-family-when-updating-and-creating-new-positions"></a>更新和新建职位时更新工作系列
更改某项职位的工作时，**工作系列**现在默认基于所选工作。

### <a name="performance-improvements-when-rendering-workspaces"></a>呈现工作区方面的性能改进
仅当访问这些页面时，才加载工作区中的分析选项卡。 首次呈现页面时，将在页面的左上角显示一个指示器。
