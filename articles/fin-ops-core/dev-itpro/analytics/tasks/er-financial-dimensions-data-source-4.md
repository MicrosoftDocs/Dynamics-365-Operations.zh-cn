---
title: ER 将财务维度用作数据源（第 4 部分 - 运行报表）
description: 本文介绍如何配置电子报告 (ER) 模型以将财务维度用作 ER 报表的数据源。 （第 4 部分）
author: NickSelin
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5ef1944655893f191502b4d1e8e1372f6d2e755f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8881121"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-4---run-the-report"></a>ER 将财务维度用作数据源（第 4 部分 - 运行报表）

[!include [banner](../../includes/banner.md)]

以下步骤说明指定为系统管理员或电子申报开发人员角色的用户可以如何配置电子申报 (ER) 模型，以便将财务维度用作 ER 报表的数据源。 这些步骤可以在 DEMF 公司执行。

若要完成这些步骤，则必须首先完成“ER 将财务维度用作数据源（第 3 部分：设计报表）”过程中的步骤。 还必须在“电子申报参数”页面中配置默认单据类型。 下载和导入任何 ER 配置时也设置默认单据类型。 


## <a name="run-report"></a>运行报表
1. 转到“组织管理”>“电子申报”>“配置”。
2. 在树中，展开“财务维度示例模型”。
3. 在树中，选择“财务维度示例模型\分类日记帐报表”。
4. 单击“运行”。
![ER 配置页面。](../media/er-financial-dimensions-guides-run1.png)
5. 在“维度名称”字段中，输入或选择一个值。
    * 若要选择当前公司中的所有维度，请输入以下信息：BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project  
![电子报表参数滑出，维度名称下拉列表。](../media/er-financial-dimensions-guides-run2.png)
6. 扩展“要包括的记录”部分。
7. 单击“筛选器”。
8. 选择“分类日记帐”表和“日记帐批号”字段的行。
9. 在“标准”字段中，键入“00057”。
10. 单击“确定”。
11. 单击“确定”。
![电子报表参数滑出，“要包括的报表”部分。](../media/er-financial-dimensions-guides-run3.png)
    * 检查生成的输出。 设置的相应维度中的财务维度表示所选批次的每个交易。 运行此报表并选择不同维度，以便了解该报表不依赖所选维度数量或为此实例配置的维度数量。  
![电子报告配置生成的输出。](../media/er-financial-dimensions-guides-run4.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
