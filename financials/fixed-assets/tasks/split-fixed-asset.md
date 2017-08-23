--- 
title: "拆分固定资产"
description: "此任务指南将把一个资产帐簿的一定百分百拆分到新资产帐簿。"
author: saraschi2
manager: AnnBe
ms.date: 10/19/2016
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
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 5aea1aab9f6b084bd0c5bd2119639bff3555bb8a
ms.contentlocale: zh-cn
ms.lasthandoff: 07/27/2017

---
# <a name="split-a-fixed-asset"></a>拆分固定资产

[!include[task guide banner](../../includes/task-guide-banner.md)]

此任务指南将把一个资产帐簿的一定百分百拆分到新资产帐簿。  它使用会计角色和 USMF 演示数据。


## <a name="create-a-new-fixed-asset"></a>创建新的固定资产
1. 转到“固定资产”>“固定资产”>“固定资产”。
2. 单击“新建”。
3. 在“固定资产组”字段中，输入或选择一个值。
4. 请注意，固定资产编号将在稍后的拆分流程使用。
5. 在“名称”字段中，键入一个值。
6. 关闭窗体。

## <a name="split-a-fixed-asset"></a>拆分固定资产
1. 在列表中，查找并选择要拆分的固定资产。
2. 在列表中，单击所选行中的链接。
3. 单击“帐簿”。
    * 选择拆分到新资产的帐簿  
4. 单击“功能”。
5. 单击“拆分固定资产”。
6. 在“目标固定资产”字段中，输入或选择一个值。
7. 在“目标帐簿”字段中，单击下拉按钮以打开查找。
8. 在“交易记录日期”字段中，输入日期。
9. 在“百分比”字段中，输入一个数字。
10. 在“日记帐名称”字段中，输入或选择一个值。
11. 单击“确定”。

## <a name="post-the-journal-transaction"></a>过帐日记帐交易记录
1. 转到固定资产>流水输入项>固定资产流水。
2. 在列表中，选择在拆分流程创建的日记帐。
3. 单击“行”。
    * 验证已创建的日记帐行。  创建原始资产的购置调整交易记录，以通过拆分流程指定的百分比减少价值。  为新资产创建相同金额的购置交易记录。  
4. 单击“过帐”。


