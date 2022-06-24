---
title: 查看和评估调查表的结果
description: 本文介绍如何查看和评估回应者完成的调查表的结果。
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: KMCollection, KMKnowledgeCollectorCollection, KMKnowledgeCollectorUserResults, HcmLearningWorkspace
audience: Application User
ms.custom: 17444
ms.assetid: 6570206a-b2c4-4025-8715-432fe6652b78
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 45be2fb7761a3022795a196b140987fcbd732a33
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855125"
---
# <a name="view-and-evaluate-the-results-of-questionnaires"></a>查看和评估调查表的结果


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本文介绍如何查看和评估回应者完成的调查表的结果。 

调查对象完成调查表后，您可以以下列方式查看和评估调查表结果：

-   **完成的回答会话** - 查看有关回应者已完成的调查表的详细信息，并生成用于总结回答和所得所有分数的报表。
-   **结果组** - 查看调查表的结果组详细信息和统计信息。 结果组统计信息可针对调查表的一个回答会话生成，也可以针对所有回答会话生成。
-   **调查表统计信息** - 指定用于计算特定回应者组的统计信息的条件。

您也可以生成各种报表，以便按人员、回答会话或结果组顺序查看结果。 可使用以下与完成的调查表相关的报表：

-   结果
-   调查表答卷
-   个人答卷
-   反馈分析

## <a name="answer-session-results"></a>回答会话结果

调查对象完成调查表后，您可以查看完成的回答会话结果。 回答会话是一个用户对调查表的响应。 您可以在 **答卷** 页面上查看有关完成的回答会话的详细信息。 **答卷** 页面上包含的回答会话将以各种方式进行筛选，具体取决于您打开此页面的方式：

-   全部调查表
-   特定调查表
-   特定人员

在 **答卷** 页面中，您可以查看有关回答、所得分数、回应者在每个结果组中的响应以及用于选定调查表的问题层次结构（如果已使用）的详细信息。 您也可以生成和打印以下报告：

-   **结果报表** - 此报表显示针对所选回答会话的每个结果组中所得分数的图形表示形式。
-   **答卷报表** - 此报表显示针对调查表上每个问题选择的回应者的回答。
-   **不正确回答** - 此报表显示与回应者所选的不正确回答相关的信息。

> [!NOTE]
> **结果** 报表仅在您在调查表上使用结果组并已在 **调查表** 页面上选择 **结果页面** 时可用。 **答卷** 报表和 **不正确回答** 报表仅在您已在 **调查表** 页面上选择 **答卷报表** 时可用。

## <a name="questionnaire-statistics"></a>调查表统计

您可以使用调查表统计分析基于您定义的计算的已完成的调查表的结果。 要定义计算，必须完成以下任务：

-   选择条件计算并显示该统计。
    -   您可以按调查表、问题、问题行或结果组显示统计。
    -   选择在查看结果时将使用的图表类型。
    -   选择网络中要包括其回答的人员的类型，如员工、联系人或申请人。 还可以包括从完成后匿名的调查表的回答。
    -   设置基于年限或资历分析结果的间隔。
-   选择或验证细化统计主题的设置。 例如，通过选择邮政编码，您可以分析某个特定地理区域内所有回应者的结果。
-   选择或验证标准以按回应者或调查表特征分析结果。 例如，通过选择 **邮政编码**，您可以分析回应者的位置和正确回答之间的相关性。

您定义的设置将被保存下来并且可用于定期重新计算结果。

[!INCLUDE[footer-include](../includes/footer-banner.md)]
