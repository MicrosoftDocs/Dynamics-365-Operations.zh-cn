---
title: 设置服务间隔
description: 服务间隔指示在您创建服务订单时为服务协议行创建服务订单行所采用的频率。
author: ShylaThompson
manager: AnnBe
ms.date: 02/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementinterval
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9203b01f578779d45d63c18d1c1afd2fe59125b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "365814"
---
# <a name="set-up-service-intervals"></a>设置服务间隔  

[!include [banner](../includes/banner.md)]

服务间隔指示在您创建服务订单时为服务协议行创建服务订单行所采用的频率。

1. 单击**服务管理** \> **设置** \> **服务协议** \> **服务间隔**。
2. 创建新的服务间隔。
3. 输入 ID 和服务间隔的描述。
4. 在**范围**字段中，选择范围。
5. 在**频率**字段中，输入频率。 必须将该频率作为系数与范围相乘，以获取服务协议间隔。
6. 按 **Alt+S** 保存服务间隔。

## <a name="example"></a>示例

您要创建为期 10 天的服务间隔。

**创建 10 天的服务间隔**

1. 单击**服务管理** \> **设置** \> **服务协议** \> **服务间隔**。
2. 创建新的服务间隔。
3. 输入 ID 和服务间隔的描述。
4. 在**范围**字段中，选择**每天**。
5. 在**频率**字段中键入 10。
6. 按 **Alt+S** 保存服务间隔。

## <a name="related-topics"></a>相关主题

[服务间隔](service-intervals.md)  
