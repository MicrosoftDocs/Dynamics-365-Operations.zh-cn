---
title: Regulatory Configuration Service (RCS) - 删除 RCS 环境
description: 本主题说明了 Regulatory Configuration Service (RCS) 系统管理员可以如何删除 RCS 环境和相关数据。
author: JaneA07
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Global
audience: Application User, System Admin
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2021-01-01
ms.dyn365.ops.version: AX 10.0.15
ms.openlocfilehash: 637962cf63bfd8c2330726f33545f939ec91d58d
ms.sourcegitcommit: dbffde1944b9d037124415c28053036c9ef1ecb7
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/23/2021
ms.locfileid: "6295810"
---
# <a name="regulatory-configuration-service-rcs---delete-an-rcs-environment"></a>Regulatory Configuration Service (RCS) - 删除 RCS 环境

[!include [banner](../includes/banner.md)]

本主题说明了 Regulatory Configuration Service (RCS) 系统管理员可以如何删除 RCS 环境和相关数据。

在完成本主题中的过程之前，必须满足以下先决条件：

- 您必须拥有为 RCS 环境分配给您的 **系统管理员** 角色。
- **系统管理员** 角色必须具有分配给它的 **RCSDeleteEnvironmentDuty** 角色。

## <a name="delete-an-rcs-environment"></a>删除 RCS 环境

1. 打开 RCS，然后选择 **电子申报** 工作区磁贴。
2. 在 **相关链接** 部分中，选择 **删除 RCS 环境**。

    ![相关链接部分中的删除 RCS 环境链接](media/01_RCS-Delete-Environ-Related-Link.PNG)

3. 在显示的对话框中，查看有关环境删除的范围的消息。

    ![删除 RCS 环境对话框中的消息](media/01_RCS-Delete-Environ-Msg_noGUID.PNG)

    > [!IMPORTANT]
    > 无法撤销 RCS 环境的删除。
    >
    > 该操作会删除选定的 RCS 环境和任何相关数据，包括存储在全局存储库中的功能和配置。 如果没有依赖关系，与其他组织共享的功能和配置将取消共享并删除。 具有依赖关系的功能和配置将标记为已停用。

4. 在提供的字段中，输入 RCS 环境的全局唯一标识符 (GUID) 以确认您要删除它。 环境的 GUID 包含在删除消息中。
5. 选择 **删除环境**。
    
现在将删除您的 RCS 环境和任何相关数据。

> [!IMPORTANT]
> 删除 RCS 环境后，将无法恢复数据。 可以在任何可用的 RCS 区域中创建新的 RCS 环境。
