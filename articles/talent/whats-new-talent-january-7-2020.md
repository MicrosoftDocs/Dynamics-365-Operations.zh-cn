---
title: Dynamics 365 Talent（2020 年 1 月 7 日）中的新增功能或更改的功能
description: 本文介绍 Microsoft Dynamics 365 Talent 中的新增功能或更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-01-07
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e227c614fdbfe6f3dd410f1a533c593979abf1ec
ms.sourcegitcommit: 615ed3e4260192ba36826e128f1afa1588e94845
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/21/2020
ms.locfileid: "2974422"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-7-2020"></a>Dynamics 365 Talent（2020 年 1 月 7 日）中的新增功能或更改的功能

本文介绍 Dynamics 365 Talent 中的新增功能或更改的功能。

## <a name="changes-in-attract"></a>Attract 中的更改

本版本中包含 Dynamics 365 Talent: Attract 的小缺陷修复。

## <a name="changes-in-onboard"></a>Onboard 中的更改

本版本中包含 Dynamics 365 Talent: Onboard 的小缺陷修复。

## <a name="changes-in-core-hr"></a>Core HR 中的更改

本部分中的更改适用于内部版本号 8.1.2697。 某些标题中括号内的数字是 Microsoft Dynamics Lifecycle Services (LCS) 中的支持号码。

 
### <a name="cant-delete-workers-that-dont-have-employment-records---386157"></a>无法删除没有就业记录的工作人员 - (386157)

此更改会在**失业工作人员**窗体中添加删除选项。 当工作人员没有未来、当前或过去的工作时，此窗体中将出现工作人员。 在此版本中，仅对系统管理员启用了删除功能。 但是，在下周的版本中，安全性将得到更新，以允许具有 HR 助手角色的所有用户删除没有工作的工作人员。 您还可以按照以下步骤手动进行这些更改。

1. 转到**安全配置**。
2. 在**特权**选项卡中，筛选**特权**列表以**维护工作人员**。
3. 在**参考**列中，选择**显示菜单项**。
4. 在**显示菜单项**中，选择 **HcmWOrkersWithoutEmployment**。
5. 将**删除**权限设置为“授予”。
6. 选择**已取消发布的对象**选项卡。
7. 选择**全部发布**。
