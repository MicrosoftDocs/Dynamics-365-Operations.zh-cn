---
title: 通过安全角色访问专用地址
description: 本主题说明如何解决客户无法访问专用地址这一问题。
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0b96733946e4ef79de244730d0c442b9900426c1
ms.sourcegitcommit: 7e32e5e39e762a4b1606161cb603a450d13b5251
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/23/2021
ms.locfileid: "7413331"
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

![全球通讯簿参数页面。](media/GAD-parameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
