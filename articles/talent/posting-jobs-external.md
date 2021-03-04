---
title: 将工作从 Attract 发布到 Broadbean
description: 本主题说明如何使用 Dynamics 365 Talent - Attract 将工作发布到 Broadbean
author: pganapmsft
manager: AnnBe
ms.date: 05/16/2019
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
ms.openlocfilehash: 41fa057606887069a9ea0f1f2178eeaff59f33ca
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460492"
---
# <a name="post-jobs-to-broadbean-from-attract"></a>将工作从 Attract 发布到 Broadbean

[!include [banner](includes/banner.md)]

Microsoft Dynamics 365 Talent: Attract 允许您将工作直接从 Attract 发布到 Broadbean，从而帮助您获得所需的人才。 [创建工作](./creating-jobs-attract.md)后，您只需单击一个按钮即可将您的工作放在 Broadbean 上所有潜在应聘者的面前。

将工作发布到 Broadbean 需要相应的 Broadbean 许可证。 Broadbean 提供各种产品和计划。 有关 Broadbean 许可和定价的详细信息，请[联系 Broadbean](https://www.broadbean.com/contact-us/)。

如果您是需要有关如何使用 Attract 配置 Broadbean 集成的更多信息的管理员，请参阅[在 Microsoft Dynamics 365 Talent - Attract 中启用 Broadbean 集成](./attract-admin-job-board-settings.md)。

## <a name="post-jobs-to-broadbean"></a>将职位发布至 Broadbean

开启 Broadbean 之后，招聘人员和管理员可以向其发布工作。 您必须有该工作的申请 URL。

1. 在 Attract 中，打开要发布到 Broadbean 的工作。
2. 在 **发布** 部分中，选择与 Broadbean 对应的 **立即发布** 按钮。
3. 按照 Broadbean 窗口中的说明操作。

Attract 将把以下信息传递到 Broadbean：

- 请求 ID
- 职位
- 工作描述
- 工作地点
- 申请 URL
- 招聘人员信息

Broadbean 成功完成发布之后，Attract 中工作的 **发布** 部分将把 Broadbean 状态显示为 **已发布**。

> [!NOTE]
> - Broadbean 需要 **行业** 字段。 目前，此字段默认设置为 **IT**。 但是，您可以在 Broadbean 作业发布的窗口中将该值更改为正确的行业。
> - Broadbean 需要一些时间才能将您的工作发布到您选择所有招聘公告中。 因此，可能在稍微延迟后 Attract 才会提供工作的状态更新。

### <a name="view-a-broadbean-job-posting"></a>查看 Broadbean 工作发布

将工作发布到 Broadbean 会话，可以通过 Attract 查看。

1. 在 Attract 中，打开要在 Broadbean 中查看的工作。
2. 在 **发布** 选项卡上，选择与 Broadbean 对应的省略号按钮 (**...**)，然后选择 **查看**。

将在新窗口中显示 Broadbean 工作发布。

### <a name="update-a-broadbean-job-posting"></a>更新 Broadbean 工作发布

可以通过两种方法更新 Broadbean 工作发布。

1. 在 Attract 中，打开要更新的工作。
2. 在 **发布** 部分中，选择与 Broadbean 对应的 **更新发布** 按钮。
3. 在 Broadbean 窗口中编辑发布。

    –或者–

1. 在 Attract 中，打开要在 Broadbean 中查看的工作。
2. 在 **发布** 部分中，选择与 Broadbean 对应的省略号按钮 (**...**)，然后选择 **查看**。
3. 在 Broadbean 窗口中，编辑工作详细信息，然后重新发布工作。 将不更改 Attract 中的工作详细信息。

### <a name="remove-a-broadbean-job-posting"></a>删除 Broadbean 工作发布

可以根据需要删除 Broadbean 中的工作发布。

1. 在 Attract 中，打开要删除的工作。
2. 在 **发布** 部分中，选择与 Broadbean 对应的省略号按钮 (**...**)，然后选择 **删除发布**。

Broadbean 删除工作之后，Attract 中的 Broadbean 项将带有 **立即发布** 按钮。 存在此按钮说明工作已删除，可以重新发布。

### <a name="troubleshoot-job-posting-to-broadbean"></a>Broadbean 工作发布疑难解答

如果将工作发布到 Broadbean 时遇到问题，请尝试以下步骤。

1. 验证在 Attract 中输入的 Broadbean 配置是否有效且正确。
2. 如果这些凭证有效且正确，请联系 [Broadbean 支持](https://www.broadbean.com/resources/support/)。
3. 如果问题仍然存在，请联系 [Microsoft 支持](./talent-support.md)。

## <a name="see-also"></a>请参阅

[在 Attract 中创建、审核和发布工作](./creating-jobs-attract.md)

[在 Microsoft Dynamics 365 Talent - Attract 中启用 Broadbean 集成](./attract-admin-job-board-settings.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]