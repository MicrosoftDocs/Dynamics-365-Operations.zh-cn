---
title: Dynamics 365 Human Resources 基础结构合并概述
description: 本文介绍 Microsoft Dynamics 365 Human Resources 基础结构的合并。
author: twheeloc
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e68b28bfde35b51605aa0b653265da6261b69a90
ms.sourcegitcommit: 68efa7b89273d04484566cbe14d3533a8fd4ee53
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/02/2022
ms.locfileid: "9819234"
---
# <a name="dynamics-365-human-resources-infrastructure-merge"></a>Dynamics 365 Human Resources 基础结构合并 

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]
[!include [preview banner](../includes/preview-banner.md)]

## <a name="dynamics-human-resources-365"></a>Dynamics Human Resources 365

Microsoft Dynamics 365 Human Resources 提供了一些工具，用于帮助 HR 团队提高组织敏捷性、转换员工体验和优化 HR 计划，以创建可供人员和企业茁壮成长的工作场所。 要了解有关 Dynamics 365 Human Resources 的详细信息，请参阅 [Dynamics 365 Human Resources](https://dynamics.microsoft.com/human-resources/overview/)。

- **转换员工体验。** 通过推动敬业度和增长的互联自助服务体验来帮助经理和员工，从而留住业绩最佳员工。
- **优化 HR 计划。** 帮助降低运营成本，并创建以人为本的休假和缺勤、时间、福利和薪酬管理计划。
- **提高组织敏捷性。** 通过使用 Dataverse 和 Microsoft Power Platform 集中人员数据并轻松扩展 Dynamics 365 Human Resources，使 HR 能够以业务所需的灵巧度进行运作。
- **发现劳动力见解。** 通过在任何设备上都可用的大量仪表板上分析和显示人员数据的功能，做出数据驱动型决策。

## <a name="human-resources-infrastructure-merge"></a>Human Resources 基础结构合并

Dynamics 365 Human Resources 是一个独立的应用程序，目前使用与其他财务和运营应用（如 Dynamics 365 Finance 或 Dynamics 365 Supply Chain Management）不同的基础结构。 基础结构合并将 Dynamics 365 Human Resources 引入与其他财务和运营应用相同的基础结构。

要详细了解 Human Resources 的基础结构合并，请参阅[合并 HR 产品/服务](https://cloudblogs.microsoft.com/dynamics365/it/2021/09/15/merging-of-hr-offerings-brings-capabilities-together-for-customers/)。 要获取常见问题的解答，请参阅 [Human Resources 基础结构合并常见问题解答](./hr-infrastructure-merge-faq.md)。

## <a name="customer-migration-vs-customer-merge"></a>客户迁移与客户合并

作为基础结构合并的一部分，Human Resources 应用程序的所有功能都已在财务和运营环境中提供。 客户可以使用 Microsoft Dynamics Lifecycle Services 中提供的迁移工具迁移 Human Resources 环境。 他们还可以选择将他们的数据与现有的财务和运营环境合并。 

客户迁移和客户合并在以下方面有所不同：

- **客户迁移** – 自动迁移工具用于执行客户数据库从 Human Resources 基础结构到财务和运营基础结构的“直接迁移”（移动）。 结果是生成了使用客户的 Human Resources 数据库的新财务和运营环境。 
- **客户合并** – Microsoft 不要求执行此额外步骤。 它由客户自行决定，可按照客户自己的时间线完成。 在此步骤中，客户数据被移动到现有环境，如 Finance 或 Project Operations 环境。 它主要是手动完成，可以使用数据管理框架 (DMF) 数据实体来完成。 

## <a name="planning-a-human-resources-environment-migration"></a>计划 Human Resources 环境迁移

作为基础结构合并的一部分，所有客户都需要从独立基础结构迁移其现有的 Human Resources 环境。 为了帮助完成此过程，我们建议您使用 Lifecycle Services 中的自动迁移工具将您当前的环境迁移到新的基础结构。 

以下一节提供有关如何使用 Lifecycle Services 工具迁移独立 Human Resources 环境的更多详细信息。 

计划迁移的客户会面临以下情况：

- 所有客户都需要迁移沙盒环境，然后才能够迁移生产环境。 
- 迁移工具仅支持沙盒到沙盒和生产到生产的迁移。 因此，您的环境类型将确定可以相应迁移的环境。 
- 客户可以在迁移生产环境之前根据需要迁移任意数量的沙盒，前提是目标沙盒槽可用。 客户还可以删除已迁移的沙盒，然后多次重新迁移。 
- 如果沙盒迁移失败，或者您想要重新开始，您可以删除财务和运营基础结构上的环境，然后重新迁移相同的环境。
- 迁移后，您的 Human Resources 环境的 URL 会不同。
- 为生产环境的迁移计划适当的停机时长。 完成自动迁移过程的估计时间范围为三到四个小时。 时间范围会因您的组织的数据而有所不同。 您应该验证迁移沙盒环境期间所需的时长，为必须完成的任何其他手动任务留出时间。

> [!IMPORTANT] 
> 当生产环境成功迁移到财务和运营基础结构时，源独立生产环境将被自动删除。 您不应删除迁移的生产环境。 

迁移过程大部分是自动的。 但是，您的业务用户必须在迁移后完成一些手动步骤和验证。

必须完成以下手动步骤：

- 为迁移创建新 Lifecycle Services 项目。
- 根据每个集成配置，通过将集成指向新 URL/终结点，将旧环境中的任何集成修改为新环境。
- 刷新嵌入式 Power BI 报表的数据存储。
- 从 DMF 工作区刷新数据实体列表。
- 链接到 Lifecycle Services 以获取帮助。
- 创建会计日历。

在自动过程中，将完成并应验证以下操作：

- 数据：

    - 配置
    - 安全角色（包括自定义角色）
    - 工作流（包括通知）
    - 个性化和已保存视图
    - 交易记录
    - 自定义字段
    - 附件
    - 预警

- 数据管理 – 提供您自己的数据库 (BYOD)。
- 功能管理 - 启用/禁用的功能。
- 嵌入式 Power Apps。
- Power Platform 管理中心附加环境（仅生产）。
- 批处理作业。
- 将为每个法人创建一个空分类帐。 将设置每个分类帐的默认汇率类型和会计货币。
- 将自动创建一个新的会计科目表，并将其链接到每个法人的 **分类帐** 页面。 在您的 Human Resources 环境中配置的财务维度将被自动添加到新科目结构并链接到分类帐。 

> [!NOTE]
> 财务和运营基础结构上需要有分类帐，将其作为 Dynamics 365 Finance 产品的一部分。 Dynamics 365 Human Resources 独立应用程序中存在的自定义维度控制器不可用。 合并后的 Human Resources 基础结构依赖于 Finance 逻辑来在 **Human Resources** 中显示财务维度。 要了解有关会计科目表和财务维度的更多信息，请参见[此处](../finance/general-ledger/plan-chart-of-accounts.md)。 

## <a name="considerations"></a>注意事项

- 迁移到环境会始终使用最新的正式发布 (GA) 版本。 根据您的迁移和测试计划，如果您对沙盒环境的迁移验证在不同版本上，我们建议您在与生产环境相同的版本上验证沙盒迁移。 
- 在迁移期间，迁移的环境将与源独立 Human Resources 环境放到同一区域。

## <a name="licensing"></a>许可授权

Dynamics 365 Human Resources 的许可在以下方面没有变化： 

- **最少许可证购买要求**
- **生产环境和沙盒环境的许可证** – 如果您现有的独立 Human Resources 许可证授予一个生产环境和一个沙盒环境权限，财务和运营基础结构上可用的许可证数量相同，无需额外费用。
- **其他沙盒许可证** – 如果您为独立 Human Resources 应用程序购买了额外的沙盒许可证，财务和运营基础结构上的标准接受度测试（沙盒）环境可用的沙盒许可证数量相同，无需额外费用。 
