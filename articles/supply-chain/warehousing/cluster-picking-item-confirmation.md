---
title: 用于群集领料的产品确认
description: 此主题描述如何设置物料验证和群集领料。
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFAutoConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 272c3a13b68e2b862faf20cc269ca790322b61de
ms.sourcegitcommit: 89022f39502b19c24c0997ae3a01a64b93280f42
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/12/2020
ms.locfileid: "3367284"
---
# <a name="product-confirmation-for-cluster-picking"></a>用于群集领料的产品确认

[!include [banner](../includes/banner.md)]

群集领料让您能够同时领取多个订单的物料。 应用群集领料时，物料确认是验证添加到群集的物料的关键。 您可以在群集领料流程中验证群集领料中的物料。

## <a name="where-it-applies"></a>适用情况

群集领料物料验证与您在非群集领料流程中验证物料的工作方式相同。 设置基于产品条码设置。

## <a name="set-up-item-verification-with-cluster-picking"></a>设置群集领料的物料验证

1. 在移动设备菜单项上，打开工作确认的设置窗体：**仓库管理** > **仓库管理** > **设置** > **移动设备** > **移动设备菜单项**。
1. 从移动设备菜单项打开**工作确认设置**。

|        选项        |                                    说明                                    |
|----------------------|-----------------------------------------------------------------------------------|
| 产品确认 | 允许您在扫描时从移动设备验证每件库存。 |
