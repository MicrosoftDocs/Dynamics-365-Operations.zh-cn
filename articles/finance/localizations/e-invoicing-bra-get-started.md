---
title: 开始使用适用于巴西的电子开票
description: 本主题提供的信息将帮助您开始使用 Finance 和 Supply Chain Management 中适用于巴西的电子开票。
author: gionoder
ms.date: 03/29/2021
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
ms.openlocfilehash: ccf2a78a5ffdb95b334f751944fdd010bf8cbf01
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/13/2021
ms.locfileid: "7345189"
---
# <a name="get-started-with-electronic-invoicing-for-brazil"></a>开始使用适用于巴西的电子开票 

[!include [banner](../includes/banner.md)]

本主题提供的信息将帮助您开始使用适用于巴西的电子开票。 本主题将指导您完成 Regulatory Configuration Services (RCS) 中与国家/地区有关的配置步骤，并补充[开始使用电子开票](e-invoicing-get-started.md)主题中描述的步骤。

## <a name="country-specific-configuration-for-brazilian-nf-e-br-electronic-invoicing-feature"></a>巴西 NF-e (BR) 电子开票功能的国家/地区特定配置

**巴西 NF-e (BR) 电子开票功能** 的一些参数使用默认值发布。 在将电子开票功能部署到服务环境之前，查看并（如有必要）更新这些值以更好地反映您的业务操作。

此部分补充 [开始使用电子开票](e-invoicing-get-started.md)主题中的 **电子开票功能的国家/地区特定配置** 部分。

1. 在 RCS 中的 **全球化功能** 工作区的 **功能** 部分中，选择 **电子开票** 磁贴。
2. 在 **电子开票功能** 页面上，验证是否选择了您创建的 **巴西 NF-e (BR)** 电子开票功能。
3. 在 **版本** 选项卡上，验证是否已选择 **草稿** 版本。
4. 在 **设置** 选项卡上的网格中，选择 **提交**，然后选择 **编辑。**
5. 在 **操作** 选项卡上的 **操作** 字段组中，选择 **（预览）签署 xml 文档** 操作。
6. 在 **参数** 字段组中，选择 **证书名称**，并在 **值** 字段中，输入与您的密钥保管库参数关联的证书名称。
7. 在 **操作** 选项卡上的 **操作** 字段组中，选择 **（预览）调用巴西 SEFAZ 服务** 操作。
8. 在 **参数** 字段组中，选择 **URL 地址** 参数。
9. 在 **值** 字段中，如有必要，请查看并更新您所在州的 SEFAZ 文档所发布的 Web 服务的 URL，然后选择 **保存。**
10. 在 **适用性规则** 选项卡上的 **适用性规则设置** 字段组中，查看 **洲** 字段，并根据需要针对与 Web 服务 URL 所引用的相同洲对其进行更新。
11. 选择 **保存**，然后关闭页面。
12. 若要将电子开票功能部署到服务环境，请参阅[开始使用电子开票](e-invoicing-get-started.md)。

## <a name="country-specific-configuration-of-application-setup-for-brazilian-nf-e-br-electronic-invoicing-feature"></a>巴西 NF-e (BR) 电子开票功能的应用程序设置的国家/地区特定配置

在将应用程序设置部署到 Finance 或 Supply Chain Management 连接的应用程序之前，请完成这些步骤。

此部分补充 [开始使用电子开票](e-invoicing-get-started.md)主题中的 **应用程序设置的国家/地区特定配置** 部分。

