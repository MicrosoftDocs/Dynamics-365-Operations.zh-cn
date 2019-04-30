---
title: 用户可以访问 Core HR，但无法访问 Onboard 或 Attract 应用
description: 此主题介绍如何解决用户可以访问 Microsoft Dynamics 365 for Talent Core HR 但无法访问 Attract 或 Onboard 应用的问题。
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: ece6a81c54ef1421284fc79ab82ed3e31a972255
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/19/2019
ms.locfileid: "855648"
---
# <a name="user-can-access-core-hr-but-not-the-onboard-or-attract-app"></a>用户可以访问 Core HR，但无法访问 Onboard 或 Attract 应用

[!include [banner](includes/banner.md)]

**环境详细信息**

- Microsoft Dynamics Lifecycle Services (LCS) 部署由用户 A 完成。
- 用户 A 将用户 B 作为用户添加到 Microsoft Dynamics 365 for Talent Core HR。

**发货**

用户 B 可以访问 Core HR，但无法访问 Talent: Attract 或 Talent: Onboard 应用。 在用户尝试转到**体验应用**时，用户被带入试用环境。

**解决方案**

用户 B 必须在设置过程被分配查看用户 A 创建的 Microsoft PowerApps 环境的权限。

有关信息，请参阅[配置 Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent) 中的“授予对环境的访问权限”部分。

**长期解决方案**

Microsoft 正在考虑当用户被添加到 Core HR 时自动向 Onboard 和 Attract 分配相应权限。
