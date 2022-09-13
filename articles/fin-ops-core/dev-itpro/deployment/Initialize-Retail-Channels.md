---
title: 初始化 Commerce Scale Unit（云）
description: 本文说明如何在 Microsoft Dynamics 365 Commerce 中初始化 Commerce Scale Unit（云）。
author: jashanno
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jashanno
ms.search.validFrom: 2018-04-30
ms.openlocfilehash: a4a36d773e0790747c017dca35492af5caf410ab
ms.sourcegitcommit: 61be5f43c9678e9f12b4a90410876b4a179ac585
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/08/2022
ms.locfileid: "9427068"
---
# <a name="initialize-commerce-scale-unit-cloud"></a>初始化 Commerce Scale Unit（云）

[!include[banner](../includes/banner.md)]

本文说明如何在 Microsoft Dynamics 365 Commerce 中初始化 Commerce Scale Unit（云）。

如果您使用的是具有应用程序版本 8.1.2.x 或更高版本的第 2 层沙盒或生产环境，您必须先初始化 Commerce Scale Unit（云），然后才能将零售渠道功能用于销售点 (POS) 运营或用于在云中使用 Retail Server 的电子商务运营。 初始化将部署 Commerce Scale Unit（云）。

> [!IMPORTANT]
> 对于云中使用零售渠道功能的现有客户，为了确保为您的业务提供持续的不间断的支持，需要您更新零售渠道以使用 Commerce Scale Unit。 不使用 Commerce Scale Unit 部署的新环境将不再接收云托管零售渠道组件的质量和服务更新。 对于仅使用 Commerce Scale Unit（自托管）的客户，无需执行任何操作。 如果您需要扩展，请与您的 Microsoft FastTrack 解决方案架构师联系。

## <a name="prerequisites"></a>先决条件

1. 部署具有 8.1.2.x 或更高版本的第 2 层沙盒或生产环境。
2. 每个环境最多可自行部署 2 个 Commerce Scale Unit。 如果每个环境需要 2 个以上的 Commerce Scale Unit，请在 Microsoft Dynamics Lifecycle Services (LCS) 中创建支持请求，输入 **请求其他 Commerce Scale Unit**，并提供环境 ID、Commerce Scale Unit 数量和所需的数据中心区域。 请求将在五个工作日内完成。 如果每个环境不需要超过 2 个 Commerce Scale Unit，则无需创建支持请求。 
3. 您必须在 Lifecycle Services 中具有项目负责人权限，才能初始化 Commerce Scale Unit。
4. 确保在您的环境中启用 Retail 许可证配置密钥。 有关详细信息，请参阅[许可证代码和配置密钥报表](../sysadmin/license-codes-configuration-keys-report.md)。 必须启用以下密钥才能使用 Commerce Scale Unit。

    - RetailBasic
    - RetaileCommerce - 如果您计划将电子商务用于 Dynamics 365 Commerce。
    - RetailGiftCard - 如果您计划使用礼品卡。
    - RetailInvent - 如果您计划使用库存。
    - RetailModernPos - 如果您计划使用销售点 (POS)。
    - RetailReplenishment - 如果您计划使用补货。
    - RetailScheduler
    - RetailStores - 如果您计划使用 POS。


## <a name="region-availability"></a>区域可用性
Commerce Scale Unit 可以在以下区域部署。

| 全球位置 | 区域              | 可用性        | 注释                  |
|-----------------|---------------------|---------------------|---------------------------|
| 美洲        | 美国东部             | 正式发布 |  没有评论。                         |
| 美洲        | 美国东部 2           | 正式发布 |  没有评论。                          |
| 美洲        | 美国中北部    | 有限容量    |  没有评论。                            |
| 美洲        | 美国中南部    | 有限容量    |  没有评论。                            |
| 美洲        | 美国中部          | 正式发布 |  没有评论。                            |
| 美洲        | 美国西部             | 正式发布 |  没有评论。                            |
| 美洲        | 美国西部 2           | 正式发布 |  没有评论。                            |
| 美洲        | 加拿大中部      | 有限容量    |  没有评论。                            |
| 美洲        | 加拿大东部         | 有限容量    |   没有评论。                           |
| 美洲        | 美国中西部     | 有限容量    |   没有评论。                           |
| APAC            | 澳大利亚东部      | 正式发布 |   没有评论。                           |
| APAC            | 东南亚      | 限制容量 | 不允许部署。    |
| APAC            | 日本东部          | 正式发布 |  没有评论。                            |
| APAC            | 日本西部          | 正式发布 |   没有评论。                           |
| APAC            | 澳大利亚东南地区 | 正式发布 |   没有评论。                           |
| APAC            | 东亚           | 有限容量    |   没有评论。                           |
| APAC            | 印度南部         | 限制容量 | 不允许部署。    |
| APAC            | 印度中部       | 有限容量    | 需要审批流程。 |
| EMEA            | 西欧         | 正式发布    |  没有评论。 |
| EMEA            | 欧洲北部        | 正式发布    |  没有评论。 |
| EMEA            | 英国南部            | 正式发布 |    没有评论。                          |
| EMEA            | 英国西部             | 正式发布 |    没有评论。                          |

