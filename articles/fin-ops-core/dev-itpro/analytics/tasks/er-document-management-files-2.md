---
title: ER 在格式输出中使用票据管理文件（第 2 部分 - 扩展数据模型）
description: 本主题介绍如何配置电子报告 (ER) 格式以在 ER 输出中使用文档管理文件（附件）。 （第 2 部分）
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1e79dd0a6c68aa6ba7b857c31c9159c68543d93b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754906"
---
# <a name="er-use-document-management-files-in-format-outputs-part-2---extend-data-model"></a>ER 在格式输出中使用票据管理文件（第 2 部分 - 扩展数据模型）

[!include [banner](../../includes/banner.md)]

以下步骤说明指定为系统管理员或电子申报开发人员角色的用户可以如何配置电子申报 (ER) 模型，以便在 ER 输出中使用票据管理文件（附件）。 这些步骤可以在任何公司执行。

若要完成这些步骤，必须首先完成“ER 在格式输出中使用票据管理文件（第 1 部分：准备数据模型）”任务指南中的步骤。

此过程针对 Dynamics 365 for Operations 版本 1611 中增加的一项功能。


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a>展开数据模型以在其中显示票据管理文件
1. 转到“组织管理”>“工作区”>“电子申报”。
2. 单击“申报配置”。
3. 在树中，展开“客户发票模型”。
4. 在树中，选择“客户发票模型\客户发票模型(自定义)”。
5. 单击“设计器”。
6. 在树中，选择“客户发票(InvoiceCustomer)”。
    * 您将扩展此数据模型以在其中显示已附加到与电子方式处理的发票有关的销售订单的任何文件。  
7. 单击“新建”，以打开对话框。
8. 在“名称”字段中，键入“发票附件”。
    * 发票附件  
9. 在“物料类型”字段中，选择“记录列表”。
10. 单击“添加”。
11. 单击“新建”，以打开对话框。
12. 在“名称”字段中，键入“文件内容”。
    * 文件内容  
13. 在“物料类型”字段中，选择“集装箱”。
14. 单击“添加”。
15. 单击“新建”，以打开对话框。
16. 在“名称”字段中，键入“文件名”。
    * 文件名  
17. 在“物料类型”字段中，选择“字符串”。
18. 单击“添加”。

## <a name="map-new-data-model-elements-to-data-sources"></a>将新数据模型元素映射到数据源
1. 单击“映射模型到数据源”。
2. 使用快速筛选来筛选值为“InvoiceCustomer”的“定义”字段。
    * InvoiceCustomer  
    * 我们将把新模型元素映射到相应数据源。  
3. 单击“设计器”。
4. 在树中，选择“发票附件”。
5. 在树中，展开“发票附件”。
6. 在树中，选择“发票附件\文件名”。
7. 单击“编辑”。
8. 在“公式”字段中，输入“CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'”。
    * CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'  
9. 单击“保存”。
10. 关闭该页面。
11. 在树中，选择“发票附件\文件内容”。
12. 单击“编辑”。
13. 在“公式”字段中，输入“CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'”。
    * CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'  
14. 单击“保存”。
15. 关闭该页面。
16. 在树中，选择“发票附件”。
17. 单击“编辑”。
18. 在“公式”字段中，输入“CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'”。
    * CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'  
19. 单击“保存”。
20. 关闭该页面。
21. 单击“保存”。
22. 关闭该页面。
23. 关闭该页面。
24. 关闭该页面。
25. 单击“更改状态”。
26. 单击“完成”。
27. 单击“确定”。



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]