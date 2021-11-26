---
title: 修改职位的报告关系
description: 该过程展示如何更改员工的报告关系。
author: twheeloc
ms.date: 10/28/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HcmPosition, HcmPositionReportsToDialog, HcmPositionLookup, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: db15394bf4bcd1b56781d269ad81aa1ad20b5e69
ms.sourcegitcommit: e91a1797192fd9bc4048b445bb5c1ad5d333d87d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/01/2021
ms.locfileid: "7728801"
---
# <a name="modify-reporting-relationships-for-a-position"></a>修改职位的报告关系

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



该过程展示如何更改员工的报告关系。 该报告关系可以通过工作流用于路线选择文件。 该过程同时也说明了如何分配给该员工附加的层次结构。 例如，一个员工作为某项目组的成员，与项目主管是非正式报告关系。 通过职位定义附加的报告关系可以用于调节各种项目或者矩阵方案。 创建此程序的演示数据公司是 USMF。

1. 转到 **人力资源** \> **职位** \> **职位**。
2. 使用“快速筛选器”以查找记录。 例如，对 **职位** 字段使用值 **000091** 进行筛选。
3. 在列表中，选择所选择行中的链接。
4. 展开 **直接上级职位** 部分。
5. 选择 **新建** 打开下拉对话框。
6. 在 **直接上级** 字段中，输入或选择一个值。
7. 选择 **创建**。
8. 展开 **关系** 部分。
9. 选择 **添加**。
10. 选择表格左侧的复选框。
11. 在 **层次结构名称** 字段中，输入或选择一个值（例如，**项目**）。
12. 在 **直接上级职位** 字段中，输入或选择一个值（例如，**000437**）。
13. 选择 **保存**。



[!INCLUDE[footer-include](../includes/footer-banner.md)]
