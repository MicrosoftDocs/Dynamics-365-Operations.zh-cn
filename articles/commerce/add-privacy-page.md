---
title: 添加隐私策略页面
description: 本文介绍如何在 Microsoft Dynamics 365 Commerce 中添加隐私政策页面。
author: v-chgri
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: a874272fe5158dd213a69c7ba996e0d28c7ed15a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272063"
---
# <a name="add-a-privacy-policy-page"></a>添加隐私策略页面

[!include [banner](includes/banner.md)]

本文介绍如何在 Microsoft Dynamics 365 Commerce 中添加隐私政策页面。

隐私合规性包括通知站点用户如何收集和处理他们的数据的组织措施。 然后，用户可以决定他们要如何处理个人数据，并可以采取适当的行动。

## <a name="review-the-microsoft-privacy-statement-in-dynamics-365-commerce"></a>在 Dynamics 365 Commerce 中查看 Microsoft 隐私声明

要在登录 Dynamics 365 Commerce 创作工具时查看 Microsoft 隐私声明，请选择右上角的 **帮助** 按钮 (**?**)，然后选择 **隐私和 Cookie**。 将打开一个新选项卡，其中包含指向 [Microsoft 隐私声明](https://privacy.microsoft.com/privacystatement) 的链接。

## <a name="build-a-privacy-policy-page-for-your-site"></a>为您的站点建立隐私政策页面

在 Dynamics 365 Commerce 中，有几种方法可以使您的站点用户访问您的隐私权政策。 本节说明如何建立隐私政策页面，然后使用页脚片段来引用该页面。

后面的指南是一个示例，显示如何为 Commerce 站点建立通用隐私政策页面。 您负责设计和实施最能满足公司法律要求的隐私政策页面解决方案。

首先，在创作工具中，转到要为其建立隐私政策页面的站点。

### <a name="create-a-template"></a>创建模板

> [!NOTE]
> 如果已经创建了可用于隐私政策页面的模板，请直接跳至[建立隐私政策页面](#build-a-privacy-policy-page)一节。

若要创建模板，请执行以下步骤。

1. 转到 **模板**，然后选择 **新建** 创建页面模板。
1. 在 **新建模板** 对话框的 **模板名称** 下，输入 **促销横幅模板**，然后选择 **确定**。
1. 在模板中，将所有需要的模块添加到所需的页面插槽中。 要获取指导，将鼠标悬停在红色感叹号上。 （例如，**HTML 标头** 插槽可能需要 **默认外部脚本** 模块。）
1. 在 **正文** 插槽中，添加一个 **默认页面** 模块。
1. 在 **默认页** 模块的 **主** 插槽中，添加一个 **内容丰富块** 模块。
1. 在 **内容丰富块** 模块中，添加一个 **内容丰富块项** 模块。
1. 选择 **保存**，选择 **完成编辑** 签入模板，然后选择 **发布** 进行发布。

### <a name="build-a-privacy-policy-page"></a>建立隐私政策页面

要建立隐私政策页面，请按照下列步骤操作。

1. 转到 **页面**，然后选择 **新建** 创建页面。
1. 在 **选择模板** 对话框中，为隐私策略页面选择模板。
1. 输入页面名称和页面 URL，然后选择 **确定**。 
1. 在页面的 **主** 插槽中，添加一个 **内容丰富块** 模块。
1. 在 **内容丰富块** 模块中，添加一个 **内容丰富块项** 模块。
1. 在 **内容丰富块** 模块的属性窗格中，选择 **添加数据源**，然后选择 **富文本内容**。
1. 在富文本编辑器中，输入隐私政策页面的内容。 根据需要将富文本编辑器扩展到全屏模式。
1. 完成内容输入后，选择 **预览** 在 Web 浏览器中预览页面。
1. 完成页面和模块属性的所有其余添加。
1. 选择 **保存**，选择 **完成编辑** 签入页面，然后选择 **发布** 进行发布。

若要发布隐私政策页面的 URL，请执行以下步骤。

1. 转到 **URL**，选择隐私政策页面的 URL。
1. 选择 **发布** 发布所选的 URL。

### <a name="create-a-link-to-the-privacy-policy-page-in-a-footer"></a>在页脚中创建指向隐私政策页面的链接

您可以将隐私政策页面的链接添加到片段中。 这样，您可以共享链接并通过引用片段跨多个站点页面对其进行更新。 本示例说明如何将隐私政策页面的链接添加到页脚片段。

若要向页脚片段添加链接，请执行以下步骤。

1. 转到 **片段**，然后选择 **新建** 创建页面片段。
1. 在 **新建片段** 对话框中，选择 **页脚** 模块。
1. 在 **片段名称** 下，输入片段的名称，然后选择 **确定**。
1. 在 **页脚类别** 插槽中，添加一个 **页脚项** 模块。
1. 在右侧的属性窗格中，选择 **链接文本**。
1. 在 **链接文本** 对话框中，输入隐私政策页面的链接文本和链接目标，然后单击 **确定**。
1. 要获取隐私政策页面的 URL，请转到 **页面**，转到隐私政策页面，然后从属性窗格中复制 URL。
1. 选择 **保存**，选择 **完成编辑** 签入片段，然后选择 **发布** 进行发布。
1. 预览片段，并测试隐私政策页面的链接。

现在可以在模板中为其他站点页面引用此片段了。 当此片段在模板的 **页脚** 模块中引用时，链接引用将出现在使用该模板建立的任何页面上。

## <a name="additional-resources"></a>其他资源

[合规概述](compliance-overview.md)

[辅助功能和功能](accessibility.md)

[Cookie 合规性](cookie-compliance.md)

[替换与所跟踪内容更改相关联的用户 ID](replace-IDs-tracked-changes.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
