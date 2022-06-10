---
title: 主计划的迁移到计划优化
description: 本主题提供有关新的主计划引擎、计划优化的信息，以及有关从现有引擎迁移的信息。
author: t-benebo
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: ''
ms.author: benebotg
ms.search.validFrom: 2020-11-05
ms.dyn365.ops.version: ''
ms.openlocfilehash: 598e29ead50e1ecb249a7338c7f0952a912b4f69
ms.sourcegitcommit: cbe9493d479f96f271d94599ec1b85131b26169f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/27/2022
ms.locfileid: "8809086"
---
# <a name="migration-to-planning-optimization-for-master-planning"></a>主计划的迁移到计划优化

[!include [banner](../includes/banner.md)]

内置的主计划引擎计划将被废弃（已弃用）。 它将替换为 Microsoft Dynamics 365 Supply Chain Management 的计划优化加载项。 本主题提供有关对新部署和现有部署的影响的信息。 它包含有关所需操作的信息。

计划优化使主计划计算可以在 Supply Chain Management 及其 Azure SQL 数据库之外进行。 与计划优化相关的好处包括在主计划运行期间改进的性能以及对 SQL 数据库的影响最小。 因为即使在工作时间内也可以进行快速计划运行，因此计划人员可以立即对需求或参数更改作出反应。

有关计划优化的详细信息，请参阅[计划优化概述](planning-optimization/planning-optimization-overview.md)。

## <a name="obsolescence-of-the-existing-master-planning-engine"></a>现有主计划引擎的废弃

Microsoft 正在废弃内置的计划引擎，以支持计划优化。 此更改会影响所有云环境。 本地安装不受影响。 在版本 10.0.16 及更高版本中，如果运行内置主计划而不生成计划的生产订单，您将收到错误消息。 但是，尽管有错误消息，主计划运行仍将成功完成。

有关内置计划引擎的废弃的详细信息，请参阅 [Dynamics 365 Supply Chain Management 中的已删除或已弃用功能](../get-started/removed-deprecated-features-scm-updates.md)中的公告。

## <a name="migration-messages-and-exceptions"></a>迁移、消息和例外

运行内置主计划引擎而不生成计划生产订单的现有环境的所有者将收到一封电子邮件，用于提供有关例外流程的详细信息。 我们建议您与合作伙伴一起评估和计划迁移到计划优化。

如前所述，在版本 10.0.16 及更高版本中，如果运行内置主计划而不生成计划的生产订单，您将收到错误消息。 此错误消息包括有关迁移的指南和有关请求例外的说明。

### <a name="new-deployments"></a>新部署

对于云中的所有新部署，必须将计划优化视为默认的主计划引擎。 通常，应该将计划优化用于在主计划期间不生成计划生产订单的所有新部署。 如果新部署依赖于计划优化当前不支持的功能，您可以请求例外，以便继续使用内置的主计划引擎。

### <a name="existing-deployments"></a>现有部署

依赖于主计划的现有基于云的部署的所有者应计划迁移到计划优化。 如果您的实施依赖于计划优化当前不支持的功能，您可以请求例外，以便继续使用内置的主计划引擎。

对于当前使用将要废弃的主计划流程的环境，Microsoft 将向环境管理员发送电子邮件。该电子邮件将提供有关迁移或请求例外所需操作的信息。

## <a name="the-exception-process"></a>例外流程

如果您因为您的业务流程在很大程度上依赖于当前在计划优化中未实现的至少一项功能，而必须继续使用内置的主计划引擎，可以请求例外。 有关可用功能的列表，请参阅[计划优化拟合分析](planning-optimization/planning-optimization-fit-analysis.md)。

当前，如果您的主计划流程不包括生产（即由主计划生成的计划生产订单）并且您需要版本 10.0.15 以上的内置主计划引擎，则仅与计划优化的例外相关。

在所需的功能变为可用后，Microsoft 将提供一个宽限期，直到例外到期。 当所需的功能变为可用并且宽限期已开始时，将通知环境管理员。

