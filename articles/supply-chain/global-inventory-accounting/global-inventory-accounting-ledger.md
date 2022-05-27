---
title: 全球库存核算分类帐
description: 本主题介绍了全球库存核算分类帐，这些分类帐由货币、日历、惯例以及与法人的关联的组合定义。
author: JennySong-SH
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: f5f610fa51fce18ecefbf96892b56b05208c666c
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/03/2022
ms.locfileid: "8676066"
---
# <a name="global-inventory-accounting-ledger"></a>全球库存核算分类帐

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!--KFM: Preview until 4/30/2022 -->

全球库存核算具有自己的一组分类帐。 每次为相关法人处理与库存相关的交易时，系统都可以根据需要在任意数量的全球库存核算分类帐中对该交易进行核算。

分类帐是借方和贷方度量的登记。 这些度量通过使用成本元素和子分类帐科目进行分类。 全球库存核算分类帐由其货币、日历、惯例以及与法人的关联的组合定义。

若要设置您的全球库存核算分类帐，请转到 **全球库存核算 \> 设置 \> 全球库存核算分类帐**。 对于每个分类帐，设置以下字段：

- **名称** – 输入分类帐的名称。
- **描述** – 输入分类帐的描述。
- **会计日历** – 指定分类帐的会计日历。
- **货币和汇率类型** – 使用此快速选项卡上的字段选择分类帐使用的记帐币种和汇率类型。 您选择的货币可能与法人使用的货币不同。 在全球库存核算中，用户可以根据需要定义尽可能多的成本计算分类帐。 全球库存核算支持多种货币和多种估价的库存核算。 设置以下字段：

    - **货币** – 选择用于维护与库存相关的值的成本计算货币。 这些值包括库存价值、所售货物成本、在途库存和各种差异。
    - **汇率类型** – 选择系统应用于以交易货币和物料的标准成本将交易金额转换为成本计算货币的汇率。

- **惯例名称** – 指定惯例。 惯例是一系列策略，用于确定如何在此分类帐中核算成本。
- **法人** – 分类帐将对过帐到选定法人的单据进行核算。
- **启动** – 选择是否应根据分类帐中的货币和惯例处理在创建分类帐之前创建的库存交易。 选择以下值之一：

    - **已启用** – 分类帐应处理在创建分类帐之前创建的交易。
    - **已停用** – 分类帐应仅处理在创建分类帐之后创建的交易。

    > [!IMPORTANT]
    > 在输入新单据后，您将 **无法** 返回并设置此字段。

- **状态** – 系统自动将新创建的分类帐状态设置为 *准备*。
