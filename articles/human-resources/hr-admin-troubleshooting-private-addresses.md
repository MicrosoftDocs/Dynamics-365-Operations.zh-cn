---
title: 通过安全角色访问专用地址
description: 本文说明如何解决客户无法访问专用地址的问题。
author: andreabichsel
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2edcef338f0ff8fcf231d4314fc972284397d000
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053315"
---
# <a name="access-to-private-addresses-by-security-role"></a>通过安全角色访问专用地址

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**发货**

在客户复制安全角色并以该新角色登录后，该客户无法看到标记为专用的地址。

**分辨率**

为了解决此问题，客户必须对复制的安全角色执行以下步骤。

1. 转到 **组织管理 \> 全球通讯簿 \> 全球通讯簿参数**。
2. 在 **专用位置安全** 选项卡上，将新安全角色从 **可用角色** 列表移到 **选定角色** 列表。
3. 选择 **保存**。

![全球通讯簿参数页面](media/GAD-parameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]