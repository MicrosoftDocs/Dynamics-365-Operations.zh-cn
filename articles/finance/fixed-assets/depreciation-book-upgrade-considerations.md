---
title: 折旧帐簿升级概览
description: 在以前的版本中，固定资产有两种评估概念，价值模型和折旧帐簿。
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.custom: 221624
ms.assetid: cf434099-36f9-4b0f-a7c8-bed091e34f39
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: ffaeafa987c85aee17404fbfcf8c69c9699e2f3b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994982"
---
# <a name="depreciation-book-upgrade-overview"></a>折旧帐簿升级概览

[!include [banner](../includes/banner.md)]

在以前的版本中，固定资产有两种评估概念 - 价值模型和折旧帐簿。 在 Microsoft Dynamics 365 for Operations (1611) 中，价值模型功能和折旧帐簿功能已经合并为一个概念，即帐簿。 本主题介绍升级时的考虑事项。 

升级流程会将您的现有设置和所有现有交易记录移动到新的帐簿结构。 价值模型将依照保留当前状态，作为过帐到总帐的帐簿。 折旧帐簿将移至 **过帐到总帐** 设置为 **否** 的帐簿。 折旧帐簿日记帐名称将移动到过帐层设置为 **无** 的总帐日记帐名称。 折旧帐簿交易记录将移到固定资产交易记录。 

在运行数据升级之前，应了解将折旧帐簿日志行升级到交易记录凭证的两个选项以及凭证系列将要使用的编号规则。 

选项 1：**系统定义的编号规则** -这是优化升级性能的默认选项。 升级不使用编号规则框架，而是使用基于设置的方法分配凭证。 升级后，将基于升级的交易记录使用适当的 **下一个编号集** 创建新的编号规则。 默认情况下，编号规则将以 FADBUpgr\#\#\#\#\#\#\#\#\# 格式使用。 使用此方法时有一些参数可供您调整格式：

-   **编号规则代码** – 标识编号规则的代码。 此编号规则代码不存在，因为它将通过升级创建。
    -   常量名称：**NumberSequenceDefaultCode**
    -   默认值："FADBUpgr"
-   **前缀** - 将用作凭证号前缀的常量字符串。
    -   常量名称：**NumberSequenceDefaultParameterPrefix**
    -   默认值："FADBUpgr"
-   **字母数字的长度** – 编号规则的字母数字段的长度。
    -   常量名称：**NumberSequenceDefaultParameterAlpanumericLength**
    -   默认值：9
-   **开始编号** - 编号规则要使用的第一个数字。
    -   常量名称：**NumberSequenceDefaultParameterStartNumber**
    -   默认值：1

选项 2：**现有的用户定义的编号规则** -此选项允许您定义升级时要使用的编号规则。 如果需要高级编号规则配置，则考虑使用此选项。 要使用编号规则，必须使用以下信息修改升级类 ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans：

-   **编号规则代码** – 编号规则的代码。
    -   常量名称：**NumberSequenceExistingCode**
    -   默认值：无默认值，必须更新到编号规则代码。
-   **共享编号规则** – 标识编号规则的作用域的布尔值。 对所有公司的共享编号规则使用“true”，对特定公司的作用域使用“false”。 使用“false”时，含有折旧帐簿交易记录的每一个公司都必须存在具有指定名称的编号规则。 含有折旧帐簿交易记录的每一个分区都存在共享编号规则。
    -   常量名称：**NumberSequenceExistingIsShared**
    -   默认值：true

参数位于 ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans 类的开头。 

*// 指定凭证分配的首选方法* 
 *// true，如果您要使用现有的编号规则代码* 
 *// false，如果您要使用系统定义的编号规则（默认）* const boolean NumberSequenceUseExistingCode = false;  

*// 如果使用系统定义的编号规则方法，则指定编号规则的参数。*
 *// 将使用这些参数创建新的编号规则。* const str NumberSequenceDefaultCode = 'FADBUpgr'; const str NumberSequenceDefaultParameterPrefix = 'FADBUpgr'; const int NumberSequenceDefaultParameterAlpanumericLength = 9; const int NumberSequenceDefaultParameterStartNumber = 1;   

*// 如果使用现有编号规则方法，则指定现有的编号规则代码。* 
 *// 将对现有的编号规则逐行进行凭证分配。* const str NumberSequenceExistingCode = ''; *// 指定现有编号规则代码的作用域* 
 *// true，如果指定的编号规则为共享* 
 *// false，如果指定的编号规则为针对特定公司* 
 *// 如果未找到具有指定作用域的编号规则代码，将使用默认的系统定义的编号规则。* const boolean NumberSequenceExistingIsShared = true; 

修改常量后重新构建含有类的项目。 

使用系统定义的编号规则方法（选项 1）时，升级将使用基于设置的处理以分配升级脚本参数中指定的凭证号。 它还将在分配后使用指定参数创建新的编号规则。 

使用用户定义的现有编号规则方法（选项 2）时，数据升级检查具有折旧帐簿交易记录的每个分区和公司的数据库中是否存在具有指定作用域的编号规则。 如果存在，升级将通过逐行处理分配编号规则通过编号规则框架指定的凭证号。 如果不存在具有指定作用域的编号规则，升级将使用默认的系统定义的编号规则方法分配凭证号，并将在分配后使用指定的默认参数创建新的编号规则。

无论使用任何一种方法，数据升级脚本都会使用为以前的折旧帐簿日记帐名称创建的新总帐日记帐名称上的 **凭证系列** 字段的编号规则。



