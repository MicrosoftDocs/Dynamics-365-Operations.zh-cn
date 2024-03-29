---
title: 服务级别和描述
description: 本文介绍资产管理中的服务级别和描述。
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetObjectServiceLevel, EntAssetWorkOrderStandardDescription, EntAssetWorkOrderServiceLevel, EntAssetServiceLevelLookup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 753ad36b1d01d1ce0594f477cf863ca0e4a1ac75
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879183"
---
# <a name="service-level-and-description"></a>服务级别和描述

[!include [banner](../../includes/banner.md)]

 

创建工作订单时，可能希望为其定义服务级别和向其添加一般描述。 可以在 **工作订单服务级别** 页上创建工作订单服务级别，在 **工作订单描述** 页上创建描述。

## <a name="create-a-service-level"></a>创建服务级别

1. 选择 **资产管理** \> **设置** \> **工作订单** \> **服务级别**。
2. 选择 **新建**。
3. 在 **服务级别** 字段中，键入服务级别（例如，一个数字）。
4. 在 **名称** 字段中输入名称。

    在 **工作订单** 快速选项卡上，可定义预计开始和结束日期和时间。 此快速选项卡上的字段定义工作订单应该的开始和结束期间。 用于手动创建的工作订单和基于维护请求创建的工作订单。 

5. 在 **开始日期** 字段中，输入天数以定义工作订单的应该开始期间。 此天数从工作订单的创建日期开始计算。 例如，如果工作订单应该在创建时开始，请输入 **0**。 如果工作订单应该在创建后一周内开始，请输入 **7**。
6. 除了开始日期，若要为工作订单再设置开始时间，请将 **设置开始时间** 选项设置为 **是**。 然后在 **开始时间** 字段中输入开始时间。 如果将此选项设置为 **否**，将使用当前时间。
7. 在 **结束日期** 字段中，输入天数以定义工作订单的应该结束期间。 此天数从工作订单的开始日期开始计算。 例如，如果工作订单应该在其开始日期后一周内结束，请输入 **7**。
8. 除了结束日期，若要为工作订单再设置结束时间，请将 **设置结束时间** 选项设置为 **是**。 然后在 **结束时间** 字段中输入结束时间。 如果将此选项设置为 **否**，将使用当前时间。
9. 选择 **保存**。

![工作订单服务级别页面。](media/19-setup-for-work-orders.png)

## <a name="create-a-description"></a>创建描述

1. 选择 **资产管理** \> **设置** \> **工作订单** \> **描述**。
2. 选择 **新建**。
3. 在 **描述** 字段中，输入描述。
4. 选择 **保存**。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]