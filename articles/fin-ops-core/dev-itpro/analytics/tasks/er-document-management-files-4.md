---
title: 运行在 ER 输出中使用票据管理文件的格式
description: 以下步骤说明指定为系统管理员或电子申报开发人员角色的用户可以如何配置电子申报模型，以便在 ER 输出中使用票据管理文件。
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustOpenInvoicesListPage, CustInvoiceJournal, SalesTable, ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d8dc541af4d26b61ff9b90e08a8ca2c6a6bb8e70
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185006"
---
# <a name="er-use-document-management-files-in-format-outputs-part-4-run-format"></a>ER 在格式输出中使用票据管理文件（第 4 部分：运行格式）

[!include [task guide banner](../../includes/task-guide-banner.md)]

以下步骤说明指定为系统管理员或电子申报开发人员角色的用户可以如何配置电子申报 (ER) 模型，以便在 ER 输出中使用票据管理文件（附件）。 这些步骤可以在 DEMF 公司执行。

若要完成这些步骤，必须首先完成“ER 在格式输出中使用票据管理文件（第 3 部分：创建格式）”过程中的步骤。

此过程针对 Dynamics 365 for Operations 版本 1611 中增加的一项功能。


## <a name="add-necessary-attachments-for-sales-order-of-a-single-invoice"></a>添加单张发票的销售订单的必要附件
1. 转至“应收账款”>“发票”>“未结客户发票”。
2. 使用“快速筛选器”以查找记录。 例如，在“发票”字段中用值“CIV-000148”进行筛选。
    * CIV-000148  
3. 单击以访问所选发票的链接。
    * CIV-000148  
4. 单击以访问“销售订单”字段中的链接。
    * 000148  
5. 在“行或标题”字段中，选择“标题”选项。
    * 选择“标题”以表示这将是添加附件的目标。  
6. 单击“附加”。
    * 将一些文件添加为此销售订单的附件。 使用票据管理支持的票据类型的文件（文件扩展名为 DOCX、DPF、XML、JPG 等）。 浏览并选择要附加并使用 ER 电子消息中的相关发票进一步处理的文件。  
7. 单击“新建”。
8. 单击“文件”。
9. 单击“新建”。
10. 单击“文件”。
11. 关闭该页面。
12. 关闭该页面。
13. 关闭该页面。
14. 关闭该页面。

## <a name="run-the-designed-report-for-the-selected-invoice"></a>运行为所选发票设计的报表
1. 转到“组织管理”>“电子申报”>“配置”。
2. 在树中，展开“客户发票模型”。
3. 在树中，展开“客户发票模型\客户发票模型(自定义)”。
4. 在树中，选择“客户发票模型\客户发票模型(自定义)\电子发票示例消息”。
5. 单击“运行”。
6. 展开“要包括的记录”部分。
7. 单击“筛选器”。
8. 选择“客户发票日记帐”的行和“销售订单”字段。
9. 在“标准”字段中，键入“000148”。
    * 在条件的“销售订单”字段中，键入订单编号 000148。  
10. 单击“确定”。
11. 单击“确定”。
    * 检查生成的输出。 请注意，已经为每个附件创建了一个 XML 节点。 附件的内容填充到 MIME (base64) 文本格式的 XML 输出中。  

