---
title: 在 Microsoft Dynamics 365 Talent - Attract 中启用 Broadbean 集成
description: 本主题说明如何配置 Microsoft Dynamics 365 Talent - Attract 以将工作发布到外部招聘网站（如 Broadbean）。
author: andreabichsel
manager: AnnBe
ms.date: 07/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-07-08
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 808f91fb4b68ba9b5cee54d86423d23232df23a4
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/23/2019
ms.locfileid: "2008585"
---
# <a name="enable-broadbean-integration"></a>启用 Broadbean 集成

[!include[banner](../includes/banner.md)]

您可能希望尽可能多的合格应聘者可以看到您的开放职位。 Broadbean 之类招聘站点可以帮助您达成这个目标。 Microsoft Dynamics 365 Talent: Attract 现在允许您将工作发布到 Broadbean，Microsoft 正在不断提供此领域的新服务/产品。

> [!NOTE]
> - 若要将工作发布到外部站点，必须安装[综合招聘加载项](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring)。
> - 要通过 Attract 向 Broadbean 发布工作，必须订阅 Broadbean。
> - 此功能现在处于预览阶段。 如果要尝试，必须[在 Attract 管理员设置中开启](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature)。

## <a name="configure-broadbean-integration"></a>配置 Broadbean 集成

1. 以管理员身份登录 Attract。

2. 选择页面右上角的**设置**按钮（齿轮符号），然后选择**管理员中心**。

3. 联系 Broadbean，并在**用户名**、**客户 ID** 和**加密令牌**字段中输入您的信息。

4. 选择**保存**。

> [!WARNING]
> 您的 Broadbean 凭证是敏感的机密信息。 因此，请妥善保存和共享。 Attract 中的所有拥有管理员角色的人员都可以查看这些凭证。

> [!NOTE]
> Microsoft 和 Attract 不会参与这些值的创建和维护。 您负责使其在 Attract 中保持最新并与 Broadbean 合作解决涉及您的配置的所有问题。
