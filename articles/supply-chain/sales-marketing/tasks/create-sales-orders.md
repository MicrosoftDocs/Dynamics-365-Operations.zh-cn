---
title: 创建销售订单
description: 此过程说明如何创建销售订单。
author: Henrikan
ms.date: 04/06/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, InventDimParmFixed, InventProductDimensionLookup, SalesTotals
audience: Application User, SalesTableDelete, SalesTableListPagePreviewPage, SalesUpdateRemain
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 462f47ab5d85665ed8132e5bfb6dd945c537c1ef
ms.sourcegitcommit: 4861ec2d3ae24cc9dd4ad3ac748fd05be3d80c70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/06/2022
ms.locfileid: "8551715"
---
# <a name="create-sales-orders"></a>创建销售订单

[!include [banner](../../includes/banner.md)]

此过程说明如何创建销售订单。 您可以在演示数据公司 USMF 中使用此过程。 销售订单通常由销售订单处理器创建。 

## <a name="enter-sales-order-header-details"></a>输入销售订单抬头详细信息
1. 转到 **导航窗格 > 模块 > 销售和营销 > 销售订单 > 所有销售订单**。
2. 选择 **新建**。
3. 在 **客户帐户** 字段中，选择下拉按钮以打开查找。
4. 在列表中，找到并选择客户记录。
    - 在本示例中，选择客户编号 US-004。  
5. 选择 **确定**。

## <a name="enter-sales-order-line-details"></a>输入销售订单行详细信息
    
您的公司销售的产品可能款式不同，可以不同维度区分，例如配置、颜色、大小和样式。 此外，产品可以设置为使用存储维度，如站点、仓库、托盘和跟踪维度，例如批号和序列号。 在分配这些维度时，您必须在订单行选择维度的数值。 为了提高订单输入效率，您可能要添加各自的维度字段到订单网格中。
    
1. 在 **销售订单行** 部分下，选择 **销售订单行**。
2. 选择 **维度**。
    
    在本示例中，选择颜色、位置和仓库维度。 您选择的维度将显示在订单网格中。 如果想要保存您的选择，则将 **保存设置** 选项设为“是”。
    
3. 选择 **确定**。
4. 在 **物料编号** 字段中，选择下拉按钮以打开查找。
5. 在本示例中，单击“物料编号 T0004”。
    - 如果物料是销售类别的一部分，物料名称将在“销售类别”字段自动显示。  
    - 如果产品维度字段已包含一个值，则该值是从定义为默认产品维度的产品记录中复制过来的。 您可以随时更改默认值。   
6. 在 **颜色** 字段中，选择下拉按钮以打开查找。
7. 在列表中，找到并选择所需记录。
8. 在 **数量** 字段中，输入一个数字。
    - 如果物料销售单位与采购、生产和存储单位不同，且测量单位在产品记录中有设置，则该值将在 **单位** 字段显示。 您可以随时更改该值。   
    - 如果 **站点** 字段已包含一个值，则该值是从订单抬头或产品相关的订单设置中复制过来的。 您可以随时更改该值。 如果此字段为空，则选择一个值。   
    - 如果 **单价** 字段已包含一个值，则该值是从有效贸易协议或产品记录中复制过来的。 （单价还可来自销售协议，但是销售协议的销售订单创建流程与此处显示的不同。）如果此字段为空，则输入一个值。   
    - **折扣** 字段包含一个产品单位的折扣金额。 若要计算总折扣金额，应用单行折扣值乘以行数。 如果 **折扣** 字段已包含一个值，则该值是从有效贸易协议中复制过来的。 如果此字段为空，且您想给该客户行折扣，则输入一个值。  
    - **折扣百分比** 字段包含计算全部行总额时减去的百分比值。  如果 **折扣百分比** 字段已包含一个值，则该值是从有效贸易协议中复制过来的。 如果此字段为空，且您想给该客户行折扣，则输入一个值。 
    - **净额** 字段包含根据行数和折扣调整后单价计算的值。  您可以用另外的值覆盖该计算值。  

## <a name="review-the-order-totals"></a>查看订单总计
1. 在 **操作窗格** 上，选择 **销售订单**。
2. 选择 **合计**。
    
    **合计** 页面显示整个订单的详细信息。 这包括小计金额（最后单行折扣调整后所有行净额的总和）、总发票金额（最后订单折扣调整后的小计金额）、费用、销售税、客户信用额度情况和其他信息。 发票金额是显示在客户的发票单据上的金额。  
    
3. 选择 **确定**。

## <a name="sales-order-creation-performance-enhancement"></a>销售订单创建性能增强
应用程序 10.0.26 版本引入的新功能减少了表 **SourceDocumentHeader** 和 **SourceDocumentLine** 的额外记录的创建。 由于不需要创建这些记录，性能得到改进，存储大小也因此减少。 这些基础源文档框架表目前不用于产品中的销售订单，也没有相关的使用计划。 启用此功能被认为是可提高性能的安全更改。 

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
