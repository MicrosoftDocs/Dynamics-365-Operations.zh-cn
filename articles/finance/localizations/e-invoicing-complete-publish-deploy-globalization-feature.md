---
title: 完成、发布和部署全球化功能
description: 本文提供有关全球化功能生命周期的信息。
author: gionoder
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 9d4a408f2169b220fefd9ab7e9f3b37217fb3cfe
ms.sourcegitcommit: 1ecfc1d8afb2201ab895ae6f93304ba2b120f14b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/21/2022
ms.locfileid: "9710827"
---
# <a name="complete-publish-and-deploy-a-globalization-feature"></a>完成、发布和部署全球化功能

[!include [banner](../includes/banner.md)]

## <a name="electronic-invoicing-feature-versions"></a>电子开票功能版本

电子开票功能已版本化。 新版本创建时，版本号会自动递增。

电子开票功能版本采用的生命周期最多包含以下三种状态：

- **草稿** – 当功能版本处于此状态时，您可以编辑其配置属性及其项目（例如，文件格式配置）。
- **完成** – 此状态指示您已完成功能版本的编辑，不打算再对其进行任何更新。 当功能版本处于此状态时，您无法再编辑它或它的任何组件。
- **已发布** – 此状态指示功能版本已发布到与您的组织关联的全局存储库中。 当功能版本处于此状态时，您无法再编辑它或它的任何组件。

您可以为新版本的电子开票功能指定 **生效开始** 日期。 通过这种方式，您可以定义一个可以使用的默认版本，或者在将功能部署到服务环境时可以覆盖该默认版本。

要更改电子开票功能版本的状态，请执行以下步骤。

1. 登录到您的 Regulatory Configuration Service (RCS) 帐户。
2. 在 **全球化功能** 工作区的 **功能** 部分中，选择 **电子开票** 磁贴。
3. 在 **电子开票功能** 页面的左侧，选择电子开票功能。
4. 在页面右侧的 **版本** 选项卡上，选择版本。
5. 选择 **更改状态**，然后选择 **完成**（如果当前状态为 **草稿**）或 **已发布**（如果当前状态为 **完成**）。
6. 在消息框中，选择 **是** 确认请求。

从 **完成** 状态到 **已发布** 状态的手动更改是可选的。 电子发票功能版本在被部署到服务环境时会自动更新为 **已发布** 状态。

您可以在 **版本** 选项卡上的 **功能版本状态** 列中跟踪状态。

## <a name="deploy-feature-versions"></a>部署功能版本

在 RCS 中，您使用 **部署** 命令将电子开票功能版本发布到目标服务环境或连接的应用程序。

1. 在 **电子开票功能** 页面的左侧，选择电子开票功能。
2. 在页面右侧的 **版本** 选项卡上，选择您要部署到服务环境或连接的应用程序的电子开票功能版本。 所选版本的状态必须为 **完成** 或 **已发布**。
3. 选择 **部署**，然后选择以下一个或全部两个选项定义部署目标：

    - **相连应用程序** – 此项为可选，但如果您希望将应用程序设置提供的配置写入之前与其关联的 Microsoft Dynamics 365 Finance 或 Dynamics 365 Supply Chain Management 的实例中，则必须使用此项。 跳过此类型部署将需要手动配置在 Finance 或 Supply Chain Management 的应用程序设置中定义的参数。
    - **服务环境** – 将电子开票功能版本部署到服务环境。 然后，电子开票就可以接收和处理 Finance 或 Supply Chain Management 发送的电子单据。

> [!NOTE]
> 通常，您将更改必须部署到服务环境的电子报告 (ER) 功能的参数。 对连接的应用程序的更改会很少。 只有在更改应用程序的相应参数时，才应将新版本部署到连接的应用程序。

要确定是否将特定版本的电子开票功能部署到特定环境，请查看 **环境** 选项卡上的信息。

## <a name="remove-feature-versions"></a>删除功能版本

在 RCS 中，您可以选择 **取消** 从服务环境中删除特定的电子开票功能版本（如果该版本已在那里部署）。

> [!IMPORTANT]
> **取消** 按钮仅对服务环境起作用。 不会从当前电子开票功能的连接的应用程序中删除任何内容。

## <a name="rebase-electronic-invoicing-features"></a>重定电子开票功能的基本版本

当一个电子开票功能是从另一个电子开票功能派生而来时，您可以选择 **重定基本版本** 使用在原始（父）功能中所做的更改来更新派生功能。

要重定您所创建功能的派生版本的基本版本，请按照下列步骤操作。

1. 通过从全局存储库导入功能来获取最新版本的功能。 有关详细信息，请参阅[从全局存储库导入功能](e-invoicing-import-feature-global-repository.md)。
2. 在功能列表中，选择要重定基本版本的功能。
3. 在 **版本** 选项卡上，选择 **新建** 创建草稿版本。
4. 选择 **重定基本版本**。
5. 在 **重定基本版本** 对话框中，选择要重定的功能版本。
6. 选择 **确定**。
7. 查看功能组件，并进行所需的更改。
8. 选择 **更改状态** 完成已重定基本版本的功能。 重定基本版本完成后，您可以执行其他操作。

## <a name="get-a-specific-version-of-electronic-invoicing-features"></a>获取特定版本的电子开票功能

当您创建电子开票功能的新版本时，系统会创建最新功能版本的副本。 要使用功能的早期版本作为新版本的基本版本，选择该版本，然后选择 **获取此版本命令**。 将创建一个新的功能草稿版本，它是所选版本的副本。
