---
title: Lifecycle Services 的双写入设置
description: 本主题说明如何从 Microsoft Dynamics Lifecycle Services (LCS) 设置双写入连接。
author: RamaKrishnamoorthy
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: e51b4ef1e309e5f89dc82a3776b88c505dc6593d
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748533"
---
# <a name="dual-write-setup-from-lifecycle-services"></a>Lifecycle Services 的双写入设置

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

此主题介绍如何从 Microsoft Dynamics Lifecycle Services (LCS) 设置新 Finance and Operations 环境与新 Dataverse 环境之间的双写入连接。

## <a name="prerequisites"></a>先决条件

您必须是管理员才能设置双写入连接。

+ 您必须有权访问该租户。
+ 您必须同时是 Finance and Operations 环境和 Dataverse 环境中的管理员。

## <a name="set-up-a-dual-write-connection"></a>设置双写入连接

按照以下步骤设置双写入连接。

1. 在 LCS 中，转到您的项目。
2. 选择 **配置** 部署新环境。
3. 选择版本。 
4. 选择拓扑。 如果只有一种拓扑可用，将自动选择该拓扑。
5. 完成 **部署设置** 向导中的第一批步骤。
6. 在 **Dataverse** 选项卡中，执行以下步骤之一：

    - 如果已经为您的租户预配了一个 Dataverse 环境，可以选择该环境。

        1. 将 **配置 Dataverse** 选项设置为 **是**。
        2. 在 **可用环境** 列中，选择要与您的 Finance and Operations 数据集成的环境。 此列表中包含您拥有其管理员权限的所有环境。
        3. 选中 **同意** 复选框表示您同意条款和条件。

        ![Dataverse 选项卡，如果已经为您的租户预配了一个 Dataverse 环境](../dual-write/media/lcs_setup_1.png)

    - 如果您的租户还没有 Dataverse 环境，将预配一个新环境。

        1. 将 **配置 Dataverse** 选项设置为 **是**。
        2. 输入 Dataverse 环境的名称。
        3. 选择要在其中部署环境的区域。
        4. 选择环境的默认语言和货币。

            > [!NOTE]
            > 以后不能更改语言和货币。

        5. 选中 **同意** 复选框表示您同意条款和条件。

        ![Dataverse 选项卡，当租户还没有 Dataverse 环境时](../dual-write/media/lcs_setup_2.png)

7. 完成 **部署设置** 向导中的其余步骤。
8. 环境的状态为 **已部署** 之后，打开环境详细信息页。 **Power Platform 集成** 部分显示链接的 Finance and Operations 环境和 Dataverse 环境的名称。

    ![Power Platform 集成部分](../dual-write/media/lcs_setup_3.png)

9. Finance and Operations 环境管理员必须登录 LCS 并选择 **链接到面向应用程序的 CDS** 以完成链接。 环境详细信息页中显示管理员的联系信息。

    完成链接之后，将把状态更新为 **已成功完成环境链接**。

10. 若要在 Finance and Operations 环境中打开 **数据集成** 工作区和控制可用模板，请选择 **链接到面向应用程序的 CDS**。

    ![Power Platform 集成部分的“链接到面向应用程序的 CDS”按钮](../dual-write/media/lcs_setup_4.png)

> [!NOTE]
> 不能使用 LCS 取消链接环境。 若要取消链接环境，请在 Finance and Operations 环境中打开 **数据集成** 工作区，然后选择 **取消链接**。



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]