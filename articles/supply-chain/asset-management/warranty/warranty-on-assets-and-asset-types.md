---
title: 资产和资产类型的保修
description: 本主题介绍如何在资产管理中为资产和资产类型设置保修。
author: josaw1
manager: AnnBe
ms.date: 08/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3b13f8aba7e1d2448495f97a4772eb573e08c025
ms.sourcegitcommit: 802dbf0a744d70f9e546632d419415b0993331ab
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/13/2019
ms.locfileid: "1874593"
---
# <a name="warranty-on-assets-and-asset-types"></a>资产和资产类型的保修

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


本主题介绍如何在资产管理中为资产和资产类型设置保修。

## <a name="set-up-a-warranty-on-an-asset-type"></a>为资产类型设置保修

1. 选择**资产管理** \> **设置** \> **资产类型** \> **资产类型**。
2. 在左窗格中，选择要为其附加供应商保修协议的资产类型，然后选择**资产类型默认**。
3. 在**常规**快速选项卡的**供应商保修**字段中，选择协议。

## <a name="set-up-a-warranty-on-an-asset"></a>为资产设置保修

1. 选择**资产管理** \> **常用** \> **资产** \> **所有资产**。
2. 选择资产，然后选择**编辑**。
3. 在**供应商**快速选项卡**供应商保修**部分中的**保修**字段中，选择保修协议。
4. 在**保修开始日期**和**保修结束日期**字段中，选择开始日期和结束日期。

    > [!IMPORTANT]
    > 如果在一个工作订单的**保修开始日期**字段中选择了日期，该工作订单的保修将从该日期开始生效。 创建工作订单时，将把**保修开始日期**字段自动设置为创建日期。 但是，可更改此日期，以使其与保修协议开始日期之类对应。
    >
    > ![图 1](media/02-warranty.png)

> [!NOTE]
> 为供应商保修涵盖的资产创建工作订单时，如果该工作订单的预期开始日期在保修期内，您将收到有关保修协议的通知。 然后可根据需要取消该工作订单。