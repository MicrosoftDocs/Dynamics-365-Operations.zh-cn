---
title: 检查货物质量
description: 本主题说明如何处理质检订单。
author: perlynne
manager: AnnBe
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 75fbfbb7b993b528e96d247dafa2bdfe20837987
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145609"
---
# <a name="inspect-the-quality-of-goods"></a>检查货物质量

[!include [banner](../../includes/banner.md)]

本主题说明如何处理质检订单。 您可以使用 USMF 公司演示数据运行此指南。 在开始此示例过程前，需要确认采购订单为“000016”，并且将产品收据过帐。 这将自动创建质检订单。 质量检查通常由质检员执行。


## <a name="select-a-quality-order"></a>选择质检订单。
1. 在导航窗格中，转到**模块 > 库存管理 > 定期任务 > 质量管理 > 质检订单**。
2. 在开始此过程前，选择已创建的质检订单。  

## <a name="record-test-results"></a>记录测试结果
1. 选择**结果**。
2. 选择**编辑**。
3. 在**结果数量**字段中，输入一个数字。
4. 在**结果**字段中，在下拉菜单中选择所需记录。  
- 在此示例中，结果将基于预定义的结果。 通常您可以记录更具体的测试结果，例如大小或其他维度。  
5. 选择**保存**。
6. 关闭该页面。

## <a name="validate-the-quality-order"></a>验证质检订单
1. 选择**验证**。
2. 在**验证者**字段中，从下拉菜单选择执行检查的用户。  
3. 单击**选择**。
4. 选择**确定**。
5. 关闭该页面。

