---
title: 创建数据集成项目
description: 本文介绍如何创建数据集成项目。
author: ShivamPandey-msft
ms.date: 05/06/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 4ff4f88c6c5d55d853aebd7d437bfb107292fb2f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8876231"
---
# <a name="create-a-data-integration-project"></a>创建数据集成项目

[!include [banner](../includes/banner.md)]

本文介绍如何创建数据集成项目。

1. 登录 Microsoft Dynamics 365 Finance。
2. 转到 **工作区 \> 数据管理**，然后选择 **数据实体**。 等至所有数据实体都已刷新，然后再继续下一步。
3. 打开 [Power Apps 门户](https://make.powerapps.com/)，然后按照以下步骤操作：

    1. 选择相应环境。
    2. 在左侧导航窗格中，选择 **Dataverse \> 连接**。
    3. 连接到以下各项的相应实例：

        - Dynamics 365
        - Dynamics 365 for Fin & Ops

4. 打开 [Power Apps 环境](https://admin.powerapps.com/environments)，然后按照以下步骤操作：

    1. 选择 **数据集成**。
    2. 选择 **连接集**。
    3. 选择 **新建连接集**。
    4. 输入连接名称。
    5. 为以下项选择相应连接：

        - Dynamics 365
        - Dynamics 365 for Fin & Ops

    6. 选择相应组织映射。
    7. 选择 **创建**。

5. 打开 [Power Apps 环境](https://admin.powerapps.com/environments)，然后按照以下步骤操作：  

    1. 通过使用刚创建的连接集，为以下每个模板创建单一数据集成项目：

        - 客户付款见解结果（CDS 到 Fin and Ops 10.0.17+）
        - 现金流时序结果（CDS 到 Fin 和 Ops）
        - 预算时序结果（CDS 到 Fin 和 Ops）

      > [!NOTE]
      > 为每个模板创建多个数据集成项目可能会导致阻止更新的错误。

    2. 为每个项目设置相应计划。

> [!NOTE]
> 如果在 Dataverse 中未看到所需实体，请转到 **信用和收款** > **设置** > **Finance Insights** > **Finance insights 参数**，启用 **客户付款预测** 功能，然后选择 **创建预测模型**。 当 AI 模型部署完成后，将部署创建集成所需的 Dataverse 实体。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
