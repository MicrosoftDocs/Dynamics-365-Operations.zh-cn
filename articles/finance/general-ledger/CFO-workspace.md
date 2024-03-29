---
title: 向首席财务官工作区添加财务维度
description: 本文说明如何向 CFO 工作区添加财务维度，以便可将其用于分类帐和预算报表。
author: aprilolson
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: ea453eed826dec2e97371ec559e91b94933bdce6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853371"
---
# <a name="add-financial-dimensions-to-the-cfo-workspace"></a>向首席财务官工作区添加财务维度

[!include [banner](../includes/banner.md)]

本文说明如何向首席财务官 (CFO) 工作区添加财务维度，以便可将其用于分类帐和预算报表。 CFO 工作区具有 **概述** 选项卡和 **财务** 选项卡。这两个选项卡上的报表受以下两个度量支持：LedgerActivityMeasure 和 BudgetActivityMeasure。 这两个度量与 DimensionCombinationEntity 实体之间存在关系。 因此，您可以选择维度。

1. 在 Finance 中的 **实体商店** 页中，更新 **LedgerActivityMeasure** 和 **BudgetActivityMeasure** 度量。
2. 在 Microsoft Visual Studio 中，打开“应用程序资源管理器”，然后搜索 **LedgerCFO**。
3. 在 **资源** 下，打开 **LedgerCFOWorkspacePBIX**。
4. 资源在 Microsoft Power BI Desktop 中打开时，依次选择 **获取数据**、**SQL Server 数据库** 和 **连接**。
5. 输入服务器名称，然后输入 **AxDW** 作为数据库。 选择 **DirectQuery**，然后选择 **确定**。
6. 搜索并选择 **LedgerActivityMeasure\_DimensionCombination**，然后选择 **加载**。

    > [!TIP]
    > 在 **字段** 列表中，重命名表 **财务维度**，以便轻松识别。

7. 选择 **管理关系**，然后选择 **新建**。
8. 在第一个字段中，选择 **总帐活动**，然后选择 **LedgerDimension**。
9. 在第二个字段中，选择 **LedgerActivityMeasure\_DimensionCombination**（如果已重命名表，则选择 **财务维度**）。 选择 **DimensionCombinationRECID** 标题。
10. 在 **基数** 字段中，选择 **多对单**。
11. 将 **跨筛选器方向** 值更改为 **单一**。
12. 同时选择 **使此关系可用** 和 **假设引用完整性**，选择 **确定**，然后选择 **关闭**。

    [![创建关系。](./media/Create-relationship.png)](./media/Create-relationship.png)

13. 在 **字段** 列表中，应该可以看到表和可用财务维度。 将所需财务维度拖到报表级筛选器。
14. 保存所做的更改。
15. 在应用程序对象树 (AOT) 中，右键单击项目，然后选择 **同步**。
16. 构建项目，然后打开应用程序查看结果。

    [![已完成的工作区。](./media/workspace.png)](./media/workspace.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
