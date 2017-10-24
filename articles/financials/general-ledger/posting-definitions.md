---
title: "过帐定义"
description: "本文提供有关过帐定义以及如何定义和关联它们的信息。 对于支持的过帐类型和文档，则可以使用过帐定义而不是过帐模板来分类会计条目中的主科目和财务维度。"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JournalizingDefinition, JournalizingDefinitionTrans, LedgerParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 15741
ms.assetid: 1495e7e0-2e39-464c-8da9-f55b1ca1c6bb
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 9c49e4abe28078f62f46b4eea4e22a268339b569
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="posting-definitions"></a>过帐定义

[!include[banner](../includes/banner.md)]


本文提供有关过帐定义以及如何定义和关联它们的信息。 对于支持的过帐类型和文档，则可以使用过帐定义而不是过帐模板来分类会计条目中的主科目和财务维度。

对于支持的过帐类型和文档，则可以使用过帐定义而不是过帐模板来分类会计条目中的主科目和财务维度。 您可以在**交易记录过帐定义**页上查看支持的文档和过帐类型。 

若要开始使用过帐定义，则在**总帐参数**页选择**使用过帐定义**选项。 即使在您使用过帐定义时，您仍必须为源条目和不支持的过帐类型和文档定义过帐模板。 

您必须使用过帐定义以便支持采购订单的预留款核算和采购申请的预留款核算。

## <a name="defining-posting-definitions"></a>定义过帐定义
使用**过帐定义**页可以指定匹配条件并定义应在匹配发生时生成的条目。 匹配条件针对源条目评估为会计分配。 

在**过帐定义**页中，您还可以分配优先级编号到条目行以控制评估行的订单。 具有最低优先级编号的行首先进行评估。 例如，具有优先级 1 的所有行进行评估，然后是具有优先级 2 的行，依此类推。 当找到匹配时，忽略其他匹配条件。 此外，只有与源交易记录匹配的组中的条件创建生成的条目。 

通过使用**测试过帐定义**向导您可以验证您的过帐定义。 在您为过帐后定义定义一个示例源条目后，您将看到生成的条目。 

您可以与生效日期一起使用过帐定义版本。 例如，您可以创建过帐定义的将来版本过帐到一个新的会计年度的不同会计科目。 

使用**交易记录过帐定义**页可以分配过帐定义到交易记录类型。

## <a name="linking-posting-definitions"></a>链接过帐定义
在您创建过帐定义时，您可以从一个过帐定义链接到另一个。 除了当前过帐定义的标准外，然后还考虑您链接到的定义的条件。 此功能帮助您节省时间，因为如果您已输入另一个定义的那些行，您则不必在**过帐定义**页的**条目**快速选项卡重新输入条件。 

在图或表中，包括您可以使用的所有链接。 为避免与当前过帐定义的冲突，请确保您链接的所有过帐定义的行是唯一的。 

当您在过帐定义创建链接时，适用以下限制:

-   指定过帐定义可以链接到另一个过帐定义或从另一个过帐定义链接，但不能同时链接这两者。 但是，过帐定义能与多个过帐定义链接。
-   您可以设置只在同一个模块中的过帐定义之间的链接。
-   您可以分配过帐定义到任何交易记录类型，但是，交易记录类型必须作为过帐定义在同一模块。 使用**交易记录过帐定义**页可以查看交易记录类型在哪个模块。


有关详细信息，请参阅[过帐定义示例](example-posting-definitions.md)。 



