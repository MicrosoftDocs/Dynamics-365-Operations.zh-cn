---
title: 准备要在 RCS 中使用的应用程序元数据
description: 本文介绍如何创建包含应用程序元数据的新报告配置。
author: kfend
ms.date: 06/28/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ''
ms.openlocfilehash: a9ccbb120be43eaf7a8ae8b5bf8eaafb4850b199
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289965"
---
# <a name="prepare-application-metadata-to-be-used-in-rcs"></a>准备要在 RCS 中使用的应用程序元数据
[!include [banner](../../includes/banner.md)]

以下步骤演示系统管理员或电子申报开发人员角色的用户如何创建其中包含应用程序元数据的新电子申报 (ER) 配置文件，以便在 Regulatory Configuration Service (RCS) 中设计 ER 模型映射配置。 此配置将用于设计示例 ER 模型映射配置，以便访问外贸交易。 在此示例中，您将创建示例公司 Litware 公司的配置。这些步骤可以在任何公司执行。 为了完成这些步骤，您必须首先完成[创建配置提供程序并标记为当前运行的](er-configuration-provider-mark-it-active-2016-11.md)一文中的步骤。

## <a name="prerequisites"></a>先决条件
1.    转到 **组织管理** > **工作区** > **电子申报**。 
2.    确保示例公司 Litware 公司的配置提供程序可用且标记为 **有效**。 如果没有看到此配置提供程序，请首先完成[创建配置提供程序并标记为当前运行的](er-configuration-provider-mark-it-active-2016-11.md)这一过程中的步骤。 
3.    单击 **元数据配置**。 
4.    假设将使用 RCS 为 Finance and Operations 应用程序设计 ER 解决方案，用于生成其中包含来自外贸业务域的信息的电子单据。 若要 ER 数据模型与所需数据源之间的映射，需要在 RCS 中访问 Finance and Operations 应用程序的元数据。 因此，在 ER 解决方案的设计过程中，将新建一个 ER 元数据配置，其中包含为所选业务域生成 ER 报表当前所需全部元数据。 

## <a name="add-metadata-configuration"></a>添加元数据配置 
1.    单击 **创建配置**，以打开下拉对话框。 
2.    在 **名称** 字段中键入“外贸元数据”。 
3.    单击 **创建配置**。 
4.    单击 **设计器**。 
5.    单击 **添加**。 
  
> [!NOTE]
> 可选择整个应用程序、所选模型或所选模块的所有元数据。 请注意，在此情况下将自动添加以下元数据：记录表、枚举和扩展数据类型。 如果需要更多元数据类型，则必须手动添加。 
 
我们已通过手动选择元数据项获得了一些与外贸交易有关的元数据。 
  
6.    单击 **添加数据源**。 
7.    单击 **表记录**。 
8.    使用“快速筛选器”以筛选一个值为“内部统计”的 **名称** 字段。 
9.    选择 **内部统计** 表记录。 
10.    单击 **确定**。
  
已添加了有关“内部统计”记录表的元数据信息。 
  
11.    在树中，展开 **表记录内部统计**\>**关系**。 
12.    在树中，选择 **表记录内部统计**\>**关系\IntrastatCommodity (表记录 EcoResCategory)**。     
13.    单击 **添加元数据**。 
  
> [!NOTE]
> 必须手动添加有关所选记录表的所需关系的元数据。 
  
16.    单击 **添加数据源**。 
17.    单击 **枚举**。 
18.    使用“快速筛选器”以筛选一个值为“IntrastatDirection”的 **名称** 字段。 
19.    选择 **IntrastatDirection 枚举** 记录。 
20.    单击 **确定**。 
21.    单击 **保存**。  
22.    关闭该页面。 
  
## <a name="complete-the-draft-version-of-metadata-configuration"></a>完成元数据配置的草稿版本
1.    单击 **更改状态**。 
2.    单击 **完成**。 
3.    单击 **确定**。 
4.    选择已完成版本 **1**。 
  
## <a name="export-the-completed-version-of-metadata-configuration-from-application-as-xml-file"></a>将元数据配置的已完成版本作为 XML 文件从应用程序导出
1.    单击 **交换**。 
2.    单击 **导出为 XML 文件**。 
3.    单击 **确定**。 
    
已将创建的 ER 元数据配置保存为 XML 文件，可将此文件导入到 RCS，并用作有关外贸业务域的元数据的信息的来源。 可根据此信息指定应用程序元数据与 ER 数据模型之间的映射。


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
