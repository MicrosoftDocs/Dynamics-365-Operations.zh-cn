--- 
title: "设置折旧帐簿"
description: "此任务指南将创建新的折旧帐簿并将其与固定资产组关联。"
author: saraschi2
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: d06d5f92e91e33dc752bf45ab890c37dfea3888d
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-depreciation-books"></a>设置折旧帐簿 

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

此任务指南将创建新的折旧帐簿并将其与固定资产组关联。  它为 USMF 法人实体使用会计角色和演示数据。


## <a name="create-a-depreciation-book"></a>创建折旧帐簿
1. 转到“固定资产”>“设置”>“折旧帐簿”。
2. 单击“新建”。
3. 在“折旧帐簿”字段中，键入一个值。
4. 在“描述”字段中，键入一个值。
5. 选中或取消选中“计算折旧”复选框。
6. 在“折旧模板”字段中，单击下拉按钮以打开查找。
7. 在列表中，查找并选择所需折旧模板。
8. 在列表中，单击所选行中的链接。
9. 在“备选折旧模板”字段中，单击下拉按钮以打开查找。
10. 在列表中，选择所需折旧模板。
11. 在列表中，单击所选行中的链接。
    * 异常折旧模板用于异常情况下资产的额外折旧。 例如，您可以使用此来记录自然灾害导致的折旧。  
12. 选中或取消选中“使用基本调整创建折旧调整”复选框。
13. 在“日历”字段中，单击下拉按钮以打开查找。
14. 在列表中，单击所选行中的链接。

## <a name="associate-the-depreciation-book-with-a-fixed-asset-group"></a>将折旧帐簿与固定资产组关联
1. 单击“固定资产组”。
2. 在“固定资产组”字段中，单击下拉按钮以打开查找。
3. 在列表中，找到并选择所需记录。
4. 在列表中，单击所选行中的链接。
5. 在“折旧惯例”字段中，选择一个选项。
6. 在“使用年限”字段中，输入一个数字。
    * 请注意，“折旧期间”字段值将在设置使用年限后计算。  


