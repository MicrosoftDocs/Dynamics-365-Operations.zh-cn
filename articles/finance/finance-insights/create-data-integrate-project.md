---
title: 创建数据集成器项目（预览）
description: 此主题介绍如何创建数据集成器项目。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 0029e093f524c61ff17a480ee3b881b3994ba95a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009435"
---
# <a name="create-a-data-integrator-project-preview"></a>创建数据集成器项目（预览）

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

此主题介绍如何创建数据集成器项目。

1. 登录到 Microsoft Dynamics 365 Finance。
2. 转到 **工作区 \> 数据管理**，然后选择 **数据实体**。 等至所有数据实体都已刷新，然后再继续下一步。
3. 打开 [Power Apps 门户](https://make.powerapps.com/)，然后按照以下步骤操作：

    1. 选择相应环境。
    2. 在左侧导航窗格中，选择 **数据 \> 连接**。
    3. 连接到以下各项的相应实例：

        - Dynamics 365
        - Dynamics 365 for Fin & Ops

4. 打开 [Power Apps 环境](https://admin.powerapps.com/environments)，然后按照以下步骤操作：

    1. 选择 **数据集成器**。
    2. 选择 **连接集**。
    3. 选择 **新建连接集**。
    4. 输入连接名称。
    5. 为以下项选择相应连接：

        - Dynamics 365
        - Dynamics 365 for Fin & Ops

    6. 选择相应组织映射。
    7. 选择 **创建**。

5. 打开 [Power Apps 环境](https://admin.powerapps.com/environments)，然后按照以下步骤操作：  

    1. 通过使用刚创建的连接集，为以下模板创建数据集成项目：

        - 客户付款见解结果（CDS 到 Fin and Ops）
        - 现金流时序结果（CDS 到 Fin 和 Ops）
        - 预算时序结果（CDS 到 Fin 和 Ops）

    2. 为每个项目设置相应计划。

> [!NOTE]
> 如果在 CDS 中未看到所需实体，请转到 **信用和收款 > 设置 > Finance Insights > Finance insights 参数**，启用客户付款预测功能，然后单击 **创建预测模型** 按钮。 当 AI 模型部署完成（成功或失败）后，将在 CDS 中部署创建集成所需的 CDS 实体。

## <a name="privacy-notice"></a>隐私声明

预览版 (1) 采用的隐私和安全措施可能比 Dynamics 365 Finance and Operations 服务少，(2) 不包含在该服务的服务级别协议 (SLA) 中，(3) 不应用于处理应遵守法律或法规合规性要求的个人数据或其他数据，以及 (4) 享受有限支持。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]