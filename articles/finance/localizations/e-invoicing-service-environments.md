---
title: 服务环境
description: 本主题提供有关电子开票服务环境的信息并说明如何设置这些环境。
author: dkalyuzh
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: a8a135098f71e1413cd20ff8ad4003f090ae3407
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371516"
---
# <a name="service-environments"></a>服务环境

[!include [banner](../includes/banner.md)]

服务环境是为支持全球化功能以及在电子开票服务中处理的相应文档而创建的逻辑分区。 必须在服务环境级别配置安全机密和数字证书以及访问权限（治理）。

可以根据需要创建任意数量的服务环境。 您创建的所有服务环境都是相互独立的。 作为最佳做法，我们建议您至少创建两个服务环境：

- 一种环境主要用于开发和验证目的。 此环境通常是用户验收测试 (UAT) 环境。
- 一个环境用于生产目的。 此环境通常是生产环境。

此类型的分区有助于确保电子开票流程在投入生产之前在沙盒中得到验证和自定义。

必须在 Regulatory Configuration Service (RCS) 中创建和维护服务环境。 然后，当服务环境准备就绪时，必须被发布到电子开票服务。 发布流程将服务环境的参数从 RCS 实例发送到电子开票服务。

如果您在创建新服务环境或调整现有服务环境（例如，通过添加或删除用户或 Microsoft Azure Key Vault 机密）后未完成发布流程，更改将无效。 只有已发布的环境可以由 Dynamics 365 Finance 或 Dynamics 365 Supply Chain Management 访问。

## <a name="service-environment-statuses"></a>服务环境的状态

服务环境可以通过状态进行管理。 您可以在 **服务环境** 页面查看环境的状态。 具有以下状态：

- **未发布** – 环境已经创建，但尚未发布。
- **已发布** – 环境已发布到电子开票服务。
- **已更改** – 已发布环境的属性已更改，但更改尚未发布。

## <a name="users"></a>用户

每个服务环境必须列出可以从 Finance 或 Supply Chain Management 连接到电子开票的用户。

## <a name="applications"></a>应用程序

在某些情况下，Finance 或 Supply Chain Management 以外的应用程序可能必须连接到电子开票服务才能提交电子单据来进行进一步处理，或检索诸如单据提交状态等信息。 在这些情况下，应在应用程序列表中定义应用程序。 这样，应用程序将有权访问电子开票服务。 应用程序还必须在 Azure Active Directory (Azure AD) 中注册为应用程序，并且必须使用对象 ID 来加以标识。 

由于 Microsoft 需要对可以连接到电子开票服务的应用程序进行高级别的安全控制，因此您必须通过 <DGXRegulatoryservicesengineering@service.microsoft.com> 联系 Microsoft 并提供应用程序的以下详细信息：

- Azure AD 租户 ID
- Microsoft Dynamics Lifecycle Services (LCS) 环境 ID
- 应用程序 ID（客户端 ID）
- 对象 ID
- 应用程序的理由和高级描述

Microsoft 将评估请求并将应用程序注册到安全注册表中，以确保它可以使用电子开票进行操作。

## <a name="number-sequences"></a>编号规则

如果您的方案需要编号规则（例如，在文件名中），您可以使用为特定环境定义的编号规则，但可以跨全球化功能或特定全球化功能使用。 定义编号规则后，您可以在变量和处理管道中使用它。 要跟踪使用情况，在 **编号规则** 页面上，查找 **In use** 参数的 **Current** 值。

### <a name="working-with-number-sequences"></a>使用编号规则
在 **编号规则** 页面上： 

- 选择 **新建** 创建编号规则。 然后，输入名称和描述。 
- 选择 **删除** 可删除不再使用的编号规则。
- 您不必在操作窗格上选择 **发布** 来发布对编号规则的更改。 更新会自动完成。

## <a name="create-a-key-vault-reference"></a>创建 Key Vault 引用

1. 登录您的 RCS 帐户。
2. 在 **全球化功能** 工作区的 **环境** 部分中，选择 **电子开票** 磁贴。
3. 在 **环境设置** 页上的操作窗格上，选择 **服务环境**。
4. 在 **服务环境** 页面上的操作窗格上，选择 **Key Vault 参数**。
5. 在 **Key Vault 参数** 页面上，选择 **新建** 创建 Key Vault 引用。
6. 在 **名称** 字段中，输入 Key Vault 引用的名称。
7. 在 **描述** 字段中，输入描述。
8. 在 **Key Vault URI** 字段中，粘贴来自密钥保管库 (`https://<your key vault>.vault.azure.net/`) 的 Key Vault URI。 有关详细信息，请参阅[在 Azure 门户中创建 Azure 密钥保管库](e-invoicing-create-azure-key-vault-azure-portal.md)。
9. 选择 **保存**。
    
## <a name="create-a-secret-for-the-storage-account-secret-token"></a>为存储帐户机密令牌创建机密

1. 在 **Key Vault 参数** 页面上，选择您在上一个过程中创建的 Key Vault 引用，然后在 **证书** 部分，选择 **添加**。
2. 在 **名称** 字段中，输入存储帐户密码的名称。 此名称应与保留存储共享访问签名 (SAS) 令牌的 Key Vault 机密的名称相匹配。 有关详细信息，请参阅[在 Azure 门户中创建 Azure 存储帐户](e-invoicing-create-azure-storage-account-azure-portal.md)。 
3. 在 **描述** 字段中，输入描述。
4. 在 **类型** 字段中，选择 **密码**。
5. 选择 **保存**。
    
## <a name="create-a-service-environment"></a>创建服务环境

1. 在 **服务环境** 页面上，选择 **新建** 创建服务环境。
2. 在 **名称** 字段中，输入电子开票环境的名称。
3. 在 **描述** 字段中，输入描述。
4. 在 **存储 SAS 令牌密码** 字段中，选择必须用于验证对存储帐户的访问权限的存储帐户机密的名称。
5. 在 **用户** 部分，选择 **添加** 添加允许通过环境提交电子发票并连接到存储帐户的用户。
6. 在 **用户 ID** 字段中，输入用户的别名。 
7. 在 **电子邮件** 字段中，输入用户的电子邮件地址。
8. 选择 **保存**。
9. 在操作窗格上，选择 **发布** 将环境发布到电子开票服务。 验证 **状态** 字段的值是否已更改为 **已发布**。
