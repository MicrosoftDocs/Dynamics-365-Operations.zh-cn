---
title: Finance and Operations 应用和 Common Data Service 的初始同步执行顺序
description: 本主题指定创建初始数据时必须遵守的同步顺序。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: cf444ef1192fed3a6a49282da37374dd8c443356
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769629"
---
# <a name="execution-order-for-initial-synchronization-of-finance-and-operations-apps-and-common-data-service"></a>Finance and Operations 应用和 Common Data Service 的初始同步执行顺序

[!include [banner](../includes/banner.md)]

使用数据集成之前，必须创建客户、供应商和联系人所需的初始数据。 例如，希望创建新的**供应商组**项，然后将其**付款期限**值设置为 **Net30**。 在此情况下，尝试创建**供应商组**项之前，必须确保应用程序和 Common Data Service 中都有 **Net30**。 （将来，Microsoft 将发布双写入平台功能，称为“初始同步”。该功能将在执行双写入设置期间执行应用程序与 Common Data Service 之间的一次性数据同步。）

> [!TIP]
> Microsoft 将为所有引用数据（包括**付款期限**）发布双写入映射。 如果一个系统中已经有初始数据，对记录执行的小型更新操作可对该记录触发双写入。

必须遵守以下过程顺序，并确保此应用程序和 Common Data Service 中均有初始数据。

## <a name="vendor"></a>供应商

下面是**供应商**实体的执行顺序：

1. 供应商组

    1. 付款期限

        1. 付款日和行
        2. 付款计划

2. 供应商付款方式

## <a name="customer-organization"></a>客户（组织）

下面是**客户**实体的执行顺序：

1. 客户组

    1. 付款期限

        1. 付款日和行
        2. 付款 

2. 客户付款方式

## <a name="contact-person"></a>联系人（个人）

下面是**联系人**实体的执行顺序：

1. 客户
2. 供应商
