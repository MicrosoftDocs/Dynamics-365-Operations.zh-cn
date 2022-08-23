---
title: 启用全球预缴税金币种汇率类型和日期类型设置
description: 本文介绍如何启用预缴税金币种汇率类型和日期类型的全局设置。
author: kailiang
ms.date: 08/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 41f12a33651c14439f3a59c5c2f2d34019dada2d
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/06/2022
ms.locfileid: "9229951"
---
# <a name="enable-the-global-withholding-tax-currency-exchange-rate-type-and-date-type-setup"></a>启用全球预缴税金币种汇率类型和日期类型设置

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

本文介绍如何启用预缴税金币种汇率类型和日期类型的全局设置。 现在，您可以为预缴税金币种选择专门的汇率类型和汇率计算日期类型。 这些选择确定用于计算付款交易中的预缴税金金额（以预缴税金币种表示）的外币汇率。

Microsoft Dynamics 365 Finance 版本 10.0.29 及更高版本中提供此功能。

1. 转到 **纳税** \> **设置** \> **参数** \> **总帐参数**。
2. 在 **预缴税金** 选项卡上，将 **启用预缴税金币种** 选项设置为 **是**。
3. 在 **汇率类型** 字段中，为预缴税金币种选择汇率类型。
4. 在 **计算日期类型** 字段中，选择确定预缴税金币种汇率的计算日期类型：

    - **付款日期** - 根据付款日记帐的过帐日期确定汇率。
    - **发票日期** - 根据发票日记帐的发票日期确定汇率。 如果凭证的发票日期为空白，则将使用发票过帐日期。 
    - **单据日期** - 根据付款日记帐的单据日期确定汇率。 如果凭证的单据日期为空白，则将使用付款日期。

5. 选择 **保存**。

如果交易币种不同于预缴税金代码中定义的预缴税金币种，则将根据先前的设置利用交易币种计算以预缴税金币种为单位的金额，并将其记录在已过帐的预缴税金交易记录中。
