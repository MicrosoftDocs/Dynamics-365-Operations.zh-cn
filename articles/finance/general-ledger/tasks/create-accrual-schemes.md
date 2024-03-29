---
title: 创建应计方案
description: 本文说明如何创建应计方案。
author: aprilolson
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerAccrualTable
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8974eed40a60aeee5a32932ac070a870289ec20a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8858412"
---
# <a name="create-accrual-schemes"></a>创建应计方案

[!include [banner](../../includes/banner.md)]

本文说明如何创建应计方案。 此任务使用 USMF 公司演示。

1. 转到 **导航窗格 > 模块 > 总帐 > 日记帐设置 > 应计方案**。
2. 选择 **新建**。
3. 在 **应计标识** 字段中，键入一个值。
4. 在 **应计方案的描述** 字段中，键入一个值。
5. 在 **借方** 字段中，指定所需值。 定义的主科目将替换日记帐凭证行的借方主科目，并且还用于根据分类帐的应计交易冲销延期交易。  
6. 在 **贷方** 字段中，指定所需值。 定义的主科目将替换日记帐凭证行的贷方主科目，并且还用于根据分类帐的应计交易冲销延期交易。  
7. 在 **凭证** 字段中，选择您想要在过帐交易记录时确定的凭证。
8. 在 **描述** 字段中，输入一个值来描述要过帐的交易记录。
9. 在 **期间频率** 字段中，选择交易记录的产生频率。
10. 在 **发生次数(按期间)** 字段中，输入一个数字。
11. 在 **过帐交易记录** 字段中，选择交易记录过帐的时间，如 **每月**。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
