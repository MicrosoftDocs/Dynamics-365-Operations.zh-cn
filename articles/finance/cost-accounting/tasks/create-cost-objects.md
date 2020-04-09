---
title: 创建成本对象
description: 此过程显示如何通过数据连接器将成本中心财务维度导入成本核算来创建成本对象。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ed020348e50158362fda7b6b36dcdb17c48b4532
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142309"
---
# <a name="create-cost-objects"></a>创建成本对象 

[!include [banner](../../includes/banner.md)]

此过程显示如何通过数据连接器将成本中心财务维度导入成本核算来创建成本对象。 用于创建该过程的是演示公司 USMF。 


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

