---
title: 解决 Store Commerce 性能问题
description: 本文介绍如何解决 Microsoft Dynamics 365 Commerce Store Commerce 应用中的性能问题。
author: mugunthanm
ms.date: 06/01/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2022-05-12
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: fef4eb7063f4acdbca5fab2ad33ec10e0cb603bd
ms.sourcegitcommit: c271b2edc4bf777f7194b09139ccbd174a359c75
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/16/2022
ms.locfileid: "9169036"
---
# <a name="troubleshoot-store-commerce-performance-issues"></a>解决 Store Commerce 性能问题

[!include [banner](../includes/banner.md)]

本文介绍如何解决 Microsoft Dynamics 365 Commerce Store Commerce 应用中的性能问题。

- 解决 Store Commerce 的性能问题时，请避免远程登录。 而是直接登录到 Store Commerce 设备。
- 如果 Store Commerce 应用速度较慢，请使用任务管理器或资源监视器检查 CPU、内存、网络和磁盘使用情况。 确保设备资源没有出现大量消耗。
- 检查您的网络连接状态，并确认 HTTPS 请求/响应不会花费超过几秒钟的时间。