有限容量区域的部署容量会受到极大限制。 将根据具体情况对部署请求进行评估。 如果您对在容量有限的区域进行部署有迫切的业务需求，您可以提交支持请求以加入等待列表。 限制容量区域目前不允许部署 Commerce Scale Unit。 

![显示区域可用性的地图。](media/Commerce-Scale-Unit-Region-Availability.png "显示区域可用性的地图")

## <a name="initialize-commerce-scale-unit-as-part-of-a-new-environment-deployment"></a>作为新环境部署的一部分初始化 Commerce Scale Unit

请确保总部可用。 这是在初始化过程中向总部登记缩放单元的必需条件。 不建议在总部提供服务时初始化缩放单元，因为在服务过程中总部可能不可用。

1. 确保总部环境可用且未处于[维护模式](../sysadmin/maintenance-mode.md)。
2. 在 LCS 中，在环境详细信息页上，选择 **环境功能 \> Commerce**。
3. 在 Commerce 设置部署页面上，选择 **初始化**。
4. 选择要初始化的 Commerce Scale Unit 的版本。
5. 选择要在其中初始化 Commerce Scale Unit 的区域。

## <a name="configure-channels-to-use-commerce-scale-unit"></a>配置渠道以使用 Commerce Scale Unit

部署 Commerce Scale Unit 后，您必须确保您的渠道已配置为为其使用数据库。 

要配置渠道以使用 Commerce Scale Unit 数据库，请按照这些步骤操作。

1. 在 Commerce Headquarters 中，转到 **Retail 和 Commerce \> Headquarters 设置 \> Commerce 计划程序 \> 渠道数据库**。
1. 在左侧窗格中，选择一个渠道数据库。
1. 在 **零售渠道** 快速选项卡上，选择 **添加**，然后在下拉列表中选择您的零售渠道。
1. 选择 **添加**，然后在下拉列表中选择您的在线渠道。 

完成后，转到 **Retail 和 Commerce \> Retail 和 Commerce IT \> 配送计划**，运行作业 9999。

> [!NOTE] 
> 作业 9999 会将所有新产品和客户同步到 Commerce Scale Unit。 此过程可能需要很长时间。 如果渠道必须只能用于电子商务站点构建器配置，您可以运行作业 1070 而不是作业 9999。

### <a name="database-refresh-and-commerce-scale-units"></a>数据库刷新和 Commerce Scale Unit

在开始之前，请确保您熟悉[为使用 Commerce 功能的环境刷新数据库后要完成的步骤](../database/database-refresh.md)。

缩放单元渠道数据库记录（在“渠道数据库”窗体中）无法作为数据库刷新的一部分跨环境移动。 这是因为记录代表环境的特定配置。

数据库刷新后，您可以通过在 LCS 中分配缩放单元的重新部署来重新生成缩放单元的渠道数据库记录。 如果检测到缺少登记，缩放单元中的任何部署或服务操作都将尝试向总部登记缩放单元。

您可以通过选择部署您的缩放单元已经处于的同一版本来分配缩放单元的重新部署，而无需更改任何组件。 这可以通过以下步骤在 LCS 中完成：

1. 在 LCS 中，在环境详细信息页上，选择 **环境功能 \> Retail**。
2. 在设置部署页上，选择要重新部署的缩放单元。
3. 在缩放单元的操作菜单上，选择 **更新**。
4. 在滑块上，在 **选择版本** 下拉列表中，选择 **指定版本** 选项。
5. 在 **指定版本** 下的文本框中，键入为缩放单元显示的版本，它将显示在 **当前版本** 标签旁边。
6. 单击 **更新** 按钮。

即使您之前已应用扩展，您也无需选择 **更新扩展**，因为在更新缩放单元时会自动选择应用到缩放单元的最后一个扩展包。

