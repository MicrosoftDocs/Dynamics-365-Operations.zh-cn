---
title: 准备 Human Resources 实行
description: 该页面提供了有关如何准备实行 Dynamics 365 Human Resources 的指南。
author: rachel-profitt
manager: tfehr
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 59d7274c3b40e78209d90960c4514321b736876a
ms.sourcegitcommit: d66fd72342931fad25a696b251c05781280d36c4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/14/2020
ms.locfileid: "4011403"
---
# <a name="prepare-for-human-resources-go-live"></a>准备 Human Resources 实行

[!include [banner](../includes/banner.md)]

本主题介绍了如何使用 Microsoft Dynamics Lifecycle Services (LCS) 准备实行 Dynamics 365 Human Resources 项目。 

此图显示了实行流程的各个阶段。 

![实行流程](./media/hr-admin-go-live-prepare-process.png)

下表列出了流程中的所有步骤、预期持续时间以及行为负责人。

| 阶段 | 行为 | 持续时间/时间 | 人员 | 说明 |
| --- | --- | --- | --- |--- |
| 1 | 在 LCS 中更新实行日期 | 最迟提前 2-3 个月 | 合作伙伴/客户 | 里程碑日期应该不断更新。 |
| 2 | 完成并发送清单 | 用户验收测试 (UAT) 完成之后 | 合作伙伴/客户 | 请按照 [FastTrack 实行评估](hr-admin-go-live-prepare.md#fasttrack-go-live-assessment)中提供的说明操作。 |
| 3 | 项目评估 (FastTrack) | FastTrack 架构师* | 架构师在收到清单后进行评估并继续进行审核，直到确定问题并采取缓解措施（如果适用）。 |
| 4 | 项目研讨会 (FastTrack) | FastTrack 架构师* | |
| 5 | 数据包导入 | 取决于项目 | 合作伙伴/客户 | 请按照[数据管理概述](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities-data-packages)中的说明操作。|
| 6 | 生产准备 | 在完成前面的所有步骤之后 | 合作伙伴/客户 | 合作伙伴/客户可以控制生产环境。|
| 7 | 直接转换活动 | 取决于项目 | 合作伙伴/客户 | |
| 8 | 实行 | 取决于项目 | 客户 | |

> [!IMPORTANT]
> *仅针对符合 FastTrack 资格的客户完成步骤 3 和 4。

## <a name="completing-the-lcs-methodology"></a>完成 LCS 方法

每个实施项目中的重要里程碑都是到生产环境的直接转换。 

为了帮助确保生产环境用于实时操作，在完成 LCS 方法中的所需活动后，Microsoft 仅在实施接近 **运行** 阶段时才预配生产实例。 有关您订阅中的环境的详细信息，请参阅  [Dynamics 365 许可指南](https://go.microsoft.com/fwlink/?LinkId=866544)。 

客户必须完成 LCS 方法中的 **分析** 、 **设计和开发** 和 **测试** 阶段，用于请求生产环境的 **配置** 按钮才可用。 若要完成 LCS 中的某个阶段，您必须首先完成该阶段中的每个必需步骤。 完成阶段中的所有步骤后，您可以完成整个阶段。 如果必须进行更改，您可以在以后始终重新打开阶段。 有关详细信息，请参阅 [适用于 Finance and Operations 应用客户的 Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs-works-lcs)。 

完成步骤的流程分为两个部分： 

- 执行实际工作，例如填补差距分析或用户验收测试 (UAT)。 
- 将 LCS 方法中的相应步骤标记为已完成。 

合理的做法是在实施流程中完成方法中的步骤。 尽早完成工作。 不要仅仅单击所有步骤，以便获得生产环境。 进行可靠的实施符合客户的最大利益。 

## <a name="uat-for-your-solution"></a>适用于您的解决方案的 UAT

在 UAT 阶段，您必须在实施项目的沙盒环境中测试已实施的所有业务流程以及所做的任何自定义。 为了帮助确保成功实行，在完成 UAT 阶段时应考虑以下事项： 

- 测试用例涵盖整个需求范围。 
- 使用迁移的数据进行测试。 此数据应包括主数据，例如工作人员、工作和职位。 还包括期初余额，例如休假和缺勤应计。 最后，包括未结交易，例如当前的福利登记。 即使未完成数据集，也可以使用所有类型的数据完成测试。 
- 使用分配给用户的正确安全角色（默认角色和自定义角色）进行测试。 
- 确保解决方案符合任何公司和行业特定的法规要求。 
- 记录所有功能，并获得客户的审批和签核。 

## <a name="fasttrack-go-live-assessment"></a>FastTrack 实行评估

符合 FastTrack 资格并与 FastTrack 解决方案架构师合作的客户将通过 Microsoft FastTrack 完成实行审核。 有关详细信息，请参阅  [Microsoft FastTrack](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/fasttrack-dynamics-365-overview)。 

大约在实行前的八周内，FastTrack 团队会要求您填写[实行清单](https://go.microsoft.com/fwlink/?linkid=2146013)。

项目经理或关键项目成员必须在项目的预先实行阶段完成实行清单。 通常，当 UAT 已完成或几乎完成时，清单将在建议的实行日期之前四到六周内完成。 

完成实行清单后，通过电子邮件将其发送给 FastTrack 解决方案架构师。 始终在电子邮件中包括来自客户和实施合作伙伴的关键利益相关者。 

提交清单后，您的 FastTrack 解决方案架构师将审查该项目并提供评估，以描述潜在风险、最佳实践以及成功实行项目的建议。 在某些情况下，解决方案架构师可能会强调风险因素并要求制定缓解计划。 

## <a name="see-also"></a>请参阅

[实施常见问题](hr-admin-go-live-faq.md)