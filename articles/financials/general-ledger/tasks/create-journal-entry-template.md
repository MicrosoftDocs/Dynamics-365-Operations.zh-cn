--- 
title: "使用模板创建日记帐条目"
description: "已过帐的日记帐凭证可以保存为凭证模板并应用到新日记帐凭证中。"
author: aprilolson
manager: AnnBe
ms.date: 02/17/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 055fe129b9fc9cf50e1d9e1a5b4cb77285f20c92
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-journal-entry-using-a-template"></a>使用模板创建日记帐条目

[!include[task guide banner](../../includes/task-guide-banner.md)]

已过帐的日记帐凭证可以保存为凭证模板并应用到新日记帐凭证中。 该程序适用于 USMF 演示公司。

1. ”总帐“>”日记帐分录“>”普通日记帐“。 单击“新建”。
    * 此程序开始时需要创建和过帐日记帐凭证，但所有以前已过帐的日记帐凭证可以保存为模板。  
2. 在“名称”字段中，单击下拉按钮以打开查找。
3. 在列表中，找到并选择所需记录。
4. 在列表中，单击所选行中的链接。
5. 单击“行”。
6. 为帐户类型输入一个帐户。
7. 在“描述”字段中，键入一个值。
8. 在“借项”字段中，输入一个金额。
9. 单击“新建”。
10. 为帐户类型输入一个不同的帐户。
11. 在“描述”字段中，键入一个值。
12. 在“借项”字段中，输入一个金额。
13. 单击“新建”。
14. 在“帐户”字段中，指定所需值。
15. 在“描述”字段中，键入一个值。
16. 在“贷项”字段中输入一个金额以使凭证试算平衡。
17. 单击“过帐”。
18. 单击“功能”。
19. 单击“保存凭证模板”。
20. 此程序使用百分比模板类型。 单击“确定”。
    * •百分比：凭证中的金额会被转换为百分比系数，当选择了凭证模板时，这允许应用任何金额。  •金额：将存储和应用实际金额。  
21. 单击“普通日记帐”。
22. 单击“新建”。
23. 在“名称”字段中，单击下拉按钮以打开查找。
24. 在列表中，单击所选行中的链接。
25. 单击“行”。
26. 单击“功能”。
27. 单击“选择凭证模板”。
28. 查找您之前创建的模板。 单击“确定”。
    * 如果存在其它模板，您可能需要单击“上一步”，然后选择正确的模板。  
29. 在“金额”字段中，输入要应用于凭证的金额。
    * 仅当凭证模板是百分比类型时才会显示金额字段。  
30. 单击“确定”。


