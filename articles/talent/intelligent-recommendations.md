---
title: Attract 中的智能建议
description: 本文说明如何在 Microsoft Dynamics 365 Talent - Attract 使用机器学习来为工作和工作应聘者提供建议。
author: andreabichsel
manager: AnnBe
ms.date: 05/16/2019
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
ms.openlocfilehash: fa06821c98e42dcd8590a764db9beb4a5c33fca2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460402"
---
# <a name="intelligent-recommendations-in-attract"></a>Attract 中的智能建议

[!include [banner](includes/banner.md)]

机器学习能够帮助招聘人员和招聘经理快速发现最适合职位的应聘者。 它还可以帮助应聘者找到最适合其个人资料和兴趣的职位。 使用这些功能并且提供反馈，推荐将有所改善。

> [!NOTE] 
> - 智能推荐功能仅通过[综合招聘加载项](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring)提供。
> - 本主题中介绍的功能作为预览版的一部分提供给目标用户。 内容和功能可能会发生变化。 若要使用此功能，请让管理员使用 Attract 中的 **管理中心** 启用。 将 **应聘者推荐**、**工作推荐** 和 **潜在人选推荐** 设置为 **开**。 有关详细信息，请参阅[访问 Microsoft Dynamics 365 Talent 中的预览功能](./access-preview-feature.md)。 


## <a name="candidate-recommendations"></a>应聘者推荐

由于工作发布可能吸引成百上千个申请人，对于招聘人员和招聘经理来说找到技能和背景最适合职位的应聘者很难。 通过分析工作描述和要求之间的相关性，以及来自应聘者简历和个人资料的数据，机器学习可以用于生成应聘者推荐。 应聘者推荐可以帮助招聘人员和招聘经理发现最适合的人才，并快速地将他们移至面试阶段。 对于任何工作，如果有超过十名应聘者有简历或完整的个人资料，与工作要求最接近的应聘者将显示在 **工作** 页的 **要考虑的申请人** 部分。

对于任何推荐的应聘者，您都可以选择应聘者卡上的 **查看应聘者** 来查看该应聘者的个人资料并对其申请采取行动。 您可以使用省略号按钮 (**...**) 在新选项卡上打开应聘者的个人资料。您还可以使用省略号按钮提供有关推荐的反馈。 这样，您可以帮助优化推荐引擎并改进将来的推荐。 您不想要的任何推荐在您刷新 **工作** 页时将从 **要考虑的申请人** 部分删除。 您可以使用反馈卡表示为何未找到有用的推荐。

## <a name="job-recommendations"></a>工作推荐 

在潜在的员工使用求职站点申请工作时，Attract 将推荐组织中的其他空缺职位。 这些推荐基于潜在人选过去的申请表，以及简历或应聘者个人资料。 因此，工作推荐帮助应聘者快速发现最适合自己的工作。 如果有超过十个工作在求职站点上发布，将为应聘者提供工作推荐。 应聘者可以从推荐卡打开工作发布的详细信息。 他们还可以提供有关推荐的反馈以帮助改进将来的推荐。

## <a name="prospect-recommendations"></a>潜在人选推荐 

新职位开放时，浏览所有过去的申请人和整个人才网络可能需要一段时间。 若要让 Attract 帮助您执行此操作，可使用智能机器学习算法。 这意味着在您创建工作帐户，Attract 将立即查看所有应聘者，并推荐匹配度高的应聘者。 若要查看这些推荐，请为工作启用 **潜在人选** 阶段。 Attract 可能需要最多一分钟扫描整个应聘者数据库来作出推荐。

将在已启用了 **潜在人选** 阶段的所有工作的 **潜在人选** 选项卡上以卡的形式显示建议。 这些卡列出潜在人选的个人资料中发现的技能，以及所有教育资格信息。 如果找到您喜欢的建议，可以将应聘者作为该工作的潜在人选添加。

> [!NOTE]
> 如果现在已开始使用 Attract，则需要等到有 10 个或更多具有完整个人资料或简历的申请人，才能使用此功能。

为了避免推荐中存在潜在偏见，Attract 仅扫描应聘者个人资料以查找技能、资格和其他与工作描述匹配的关键字。 此外，Attract 还会在评估之前从应聘者个人资料中删除个人身份信息。
