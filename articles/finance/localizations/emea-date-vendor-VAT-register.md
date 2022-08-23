---
title: 供应商增值税登记簿的日期
description: 本文提供有关启用供应商增值税登记簿日期的功能的信息
author: AdamTrukawka
ms.date: 01/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: global
ms.author: atrukawk
ms.search.validFrom: 2022-01-15
ms.dyn365.ops.version: AX 10.0.24
ms.custom: intro-internal
ms.openlocfilehash: 4af770427f5b19eaf2a129b26d54aeacc6c2f148
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278269"
---
# <a name="date-of-vendor-vat-register"></a>供应商增值税登记簿的日期

在 Microsoft Dynamics 365 Finance 版本 10.0.24 中，新的 **供应商增值税登记簿日期** 字段适用于供应商发票。 此字段指定采购的应纳税供应的日期。

若要启用此新字段，请转到 **功能管理** 工作区，查找并选择 **在供应商发票上启用供应商增值税登记簿的日期** 功能，然后选择 **立即启用**。

供应商的传入发票可以有两个日期：供应商开具发票的日期和应纳税供应的日期（即供应商收取应付增值税 [VAT] 的日期）。 在某些情况下，这两个日期可能不同。

您可以扣除采购发票的进项增值税金额，并稍后在与前面提到的两个日期都不同的日期将该发票包含在增值税报告中。 此日期由关于在某些情况下推迟抵扣增值税的当地法规来控制。 它因国家或地区而异。

某些增值税报表，例如捷克共和国的[增值税控制报表](emea-cze-vat-declaration-tax-declaration-model.md#vat-control-statement)，要求针对采购单据报告应纳税供应的日期。 必须报告此日期，以便税务主管机构可以对对方之间的增值税申报进行对帐。

在 Finance 中，您可以在以下字段中定义日期：

- **发票日期** - 供应商开具发票的日期。
- **增值税登记簿的日期** - 采购发票的增值税金额扣除日期。
- **供应商增值税登记簿的日期** - 供应商的应纳税供应的日期。
- **接收单据日期** - 您收到发票的日期。

以下页面中包含这些字段：

- 供应商发票
- 供应商发票登记簿
- 供应商发票审核
- 供应商发票日记帐

在过帐供应商发票后，您可以查看 **发票日记帐** 和 **供应商交易** 页面上的日期。
