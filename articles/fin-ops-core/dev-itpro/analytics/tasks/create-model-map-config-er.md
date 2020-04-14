---
title: 创建电子申报 (ER) 模型映射配置
description: 此过程用于设计新电子申报 (ER) 模型映射配置和使用内置 ER 执行有效聚合计算的信息。
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c6ba23af5f7eb517cc58994e54e918b2a305da17
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142148"
---
# <a name="create-electronic-reporting-er-model-mapping-configurations"></a>创建电子申报 (ER) 模型映射配置

[!include [banner](../../includes/banner.md)]

此过程用于设计新电子申报 (ER) 模型映射配置和使用内置 ER 执行有效聚合计算的信息。 在此过程中，您将创建示例公司“Litware 公司”的配置。 

此过程是为向其分配了系统管理员角色或电子申报开发人员角色的用户创建的。

可使用任何数据集完成这些步骤。 为了完成这些步骤，您必须首先完成“创建配置提供商并标记为有效”这一过程中的步骤。

1. 转到“组织管理”>“工作区”>“电子申报”。
    * 确保示例公司 Litware 公司的配置提供程序可用且标记为“有效”。 如果没有看到此配置提供程序，请首先完成“创建配置提供程序并标记为有效”这一过程中的步骤。  
2. 单击“申报配置”。
3. 单击“显示筛选器”。
4. 在“名称”字段中输入筛选器值、“内部统计”并使用筛选器运算符“begins with”。
    * 应用此筛选器来查找“内部统计”数据模型配置。 此模型可能已在配置树中存在。 如果存在，请跳过下一个子任务。   

## <a name="get-the-intrastat-model-configuration-provided-by-microsoft"></a>获取 Microsoft 提供的内部统计模型配置
1. 关闭该页面。
2. 关闭该页面。
3. 转到“组织管理”>“工作区”>“电子申报”。
4. 在列表中，找到并选择所需记录。
    * 选择 Microsoft 提供程序磁贴。  
5. 单击“存储库”。
    * 单击 Microsoft 提供程序磁贴上的“存储库”。  
6. 单击“显示筛选器”。
7. 在“类型名称”字段中输入筛选器值、“资源”并使用筛选器运算符“contains”。 
8. 单击“打开”。
9. 在树中，选择“内部统计模型”。
10. 单击“导入”。
11. 单击“是”。
    * 您导入了包含您将用于探索新 ER 功能如何使用的数据模型的 ER 模型配置。  
12. 关闭该页面。
13. 关闭该页面。
14. 单击“申报配置”。

## <a name="add-a-new-model-mapping-configuration"></a>添加新模型映射配置
1. 在树中，选择“内部统计模型”。
2. 单击“创建配置”，以打开下拉对话框。
3. 在“新建”字段中，输入“基于数据模型内部统计的模型映射”。
4. 在“名称”字段中，键入“内部统计示例映射”。
    * 内部统计示例映射  
5. 单击“创建配置”。

