---
title: 业务文档管理中的新文档用户界面
description: 本主题提供有关如何在电子报告 (ER) 框架的业务文档管理功能中使用新文档用户界面 (UI) 的信息。
author: v-anamir
manager: AnnBe
ms.date: 05/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-anamir
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2cb6e0da4af07b9b8486bf1e5bda29523cbd08e9
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681344"
---
# <a name="new-document-user-interface-in-business-document-management"></a>业务文档管理中的新文档用户界面

[!include [banner](../includes/banner.md)]

业务文档管理使业务用户可以使用 Microsoft 365 服务或相应的 Microsoft Office 桌面应用程序来编辑业务文档模板。 编辑可能包括设计更改或新部署，或者用户可能会添加占位符以包含其他数据，而不必更改源代码。 有关如何使用业务文档管理的更多信息，请参见[业务文档管理概述](er-business-document-management.md)。

新的文档用户界面 (UI) 更清晰，使用起来更舒适。 **业务文档** 区域仅显示当前提供商可用的模板。

利用 **新建文件** 按钮，用户能够以其他提供商提供的电子报告 (ER) 格式配置创建和编辑模板。 在本主题的示例中，提供者是 Microsoft。

## <a name="make-the-new-document-ui-in-business-document-management-available"></a>使业务文档管理中的新文档 UI 可用

要开始使用业务文档管理中的新文档 UI，必须打开 **功能管理** 工作区中的 **类似于 Office 的业务文档管理 UI 体验** 功能。

请按照以下步骤为所有法人启用此功能。

1. 在 **功能管理** 工作区中的 **新建** 选项卡上，选择列表中的 **类似于 Office 的业务文档管理 UI 体验** 功能。
2. 选择 **立即启用** 以打开所选功能。
3. 刷新页面以访问新功能。

### <a name="edit-templates-that-are-owned-by-other-providers"></a>编辑其他提供商拥有的模板

1. 在 **业务文档管理** 工作区中，选择 **新建文档**。

    ![业务文档管理工作区](./media/BDM_overview_new_template1.png)

2. 在此对话框中，选择要用作模板的文档，然后选择 **创建文档**。

    ![业务文档对话框](./media/BDM_overview_new_template2.png)

3. 在此新对话框内的 **标题** 字段中，根据需要更改标题。 标题文本用于命名自动创建的新 ER 格式配置。 此配置 (**Customer FTI report (GER) Copy**) 的草稿版本将包含编辑的模板，并且将用于为当前用户运行此 ER 格式。 将使用来自基本 ER 格式配置的原始模板为每个其他用户运行此 ER 格式。
4. 在 **名称** 字段中，更改将自动创建的可编辑模板第一个修订的名称。
5. 在 **注释** 字段中，更新有关将自动创建的可编辑模板的修订注解。
6. 选择 **确定** 以确认开始执行编辑流程。

    ![文档创建对话框](./media/BDM_overview_new_template3.png)

**新建文件** 按钮用于以其他提供商提供的 ER 格式配置创建和编辑模板。 在本示例中，提供商是 Microsoft。 当您选择 **新建文档** 时，您可以查看当前提供商和其他提供商拥有的所有模板。 选择模板后，将打开它进行编辑。 然后将把编辑后的模板存储在自动生成的新 ER 格式配置中。

有关更多信息，请参见[业务文档管理概述](er-business-document-management.md)。
