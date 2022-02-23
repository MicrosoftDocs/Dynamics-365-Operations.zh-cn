---
title: 将 Dynamics 365 Supply Chain Management（资产管理）与 Dynamics 365 Guides 集成
description: 本主题说明如何将 Microsoft Dynamics 365 Supply Chain Management 中的资产管理模块与 Dynamics 365 Guides 集成，以便在日常服务和维护工作流中利用混合现实指南。
author: kamaybac
manager: tfehr
ms.date: 04/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2020-04-28
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: f9ee7f1af8e88f56589c84bfaa063ea005aa353a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4422827"
---
# <a name="integrate-dynamics-365-supply-chain-management-asset-management-with-dynamics-365-guides"></a>将 Dynamics 365 Supply Chain Management（资产管理）与 Dynamics 365 Guides 集成

您可以将 Microsoft Dynamics 365 Supply Chain Management 中的 **资产管理模块** 与 Dynamics 365 Guides 集成，以便在日常服务和维护工作流中利用混合现实指南。 如果指南与资产管理工作订单相关联，则在 Supply Chain Management (Dynamics 365) 移动应用中打开工作订单的维护清单的工作人员会发现指南可用。 然后，工作人员可以在 Dynamics 365 Guides HoloLens 应用中查找并打开该指南。

## <a name="prerequisites"></a>先决条件

在将指南附加到资产管理工作订单之前，您必须满足以下先决条件：

- [设置 Dynamics 365 Supply Chain Management](../../fin-ops-core/fin-ops/index.md) 10.0.9 或更高版本。
- [为 Supply Chain Management 应用打开双重写入](../../fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write.md)。
- 针对 **MRGuidesFeature** 功能[打开发布外部测试版](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md#features-flighted-in-data-management-and-enabling-flighted-features)。 （对于生产环境，您必须首先提交支持票证，才能将您的租户添加到外部测试组。）
- 在 **许可证配置** 页面上，[打开以下配置密钥](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/license-code-and-configuration-key-reference)：

    - 资产管理 \> 资产管理混合现实
    - 混合现实 \> 混合现实指南

- [设置 Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) 200.0.0.96 或更高版本。

## <a name="use-dynamics-365-guides-with-asset-management"></a>将 Dynamics 365 Guides 与资产管理配合使用

要关联指南，请使用资产管理中的维护清单行。 您可以通过维护清单模板、维护作业类型或工作订单创建关联，因为这三项全都包含维护清单行。 您可以使用模板来节省时间，因为模板可以与使用它的所有维护作业类型相关联。 例如，与维护作业类型相关联的指南会自动与指定该作业类型的所有工作订单相关联。 另一方面，工作订单仅存在直接与该工作订单相关联的指南。

### <a name="associate-a-guide-with-a-maintenance-checklist-template"></a>将指南与维护清单模板关联

要将指南与维护清单模板关联，请执行以下步骤。

1. 使用 Dynamics 365 Guides PC 和 HoloLens 应用创建指南。 有关如何创建指南的信息，请参阅以下主题：

    - [使用 PC 应用创建指南](https://docs.microsoft.com/dynamics365/mixed-reality/guides/pc-app-overview)
    - [使用 HoloLens 应用放置全息影像](https://docs.microsoft.com/dynamics365/mixed-reality/guides/hololens-app-overview)

1. 在 Supply Chain Management 中，[创建维护清单模板](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-checklist-template)。
1. 将您创建的指南与新维护清单模板中的维护清单行相关联：

    1. 在 **维护清单行** 快速选项卡上，选择要与指南关联的行。
    1. 在 **关联的指南** 快速选项卡上，选择 **添加指南**。

        ![将指南与维护清单行关联](media/am-guides-integration-add-guide.png "将指南与维护清单行关联")

    1. 在 **名称** 字段中，选择指南，然后选择 **保存**。

        ![在“名称”字段中选择指南](media/am-guides-integration-select-guide.png "在“名称”字段中选择指南")

1. 将维护清单模板与作业类型关联：

    1. [创建维护作业类型](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-job-type)，或选择现有的维护作业类型。
    1. 在操作窗格上，选择 **维护作业类型默认值**。

        ![维护作业类型默认值按钮](media/am-guides-integration-job-defaults.png "维护作业类型默认值按钮")

    1. 创建一个行，然后选择 **保存**。

        ![创建行](media/am-guides-integration-add-line.png "创建行")

    1. 在操作窗格上，选择 **维护清单**。

        ![维护清单按钮](media/am-guides-integration-maintenance-checklist.png "维护清单按钮")

    1. 在 **维护清单行** 快速选项卡上，添加一个行，然后将 **类型** 字段的值更改为 **模板**。

        ![更改类型值](media/am-guides-integration-checklist-lines.png "更改类型值")

    1. 在 **行详细信息** 快速选项卡上的 **模板** 字段中，选择与指南关联的模板，然后选择 **保存**。

        ![选择模板](media/am-guides-integration-checklist-line-details.png "选择模板")

1. [创建工作订单](work-orders/manually-created-workorders.md#create-work-order)，然后选择使用与指南相关联的维护清单模板的维护作业类型。 指南会自动与工作订单关联。

    ![选择维护作业类型](media/am-guides-integration-create-work-order.png "选择维护作业类型")

1. 查看与工作订单和工作人员相关联的指南：

    1. 打开[资产管理移动工作区](asset-management-mobile-workspace.md)以访问工作订单。
    1. 针对此工作订单，[打开维护清单](asset-management-mobile-workspace.md#view-maintenance-checklist-on-a-work-order-job)。
    1. 选择清单行以查看关联的指南。

        ![与清单行关联的指南](media/am-guides-integration-show-guide.png "与清单行关联的指南")

    1. 在 HoloLens 上打开指南。

        ![在 HoloLens 上打开指南](media/am-guides-integration-hololens-select.png "在 HoloLens 上打开指南")

> [!NOTE]
> 您也可以直接在工作订单或工作类型的维护清单中关联指南。

> [!IMPORTANT]
> 存在一个已知问题，即，当您将维护清单模板与默认的维护作业类型相关联时，链接到该模板的指南不会出现在 **维护作业类型默认值** 页面的 **关联的指南** 快速选项卡上。 但是，在将该作业类型应用于 **关联的指南** 快速选项卡上的工作订单后，将会显示该指南。

## <a name="see-also"></a>请参阅

- [双写入概览](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview.md)
- [资产管理概览](index.md)
