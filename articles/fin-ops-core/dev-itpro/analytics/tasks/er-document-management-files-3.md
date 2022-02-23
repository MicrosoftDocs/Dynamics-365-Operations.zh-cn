---
title: ER 在格式输出中使用票据管理文件（第 3 部分 - 创建格式）
description: 以下步骤说明指定为系统管理员或电子申报开发人员角色的用户可以如何配置电子申报模型，以便在 ER 输出中使用票据管理文件。
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bfcc03fa7470d4f2fa45ef012e30acef0712bf99
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681845"
---
# <a name="er-use-document-management-files-in-format-outputs-part-3---create-format"></a>ER 在格式输出中使用票据管理文件（第 3 部分 - 创建格式）

[!include [banner](../../includes/banner.md)]

以下步骤说明指定为系统管理员或电子申报开发人员角色的用户可以如何配置电子申报 (ER) 模型，以便在 ER 输出中使用票据管理文件（附件）。 这些步骤可以在任何公司执行。

若要完成这些步骤，必须首先完成“ER 在格式输出中使用票据管理文件（第 2 部分：扩展数据模型）”过程中的步骤。

此过程针对 Dynamics 365 for Operations 版本 1611 中增加的一项功能。


## <a name="create-a-format-to-process-invoices"></a>创建用于处理发票的格式
1. 转到“组织管理”>“工作区”>“电子申报”。
2. 单击“申报配置”。
3. 在树中，展开“客户发票模型”。
4. 在树中，选择“客户发票模型\客户发票模型(自定义)”。
    * 您将创建格式，以便使用有关已附加到与以电子方式处理发票的销售订单的任何文件有关的信息生成电子消息。  
5. 单击“创建配置”，以打开下拉对话框。
6. 在“新建”字段中，输入“格式基于数据模型客户发票模型（自定义）”。
7. 在“名称”字段中，键入“电子发票示例消息”。
    * 电子发票示例消息  
8. 在“数据模型定义”字段中，输入或选择一个值。
    * InvoiceCustomer  
9. 单击“创建配置”。

## <a name="design-a-format-to-populate-attachments-into-generating-a-message-in-mime-format"></a>设计格式以将附件填充到生成的 MIME 格式的消息中
1. 单击“设计器”。
2. 单击“添加根”以打开下拉对话框。
3. 在树结构中，选择“XML\元素”。
4. 在“名称”字段中，键入“发票”。
    * 开票  
5. 单击“确定”。
6. 单击“添加”以打开下拉对话框。
7. 在树结构中，选择“Xml：文件\属性”。
8. 在“名称”字段中，键入“SalesOrder”。
    * SalesOrder  
9. 单击“确定”。
10. 单击“添加属性”。
11. 在“名称”字段中，键入“InvoiceNumber”。
    * InvoiceNumber  
12. 单击“确定”。
13. 单击“添加属性”。
14. 在“名称”字段中，键入“InvoiceAmount”。
    * InvoiceAmount  
15. 单击“确定”。
16. 单击“添加”以打开下拉对话框。
17. 在树结构中，选择“XML\元素”。
18. 在“名称”字段中，键入“EnclosedDocs”。
    * EnclosedDocs  
19. 单击“确定”。
20. 在树中，选择“发票\EnclosedDocs”。
21. 单击“添加元素”。
22. 在“名称”字段中，键入“票据”。
    * 原始凭证  
23. 单击“确定”。
24. 在树中，选择“发票\EnclosedDocs\票据”。
25. 单击“添加”以打开下拉对话框。
26. 在树结构中，选择“Xml：文件\属性”。
27. 在“名称”字段中，键入“FileName”。
    * FileName  
28. 单击“确定”。
29. 单击“添加”以打开下拉对话框。
30. 在树结构中，选择“XML\元素”。
31. 在“名称”字段中，键入“FileContent”。
    * FileContent  
32. 单击“确定”。
33. 在树中，选择“发票\EnclosedDocs\票据\FileContent”。
34. 单击“添加”以打开下拉对话框。
35. 在树中，选择“文本\Base64”。
36. 单击“确定”。

## <a name="map-format-elements-to-data-model-as-data-source"></a>将格式元素映射到数据模型充当数据源
1. 在树中，选择“发票\SalesOrder”。
2. 单击“映射”选项卡。
3. 在树中，展开“模型”。
4. 在树中，选择“模型\销售订单编号(SalesId)”。
5. 单击“绑定”。
6. 在树中，选择“发票\InvoiceNumber”。
7. 在树中，展开“模型\基础发票(InvoiceBase)”。
8. 在树中，选择“模型\基础发票(InvoiceBase)\发票编号(Id)”。
9. 单击“绑定”。
10. 在树中，选择“发票\InvoiceAmount”。
11. 在树中，选择“模型\基础发票(InvoiceBase)\发票金额(Amount)”。
12. 单击“绑定”。
13. 在树中，展开“模型\发票附件”。
14. 在树中，选择“模型\发票附件\文件内容”。
15. 在树中，选择“发票\EnclosedDocs\票据\FileContent\Base64”。
16. 单击“绑定”。
17. 在树中，选择“模型\发票附件\文件名”。
18. 在树中，选择“发票\EnclosedDocs\票据\FileName”。
19. 单击“绑定”。
20. 在树中，选择“模型\发票附件”。
21. 在树中，选择“发票\EnclosedDocs\票据”。
22. 单击“绑定”。
23. 单击“保存”。
24. 关闭该页面。

