---
title: 自定义主数据查找的税务配置
description: 本文介绍如何自定义税务配置以扩展主数据查找功能。
author: kai-cloud
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: pashao
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 31c15c47fa1dc6861ff555a991d5f9233b7df35e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8845175"
---
# <a name="customize-tax-configurations-for-master-data-lookup"></a>自定义主数据查找的税务配置

[!include [banner](../includes/banner.md)]

按照本文中的步骤自定义税务配置以扩展主数据查找功能。

## <a name="import-a-tax-configuration-provided-by-microsoft"></a>导入 Microsoft 提供的税务配置

1. 在 Regulatory Configuration Service (RCS) 中，在 **电子报告** 工作区中，选择 **Microsoft** 配置提供程序。
2. 选择 **存储库**。
3. 选择 **全局**，然后选择 **打开**。
4. 选择一个税务配置，如 **税款计算配置**，然后在 **版本** 选项卡上选择一个版本。
5. 选择 **导入**。

> [!NOTE]
> 默认情况下，将导入 Dataverse 模型映射。 如果您在配置导入过程中收到警告消息，请在 Dataverse 中启用虚拟实体。 有关详细信息，请参阅[启用 Dataverse 虚拟实体](../../fin-ops-core/dev-itpro/power-platform/enable-virtual-entities.md)。

## <a name="create-a-customized-data-model-configuration"></a>创建自定义数据模型配置

1. 在 **电子报告** 工作区中，选择 **税务配置**，然后选择要扩展的数据模型配置。 例如，选择 **税款计算数据模型**。
2. 选择 **创建配置**。
3. 选择 **派生自名称的应纳税单据模型: 税款计算数据模型，Microsoft**。
4. 在 **名称** 字段中，输入 **自定义数据模型**。
5. 选择 **创建配置**。

## <a name="create-customized-reference-models"></a>创建自定义引用模型

1. 在 **税务配置** 页面上，选择 **自定义数据模型**，然后选择 **设计器**。
2. 选择省略号按钮 (**...**)，然后选择 **引用模型** 视图。

    [![引用模型。](./media/pic2.png)](./media/pic2.png)

3. 创建自定义引用模型。 自定义模型是根模型。 自定义实体是一个记录列表。 自定义字段是您要在查找中使用的字符串字段。 您可以根据需要添加更多字段。
4. 选择省略号按钮 (**...**)，然后选择 **应纳税单据** 视图。
5. 选择要绑定到自定义引用模型的属性。 例如，选择 **自定义属性**，然后按照以下步骤操作：

    1. 选择 **选择引用模型**。
    2. 选择 **自定义模型**，然后选择 **确定**。 引用模型名称将更新为 **自然键** 字段的值。

        [![选择引用模型对话框。](./media/pic5.png)](./media/pic5.png)

    3. 选择 **保存**，然后选择 **完成**。

## <a name="create-a-customized-model-mapping-configuration"></a>创建自定义模型映射配置

1. 在 **电子报告** 工作区中，选择 **税务配置**，然后选择 **Dataverse 模型映射** 配置。
2. 在 **模型映射的默认值** 字段中，选择 **否**。
3. 选择 **创建配置**。
4. 选择 **派生自名称的应纳税单据模型映射: Dataverse 模型映射，Microsoft**。
5. 在 **名称** 字段中，输入 **自定义模型映射**。
6. 在 **目标模型** 字段中，选择 **自定义数据模型** 数据模型。
7. 选择 **创建配置**。

    [![“创建配置”下拉对话框。](./media/pic6.png)](./media/pic6.png)

8. 选择 **自定义模型映射**，将 **相连应用程序** 字段设置为在[设置用于主数据查找的环境](tax-service-set-up-environment-master-data-lookup.md)的步骤 8 中创建的连接。
9. 将 **模型映射的默认值** 字段设置为 **是**。

## <a name="create-customized-model-mappings"></a>创建自定义模型映射

1. 在 **税务配置** 页面上，选择 **自定义模型映射**。
2. 选择 **设计器**，然后选择 **自定义模型**。

    [![自定义模型。](./media/pic8.png)](./media/pic8.png)

## <a name="map-a-model-mapping-to-a-dataverse-entity"></a>将模型映射映射映射到 Dataverse 实体

1. 在 **模型映射设计器** 页面上，选择 **自定义模型**，然后选择 **设计器**。
2. 在 **数据源类型** 树中，选择 **Dataverse 表**。
3. 在 **数据源** 选项卡上，选择 **添加根**。
4. 在 **名称** 字段中，输入 **自定义 Dataverse**。
5. 在第二个 **名称** 字段中，选择一个实体。
6. 选择 **确定**。

    [![“表”数据源属性对话框。](./media/pic9.png)](./media/pic9.png)

7. 选择 **自定义 Dataverse** 和 **自定义实体**，然后选择 **绑定**。

    [![自定义 Dataverse 和自定义实体绑定。](./media/pic10.png)](./media/pic10.png)

8. 在 **自定义 Dataverse** 和 **自定义字段** 下，选择一个字段，然后选择 **绑定**。

    [![自定义 Dataverse 和自定义字段绑定。](./media/pic11.png)](./media/pic11.png)

9. 选择 **保存**，然后选择 **完成**。

## <a name="create-a-customized-tax-configuration"></a>创建自定义税务配置

1. 在 **电子报告** 工作区中，选择 **税务配置**，然后选择 **税款计算配置**。
2. 选择 **创建配置**。
3. 选择 **派生自名称的税务服务配置: 税款计算配置，Microsoft**。
4. 在 **名称** 字段中，输入 **自定义配置**。
5. 选择 **创建配置**。
6. 选择 **自定义配置**，然后选择 **设计器**。
7. 在 **数据模型** 字段中，选择 **自定义数据模型**。
8. 在 **数据模型版本** 字段中，选择对应的数据模型版本。

    [![属性部分。](./media/pic13.png)](./media/pic13.png)

9. 选择 **完成**。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
