---
title: 创建新电子开票功能
description: 本主题介绍了当没有现成的可配置功能可供您所在国家或地区使用时如何创建新的电子开票功能。
author: gionoder
ms.date: 07/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2021-07-21
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: ffef49c78fd0564db7a2329580ad33a9ccc633c8ac74557e625d1cfb29931576
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6744927"
---
# <a name="create-a-new-electronic-invoicing-feature"></a>创建新电子开票功能

[!include [banner](../includes/banner.md)]

本主题介绍了当没有现成的可配置功能可供您所在国家或地区使用时如何创建新的电子开票功能。

要创建新的电子开票功能，请完成以下任务：

1. 通过使用所提供的发票模型配置并利用要创建的功能的现有发票映射，创建新的文件格式配置。
2. 将文件格式配置添加到电子发票功能配置。
3. 创建电子开票功能设置。
4. 完成新的电子开票功能，并将其发布到组织的全局存储库。
5. 将新电子开票功能部署到服务环境。

## <a name="create-new-file-format-configurations-that-are-derived-from-the-existing-invoice-model"></a>创建源自现有发票模型的新文件格式配置

在此过程中，您将创建要创建的新电子开票功能所需的文件格式配置。 您可以创建电子发票文件格式配置以及新电子开票功能可能需要的任何其他文件格式配置。

在开始此过程之前，请登录到您的 Regulatory Configuration Service (RCS) 帐户。

1. 在 Microsoft Dynamics 365 Finance 内的 **电子申报** 工作区中，为 **Microsoft** 配置提供程序选择 **存储库**。
2. 选择 **全局**，选择 **打开**，然后在左侧窗格中选择 **发票模型** 配置。

    > [!IMPORTANT]
    > 对于巴西，请改为选择 **会计单据** 模型配置。

3. 在 **配置** 选项卡上，选择 **导入**。
4. 关闭该页面。
5. 关闭该页面。
6. 选择 **申报配置** 磁贴，然后选择您导入的发票模型。
7. 选择 **创建配置**，然后选择 **基于发票上下文模型的格式**。
8. 为格式配置输入名称和描述。
9. 在 **格式类型** 字段中，选择文件扩展名类型。
10. 选择 **创建配置**，然后选择您创建的格式配置。
11. 选择 **设计器**，并使用格式设计器工具配置文件布局，使其符合文件格式规格。
12. 关闭该页面。
13. 在 **版本** 快速选项卡上，选择 **更改状态** \> **完成**。
14. 选择 **更改状态**\>**共享** 以将格式配置发布到全局存储库。

必须先与 Microsoft 域共享新文件格式配置，然后电子开票服务才能使用该配置。

1. 选择您正在处理的格式配置。 必须 **共享** 配置的状态。
2. 在 **版本** 选项卡上，选择 **高级共享**\>**全局存储库**。
3. 在 **共享对象** 选项卡上，选择 **组织**。
4. 在 **参数** 字段中，输入 **Microsoft.com** 以与 Microsoft 域共享格式配置。
5. 选择 **确定**。

## <a name="create-the-new-electronic-invoicing-feature"></a>创建新电子开票功能

1. 在 RCS 内的 **全球化功能** 工作区的 **功能** 部分中，选择 **电子开票** 磁贴。
2. 选择 **添加**，然后选择 **新功能**。
3. 输入电子发票功能的名称和描述。
4. 选择 **创建功能**。

## <a name="add-electronic-invoicing-feature-configurations"></a>添加电子开票功能配置

1. 选择您要使用的电子开票功能。
2. 在 **配置** 选项卡上，选择 **添加**。
3. 在 **配置** 网格中，浏览并选择电子开票功能生成电子发票文件所需的文件格式配置。
4. 选择 **确定**。

## <a name="add-electronic-invoicing-feature-setups"></a>添加电子开票功能设置

1. 在 **设置** 选项卡上，选择 **添加**，然后选择 **自定义设置**。
2. 为功能设置输入名称和描述。
3. 在 **设置类型** 字段中，选择 **处理管道**。
4. 选择 **创建**。
5. 选择要使用的设置，然后选择 **编辑**。
6. 在 **处理管道** 选项卡上，选择 **新建** 以添加管道操作。 有关管道的详细信息，请参阅[操作](e-invoicing-configuration-rcs.md#actions)。
7. 在 **适用性规则** 选项卡上，选择 **新建** 以添加适用性规则子句。 有关适用性规则的详细信息，请参阅[适用性规则](e-invoicing-configuration-rcs.md#applicability-rules)。
8. 在 **变量** 选项卡上，选择 **新建** 以根据需要添加变量。
9. 选择 **保存**，然后选择 **验证** 以检查配置的一致性。
10. 关闭该页面。

## <a name="deploy-the-electronic-invoicing-feature-to-the-service-environment"></a>将电子开票功能部署到服务环境

有关如何完成此任务的信息，请参阅[将电子开票功能部署到服务环境](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-service-environment)。

## <a name="deploy-the-electronic-invoicing-feature-to-a-connected-application"></a>将电子开票功能部署到连接的应用程序

有关如何完成此任务的信息，请参阅[配置应用程序设置](e-invoicing-get-started.md#configure-the-application-setup)和[将电子发票功能部署到连接的应用程序](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-connected-application)。
