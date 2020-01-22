---
title: Talent 未在 Microsoft Dynamics 365 应用 (Common Data Service 1.0) 中显示
description: 本主题说明如果客户在 Microsoft Dynamics 365 应用之间看不到 Microsoft Dynamics 365 Talent 应用该做什么。
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
ms.openlocfilehash: a44d2e43752960d3026fa7ac92c7b261aee05448
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897019"
---
# <a name="talent-doesnt-appear-among-the-microsoft-dynamics-365-apps-common-data-service-10"></a>Talent 未在 Microsoft Dynamics 365 应用 (Common Data Service 1.0) 中显示

**发货**

客户在 Microsoft Dynamics 365 应用之间看不到 Dynamics 365 Talent 应用。

**分辨率**

用户必须在 Microsoft Power Apps 中被添加到环境的环境制造者角色。

1. 具有 Power Apps 计划 2 许可证的管理员用户必须打开 [Power Apps 管理门户](https://preview.admin.powerapps.com/)。
2. 选择**环境**，然后为 Talent 选择正确的环境。
3. 在**安全**选项卡上，在**环境角色**选项卡上，选择**环境制造者**。

    ![环境角色选项卡](media/environment-roles.png)

4. 在**用户**选项卡上，添加用户或您的组织。

    ![用户选项卡](media/environment-maker.png)

5. 选择**保存**。
6. 用户现在必须登录到 [Microsoft Dynamics 365](https://home.dynamics.com/)。
7. 选择**同步**更新用户应用。

    ![同步按钮](media/get-more.png)

    在完成同步后，Talent 将显示在主页上。
