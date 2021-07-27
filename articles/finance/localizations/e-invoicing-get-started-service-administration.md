---
title: 开始使用电子开票服务管理
description: 本主题说明如何开始使用电子开票。
author: gionoder
ms.date: 05/24/2021
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
ms.openlocfilehash: 8adbe577e5111a6a4afdba6aed32855b2e30b39b
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/03/2021
ms.locfileid: "6335682"
---
# <a name="get-started-with-electronic-invoicing-service-administration"></a>开始使用电子开票服务管理

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a>先决条件

在完成本主题中的过程之前，必须具备以下先决条件：

- 您必须有权访问您的 Microsoft Dynamics Lifecycle Services (LCS) 帐户。
- 您必须有包含版本 10.0.17 或更高版本的 Microsoft Dynamics 365 Finance 和 Dynamics 365 Supply Chain Management 的 LCS 项目。 此外，必须将这些应用部署在以下 Azure 地理区域之一：

    - 美国
    - 欧洲
    - 英国
    - 亚洲

- 您必须有权访问您的 Dynamics 365 Regulatory Configuration Services (RCS) 帐户。
- 您必须在“功能管理”中为 RCS 帐户激活全球化功能。 有关详细信息，请参阅 [Regulatory Configuration Services (RCS) - 全球化功能](rcs-globalization-feature.md)。
- 您必须在 Azure 中创建密钥保管库和存储帐户。 有关详细信息，请参阅[创建 Azure 存储帐户和密钥保管库](e-invoicing-create-azure-storage-account-key-vault.md)。

## <a name="install-the-add-in-for-microservices-in-lifecycle-services"></a>在 Lifecycle Services 中安装微服务的加载项

1. 登录您的 LCS 帐户，在 LCS 项目仪表板上选择一个 LCS 项目。
2. 在该项目中，在环境仪表板上，选择您的 LCS 部署项目。 您选择的项目必须在运行。
3. 在 **Power Platform 集成** 选项卡上，在 **环境加载项** 字段组中，选择 **安装新加载项**。
4. 选择 **电子开票**。
5. 在 **AAD 应用程序 ID** 字段中，输入 **091c98b0-a1c9-4b02-b62c-7753395ccabe**。 这是一个固定值。
6. 在 **AAD 租户 ID** 字段中，输入您的 Azure 订阅帐户的租户 ID。
7. 查看条款和条件，然后选中相应的复选框。
8. 选择 **安装**。


## <a name="set-up-the-parameters-for-rcs-integration-with-electronic-invoicing"></a>为与电子开票的 RCS 集成设置参数

1. 登录您的 RCS 帐户。
2. 在 **电子申报** 工作区的 **相关链接** 部分中，选择 **电子申报参数**。
3. 在 **电子开票服务** 选项卡上，在 **服务终结点 URI** 字段中，为您的 Azure 地理位置输入适当的服务终结点，如下表所示。

    | 数据中心 Azure 地理位置 | 服务终结点 URI                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | 美国              | <p>`https://gw.us-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | 欧洲                     | <p>`https://gw.eu-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il110.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | 英国             | <p>`https://gw.uk-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.uk-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | 亚洲                       | <p>`https://gw.as-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.as-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |

4. 确认 **应用程序 ID** 字段设置为 **0cdb527f-a8d1-4bf8-9436-b352c68682b2**。 此值是一个固定值。
5. 在 **LCS 环境 ID** 字段中，输入您的 LCS 环境的 ID。
6. 选择 **保存**，然后关闭页面。

## <a name="create-key-vault-references"></a>创建密钥保管库参考

1. 登录您的 RCS 帐户。
2. 在 **全球化功能** 工作区的 **环境** 部分中，选择 **电子开票** 磁贴。
3. 在 **环境设置** 页上的操作窗格上，选择 **服务环境**，然后选择 **密钥保管库参数**。
4. 选择 **新建** 以创建密钥保管库参考。
5. 在 **名称** 字段中，输入密钥保管库参考的名称。 在 **描述** 字段中，输入描述。
6. 在 **密钥保管库 URI** 字段中，粘贴来自 Azure 密钥保管库的密钥保管库密码。 有关详细信息，请参阅[创建 Azure 存储帐户和密钥保管库](e-invoicing-create-azure-storage-account-key-vault.md)。
7. 选择 **保存**。

## <a name="create-storage-account-secret"></a>创建存储帐户密码

1. 在 **环境设置** 页面上的操作窗格上，选择 **服务环境** > **密钥保管库参数**。
2. 选择 **密钥保管库参考**，然后在 **证书** 部分中，选择 **添加**。
3. 在 **名称** 字段中，输入存储帐户密码的名称。 有关详细信息，请参阅[创建 Azure 存储帐户和密钥保管库](e-invoicing-create-azure-storage-account-key-vault.md)。
4. 在 **描述** 字段中，输入描述。
5. 在 **类型** 字段中，选择 **密码**。
6. 选择 **保存**，然后关闭页面。

## <a name="create-a-digital-certificate-secret"></a>创建数字证书机密

