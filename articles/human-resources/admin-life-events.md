---
title: 设置生命事件管理员权限
description: 本文介绍如何在 Microsoft Dynamics 365 Human Resources 中配置生命事件管理员权限。
author: twheeloc
ms.date: 08/01/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9deed240977394667cee8b107397267b182d960b
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/06/2022
ms.locfileid: "9229886"
---
# <a name="set-administrator-rights-for-life-events"></a>设置生命事件管理员权限

[!include [banner](../includes/preview-banner.md)]

管理员可以根据配置设置更新生命事件选项。 在 **人力资源参数** 页面上，您可以配置允许管理员对计划选择进行更改的参数。 您还可以完全限制管理员进行更改。

在 **人力资源参数** 页面上，您可以为已确认的计划和生命事件选项设置计划更改限制。

如果选择了 **已确认计划** 选项，则只能在登记期间处于活动状态时进行更改。 （登记期间的示例包括未结登记期间、新的雇用登记期间和生命事件登记期间。）如果未选择此选项，则可随时进行更改。

如果选择了 **生命事件选项** 选项，则生命事件期间的计划更改受计划类型上定义的生命事件选项的限制。 如果未选择此选项，则可以在生命事件期间更改计划选择。

## <a name="set-plan-change-restrictions"></a>设置计划更改限制

在 **人力资源参数** 页面上的 **福利管理** 选项卡上，以下字段可用。

| 字段 | Description |
|-------|-------------|
| 已确认计划 | 如果仅在登记期间处于活动状态时才能更改计划，则选择此选项。 如果未选择此选项，则可随时进行更改。 |
| 生命事件选项 | 如果生命事件期间的计划更改受计划类型上定义的生命事件选项的限制，则选择此选项。 如果未选择此选项，则可以在生命事件期间更改计划选择。 |
