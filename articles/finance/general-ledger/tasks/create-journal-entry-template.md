---
title: 使用模板创建日记帐分录
description: 已过帐的日记帐凭证可以保存为凭证模板并应用到新日记帐凭证中。
author: aprilolson
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransDaily, LedgerJournalTransVoucherTemplate
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 360df29e6349fd4d42d6d14af646e929b73943bd
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145140"
---
# <a name="create-a-journal-entry-using-template"></a>使用模板创建日记帐分录

[!include [banner](../../includes/banner.md)]

已过帐的日记帐凭证可以保存为凭证模板并应用到新日记帐凭证中。 该程序适用于 USMF 演示公司。

1. 转到**导航窗格 > 模块 > 总帐 > 日记帐条目 > 普通日记帐**。
2. 在**操作窗格**中，单击**新建**。 此程序开始时需要创建和过帐日记帐凭证，但所有以前已过帐的日记帐凭证可以保存为模板。  
3. 在**名称**字段中，单击下拉按钮以打开查找。
4. 在列表中，找到并选择所需记录。
5. 在列表中，单击所选行中的链接。
6. 单击**行**。
7. 在**帐户类型**字段中，键入一个值。
8. 在**描述**字段中，键入一个值。
9. 在**借方**字段中，键入一个值。
10. 单击**新建**。
11. 在**帐户类型**字段中，键入一个值。
12. 在**描述**字段中，键入一个值。
13. 在**借方**字段中，键入一个值。
14. 单击**新建**。
14. 在**帐户**字段中，指定所需值。
15. 在**描述**字段中，键入一个值。
16. 在**贷项**字段中，键入一个值以使凭证试算平衡。
17. 在**操作窗格**上，单击**过帐**。
18. 单击**功能**。
19. 单击**保存凭证**模板。
20. 此程序使用**百分比模板**类型。 单击“确定”。
    - 百分比：凭证中的金额会被转换为百分比系数，当选择了凭证模板时，这允许应用任何金额。
    - 金额：将存储和应用实际金额。  
21. 单击**普通日记帐**。
22. 单击**新建**。
23. 在**名称**字段中，单击下拉按钮以打开查找。
24. 在列表中，单击所选行中的链接。
25. 单击**行**。
26. 单击**功能**。
27. 单击**选择凭证模板**。
28. 查找您之前创建的模板。 单击 **确定**。 如果存在其它模板，您可能需要单击**上一步**，然后选择正确的模板。  
29. 在**金额**字段中，输入要应用于凭证的金额。 仅当凭证模板是百分比类型时才会显示**金额**字段。  
30. 单击 **确定**。

