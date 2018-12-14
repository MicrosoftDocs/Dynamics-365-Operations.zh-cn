---
title: "用户可以访问 Core HR，但无法访问 Onboard 或 Attract 应用"
description: "此主题介绍如何解决用户可以访问 Microsoft Dynamics 365 for Talent Core HR 但无法访问 Attract 或 Onboard 应用的问题。"
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 2e5d0b1bf993aec89c7d2c6d4916732f5824310d
ms.contentlocale: zh-cn
ms.lasthandoff: 12/04/2018

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

