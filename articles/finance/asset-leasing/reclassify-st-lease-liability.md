---
title: 重新分类租赁负债的短期部分
description: 本主题说明如何创建月度日记帐条目以将部分租赁负债重新分类为短期租赁。
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 3a71b809b4bb16c2b918b7acd4fbb8bc49278ff6
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/07/2022
ms.locfileid: "8727725"
---
# <a name="reclassify-the-short-term-portion-of-lease-liability"></a>重新分类租赁负债的短期部分

[!include [banner](../includes/banner.md)]

本主题说明如何创建月度日记帐条目以将部分租赁负债重新分类为短期租赁。 当在批处理过程中选择的计划是 **短期租赁负债重新分类** 时，将创建日记帐条目。 该条目用于在当月的最后一天过帐租赁负债的当前部分。 同时，从下个月的第一天开始过帐冲销条目。

负债摊销计划中将显示租赁负债的短期部分。 过帐日记帐条目过帐后，**已创建的负债重分类日记帐** 列变为可用，并且也在计划中填写了日记帐 ID。

要创建并过帐短期负债重新分类日记帐条目，请按照下列步骤操作。

1. 转到 **资产租赁 \> 定期 \> 批量日记帐创建**。
2. 在 **批量日记帐创建** 对话框的 **选择计划** 字段中，选择 **短期租赁负债重新分类**。
3. 在 **租赁组** 字段中，选择租赁组。 或者，在 **帐簿** 字段中，选择帐簿 ID。
4. 打开 **过帐** 参数。 或者，如果应创建但不过帐条目，请关闭此参数。
5. 选择 **确定**。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
