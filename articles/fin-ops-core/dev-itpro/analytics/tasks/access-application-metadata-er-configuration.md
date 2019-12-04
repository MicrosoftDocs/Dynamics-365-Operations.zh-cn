---
title: 通过使用 ER 配置访问应用程序元数据
description: 本主题中的步骤介绍 Regulatory Configuration Service (RCS) 用户如何在 Finance and Operations 中通过使用元数据设计新的电子申报 (ER) 模型映射。
author: NickSelin
manager: AnnBe
ms.date: 06/28/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: aa8444b081650e3d375e6f28f47866c8d4853721
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772455"
---
# <a name="access-application-metadata-by-using-er-configuration"></a>通过使用 ER 配置访问应用程序元数据

[!include [task guide banner](../../includes/task-guide-banner.md)]

以下步骤介绍系统管理员或电子报表开发人员角色的 Regulatory Configuration Service (RCS) 用户如何使用应用程序元数据设计新的电子报表 (ER) 模型映射。 可访问应用程序元数据，方法是使用其中包含一组示例元数据的 ER 配置访问外贸交易。 为了完成这些步骤，您必须首先在 RCS 中完成[创建配置提供程序并标记为当前运行的](er-configuration-provider-mark-it-active-2016-11.md)主题中的步骤。 然后完成[在 RCS 中准备要使用的应用程序元数据](prepare-application-metadata-rcs.md)主题中的步骤。

## <a name="prerequisites"></a>先决条件
1. 转到**所有工作区** > **电子申报**。 
2. 确保示例公司 Litware 公司的配置提供程序可用且标记为**有效**。 如果没有看到此配置提供程序，请首先完成[创建配置提供程序并标记为当前运行的](er-configuration-provider-mark-it-active-2016-11.md)这一过程中的步骤。 

## <a name="import-metadata-configuration"></a>导入元数据配置 
1. 单击**元数据配置**。 
2. 导入包含已配置为为外贸业务生成电子单据的元数据的 ER 元数据配置。 由于已完成了[在 RCS 中准备要使用的应用程序元数据](prepare-application-metadata-rcs.md)过程中的步骤，所以此 ER 元数据配置已导出为 XML 文件。 
3. 单击**交换**。 
4. 单击**从 XML 文件加载**。 
5. 单击**浏览**并选择“Foreign trade metadata.xml”文件。 
6. 单击 **确定**。 
7. 关闭该页面。 

## <a name="create-data-model-configuration"></a>创建数据模型配置
1. 单击**申报配置**。 
2. 单击**创建配置**，以打开下拉对话框。 
3. 在**名称**字段中键入“外贸模型”。 
4. 单击**创建配置**。 
5. 单击**设计器**。 
6. 单击**新建**，以打开对话框。 
7. 在**名称**字段中，键入“根”。 
8. 单击**添加**。 
9. 单击**新建**，以打开对话框。 
10. 在**名称**字段中，键入“交易”。 
11. 在**物料类型**字段中，选择**记录列表**。 
12. 单击**添加**。 
13. 单击**新建**，以打开对话框。 
14. 在**名称**字段中，键入“商品代码”。 
15. 在**物料类型**字段中，选择**字符串**。 
16. 单击**添加**。 
17. 单击**新建**，以打开对话框。 
18. 在**名称**字段中，键入“开票金额”。 
19. 在**物料类型**字段中，选择**实际**。 
20. 单击**添加**。 
21. 单击**新建**，以打开对话框。 
22. 在**名称**字段中，键入“日期”。 
23. 在**物料类型**字段中，选择**日期**。 
24. 单击**添加**。 
25. 单击**根引用**。 
26. 单击 **确定**。 
27. 单击**保存**。 
28. 关闭该页面。 
29. 单击**更改状态**。 
30. 单击**完成**。 
31. 单击 **确定**。 

## <a name="create-model-mapping-configuration"></a>创建模型映射配置 
1. 单击**创建配置**，以打开下拉对话框。 
2. 在**新建**字段中，输入“基于数据模型‘外贸模型’的模型映射”。 
3. 在**名称**字段中键入“外贸映射”。 
4. 单击**创建配置**。 
5. 展开**先决条件**部分。 
6. 单击**编辑**。 
7. 单击**新建**。 
8. 在列表中，标记所选的行。 
9. 在**先决条件组件类型**字段中，选择**配置**。 
10. 选择**外贸元数据**配置。 
11. 单击**保存**。 
12. 已添加了对“外贸元数据”配置版本 1 的引用。 设计此模型映射时，将提供来自此配置的应用程序元数据。 
13. 关闭该页面。 
14. 单击**设计器**。 
15. 单击**设计器**。 
16. 在树中，选择 **Dynamics 365 for Operations\表记录**。 
17. 单击**添加根**。 
18. 在**名称**字段中，键入“内部统计”。 
19. 选择**内部统计**表记录。 
20. 单击 **确定**。 

> [!NOTE]
> 仅提供了 2 个表，因为仅向当前正在使用的元数据集添加了 2 个表。 

21. 单击**绑定**。 
22. 在树中，展开**内部统计**。 
23. 在树中，选择**内部统计\AmountMST**。 
24. 在树中，展开**交易 = 内部统计**。 
25. 在树中，选择**交易 = 内部统计\开票金额**。 
26. 单击**绑定**。 
27. 在树中，选择**内部统计\TransDate**。 
28. 在树中，选择**交易 = 内部统计\日期**。 
29. 单击**绑定**。 
30. 在树中，展开**内部统计\>关系**。 
31. 在树中，展开**内部统计\>关系\IntrastatCommodity**。 
32. 在树中，选择**内部统计\>关系\IntrastatCommodity\代码**。 
33. 在树中，选择**交易 = 内部统计\商品代码**。 
34. 单击**绑定**。 
35. 单击**验证**。 

> [!NOTE]
> 我们已使用来自引用的 ER 元数据配置的应用程序元数据详细信息成功绑定了带有介绍的数据源项的数据模型的元素。 
36. 单击**保存**。 
37. 关闭该页面。 
38. 关闭该页面。 
39. 在需要时，您可以扩展现有的元数据集，然后导出新的已完成版本的 ER 元数据配置。 然后，您可以将其导入 RCS，并更新配置的模型映射配置（引用已导入元数据配置的新版本）的先决条件。 

> [!NOTE]
> 本地部署的应用程序（此时使用本地业务数据 (LBD) 或本地部署的部署模型）只能使用这种方法获取有关应用程序元数据的信息。
        