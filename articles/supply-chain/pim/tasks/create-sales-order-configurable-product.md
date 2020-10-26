---
title: 创建可配置产品的销售订单
description: 此过程显示如何将配置模板应用于销售订单中的一个产品。
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, PCRuntimeConfigurator, PCTemplateConfigurationSelection
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 988d87757019d20dcaf675af925166ed376685f5
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/10/2020
ms.locfileid: "3985477"
---
# <a name="create-a-sales-order-for-a-configurable-product"></a>创建可配置产品的销售订单

[!include [banner](../../includes/banner.md)]

此过程显示如何将配置模板应用于销售订单中的一个产品。 此示例使用 USMF 演示数据公司中的 D0006 扬声器模型。 通常，销售订单处理人员使用此过程。


## <a name="create-a-sales-order"></a>创建销售订单
1. 点击“销售订单处理和查询”。
2. 单击“新建”。
3. 单击“销售订单”。
4. 在“客户帐户”字段中选择“US-001”。 
5. 单击“确定”。
6. 在“物料编号”字段中，选择 D0006。
    * 对于此任务，必须选择一个可配置产品。  
7. 单击“产品和供应”。
8. 单击“配置行”。
    * 请注意，已根据选择的配置更改了价格，并且“含电缆”字段现在已设置为 True。  
    * 记下为电缆选择的默认价格和设置。  
9. 单击“加载模板”。
    * 此示例显示如何应用模板以选择预定义的配置。 如果将此过程用作任务指南并希望查看可用的其他属性值，必须单击“解锁”按钮。  
10. 单击“确定”。
11. 单击“确定”。
12. 展开“行明细”部分。
13. 单击“产品”选项卡。
    * 此物料的配置现在在产品维度下列出。  
14. 关闭该页面。

## <a name="select-the-product-configuration"></a>选择产品配置

