---
title: 开始使用适用于埃及的电子开票
description: 本主题提供的信息将帮助您开始使用 Finance 和 Supply Chain Management 中适用于埃及的电子开票。
author: gionoder
ms.date: 04/20/2021
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
ms.openlocfilehash: 133c47d52bb301f862888c367d19fd58701ecb3c
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/03/2021
ms.locfileid: "6340121"
---
# <a name="get-started-with-electronic-invoicing-for-egypt"></a>开始使用适用于埃及的电子开票

[!include [banner](../includes/banner.md)]

本主题提供的信息将帮助您开始使用适用于埃及的电子开票。 本主题将指导您完成 Regulatory Configuration Services (RCS) 中与国家/地区有关的配置步骤，并补充[开始使用电子开票](e-invoicing-get-started.md)中描述的步骤。

## <a name="country-specific-configuration-for-egyptian-electronic-invoice-eg-electronic-invoicing-feature"></a>埃及电子发票 (EG) 电子开票功能的国家/地区特定配置

**埃及电子发票 (EG) 电子开票功能** 的一些参数使用默认值发布。 在将电子开票功能部署到服务环境之前，查看并（如有必要）更新这些值以更好地反映您的业务操作。

此部分补充 [开始使用电子开票](e-invoicing-get-started.md)主题中的 **电子开票功能的国家/地区特定配置** 部分。

### <a name="prerequisites"></a>先决条件

在完成本节中的过程之前，您必须：

- 创建数字证书机密，如 [开始使用电子开票服务管理](e-invoicing-get-started-service-administration.md)内 **创建数字证书机密** 部分中所述。 出于测试目的，埃及税务机关提供了特定的测试数字证书，这些证书只能在测试和解决方案验证阶段才可以使用。 有关详细信息，请使用[埃及电子开票 SDK](https://sdk.sit.invoicing.eta.gov.eg/faq/) 中提供的链接访问埃及税务局网站。

1. 在 RCS 中的 **全球化功能** 工作区的 **功能** 部分中，选择 **电子开票** 磁贴。
2. 在 **电子开票功能** 页面上，验证是否选择了您创建的 **埃及电子发票 (EG)** 电子开票功能。
3. 在 **版本** 选项卡上，验证是否已选择 **草稿** 版本。
4. 在 **设置** 选项卡上的网格中，选择 **销售发票** 功能设置。
5. 选择 **编辑**，在 **操作** 选项卡上的 **操作** 字段组中，选择 **对埃及税务主管机构的 json 文档签名**。
6. 在 **参数** 字段组中，选择 **证书名称** 参数，并选择所创建的要与电子开票功能配合使用的数字证书名称。
7. 在 **操作** 字段组中，选择 **与埃及 ETA 服务集成**。 对于两次发生的此操作，请重复此步骤。
8. 在 **参数** 字段组中，选择 **Web 服务 URL** 和 **登录服务 URL**，并在必要时查看 URL 参数。 使用[埃及电子开票 SDK](https://sdk.sit.invoicing.eta.gov.eg/faq/) 中提供的链接，访问埃及税务局网站以获取测试和生产 URL。
9. 选择 **保存**，然后关闭页面。
10. 若要将电子开票功能部署到服务环境，请参阅[开始使用电子开票](e-invoicing-get-started.md)。

## <a name="country-specific-configuration-of-the-application-setup-for-the-egyptian-electronic-invoice-eg-electronic-invoicing-feature"></a>埃及电子发票 (EG) 电子开票功能的应用程序设置的国家/地区特定配置

在将应用程序设置部署到 Finance 或 Supply Chain Management 连接的应用程序之前，请完成这些步骤。

此部分补充 [开始使用电子开票](e-invoicing-get-started.md)主题中的 **应用程序设置的国家/地区特定配置** 部分。

1. 在 RCS 中的 **全球化功能** 工作区的 **功能** 部分中，选择 **电子开票** 磁贴。
2. 在 **电子开票功能** 页面中，验证是否选择了 **埃及电子发票 (EG)** 电子开票功能。
3. 在 **版本** 选项卡上，验证是否已选择 **草稿** 版本。
4. 在 **设置** 选项卡上，选择 **应用程序设置**，并在 **相连应用程序** 字段中，选择要部署到的应用程序。
5. 在 **表名称** 字段中，验证是否选择了客户发票日记帐。
6. 选择 **响应类型**，然后选择 **新建**。
7. 在 **响应类型** 字段中，输入“响应”，然后在 **描述** 字段中，输入“描述”。
8. 在 **提交状态** 字段中，选择 **待处理**。
9. 在 **模型映射** 字段中，选择具有 **（预览）响应消息导入格式** 的 **来自响应消息的模型映射**，然后选择 **保存**。
10. 选择 **新建**，然后在 **响应类型** 字段中输入“ResponseData”作为固定值。 在 **描述** 字段中，输入“描述”。
11. 在 **提交状态** 字段中，选择 **待处理**。
12. 在 **数据实体名称** 字段中，选择 **销售发票抬头 V2**。
13. 在 **模型映射** 字段中，选择具有 **（预览）埃及响应数据导入格式** 的 **埃及响应数据导入**，然后选择 **保存**。
14. 若要将应用程序设置部署到 Finance 或 Supply Chain Management 连接的应用程序，请参阅[开始使用电子开票](e-invoicing-get-started.md)。

## <a name="privacy-notice"></a>隐私声明

启用 **埃及电子发票 (EG)** 功能可能需要发送有限的数据，包括组织税务登记 ID。 此数据将被传输到税务机构授权的第三方机构，以便以与政府的 Web 服务集成所需的预定义格式向该税务机构发送电子发票。 管理员可以通过导航到 **组织管理** > **设置** > **电子单据参数** 来启用和禁用此功能。 在 **功能** 选项卡上，选择包含 **埃及电子发票 (EG)** 功能的行，然后进行适当的选择。 从这些外部系统导入到此 Dynamics 365 在线服务的数据受我们的[隐私声明](https://go.microsoft.com/fwlink/?LinkId=512132)的约束。 有关详细信息，请查阅国家/地区特定功能文档中的“隐私声明”部分。

## <a name="additional-resources"></a>其他资源

- [电子开票概览](e-invoicing-service-overview.md)
- [开始使用电子开票服务管理](e-invoicing-get-started-service-administration.md)
- [开始使用电子开票](e-invoicing-get-started.md)
- [埃及的客户电子发票](emea-egy-e-invoices.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
