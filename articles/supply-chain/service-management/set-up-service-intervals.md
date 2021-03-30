---
title: 设置服务间隔
description: 服务间隔指示在您创建服务订单时为服务协议行创建服务订单行所采用的频率。
author: ShylaThompson
manager: tfehr
ms.date: 02/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementinterval
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: aee440226c4bda40f9f14b3b6b1edc2cc495574d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5242461"
---
# <a name="set-up-service-intervals"></a>设置服务间隔  

[!include [banner](../includes/banner.md)]

服务间隔指示在您创建服务订单时为服务协议行创建服务订单行所采用的频率。

1. 单击 **服务管理** \> **设置** \> **服务协议** \> **服务间隔**。
2. 创建新的服务间隔。
3. 输入 ID 和服务间隔的描述。
4. 在 **范围** 字段中，选择范围。
5. 在 **频率** 字段中，输入频率。 必须将该频率作为系数与范围相乘，以获取服务协议间隔。
6. 按 **Alt+S** 保存服务间隔。

## <a name="example"></a>示例

您要创建为期 10 天的服务间隔。

**创建 10 天的服务间隔**

1. 单击 **服务管理** \> **设置** \> **服务协议** \> **服务间隔**。
2. 创建新的服务间隔。
3. 输入 ID 和服务间隔的描述。
4. 在 **范围** 字段中，选择 **每天**。
5. 在 **频率** 字段中键入 10。
6. 按 **Alt+S** 保存服务间隔。

## <a name="related-topics"></a>相关主题

[服务间隔](service-intervals.md)  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]