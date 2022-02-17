---
title: 集成的分类帐
description: 本主题介绍使用 Dataverse 在 Finance and Operations 与其他 Dynamics 365 应用程序之间的分类帐数据的集成。
author: tonyafehr
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: tfehr
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 0deb4198acb59b90bf06e4050889d028df2223e3
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/31/2022
ms.locfileid: "8063639"
---
# <a name="integrated-ledger"></a>集成的分类帐

[!include [banner](../../includes/banner.md)]



在业务应用程序中，分类帐数据定义公司如何开展业务的核心设置。 例如，分类帐数据描述公司遵循的会计年度、交易所用的货币以及所使用的帐户。 本主题介绍此核心财务数据的集成。

## <a name="templates"></a>模板

分类帐数据包括核心财务表映射的集合，这些映射在数据交互期间协同工作，如下表所示。

Finance and Operations 应用 | 客户互动应用     | 说明
---------------------------------|----------------------------------|------------
[CDS 汇率](mapping-reference.md#123) | msdyn_currencyexchangerates |
[会计帐户表](mapping-reference.md#121) | msdyn_chartofaccountses |
[币种](mapping-reference.md#218) | transactioncurrencies |
[汇率币种对](mapping-reference.md#122) | msdyn_currencyexchangeratepairs |
[汇率类型](mapping-reference.md#129) | msdyn_exchangeratetypes |
[财务维度格式](mapping-reference.md#130) | msdyn_financialdimensionformats |
[财务维度](mapping-reference.md#128) | msdyn_dimensionattributes |
[会计日历集成实体](mapping-reference.md#132) | msdyn_fiscalcalendars |
[会计日历期间](mapping-reference.md#131) | msdyn_fiscalcalendarperiods |
[会计日历年度集成实体](mapping-reference.md#133) | msdyn_fiscalcalendaryears |
[总帐](mapping-reference.md#148) | msdyn_ledgers |
[主帐户](mapping-reference.md#152) | msdyn_mainaccounts |
[主帐户类别](mapping-reference.md#151) | msdyn_mainaccountcategories |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
