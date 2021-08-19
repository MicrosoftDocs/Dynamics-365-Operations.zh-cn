---
title: 将渠道添加到组织层次结构
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 中将渠道添加到组织层次结构。
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 64d9c649212eca4dc703e5b80fdf2c3c6a57a61745fc440b0650d7796a4d06e3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6720975"
---
# <a name="add-a-channel-to-an-organizational-hierarchy"></a>将渠道添加到组织层次结构


[!include [banner](includes/banner.md)]

此主题介绍如何在 Microsoft Dynamics 365 Commerce 中将渠道添加到组织层次结构。

## <a name="overview"></a>概览

渠道需要与一个或多个组织层次结构相关联。 在创建渠道之前，您需要确认已设置组织层次结构。  

参阅[组织层次结构](channels-org-hierarchies.md)，以了解有关如何创建组织层次结构的更多详细信息。

## <a name="select-a-hierarchy"></a>选择层次结构

若要选择层次结构，请按照下列步骤操作。

1. 在导航窗格中，转到 **模块 \> Retail and Commerce \> 渠道设置 \> 组织层次结构**。
1. 从列表中，选择要将渠道添加到的组织层次结构。
1. 在操作窗格上，选择 **查看** 以查看层次结构详细信息。

下图显示了所选层次结构的组织层次结构详细信息。

![所选层次结构的组织层次结构详细信息。](media/channel-add-to-org-hierarchy-1.png)

## <a name="add-a-channel-to-a-hierachy-node"></a>将渠道添加到层次结构节点

若要将渠道添加到层次结构节点，请执行以下步骤。

1. 在操作窗格上，选择 **编辑**。
1. 选择要将渠道添加到的层次结构节点，然后从 **插入** 下拉列表中选择 **零售渠道**。 
1. 选择要添加的渠道，然后选择 **确定** 按钮。
1. 在操作窗格上，选择 **保存**。
1. 在操作窗格上，选择 **发布** 并提供一个过去的 **生效日期** 以立即执行此操作。

下图显示了如何选择要添加到层次结构节点的渠道。

![选择要添加到层次结构节点的渠道。](media/channel-add-to-org-hierarchy-2.png)

下图显示了添加了各种渠道的层次结构。

![添加了各种渠道的层次结构。](media/channel-add-to-org-hierarchy-3.png)

## <a name="additional-resources"></a>其他资源

[渠道概览](channels-overview.md)

[渠道设置先决条件](channels-prerequisites.md)

[组织和组织层次结构概览](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[规划组织层次结构](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[组织层次结构](channels-org-hierarchies.md)

[设置零售渠道](channel-setup-retail.md)
    
[设置在线渠道](channel-setup-online.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]