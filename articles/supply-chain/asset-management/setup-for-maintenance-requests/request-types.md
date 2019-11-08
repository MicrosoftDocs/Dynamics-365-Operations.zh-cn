---
title: 维护请求类型
description: 本主题说明如何在资产管理中设置维护请求类型。
author: josaw1
manager: AnnBe
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 430e475b52638dd80512ffd79d42aac6f5f340e1
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571131"
---
# <a name="maintenance-request-types"></a>维护请求类型

[!include [banner](../../includes/banner.md)]

 

维护请求类型用于为维护请求分类。 例如，您可能有与预防性维护和修复性维护有关的维护请求。 也可能有用于管理资产维修（仓库维修）的特殊维护请求类型。

维护请求类型定义与维护请求生命周期状态组（维护生命周期模型）之间的隶属关系。 维护请求生命周期模型定义可为维护请求设置的生命周期状态。 （维护请求生命周期状态的示例包括**已创建**、**活动**和**已结束**。）

1. 选择**资产管理** \> **设置** \> **维护请求** \> **维护请求类型**。
2. 选择**新建**创建维护请求类型。
3. 在**维护请求类型**字段中，输入维护请求类型的 ID。
4. 在**名称**字段中输入名称。
5. 在**常规**快速选项卡上的**维护请求生命周期模型**字段中，选择一个维护请求生命周期模型。
6. 在**工作订单类型**字段中，选择一个工作订单类型。 维护请求转化为工作订单之后，该工作订单将自动获取与维护请求类型关联的工作订单类型。

下图显示**维护请求类型**页的示例。

![维护请求类型页面](media/07-setup-for-requests.png)
