---
title: "对未结工作列表的系统分组"
description: "此主题描述如何在移动设备上筛选未结工作列表。"
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: d9ca6b0d4a9909d419d6241a044336d7a02aea02
ms.contentlocale: zh-cn
ms.lasthandoff: 04/13/2018

---

# <a name="system-grouping-on-an-open-work-list"></a>对未结工作列表的系统分组

[!include [banner](../includes/banner.md)]

通过使用系统分组字段可以筛选未结工作列表，而不必编辑移动设备菜单项。
适用时，系统分组可用于在单个工作标题字段上筛选工作列表。 无法使用系统分组筛选行级别字段。

## <a name="set-up-system-grouping-on-an-open-work-list"></a>对未结工作列表设置系统分组
使用这些步骤对未结工作列表设置系统分组。

-   从移动设备菜单项选择**模式：间接**和**活动代码：显示未结工作列表**。 以下选项可用。 对未结工作列表设置系统分组需要这些选项。 

|        选项         |                                                                                                                                                                                                                                                                         说明                                                                                                                                                                                                                                                                         |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 允许系统分组 |                                                                                                                                                                                                                                                 启用对所选工作列表进行系统分组菜单项。                                                                                                                                                                                                                                                  |
| 系统分组字段 | 仅当<strong>允许系统工作</strong>设置为<strong>是</strong>时可用。 选择决定如何为工作人员对领料工作进行分组的字段。 例如，如果您选择“ShipmentId”<strong></strong>字段，工作人员将扫描装运 ID 来对领料工作进行分组。 然后将装运的所有工作分配给工作人员。 此字段要求您创建一个菜单项从而使用系统分组现有工作。 使用<strong>系统分组标签</strong>字段通知工作人员要扫描的内容。 |
| 系统分组标签 |                       仅当<strong>允许系统工作</strong>设置为<strong>是</strong>时可用。 输入信息通知工作人员对领料工作分组时要扫描的内容。 例如，如果您使用 <strong>ShipmentId</strong> 字段按照装运分组领料工作，您可以在字段中输入装运 ID。 此字段要求您创建一个菜单项从而使用系统分组现有工作。 您还必须在<strong>系统分组</strong>字段中选择要按其分组的字段。                       |


