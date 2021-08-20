---
title: 使用电子开票服务导入供应商发票
description: 本主题提供有关如何使用电子开票服务导入供应商发票的信息。
author: gionoder
ms.date: 08/03/2021
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
ms.openlocfilehash: 434bf1f6a5a727a71592493b85ab166cbeff2f0980c2c968c99973a03f4dc660
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6751244"
---
# <a name="use-the-electronic-invoicing-service-to-import-vendor-invoices"></a>使用电子开票服务导入供应商发票

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

本主题提供的信息将帮助您开始使用电子开票服务导入供应商发票。 它指导您完成 Regulatory Configuration Services (RCS)、Dynamics 365 Finance 和 Dynamics 365 Supply Chain Management 中的配置步骤，您必须遵循这些步骤才能从供应商接收电子供应商发票。

## <a name="set-up-vendor-invoice-import-in-rcs"></a>在 RCS 中设置供应商发票导入
若要在 RCS 中设置供应商发票导入，请按照以下步骤操作：

1. 查阅[公开发布的电子发票功能](e-invoicing-configuration-rcs.md#generally-available-features)列表。
2. 选择并导出电子开票功能。 有关详细信息，请参阅[从 Microsoft 配置提供者导入电子开票功能](e-invoicing-get-started.md#import-an-electronic-invoicing-feature-from-the-microsoft-configuration-provider)。
3. 为您的组织创建电子开票功能。 有关详细信息，请参阅[在您的组织提供者下创建电子开票功能](e-invoicing-get-started.md#create-an-electronic-invoicing-feature-under-your-organization-provider)。

## <a name="configure-an-email-account-channel"></a>配置电子邮件帐户渠道

如果您创建的电子开票功能从通过电子邮件接收的附加文件导入电子供应商发票，则配置电子邮件帐户渠道。

1. 在 RCS 中，选择您创建的电子开票功能。 确保您选择 **草稿** 状态的版本。
2. 在 **设置** 选项卡上的网格中，选择功能设置，然后选择 **编辑**。
3. 在 **参数** 字段组中的 **数据渠道** 选项卡上，选择 **服务器地址** 并输入电子邮件帐户提供者。
4. 选择 **服务器端口** 并输入电子邮件帐户提供者使用的端口。
5. 选择 **用户名密码** 并输入包含电子邮件用户帐户 ID 的密钥保管库密钥的名称。
6. 选择 **用户密码** 并输入包含电子邮件用户帐户密码的密钥保管库密钥的名称。
7. 选择 **主题筛选器**。 查看并更新包含默认电子邮件主题的字符串，以标识包含要导入的电子供应商发票的电子邮件。
8. 必要时，在 **适用性规则** 选项卡上查看和更新条件。 有关详细信息，请参阅[适用性规则](e-invoicing-configuration-rcs.md#applicability-rules)。
9. 选择 **保存**，然后关闭页面。

### <a name="configure-a-microsoft-sharepoint-channel"></a>配置 Microsoft SharePoint 渠道

如果电子开票功能从放在 SharePoint 文件夹中的文件导入电子供应商发票，则配置 Microsoft SharePoint 渠道。

1. 在 RCS 中，选择您创建的电子开票功能。 确保您选择了 **草稿** 状态的 **版本**。
2. 在 **设置** 选项卡上的网格中，选择功能设置，然后选择 **编辑**。
3. 在 **参数** 字段组中的 **数据渠道** 选项卡上，选择 **SharePoint 地址** 并输入 SharePoint URL。
4. 选择 **服务器端口** 并输入电子邮件帐户提供者使用的端口。
5. 选择 **应用程序 ID** 并输入包含电子 SharePoint 客户端 ID 的密钥保管库密钥的名称。
6. 选择 **应用程序密钥** 并输入包含电子 SharePoint 客户端密码的密钥保管库密钥的名称。
7. 选择 **文件筛选器**。 查看并更新掩码以筛选包含要导入的电子供应商发票的文件。
8. 必要时，在 **适用性规则** 选项卡上查看和更新条件。 有关详细信息，请参阅[适用性规则](e-invoicing-configuration-rcs.md#applicability-rules)。
9. 选择 **保存**，然后关闭页面

### <a name="deploy-an-electronic-invoicing-feature"></a>部署电子开票功能

若要部署电子开票功能，请参阅[将电子开票功能部署到服务环境](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-service-environment)。

## <a name="set-up-vendor-invoice-import-in-finance-and-supply-chain-management"></a>在 Finance 和 Supply Chain Management 中设置供应商发票导入
完成以下两个部分中的步骤以设置不同类型的供应商发票导入。

### <a name="import-vendor-invoices-from-email"></a>从电子邮件中导入供应商发票

1. 登录到 Finance 或 Supply Chain Management 环境，确认您位于正确的法人中。
2. 转到 **组织管理** > **设置** > **电子单据参数**。
3. 在 **功能** 选项卡上，请确保选择了 **NF-e 联邦 - 巴西电子发票**。
4. 在 **外部渠道** 选项卡上的 **渠道** 字段组中，选择 **添加**。
5. 在 **渠道** 字段中，输入 **NFe**（在 RCS 中电子发票功能的数据渠道配置中给出的渠道名称）。
6. 在 **描述** 字段中，输入描述。 在 **公司** 字段中，选择相应法人。
7. 在 **单据上下文** 字段中，选择 **会计单据上下文 - 客户发票上下文模型**。
8. 在 **导入源** 字段组中，选择 **添加**。
9. 在 **名称** 字段中，输入 **XmlFile**（在 RCS 中电子发票功能的数据渠道配置中给出的 **附件筛选器**）。
10. 在 **说明** 字段中，输入说明，在 **数据实体名称** 字段中，选择 **已接收的 NF-e XML 文档**。
11. 在 **模型映射** 字段中，选择 **NF-e 邮件导入 - NF-e 电子邮件导入 (BR)**，然后选择 **保存**。
12. 在 **电子单据** 选项卡上的 **电子报告** 字段组中，选择 **添加**，在 **表名称** 字段中，选择 **已接收的 NF-e XML 文档**。
13. 在 **单据上下文** 字段中，选择 **查询会计单据上下文 - 客户发票上下文模型**。
14. 在 **电子单据模型映射** 字段中，选择 **查询映射 - 会计单据映射**。
15. 选择 **响应类型**，然后选择 **新建**。
16. 在 **响应类型** 字段中，输入 **响应**。 在 **提交状态** 字段中，输入 **已计划**。
17. 在 **模型映射** 字段中，选择 **来自响应消息的模型映射 - 响应消息导入格式**。
18. 选择 **保存**，然后关闭此页面。

### <a name="import-peppol-electronic-vendor-invoices"></a>导入 PEPPOL 电子供应商发票

1. 转到 **电子申报** 工作区中，并选择 **报告配置**。
2. 选择 **客户发票上下文模型** 并创建派生配置。
3. 在 **草稿** 版本上，选择 **设计器**。
4. 在 **数据模型** 树中，选择 **客户发票**，然后选择 **映射模型到数据源**。
5. 在 **定义** 树中，选择 **CustomerInvoice**，然后选择 **设计器**。
6. 在 **数据源** 树中，选择 **上下文\_渠道**。 在 **值** 字段中，选择 **PEPPOL**。 这是在 RCS 中电子发票功能的数据渠道配置中给出的渠道名称。 
7. 选择 **保存**，然后关闭页面。
8. 关闭该页面。
9. 选择 **客户发票上下文模型**，并在 **版本** 快速选项卡上选择 **更改状态** > **已完成**。
10. 转到 **组织管理** > **设置** > **电子单据参数**，并在 **功能** 选项卡上，确保选择了 **PEPPOL 全局电子发票**。 
11. 在 **外部渠道** 选项卡上的 **渠道** 字段组中，选择 **添加**。
12. 在 **渠道** 字段中，输入 **PEPPOL**。 在 **描述** 字段中，输入描述。
13. 在 **公司** 字段中，选择相应法人。 在 **单据上下文** 字段中，选择 **客户发票上下文 - 客户发票上下文模型**。
14. 选择 **保存**，然后关闭此页面。


## <a name="receive-electronic-invoices"></a>接收电子发票
若要接收电子发票，请按照以下步骤操作：

1. 转到 **组织管理** > **定期** > **电子单据** > **接收电子单据** 。
2. 选择 **确定**，然后关闭此页面。

## <a name="view-receive-logs-for-electronic-invoices"></a>查看电子发票的接收日志

若要查看电子发票的接收日志，请转到 **组织管理** > **定期** > **电子单据** > **电子单据收据日志**。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
