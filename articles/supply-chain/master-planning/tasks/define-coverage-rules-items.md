---
title: 定义物料的覆盖规则
description: 创建此程序的演示数据公司是 USMF。
author: ShylaThompson
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ReqGroup, DefaultDashboard, EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ff2d83a01f366517502bfc5c885b6f963bd945ca
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829704"
---
# <a name="define-coverage-rules-for-items"></a>定义物料的覆盖规则

[!include [banner](../../includes/banner.md)]

创建此程序的演示数据公司是 USMF。 该过程会显示如何创建覆盖范围规则，以及覆写特定物料的覆盖范围设置。 它也显示了如何确定默认库存设置。


## <a name="create-a-coverage-group"></a>创建覆盖范围组
1. 转到 **导航窗格 > 模块 > 主计划 > 设置 > 覆盖范围组**。
2. 单击 **新建**。
3. 在 **覆盖范围组** 字段中，键入一个值。
4. 在 **名称** 字段中，键入一个值。
5. 在 **日历** 字段中，键入一个值。 选择总体规划用于创建本组内物料的补货建议的日历。  
6. 在 **覆盖范围代码** 字段中，选择一个选项。 选择此过程的“要求”。  
7. 在 **覆盖时限（以天为单位）** 字段中，输入“90”。 对于该项目，主计划将创建未来 90 天的附属建议。  
8. 在 **负天数** 字段中，输入“1”。
9. 在 **正天数** 字段中，输入“1”。
10. 展开或折叠 **其他** 部分。
11. 在 **安全宽限期(天)** 部分的 **添加到需求日期的收货宽限期** 字段中，输入“1”。 例如，如果将收货宽限期设置为 1 天，并且一个采购订行计划在 5 月 15 日收货，则总体规划会将调整后的收货日期计算为 5 月 16 日。  
12. 在 **从需求日期中减去的发货宽限期** 字段中，输入"1"。 例如，如果将安全宽限期设置为 1 天，并且一个销售订行计划在 5 月 15 日交货，则主计划编制将调整后的交货日期计算为 5 月 14 日。  
13. 在 **再订购宽限期添加到物料提前期** 字段中，输入"1"。
14. 单击 **保存**。

## <a name="create-a-new-product"></a>创建新产品
1. 转到 **导航窗格 > 模块 > 产品信息管理 > 产品 > 已发放产品**。
2. 单击 **新建**。
3. 在 **产品编号** 字段中，键入一个值。
4. 在 **产品名称** 字段中，键入一个值。
5. 在 **物料模型组** 字段中，单击下拉按钮以打开查找。
6. 在列表中，找到并选择所需记录。
7. 在列表中，单击所选行中的链接。
8. 在 **物料组** 字段中，单击下拉按钮以打开查找。
9. 在列表中，找到并选择所需记录。
10. 在列表中，单击所选行中的链接。
11. 在 **存储维度组** 字段中，单击下拉按钮以打开查找。
12. 在列表中，找到并选择所需记录。
13. 在列表中，单击所选行中的链接。
14. 在 **跟踪维度组** 字段中，单击下拉按钮以打开查找。
15. 在列表中，找到并选择所需记录。
16. 在列表中，单击所选行中的链接。
17. 单击 **确定**。

## <a name="setup-default-order-settings"></a>设置默认订单设置
1. 在 **操作窗格** 中，单击 **计划**。
2. 在 **订单设置** 下，单击 **默认订单设置**。
3. 在 **采购订单** 下的 **默认站点** 字段中，键入在创建采购订单时的默认站点。
4. 在 **默认仓库** 字段中，键入存储物料的站点。
5. 展开或折叠 **库存** 部分。
6. 在 **倍数** 字段中，键入“10”。
7. 在 **最小订单数量** 字段中，键入“10”。
8. 在 **最大订单数量** 字段中，键入“100”。
9. 在 **标准订单数量** 字段中，键入“10”。
10. 在 **采购提前期** 字段中，输入数值。
11. 选中或取消选中 **工作日** 复选框。
12. 单击 **保存**。
13. 在 **默认订单类型** 字段中选择“采购订单”。
14. 单击 **保存**。
15. 关闭该页面。 关闭“默认订单设置”页面。  

## <a name="add-an-item-to-a-coverage-group"></a>向覆盖范围组中添加物料
1. 展开或折叠 **计划** 部分。
2. 在 **覆盖范围组** 字段中，单击下拉按钮以打开查找。
3. 在列表中，找到您创建的 **覆盖范围组**。
4. 在列表中，单击所选行中的链接。

## <a name="create-item-coverage-rules"></a>创建物料覆盖范围规则
1. 在 **操作窗格** 中，单击 **计划**。
2. 在 **覆盖范围** 下，单击 **物料覆盖范围**。
3. 单击 **新建**。
4. 单击 **常规** 选项卡。
5. 选中 **覆写覆盖范围组** 设置标题上的选择框。
6. 在 **覆盖时限（以天为单位）** 字段中，输入“60”。 尽管物料覆盖范围组要求的物料需提前 90 天做计划，此物料只需提前 60 天做计划。  
7. 在 **负天数** 字段中，输入“2”。
8. 在 **正天数** 字段中，输入“2”。
9. 单击 **提前期** 选项卡。
10. 选中 **采购** 标题上的选择框。
11. 在 **采购时间** 字段中，输入“5”。
12. 单击 **保存**。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]