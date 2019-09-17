---
title: Attract 与 LinkedIn 集成的常见问题
description: 本主题回答有关您可能遇到的 LinkedIn 与 Microsoft Dynamics 365 for Talent - Attract 之间的集成问题。
author: hasrivas
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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: hasrivas
ms.search.validFrom: 2019-07-08
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: c49181fe7e9359fb9d7d43f479273080f90542f4
ms.sourcegitcommit: c62756cb04549b2ff5de9b93d497e964a340335a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/17/2019
ms.locfileid: "1756191"
---
# <a name="linkedin-integration-faq"></a>LinkedIn 集成常见问题

[!include [banner](includes/banner.md)]

LinkedIn 是全球最大的在线职业网络。 Microsoft Dynamics for Talent: Attract 与 LinkedIn 集成，让您可以联系世界顶级人才。 Attract 允许您将工作直接发布到 LinkedIn，它还允许您将 LinkedIn 中的应聘者信息导入到 Attract 中。

## <a name="for-recruiters-and-hiring-managers"></a>针对招聘人员和招聘经理

以下是有关如何结合使用 Attract 和 LinkedIn 的常见问题解答。

### <a name="what-linkedin-features-do-i-get-with-attract"></a>使用 Attract 可以获得哪些 LinkedIn 功能？

Attract 与 LinkedIn 的集成使您可以执行以下任务：

