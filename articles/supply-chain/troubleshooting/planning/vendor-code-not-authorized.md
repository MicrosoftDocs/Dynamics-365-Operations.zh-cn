---
title: 供应商代码未针对特定产品和日期授权
description: 当您尝试确认计划订单或向采购订单添加一行时，将收到一条错误消息，指示供应商代码未针对产品和日期授权。
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPO_ReqTransPoMarkFirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 67cb054a648eac2b9a0e89b5e6a645af3c6142ad25237adb7afbd28f96c7e2eb
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6777711"
---
# <a name="vendor-code-isnt-authorized-for-a-specific-product-and-date"></a>供应商代码未针对特定产品和日期授权

错误代码：SYP4881415

## <a name="symptoms"></a>故障特征

当您尝试确认计划订单或向采购订单添加一行时，将收到以下错误消息：

> 供应商代码 %1 未针对 %3 上的 %2 授权。

## <a name="cause"></a>原因

发生错误的原因是指定产品的 **核准供应商检查方法** 字段设置为 *仅警告* 或 *不允许*，并且供应商当前未授权供应该产品。

## <a name="resolution"></a>解决方法

若要解决此问题，请禁用相关产品的供应商检查或审核供应商。

若要禁用产品的供应商检查，请按照以下步骤操作。

1. 转到 **产品信息管理 \> 产品 \> 已发布产品**。
1. 打开相关产品。
1. 在 **购买** 快速选项卡上，将 **核准供应商检查方法** 字段设置为除 *仅警告* 或 *不允许* 以外的值。

若要审核产品的供应商，请按照以下步骤操作。

1. 转到 **产品信息管理 \> 产品 \> 已发布产品**。
1. 打开相关物料。
1. 在操作窗格上的 **购买** 选项卡上，在 **核准供应商** 组中，选择 **设置**。
1. 在 **核准供应商** 列表页面上，向网格添加一行，然后为其设置以下值：

    - **供应商** – 选择要为当前产品审核的供应商。
    - **生效日期** – 选择供应商获得批准的第一个日期。
    - **到期日期** – 选择供应商获得批准的最后一个日期。

有关详细信息，请参阅[审核特定产品的供应商](/dynamics365/supply-chain/procurement/tasks/approve-vendors-specific-products.md)。
