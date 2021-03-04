---
title: ER 在格式输出中使用票据管理文件（第 5 部分 - 修改和运行格式）
description: 以下步骤说明指定为系统管理员或电子申报开发人员角色的用户可以如何配置电子申报 (ER) 模型，以便在 ER 输出中使用票据管理文件（附件）。
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERComponentTypeDropDialog, ERExpressionDesignerFormula, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8b949c2629df0e9db8c11322c9d0d090b200edc2
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681749"
---
# <a name="er-use-document-management-files-in-format-outputs-part-5---modify-and-run-format"></a>ER 在格式输出中使用票据管理文件（第 5 部分 - 修改和运行格式）

[!include [banner](../../includes/banner.md)]

以下步骤说明指定为系统管理员或电子申报开发人员角色的用户可以如何配置电子申报 (ER) 模型，以便在 ER 输出中使用票据管理文件（附件）。 这些步骤可以在 DEMF 公司执行。

若要完成这些步骤，必须首先完成“ER 在格式输出中使用票据管理文件（第 4 部分：运行格式）”过程中的步骤。

此过程针对 Dynamics 365 for Operations 版本 1611 中增加的一项功能。


## <a name="modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format"></a>修改格式以将附件填充到生成的二进制格式的消息中
1. 转到“组织管理”>“电子申报”>“配置”。
2. 在树中，展开“客户发票模型”。
3. 在树中，展开“客户发票模型\客户发票模型(自定义)”。
4. 在树中，选择“客户发票模型\客户发票模型(自定义)\电子发票示例消息”。
5. 单击“设计器”。
    * 您将使用 UNICODE 编码在生成的格式为 XML 文件的输出中填充发票消息。  
6. 单击“添加根”以打开下拉对话框。
7. 在树结构中，选择“常见\文件”。
8. 在“名称”字段中，键入“Xml 消息”。
    * Xml 消息  
9. 在“编码”字段中，键入“UTF-8”。
    * UTF-8  
10. 单击“确定”。
    * 将生成的输出配置为压缩文件。  
11. 单击“添加根”以打开下拉对话框。
12. 在树中，选择“常见\文件夹”。
13. 在“名称”字段中，键入“压缩输出”。
    * 压缩输出  
14. 单击“确定”。
15. 在树中，选择“压缩输出”。
    * 将附件作为采用原始名称和扩展名的文件添加到生成的压缩文件中。  
16. 单击“添加”以打开下拉对话框。
17. 在树结构中，选择“常见\文件”。
18. 在“名称”字段中，键入“附加文件”。
    * 附加文件  
19. 单击“确定”。
20. 在树中，选择“压缩输出\附加文件”。
21. 单击“添加”以打开下拉对话框。
22. 在树中，选择“文本\Base64”。
23. 单击“确定”。

## <a name="map-new-format-elements-to-data-model"></a>将新格式元素映射到数据模型
1. 单击“映射”选项卡。
2. 在树结构中，展开“模型”。
3. 在树中，展开“模型\发票附件”。
4. 在树中，选择“压缩输出\附加文件\Base64”。
5. 在树中，选择“模型\发票附件\文件内容”。
6. 单击“绑定”。
7. 在树中，选择“压缩输出\附加文件”。
8. 单击“编辑文件名”。
9. 在树中，展开“模型”。
10. 在树中，展开“模型\发票附件”。
11. 在树中，选择“模型\发票附件\文件名”。
12. 单击“添加数据源”。
13. 单击“保存”。
14. 关闭该页面。
15. 在树中，选择“模型\发票附件”。
16. 单击“绑定”。
17. 单击“保存”。
18. 关闭该页面。

## <a name="run-the-designed-report-for-the-selected-invoice"></a>运行为所选发票设计的报表
1. 单击“运行”。
2. 展开“要包括的记录”部分。
3. 单击“筛选器”。
4. 选择“客户发票日记帐”的行和“销售订单”字段。
5. 在"条件"字段中，在条件的“销售订单”字段中，键入订单编号 000148。
    * 000148  
6. 单击“确定”。
7. 单击“确定”。
    * 检查生成的输出。 请注意，除了 XML 格式的发票，还为每个附件创建了一个文件。 附件文件使用二进制格式的压缩输出填充。  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]