如果您有多个缩放单元，您需要为每个缩放单元执行上面的操作。 如果需要，您可以并行执行这些操作。

## <a name="deploy-additional-commerce-scale-units-optional"></a>部署其他 Commerce Scale Unit（可选）

初始化 Commerce Scale Unit 后，如果您的许可证具备权限，您可以自行部署第二个 Scale Unit。 要部署两个以上的 Scale Unit，您必须创建支持请求。 在支持请求中，说明您需要的 Commerce Scale Unit 数量、环境名称和所需区域。 有关许可的详细信息，请参阅 [Dynamics 365 许可指南](https://go.microsoft.com/fwlink/?LinkId=866544&clcid=0x409)。 

对于您额外部署的每个 Commerce Scale Unit，我们建议您通过执行这些步骤创建单独的渠道数据库组。

1. 在 Commerce 总部，转到 **Retail 和 Commerce > Retail Headquarters > 零售调度设置 > 渠道数据库组**。
2. 新建渠道数据库组。
3. 转到 **Retail 和 Commerce > Retail Headquarters > 零售调度设置 > 渠道数据库**，然后选择与新创建的 Commerce Scale Unit 对应的渠道数据库。
4. 选择 **编辑**，选择新的渠道数据库组。
5. 选择 **保存**。
6. 为选定的渠道数据库选择 **运行完全数据同步**。

## <a name="additional-considerations-if-you-initialize-cloud-hosted-commerce-channel-components-in-an-existing-environment"></a>在现有环境中初始化云托管的 Commerce 渠道组件的其他注意事项

如果您已在环境中使用云托管的 Commerce 渠道组件，初始化 Commerce Scale Unit 将有助于在更新这些组件时减少停机时间。 在初始化 Commerce Scale Unit 之前需要进行其他计划。

当您在使用云托管的 Commerce 渠道组件的环境中初始化第一个 Commerce Scale Unit 时，初始化过程会将与云托管渠道组件关联的渠道迁移到第一个缩放单元。 与商店缩放单元关联的渠道不会受影响。

迁移过程对渠道是透明的。 缩放单元初始化开始后，将自动执行以下操作：

1. 将创建一个新的 Commerce Scale Unit，并与环境关联。
2. Commerce Scale Unit 将登记为总部中的可用渠道数据库。
3. 映射到总部中 **默认** 渠道数据库的所有渠道都将更新以映射到新的 Commerce Scale Unit。
4. 将执行 Commerce Data Exchange (CDX) 完全数据同步以将渠道数据引入新的缩放单元。

**Commerce Scale Unit 初始化的计划和测试** 作为一般规则，在初始化 Commerce Scale Unit 时，您必须为商店运营以及使用 Retail Server 或云销售点的任何电子商务渠道运营计划五小时的停机窗口期。

1. 执行从生产环境到沙盒 UAT 环境的数据库刷新。 
2. 在沙盒 UAT 环境中初始化 Commerce Scale Unit。 
3. 注意 Commerce Scale Unit 完成初始化的时间。 这将与此操作在您的生产环境中花费的时间相当，在此期间商店运营和电子商务运营将不可用。

在初始化 Commerce Scale Unit 之前，您必须执行以下的其他步骤。

- **结束所有 POS 班次** - 迁移后，POS 用户将无法结束迁移过程中活动的任何班次。
- **验证所有 P 作业是否已全部成功完成** - 建议在 CSU 初始化之前完成同步待处理交易记录的 P 作业。
- **注销所有 POS 设备** - 迁移期间不支持 POS 操作。
- **在 POS 撤回和取消所有暂停的交易记录** - 暂停的交易不会作为初始化的一部分保留。

> [!IMPORTANT]
> 作为 Commerce Scale Unit 初始化的一部分，先前已暂停的交易记录将丢失，无法撤回。 

以下是初始化期间发生的变化：

- 云托管的 Commerce 渠道不工作，除非您启用 POS 离线功能。
- 启用脱机功能的 POS 设备的功能将会减少。
- 任何依赖 Retail Server 的电子商务客户端都将中断。
- 在 Commerce Scale Unit 上托管（自托管）的渠道不会受影响。
- 总部功能不受影响。

以下是初始化完成后发生的变化：

- 保留所有已激活 POS 设备的设备激活状态，这意味着不必重新激活这些设备。
- 独立硬件站实例将继续工作。
- POS 渠道端报表将重置，不会显示初始化前的数据。
- 显示日记帐操作也将重置，不会显示初始化前的数据。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
