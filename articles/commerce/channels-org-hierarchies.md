---
title: 设置组织层次结构
description: 本文描述如何在 Microsoft Dynamics 365 Commerce 中设置组织层次结构。
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
ms.openlocfilehash: 01ba05566e966eb62a4df0b7b97ee3a442027936
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8847672"
---
# <a name="set-up-organization-hierarchies"></a>设置组织层次结构

[!include [banner](includes/banner.md)]

本文描述如何在 Microsoft Dynamics 365 Commerce 中设置组织层次结构。

在创建渠道之前，您需要确保已设置组织层次结构。

可以使用组织层次结构从自各种视角查看和申报业务。 例如，您可以针对纳税、法律或法定申报设置一种层次结构。 然后，您可以设置另一层次结构，以报告不是法律要求但用于内部报表的财务信息。

在创建某一组织层次结构之前，必须先创建组织。 有关详细信息，请参阅[创建法人](channels-legal-entities.md)或[创建运营单位](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json)。


有关详细信息，请参阅以下文章。
- [组织和组织层次结构概览](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)
- [规划组织层次结构](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)
- [创建组织层次结构](../fin-ops-core/fin-ops/organization-administration/tasks/create-organization-hierarchy.md?toc=/dynamics365/commerce/toc.json)

## <a name="create-an-organizational-hierarchy"></a>创建组织层次结构

若要创建组织层次结构，请按照下列步骤操作。

1. 在导航窗格中，转到 **模块 \> Retail and Commerce \> 渠道设置 \> 组织层次结构**。
1. 在操作窗格上，选择 **新建**。
1. 在 **名称** 字段中，输入一个值。
1. 在 **用途** 部分中，选择 **分配用途**。
1. 在列表中，找到并选择所需记录。 选择分配给组织层次结构的用途。
1. 在 **已分配层次结构** 部分中，选择 **添加**。
1. 在列表中，标记所选的行。 查找您刚才创建的层次结构。
1. 选择 **确定**。

下图显示了为商店的虚拟“Adventure Works”组创建的组织层次结构示例。

![组织层次结构示例。](media/organizational-hierarchies.png)

### <a name="add-organizations-to-a-hierarchy"></a>将组织添加到层次结构

若将组织添加到层次结构，请执行以下步骤。

1. 在列表中，找到并选择所需记录。 选择层次结构。
1. 在操作窗格上，选择 **查看**。
1. 根据需要添加组织。
1. 要添加组织，请选择 **编辑**，然后选择 **插入**。 在进行更改后，您可以保存草稿和发布更改。

下图显示了在层次结构根位置添加的法人，并为“购物中心”、“出口”、“在线”和“呼叫中心”渠道添加了四个成本中心。 然后可以将各种零售、呼叫中心和在线渠道添加到每个成本中心。

![层次结构设计器示例。](media/hierarchy-designer.png)

## <a name="additional-resources"></a>其他资源

[组织和组织层次结构概览](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[规划组织层次结构](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[创建法人](channels-legal-entities.md)

[创建运营单位](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json)

[渠道概览](channels-overview.md)

[渠道设置先决条件](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
