---
title: 清除项目评估
description: 本主题提供有关在项目评估完成后清除项目评估的信息。
author: kfend
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: eb323bdeb2a4701cdc9383b8da29e05a4cab107c
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410194"
---
# <a name="eliminate-a-project-estimate"></a>清除项目评估

[!include [banner](../includes/banner.md)]

项目评估提供为项目估计和计划的工作的财务观点。 若要使用某一项目的评估，则必须将该项目附加到某一评估项目。 评估项目始终基于现有项目，但是，多个项目可以引用单个评估项目。 只能附加固定价格项目和投资项目来评估项目，并且这些项目必须与评估项目属于同一项目组。

若要清除评估项目，该项目必须已完成。 以下步骤说明如何清除评估。

1. 转到**项目管理与核算** > **所有项目**，打开项目。 
2. 在**管理**选项卡上，选择**评估**，然后在**评估**页面上选择**评估**。
3. 在**常规**选项卡上的**清除评估**页面，设置以下选项：

   - **期间代码**：选择期间代码以挑选相应的评估项目。 
   - **评估日期**：选择有关的评估日期以进行清除。
   - **WIP 消除警告**：启用此选项可在清除与进行中的工作 (WIP) 关联的评估时提供通知。 如果未启用此选项，如果存在任何未评估的交易，将无法继续清除。 
   > [!NOTE]
   > 仅当对评估项目应用清除时，此选项才可用。 如果您使用的定期过帐，它不可用。 此设置在**存在未估计的交易时允许清除**字段组中，与**项目参数**页面上**评估**选项卡上的设置一起使用。
   - **将阶段设置为已完成**：启用此选项可在运行清除后将评估项目的阶段设置为**已完成**。
   - **打印评估列表**：选择在打印评估列表时所要包括的信息。
   - **显示信息日志**：启用此选项可以显示信息日志。
   - **过帐日期**：选择评估的分类帐过帐日期。

4.  选择**确定**。
5. 清除流程完成后，清除的评估项目将显示，其中包含负值。 

如果您不打算清除评估，您可以选择清除的评估，然后选择**反向清除**。   
