---
title: 修改职位的报告关系
description: 该过程展示如何更改员工的报告关系。
author: andreabichsel
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HcmPosition, HcmPositionReportsToDialog, HcmPositionLookup, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 78410347e7e6cf67f692c7e9193419ffd87e3057
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/18/2021
ms.locfileid: "6057084"
---
# <a name="modify-reporting-relationships-for-a-position"></a>修改职位的报告关系

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



该过程展示如何更改员工的报告关系。 该报告关系可以通过工作流用于路线选择文件。 该过程同时也说明了如何分配给该员工附加的层次结构。 例如，一个员工作为某项目组的成员，与项目主管是非正式报告关系。 通过职位定义附加的报告关系可以用于调节各种项目或者矩阵方案。 创建此程序的演示数据公司是 USMF。

1. 转到“人力资源”>“职位”>“职位”。
2. 使用“快速筛选器”以查找记录。 例如，在“职位”字段中用值“000091”进行筛选。
3. 在列表中，单击所选行中的链接。
4. 展开“职位报告”部分。
5. 单击“新建”，以打开对话框。
6. 在“报告”字段中，输入或选择一个值。
7. 单击“创建”。
8. 展开“关系”部分。
9. 单击“添加”。
10. 选择表格左侧的复选框。
11. 在“层次结构名称”字段中，输入或选择一个值。
    * 示例：项目  
12. 在“直接上级职位”字段中，输入或选择一个值。  示例：000437
13. 单击“保存”。



[!INCLUDE[footer-include](../includes/footer-banner.md)]