---
title: 配置工作人员
description: 此过程演示如何将工作人员配置为有资格享受 POS 中的销售佣金的销售代表。
author: jblucher
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CommissionSalesGroup, CommissionSalesMember, DirPartyLookup, HcmWorker
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fd437f549ffc1f8879ce3814ace1193040b280e1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410575"
---
# <a name="configure-a-worker"></a>配置工作人员

[!include [banner](../includes/banner.md)]

此过程演示如何将工作人员配置为有资格享受 POS 中的销售佣金的销售代表。 此程序使用 USRT 演示数据公司。


## <a name="create-a-commission-sales-group-for-the-worker"></a>为工作人员创建佣金销售组
1. 转到“销售和市场营销”>“佣金”>“销售组”。
    * 可以将工作人员分配给一个或多个销售组。 在 POS 中，可以从商店通讯簿中选择包含工作人员的任何销售组。  
2. 单击“新建”。
3. 在“组”字段中，输入一个值。
4. 在“名称”字段中，键入一个值。
5. 单击“保存”。
6. 在操作窗格上，单击“常规”。
7. 单击“销售代表”。
    * 一个销售组可以包含多个工作人员。 可以根据定义的佣金份额在工作人员之间分佣金。  
8. 在“名称”字段中，输入或选择一个值。
9. 在“佣金份额”字段中，输入一个数字。
10. 单击“保存”。
11. 关闭该页面。
12. 关闭该页面。

## <a name="assign-the-workers-default-sales-group"></a>为工作人员分配默认销售组
1. 转至“Retail 和 Commerce”>“员工”>“工作人员”。
2. 在列表中，找到并选择所需记录。
3. 在列表中，单击所选行中的链接。
4. 单击“商业”选项卡。
    * 可以将工作人员分配给默认销售组。 如果商店的功能模板中启用了此选项，将把默认销售组自动添加到 POS 中的销售行。  
5. 单击“编辑”。
6. 在“默认组”字段中，输入或选择一个值。
7. 单击“保存”。

