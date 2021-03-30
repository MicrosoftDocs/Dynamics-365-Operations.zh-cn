---
title: 销售报价单故障排除
description: 本主题介绍如何解决在使用销售报价单时可能遇到的问题。
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesQuotationTable, SalesQuotationTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 9a9cc821d2fe9accad1dae210271682cdd2ce4ba
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232198"
---
# <a name="troubleshoot-sales-quotations"></a>销售报价单故障排除

本主题介绍如何解决在使用销售报价单时可能遇到的问题。

## <a name="i-cant-change-the-sales-quantity-of-a-sales-quotation-for-a-service-item"></a>我无法更改服务物料的销售报价单的销售数量。

### <a name="issue-description"></a>问题描述

如果您尝试在销售报价单行上为 *服务* 类型的物料设置销售数量（**SalesQty** 字段），您将收到以下消息：“不允许更新“数量”字段”。

### <a name="issue-resolution"></a>解决问题

您不能为属于服务物料的产品设置销售数量。 例如，如果您提供安装物料的服务，那么记录数量是没有意义的，因为没有实际物料。 只有服务。



[!INCLUDE[footer-include](../../includes/footer-banner.md)]