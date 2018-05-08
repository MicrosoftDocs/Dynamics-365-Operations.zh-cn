---
title: "配置行项工作流"
description: "本主题说明如何配置行项工作流元素。"
author: sericks007
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195833
ms.assetid: 3237347e-71d5-4569-bc9a-0d0fc9410b78
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: d30d6aeda6be7bc81763c0b3f20c568d3fc81526
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="configure-a-line-item-workflow"></a>配置行项工作流

[!include [banner](../includes/banner.md)]

本主题说明如何配置行项工作流元素。

要配置行项工作流元素，在工作流编辑器中，右键单击该元素，然后单击“**属性**”以打开“**属性**”页。 然后使用以下过程配置行项工作流元素的属性。

## <a name="name-the-line-item-workflow-element"></a>对行项工作流元素命名。
按照以下步骤为行项工作流元素输入一个名称。

1.  在左侧窗格中，单击**基本设置**。
2.  在“**名称**”字段中，为行项工作流元素输入唯一名称。

## <a name="specify-whether-the-same-workflow-is-used-to-process-all-line-items"></a>指定是否使用相同工作流处理所有行项
按照以下步骤指定是否使用相同的工作流处理在文档中的所有行项。

1.  在左侧窗格中，单击**基本设置**。
2.  如果相同的工作流处理单据上的所有行项，则单击“**为所有行项调用一个单一工作流**”。 然后，选择用于处理行项的工作流。
3.  如果特定工作流应处理满足一组特定条件的行项，则单击“**为每个行项调用一个工作流**”。 然后按照以下步骤定义一组条件：
    1.  单击“**添加**”。
    2.  选择表中的条件。
    3.  在“**条件名称**”选项卡上，输入您定义的一组条件的名称。
    4.  单击“**添加条件**”输入条件。
    5.  输入需要的任何其他条件。
    6.  要验证输入的该组条件是否配置正确，请单击“**测试**”。 在“**测试工作流条件**”页面，在“**验证条件**”区域，选择一条记录，然后单击“**测试**”。 系统对该记录进行评估，判断其是否符合您定义的条件。 单击**确定**或**取消**返回到**属性**页面。

    在“**工作流**”选项卡，选择处理满足您定义的一组条件的行项时要使用的工作流。





