---
title: 创建采购订单时应用采购协议
description: 该过程会显示在创建采购订单时，如何使用采购协议。
author: GalynaFedorova
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a21821d75be2d5340cd418c12be39431870d2779
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/03/2022
ms.locfileid: "8678734"
---
# <a name="apply-a-purchase-agreement-when-creating-a-purchase-order"></a>创建采购订单时应用采购协议

[!include [banner](../../includes/banner.md)]

该过程会显示在创建采购订单时，如何使用采购协议。 在创建采购订单时必须应用采购协议，因为存在应复制到采购订单标题的一般条件。 此任务通常由采购人员完成。 作为本指南的先决条件，您必须拥有某个供应商和物料的带产品数量承诺的有效采购协议。 如果您拥有带其他类型承诺的采购协议，则可以使用相同过程。

## <a name="create-a-purchase-order"></a>创建采购订单

1. 转到 **生产和采购 \> 工作区 \> 采购订单准备**。
1. 在操作窗格上选择 **新建采购订单**。
1. **创建采购订单** 对话框将打开。 选择 **供应商帐户**。 根据需要检查和调整其他地址字段。
1. 展开 **常规** 快速选项卡。
1. 在 **采购协议** 字段中，查找并选择要使用的有效协议。 该供应商的所有可用协议皆列示于此。  
1. 选择 **是**。
1. 选择 **确定**。

## <a name="add-a-line"></a>添加行

1. 在 **项目编号** 字段中，键入一个值。 如果承诺的特定库存或位置维度存在，您必须在采购订单行上输入相同的值，以便利用协议。
1. 在 **站点** 字段中，选择下拉按钮以打开查找。 站点可能已填充来自订单或供应商的默认值。 如果是这种情况，请跳过此步骤。  
1. 在列表中，找到并选择所需记录。
1. 在列表中，选择所选择行中的链接。
1. 在 **数量** 字段中，输入一个数字。 验证价格是从承诺复制而来的。  

## <a name="look-up-the-commitment"></a>查找承诺

1. 选择 **更新行**。
1. 选择 **已附加**。 您可在此获得采购协议的详情。 例如，您可以查看价格以及价格和折扣是否被固定，这意味着，如果您将采购订单上的价格或折扣更改为不同于承诺载明的值，系统将会删除链接，以使采购订单行不履行承诺。 您还可以查看是否选择“最大值”是强制执行的选项，这意味着所有履行承诺的订单的数量综合不能超过承诺载明的数量。  
1. 关闭该页面。

## <a name="look-up-the-purchase-agreement"></a>查找采购协议

1. 在 **操作窗格** 上，选择 **常规**。
1. 选择 **采购协议**。
1. 关闭该页面。
1. 关闭该页面。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]