---
title: 导入供应商发票时生成发票行
description: 本主题介绍在导入发票时自动生成供应商发票上的发票行的功能。
author: sunfzam
ms.date: 09/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-08-30
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 87dec3c142ae296975ab98432421be4548085c80
ms.sourcegitcommit: 9e8d7536de7e1f01a3a707589f5cd8ca478d657b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2021
ms.locfileid: "7647875"
---
# <a name="generate-invoice-lines-when-you-import-vendor-invoices"></a>导入供应商发票时生成发票行

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

本主题介绍在导入发票时自动生成供应商发票上的发票行的功能。

有时，供应商发票包含有限的信息，如接收人信息和小计。 但是，它们不包含行项的信息。 导入发票时，系统可以根据对应采购订单上的信息自动生成发票行。

要启用自动创建发票行，请按照这些步骤操作。

1.  转到 **应付帐款 \>设置 \> 应付帐款参数**。
2.  在 **供应商发票自动化** 选项卡上，在 **自动为导入的发票创建行** 下，将 **自动创建发票行** 选项设置为 **是**。 
4.  在 **选择将自动创建的默认发票行数量** 字段中，选择系统应用于自动生成发票行的数量：

    - **订购数量** – 系统将从采购订单行生成行。 此值为默认值。
    - **物料收货数量** – 系统将使用采购订单编号查找相关的物料收货。 然后，将使用物料收货数量生成发票行。

## <a name="data-entity-changes"></a>数据实体更改

为了支持此主题中介绍的功能，**供应商发票标题** 数据实体已增强。 添加了三个字段：

- **HeaderOnlyImport** – 必须将此字段设置 **是**，系统才能为发票标题生成行。
- **PurchIdRange** – 采购订单编号的列表。 发票编号可以是一个范围，如 **INV0001..INV0009**（其中两个点分隔范围的开始和结束），或离散值，如 **INV0001, INV0003, INV0006**。 所有采购订单必须属于发票标题上的同一供应商帐户。 否则，您将收到以下错误消息：“无法生成发票行。 采购订单具有不同的供应商帐户。”
- **PackingslipRange** – 物料收货编号的列表。 可从物料收货创建供应商发票行。 但是，通常不在供应商发票上包含物料收货编号。 仅当您能够明确确定特定发票的物料收货时，再将物料收货编号输入此字段。 可以根据物料收货生成发票行。 如果使用此字段，将忽略 **应付帐款参数** 页上 **选择将自动创建的默认发票行数量** 字段的设置。 

**限制**：如果输入多个物料收货编号，将使用相同的发票编号创建多个待处理供应商发票。 您必须先手动合并它们，然后才能进一步处理发票。 在以后的版本中，我们计划实现由系统自动合并发票，因此将消除此限制。

所有物料收货必须属于发票标题上的同一供应商帐户。

## <a name="result"></a>结果

如果系统成功生成行，将在供应商发票自动化历史记录中记录以下消息：“自动创建发票行: 成功。”

如果系统生成行失败，将记录以下错误消息：“自动创建发票行: 失败。”