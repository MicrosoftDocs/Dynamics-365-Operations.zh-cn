---
title: 埃及电子开票
description: 本文提供的信息将帮助您开始使用 Microsoft Dynamics 365 Finance 和 Dynamics 365 Supply Chain Management 中的埃及电子开票。
author: gionoder
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
ms.openlocfilehash: c2a46ef938c5dee62c0d0acd1648584df344c81a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904403"
---
# <a name="electronic-invoicing-for-egypt"></a>埃及电子开票

[!include [banner](../includes/banner.md)]

本文提供的信息将帮助您开始使用适用于埃及的电子开票。 指导您完成 Regulatory Configuration Service (RCS) 中与国家/地区相关的配置步骤。 这些步骤补充了[设置电子开票](e-invoicing-set-up-overview.md)中描述的步骤。

## <a name="prerequisites"></a>先决条件

在开始本文中的过程之前，请完成以下先决条件：

- 熟悉[电子开票概述](e-invoicing-service-overview.md)中所述的电子开票。
- 注册 RCS，并设置电子开票。 有关详细信息，请参阅以下主题：

    - [注册并安装电子开票服务](e-invoicing-sign-up-install.md)
    - [设置电子开票的 Azure 资源](e-invoicing-set-up-azure-resources.md)
    - [在 Lifecycle Services 中安装微服务的加载项](e-invoicing-install-add-in-microservices-lcs.md)
    
