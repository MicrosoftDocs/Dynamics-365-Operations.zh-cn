---
title: 文档状态和生命周期
description: 此主题介绍 Microsoft Dynamics 365 Commerce 中的页面元素的各种文档状态。
author: phinneyridge
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: b4f1c462f734b2d58843308f0f877fe18a4d9af7
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002973"
---
# <a name="document-states-and-lifecycle"></a>文档状态和生命周期


[!include [banner](includes/banner.md)]

此主题介绍 Microsoft Dynamics 365 Commerce 中的页面元素的各种文档状态。

## <a name="document-state-descriptions"></a>文档状态描述

[页面元素](page-elements-overview.md)主题列出了内容管理系统 (CMS) 中的各种文档类型。 在创作工具中，这些文档类型可以具有多种状态。 文档状态可帮助避免数据冲突和实施版本控制。 它们决定谁可以更改文档，何时可以更改文档，以及其他人何时可查看更改。

下表显示 Commerce 中的页面元素可以的文档状态。

| 单据状态 | 说明 |
|---|---|
| 已签出 | CMS 项签出给您后，不能被其他已经过身份验证的系统用户编辑。 您对项进行的所有更改只能对您显示。 |
| 已签入 | CMS 项签入后，所有更改对其他已经过身份验证的系统用户显示，然后，这些用户可以签出和编辑该项。 每次签入在项的历史记录中创建一个文档版本记录。 |
| 已发布 | CMS 项发布后，将推送到您的活动站点，并且在 Internet 中可被未经身份验证的外部用户发现。 只能发布已签入的项。 |
| 已保存 | 可以将对已签出 CMS 项进行的更改保存到 CMS，之后才能签入或发布。 签入项之前，保存的这些更改不对其他已身份验证的系统用户显示。 发布项之前，不对外部用户显示。 |
| 放弃签出 | 如果放弃已签出的 CMS 项，将删除保存的所有更改，而项将还原为最近签入的版本。 |

## <a name="additional-resources"></a>其他资源

[添加内容的方法](add-manage-content.md)

[页面模型词汇表](page-elements-overview.md)

[使用发布组](publish-groups.md)

[使用模块](work-with-modules.md)

[使用片段](work-with-fragments.md)

[模板和布局概览](templates-layouts-overview.md)

[自定义站点导航](customize-site-navigation.md)
