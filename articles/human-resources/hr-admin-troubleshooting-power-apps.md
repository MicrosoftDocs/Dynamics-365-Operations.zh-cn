---
title: 无法在 Power Apps 管理中心内创建环境
description: 本文说明如果管理员无法在 Microsoft Power Apps 管理中心创建环境该做什么。
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 26a228229a09e74809a048675a3ff90025f2a26c
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/13/2021
ms.locfileid: "5892219"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a>无法在 Power Apps 管理中心内创建环境

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**发货**

- 租户/环境管理员无法在 Microsoft Power Apps 管理中心创建环境。
- 用户没有授予创建环境权限的许可证。

**解决方案**

确保租户管理员已向创建环境的用户分配了有效的 Power Apps P2 许可证。 以下 Microsoft Dynamics 服务计划提供创建环境的权限：

| 整个产品库存单位 (SKU)       | Power Apps P2 服务计划  |
|------------------------------------------------|----------------------------|
| Microsoft Dynamics 365 for Operations          | Power Apps for Dynamics 365 |
| Microsoft Dynamics 365 计划 Enterprise Edition | Power Apps for Dynamics 365 |

请注意，各个 Microsoft Office SKU 也提供权限，以及独立的 Power Apps 计划 2 SKU。 重点是这些 SKU 中的一个必须存在。

1. 转到 [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments)。
2. 按照[配置 Human Resources](/dynamics365/unified-operations/talent/provisioning-talent) 中的说明创建环境。


[!INCLUDE[footer-include](../includes/footer-banner.md)]