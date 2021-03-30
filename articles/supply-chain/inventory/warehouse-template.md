---
title: 使用仓库配置模板设置仓库
description: 此主题介绍如何使用仓库配置模板设置仓库。
author: perlynne
manager: tfehr
ms.date: 11/16/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DataManagementWorkspace, DMFQuickImportExportEnhanced, DMFDefinitionGroupTemplate, DMFEntityTemplateDefinitionLoadDialog
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 7bf69ccec59f2c540d71d44347bd99dc2378dc4c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5224970"
---
# <a name="set-up-a-warehouse-by-using-a-warehouse-configuration-template"></a>使用仓库配置模板设置仓库

[!include [banner](../includes/banner.md)]

此主题介绍如何使用仓库配置模板设置仓库。 有多个预定义的配置模板可供使用。 有关如何使用这些模板的信息，请参阅[配置数据模板](../../dev-itpro/data-entities/configuration-data-templates.md)。

## <a name="scenarios-where-configuration-templates-can-be-helpful"></a>配置模板可能有用的方案

配置模板在许多方案中都有用。 下面举了一些示例加以说明：

- 您完成了一个配置设置并在测试环境中进行了测试，您现在想要将该设置复制到生产环境。
- 您想要向多个法人推出该仓库设置或在相同法人中创建新的仓库。
- 您想要尽快为演示仓库功能做好准备。
- 您想要现有的物料和仓库使用仓库管理中的功能，而不是使用库存管理中的功能。

此主题主要介绍这些方案中的第一个方案。 它演示了您可以如何使用配置模板将测试环境中的配置设置复制到生产环境。

## <a name="copy-a-configuration-setup-from-a-test-environment-to-a-production-environment"></a>将测试环境中的配置设置复制到生产环境

在此方案中，测试环境中已经存在用于仓库和一些交易流程的配置设置。 您现在想要将仓库的配置设置从测试环境复制到生产环境。

> [!NOTE]
> 重要的一点是在复制配置设置时包括其他相关设置数据。 例如，您想要复制测试环境中的设置以设置产品。 但在创建该产品前，您不能设置产品的固定领料库位。 尽管单个配置模板不支持这种类型的依赖项，但存在支持它的默认数据模板。 您可以将这些默认数据模板轻松包括在配置流程中。

### <a name="export-a-default-warehouse-template"></a>导出默认仓库模板 

1. 打开 **数据管理** 工作区。

    > [!NOTE]
    > 如果您是第一次使用此工作区，必须加载所有数据实体后才能继续。

2. 选择 **模板** 磁贴，然后选择 **加载默认模板** 以加载默认模板。

    > [!NOTE]
    > **加载默认模板** 仅在 **增强型** 视图中可用。 选择 **框架参数**，然后在 **查看默认值** 字段中选择 **增强型视图**。

3. 加载默认模板后，可以进行更改，使其满足您的业务要求。

    > [!NOTE]
    > 若要加载默认模板并导入模板，必须拥有系统管理员访问权限。 此要求有助于保证所有实体正确地加载到模板。

4. 确保您所在的法人是您要从中导出公司特定数据的法人。
5. 在该工作区中，选择 **导出**。
6. 创建新的导出项目。
7. 选择 **+ 添加模板**，并找到 **400 - WMS** 默认仓库模板。 此模板添加用于仓库配置的数据实体。

    > [!NOTE]
    > 如果必须要筛选您正在导出的数据（例如，您只想要导出与特定仓库有关的数据），则必须评估每个数据实体并添加通过查询进行筛选。 或者可以导出所有数据，然后删除在目标文件中不需要的记录。

8. 选择 **导出**。 导出与项目中的所有数据实体有关的数据。

您可以下载数据包的压缩文件。 此文件包含所选格式（例如，Excel 格式）的所有数据。 正如前面所指出的，数据包文件中的一些记录可能必须进行更改，才能将其导入到生产环境。 如果更新记录，请确保不要更改文件名。

### <a name="import-a-warehouse-configuration-setup"></a>导入仓库配置设置

1. 在目标环境中，请确保您所在的公司是您要将仓库数据导入其中的公司。

    > [!NOTE]
    > 在执行导入前，应确定任何数据依赖项。 例如，**仓库管理** 模板包括命名为 **仓库处置代码** 的数据实体。 此实体包含与 **处置代码** 设置页（**仓库管理** > **设置** > **移动设备** > **处置代码**）有关的数据。 如果现有设置已处理销售订单的退货流程，则 **退货处置代码** 字段包含值。 此字段中的处置代码与 **处置代码** 数据实体有关，是 **销售和市场营销** 模板的一部分。 如果来自 **处置代码** 数据实体的数据不在来自 **仓库处置代码** 字段的数据的前面导入，导入将失败。

2. 在 **数据管理** 工作区中，选择 **导入**。
3. 创建新的导入项目。
4. 选择 **+ 添加文件**，并上载数据包的压缩文件。
5. 选择 **导入**。 在 **增强型** 视图中，可以使用 **筛选器** 选项快速获取在导入过程中可能发生的问题的概览。

**查看执行** 日志提供与导入的各个数据实体有关的详细信息。 您可以使用暂存数据视图快速定位到目标数据。 这样一来，您可以看到导入的数据在应用程序中的相关页面上的外观。 当您使用默认数据模板时，各数据实体的导入顺序采用预定义的方式，以帮助保证先导入所有依赖项数据。 如果自定义数据实体是项目的一部分，必须确保定义正确的顺序。 有关详细信息，请参阅[配置数据模板](../../dev-itpro/data-entities/configuration-data-templates.md)。

若要了解有关如何在同一个实例内使用仓库模板将仓库的配置从一家公司复制到新公司的详细信息，请观看 YouTube 上的这个 3 分钟的视频：[如何使用仓库模板复制 Finance and Operations 的配置](https://www.youtube.com/watch?v=K2WIfFlqJYs)。

## <a name="related-topic"></a>相关主题

[配置数据模板](../../dev-itpro/data-entities/configuration-data-templates.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]