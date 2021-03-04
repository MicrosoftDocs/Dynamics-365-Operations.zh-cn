---
title: 通过安全角色访问专用地址
description: 本文说明如何解决客户无法访问专用地址的问题。
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: fbe0e8acc1b879e4d7982b33413236432f25f630
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4417434"
---
# <a name="access-to-private-addresses-by-security-role"></a>通过安全角色访问专用地址

**发货**

在客户复制安全角色并以该新角色登录后，该客户无法看到标记为专用的地址。

**分辨率**

为了解决此问题，客户必须对复制的安全角色执行以下步骤。

1. 转到 **组织管理 \> 全球通讯簿 \> 全球通讯簿参数**。
2. 在 **专用位置安全** 选项卡上，将新安全角色从 **可用角色** 列表移到 **选定角色** 列表。
3. 选择 **保存**。

![全球通讯簿参数页面](media/GAD-parameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]