---
title: ER 使用可水平扩展的范围在 Excel 报表中动态添加列（第 2 部分 - 运行格式）
description: 本主题介绍如何配置电子报告 (ER) 格式以将报表生成为 OPENXML 工作表 (Excel) 文件。 （第 2 部分）
author: NickSelin
ms.date: 08/29/2018
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
ms.openlocfilehash: a62bad6ca241a2372a72e312ec5a707008a5fc09
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744979"
---
# <a name="er-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-part-2---run-format"></a>ER 使用可水平扩展的范围在 Excel 报表中动态添加列（第 2 部分 - 运行格式）

[!include [banner](../../includes/banner.md)]

下列步骤介绍指定为系统管理员或电子申报开发人员角色的用户如何配置电子申报 (ER) 格式，以便将报表生成为 OPENXML 工作表 (Excel) 文件格式，在这种文件中，可以根据可水平扩展的范围动态创建所需列。 这些步骤可以在 DEMF 公司执行。

必须首先完成“ER 使用可水平扩展的范围在 Excel 报表中动态添加列（第 1 部分：设计格式）”过程中的步骤，才能完成这些步骤。

此过程针对 Dynamics 365 for Operations 版本 1611 中增加的一项功能。


## <a name="find-created-format"></a>查找创建的格式
1. 转到“组织管理”>“电子申报”>“配置”。
2. 在树中，展开“财务维度示例模型”。
3. 在树中，选择“财务维度示例模型\包含可水平扩展范围的示例报表”。

## <a name="execute-format-to-create-excel-output"></a>执行格式以创建 Excel 输出
1. 单击“运行”。
2. 在“维度名称”字段中，键入“BusinessUnit;CostCenter;Department”。
    * 在“维度名称”字段中，输入或选择一个值。  若要选择当前公司的所有维度，请输入以下内容：BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project  
3. 扩展“要包括的记录”部分。
4. 单击“筛选器”。
5. 选择“分类日记帐”表和“日记帐批号”字段的行。
6. 在“条件”字段中，键入“00057..00058”。
    * 00057..00058  
7. 单击“确定”。
8. 单击“确定”。
    * 检查生成的输出。 请注意，新创建的 Excel 文件中包含为财务维度选择的相同数量的列。 这些列中的报表标题表示财务维度的名称。 这些列中的交易行表示财务维度的名称。 运行此报表并选择不同维度，以便了解该报表不依赖所选维度数量或为此实例配置的维度数量。  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]