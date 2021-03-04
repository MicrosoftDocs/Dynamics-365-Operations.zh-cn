---
title: 通过使用相连应用程序访问应用程序元数据
description: 本主题中的步骤介绍 Regulatory Configuration Service (RCS) 用户如何在 Finance and Operations 中通过使用元数据设计新的电子申报 (ER) 模型映射。
author: NickSelin
manager: AnnBe
ms.date: 06/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 751ac21dc056373e1cd89a5149bf38789134e0cc
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682133"
---
# <a name="access-application-metadata-by-using-connected-applications"></a>通过使用相连应用程序访问应用程序元数据

[!include [banner](../../includes/banner.md)]

以下步骤介绍系统管理员或电子报表开发人员角色的 Regulatory Configuration Service (RCS) 用户如何使用 Finance and Operations 中的元数据设计新的电子报表 (ER) 模型映射。 将使用与 RCS 相连的应用程序联机访问应用程序元数据。 将配置示例 ER 模型映射以访问外贸交易。 为了完成这些步骤，在 RCS 中，您必须首先完成[创建配置提供程序并标记为当前运行的](er-configuration-provider-mark-it-active-2016-11.md)主题中的步骤。 如果已完成了[使用 ER 配置访问应用程序元数据](access-application-metadata-er-configuration.md)主题中的步骤，请转至[电子申报示例页](https://go.microsoft.com/fwlink/?linkid=862266)下载并保存以下 ER 配置：Foreign trade metadata.xml、Foreign trade model.xml、Foreign trade mapping.xml，然后完成此过程中的步骤。

## <a name="prerequisites"></a>先决条件
1. 转到 **所有工作区** > **电子申报**。 
2. 确保示例公司 Litware 公司的配置提供程序可用且标记为 **有效**。 如果没有看到此配置提供程序，请首先完成[创建配置提供程序并标记为当前运行的](er-configuration-provider-mark-it-active-2016-11.md)这一过程中的步骤。 

## <a name="get-required-er-configurations"></a>获取所需的 ER 配置
1. 单击 **申报配置**。 
2. 如果已经完成了[使用 ER 配置访问应用程序元数据](access-application-metadata-er-configuration.md)过程中的步骤，则当前 RCS 实例中已经拥有了所有必需的 ER 配置（外贸元数据、模型和映射配置）。 您可以跳过此子任务的所有其余步骤。 
3. 单击 **交换**。 
4. 单击 **从 XML 文件加载**。 
5. 单击 **浏览** 并选择 **Foreign trade metadata.xml** 文件。 
6. 单击 **确定**。 
7. 单击 **交换**。 
8. 单击 **从 XML 文件加载**。 
9. 单击 **浏览** 并选择 **Foreign trade model.xml** 文件。 
10. 单击 **确定**。 
11. 单击 **交换**。 
12. 单击 **从 XML 文件加载**。 
13. 单击 **浏览** 并选择 **Foreign trade mapping.xml** 文件。 
14. 单击 **确定**。 

## <a name="register-a-connected-application"></a>注册连接的应用程序
1. 关闭该页面。 
2. 关闭该页面。 
3. 转到 **所有工作区** > **电子申报**。 
4. 单击 **相连应用程序**。 
5. 确保配置的应用程序基于 Azure 且可供当前 RCS 用户访问。 还要求当前 RCS 用户可访问所选应用程序，并且已注册为此应用程序的用户，从而使其有权访问应用程序的元数据。 
6. 单击 **新建**。 
7. 在 **名称** 字段中，键入“MyConnectedApp”。 
8. 在 **应用程序** 字段中，键入“https:// mycompany.operations.dynamics.com”。 
9. 在 **租户** 字段中，键入“mycompany.onmicrosoft.com”。 
10. 单击 **保存**。 
11. 检查与配置的应用程序之间的连接时，请在 **连接到远程应用程序** 页中，单击 **单击此处连接到所选远程应用程序** 链接。 
12. 单击 **检查连接**。 
13. 单击 **关闭**。 
14. 连接验证成功完成后，将在当前网格中更新所配置应用程序的版本和租户详细信息。 

## <a name="review-existing-model-mapping-configuration"></a>检查现有模型映射配置
1. 关闭该页面。 
2. 单击 **申报配置**。 
3. 在树中，展开 **外贸模型**。 
4. 在树中，选择 **外贸模型\外贸映射**。 
5. 展开 **先决条件** 部分。 

    > [!NOTE]
    > 此映射当前引用元数据配置。 设计此模型映射时，将提供来自此配置的应用程序元数据。 

6. 单击 **设计器**。 
7. 单击 **设计器**。 
8. 在树中，选择 **Dynamics 365 for Operations\表记录**。 
9. 单击 **添加根**。 
10. 在 **表格** 字段中，输入或选择一个值。 

    > [!NOTE]
    > 此映射当前引用元数据配置。 设计此模型映射时，将提供来自此配置的应用程序元数据。 

11. 单击 **取消**。 
12. 关闭该页面。 
13. 关闭该页面。 

## <a name="assign-connected-application-to-model-mapping"></a>将相连应用程序分配给模型映射 
1. 单击 **编辑**。 
2. 选择 **MyConnectedApp** 应用程序。 

    > [!NOTE]
    > 目前此映射引用所选相连应用程序的元数据。 当同一个映射同时引用元数据配置和相连应用程序时，将使用相连应用程序的元数据。 

3. 单击 **设计器**。 
4. 单击 **设计器**。 
5. 在树中，选择 **Dynamics 365 for Operations\表记录**。 
6. 单击 **添加根**。 
7. 在 **表格** 字段中，输入或选择一个值。 

    > [!NOTE]
    > 现在提供了两个以上的应用程序表，因为此映射使用已经为其分配的相连应用程序的所有元数据。 

8. 单击 **取消**。 
9. 单击 **验证**。 

    > [!NOTE]
    > 我们已使用已为此映射分配的相连应用程序的元数据详细信息成功绑定了带有介绍的数据源项的数据模型的元素。 

10. 关闭该页面。 
11. 关闭该页面。 

如果需要使用另一个版本应用程序的元数据评估此模型映射，请再注册一个相连应用程序，将其分配给此模型映射，然后使用新元数据再次验证。


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]