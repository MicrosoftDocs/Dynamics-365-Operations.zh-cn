---
title: ER 将财务维度用作数据源（第 4 部分 - 运行报表）
description: 本主题介绍如何配置电子报告 (ER) 模型以将财务维度用作 ER 报表的数据源。 （第 4 部分）
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c1fe332de84339d3369ba495ca13f50c4901f366
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092267"
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
![ER 配置页](../media/er-financial-dimensions-guides-run1.png)
5. 在“维度名称”字段中，输入或选择一个值。
    * 若要选择当前公司中的所有维度，请输入以下信息：BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project  
![ER 配置页](../media/er-financial-dimensions-guides-run2.png)
6. 扩展“要包括的记录”部分。
7. 单击“筛选器”。
8. 选择“分类日记帐”表和“日记帐批号”字段的行。
9. 在“标准”字段中，键入“00057”。
10. 单击“确定”。
11. 单击“确定”。
![ER 配置页](../media/er-financial-dimensions-guides-run3.png)
    * 检查生成的输出。 设置的相应维度中的财务维度表示所选批次的每个交易。 运行此报表并选择不同维度，以便了解该报表不依赖所选维度数量或为此实例配置的维度数量。  
![ER 配置页](../media/er-financial-dimensions-guides-run4.png)
