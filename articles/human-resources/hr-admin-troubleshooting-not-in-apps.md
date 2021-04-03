---
title: Human Resources 未出现在 Microsoft Dynamics 365 应用中
description: 本文说明如果客户在 Microsoft Dynamics 365 应用之间看不到 Microsoft Dynamics 365 Human Resources 应用该做什么。
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
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
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9be1c2b862a01d6f14ad98dbcb01e061649c6af0
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/17/2021
ms.locfileid: "5463976"
---
# <a name="human-resources-doesnt-appear-in-microsoft-dynamics-365-apps"></a>Human Resources 未出现在 Microsoft Dynamics 365 应用中

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**发货**

客户在 Microsoft Dynamics 365 应用之间看不到 Dynamics 365 Human Resources。

**解决方法**

用户必须在 Microsoft Power Apps 中被添加到环境的环境制造者角色。

1. 具有 Power Apps 计划 2 许可证的管理员用户必须打开 [Power Apps 管理门户](https://preview.admin.powerapps.com/)。

2. 选择 **环境**，然后为 Human Resources 选择正确的环境。

3. 在 **安全** 选项卡上，在 **环境角色** 选项卡上，选择 **环境制造者**。

    ![环境角色选项卡](media/environment-roles.png)

4. 在 **用户** 选项卡上，添加用户或您的组织。

    ![用户选项卡](media/environment-maker.png)

5. 选择 **保存**。

6. 用户现在必须登录到 [Microsoft Dynamics 365](https://home.dynamics.com/)。

7. 选择 **同步** 更新用户应用。

    ![同步按钮](media/get-more.png)

    在完成同步后，Human Resources 将显示在主页上。


[!INCLUDE[footer-include](../includes/footer-banner.md)]