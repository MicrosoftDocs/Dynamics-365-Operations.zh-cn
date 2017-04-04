---
title: "折旧帐簿概览升级"
description: "在以前的版本中，有两种评估概念对于固定资产-价值模型和折旧帐簿。 在 Microsoft Dynamics 365 for Operations 版本 1611 中，价值模型功能和折旧帐簿功能已经合并为一个概念，即帐簿。 本主题介绍升级时的考虑事项。"
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer
ms.search.scope: Operations, Core
ms.custom: 221624
ms.assetid: cf434099-36f9-4b0f-a7c8-bed091e34f39
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: bec019d218d80ba059d5a1c232072f46b1ae3ee2
ms.openlocfilehash: d29cb7bc5acc29be93332b4211adebc4486a7a25
ms.lasthandoff: 03/31/2017


---

# <a name="depreciation-book-upgrade-overview"></a>折旧帐簿概览升级

在以前的版本中，有两种评估概念对于固定资产-价值模型和折旧帐簿。 在 Microsoft Dynamics 365 for Operations 版本 1611 中，价值模型功能和折旧帐簿功能已经合并为一个概念，即帐簿。 本主题介绍升级时的考虑事项。 

升级流程会将您的现有设置和所有现有交易记录移动到新的帐簿结构。 价值模型将依照保留当前状态，作为过帐到总帐的帐簿。 折旧帐簿将移至“**过帐到总帐**”设置为“**否**”的帐簿。 折旧帐簿日志名称要移到与设置的过帐层的总帐日志名称** ** "无"。 折旧帐簿交易记录要移到固定资产交易记录。 

在运行数据升级之前，应了解将折旧帐簿日志行升级到交易记录凭证的两个选项以及凭证系列将要使用的编号规则。 

选项 1：**系统定义的编号规则** -这是优化升级性能的默认选项。 升级不使用编号规则框架，而是使用基于设置的方法分配凭证。 在升级，新编号规则将创建具有基于升级的交易记录后设置** **下一个编号正确的。 默认情况下，使用的编号规则 FADBUpgr 在\#\#\#\#\#\#\#\#\# 格式。 有一些参数可供您调整的格式，在使用此方法时：

-   ** **编号规则代码–标识编号规则代码。 因为将按照升级，创建此编号规则代码不能存在。
    -   常量名称：**NumberSequenceDefaultCode**
    -   默认值："FADBUpgr"
-   **前缀** - 将用作凭证号前缀的常量字符串。
    -   常量名称：**NumberSequenceDefaultParameterPrefix**
    -   默认值："FADBUpgr"
-   **字母数字的长度** – 编号规则的字母数字段的长度。
    -   定额的名称：** NumberSequenceDefaultParameterAlpanumericLength **
    -   默认值：9
-   **开始编号** - 编号规则要使用的第一个数字。
    -   定额的名称：** NumberSequenceDefaultParameterStartNumber **
    -   默认值：1

选项 2:**现有的用户定义的编号规则** -此选项允许您定义用于升级要使用的编号规则。 如果需要更高级的配置编号规则，则可以考虑使用此选项。 若要使用编号规则，必须升级 ReleaseUpdateDB70 类修改具有以下信息的\_FixedAssetJournalDepBookRemovalDepBookJournalTrans:

-   **编号规则代码** – 编号规则的代码。
    -   定额的名称：** NumberSequenceExistingCode **
    -   默认值：无默认值，必须更新到编号规则代码。
-   **共享编号规则** – 标识编号规则的作用域的布尔值。 对所有公司的共享编号规则使用“true”，对特定公司的作用域使用“false”。 在使用“错误”，将使用指定的名称的编号规则必须位于包含折旧帐簿交易记录的各个公司中存在。 共享的编号规则存在包含折旧帐簿交易记录的每个部分。
    -   定额的名称：** NumberSequenceExistingIsShared **
    -   默认值：true

参数在 ReleaseUpdateDB70\_开头 FixedAssetJournalDepBookRemovalDepBookJournalTrans 类中。 

*请指定 allocation*错误 
凭证 
更可提供的方法*，请为，如果要使用现有的编号规则 code* * 
的，但是，如果您想要使用系统中定义的编号规则 (默认) * const 布尔型 NumberSequenceUseExistingCode =错误；  

*，则使用系统中定义的编号规则 sequence.*编号方法，它
请指定参数*新编号规则将创建具有这些 parameters.* const str NumberSequenceDefaultCode =“FADBUpgr”;const str NumberSequenceDefaultParameterPrefix =“FADBUpgr”;const int NumberSequenceDefaultParameterAlpanumericLength = 9;const int NumberSequenceDefaultParameterStartNumber = 1;   

*，则使用现有编号规则方法，指定现有的编号规则 code.* * 
凭证分配要保持现有的编号的 sequences.*行由行 const str NumberSequenceExistingCode = ";*请指定现有的编号规则 code*错误 
作用域*，请为，如果指定的编号规则的 shared*， 
*，如果指定的编号规则的 per-company* * 
将使用默认系统定义的编号规则，则将使用指定的作用域的编号规则代码不是 found.* const boolean NumberSequenceExistingIsShared = true; 

修改常量后重新构建含有类的项目。 

在使用系统生成的编号规则方法时 (可选)，1 升级将使用分配凭证号基于设置的处理在升级脚本电影写中指定参数。 在以后分配它还将创建具有指定的参数的新编号规则。 

使用用户定义的现有编号规则方法（选项 2）时，数据升级检查具有折旧帐簿交易记录的每个分区和公司的数据库中是否存在具有指定作用域的编号规则。 如果它存在，则升级将用于处理的行由行分配凭证号。指定按编号规则使用编号规则框架。 如果编号规则存在不使用指定的作用域，升级系统将使用默认定义的编号规则分配凭证号方法和分配。此后创建使用指定的默认参数的新编号规则。

无论使用任何一种方法，数据升级脚本都会使用为以前的折旧帐簿日记帐名称创建的新总帐日记帐名称上的“**凭证系列**”字段的编号规则。


