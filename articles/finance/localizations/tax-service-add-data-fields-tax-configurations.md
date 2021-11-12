---
title: 在税务配置中添加数据字段
description: 本主题说明如何通过添加数据字段自定义税务配置。
author: Kai-Cloud
ms.date: 10/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 590c2d62995f260ba4277e1031349b0dc43f1417
ms.sourcegitcommit: 1707cf45217db6801df260ff60f4648bd9a4bb68
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/23/2021
ms.locfileid: "7674892"
---
# <a name="add-data-fields-in-tax-configurations"></a>在税务配置中添加数据字段

[!include [banner](../includes/banner.md)]

本主题说明如何通过使用[在税务集成中添加的数据字段](tax-service-add-data-fields-tax-integration-by-extension.md)自定义税务配置。

## <a name="customize-the-tax-data-model"></a>自定义税务数据模型

1. 在 Microsoft Dynamics 365 Finance 中，转到 **电子报告** > **税务配置**。
2. 在配置树中，选择 **税款计算数据模型**。 然后，在操作窗格上，选择 **创建配置**。 

  > [!NOTE] 
  > 如果没有可用的配置提供程序，请创建一个配置，并使其对您的税务配置可用。 有关详细信息，请参阅[创建配置提供程序并将其标记为有效](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md)。
  
3. 在下拉对话框中，选择 **派生自名称的应纳税单据模型: 税款计算数据模型，Microsoft**，输入新税务数据模型的名称，然后选择 **创建配置**。
4. 选择您刚创建的税务数据模型，然后在操作窗格上，选择 **设计器**。
5. 展开数据模型树，选择 **行**，然后选择 **新建**。
6. 在 **创建节点** 对话框中，输入名称，指定物料类型，然后选择 **添加**。
7. 添加任何必需的列。
8. 在操作窗格上，选择 **保存**，然后选择 **完成**。
9. 关闭页面，然后查看税务数据模型的已完成版本。

## <a name="customize-the-tax-configuration"></a>自定义税务配置

1. 在 Finance 中，转到 **电子报告** > **税务配置**。
2. 在配置树中，选择 **税款计算配置**。 然后，在操作窗格上，选择 **创建配置**。
3. 在下拉对话框中，选择 **派生自名称的税务服务配置: 税款计算配置，Microsoft**，输入新税务配置的名称，然后选择 **创建配置**。
4. 选择您刚创建的税务配置，然后在操作窗格上，选择 **设计器**。
5. 在 **属性** 部分中，在 **数据模型** 字段中，选择您之前创建的自定义税务数据模型。
6. 在 **数据模型版本** 字段中，选择税务数据模型的已完成版本。
7. 选择 **添加**，然后添加所需的税务措施。
8. 在操作窗格上，选择 **保存**，然后选择 **完成**。
9. 关闭页面，然后查看税务配置的已完成版本。

## <a name="implement-tax-features-in-the-customized-tax-configuration"></a>在自定义税务配置中实施税务功能

1. 在 Regulatory Configuration Service (RCS) 中，转到 **全球化功能** > **税务**。
2. 选择 **添加**，输入有关新功能的信息，然后选择 **创建功能**。
3. 在 **版本** 选项卡上，选择功能，然后选择 **编辑**。
4. 在 **常规** 选项卡上，在 **配置版本** 字段中，选择自定义税务配置和版本。
5. 在 **管理列** 对话框中，选择要包含在自定义税务措施中的标题和行列，然后选择向右箭头按钮将其添加到 **所选列** 列表中。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