- [将工作发布到 LinkedIn](./attract-post-jobs-to-linkedin.md)（作为免费的 Limited Listings(有限列表)）。
- [将应聘者信息从 LinkedIn 导出到 Attract](./attract-linkedin-recruiter.md#export-linkedin-candidates-to-attract-with-one-click).
- [允许工作应聘者通过 LinkedIn 申请工作](./attract-admin-linkedin.md#set-up-apply-with-linkedin-in-attract).

### <a name="what-do-i-need-before-i-can-post-jobs-to-linkedin"></a>在将工作发布到 LinkedIn 之前，我需要什么？

您的管理员必须[在 Attract 中配置 LinkedIn 集成](./attract-admin-linkedin.md#configure-job-posting-to-linkedin)。 在那之后，您已经准备好了。

### <a name="how-do-i-post-jobs-to-linkedin-from-attract"></a>如何从 Attract 向 LinkedIn 发布工作？

在 Attract 中创建工作后，您只需选择与 LinkedIn 对应的**立即发布**按钮即可。 有关详细信息，请参阅[将工作从 Attract 发布到 LinkedIn](./attract-post-jobs-to-linkedin.md#post-jobs-to-linkedin)。

### <a name="can-i-get-candidate-information-from-linkedin-into-attract"></a>我可以将 LinkedIn 中的应聘者信息放到 Attract 中吗？

是。 如果您在 LinkedIn 上看到一个合适的应聘者，您可以轻松地将该应聘者的信息导出到 Attract 中。 有关详细信息，请参阅[使用 LinkedIn Recruiter 寻求应聘者](attract-linkedin-recruiter.md)。

### <a name="how-can-i-get-help-accessing-linkedin-from-attract"></a>如何获取从 Attract 访问 LinkedIn 的帮助？

如果您在登录或从 Attract 向 LinkedIn 发布工作时遇到问题，请参阅 [LinkedIn 集成疑难解答](./attract-troubleshoot-linkedin.md)。

有关 Attract 的其他问题，请参阅[获取 Talent 支持](./talent-support.md)。 有关 LinkedIn 的帮助，请参阅 [LinkedIn 支持页面](https://www.linkedin.com/help)。

## <a name="for-admins-and-developers"></a>针对管理员和开发人员

以下是有关如何配置 Attract 与 LinkedIn 之间的集成的常见问题解答。

### <a name="how-do-i-configure-attract-so-that-recruiters-and-hiring-managers-can-post-jobs-to-linkedin"></a>如何配置 Attract，以便招聘人员和招聘经理可以将工作发布到 LinkedIn？

您可以在“管理中心”的 **LinkedIn 集成**选项卡上配置可用选项。 有关详细信息，请参阅[设置与 LinkedIn 的集成](./attract-admin-linkedin.md)。

### <a name="can-i-export-candidate-information-from-linkedin"></a>我可以从 LinkedIn 导出应聘者信息吗？

可以，但您必须首先配置与 LinkedIn Recruiter 的集成。 有关详细信息，请参阅[设置与 LinkedIn 的集成](./attract-admin-linkedin.md)。

### <a name="how-can-i-post-jobs-to-premium-job-slots-on-linkedin"></a>如何将工作发布到 LinkedIn 上的 Premium Job Slots（高级职位空缺）？

尽管 Attract 为将工作发布到 LinkedIn 提供了强大的解决方案，但您可能会发现您还需要额外的灵活方式。 例如，除了免费的 Limited Listings（有限列表）之外，您可能希望能够发布 Premium Job Slots（高级职位空缺），或者您可能希望 LinkedIn 每天多次处理您的批量工作发布。

#### <a name="types-of-linkedin-job-posts"></a>LinkedIn 的工作发布类型

LinkedIn 提供以下类型的工作发布：

- **Limited Listing** – 当应聘者在 LinkedIn 和公司的 LinkedIn 页面上搜索工作时，搜索结果中显示的免费工作发布。 Limited Listings（有限列表）针对主动的求职者。 此类列表是 Attract 为 LinkedIn 提供的类型。 您不能在 LinkedIn 上宣传 Limited Listing（有限列表）工作。 如果您想宣传 Limited Listings（有限列表），您必须与 LinkedIn 合作来启用 Job Wrapping（工作包装）。 有关 Job Wrapping（工作包装）的详细信息，请参阅 [Limited Listings（有限列表）与 Job Wrapping（工作包装）的 Premium Job Slots（高级职位空缺）](https://www.linkedin.com/help/recruiter/answer/79049/limited-listings-vs-premium-job-slots-for-job-wrapping)和 [Job Wrapping Plus（工作包装增强版）- 常见问题](https://www.linkedin.com/help/recruiter/answer/79050/job-wrapping-frequently-asked-questions)。
- **Premium Job Slot（高级职位空缺）**– 购买的工作发布出现在 LinkedIn 的各个位置，如 LinkedIn Feed、电子邮件和**您可能感兴趣的工作**区域。 Premium Job Slots（高级职位空缺）主要针对被动应聘者，但它们也出现在工作搜索中。

Attract 作为 Limited Listings（有限列表）将工作发布到 LinkedIn。 如果要使用 Premium Job Slots（高级职位空缺），则必须通过 LinkedIn Recruiter 使用 Job Wrapping（工作包装）。 Job Wrapping（工作包装）需要 LinkedIn 签订工作包装合同。 有关详细信息，请参阅[通过 LinkedIn Recruiter 使用 Job Wrapping（工作包装）- 概述](https://www.linkedin.com/help/recruiter/answer/79037)。

#### <a name="frequency-of-batch-processing-on-linkedin"></a>LinkedIn 上的批处理频率

LinkedIn 每天通过 Attract 批处理一次工作发布。 因此，在通过 Attract 发布工作后，最多可能需要 48 小时在 LinkedIn 上显示工作。 如果您需要在 LinkedIn 上更早显示工作，或者您需要任何额外的灵活性，可以使用 LinkedIn 提供的 Recruiter System Connect 应用程序编程接口 (API)。 有关详细信息，请参阅 [Recruiter System Connect](https://docs.microsoft.com/linkedin/talent/recruiter-system-connect)。

#### <a name="table-of-options-for-job-posting-to-linkedin"></a>向 LinkedIn 发布工作的选项表

下表描述了将工作发布到 LinkedIn 的不同选项。 其中包括每个选项的优点和其他信息。

|  | Attract | 通过 LinkedIn Recruiter 使用 Job Wrapping（工作包装） | Recruiter System Connect API |
|---|---|---|---|
| **说明** | Attract 将工作作为 XML 源发布到 LinkedIn。 | 公司与 LinkedIn 签订合同，并提供用于发布工作的 XML 源。 | 客户使用 API 在 Attract 和 LinkedIn Recruiter 之间同步信息。 |
| **我可以发布哪类工作？** | Limited Listing（有限列表） | Premium Job Slot（高级职位空缺）或 Limited Listing（有限列表） | Limited Listing（有限列表） |
| **我可以在 LinkedIn 上宣传此工作吗？** | 否 | Premium Job Slots（高级职位空缺）：是<br>Limited Listings（有限列表）：否 | 否 |
| **LinkedIn 发布工作的频率如何？** | 每天一次 | 每天一次 | 每天多次，由 API 定义 |
| **LinkedIn 推荐？** | 否 | 是 | 否 |
| **我需要什么？** | 购买 Attract | 与 LinkedIn 签订工作包装合同并购买 Premium Job Slots（高级职位空缺） | 与 LinkedIn 的 API 协议 | 
| **我可以在何处找到详细信息？** | [设置与 LinkedIn 的集成](./attract-admin-linkedin.md) | [通过 LinkedIn Recruiter 使用 Job Wrapping（工作包装）- 概述](https://www.linkedin.com/help/recruiter/answer/79037) | [Recruiter System Connect](https://docs.microsoft.com/linkedin/talent/recruiter-system-connect) |

> [!NOTE]
> 您不需要 LinkedIn Recruiter System Connect 许可证即可通过 Attract 将工作发布到 LinkedIn。

## <a name="see-also"></a>请参阅

[设置与 LinkedIn 的集成](./attract-admin-linkedin.md)

[将工作从 Attract 发布到 LinkedIn](./attract-post-jobs-to-linkedin.md)

[使用 LinkedIn Recruiter 寻求应聘者](./attract-linkedin-recruiter.md)

[LinkedIn 集成疑难解答](./attract-troubleshoot-linkedin.md)
