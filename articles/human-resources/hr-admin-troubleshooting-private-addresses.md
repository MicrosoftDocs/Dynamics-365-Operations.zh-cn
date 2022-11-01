---
title: 通过安全角色访问专用地址
description: 本文说明如何解决客户无法访问专用地址这一问题。
author: twheeloc
ms.date: 09/13/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7c1db052937b03817f22b37c50b9f1b319579cb2
ms.sourcegitcommit: 27ce4fc706100b626b81c3a1023238acd872e76c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/20/2022
ms.locfileid: "9702095"
---
# <a name="access-to-private-addresses-by-security-role"></a>通过安全角色访问专用地址


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**发货**

在客户复制安全角色并以该新角色登录后，该客户无法看到标记为专用的地址。

**分辨率**

为了解决此问题，客户必须对复制的安全角色执行以下步骤。

1. 转到 **组织管理 \> 全球通讯簿 \> 全球通讯簿参数**。
2. 在 **专用位置安全** 选项卡上，将新安全角色从 **可用角色** 列表移到 **选定角色** 列表。
3. 选择 **保存**。

![全球通讯簿参数页面。](media/GAD-parameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
