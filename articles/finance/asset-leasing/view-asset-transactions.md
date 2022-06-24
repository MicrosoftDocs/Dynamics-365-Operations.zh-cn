---
title: 查看负债、资产和费用交易
description: 本文说明如何查看租赁资产的交易。 这些交易包括已过帐的租赁负债交易和执行费用交易。
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 552b5a6044950c4dd7547a5239c1b3f7d355dbce
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8906404"
---
# <a name="view-liability-asset-and-expense-transactions"></a>查看负债、资产和费用交易

[!include [banner](../includes/banner.md)]

本文说明如何查看租赁资产的交易。 这些交易包括已过帐的租赁负债交易和执行费用交易。 多种报表中都使用负债和使用权 (ROU) 资产的帐面价值。 还用于计算调整值。

## <a name="liability-transactions"></a>负债交易记录

要查看租赁负债交易，请在 **租赁摘要** 页上选择一个租赁，然后选择 **帐簿** 打开租赁记录的附加帐簿。 过帐初始确认、发票或利息日记帐之后，选择 **负债交易**。

**负债交易** 页显示增加或减少租赁负债的交易。 此页面上的负数表示标准应用程序中的信用证交易。 任何应计利息均显示为负值，并增加总租赁负债。 任何租赁调整均显示为正值或负值，具体取决于租赁帐簿的性质和影响。 所选租赁的租赁负债的当前总净额显示在页面的左下方。

## <a name="asset-transactions"></a>资产交易记录

要查看租赁资产交易，请在 **租赁摘要** 页上选择一个租赁，然后选择 **帐簿** 打开租赁记录的附加租赁帐簿。 然后选择 **租赁交易**。

**资产交易** 页面显示增加或减少租赁资产和累计折旧科目的交易。 借项显示为正数，贷项显示为负数，正如 **负债交易** 页上。 过帐的初始确认和下一个累计折旧在页面的左下方显示为资产余额。 

## <a name="expenses-transactions"></a>费用交易

要查看租赁费用交易，请在 **租赁摘要** 页上选择一个租赁，然后选择 **帐簿** 打开租赁记录的附加租赁帐簿。 然后选择 **费用交易**。

**费用交易** 页显示已针对租赁过帐的所有费用，例如利息费用、折旧费用和任何执行成本。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
