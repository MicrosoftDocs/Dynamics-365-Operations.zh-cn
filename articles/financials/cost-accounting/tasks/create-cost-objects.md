---
title: 创建成本对象
description: 此过程显示如何通过数据连接器将 Dynamics 365 for Finance and Operations Enterprise Edition 成本中心财务维度导入成本核算来创建成本对象。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1e12de1d51658092fb19f652cef7c1cc78b255b5
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1543763"
---
# <a name="create-cost-objects"></a>创建成本对象 

[!include [task guide banner](../../includes/task-guide-banner.md)]

此过程显示如何通过数据连接器将 Dynamics 365 for Finance and Operations Enterprise Edition 成本中心财务维度导入成本核算来创建成本对象。 用于创建该过程的是演示公司 USMF。 此过程针对 Dynamics 365 for Operations 版本 1611 中增加的成本核算功能。


## <a name="create-new-cost-objects"></a>新建成本对象
1. 转到“成本核算”>“维度”>“成本对象维度”。
2. 单击“新建”。
3. 在“名称”字段中，键入一个值。
4. 在“维度成员的数据连接器”字段中，输入或选择一个值。
5. 在“描述”字段中，键入一个值。
6. 单击“保存”。

## <a name="configure-the-data-connector"></a>配置数据连接器
1. 单击“配置维度成员提供方”。
    * 选择 CostCenter 将 CostCenter 维度导入成本核算中。  
2. 在“维度名称”字段中，选择“成本中心”。
3. 单击“确定”。

## <a name="import-cost-centers"></a>导入成本中心
1. 单击“导入维度成员”。
2. 单击“确定”。

## <a name="view-the-imported-cost-centers"></a>查看导入的成本中心
1. 单击“查看维度成员”。

