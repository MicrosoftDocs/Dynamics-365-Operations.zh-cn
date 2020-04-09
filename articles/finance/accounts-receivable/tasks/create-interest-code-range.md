---
title: 创建带范围的利息代码
description: 可以设置利息代码，根据值范围以计算不同的利息金额。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Interest, CustInterestRange
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c0c5b20ff6fff2bc62daca68c46e949a38df8d92
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140258"
---
# <a name="create-an-interest-code-with-a-range"></a>创建带范围的利息代码

[!include [banner](../../includes/banner.md)]
可以设置利息代码，根据值范围以计算不同的利息金额。 该过程将向您显示如何添加利息代码和范围。

1. 转到“信贷和收款”>“利息”>“设置利息代码”。
2. 单击“新建”。
3. 在“利息代码”字段，输入利息代码名称。
4. 在“描述”字段，输入利息代码的描述。
5. 选择“月份”。
6. 展开“收益”部分。
7. 展开“原币收益”部分。
8. 在“分类帐过帐帐户”字段中，指定所需值。
9. 在“范围利息”字段，选择“月份”。
10. 单击“添加”。
11. 在“描述”字段中，输入货币和范围的描述。
12. 单击“保存”。
13. 单击“范围”。
14. 单击“新建”。
15. 在“开始值”中输入 0，然后输入将用于计算利息的月利息百分比。 示例：开始值为 1.5。
16. 单击“新建”。
17. 输入“下一开始值”为 4，是您将计算新的利息金额的第一个月。
18. 输入将用于计算月份 4 后的月利息百分比。 在本示例中，为 2.0。
19. 单击“新建”。
20. 输入“下一开始值”为 7，是计算新的利息金额的下一个月。
21. 输入将用于计算月份 7 后的月利息百分比。 在本示例中，为 2.5。
22. 单击“关闭”以完成设置。

