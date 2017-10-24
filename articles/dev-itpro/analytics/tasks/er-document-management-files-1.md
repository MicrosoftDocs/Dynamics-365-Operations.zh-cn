--- 
title: "针对电子申报 (ER) 为数据模型做好在格式输出中使用票据管理文件的准备"
description: "以下步骤说明指定为系统管理员或电子申报开发人员角色的用户可以如何配置电子申报 (ER) 模型，以便在 ER 输出中使用票据管理文件（附件）。"
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 5d224afd799306828a59e97f7f3bcd4cb831537c
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="prepare-data-model-to-use-document-management-files-in-format-outputs-for-electronic-reporting-er"></a>针对电子申报 (ER) 为数据模型做好在格式输出中使用票据管理文件的准备

[!include[task guide banner](../../includes/task-guide-banner.md)]

以下步骤说明指定为系统管理员或电子申报开发人员角色的用户可以如何配置电子申报 (ER) 模型，以便在 ER 输出中使用票据管理文件（附件）。 这些步骤可以在任何公司执行。

为了完成这些步骤，您必须首先完成“创建配置提供商并标记为有效”这一过程中的步骤。

此过程针对 Dynamics 365 for Operations 版本 1611 中增加的一项功能。


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a>访问 Microsoft 提供的配置列表
1. 转到“组织管理”>“工作区”>“电子申报”。
    * 确保“Litware 公司” 提供程序可用且标记为有效。  
2. 选择“Litware 公司” 提供程序。
3. 单击“存储库”。
    * 如果已存在“运营资源”类型的存储库，请跳过当前子任务的其余步骤。  
4. 单击“添加”以打开下拉对话框。
5. 在“配置存储库类型”字段中，输入“运营资源”。
6. 单击“创建存储库”。
7. 单击“确定”。

## <a name="get-the-customer-invoice-model-configurations-provided-by-microsoft"></a>获取 Microsoft 提供的客户发票模型配置
1. 单击“显示筛选器”。
2. 应用下面的筛选器：在“名称”字段中输入以“开头为”筛选器运算符开始的“运营资源”筛选器值；在“描述”字段中输入以“开头为”筛选器运算符开始的筛选器值
3. 单击“显示筛选器”。
4. 单击“打开”。
5. 在树中，选择“客户发票模型”。
    * 选择模型配置“客户发票模型”将其导入。  
6. 单击“导入”。
    * 单击所选配置版本 1 的“导入”。  
7. 单击“是”。
8. 关闭该页面。
9. 关闭该页面。
10. 单击“申报配置”。
11. 在树中，选择“客户发票模型”。

## <a name="create-the-derived-model-to-support-access-to-the-document-management-files"></a>创建衍生模型以支持访问票据管理文件。
    * 您将创建自己的客户发票模型配置，该配置派生自 Microsoft 提供的配置。 您将使用此配置实施对票据管理文件的访问，并将其提供给您将基于此模型创建的电子票据。  
1. 单击“创建配置”，以打开下拉对话框。
2. 在"新建"字段中，输入“从以下名称派生：客户发票模型，Microsoft”。
3. 在“名称”字段中，键入“客户发票模型（自定义）”。
    * 客户发票模型（自定义）  
4. 单击“创建配置”。


