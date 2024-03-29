---
title: 定义资源功能
description: 资源功能描述了运营资源可执行的内容。
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WrkCtrCapability
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 42451da0bd465ce3a18ecf18570f3331847474c1
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579104"
---
# <a name="define-resource-capabilities"></a>定义资源功能

[!include [banner](../../includes/banner.md)]

资源功能描述了运营资源可执行的内容。 在安排期间，每个工作和操作的要求都将与可用资源的功能相匹配。 该任务指南将帮助您创建资源功能并其分配给资源。 创建此任务的演示数据公司是 USMF。


## <a name="create-a-resource-capability"></a>创建资源功能
1. 转到“资源功能”。
2. 单击“新建”。
3. 在“功能”字段中，键入资源功能的 ID。
    * 对于特定工序，请使用功能 ID 指定必须具有此功能才能执行操作的资源。  
4. 在“描述”字段中，输入功能的描述。

## <a name="assign-capability-to-a-resource"></a>将功能分配给资源
1. 单击“添加”。
2. 在“资源”字段中，键入资源功能的 ID。
    * 资源功能可分配给一个或多个资源。  
3. 在“截止日期”字段，输入日期。
    * 您可以使用该字段指定某个资源只在限定时间内具有此功能。  
4. 在“优先”字段，输入一个数字。
    * 在安排工作和操作时，可以指定是否按优先级选择资源。 如果您按优先级选择资源，并且在请求日期之前有多个可执行该工作或操作的资源，则根据所要求的功能选择最低优先级的资源。  
5. 在“水平”字段，输入一个数值。
    * 当您指定某项工作或操作需要某种特定功能，您还可以指定所需功能的最低水平。 使用功能级别区分资源可以根据不同的速度、力量、大小等执行同类工作。  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]