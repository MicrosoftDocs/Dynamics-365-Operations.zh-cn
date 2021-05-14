---
title: 创建可配置产品的销售订单
description: 此过程显示如何将配置模板应用于销售订单中的一个产品。
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, PCRuntimeConfigurator, PCTemplateConfigurationSelection
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8607de5705354aa58c985fb536f3e1d52acd1f37
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921281"
---
# <a name="create-a-sales-order-for-a-configurable-product"></a>创建可配置产品的销售订单

[!include [banner](../../includes/banner.md)]

此过程显示如何将配置模板应用于销售订单中的一个产品。 此示例使用 USMF 演示数据公司中的 D0006 扬声器模型。 通常，销售订单处理人员使用此过程。

## <a name="create-a-sales-order"></a>创建销售订单

1. 转到 **销售和市场营销 \> 工作区 \> 销售订单处理和查询**。
1. 选择 **新建**。
1. 选择 **销售订单**。
1. 在 **客户帐户** 字段中选择 *US-001*。 
1. 选择 **确定**。
1. 在 **物料编号** 字段中，选择 *D0006*。
    * 对于此任务，必须选择一个可配置产品。  
1. 选择 **产品和供应**。
1. 选择 **配置行**。
    * 请注意，已根据选择的配置更改了价格，并且 **含电缆** 字段现在已设置为 *True*。  
    * 记下为电缆选择的默认价格和设置。  
1. 选择 **负荷模板**。
    * 此示例显示如何应用模板以选择预定义的配置。 如果将此过程用作任务指南并希望查看可用的其他属性值，必须选择 **解锁** 按钮。  
1. 选择 **确定**。
1. 选择 **确定**。
1. 展开 **行详细信息** 部分。
1. 选择 **产品** 选项卡。
    * 此物料的配置现在在产品维度下列出。  
1. 关闭该页面。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]