---
title: 设置服务间隔
description: 此主题描述如何设置服务间隔。 服务间隔指示在您创建服务订单时为服务协议行创建服务订单行所采用的频率。
author: sorenva
ms.date: 02/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAAgreementinterval
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 943ed0b8f329b45225b61247998e15a1d82356aa
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/03/2022
ms.locfileid: "8673429"
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