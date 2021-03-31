---
title: 建议固定资产购置
description: 本主题介绍如何使用固定资产日记帐中的购置方案购置固定资产。
author: saraschi2
manager: AnnBe
ms.date: 07/27/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 426a5e42c1fc26958ab37eddd915334f8b0e19cc
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5205020"
---
# <a name="propose-fixed-asset-acquisitions"></a>建议固定资产购置

[!include [banner](../../includes/banner.md)]

本主题介绍如何使用固定资产日记帐中的购置方案购置固定资产。 它为 USMF 法人实体使用会计角色和演示数据。 要通过固定资产建议日记帐获取固定资产，必须首先创建固定资产记录，然后在资产帐簿中定义购置价格。

1. 在导航窗格中，转到 **模块 > 固定资产 > 日记帐条目 > 固定资产日记帐**。
2. 选择 **新建**。
3. 在 **名称** 字段中，输入或选择一个值。
4. 在操作窗格中，选择 **行**。
5. 选择 **方案**。
6. 选择 **购置方案**。
7. 选择 **筛选器**。 选择 **重置** 以清除先前值。
8. 选择 **固定资产编号** 行。
9. 在 **标准** 字段中，输入或选择一个值。 为您想要以此方案购置的固定资产设置其他条件。  
10. 选择 **确定** 两次退出窗格。
- 验证已创建的交易记录行。  
- 只有在帐簿中设置了购置日期和购置价格的固定资产才会包含在购置方案中。  
11. 在页面上，选择 **帐簿** 选项卡。
12. 选择 **过帐**。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]