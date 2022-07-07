---
title: 将地址添加到服务订单
description: 本文描述如何将客户地址添加到服务订单。
author: sorenva
ms.date: 06/15/2020
ms.topic: article
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c485c50bab7c2e945aa0f0fc0601008dcebd3328
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015716"
---
# <a name="add-an-address-to-a-service-order"></a>将地址添加到服务订单

[!include [banner](../includes/banner.md)]

本文描述如何将客户地址添加到服务订单。 在您创建某一服务订单时，地址信息将从该服务订单附加到的项目转移。 但是，您可以从已在 Microsoft Dynamics AX 中输入的客户、供应商、站点、仓库、服务订单和项目的地址，选择备选位置。

您还可以创建新地址。 默认情况下，将新地址转移到项目。 但是，您可以指定新地址仅与该服务实例相关。 如果您执行此操作，则新地址不会转移到项目。

## <a name="create-a-customer-address-for-a-service-order"></a>为服务订单创建客户地址

若要添加地址到销售订单，请执行以下步骤：

1. 转到 **服务管理** \> **服务订单** \> **服务订单**。

1. 打开想要为其创建地址的服务订单。

1. 打开 **标头** 选项卡。

1. 展开 **地址** 快速选项卡，然后从快速选项卡工具栏中选择 **添加地址**。

1. 在 **新地址** 对话框中，输入地址的唯一名称并完成其余的字段。 

    > [!WARNING]
    > 如果输入与现有地址相同的名称，则您在剩余字段中输入的信息将覆盖现有地址信息。

1. 选择 **确定** 以将新地址复制到您的服务订单中。

## <a name="specify-an-alternative-address-on-a-service-order"></a>在服务订单上指定备选地址

若要将备选地址添加到服务订单，请执行以下步骤：

1. 转到 **服务管理** \> **服务订单** \> **服务订单**。

1. 打开您想要为其输入备选地址的服务订单。

1. 打开 **标头** 选项卡。

1. 展开 **地址** 快速选项卡，然后从快速选项卡工具栏中选择 **其他地址**。

1. 在 **地址选择** 对话框中，从网格上方的下拉列表中选择 **服务订单**。

1. 选择地址，然后选择 **确定** 以将其复制到您的服务订单中。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]