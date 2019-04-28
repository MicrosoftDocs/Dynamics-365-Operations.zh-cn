---
title: 追踪应聘者个人资料和申请的来源
description: 本主题提供有关跟踪应聘者个人资料和申请来源的信息。
author: hachandr
manager: AnnBe
ms.date: 03/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: ebc82ada31d2803800358cd9aecfe389ada8f0dc
ms.sourcegitcommit: dd1e1636d351a15f9c1b6808bea359417a9bd690
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/25/2019
ms.locfileid: "897448"
---
# <a name="track-sources-for-candidate-profiles-and-applications"></a>追踪应聘者个人资料和申请的来源 

[!include[banner](../includes/banner.md)]

> [!NOTE] 
> 本主题中介绍的功能作为预览版的一部分提供给目标用户。 内容和功能可能会发生变化。 若要使用此功能，请让管理员使用 Attract 中的**管理员设置**启用。 将来的版本将提供资源跟踪报告。 有关详细信息，请参阅[访问 Talent 中的预览功能](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/access-preview-feature)。

应聘者申请工作时，Attract 将自动跟踪其申请来源，并为您提供宝贵的信息来帮助您的招聘工作不走弯路。 招聘人员或招聘经理也可以在手动向工作或人才池添加应聘者时选择申请来源。

可以在**活动**选项卡下的申请活动详细信息中和人才池的**个人资料**下的申请历史记录中查看申请来源。 可以在申请和人才池中**个人资料**选项卡下的应聘者详细信息内找到应聘者的个人资料来源。

> [!NOTE] 
> 可以在[综合招聘加载项](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/attract-comprehensive-hiring)中找到流程模板。

## <a name="pre-configured-sources"></a>预配置来源

默认来源列表中包含常见申请来源。 某些来源类型（如**招聘公告**和**社交网络**）中包含更多来源详细信息。 例如，**社交网络**包括 Facebook 和 Twitter。 **引荐**来源类型允许您指定内部员工为引荐人。 默认来源列表中包含下面的预配置来源：

-   Attract 求职站点

-   机构

-   招聘会

-   公司市场营销

-   会议和展览会

-   专业协会

-   招聘公告

    -   Indeed

    -   Seek

    -   CareerBuilder

    -   Google Jobs

    -   Xing

    -   Glassdoor

    -   Monster Jobs

-   杂志和出版物

-   社交网络

    -   Facebook

    -   Twitter

-   大学校园招聘

-   LinkedIn

-   分类广告

-   分派

-   预配置添加的来源

-   其他

## <a name="customize-the-source-list"></a>自定义来源列表 

可以扩展来源列表以包括更多申请来源。 若要自定义此列表，请按照[扩展 Attract 中的选项集](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/extensibility-attract#extending-option-sets-in-attract)中的说明操作。 单击 **TalentSource** 实体可添加更多来源。 

若要避免对用户界面 (UI) 造成负面影响，,请勿编辑或删除以下对象的 **TalentCategory** 枚举值（而不是名称）：

- **分派**
- **LinkedIn**
- **其他**

而是扩展 **TalentSource** 枚举以添加其他来源类型。
