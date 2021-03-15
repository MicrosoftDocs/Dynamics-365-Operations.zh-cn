---
title: 正在接收混合牌照
description: 此主题描述如何在移动设备上使用混合牌照接收为多个物料登记和创建工作。
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFAutoConfirm, WHSLicensePlate
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c4dcafa5d997bce21d37d02f87fbf604568c24e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965622"
---
# <a name="mixed-license-plate-receiving"></a>正在接收混合牌照

[!include [banner](../includes/banner.md)]

混合牌照接收允许您在登记和创建入库工作前生成包含多个物料的牌照。 

包含多个物料的牌照不必在您登记每个物料时在收货台进行拆分。 

使用物料相关流确定原始凭证行时，您可以扫描物料控制上的条码。 如果条码上配置了一个数量和一个度量单位 (UOM)，该物料和数量将自动添加到混合牌照，且您将返回到屏幕以扫描其他物料。 这可用于快速扫描所有物料，而不必在每个步骤进行确认。 

在混合牌照接收流中，您可以显示已经扫描到牌照的物料的列表，并从此处修改或更正物料的数量。

## <a name="where-it-applies"></a>适用情况

混合牌照接收是同时为多个行/物料登记和创建工作的移动设备接收流。 这在您收到具有多个物料的传入牌照时很有用。 

## <a name="how-to-set-up-mixed-license-plate-receiving"></a>如何设置混合牌照接收
混合牌照接收设置为移动设备菜单项。

您需要创建一个使用模式工作的新菜单项，其不使用现有工作，且使用以下其中一种方法：

- 正在接收混合牌照
- 混合牌照接收和储存

用于标识原始凭证行的选项为采购订单物料、采购订单行、退货订单、转移单物料和转移单行。 这些选项可以更改对单个牌照的接收单。 最后一个选项是按加载物料。 您可以将多个物料添加到牌照，但不能在多个负荷之间切换。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]