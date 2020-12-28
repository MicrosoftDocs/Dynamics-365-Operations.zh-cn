---
title: 承运人组
description: 本主题介绍如何设置承运人组的数据。
author: Henrikan
manager: ''
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSCarrierGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 2570479edac9bc8cc7aa998a8b69f54ffc10cd61
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646366"
---
# <a name="carrier-groups"></a>承运人组

承运人组是装运承运人和承运人服务的集合。 每个承运人组都为包含的装运承运人和承运人服务指定了优先顺序。

当同一路线细分存在多个装运承运人和承运人服务时，您可以在路线计划或路线指南中指定承运人组，而不是特定的装运承运人和承运人服务。

## <a name="create-a-carrier-group"></a>创建承运人组

1. 转到 **运输管理 &gt; 设置 &gt; 承运人 &gt; 承运人组**。
1. 选择 **新建**。
1. 在 **承运人组** 字段中，输入组的唯一标识符 (ID)。
1. 在 **名称** 字段中，输入组的描述性名称。
1. 在 **详细信息** 快速选项卡上，添加一行，并为其选择装运承运人和承运人服务。 重复此步骤，直到您为组添加了所需数量的承运人。
1. 关闭该页面。
