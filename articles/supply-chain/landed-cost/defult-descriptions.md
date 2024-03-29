---
title: 总帐的默认描述
description: 可以使用默认描述将凭证过帐中的“描述”字段更新为总帐。
author: Weijiesa
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TransactionTexts
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 7020c39dd599be047e07caa391d6d4c69c426328
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8889539"
---
# <a name="default-descriptions-for-the-general-ledger"></a>总帐的默认描述

[!include [banner](../../includes/banner.md)]

可以使用默认描述将凭证过帐中的 **描述** 字段更新为总帐。 此功能已得到增强，可以处理登陆成本。

要设置分类帐过帐的默认描述，请转到 **组织管理 \> 设置 \> 默认描述**。

下表列出了为支持登陆成本在 **默认描述** 页上为 **描述** 字段添加的新值。

| 描述类型 | 说明 |
|---|---|
| 进口成本计算 – 成本应计 | 过帐采购订单发票时，将处理估计航行成本的成本应计。 可以将默认描述指定为将航行编号添加到描述中。 使用 *%4* 作为装运编号。 |
| 进口成本计算 – 在途货物订单 | 如果您使用的是在途处理，采购订单发票将过帐，货物将过帐到在途货物帐户。 可以将默认描述指定为将在途订单编号添加到描述中。 使用 *%4* 作为在途订单编号。 |
| 库存 – 结转 – 调整 | 为航行成本处理应付帐款 (AP) 发票时，将处理库存调整以估计航行成本。 可以将默认描述指定为将航行编号添加到描述中。 使用 *%4* 作为装运编号。 |

有关如何使用 **默认描述** 页的详细信息，请参阅[设置自动过帐的默认描述](../../finance/general-ledger/set-up-default-descriptions-for-automatic-posting.md)。
