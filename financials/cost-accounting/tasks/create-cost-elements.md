--- 
title: "创建成本元素"
description: "可通过几种方法在成本核算中创建成本要素。"
author: YuyuScheller
manager: AnnBe
ms.date: 10/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 0b1045610881bc272798f1176fbca58731e5d43b
ms.contentlocale: zh-cn
ms.lasthandoff: 07/27/2017

---
# <a name="create-cost-elements"></a>创建成本元素 

[!include[task guide banner](../../includes/task-guide-banner.md)]

可通过几种方法在成本核算中创建成本要素。 此过程显示如何通过数据连接器导入主科目来创建成本要素。 用于创建该过程的是演示公司 USMF。 此过程针对 Microsoft Dynamics 365 for Operations 版本 1611 中增加的成本核算功能。


## <a name="create-new-cost-elements"></a>新建成本要素
1. 转到“成本核算”>“维度”>“成本要素维度”。
2. 单击“新建”。
3. 在“名称”字段中，键入一个值。
4. 在“维度成员的数据连接器”字段中，输入或选择一个值。
5. 在“描述”字段中，键入一个值。
6. 单击“保存”。

## <a name="configure-the-data-connector"></a>配置数据连接器
1. 单击“配置维度成员提供方”。
2. 在“会计科目表”字段中，输入或选择一个值。
    * 选择“共享”以使用共享的会计科目表。  
3. 单击“新建”。
4. 在列表中，标记所选的行。
    * 可以为科目应用筛选器以满足条件。  
5. 在“源主科目”字段中，输入或选择一个值。
6. 在“目标主科目”字段中，输入或选择一个值。
7. 单击“确定”。

## <a name="import-main-accounts"></a>导入主科目
1. 单击“导入维度成员”。
    * 将把主科目导入成本核算并用作成本要素。  
2. 单击“确定”。

## <a name="view-the-imported-accounts-as-cost-elements"></a>将导入的科目作为成本要素查看
1. 单击“查看维度成员”。
    * 将导入的会计科目作为成本可流向的业务中的成本要素查看。  


