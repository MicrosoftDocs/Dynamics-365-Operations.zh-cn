---
title: 安装 Adventure Works 主题
description: 本主题介绍如何在 Microsoft Dynamics 365 Commerce 中安装 Adventure Works 主题。
author: anupamar-ms
ms.date: 07/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 9c94dd8ead32f58a25a396376840101d9c2c9b08
ms.sourcegitcommit: 0c77dbb8547cd36fce3977ca9515fa1474efa77a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/22/2021
ms.locfileid: "6655840"
---
# <a name="install-the-adventure-works-theme"></a>安装 Adventure Works 主题

[!include [banner](includes/banner.md)]

本主题介绍如何在 Microsoft Dynamics 365 Commerce 中安装 Adventure Works 主题。 

> [!IMPORTANT]
> Adventure Works 主题和模块从 Dynamics 365 Commerce 版本 10.0.20 发行版本开始提供。 它们通过 Microsoft AppSource 提供。

## <a name="prerequisites"></a>先决条件

在安装 Adventure Works 主题之前，您必须有一个 Dynamics 365 Commerce（Commerce 版本 10.0.20 或更高版本），其中包括 Retail Cloud Scale Unit (RCSU)、Commerce 联机软件开发套件 (SDK) 和 Commerce 模块库。 有关如何安装 Commerce SDK 和模块库的信息，请参阅 [SDK 和模块库更新](e-commerce-extensibility/sdk-updates.md)。 

## <a name="installation-steps"></a>安装步骤

### <a name="install-the-adventure-works-theme-in-your-application"></a>在应用程序中安装 Adventure Works 主题

Adventure Works 主题包在 **dynamics365-commerce** 源中提供，如 **@msdyn365-commerce-theme/adventureworks-theme-kit**。 但是，虽然 Adventure Works 主题包是该源的一部分，但它位于不同的命名空间。 因此，您必须按照以下步骤为命名空间添加注册表项。

1. 更新 **.npmrc** 文件，使其包含以下注册表项（如果尚未包含该项）：

    `@msdyn365-commerce-theme:registry=https://pkgs.dev.azure.com/commerce-partner/Registry/_packaging/dynamics365-commerce/npm/registry/`

1. 更新 **.yarnrc** 文件，使其包含以下注册表项（如果尚未包含该项）：

    `"@msdyn365-commerce-theme:registry" "https://pkgs.dev.azure.com/commerce-partner/Registry/_packaging/dynamics365-commerce/npm/registry/"`  
    
要在本地环境中安装包，请从命令提示符运行以下命令。 此命令会自动更新 package.json 文件，使其包含依赖项。

`yarn add @msdyn365-commerce-theme/adventureworks-theme-kit`

在 **package.json** 文件中，您应将主题版本更新为特定版本。

> [!IMPORTANT]
> - 主题版本应与模块库版本匹配，以确保所有功能都按预期工作。 
> - Commerce 模块库和 SDK 的最低版本应为 10.0.20 (9.31)。 

### <a name="add-the-font-files-for-the-adventure-works-theme"></a>为 Adventure Works 主题添加字体文件

在应用中安装 Adventure Works 主题后，必须添加其所需的字体文件。 要完成此步骤，将 **\node_modules@msdyn365-commerce-theme\adventureworks-theme-kit\src\modules\adventureworks\public\webfonts** 中的所有字体文件复制到合作伙伴应用程序公共目录路径 **\public\webfonts**。

### <a name="set-up-the-resources-for-the-adventure-works-theme"></a>为 Adventure Works 主题设置资源

下一步是更新主题所需的默认资源。 要完成此步骤，将 **\node_modules@msdyn365-commerce-theme\adventureworks-theme-kit\src\modules\adventureworks\resources\modules** 下 global.json 文件中的内容复制到 **\src\resources\modules** 下的合作伙伴应用程序 global.json 文件。 如果 **\src\resources** 目标目录不存在，可以从 **\node_modules@msdyn365-commerce-theme\adventureworks-theme-kit\src\modules\adventureworks** 源目录将它整体复制到 **\src** 目标目录。

### <a name="pull-updates-and-validate-the-theme"></a>拉取更新与验证主题

有关如何拉取最新 SDK、模块库和其他依赖项更新的信息，请参阅 [SDK 和模块库更新](e-commerce-extensibility/sdk-updates.md#pull-updates)的“拉取更新”一节。

拉取最新的依赖后，您可以运行 **yarn start** 命令在您的开发环境中启动 Node 服务器并测试新的 Adventure Works 主题。 使用查询字符串参数 `?theme=adventureworks` 本地浏览应用程序（例如，`https://localhost:4000/?theme=adventureworks`）。

## <a name="additional-resources"></a>其他资源

[Adventure Works 主题](adventure-works-theme.md)

[模块库概览](starter-kit-overview.md)

[SDK 和模块库更新](e-commerce-extensibility/sdk-updates.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]