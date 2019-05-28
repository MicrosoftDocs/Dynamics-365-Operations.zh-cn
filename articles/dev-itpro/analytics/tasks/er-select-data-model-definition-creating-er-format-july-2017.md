---
title: 创建格式时选择数据模型定义
description: 为了完成此过程中的步骤，您必须首先完成“ER 创建配置提供商并标记为有效”这一过程。
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
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
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dc357db8acbdb98741a694a8a9d3c0c0625c50e4
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551081"
---
# <a name="select-data-model-definitions-when-you-create-formats"></a>创建格式时选择数据模型定义

[!include [task guide banner](../../includes/task-guide-banner.md)]

为了完成此过程中的步骤，您必须首先完成“ER 创建配置提供商并标记为有效”这一过程。 

此过程显示如何将模型的根项作为数据模型定义选择，以便插入为生成电子单据而设计的电子申报 (ER) 格式配置。 在此过程中，您将为示例公司 Litware 公司添加一个新的 ER 格式配置。 

此过程针对向其分配了系统管理员角色或电子申报开发人员角色的用户。 可使用任何数据集完成这些步骤。

1. 转到“组织管理”>“工作区”>“电子申报”。
    * 确保示例公司 Litware 公司的配置提供程序可用且标记为“有效”。 如果没有看到此配置提供程序，请首先完成“创建配置提供程序并标记为有效”这一过程中的步骤。  
2. 单击“申报配置”。

## <a name="add-a-new-er-data-model-configuration"></a>添加新 ER 数据模型配置
1. 单击“创建配置”，以打开下拉对话框。
    * 我们新增一个 ER 模型配置，其中包含一个数据模型，设计为用作生成 ER 报表的数据源。  
2. 在“名称”字段中，键入“付款模型（虚构）”。
    * 付款模型（虚构）  
3. 单击“创建配置”。
4. 单击“设计器”。
    * 打开 ER 设计器以指定此配置的数据模型结构。  
    * 假设为付款业务域设计数据模型，以便为贷方转帐和直接借记这两种付款方式提供支持。  
5. 单击“新建”，以打开对话框。
6. 在“名称”字段中，键入“付款 - 贷方转帐”。
    * 付款 - 贷方转帐  
7. 单击“添加”。
8. 单击“新建”，以打开对话框。
9. 在“作为以下项的新节点”字段中，输入“模型根”。
10. 在“名称”字段中，键入“付款 - 直接借记”。
    * 付款 - 直接借记  
11. 单击“添加”。
12. 单击“保存”。
13. 关闭该页面。
14. 单击“更改状态”。
    * 完成模型的草稿版本，以便将其提供给新模型映射和格式。  
15. 单击“完成”。
16. 单击“确定”。

## <a name="start-to-enter-a-new-er-format-configuration"></a>开始输入新 ER 格式配置
1. 单击“创建配置”，以打开下拉对话框。
2. 在“新建”字段中，输入“基于数据模型‘付款模型（虚构）’的格式”。
3. 在“数据模型定义”字段中，输入或选择一个值。
    * 请注意，所选数据模型的所有根项均可作为数据模型定义选择。 可通过使用数据模型的任何所需根项继续设计格式。 缺少所选根项的模型映射不会妨碍您继续操作。  
4. 关闭该页面。

## <a name="add-a-new-er-model-mapping-configuration"></a>添加新 ER 模型映射配置
1. 单击“创建配置”，以打开下拉对话框。
2. 在“新建”字段中，输入“基于数据模型‘付款模型（虚构）’的模型映射”。
3. 在“名称”字段中，键入“付款模型映射（虚构）”。
    * 付款模型映射（虚构）  
4. 在“数据模型定义”字段中，输入或选择一个值。
5. 单击“创建配置”。

## <a name="design-er-model-mappings"></a>设计 ER 模型映射
1. 单击“设计器”。
    * 使用 ER 设计器为所需根项指定模型映射。  
2. 单击“设计器”。
    * 模拟设置所选模型的根项的所选模型映射。  
3. 在树中，选择“Dynamics 365 for Operations\表记录”'。
4. 单击“添加根”。
5. 在“名称”字段中，键入“分类帐”。
6. 在“表格”字段中，键入“分类日记帐交易记录”。
    * 分类日记帐交易记录  
7. 单击“确定”。
8. 单击“保存”。
9. 关闭该页面。
10. 关闭该页面。

## <a name="start-to-enter-another-new-er-format-configuration"></a>开始输入又一个新 ER 格式配置
1. 在树中，选择“付款模型（虚构）”。
2. 单击“创建配置”，以打开下拉对话框。
3. 在“新建”字段中，输入“基于数据模型‘付款模型（虚构）’的格式”。
4. 在“数据模型定义”字段中，输入或选择一个值。
    * 请注意，现在只有一个根项可映射到应用程序数据源。 如果引入了至少一个模型映射，添加 ER 格式时，只能将映射到应用程序数据源的模型根项选择为模型定义。   
5. 关闭该页面。

