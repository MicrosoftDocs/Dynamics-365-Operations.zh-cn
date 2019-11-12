---
title: 在 Attract 中创建流程模板
description: 此主题提供有关如何在 Attract 中创建流程模板的信息。
author: andreabichsel
manager: AnnBe
ms.date: 10/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: AX 8.1
ms.openlocfilehash: 533b9abd3d57c5bf8f3d9da85020c86012436f2f
ms.sourcegitcommit: dd991154231280aff9c9c5799e42799e2bfc02fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/15/2019
ms.locfileid: "2622710"
---
# <a name="create-a-process-template-in-attract"></a>在 Attract 中创建流程模板

[!include [banner](includes/banner.md)]

*招聘流程模板*包含应作为工作招聘流程的一部分包含的所有活动。 此主题描述 Microsoft Dynamics 365 Talent: Attract 中的流程模板元素。 它还介绍了如何创建模板。

> [!NOTE]
> 模板创建是 Attract 的综合招聘附件的一部分。

## <a name="template-management"></a>模板管理

组织可以决定是团队成员还是只有管理员可以在 Attract 中创建流程模板。 若要配置模板管理，请转到**管理员中心** \> **模板管理**。 要允许团队成员创建自己的模板，请打开模板管理。 如果未打开模板管理，只有管理员才能创建模板。

## <a name="default-template"></a>默认模板

只有管理员可以设置默认模板。 如果创建工作时未选择模板，将使用默认模板。 若要设置默认模板，请转到**管理员中心** \> **模板管理**。 在应是默认模板的模板的卡上，选择省略号按钮 (**...**)，然后选择**设置为默认值**。

## <a name="create-a-process-template"></a>创建流程模板

管理员、招聘人员和招聘经理可以创建流程模板。 流程模板包含*阶段*和*活动*。 阶段将一个或多个活动分组到一起。 默认情况下，每个流程模板具有应聘者、申请和聘约活动。 包含这些活动的阶段可以重命名。 您可以通过选择 **+ 新建阶段**来添加更多阶段。 您可以通过将活动拖动到相应的阶段或在活动列表中双击它们来将活动添加到阶段。

> [!NOTE]
> 阶段名称对**申请状态**页上的应聘者可见。 在您为阶段选择名称时应考虑此事实。

若要了解有关活动的详细信息，请参阅 [Attract 中的招聘流程活动](./activities-attract.md)。

请执行以下步骤创建招聘流程模板。

1. 转到**模板**。
2. 选择**新建**。
3. 在**模板名称**字段上，请输入模板的名称，然后选择**创建**。
4. 在**选择审核流程**列表中，请选择**默认**以要求审核工作。
5. 选择启用或禁用应聘者。
6. 可选：添加或删除阶段。

    - 若要添加阶段，请选择 **+ 新阶段**。
    - 若要删除阶段，将指针悬停在阶段上，然后选择出现的垃圾桶按钮。

        > [!NOTE]
        > 不能删除“应聘者”、“申请”和“聘约”阶段，但可以重命名。

7. 可选：添加或删除活动。

    - 要添加活动，请将其从右侧的活动列表拖到相应的阶段。 或者，双击活动，然后选择要添加到的阶段。
    - 若要删除活动，展开它，然后选择活动标题上的垃圾桶按钮。

8. 选择**保存**。
