---
title: 在转移单单据上打印税务信息
description: 本主题介绍如何在转移单单据上打印由税款计算服务确定的税务信息。
author: Kai-Cloud
ms.date: 10/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-10-12
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: d55767ef47e01edd11099f644134cfa48ea70e18
ms.sourcegitcommit: 1707cf45217db6801df260ff60f4648bd9a4bb68
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/23/2021
ms.locfileid: "7675712"
---
# <a name="print-tax-information-on-transfer-order-documents"></a>在转移单单据上打印税务信息

[!include [banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

本主题介绍如何在转移单单据上打印税务信息。 对于根据欧盟 (EU) 增值税 (VAT) 法规被视为集团内部供应和集团内部采购的存货转移，您可以打印转移单的估价单单据。 

以下与税务相关的数据将添加到转移单单据上：

- 存货转移的名称以及发货和收货地址
- 供应商和收货人的纳税标识号
- 供应货物的单价和应纳税金额
- 税码、税率、税额和税务指令

要配置此数据，您必须完成以下主要步骤。

1. [启用和设置转移单的税务功能](tasks/Tax-feature-support-for-transfer-order.md)。
2. [为法人创建和设置多个税务登记编号](emea-multiple-vat-registration-numbers.md)。
3. 在税码中设置免税代码、说明、税务指令和打印代码。 对于此示例，在 Microsoft Dynamics 365 Finance 中创建并同步了三个税码：**NL-Exempt**、**BE-RC-21** 和 **BE-RC+21**。

    1. 在 Finance 中，转到 **税务** \> **设置** \> **销售税** \> **免税(销售税)代码**。
    2. 选择 **编辑**，为 **EC** 免税代码输入说明。 例如，输入 **具有税务登记编号的免税 EC 装运**。
    3. 转到 **税** \> **间接税** \> **销售税** \> **销售税代码**。
    4. 选择 **BE-RC-21** 税码，然后选择 **税务指令**。
    5. 选择 **新建**。
    6. 在 **语言** 字段中，选择 **EN-US**。 然后，在 **文本** 字段中，输入 **根据欧盟增值税指令 2006/112/EC 第 138. 2. c) 条规定的货物转移单据**。
    7. 关闭该页面。
    8. 在 **常规** 快速选项卡上，在 **打印** 字段中，选择 **销售税率**。
    8. 选择 **NL-Exempt** 税码，然后在 **常规** 快速选项卡上，在 **打印** 字段中，选择 **销售税率**。

    > [!NOTE] 
    > 如果没有为税码维护免税代码说明或税务指令，税码、税率和免税说明不会打印在转移单单据上。

## <a name="print-the-transfer-order---shipment-document"></a>打印转移单 - 装运单据

装运转移货物后，按照这些步骤打印转移单 - 装运单据。

1. 转到 **库存管理** \> **查询和报表** \> **转移单** \> **装运**。
2. 在 **参数** 选项卡上，在 **打印** 组中，启用 **税务信息**。
3. 在 **要包括的记录** 选项卡上，选择 **筛选器**，选择转移单编号，然后选择 **确定**。
4. 选择 **确定** 打印转移单 - 装运单据。

## <a name="print-the-transfer-order---receipt-document"></a>打印转移单 - 收货单据

接收转移货物后，按照这些步骤打印转移单 - 收货单据。

1. 转到 **库存管理** \> **查询和报表** \> **转移单** \> **收货**。
2. 在 **参数** 选项卡上，在 **打印** 组中，启用 **税务信息**。
3. 在 **要包括的记录** 选项卡上，选择 **筛选器**，选择转移单编号，然后选择 **确定**。
4. 选择 **确定** 打印转移单 - 收货单据。

## <a name="print-the-transfer-overview-document"></a>打印转移概览单据

按照这些步骤打印转移概览单据。

> [!NOTE]
> 仅当转移单已装运或收货时，税务信息才可用。

1. 转到 **库存管理** \> **查询和报表** \> **转移单** \> **转移概览**。
2. 在 **参数** 选项卡上，在 **打印** 组中，启用 **税务信息**。
3. 在 **要包括的记录** 选项卡上，选择 **筛选器**，选择转移单编号，然后选择 **确定**。
4. 选择 **确定** 打印转移概览单据。

[!INCLUDE [footer-include](../../includes/footer-banner.md)]
