---
title: 更改多项固定资产的折旧惯例
description: 此任务更新特定固定资产组的折旧惯例。
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysQueryForm, SrsReportViewerForm
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 21baf3692cbcb87f6ed37459848376a1fa87a438
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840065"
---
# <a name="change-depreciation-conventions-for-multiple-fixed-assets"></a>更改多项固定资产的折旧惯例

[!include [task guide banner](../../includes/task-guide-banner.md)]

此任务更新特定固定资产组的折旧惯例。 此任务指南使用 USMF 公司演示。

1. 转到“固定资产”>“定期任务”>“成批更新”
2. 在“折旧帐簿”字段中，单击下拉按钮以打开查找。
3. 在列表中，单击所选行中的链接。
4. 在“开始投入使用”字段，输入日期。
5. 在“投入使用结束”字段，输入日期。
    * 仅所选折旧帐簿中的且在该等日期之间投入使用的资产才会更新。  
6. 在“当前折旧惯例”字段中，选择一个选项。
    * 仅属于当前折旧惯例的资产才会更新。  
7. 在“新折旧惯例”字段中，选择一个选项。
    * 验证报表将打印给所选目标。  
8. 扩展“要包括的记录”部分。
9. 单击“筛选器”。
10. 在列表中选择固定资产组。
11. 在“标准”字段中，单击下拉按钮以打开查找。
12. 选择期望的固定资产组。
13. 在列表中，单击所选行中的链接。
14. 单击“确定”。
15. 单击“确定”。
    *  流程结果将在成批更新报表中显示。     

