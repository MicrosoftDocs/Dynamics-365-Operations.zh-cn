---
title: 阈值限制和异常阈值限制
description: 本主题介绍了从源扣缴税款 (TDS) 的阈值和异常限制。
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 7fa7d871fdf25f29b003a68cacd9fc0d487dce5b
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/07/2022
ms.locfileid: "8726007"
---
# <a name="threshold-limit-and-exception-threshold-limit"></a>阈值限制和异常阈值限制

[!include [banner](../includes/banner.md)]

本主题介绍了从源扣缴税款 (TDS) 的阈值和异常限制。 在针对发票和付款计算 TDS 时，始终考虑在 **预缴税金组分** 页面上为 TDS 税种组分定义的阈值限制和异常阈值限制。 TDS 税种组分附加到包括在 TDS 税组中的 TDS 税码。 TDS 税组附加到供应商和客户，以在发票级别或付款级别计算 TDS。

如果通过供应商的特定 TDS 组过帐的交易或累计交易的金额超过在 **预缴税金组分** 页面上指定的阈值限制，将计算 TDS。 在累计交易金额超过指定的阈值限制之前，不会计算 TDS。

如果同时指定了异常阈值限制和 TDS 组分的阈值限制，当特定交易金额超过异常阈值限制时，即使累计交易金额未超过指定的阈值限制，也会计算 TDS。

### <a name="example"></a>示例
称为 TDS 的税种组分将设置并附加到称为合同工的 TDS 税组。 对于 TDS 税种组分，阈值已定义为 50,000，异常阈值已定义为 20,000。 对于供应商 1，TDS 组合同工将定义为默认的 TDS 组。

对于供应商 1，将为 10000 过帐采购发票 001。 不计算发票的 TDS，因为发票金额未超过阈值限制或异常阈值限制。 对于供应商 1，将为 25,000 过帐采购发票 002。 计算发票的 TDS，因为发票金额已超过异常阈值限制。 对于供应商 1，将为 20,000 过帐采购发票 003。 计算发票的 TDS，因为为供应商签发的三个发票的发票总金额已超过阈值限制。 根据为供应商签发的之前尚未计算 TDS 的所有发票计算 TDS。 因此，根据 30,000 计算 TDS，这是发票 001 和 003 的发票总金额。

如果对于附加到交易的 TDS 组中的 TDS 税码选中 **忽略阈值** 复选框，则在计算 TDS 时不考虑阈值限制和异常阈值限制。 将不在选中了 **忽略阈值** 复选框的 TDS 组的 TDS 税码中使用异常限制。

如果针对某些发票的特定 TDS 组，但不针对已为特定供应商/客户创建的其他发票选中 **忽略阈值** 复选框，考虑到之前尚未计算 TDS 的所有发票的累计金额，可能会在不忽略少数发票的阈值限制的情况下计算 TDS。

例如，阈值限制为 25000。 为供应商 A 创建以下发票。

- 发票 1 – 2,0000 –（未选中 **忽略阈值** 复选框）：不计算 TDS。

- 发票 2 – 4,000 –（选中 **忽略阈值** 复选框）：根据 4,000 计算 TDS。

- 发票 2 – 3,000 –（未选中 **忽略阈值**）：当累计发票金额 27,000 (20000+4000+3000) 超过阈值限制时计算 TDS。 针对之前尚未计算 TDS 的累计发票金额 23,000 (20000+3000) 计算 TDS。
