---
title: 文档状态和生命周期
description: 此主题介绍 Microsoft Dynamics 365 Commerce 中的页面元素的各种文档状态。
author: phinneyridge
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 7c30932800beda13ac8fe6b0386fe29efe93f79c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982608"
---
# <a name="document-states-and-lifecycle"></a>文档状态和生命周期

[!include [banner](includes/banner.md)]

此主题介绍 Microsoft Dynamics 365 Commerce 中的页面元素的各种文档状态。

## <a name="document-state-descriptions"></a>文档状态描述

[页面元素](page-elements-overview.md)主题列出了内容管理系统 (CMS) 中的各种文档类型。 在创作工具中，这些文档类型可以具有多种状态。 文档状态可帮助避免数据冲突和实施版本控制。 它们决定谁可以更改文档，何时可以更改文档，以及其他人何时可查看更改。

下表显示 Commerce 中的页面元素可以的文档状态。

| 单据状态      | 站点构建器操作        | 说明                                                  |
| ------------------- | -------------------------- | ------------------------------------------------------------ |
| 已结账         | 选择 **编辑**。           | 将把适用的文档签出给您。 当文档处于此状态时，其他经过身份验证的系统用户不能更改此文档，而您对此文档进行的任何更改都仅对您可见。 |
| 已保存               | 选择 **保存**。           | 将把已对签出文档进行的更改保存到数据库，但是尚未签入或发布该文档。 作者选择 **完成编辑** 之前，保存的更改不对其他已身份验证的系统用户显示。 发布项之前，不对外部用户显示。 |
| 放弃签出 | 选择 **放弃编辑**。  | 将放弃对签出文档进行的所有更改，而项目将恢复为签出前的最后一个版本。 |
| 已签入          | 选择 **完成编辑**。 | 将签入编辑的文档。 所有更改对其他已身份验证系统用户可见，并且这些用户可编辑此文档。 每次签入在项的历史记录中创建一个文档版本记录。 |
| 已发布           | 选择 **发布**。        | 将发布文档，并且更改将发布给您的实时站点，并可被外部用户发现。 项只有在先通过选择 **完成编辑** 签入后才能发布。 |

## <a name="additional-resources"></a>其他资源

[添加内容的方法](add-manage-content.md)

[页面模型词汇表](page-elements-overview.md)

[使用发布组](publish-groups.md)

[启用和使用跨渠道共享](cross-channel-sharing.md)

[使用模块](work-with-modules.md)

[使用片段](work-with-fragments.md)

[模板和布局概览](templates-layouts-overview.md)

[自定义站点导航](customize-site-navigation.md)