- 激活 Microsoft Dynamics 365 Finance 或 Dynamics 365 Supply Chain Management 应用程序与电子开票服务之间的集成，如[激活和设置与电子开票的集成](e-invoicing-activate-setup-integration.md)中所述。
- 在 Azure Key Vault 中创建一个数字证书机密，并按照[客户证书和机密](e-invoicing-customer-certificates-secrets.md)中的说明进行设置。 出于测试目的，埃及税务机关提供了特定的测试数字证书，这些证书只能在测试和解决方案验证阶段才可以使用。 有关详细信息，请使用[埃及电子开票 SDK](https://sdk.invoicing.eta.gov.eg/faq/) 中提供的链接转到埃及税务局网站。

## <a name="country-specific-configuration-for-the-egyptian-electronic-invoice-eg-feature"></a>埃及电子发票 (EG) 功能的国家/地区特定配置

**埃及电子发票 (EG)** 电子开票功能的一些参数使用默认值发布。 在将电子开票功能部署到服务环境之前，请查看默认值并根据需要进行更新，以便它们更好地反映您的业务操作。

1. 导入最新版本的 **埃及电子发票 (EG)** 全球化功能，如[从全局存储库导入功能](e-invoicing-import-feature-global-repository.md)中所述。
2. 创建导入的全球化功能的副本，并为其选择配置提供程序，如[创建全球化功能](e-invoicing-create-new-globalization-feature.md)中所述。
3. 在 **版本** 选项卡上，验证是否已选择 **草稿** 版本。
4. 在 **设置** 选项卡上的网格中，选择 **派生的销售发票** 功能设置。
5. 选择 **编辑**。
6. 在 **处理管道** 选项卡的 **处理管道** 部分，选择 **对埃及税务主管机构的 json 文档签名**。
7. 在 **参数** 部分，选择 **证书名称**，然后选择您创建的数字证书的名称。
8. 在 **处理管道** 部分，选择 **与埃及 ETA 服务集成**。 对于两次发生的此操作，请重复此步骤。
9. 在 **参数** 部分，选择 **Web 服务 URL** 和 **登录服务 URL**。 然后查看 URL 参数。 要获取测试和生产 URL，请使用[埃及电子开票 SDK](https://sdk.invoicing.eta.gov.eg/faq/) 中提供的链接转到埃及税务局网站。
10. 选择 **保存**，然后关闭页面。
11. 对 **派生的项目发票** 功能设置重复步骤 4 到 10。

## <a name="country-specific-configuration-for-the-egyptian-electronic-invoice-eg-application-setup"></a>埃及电子发票 (EG) 应用程序设置的国家/地区特定配置

您的 Finance 或 Supply Chain Management 环境中必须设置一些参数。 您可以在以下两个位置之一完成此设置：

- 直接在您的 Finance 或 Supply Chain Management 环境中。 有关详细信息，请参阅[设置电子开票参数](e-invoicing-set-up-parameters.md)。
- 在 RCS 中。 在电子开票功能设置的范围内，您可以定义所有参数，然后在部署电子开票功能时将它们直接部署到您的 Finance 或 Supply Chain Management 环境中。

对于这两个选项，参数是相同的。 如果您是在电子开票服务中设置您的第一项功能，我们建议您按照以下步骤在 RCS 中设置参数，然后将它们部署到已连接的应用程序。

> [!NOTE]
> 某些电子开票功能版本可能包含一组预定义的 Finance 或 Supply Chain Management 的应用程序特定参数。 在这种情况下，您应该验证数据是否正确。 或者手动设置参数。

1. 找到您创建的 **埃及电子发票 (EG)** 全球化功能的副本。
2. 在 **版本** 选项卡上，验证是否已选择 **草稿** 版本。
3. 在 **设置** 选项卡中，选择 **应用程序设置**。
4. 在 **相连应用程序** 字段中，选择要部署参数的应用程序。
5. 在 **电子单据类型** 页面上，选择 **添加** 创建记录。
6. 在 **表名称** 字段中，添加 **CustInvoiceJour**。
7. 在 **上下文** 字段中，添加对 **客户发票上下文** 映射名称的引用。 配置是 **客户发票上下文模型**。
8. 在 **客户单据映射** 字段中，添加对 **客户发票** 映射名称的引用。 配置是 **发票模型映射**。
9. 选择 **保存**。
10. 在 **响应类型** 页上，选择 **添加**。
11. 在 **响应类型** 字段中，输入 **响应**。
12. 在 **说明** 字段中，输入 **处理响应**。
13. 在 **提交状态** 字段中，选择 **待处理**。
14. 在 **模型映射** 字段中，选择 **响应消息导入**。 配置是 **埃及响应消息导入 (EG)**。
15. 选择 **保存**。
16. 选择 **添加**。
17. 在 **响应类型** 字段中，输入 **ResponseData**。
18. 在 **说明** 字段中，输入 **处理响应数据**。
19. 在 **提交状态** 字段中，选择 **待处理**。
20. 在 **数据实体名称** 字段中，选择 **SalesInvoiceHeaderV2Entity**。
21. 在 **模型映射** 字段中，选择 **响应数据导入**。 配置是 **埃及响应数据导入格式 (EG)**。
22. 选择 **保存**，然后关闭页面。
23. 关闭该页面。

要将功能部署到服务环境并将应用程序设置部署到 Finance 或 Supply Chain Management 连接的应用程序，请参阅[完成、发布和部署全球化功能](e-invoicing-complete-publish-deploy-globalization-feature.md)

## <a name="privacy-notice"></a>隐私声明

启用 **埃及电子发票 (EG)** 功能可能需要发送有限的数据。 此数据包括组织的税务登记 ID。 数据将被传输到税务机构授权的第三方机构，以与政府 Web 服务集成所需的预定义格式向该税务机构发送电子发票。 管理员可以通过转到 **组织管理** \> **设置** \> **电子单据参数** 来启用和禁用此功能。 在 **功能** 选项卡上，选择包含 **埃及电子发票 (EG)** 功能的行，然后进行适当的选择。 从外部系统导入到此 Dynamics 365 在线服务的数据受我们的[隐私声明](https://go.microsoft.com/fwlink/?LinkId=512132)的约束。 有关详细信息，请查阅国家/地区特定功能文档中的“隐私声明”部分。

## <a name="additional-resources"></a>其他资源

- [电子开票概览](e-invoicing-service-overview.md)
- [开始使用电子开票服务管理](e-invoicing-get-started-service-administration.md)
- [开始使用电子开票](e-invoicing-get-started.md)
- [埃及的客户电子发票](emea-egy-e-invoices.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
