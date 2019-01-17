---
title: "信息代码和信息代码组"
description: "本文提供有关信息代码、信息代码组以及如何使用它们的概览。"
author: mugunthanm
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailInfocodeTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 22761
ms.assetid: 99877dba-a6e3-4d88-ba0a-ee5913aea17e
ms.search.region: global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: c9cd9197f395b69f65137a59392a4d83d692f6fa
ms.contentlocale: zh-cn
ms.lasthandoff: 01/04/2019

---

# <a name="info-codes-and-info-code-groups"></a>信息代码和信息代码组

[!include [banner](includes/banner.md)]

本文提供有关信息代码、信息代码组以及如何使用它们的概览。

信息代码为您提供一个在销售终端 (POS) 收银机捕获数据的方法。 您可以使用此信息代码提示出纳在各种 POS 操作（例如物料销售，物料退还或选择客户）期间输入信息。 出纳可以从列表中选择输入或输入代码、数字、日期或文本。 您可以将信息代码分配给预定义的商店操作、零售物料、付款方式、客户或特定的销售终端活动。 您可以使用信息代码进行以下操作：

- 在交易记录时间捕获附加信息，例如航班号或退货原因。
- 提示暂存器出纳从特定产品的价格列表中选择。
- 执行特定活动时，将子代码链接到信息代码以提示出纳输入。 例如，当客户退回产品时，您可以提示出纳该产品被退回的原因。 然后您可以使用子代码显示出纳可以从中选择的原因列表。
- 销售的产品为常规销售、折扣销售或免费产品。
- 当出纳代在未执行销售操作时打开暂存器抽屉时，提示出纳输入值或从子代码列表中选择。

## <a name="info-codes-group"></a>信息代码组

在 Dynamics 365 for Retail 中，可以创建信息代码组。 信息代码组通过允许您定义少数的信息代码来增加灵活性，然后以更多样化的方式使用它们。 您可以通过以下方式使用信息代码组：

- 定义少数信息代码，轻松重复使用。 信息代码组中包括的信息代码没有预定义依赖其他信息代码。 多个信息代码组可以包含相同的信息代码，然后使用优先级按照在任意情形下都有效的顺序为相同的信息代码排序。
- 将信息代码链接到其他信息代码或信息代码组以收集关于产品或交易的信息，而无需为每个场景定义单独的信息代码或链接的信息代码。

## <a name="info-code-examples"></a>信息代码示例

**示例 1：重复使用信息代码**

您可以链接信息代码，以便在一个信息代码被触发时，另一个信息代码也在之后被立即触发。 例如，在您销售某些产品时，您可以提示出纳询问客户是否需要购买电池和产品担保。 在您销售其他产品时，您可以提示出纳询问客户是否需要购买电池，并收集客户的邮政编码。 如果您为这些场景创建链接了的信息代码，必须设置信息代码的每个变量，以便提示出纳索要正确的信息。 如果您使用信息代码组、常用信息代码，例如请求电池，可以设置一次，然后在多个信息代码组中重复使用。 您也可以在信息代码组中使用优先级标识显示提示的顺序。

**示例 2：将信息代码链接到信息代码组**

在您销售特定产品时，例如移动设备，总想收集一组特定信息，比如电话号码、移动设备标识 (MEID) 和序列号。 但是您还想收集平板电脑与移动电话的区别。 您可以设置包括提示电话号码、MEID 和序列号的信息代码组，然后将信息代码组链接到单个信息代码。 在产品特殊化信息代码被触发后，接下来会触发信息代码组以使您能够收集常用数据，而不必为每台设备定义多个链接信息代码集。

