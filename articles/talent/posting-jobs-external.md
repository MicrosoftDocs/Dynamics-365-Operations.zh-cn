---
title: 通过 Attract 将工作发布到外部求职站点
description: 本主题介绍如何使用 Dynamics 365 for Talent - Attract 将工作发布到外部招聘站点。
author: pganapmsft
manager: AnnBe
ms.date: 03/20/2019
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
ms.search.validFrom: 2019-03-19
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: eca599ad189edae29ef2de496196b08799a5e745
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517435"
---
# <a name="post-jobs-to-external-career-sites-from-attract"></a>通过 Attract 将工作发布到外部求职站点

[!include [banner](../includes/banner.md)]

您可能希望尽可能多的合格应聘者可以看到您的开放职位。 Broadbean 之类招聘站点可以帮助您达成这个目标。 Microsoft Dynamics 365 Talent: Attract 现在允许您将工作发布到 Broadbean，而 Microsoft 将继续提供此领域中的新功能。

## <a name="post-jobs-to-broadbean"></a>将工作发布到 Broadbean

必须先配置 Broadbean 集成，才能将工作发布到 Broadbean。

> [!NOTE]
> - 若要将工作发布到外部站点，必须安装[综合招聘加载项](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring)。
> - 此功能现在处于预览阶段。 如果要尝试，必须[在 Attract 管理员设置中开启](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature)。

### <a name="configure-broadbean-integration"></a>配置 Broadbean 集成

1. 以管理员身份登录 Attract。
2. 选择页面右上角的**设置**按钮（齿轮符号），然后选择**管理员中心**。
3. 在**招聘公告设置**选项卡的**启用 Broadbean 集成**部分中，开启集成。
4. 联系 Broadbean，然后在**用户名、客户端 ID 和加密令牌**中输入您的信息。

> [!WARNING]
> 您的 Broadbean 凭证是敏感的机密信息。 因此，请妥善保存和共享。 Attract 中的所有拥有管理员角色的人员都可以查看这些凭证。

> [!NOTE]
> Microsoft 和 Attract 不会参与这些值的创建和维护。 您负责使其在 Attract 中保持最新并与 Broadbean 合作解决涉及您的配置的所有问题。

### <a name="post-a-job-to-broadbean"></a>将工作发布到 Broadbean

开启 Broadbean 之后，招聘人员和管理员可以向其发布工作。 您必须有该工作的申请 URL。

1. 在 Attract 中，打开要发布到 Broadbean 的工作。
2. 在**发布**部分中，选择与 Broadbean 对应的**立即发布**按钮。
3. 按照 Broadbean 窗口中的说明操作。

Attract 将把以下信息传递到 Broadbean：

- 请求 ID
- 职位
- 工作描述
- 工作地点
- 申请 URL
- 招聘人员信息

Broadbean 成功完成发布之后，Attract 中工作的**发布**部分将把 Broadbean 状态显示为**已发布**。

> [!NOTE]
> - Broadbean 需要**行业**字段。 目前，此字段默认设置为 **IT**。 但是，您可以在 Broadbean 作业发布的窗口中将该值更改为正确的行业。
> - Broadbean 需要一些时间才能将您的工作发布到您选择所有招聘公告中。 因此，可能在稍微延迟后 Attract 才会提供工作的状态更新。

### <a name="view-a-broadbean-job-posting"></a>查看 Broadbean 工作发布

将工作发布到 Broadbean 会话，可以通过 Attract 查看。

1. 在 Attract 中，打开要在 Broadbean 中查看的工作。
2. 在**发布**部分中，选择与 Broadbean 对应的省略号按钮 (**...**)，然后选择**查看**。

将在新窗口中显示 Broadbean 工作发布。

### <a name="update-a-broadbean-job-posting"></a>更新 Broadbean 工作发布

可以通过两种方法更新 Broadbean 工作发布。

1. 在 Attract 中，打开要更新的工作。
2. 在**发布**部分中，选择与 Broadbean 对应的**更新发布**按钮。
3. 在 Broadbean 窗口中编辑发布。

–或者–

1. 在 Attract 中，打开要在 Broadbean 中查看的工作。
2. 在**发布**部分中，选择与 Broadbean 对应的省略号按钮 (**...**)，然后选择**查看**。
3. 在 Broadbean 窗口中，编辑工作详细信息，然后重新发布工作。 将不更改 Attract 中的工作详细信息。

### <a name="remove-a-broadbean-job-posting"></a>删除 Broadbean 工作发布

可以根据需要删除 Broadbean 中的工作发布。

1. 在 Attract 中，打开要删除的工作。
2. 在**发布**部分中，选择与 Broadbean 对应的省略号按钮 (**...**)，然后选择**删除发布**。

Broadbean 删除工作之后，Attract 中的 Broadbean 项将带有**立即发布**按钮。 存在此按钮说明工作已删除，可以重新发布。

### <a name="troubleshoot-the-broadbean-integration"></a>Broadbean 集成故障排除

如果将工作发布到 Broadbean 时遇到问题，请尝试以下步骤。

1. 验证在 Attract 中输入的 Broadbean 配置是否有效且正确。
2. 如果这些凭证有效且正确，请联系 [Broadbean 支持](https://www.broadbean.com/resources/support/)。
3. 如果问题仍然存在，请联系 [Microsoft 支持](./talent-support.md)。
