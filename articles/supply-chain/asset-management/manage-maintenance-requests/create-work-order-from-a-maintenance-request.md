---
title: 根据维护请求创建工作订单
description: 本主题说明如何在资产管理中根据维护请求创建工作订单。
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 23039306bb827beb861eaacc3177f4917fabc8bf
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/16/2021
ms.locfileid: "5018088"
---
# <a name="create-work-orders-from-maintenance-requests"></a>根据维护请求创建工作订单

[!include [banner](../../includes/banner.md)]

 


创建了维护请求之后，可将其轻松转化为工作订单。 本主题介绍处理维护请求，同时更新多个维护请求，然后同时为多个维护请求创建一个工作订单的最快方法。 在 **有效维护请求** 或 **我的功能位置维护请求** 页，也可以一次处理一个维护请求，并将一个维护请求转化为工作订单。

> [!NOTE]
> 每个维护请求只能与一个工作订单关联。 但是，一个工作订单中可以包含多个维护请求，即使这些维护请求具有不同资产也不例外。

1. 选择 **资产管理** \> **常用** \> **维护请求** \> **所有维护请求**。
2. 必须为维护请求先至少选择一个维护作业类型，并且还选择维护作业类型变体和交易（如果此信息相关），才能基于维护请求创建工作订单。 在网格视图中，可以轻松更新维护请求的信息。
3. 准备好创建工作订单时，选择要在其中包含的维护请求。

    - 如果选择多个要转化为工作订单的维护请求，则必须先设置 **资产** 字段和 **维护作业类型** 字段，才能创建工作订单。
    - 如果选择一个要转化为工作订单的维护请求，则必须先仅设置 **资产** 字段，才能创建工作订单。 但是，创建工作订单时，可以在 **创建工作订单** 对话框中选择维护作业类型（如果此信息相关，则还需要选择关联的维护作业类型变体和交易）。

4. 选择 **工作订单**。
5. 在 **创建工作订单** 对话框中，设置字段，然后选择 **确定**。

    可能会通过消息栏通知您已创建了新工作订单。

    此外，创建基于维护请求的工作订单时，如果一个保修协议中涵盖与该维护请求关联的资产，则会通过消息栏告知您这个保修协议。

6. 选择 **资产管理** \> **常用** \> **工作订单** \> **所有工作订单**，然后打开新工作订单。

    ![打开新工作订单](media/05-manage-maintenance-requests.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]