1. 在 **环境设置** 页面上的操作窗格上，选择 **服务环境**，然后选择 **密钥保管库参数**。
2. 选择 **密钥保管库参考**，然后在 **证书** 部分中，选择 **添加**。
3. 在 **名称** 字段中，输入数字证书机密的名称。 有关详细信息，请参阅[创建 Azure 存储帐户和密钥保管库](e-invoicing-create-azure-storage-account-key-vault.md)。
4. 在 **描述** 字段中，输入描述。
5. 在 **类型** 字段中，选择 **证书**。
6. 选择 **保存**，然后关闭页面。

## <a name="create-a-service-environment"></a>创建服务环境

1. 登录您的 RCS 帐户。
2. 在 **全球化功能** 工作区的 **环境** 部分中，选择 **电子开票** 磁贴。
3. 在 **环境设置** 页上的操作窗格上，选择 **服务环境**。
4. 选择 **新建** 创建新服务环境。
5. 在 **名称** 字段中，输入电子开票环境的名称。 在 **描述** 字段中，输入描述。
6. 在 **存储 SAS 令牌密码** 字段中，选择必须用于验证对存储帐户的访问权限的存储帐户机密的名称。
7. 在 **用户** 部分，选择 **添加** 添加允许通过环境提交电子发票并连接到存储帐户的用户。
8. 在 **用户 ID** 字段中，输入用户的别名。 在 **电子邮件** 字段中，输入用户的电子邮件地址。
9. 选择 **保存**。
10. 如果您的国家/地区特定发票需要证书链应用数字签名，请在操作窗格上，选择 **密钥保管库参数**，然后选择 **证书链**，并按照以下步骤操作：
    1. 选择 **新建** 创建证书链。
    2. 在 **名称** 字段中，输入证书链的名称。 在 **描述** 字段中，输入描述。
    3. 在 **证书** 部分，选择 **添加** 将证书添加到链中。
    4. 使用 **向上** 或 **向下** 按钮更改证书在链中的位置。
    5. 选择 **保存**，然后关闭页面。
    6. 关闭该页面。
11. 在 **服务环境** 页上的操作窗格上，选择 **发布** 将环境发布到云中。 **状态** 字段的值将更改为 **已发布**。

## <a name="create-a-connected-application"></a>创建连接的应用程序

1. 在 **环境设置** 页上的操作窗格上，选择 **相连应用程序**。
2. 选择 **新建** 创建连接的应用程序。
3. 在 **名称** 字段中，输入要连接的应用程序的名称。
4. 在 **应用程序** 字段中，输入要连接的 Finance 和 Supply Chain Management 环境的 URL。
4. 在 **租户** 字段中，输入 Finance 和 Supply Chain Management 环境的租户。
5. 选择 **保存**。
6. 在操作窗格上，选择 **检查连接** 测试与环境的连接。 然后关闭页面。

## <a name="link-connected-applications-to-environments"></a>将连接的应用程序链接到环境

1. 在 **环境设置** 页上，选择 **新建** 将连接的应用程序分配给环境。
2. 在 **相连应用程序** 字段中，选择一个连接的应用程序。
3. 在 **服务环境** 字段中，选择一个服务环境。
4. 选择 **保存**，然后关闭页面。

## <a name="set-up-electronic-invoicing-integration-in-finance-and-supply-chain-management"></a>在 Finance 和 Supply Chain Management 中设置电子开票集成

### <a name="turn-on-the-electronic-invoicing-integration-feature"></a>打开电子开票集成功能

1. 登录您的 Finance 或 Supply Chain Management 实例。
2. 在 **功能管理** 工作区中，搜索 **电子开票集成** 功能。 如果此功能未出现在页面上，请选择 **检查更新**。
3. 选择此功能，然后然后选择 **立即启用**。

### <a name="set-up-the-service-endpoint-url"></a>设置服务终结点 URL

1. 转到 **组织管理 \> 设置 \> 电子单据参数**。
2. 在 **提交服务** 选项卡上，在 **服务终结点 URL** 字段中，为您的 Azure 地理位置输入适当的服务终结点，如下表所示。

    | 数据中心 Azure 地理位置 | 服务终结点 URI                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | 美国              | <p>`https://gw.us-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | 欧洲                     | <p>`https://gw.eu-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il110.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | 英国             | <p>`https://gw.uk-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.uk-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | 亚洲                       | <p>`https://gw.as-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.as-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |

3. 在 **环境** 字段中，输入在电子开票中发布的服务环境的名称。
4. 选择 **保存**，然后关闭页面。

### <a name="enable-flighting-keys"></a>启用发布外部测试版密钥

为 Microsoft Dynamics 365 Finance 或 Microsoft Dynamics 365 Supply Chain Management 版本 10.0.17 或更早版本启用发布外部测试版密钥。 
1. 执行以下 SQL 命令：

    插入 SYSFLIGHTING（FLIGHTNAME，已启用）值（“BusinessDocumentSubmissionServiceEnabled”，1）
    
    插入 SYSFLIGHTING（FLIGHTNAME，已启用）值（“ElectronicInvoicingServiceIntegrationFeature”，1）

2. 执行所有 AOS 的 IISreset 命令。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
