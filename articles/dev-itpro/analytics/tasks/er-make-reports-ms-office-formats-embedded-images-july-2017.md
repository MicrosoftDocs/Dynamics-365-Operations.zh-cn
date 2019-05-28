---
title: 设计配置以生成 Office 格式的包含嵌入图像的报表
description: 本主题中的步骤提供有关如何设计电子申报 (ER) 配置，以便生成 Microsoft Office 格式（Excel 和 Word）且包含嵌入图像的电子单据的信息。
author: NickSelin
manager: AnnBe
ms.date: 01/23/2018
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
ms.openlocfilehash: 1fb02e561f6792c57b924ba64a5ca3d3974289ee
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544395"
---
# <a name="design-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a>设计配置以生成 Office 格式的包含嵌入图像的报表

[!include [task guide banner](../../includes/task-guide-banner.md)]

为了完成此过程中的步骤，首先完成“ER 创建配置提供商并标记为有效”这一过程。 此过程介绍如何设计电子申报 (ER) 配置，以便生成包含嵌入图像的 Microsoft Excel 或 Word 文档。 在此过程中，将为示例公司 Litware, Inc. 创建所需 ER 配置。可使用 USMF 数据集完成这些步骤。 此过程是为向其分配了系统管理员角色或电子申报开发人员角色的用户创建的。 首先，下载并保存“帮助”主题[业务文档中使用电子申报工具生成的嵌入图像和形状](../electronic-reporting-embed-images-shapes.md)中列举的文件。 这些文件是：Model for cheques.xml、Cheques printing format.xml、Company logo.png、Signature image.png、Signature image 2.png 和 Cheque template Word.docx。

## <a name="verify-prerequisites"></a>验证先决条件  
 1. 转到“组织管理”>“工作区”>“电子申报”。  
 2. 确保示例公司 Litware 公司的配置提供程序可用且标记为“有效”。 如果没有看到此配置提供程序，请首先完成“创建配置提供程序并标记为有效”这一过程中的步骤。   
 3. 单击“申报配置”。  
 
## <a name="add-a-new-er-model-configuration"></a>添加新 ER 模型配置  
 1. 不是创建新模型，您可以加载之前保存的 ER 模型配置文件 (Model for cheques.xml)。 此文件包含付款支票的示例数据模型和数据模型到 Dynamics 365 for Operations 应用程序的数据组件的映射。   
 2. 在“版本”快速选项卡上，单击“交换”。   
 3. 单击“从 XML 文件加载”。  
 4. 单击“浏览”，然后选择 Model for cheques.xml。   
 5. 单击“确定”。  
 6. 加载的模块将用作生成在 Excel 和 Word 中包含图像的文档的信息数据源。  

## <a name="add-a-new-er-format-configuration"></a>添加新 ER 格式配置  
 1. 不是创建新格式，您可以加载之前保存的 ER 格式配置文件 (Cheques printing format.xml)。 此文件包含使用预打印表打印支票的格式的示例布局以及此格式到“支票模型”数据模型的映射。   
 2. 单击“交换”。  
 3. 单击“从 XML 文件加载”。  
 4. 单击“浏览”并选择 Cheques printing format.xml 文件。   
 5. 单击“确定”。  
 6. 在树中，展开“支票的模型”。  
 7. 在树中，展开“支票的模型\支票打印格式“。  
 8. 加载的格式将用于生成在 Excel 和 Word 中包含图像的文档。   

## <a name="configure-er-user-parameters"></a>配置 ER 用户参数  
 1. 在操作窗格上，单击“配置”。  
 2. 单击“用户参数”。  
 3. 在“运行设置”字段中选择“是”。  
  打开“运行草稿”标志以启动所选格式的草稿版（而不是已完成格式）。  
 4. 单击“确定”。  

## <a name="configure-cash--bank-management-parameters"></a>配置现金和银行管理参数  
 1. 转至“现金和银行管理”>“银行帐户”>“银行帐户”。  
 2. 使用“快速筛选器”以筛选含有 'USMF OPER' 值的“银行帐户”。  
 3. 单击“操作窗格”上的“设置”。  
 4. 单击“确认”。  
 5. 展开“设置”部分。  
 6. 单击“编辑”。  
 7. 在“公司徽标”字段中，选择“是”。  
 8. 单击“公司徽标”。  
 9. 单击“更改”。  
 10. 单击“浏览”并选择您之前下载的文件 Company logo.png。   
 11. 单击“保存”。  
 12. 关闭该页面。  
 13. 展开“签名”部分。  
 14. 在“打印第一个签名”字段中选择“是”。  
 15. 单击“更改”。  
 16. 单击“浏览”并选择您之前下载的文件 Signature image.png。   
 17. 展开“份数”部分。  
 18. 在“水印”字段中，选择一个选项。  
 19. 在“普通电子导出格式”字段中，选择“是”。  
 20. 选择“支票打印格式”配置。  
 21. 现在所选的 ER 格式将用于打印支票。  
 22. 单击“附加”。  
 23. 单击“新建”。  
 24. 单击“文件”。  
 25. 单击“浏览”并选择您之前下载的文件 Signature image 2.png。   
 26. 关闭该页面。  
 27. 关闭该页面。  
 28. 关闭该页面。  
 29. 转到“现金和银行管理”>“设置”>“现金和管理银行参数”。  
 30. 在“允许在无效银行帐户上进行预验证创建:”字段中选择“是”。  
 31. 单击“保存”。  
 32. 关闭该页面。  
