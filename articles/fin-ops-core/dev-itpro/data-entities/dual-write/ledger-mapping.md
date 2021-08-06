---
title: 集成的分类帐
description: 本主题介绍使用 Dataverse 在 Finance and Operations 与其他 Dynamics 365 应用程序之间的分类帐数据的集成。
author: robinarh
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: rhaertle
ms.openlocfilehash: 9e6e65b2b8ec8241bc2082b30ae641692c31afdd
ms.sourcegitcommit: f65bde9ab0bf4c12a3250e7c9b2abb1555cd7931
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/13/2021
ms.locfileid: "6542653"
---
# <a name="integrated-ledger"></a>集成的分类帐

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

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
