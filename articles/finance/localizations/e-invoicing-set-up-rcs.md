---
title: 设置 Regulatory Configuration Service (RCS)
description: 本主题说明如何设置 Regulatory Configuration Service (RCS)。
author: dkalyuzh
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 33aab6f0a482ce3d90a7e9828015a8e7bebb7827
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371529"
---
# <a name="set-up-regulatory-configuration-service-rcs"></a>设置 Regulatory Configuration Service (RCS)

[!include [banner](../includes/banner.md)]

本主题说明如何设置 Regulatory Configuration Service (RCS)。

## <a name="turn-on-globalization-features"></a>开启全球化功能

1. 登录您的 RCS 帐户。
2. 选择 **功能管理** 磁贴。
3. 在 **功能管理** 工作区，在列表中选择 **全球化功能**，然后选择 **立即启用**。

**全球化功能** 工作区的磁贴现在应会出现在主 RCS 仪表板上。

## <a name="set-up-the-parameters-for-rcs-integration-with-electronic-invoicing"></a>为与电子开票的 RCS 集成设置参数

1. 在 **全球化功能** 工作区的 **相关设置** 部分中，选择 **电子报告参数**。
2. 在 **电子开票** 选项卡上，在 **服务终结点 URI** 字段中，为您的 Microsoft Azure 地理位置输入适当的服务终结点，如下表所示。

    | 数据中心 Azure 地理位置 | 服务终结点 URI |
    |----------------------------|----------------------|
    | 美国              | <p>`https://gw.us-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | 欧洲                     | <p>`https://gw.eu-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il110.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | 英国             | <p>`https://gw.uk-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.uk-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | 亚洲                       | <p>`https://gw.as-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.as-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | 日本                      | <p>`https://gw.jp-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |

3. 确认 **应用程序 ID** 字段设置为 **0cdb527f-a8d1-4bf8-9436-b352c68682b2**。 此值是一个固定值。 确保仅输入了全局唯一标识符 (GUID)，并且该值不包含任何其他符号，如空格、逗号、句点或引号。
4. 在 **LCS 环境 ID** 字段中，输入您的 Microsoft Dynamics Lifecycle Services (LCS) 环境的 ID。 此值是对您将用于电子开票服务的 Finance 或 Supply Chain Management 环境的引用。 要获取您的 ID，请登录 [LCS](https://lcs.dynamics.com/)，打开您的项目，然后在 **管理环境** 选项卡的 **环境详细信息** 部分，查看 **环境 ID** 字段。

    > [!IMPORTANT]
    > 如果电子开票加载项安装在 LCS 中的多个 Finance 或 Supply Chain Management 环境中，请始终使用最近安装的环境的环境 ID。 如果您决定在新环境中安装加载项，设置并使用电子开票功能后，将 RCS 中的 **LCS 环境 ID** 字段更新为最新值。

5. 选择 **保存**，然后关闭页面。

## <a name="configuration-providers"></a>配置提供方

您可以使用配置提供程序来区分电子开票流程中使用的电子报告 (ER) 配置的负责人和负责人全球化功能。 对于 Microsoft 提供并在全局存储库中发布的所有全球化功能，配置提供程序设置为 **Microsoft** (`http://microsoft.com`)。

您只能调整属于活动配置提供程序的 ER 配置和全球化功能。 您可以将这些配置和功能用作模板来创建属于活动配置提供程序的配置和功能，以便您可以调整它们。

首先，创建配置提供程序。 然后将其中一个设置为活动。 您不能将 **Microsoft** 配置提供程序设置为活动。

### <a name="create-a-configuration-provider"></a>创建配置提供程序

1. 在 **电子报告** 工作区的 **相关链接** 部分，选择 **配置提供程序**。
2. 选择 **新建**。
3. 在 **名称** 字段中，为配置提供程序输入唯一名称。
4. 在 **Internet 地址** 字段中，输入唯一的配置提供程序 URL。
5. 选择 **保存**，然后关闭页面。

### <a name="select-a-configuration-provider-as-active"></a>选择一个配置提供程序作为活动提供程序

1. 在配置提供程序列表中，选择要设置为活动的配置提供程序。
2. 选择 **设置有效**。

## <a name="import-er-configurations-from-the-global-repository"></a>从全局存储库导入 ER 配置

1. 在 **电子报告** 工作区的 **相关链接** 部分，选择 **配置提供程序**。
2. 在配置提供程序列表中，选择 **Microsoft**，然后选择 **存储库**。
3. 选择 **全局**，然后在操作窗格上，选择 **打开**。
4. 导入以下 ER 模型：

    - **客户发票上下文模型**
    - **发票模型**
    - **会计单据**（对于巴西场景，如果需要）
    - **响应消息模型**

5. 如果 **发票模型映射** 没有自动导入，请导入。
6. 关闭该页面。
