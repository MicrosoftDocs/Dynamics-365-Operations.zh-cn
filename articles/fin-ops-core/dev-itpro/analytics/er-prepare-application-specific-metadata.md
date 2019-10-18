---
title: 为 RCS 和 ER 准备应用程序特定的元数据
description: 本主题介绍如何为 Regulatory Configuration Service (RCS) 和电子申报 (ER) 准备应用程序特定的元数据。
author: NickSelin
manager: AnnBe
ms.date: 04/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: c036eab38845db8427c447b27cce0be8048669fd
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/30/2019
ms.locfileid: "2248646"
---
# <a name="prepare-application-specific-metadata-for-rcs"></a>为 RCS 准备应用程序特定的元数据

[!include[banner](../includes/banner.md)]

本主题引导您学习以下任务的示例：

- [准备可在 RCS 中使用的应用程序元数据](#prepare-application-metadata-that-can-be-used-in-rcs)
- [通过使用 ER 配置访问应用程序元数据](#access-application-metadata-by-using-an-er-configuration)
- [通过使用相连应用程序访问应用程序元数据](#access-application-metadata-by-using-connected-applications)

## <a name="prepare-application-metadata-that-can-be-used-in-rcs"></a>准备可在 RCS 中使用的应用程序元数据

以下过程显示具有**系统管理员**或**电子申报开发人员**角色的用户如何创建其中包含应用程序的元数据，并用于在 Regulatory Configuration Service (RCS) 中设计 ER 模型映射配置的电子申报 (ER) 配置。 此示例中创建的示例 ER 模型映射配置将用于访问外贸交易。

对于此示例，您要使用 RCS 为应用程序设计 ER 解决方案，用于生成其中包含来自外贸业务域的信息的电子单据。 若要 ER 数据模型与所需数据源之间的映射，必须可以在 RCS 中访问应用程序元数据。 因此，在 ER 解决方案的设计过程中，必须新建一个 ER 元数据配置，其中包含为所选业务域生成 ER 报表当前所需全部元数据。

> [!NOTE]
> 在此示例中，您将创建示例公司 Litware 公司的配置。这些步骤可以在任何公司执行。

1. 转到**组织管理 \> 工作区 \> 电子申报**。
2. 确保示例公司 Litware 公司的配置提供程序可用且标记为**有效**。 如果没有看到此配置提供程序，请完成[创建配置提供程序并标记为当前运行的](tasks/er-configuration-provider-mark-it-active-2016-11.md)过程。 
3. 选择**元数据配置**。
4. 选择**创建配置**。
5. 在下拉对话框的**名称**字段中，输入名称。 对于此示例，请输入**外贸元数据**。
6. 选择**创建配置**。
7. 选择**设计器**。
8. 选择**添加**。

    > [!NOTE]
    > 可为整个应用程序，或所选模型或模块选择所有元数据。 在这两种情况下，请注意，将自动添加以下元数据：记录表、枚举和扩展数据类型 (EDT)。 如果需要更多元数据类型，则必须手动添加。

必须添加一些与外贸交易有关的元数据，并手动选择元数据项。

9. 选择**添加数据源 \> 表记录**。
10. 筛选**名称**字段中的**内部统计**值。
11. 选择**内部统计**表记录。
12. 选择**确定**。

必须添加有关“内部统计”记录表的元数据信息。

13. 在树中，选择**表记录‘内部统计’ \> \>关系 \> IntrastatCommodity（表记录 EcoResCategory）**。
14. 选择**添加元数据**。

    > [!NOTE]
    > 必须手动添加有关所选记录表的所需关系的元数据。

15. 选择**添加数据源**。
16. 选择**枚举**。
17. 筛选**名称**字段中的 **IntrastatDirection** 值。
18. 选择 **IntrastatDirection** 枚举记录。
19. 选择**确定**。
20. 选择**保存**。
21. 关闭该页面。
22. 完成元数据配置的草稿版本。

    1. 选择**更改状态 \> 完成**。
    2. 选择**确定**。
    3. 选择已完成版本 1。

23. 将元数据配置的已完成版本作为 XML 文件从应用程序导出：

    1. 选择**交还 \> 导出为 XML 文件**。
    2. 选择**确定**。

将把创建的 ER 元数据配置另存为 **Foreign trade metadata.xml** 文件。 现在可将其导入到 RCS 中，以便将其用作外贸业务域的元数据源。 可根据此信息指定应用程序元数据与 ER 数据模型之间的映射。

## <a name="access-application-metadata-by-using-an-er-configuration"></a>通过使用 ER 配置访问应用程序元数据

以下过程显示具有**系统管理员**或**电子申报开发人员**角色的 RCS 用户如何使用来自应用程序的元数据设计新的 ER 模型映射。 可访问应用程序元数据，方法是使用其中包含一组示例元数据的 ER 配置访问外贸交易。

必须首先完成以下过程，才能完成此过程：

- [创建一个配置提供程序，并标记其为当前运行的](tasks/er-configuration-provider-mark-it-active-2016-11.md)
- [准备可在 RCS 中使用的应用程序元数据](#prepare-application-metadata-that-can-be-used-in-rcs)

1. 转到**所有工作区 \> 电子申报**。
2. 确保示例公司 Litware 公司的配置提供程序可用且标记为**有效**。 如果没有看到此配置提供程序，请完成[创建配置提供程序并标记为当前运行的](tasks/er-configuration-provider-mark-it-active-2016-11.md)过程。 
3. 导入包含应用程序的元数据且为了生成外贸业务域所用电子单据而配置的元数据的 ER 元数据配置。 您已在本主题前面的[准备可在 RCS 中使用的应用程序元数据](#prepare-application-metadata-that-can-be-used-in-rcs)过程中创建了此 ER 元数据配置并将其导出为 XML 文件。

    1. 选择**元数据配置**。
    2. 选择**交换**。
    3. 选择**从 XML 文件加载**。
    4. 浏览到并选择 **Foreign trade metadata.xml** 文件。
    5. 选择**确定**。
    6. 关闭该页面。

4. 创建数据模型配置：

    1. 选择**申报配置**。
    2. 选择**创建配置**。
    3. 在下拉对话框的**名称**字段中，输入**外贸模型**。
    4. 选择**创建配置**。
    5. 选择**设计器**。
    6. 选择**新建**，以打开对话框。

        1. 在**名称**字段中，键入**根**。
        2. 选择**添加**。
    
    7. 选择**新建**，以打开对话框。

        1. 在**名称**字段中，键入**交易**。
        2. 在**物料类型**字段中，选择**记录列表**。
        3. 选择**添加**。
 
    8. 选择**新建**，以打开对话框。

        1. 在**名称**字段中，键入**商品代码**。
        2. 在**物料类型**字段中，选择**字符串**。
        3. 选择**添加**。

    9. 选择**新建**，以打开对话框。

        1. 在“名称”字段中，键入**开票金额**。
        2. 在**物料类型**字段中，选择**实际**。
        3. 选择**添加**。

    10. 选择**新建**，以打开对话框。

        1. 在**名称**字段中，键入**日期**。
        2. 在**物料类型**字段中，选择**日期**。
        3. 选择**添加**。
 
    11. 选择**添加 \> 根引用**。
    12. 选择**确定**。
    13. 选择**保存**。
    14. 关闭该页面。
    15. 选择**更改状态 \> 完成**。
    16. 选择**确定**。

5. 创建模型映射配置：

    1. 选择**创建配置**。
    2. 在下拉对话框的**新建**字段中，输入**基于数据模型‘外贸模型’的模型映射**。
    3. 在**名称**字段中输入**外贸映射**。
    4. 选择**创建配置**。
    5. 在**先决条件**快速选项卡中，选择**编辑**。
    6. 选择**新建**。
    7. 在**先决条件组件类型**字段中，选择**配置**。
    8. 选择**外贸元数据**配置。
    9. 选择**保存**。 请注意，将向**外贸元数据**配置版本 1 添加引用。 设计模型映射时，将提供来自此配置的应用程序元数据。
    10. 关闭该页面。
    11. 选择**设计器**。
    12. 选择**设计器**。
    13. 在树中，选择 **Dynamics 365 for Operations \> 表记录**。
    14. 选择**添加根**。
    15. 在**名称**字段中，输入**内部统计**。
    16. 选择**内部统计**表记录。
    17. 选择**确定**。

        > [!NOTE]
        > 仅提供了两个表，因为仅向当前使用的元数据集添加了两个表。

    18. 选择**绑定**。
    19. 在树中，选择**内部统计 \> AmountMST**。
    20. 在树中，选择**交易 = 内部统计 \> 开票金额**。
    21. 选择**绑定**。
    22. 在树中，选择**内部统计 \> TransDate**。
    23. 在树中，选择**交易 = 内部统计 \> 日期**。
    24. 选择**绑定**。
    25. 在树中，选择**内部统计 \> \>关系 \> IntrastatCommodity \> 代码**。
    26. 在树中，选择**交易 = 内部统计 \> 商品代码**。
    27. 选择**绑定**。
    28. 选择**验证**。

        > [!NOTE]
        > 完成验证之后，我们已使用来自引用的 ER 元数据配置的应用程序元数据详细信息将数据模型的元素成功绑定到了介绍的数据源项。

    29. 选择**保存**。

如果需要，可以扩展应用程序中的现有元数据集。 然后就可以导出新的 ER 元数据配置已完成版本，导入到 RCS 中，然后更新引用新的所导入元数据配置版本的所配置模型映射配置的必备条件。

> [!NOTE]
> 本地部署的应用程序（即在对应用程序使用本地业务数据 \[LBD\] 或本地部署的部署模型）只能使用这种方法获取有关应用程序元数据的信息。

## <a name="access-application-metadata-by-using-connected-applications"></a>通过使用相连应用程序访问应用程序元数据

以下过程显示具有**系统管理员**或**电子申报开发人员**角色的 RCS 用户如何使用应用程序的元数据设计新的 ER 模型映射。 将使用与 RCS 相连的应用程序联机访问应用程序元数据。 将配置示例 ER 模型映射以访问外贸交易。

为了完成此过程，您必须首先在 RCS 中完成[创建配置提供程序并标记为当前运行的](tasks/er-configuration-provider-mark-it-active-2016-11.md)过程。 如果尚未完成本主题中前面的[使用 ER 配置访问应用程序元数据](#access-application-metadata-by-using-an-er-configuration)过程，请转至[Dynamics 365 for Finance and Operations 8.1 电子申报任务指南](https://go.microsoft.com/fwlink/?linkid=2082739)页提前下载以下 ER 配置文件并在本地保存：**Foreign trade metadata.xml**、**Foreign trade model.xml** 和 **Foreign trade mapping.xml**。


### <a name="get-required-er-configurations"></a>获取所需的 ER 配置

如果已经完成了本主题前面的[使用 ER 配置访问应用程序元数据](#access-application-metadata-by-using-an-er-configuration)过程，则当前 RCS 实例中已经拥有了所有必需的 ER 配置（外贸元数据、模型和映射配置）。 在这种情况下，您可以跳过此过程。

1. 转到**所有工作区 \> 电子申报**。
2. 选择**申报配置**。
3. 加载 **Foreign trade metadata.xml**、**Foreign trade model.xml** 和 **Foreign trade mapping.xml** 配置文件，并对这些文件每一个重复执行下面的一系列步骤：

    1. 选择**交换**。
    2. 选择**从 XML 文件加载**。
    3. 选择**浏览**，然后选择文件。
    4. 选择**确定**。

### <a name="register-the-connection-with-the-application"></a>注册与应用程序之间的连接

1. 转到**所有工作区 \> 电子申报**。
2. 选择**相连应用程序**。
3. 确保配置的应用程序基于 Microsoft Azure，并且通常可供 RCS 用户访问。 当前 RCS 用户必须可访问所配置应用程序，已注册为此应用程序的用户，并且其角色有权访问此应用程序的元数据。
4. 选择**新建**。
5. 在**名称**字段，输入 **MyConnectedApp** 作为相连应用程序的名称。
6. 在**应用程序**字段中，指定应用程序的 URL。
7. 在**租户**字段中，指定应用程序的提供程序。
8. 选择**保存**。 
9. 检查与配置的应用程序之间的连接时，请在**连接到远程应用程序**页中选择**选择此处连接到所选远程应用程序**链接。 
10. 选择**检查连接**以验证所配置应用程序的访问权限。
11. 选择**关闭**。

完成此过程且连接验证成功后，将在当前网格中更新所配置应用程序的版本和租户详细信息。

### <a name="review-the-existing-model-mapping-configuration"></a>检查现有模型映射配置

1. 转到**所有工作区 \> 电子申报**。
2. 选择**申报配置**。
3. 在树中，选择**外贸模型 \> 外贸映射**。
4. 选择**先决条件**快速选项卡。

    > [!NOTE]
    > 此映射当前引用元数据配置。 设计此模型映射时，将提供来自此配置的应用程序元数据。

4. 选择**设计器**。
5. 选择**设计器**。
6. 在树中，选择 **Dynamics 365 for Operations \> 表记录**。
7. 选择**添加根**。
8. 在**表格**字段中，输入或选择一个值。

    > [!NOTE]
    > 此映射当前引用元数据配置。 设计此模型映射时，将提供来自此配置的应用程序元数据。

9. 选择**取消**。

### <a name="assign-the-connected-application-to-a-model-mapping"></a>将相连应用程序分配给模型映射

1. 选择**编辑**。
2. 在**相连应用程序**字段中，选择 **MyConnectedApp** 应用程序。

    > [!NOTE]
    > 此映射引用所选相连应用程序的元数据。 如果映射同时引用元数据配置和相连应用程序时，将使用相连应用程序的元数据。

3. 选择**设计器**。
4. 选择**设计器**。
5. 在树中，选择 **Dynamics 365 for Operations \> 表记录**。
6. 选择**添加根**。
7. 在**表格**字段中，输入或选择一个值。

    > [!NOTE]
    > 此时提供了两个以上的应用程序表，因为此映射使用已经为其分配的相连应用程序的所有元数据。

8. 选择**取消**。
9. 选择**验证**。

现在已使用已为此映射分配的相连应用程序的元数据详细信息将数据模型的元素绑定到了介绍的数据源项。

如果必须使用另一个版本应用程序的元数据评估此模型映射，请再注册一个相连应用程序，将其分配给此模型映射，然后使用新元数据再次验证。

## <a name="additional-resources"></a>其他资源

也可以播放应用程序中的**准备可在 RCS 中使用的应用程序元数据**任务指南，以及 RCS 中的**通过使用 ER 配置访问应用程序元数据**和**通过使用相连应用程序访问应用程序元数据**任务指南。 可以从 [Dynamics 365 for Finance and Operations 8.1 电子申报任务指南](https://go.microsoft.com/fwlink/?linkid=2082739)页下载这些任务指南。