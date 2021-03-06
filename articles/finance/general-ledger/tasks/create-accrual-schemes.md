---
title: 创建应计方案
description: 本主题说明如何创建应计方案。
author: aprilolson
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerAccrualTable
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 41ea75b5c54f43efd4d5b9ef194e6394fc50bccc
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815132"
---
# <a name="create-accrual-schemes"></a>创建应计方案

[!include [banner](../../includes/banner.md)]

本主题说明如何创建应计方案。 此任务使用 USMF 公司演示。

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