以下流程图总结了本主题中提供的信息，以便您可以快速确定是否应请求例外。 如果需要请求例外，请填写并提交[计划优化迁移和例外调查表](https://go.microsoft.com/fwlink/?linkid=2144962)。 产品组负责评估和审核每个异常请求，因此请使用提供的链接直接将您的请求提交给产品组，并且不为此创建支持票证。 如果您的请求被拒绝，请不要创建支持票证，因为 Microsoft 支持人员无法重新评估或准许异常。

![例外流程图。](media/exception-diagram.png "例外流程图")

> [!NOTE]
> 您只能针对当前包括或将包括生产环境的租户（而不能仅针对具有沙盒环境的租户）请求例外。 如果您需要在基础结构即服务 (IaaS) 沙盒环境上禁用计划优化例外错误，请运行在[沙盒环境](#faq-sandbox)中提供的 SQL 查询。

## <a name="frequently-asked-questions"></a>常见问题

### <a name="sandbox-environments"></a><a name="faq-sandbox"></a>沙盒环境

是否可以在我的沙盒环境上使用内置主计划？ 是否需要例外？

**回答：** 例外通常与沙盒环境无关，因为计划优化例外错误不会阻止内置主计划引擎成功运行。 但是，如果错误消息打扰到您，可以通过在您的数据库上运行以下查询来在 IaaS（而非 Service Fabric）沙盒环境上禁用它：

```sql
-- Insert or update an enabled flight:
DECLARE @flightName NVARCHAR(100) = 'ReqPlanningOptimizationExceptionToggle';
IF NOT EXISTS (SELECT TOP 1 1 FROM SysFlighting WHERE flightName = @flightName)
    INSERT INTO SYSFLIGHTING(FLIGHTNAME,ENABLED, FLIGHTSERVICEID,PARTITION)
    SELECT @flightName, 1, 12719367,RECID FROM DBO.[PARTITIONS];
ELSE
    UPDATE SysFlighting SET enabled = 1, flightServiceId = 12719367 WHERE flightName = @flightName;
```

### <a name="on-premises-environments"></a>本地环境

我的环境是本地的。 是否需要例外？

**回答：** 否。 本地环境不需要例外。 您可以继续使用内置主计划。 如果需要任何操作，您的环境管理员将收到通知。

### <a name="production-scenarios"></a>生产方案

我们使用计划生产订单，但是我担心升级到版本 10.0.16 时会发生什么。 是否应采取任何操作？

**回答：** 您不必担心。 您可以在版本 10.0.16 中继续使用内置主计划。 但是，我们建议您评估是否可以从当前功能开始迁移到计划优化。 我们还建议您随时了解新功能。

### <a name="email-from-microsoft"></a>来自 Microsoft 的电子邮件

我们的环境管理员收到了来自 Microsoft 的电子邮件。 此电子邮件表明我们应该迁移到计划优化或请求例外。 是否需要采取任何操作？

**回答：** 是。 除非您遵循电子邮件中的说明，否则您的环境将受影响。 您可以按指定的日期迁移到计划优化，也可以使用电子邮件中的链接请求例外。 此链接将打开一个调查表。 完成并提交此调查表后，您将通过电子邮件收到回复。 尽管此流程是手动的，但 Microsoft 将尝试在提交调查表后的一周内回复。

### <a name="error-messages"></a>错误消息

我使用的是版本 10.0.16 或更高版本，并且在运行主计划时收到以下错误消息。 是否阻止主计划？

> 您收到此错误消息是因为内置主计划引擎用于计划优化所支持的方案。 您现在应该迁移到计划优化，因为当前的内置主计划已弃用。 请注意，此主计划运行已成功完成。
>
> 如果您的迁移非常依赖待定功能，可以请求继续使用内置主计划引擎的例外。
>
> 请完成以下调查表以开始使用（如果与从迁移到计划优化请求例外相关）。

**回答：** 否，不阻止主计划。 您的主计划运行已成功完成，可按常规方式使用结果。 但是，为了避免在以后的主计划运行期间收到此错误消息，您必须立即迁移到计划优化或使用错误消息中的链接请求例外。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