1. 在 RCS 中的 **全球化功能** 工作区的 **功能** 部分中，选择 **电子开票** 磁贴。
2. 在 **电子开票功能** 页面上，验证是否选择了 **巴西 NF-e (BR)** 电子开票功能。
3. 在 **版本** 选项卡上，验证是否已选择 **草稿** 版本。
4. 在 **设置** 选项卡上，选择 **应用程序设置**，并在 **相连应用程序** 字段中，选择要部署到的应用程序。
5. 在 **表名称** 字段中，验证是否选择了 **会计单据标题**。
6. 选择 **响应类型**，然后选择 **新建**。
7. 在 **响应类型** 字段中，输入“响应”作为固定值，然后在 **描述** 字段中，输入“描述”。
8. 在 **提交状态** 字段中，选择 **待处理**。
9. 在 **模型映射** 字段中，选择具有 **（预览）响应消息导入格式** 的 **来自响应消息的模型映射**，然后选择 **保存**。
10. 选择 **新建**，在 **响应类型** 字段中，输入“响应数据”作为固定值，然后在 **描述** 字段中，输入“描述”。
11. 在 **提交状态** 字段中，选择 **待处理**。
12. 在 **模型映射** 字段中，选择具有 **（预览）NF-e 响应数据导入格式 (BR)** 的 **响应数据导入**，然后选择 **保存**。
13. 若要将应用程序设置部署到 Finance 或 Supply Chain 连接的应用程序，请参阅[开始使用电子开票](e-invoicing-get-started.md)。

## <a name="country-specific-configuration-for-brazilian-nfs-e-abrasf-curitiba-br-electronic-invoicing-feature"></a>巴西 NFS-e ABRASF 库里蒂巴 (BR) 电子开票功能的国家/地区特定配置

**巴西 NFS-e ABRASF 库里蒂巴 (BR) 电子开票功能** 的一些参数使用默认值发布。 在将电子开票功能部署到服务环境之前，查看并（如有必要）更新这些值以更好地满足您的业务操作需求。

此部分补充 [开始使用电子开票](e-invoicing-get-started.md)主题中的 **电子开票功能的国家/地区特定配置** 部分。

1. 在 RCS 中的 **全球化功能** 工作区的 **功能** 部分中，选择 **电子开票** 磁贴。
2. 在 **电子开票功能** 页面上，验证是否选择了您创建的 **巴西 NFS-e ABRASF 库里蒂巴 (BR)** 电子开票功能。
3. 在 **版本** 选项卡上，验证是否选择了 **草稿** 版本，然后在 **设置** 选项卡上的网格中，选择 **提交**。
4. 选择 **编辑**，在 **操作** 选项卡上的 **操作** 字段组中，选择第一个出现的 **（预览）签署 xml 文档**。
5. 在 **参数** 字段组中，选择 **证书名称**。
6. 在 **值** 字段中，输入与您的密钥保管库参数关联的证书名称。
7. 在 **操作** 字段组中，选择第二个出现的 **（预览）签署 xml 文档**。
8. 在 **参数** 字段组中，选择 **证书名称**。
9. 在 **值** 字段中，输入与您的密钥保管库参数关联的证书名称。
10. 在 **操作** 选项卡上的 **操作** 字段组中，选择 **（预览）调用巴西 SEFAZ 服务** 操作。
11. 在 **参数** 字段组中，选择 **URL 地址** 参数。
12. 在 **值** 字段中，如有必要，请查看并更新库里蒂巴市税务部门所发布的 Web 服务的 URL，然后选择 **保存。**
13. 在 **设置** 选项卡上的网格中，选择 **查询**，然后选择 **编辑。**
14. 在 **操作** 选项卡上的 **操作** 字段组中，选择 **（预览）调用巴西 SEFAZ 服务** 操作。
15. 在 **参数** 字段组中，选择 **URL 地址** 参数。
16. 在 **值** 字段中，如有必要，请查看并更新库里蒂巴市税务部门所发布的 Web 服务的 URL。
17. 选择 **保存**，然后关闭此页面。
18. 若要将电子开票功能部署到服务环境，请参阅[开始使用电子开票](e-invoicing-get-started.md)。

## <a name="country-specific-configuration-of-application-setup-for-brazilian-nfs-e-abrasf-curitiba-br-electronic-invoicing-feature"></a>巴西 NFS-e ABRASF 库里蒂巴 (BR) 电子开票功能的应用程序设置的国家/地区特定配置

