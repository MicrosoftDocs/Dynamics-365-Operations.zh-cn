---
title: 设置指数利率
description: 本文说明如何设置指数利率。 如果您的组织将租赁付款额与一组指数利率关联，则需要指数利率。
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseIndexRateType
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e700c6c0c66b855a3e329302ac27681f4d0144a7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8883378"
---
# <a name="set-up-index-rates"></a>设置指数利率

[!include [banner](../includes/banner.md)]

如果租赁付款取决于指数，则可以在系统中添加并维护指数利率类型。 为了从 **指数利率类型** 页面重估租赁付款，指数利率重估流程使用自重估之日起的最新指数利率。

若要添加指数利率类型和指数利率，请按照下列步骤操作。

1. 转到 **资产租赁 \> 设置 \> 指数利率类型**。
2. 选择 **新建**。
3. 在相应字段中，输入指数利率的利率类型和名称。
4. 要添加新的指数利率值，请选择指数利率类型，然后选择 **添加**。
5. 选择利率的生效日期，然后选择利率值。

您必须选择 **指数利率值差** 要么 **指数利率值** 作为指数利率方法。

- 根据开始日期的指数利率与最近指数利率之间的差选择用于计算新租赁付款的 **指数利率值差** 方法。 指数利率在 **指数利率(%)** 字段中定义。
- 通过选择 **指数利率(%)** 字段中指定的百分比，选择用于计算租赁付款的 **指数利率值** 方法。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
