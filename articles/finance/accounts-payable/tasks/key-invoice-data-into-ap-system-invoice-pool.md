---
title: 使用发票池将发票数据键入 AP 系统
description: 此主题介绍如何使用发票登记簿创建发票。
author: abruer
manager: AnnBe
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 670dd2ec15aa26791758ec4bea2b431482499436
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227152"
---
# <a name="key-invoice-data-into-the-ap-system-using-invoice-pool"></a>使用发票池将发票数据键入 AP 系统

[!include [banner](../../includes/banner.md)]

此主题介绍如何使用发票登记簿创建发票。 然后使用发票池对发票与采购订单进行匹配，并在“供应商发票”页对费用进行关帐。


## <a name="create-a-purchase-order"></a>创建采购订单
1. 在导航窗格中，转到 **模块 > 应付帐款 > 采购订单 > 采购订单**。
2. 选择 **新建** 以创建新的采购订单。
3. 在 **供应商帐户** 字段中，从下拉列表选择供应商。 例如，选择供应商 **1001**。
4. 选择 **确定**。
5. 在 **物料编号** 字段中，在下拉列表中选择服务物料编号。 例如，选择 **S0001**。 净额为 75.00。  这是我们预期的发票金额。  
6. 在操作窗格上，选择 **采购**。
7. 选择 **确认**。

## <a name="create-and-post-and-invoice"></a>创建并过帐发票
1. 在导航窗格中，转到 **模块 > 应付帐款 > 发票 > 发票登记簿**。
2. 选择 **新建**。
3. 打开查找以选择您想使用的发票登记簿的名称。
4. 选择您想要使用的发票登记簿名称。
5. 单击 **行**，以打开登记簿和输入费用行。
6. 在查找中，选择供应商。 例如，选择供应商 **1001**。
7. 在 **发票** 字段中，输入发票编号。
8. 在 **描述** 字段中，键入一个值。
9. 在 **信用** 字段中，输入一个数字。
10. 在 **采购订单** 字段中，打开下拉列表选择您之前创建的采购订单。
11. 在 **审核人** 字段中，在下拉列表中突出显示一个审核人，然后单击 **选择** 选择该审核人。
12. 选择 **过帐**。

## <a name="open-an-invoice-from-the-pool-and-match-it-to-a-purchase-order-to-complete-the-invoice-process"></a>从发票池中打开发票并与采购订单进行匹配以此完成发票流程
1. 在导航窗格中，转到 **模块 > 应付帐款 > 发票 > 发票池**。
2. 选择 **采购订单** 以从池中的发票中创建供应商发票。
3. 选择您想要查看的发票。
4. 选择 **更新匹配状态** 以完成匹配。
5. 在操作窗格上，选择 **选项**。
6. 选择 **更改视图**。
7. 选择 **网格视图**。
8. 选择 **过帐**。
9. 关闭窗体。
10. 在导航窗格中，转到 **模块 > 应付帐款 > 供应商 > 供应商**。
11. 选择采购订单上的供应商。 例如，选择供应商 **1001**。
12. 在操作窗格上，选择 **供应商**。
13. 选择 **交易记录**。
14. 选择您创建的发票。 发票登记簿应计项目被冲销并被过帐到相应的费用帐户。  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]