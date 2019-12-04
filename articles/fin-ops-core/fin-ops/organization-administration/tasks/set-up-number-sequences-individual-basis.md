---
title: 逐个设置编号规则
description: 本主题介绍如何逐个设置编号规则。
author: sericks007
manager: AnnBe
ms.date: 08/16/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: NumberSequenceTableListPage, NumberSequenceDetails
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 818e641d19444e94a287134b68b25d52a05021d0
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189859"
---
# <a name="set-up-number-sequences-on-an-individual-basis"></a>逐个设置编号规则

[!include [task guide banner](../../includes/task-guide-banner.md)]

本主题介绍如何逐个设置编号规则。 “数序”被用于为需要它们的主数据记录和交易记录记录生成可读的唯一的标识符。 需要标识符的主数据或交易记录称为“参考”。 在您能为一个参考创建新记录之前，您必须设置编号规则并将其与参考相关联。 您可以通过使用**设置编号规则**向导同时设置所有需要的编号规则，或者您可以通过使用**编号规则**页面修改各个编号规则。

1. 转到**导航窗格 > 模块 > 组织管理 > 标号规则 > 编号规则**。
2. 选择**编号规则**。
3. 在**编号规则代码**字段中，键入一个值。
4. 在**名称**字段中，键入一个值。
5. 在**范围参数**快速选项卡上，为该编号规则选择范围，然后从下拉列表选择范围值。 该范围定义了使用该编号规则的组织。 此外，具有一个范围而不是**共享**的编号规则可能具有与它们的范围对应的段。 例如，具有**法人**范围的编号规则可能包含法人段。 有关范围的详细信息，请参阅[编号规则概览](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/number-sequence-overview)。 
6. 展开**分段**部分。
    - 通过添加、删除和重新排列段落为该编号规则定义格式。  
    - 所有范围的编号规则可以包含*常量段*和*字母数字段*。 “常量”段包含不更改的一组字母数字字符。 使用此段类型可以在编号规则段之间添加连字符或其他分隔符。 字母数字段包含数字标志 (#) 与和符号 (&) 的组合。 这些字符表示每次使用该规则的编号时的增量的字母和编号。 使用数字标志（#）指示递增的编号，使用符号（&）指示递增的字母。 例如，格式 `#####_2014` 创建了 `00001_2014`、`00002_2014` 等序列。 必须出现至少一个字母数字段。 公司或法人等范围段不是必需的。 但是，如果您不在此格式中包括范围段，每个范围仍会生成所选参考的编号。  
7. 展开**引用**部分。 选择此编号规则所分配到的文档类型或记录。 此步骤对于为特殊的应用程序使用模式而定义的规则而言是可选的。 在这些情况下，通过使用编号规则代码或 ID 的值而不是参考生成了新编号。 特殊的应用程序使用模式的示例是用于特定日志名称的凭证系列。 但是，我们建议您不要使用这类模式。  
8. 展开**常规**部分。 在“常规”快速选项卡上，指定该编号规则是手动的、连续的还是间断的。 此外，输入可以用于该编号规则的最小编号和最大编号。 我们建议不要将间断的编号规则更改为连续的编号规则。 该编号规则将不是真正意义上的连续。 此更改还可能导致数据库中重复键违规。 此外，连续编号规则在执行时会有更大的效果。   
9. 单击**保存**。
