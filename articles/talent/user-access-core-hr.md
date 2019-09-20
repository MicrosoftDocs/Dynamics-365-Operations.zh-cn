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
ms.openlocfilehash: 6fc27a4c137fef2f8d204d90366c316389da08e6
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/12/2019
ms.locfileid: "1741701"
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

有关信息，请参阅[配置 Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent) 中的“授予对环境的访问权限”部分。

**长期解决方案**

Microsoft 正在考虑当用户被添加到 Core HR 时自动向 Onboard 和 Attract 分配相应权限。
