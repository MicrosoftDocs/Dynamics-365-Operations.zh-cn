---
title: ER 上载配置到 Lifecycle Services
description: 以下步骤说明属于系统管理员或电子报表开发人员用户如何创建新电子申报 (ER) 配置并将其上载到 Microsoft Lifecycle Services (LCS)。
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 19ae8820e5d4a798a5789e9632edb431fe9fede4
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "335086"
---
# <a name="er-upload-a-configuration-into-lifecycle-services"></a>ER 上载配置到 Lifecycle Services

[!include [task guide banner](../../includes/task-guide-banner.md)]

以下步骤说明属于系统管理员或电子报表开发人员用户如何创建新电子申报 (ER) 配置并将其上载到 Microsoft Lifecycle Services (LCS)。

此示例以示例公司 Litware，Inc. 为例，您将创建一个配置提供程序并将其上载到 LCS。这些步骤可在任何公司执行，因为公司之间共享 ER 配置。 为了完成这些步骤，您必须首先完成“创建配置提供商并标记为有效”这一过程中的步骤。 完成这些步骤还需要能够访问 LCS。

1. 转到“组织管理”>“工作区”>“电子申报”。
2. 选择“Litware 公司” 并设置为活动状态。
3. 单击“配置”。

## <a name="create-a-new-data-model-configuration"></a>创建新的数据模型配置
1. 单击“创建配置”，以打开下拉对话框。
    * 您将创建含有电子单据的示例数据模型的配置。 此数据模型配置稍后将上载到 LCS。  
2. 在“名称”字段中，键入“示例模型配置”。
    * 示例模型配置  
3. 在“描述”字段中，键入“示例模型配置”。
    * 示例模型配置  
4. 单击“创建配置”。
5. 单击“模型设计器”。
6. 单击“新建”。
7. 在“名称”字段中，键入“入口点”。
    * 入口点  
8. 单击“添加”。
9. 单击“保存”。
10. 关闭该页面。
11. 单击“更改状态”。
12. 单击“完成”。
13. 单击“确定”。

## <a name="register-a-new--repository"></a>登记新存储库
1. 关闭该页面。
2. 单击“存储库”。
    * 这使您打开 Litware, Inc 配置提供程序的 存储库列表。  
3. 单击“添加”以打开下拉对话框。
    * 这允许您添加新的存储库。  
4. 在“配置存储库类型”字段中，选择 LCS。
5. 单击“创建存储库”。
6. 在“项目”字段中，输入或选择一个值。
    * 选择所需的 LCS 项目。 您必须有权访问该项目。  
7. 单击“确定”。
    * 完成新的存储库输入。  
8. 在列表中，标记所选的行。
    * 选择 LCS 存储库记录。  
    * 请注意，登记的存储库由当前提供程序标记，这意味着该提供程序拥有的唯一配置可放置到此存储库中，因此，可上载到所选 LCS 项目。  
9. 单击“打开”。
    * 打开存储库查看 ER 配置列表。 如果此项目没有用于 ER 配置共享，其将为空。  
10. 关闭该页面。
11. 关闭该页面。

## <a name="upload-configuration-into-lcs"></a>上载配置到 LCS
1. 单击“配置”。
2. 在树结构中，选择“示例模型配置”。
    * 选择已完成的创建的配置。  
3. 在列表中，找到并选择所需记录。
    * 选择状态为“已完成”的所选配置的版本。  
4. 单击“更改状态”。
5. 单击“共享”。
    * 当在 LCS 中发布时，配置状态将从“已完成”更改为“已共享”。  
6. 单击“确定”。
7. 在列表中，找到并选择所需记录。
    * 选择状态为“已共享”的配置版本。  
    * 请注意，所选版本的状态已从“已完成”更改为“已共享”。  
8. 关闭该页面。
9. 单击“存储库”。
    * 这使您打开 Litware, Inc 配置提供程序的 存储库列表。  
10. 单击“打开”。
    * 选择 LCS 存储库然后打开它。  
    * 请注意，所选配置显示为所选 LCS 项目的资产。  
    * 使用 https://lcs.dynamics.com 打开 LCS。 打开之前用于存储库登记的项目，打开此项目的“资产库”，然后展开“GER 配置”资产类型 – 上载的的 ER 配置将可用。 请注意，如果提供程序有权访问此 LCS 项目，上载的 LCS 配置可以导入到其他 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 实例。  

