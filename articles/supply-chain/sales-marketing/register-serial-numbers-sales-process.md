---
title: 使用序列化物料
description: 本文说明如何在销售流程中登记装箱单或发票的序列号。 如何公司希望捕获序列号是为了用于服务和保修用途，但不必在从收货到发货的库存中维护序列号，那么此功能很有用。
author: Henrikan
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResTrackingDimensionGroup, InventTrackingRegisterTrans, SalesEditLines, SalesTable, InventSerial
audience: Application User
ms.reviewer: kamaybac
ms.custom: 28931
ms.assetid: 5d39630f-607e-492b-8c1e-790ca53effa0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b89e9ab547d13e68ead88d76f9922d14fde4beb3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901841"
---
# <a name="working-with-serialized-items"></a>使用序列化物料

[!include [banner](../includes/banner.md)]

本文说明如何在销售流程中登记装箱单或发票的序列号。 如何公司希望捕获序列号是为了用于服务和保修用途，但不必在从收货到发货的库存中维护序列号，那么此功能很有用。

许多公司捕获序列号只是为了用于服务和保修用途，因此不必在从收货到发货的库存中维护序列号。 在这些情况下，在产品销售时可以登记装箱单或发票的序列号。 如果产品后来退货，您可以跟踪每个发票的产品以确定是否销售产品，服务或保修合同是否有效。

您必须通过选择 **跟踪维度组** 页的 **在销售流程中有效** 选项来启用销售流程的序列号。 然后，在 Supply Chain Management 中将发生以下事件：
-   在 **序列号** 快速选项卡上，选择 **序列号控制** 选项。 如果选中此选项，则必须在装箱单或发票上登记每个物料的序列号。
-   除了 **允许空发货** 选项外，清除序列号跟踪维度组的所有选择。 可以选中 **允许空发货** 选项来覆盖序列号控制并允许产品在没有登记序列号的情况下包装和开票。

## <a name="when-do-i-register-serial-numbers-during-the-sales-process"></a>何时在销售流程中登记序列号？
可以在销售订单的装箱单或在发票上登记序列号。 当为附带装箱单的已装运序列化物料准备发票时，可以选择装箱单上的序列号开发票。 登记序列号的数量不能超过已装运物料的数量。 若创建一个部分发票，可以选择的序列化物料少于登记在装箱单上的。 当打印装箱单或发票时，要包括登记的序列号。

## <a name="can-i-enter-serial-numbers-by-scanning-them-or-do-i-have-to-type-them"></a>我可以通过扫描它们输入序列号吗？还是必须键入它们？
您可以扫描或键入序列号。 在使用扫描仪时，扫描模式确定是否要在发票或装箱单的序列号列表中添加或删除序列号。 如果想要扫描序列号，例如使用手持式条码扫描仪，请在序列号后发送 Enter 或 TAB 命令来配置扫描仪。 此命令将指示数据流的结束。 否则，您必须在每个序列号扫描后按键盘上的 Enter 或 TAB。

## <a name="if-i-enable-serial-numbers-for-the-sales-process-do-i-have-to-register-all-serial-numbers-for-all-items"></a>若启用销售流程的序列号，是否必须登记所有物料的所有序列号？
分配给产品的跟踪维度组的设置确定是否必须为装箱单或发票上的所有物料登记序列号。 当启用销售流程的序列号时，**序列号控制** 选项将被自动选定。 然后您必须为装箱单或发票上的每个物料登记序列号或者为不可读编号登记一个空登记。 若不想为每个物料要求序列号，在该物料所分配的跟踪维度组上选择 **允许空发货** 选项。 然后可以登记的序列号少于装运物料的数量。 若登记的序列号多于装运物料的数量，装箱单或发票将不能过帐。

## <a name="can-i-register-serial-numbers-for-partial-invoices-and-partial-shipments"></a>可以登记部分发票或部分装运的序列号吗？
可以为销售订单创建部分发票和装箱单，只登记那些发票和装箱单所包括的物料序列号。 若想创建部分发票，并且具有销售订单的多个装箱单，可以包括多个装箱单中的序列号。 不过，只能有一个不包括所有序列号的装箱单。 例如，若有三个装箱单且每个装箱单包含两个序列化物料，则不能从每个装箱单中为物料创建部分发票。

## <a name="what-do-i-do-when-a-serial-number-isnt-readable"></a>在序列号不可读时该怎么办？
若序列号不能读取或扫描，可以通过单击 **序列号** 页的 **不可读** 为物料创建一个空白行。 若序列号以后可用，则可以更新发票或装箱单。 有关详细信息，请参阅下一个部分“是否能更正或更改已为销售订单登记的序列号？”

## <a name="can-i-correct-or-change-the-serial-numbers-that-i-have-registered-for-a-sales-order"></a>是否能更正或更改已为销售订单登记的序列号？
可以，则当满足以下条件时可以更正序列号：
-   **发票** – 可以更改未开发票物料的序列号。 然后还更新装箱单。 但是，若销售订单行由登记负数量更改，则不能更改销售订单行的序列号。
-   **装箱单** – 不能部分更正包含序列化物料的装箱单行。 必须冲销该行的全部数量。 若装箱单已被取消或更正，当为相同的序列化物料创建新装箱单时则不必再登记已冲销的序列号。 将使用已登记的编号。

## <a name="can-i-view-the-serial-numbers-that-were-shipped-together-with-a-specific-packing-slip-or-that-were-included-on-an-invoice"></a>可以查看随特定装箱单装运的序列号或包含在发票中的序列号吗？
可以，则可以在装箱单日志行或发票日志行运行查询来查看包含在该文档中的所有序列号列表。

## <a name="can-i-view-the-serialized-items-that-i-have-on-hand"></a>可以查看现有序列化物料吗？
不可以，您不能查看现有序列化物料，因为直到物料销售才会为物料登记序列号。

## <a name="can-i-register-serial-numbers-for-catchweight-items"></a>可以为实际称重物料登记序列号吗？
不可以，在销售流程中不能为实际称重物料登记序列号。 此外，如果产品设置为非定重物料，您无法将产品分配到设置为仅在销售流程中使用序列号的跟踪维度组。

## <a name="can-i-register-serial-numbers-at-the-retail-pos"></a>我可以在 Retail POS 登记序列号吗？

可以，当用户销售分配到设置为仅在销售流程中使用序列号的跟踪维度组的物料时，零售销售点 (POS) 将提示用户输入序列号。

## <a name="what-security-roles-are-required-in-order-to-register-serial-numbers-during-the-sales-process"></a>在销售流程中登记序列号需要哪些安全角色？
此功能对可以维护销售装箱单和销售发票的所有角色均可用。 以下职责使工作人员可更正序列号，为无法读取或扫描的序列号登记空白项：
-   维护序列号更正
-   维护不可读序列号的登记







[!INCLUDE[footer-include](../../includes/footer-banner.md)]