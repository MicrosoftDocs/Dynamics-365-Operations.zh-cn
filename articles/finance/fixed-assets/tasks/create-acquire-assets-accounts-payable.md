---
title: 从应付帐款创建和购置资产
description: '此过程逐步演示如何遵照采购流程来创建和购置固定资产。 '
author: saraschi2
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetParameters, VendInvoiceWorkspace, VendEditInvoice, VendTableLookup, InventItemIdLookupSimple, AssetTable
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dbac069362a15b5ab1d2dbf88a732a14a3cf709d
ms.sourcegitcommit: 03f53980a4bc67b73ac2be76a3b3e7331d0db705
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/18/2021
ms.locfileid: "7394650"
---
# <a name="create-and-acquire-assets-from-accounts-payable"></a>从应付帐款创建和购置资产

[!include [banner](../../includes/banner.md)]

此过程逐步演示如何遵照采购流程来创建和购置固定资产。   本任务需要用到普通及应付帐目会计和演示公司USMF的数据。


## <a name="set-fixed-assets-parameters"></a>设置固定资产参数
1. 在 **导航窗格** 中，转到 **模块 > 固定资产 > 设置 > 固定资产参数**。
2. 展开 **采购订单** 快速选项卡。
3. 选中 **允许从采购中购置资产** 复选框。
4. 选中 **在产品收据或发票过帐期间创建资产** 复选框。

## <a name="create-a-new-vendor-invoice"></a>创建新的供应商发票
1. 在 **导航窗格** 中，转到 **模块 > 应付帐款 > 工作区 > 供应商发票条目**。
2. 单击 **新建供应商发票**。
3. 在 **发票帐户** 字段中，单击下拉按钮以打开查找。
4. 在列表中，单击所选行中的链接。
5. 在 **编号** 字段中，键入一个值。
6. 在 **过帐日期** 字段中，输入日期。
7. 单击 **添加行**。
8. 在 **物料编号** 字段中，单击下拉按钮以打开查找。 输入固定资产购置时可使用的非贮存物料或采购类别。  
9. 在列表中，单击所选行中的链接。
10. 在 **数量** 字段中，输入一个数字。 一个发票行只创建一哥固定资产，不考虑数量。 发票数量字段的值会被传送到固定资产数量参数  
11. 在 **单价** 字段中，输入一个数字。
12. 展开 **行详细信息** 快速选项卡。
13. 单击 **固定资产** 选项卡。
14. 选中 **创建新的固定资产** 复选框。
15. 在 **固定资产组** 字段中，单击下拉按钮以打开查找。
16. 在列表中，选择创建新固定资产时要使用的固定资产组。
17. 在列表中，单击所选行中的链接。
18. 单击 **过帐**。 在过帐发票时，将会创建和购置固定资产。  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
