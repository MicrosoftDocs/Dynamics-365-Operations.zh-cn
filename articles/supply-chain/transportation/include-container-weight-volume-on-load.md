---
title: 包括容器重量和负荷的体积
description: 此主题描述如何设置和应用要包括容器重量和负荷的体积的功能。
author: Henrikan
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSRateRouteWorkbench, TMSDriverLogListPage, TMSTransportationTender
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 52b42bd0b97564a493a50331d1424ca8084b389b29518f012f443d9cf722efe7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6763907"
---
# <a name="include-container-weight-and-volume-on-load"></a>包括容器重量和负荷的体积

[!include [banner](../includes/banner.md)]

用于包括容器重量和负荷的体积的功能明确表示容器的总重量和体积以及进入负荷的物料。

负荷包含单个或多个装运，这些装运包含属于单个或多个销售订单的独特物料。 这些物料存储在容器中，且容器加载在负荷上。 位于容器外的物料也可以成为负荷的一部分。 基于这些条件，系统通过考虑容器和物料的重量和体积来计算负荷上的重量和体积的值。

如果计算的值不准确，您可以通过输入负荷上的重量和体积的实际值来进行调整。 重量和体积的值在运输管理流程中使用。 例如，这些值在费率路线工作台中使用，帮助定义负荷的费率和路线，且用于运输支付方式和驾驶员签入。

## <a name="where-it-applies"></a>适用情况

用于包括容器重量和负荷的体积的功能在运输管理流程中应用，如费率路线工作台、运输支付方式和驾驶员签入。

## <a name="how-it-is-set-up"></a>如何设置

应为负荷考虑的容器的数量基于容器的重量和体积以及使用的容器的百分比进行计算。

-   若要设置容器的重量和体积，请单击 **仓库管理** \> **设置** \> **容器** \> **容器类型**。

-   若要设置容器利用率百分比，请单击 **仓库管理** \> **设置** \> **容器** \> **容器组**，然后在 **容器利用率百分比** 字段中输入一个值。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]