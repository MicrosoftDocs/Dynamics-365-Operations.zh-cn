---
title: Attract 用户无法通过求职门户申请职位
description: 本主题介绍如何解决 Attract 用户无法通过求职门户申请职位的问题。
author: andreabichsel
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-09-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: e1d72bef6d8bbe15e27326f66341915ba44a09b4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460414"
---
# <a name="attract-users-cant-apply-for-jobs-from-career-portal"></a>Attract 用户无法通过求职门户申请职位

[!include [banner](includes/banner.md)]

## <a name="issue"></a>签发

Attract 用户无法通过求职门户申请职位。 当他们尝试申请在 Dynamics 365 Talent: Attract 中创建的职位时，浏览器将持续加载页面，并且无法完成操作。

## <a name="cause"></a>原因

当 Talent 关系团队没有 Talent 用户角色时，会发生此问题。

## <a name="resolution"></a>解决方法

将 Talent 用户角色分配给 Talent 关系团队。

1. 使用以下任何管理员凭据登录到 [Power Platform 管理中心](https://admin.powerplatform.microsoft.com)：

   - Dynamics 365 管理员
   - 全局管理员
   - Power Platform 管理员

2. 在导航窗格中，选择 **环境**，然后选择要在其中将 Talent 用户角色分配给 Talent 关系团队的环境。

   ![选择环境](./media/attract-troubleshoot-career-portal-select-environment.png)

3. 在 **环境** 窗格中，选择 **环境 URL**，然后登录到环境的管理门户（例如 https:<orgname>.crm.dynamics.com）。

4. 选择 **设置**，选择 **系统**，然后选择 **安全性**。

   ![导航到安全性](./media/attract-troubleshoot-career-portal-security.png)

5. 选择 **团队**。

   ![选择团队](./media/attract-troubleshoot-career-portal-security-teams.png)

6. 在搜索框中搜索 **Talent 关系团队**，然后从搜索结果中选择团队。

7. 从功能区中选择 **管理角色**。

8. 在 **管理团队角色** 对话框中，从可用角色列表中选择 **Talent 用户**，然后选择 **确定** 以应用角色。

   ![应用角色](./media/attract-troubleshoot-career-portal-apply-role.png)

9. 测试您的更改：

   1. 从新的浏览器窗口登录到求职门户。
   2. 通过求职门户申请职位。 

[!INCLUDE[footer-include](../includes/footer-banner.md)]