在将应用程序设置部署到 Finance 或 Supply Chain Management 连接的应用程序之前，请完成这些步骤。

此部分补充 [开始使用电子开票](e-invoicing-get-started.md)主题中的 **应用程序设置的国家/地区特定配置** 部分。

1. 在 RCS 中的 **全球化功能** 工作区的 **功能** 部分中，选择 **电子开票** 磁贴。
2. 在 **电子开票功能** 页面上，验证是否选择了 **巴西 NFS-e ABRASF 库里蒂巴 (BR)** 电子开票功能。
3. 在 **版本** 选项卡上，验证是否选择了 **草稿** 版本，然后在 **设置** 选项卡上，选择 **应用程序设置**。
4. 在 **相连应用程序** 字段中，选择要部署的应用程序。
5. 在 **表名称** 字段上，验证是否选择了会计单据标题。
6. 选择 **响应类型**，然后选择 **新建**。
7. 在 **响应类型** 字段中，输入“ABRASFCuritibaSubmitResponse”作为固定值，然后在 **描述** 字段中，输入“描述”。
8. 在 **提交状态** 字段中，选择 **待处理**。
9. 在 **模型映射** 字段中，选择 **响应消息导入** 以及 **（预览）NFS-e ABRASF 库里蒂巴响应消息导入 (BR)**，然后选择 **保存**。
10. 选择 **新建**，在 **响应类型** 字段中，输入“ABRASFCuritibaSubmitResponseData”，然后在 **描述** 字段中，输入“描述”。
11. 在 **提交状态** 字段中，选择 **待处理**。
12. 在 **模型映射** 字段中，选择具有 **（预览）NFS-e ABRASF 响应数据导入格式 (BR)** 的 **响应数据导入**，然后选择 **保存**。
13. 选择 **新建**，在 **响应类型** 字段中，输入“ABRASFCuritibaInquireResponse”，然后在 **描述** 字段中，输入“描述”。
14. 在 **提交状态** 字段中，选择 **待处理**。
15. 在 **模型映射** 字段中，选择 **响应消息导入** 以及 **（预览）NFS-e ABRASF 库里蒂巴响应消息导入 (BR)**。
16. 选择 **保存**，然后关闭页面。
17. 若要将应用程序设置部署到 Finance 或 Supply Chain 连接的应用程序，请参阅[开始使用电子开票](e-invoicing-get-started.md)。

## <a name="privacy-notice"></a>隐私声明
启用 **NF-e 联邦 - 巴西电子发票 (BR)** 和 **NFS-e - 巴西服务（城市）电子发票** 功能可能需要发送有限的数据，包括组织税务注册 ID。 此数据会传输到税务机构授权的第三方机构，以便以与政府的 Web 服务集成所需的预定义格式向该税务机构发送电子发票。 作为管理员，您可以启用或关闭 **NF-e 联邦 - 巴西电子发票 (BR)** 和 **NFS-e - 巴西服务（城市）电子发票** 功能。 以下步骤表明了如何执行此操作： 

1. 转到 **组织管理** > **设置** > **电子单据参数**。 
2. 在 **功能** 选项卡上，选择包含 **NF-e 联邦 - 巴西电子发票 (BR)** 或 **NFS-e - 巴西服务（城市）电子发票** 功能的行，然后选择相应的功能。 从这些外部系统导入到此 Dynamics 365 在线服务的数据受我们的[隐私声明](https://go.microsoft.com/fwlink/?LinkId=512132)的约束。 有关详细信息，请查阅国家/地区特定功能文档中的“隐私声明”部分。

## <a name="additional-resources"></a>其他资源

- [电子开票概览](e-invoicing-service-overview.md)
- [开始使用电子开票服务管理](e-invoicing-get-started-service-administration.md)
- [开始使用电子开票](e-invoicing-get-started.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
