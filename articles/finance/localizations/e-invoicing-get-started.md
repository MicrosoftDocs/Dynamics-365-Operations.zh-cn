---
title: 开始使用电子开票
description: 本主题提供的信息将帮助您开始使用 Microsoft Dynamics 365 Finance 和 Dynamics 365 Supply Chain Management 中的电子开票。
author: gionoder
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: cf553f2ffecf18859b88932e68360231ca46410f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840116"
---
# <a name="get-started-with-electronic-invoicing"></a>开始使用电子开票

[!include [banner](../includes/banner.md)]

本主题提供的信息将帮助您开始使用电子开票。 本主题将指导您完成 Regulatory Configuration Services (RCS) 和 Dynamics 365 Finance 中的常见配置步骤，并提供在提交业务单据和查看处理结果时必须遵循的步骤。

## <a name="prerequisites"></a>先决条件

在完成本主题中的过程之前，必须具备以下先决条件：

- 配置您的 Microsoft Dynamics Lifecycle Services (LCS)、Regulatory Configuration Service (RCS) 和 Microsoft Dynamics 365 Finance 或 Dynamics 365 Supply Chain Management 环境。 有关详细信息，请参阅[开始使用电子开票服务管理](e-invoicing-get-started-service-administration.md)。
- 为您的组织创建配置提供者。 有关详细信息，请参阅[创建配置提供者并将其标记为活动](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md)。

## <a name="import-an-electronic-invoicing-feature-from-the-microsoft-configuration-provider"></a>从 Microsoft 配置提供者导入电子开票功能 

1. 登录到您的 Regulatory Configuration Service (RCS) 帐户。
2. 在 **全球化功能** 工作区的 **功能** 部分中，选择 **电子开票** 磁贴。
3. 选择 **导入**，然后选择 **同步**。
4. 使用一词 **Microsoft** 筛选 **配置提供者** 列。
5. 从本主题开头的表中选择电子开票功能的名称，然后选择 **导入**。

## <a name="create-an-electronic-invoicing-feature-under-your-organization-provider"></a>在您的组织提供者下创建电子开票功能

1. 在 RCS 中的 **全球化功能** 工作区的 **功能** 部分中，选择 **电子开票** 磁贴。
2. 选择 **添加** > **基于现有功能**，然后在 **名称** 字段中，输入电子开票功能的名称。
3. 在 **描述** 字段中，输入功能的描述。
4. 在 **基本功能字段** 中，从 Microsoft 配置提供者中选择导入的电子开票功能。
5. 选择 **创建功能**。

## <a name="country-specific-configuration-for-electronic-invoicing-feature"></a>电子开票功能的国家/地区特定配置

根据国家或地区，电子开票功能可能需要特定配置。 

有关具体步骤，请参阅为您所在国家或地区提供的“入门”文档。

## <a name="import-the-model-mapping-configurations-from-electronic-reporting"></a>从电子报告中导入模型映射配置

1. 在 RCS 中，选择 **电子报告** 工作区。
2. 从 **Microsoft** 配置提供者中，选择 **存储库**。
3. 选择 **全球**，然后在操作窗格上，选择 **打开**。
4. 根据下表按功能名称导入模型映射配置。

| 功能名称                         | 模型映射配置 |
|--------------------------------------|-----------------------------|
| 奥地利电子发票 (AT)    | <p>客户发票上下文模型</p><p>发票模型</p> |
| 比利时电子发票 (BE)      | <p>客户发票上下文模型</p><p>发票模型</p> |
| 巴西 NF-e (BR)                  | <p>客户发票上下文模型</p><p>会计单据</p><p>响应消息模型</p> |
| 巴西 NFS-e ABRASF 库里蒂巴 (BR) | <p>客户发票上下文模型</p><p>会计单据</p><p>响应消息模型</p> |
| 丹麦电子发票 (DK)       | <p>客户发票上下文模型</p><p>发票模型</p> |
| 埃及电子发票 (EG)     | <p>客户发票上下文模型</p><p>发票模型</p><p>响应消息模型</p> |
| 爱沙尼亚电子发票 (EE)     | <p>客户发票上下文模型</p><p>发票模型</p> |
| 芬兰电子发票 (FI)       | <p>客户发票上下文模型</p><p>发票模型</p> |
| 法国电子发票 (FR)       | <p>客户发票上下文模型</p><p>发票模型</p> |
| 德国电子发票 (DE)       | <p>客户发票上下文模型</p><p>发票模型</p> |
| FatturaPA (IT)                       | <p>客户发票上下文模型</p><p>发票模型</p> |
| 墨西哥 CFDI Interfactura (MX)       | <p>客户发票上下文模型</p><p>发票模型</p><p>响应消息模型</p> |
| 荷兰电子发票 (NL)        | <p>客户发票上下文模型</p><p>发票模型</p> |
| 挪威电子发票 (NO)    | <p>客户发票上下文模型</p><p>发票模型</p> |
| 西班牙电子发票 (ES)      | <p>客户发票上下文模型</p><p>发票模型</p> |
| PEPPOL 电子发票            | <p>客户发票上下文模型</p><p>发票模型</p> |


## <a name="configure-the-application-setup"></a>配置应用程序设置

1. 选择您创建的电子开票功能。
2. 在 **设置** 选项卡中，选择 **应用程序设置**。
3. 在 **连接应用程序** 字段中，选择与您的 Finance 或 Supply Chain Management 实例关联的连接。
4. 在 **电子单据类型** 部分，选择 **添加**。
5. 根据下表选择并输入 **表名称** 值。

    | 功能名称                         | 业务文档 | 表名 |
    |--------------------------------------|-------------------|------------|
    | 奥地利电子发票 (AT)    | <p>销售账单</p><p>项目账单</p> | <p>客户账单日记帐</p><p>项目账单</p> |
    | 比利时电子发票 (BE)      | <p>销售账单</p><p>项目账单</p> | <p>客户账单日记帐</p><p>项目账单</p> |
    | 巴西 NF-e (BR)                  | <p>会计单据</p><p>更正单</p> | 会计单据 |
    | 巴西 NFS-e ABRASF 库里蒂巴 (BR) | 服务会计单据 | 会计单据 |
    | 丹麦电子发票 (DK)       | <p>销售账单</p><p>项目账单</p> | <p>客户账单日记帐</p><p>项目账单</p> |
    | 埃及电子发票 (EG)     | <p>销售账单</p><p>项目账单</p> | <p>客户账单日记帐</p><p>项目账单</p> |
    | 爱沙尼亚电子发票 (EE)     | <p>销售账单</p><p>项目账单</p> | <p>客户账单日记帐</p><p>项目账单</p> |
    | 芬兰电子发票 (FI)       | <p>销售账单</p><p>项目账单</p> | <p>客户账单日记帐</p><p>项目账单</p> |
    | 法国电子发票 (FR)       | <p>销售账单</p><p>项目账单</p> | <p>客户账单日记帐</p><p>项目账单</p> |
    | 德国电子发票 (DE)       | <p>销售账单</p><p>项目账单</p> | <p>客户账单日记帐</p><p>项目账单</p> |
    | FatturaPA (IT)                       | <p>销售账单</p><p>项目账单 | <p>客户账单日记帐</p><p>项目账单</p> |
    | 墨西哥 CFDI Interfactura (MX)       | <p>销售账单</p><p>装箱单</p><p>库存转移</p><p>付款补充</p> | 客户账单日记帐 |
    | 荷兰电子发票 (NL)        | <p>销售账单</p><p>项目账单</p> | <p>客户账单日记帐</p><p>项目账单</p> |
    | 挪威电子发票 (NO)    | <p>销售账单</p><p>项目账单</p> | <p>客户账单日记帐</p><p>项目账单</p> |
    | 西班牙电子发票 (ES)      | <p>销售账单</p><p>项目账单</p> | <p>客户账单日记帐</p><p>项目账单</p> |
    | PEPPOL 电子发票            | <p>销售账单</p><p>项目账单</p> | <p>客户账单日记帐</p><p>项目账单</p> |

7. 对于您创建的每个表名称，根据下表选择并输入上下文值。

    | 功能名称                         | 业务文档 | 上下文 |
    |--------------------------------------|-------------------|---------|
    | 奥地利电子发票 (AT)    | <p>销售账单</p><p>项目账单</p> | <p>客户发票上下文模型 – 客户发票上下文</p><p>客户发票上下文模型 – 项目发票上下文</p> |
    | 比利时电子发票 (BE)      | <p>销售账单</p><p>项目账单</p> | <p>客户发票上下文模型 – 客户发票上下文</p><p>客户发票上下文模型 – 项目发票上下文</p> |
    | 巴西 NF-e (BR)                  | <p>会计单据</p><p>更正单</p> | <p>客户发票上下文模型 – 会计单据上下文</p><p>客户发票上下文模型 – FD 更正单上下文</p> |
    | 巴西 NFS-e ABRASF 库里蒂巴 (BR) | 服务会计单据| 客户发票上下文模型 – 会计单据上下文 |
    | 丹麦电子发票 (DK)       | <p>销售账单</p><p>项目账单</p> | <p>客户发票上下文模型 – 客户发票上下文</p><p>客户发票上下文模型 – 项目发票上下文</p> |
    | 埃及电子发票 (EG)     | <p>销售账单</p><p>项目账单</p> | <p>客户发票上下文模型 – 客户发票上下文</p><p>客户发票上下文模型 – 项目发票上下文</p> |
    | 爱沙尼亚电子发票 (EE)     | <p>销售账单</p><p>项目账单</p> | <p>客户发票上下文模型 – 客户发票上下文</p><p>客户发票上下文模型 – 项目发票上下文</p> |
    | 芬兰电子发票 (FI)       | <p>销售账单</p><p>项目账单</p> | <p>客户发票上下文模型 – 客户发票上下文</p><p>客户发票上下文模型 – 项目发票上下文</p> |
    | 法国电子发票 (FR)       | <p>销售账单</p><p>项目账单</p> | <p>客户发票上下文模型 – 客户发票上下文</p><p>客户发票上下文模型 – 项目发票上下文</p> |
    | 德国电子发票 (DE)       | <p>销售账单</p><p>项目账单</p> | <p>客户发票上下文模型 – 客户发票上下文</p><p>客户发票上下文模型 – 项目发票上下文</p> |
    | FatturaPA (IT)                       | <p>销售账单</p><p>项目账单</p> | <p>客户发票上下文模型 – 客户发票上下文</p><p>客户发票上下文模型 – 项目发票上下文</p> |
    | 墨西哥 CFDI Interfactura (MX)       | <p>销售账单</p><p>装箱单</p><p>库存转移</p><p>付款补充</p> | 客户发票上下文模型 – 客户发票上下文 |
    | 荷兰电子发票 (NL)        | <p>销售账单</p><p>项目账单</p> | <p>客户发票上下文模型 – 客户发票上下文</p><p>客户发票上下文模型 – 项目发票上下文</p> |
    | 挪威电子发票 (NO)    | <p>销售账单</p><p>项目账单</p> | <p>客户发票上下文模型 – 客户发票上下文</p><p>客户发票上下文模型 – 项目发票上下文</p> |
    | 西班牙电子发票 (ES)      | <p>销售账单</p><p>项目账单</p> | <p>客户发票上下文模型 – 客户发票上下文</p><p>客户发票上下文模型 – 项目发票上下文</p> |
    | PEPPOL 电子发票            | <p>销售账单</p><p>项目账单</p> | <p>客户发票上下文模型 – 客户发票上下文</p><p>客户发票上下文模型 – 项目发票上下文</p> |

8. 对于每个表名称和上下文，根据下表选择并输入业务单据映射值。

    | 功能名称                         | 业务文档 | 业务文档映射 |
    |--------------------------------------|-------------------|---------------------------|
    | 奥地利电子发票 (AT)    | <p>销售账单</p><p>项目账单</p> | <p>发票模型映射 – 客户发票</p><p>发票模型映射 – 项目发票</p> |
    | 比利时电子发票 (BE)      | <p>销售账单</p><p>项目账单</p> | <p>发票模型映射 – 客户发票</p><p>发票模型映射 – 项目发票</p> |
    | 巴西 NF-e (BR)                  | <p>会计单据</p><p>更正单</p> | <p>会计单据映射 – 会计单据映射</p><p>会计单据映射 – 更正单映射</p> |
    | 巴西 NFS-e ABRASF 库里蒂巴 (BR) | 服务会计单据 | 会计单据映射 – 会计单据映射 |
    | 丹麦电子发票 (DK)       | <p>销售账单</p><p>项目账单</p> | <p>发票模型映射 – 客户发票</p><p>发票模型映射 – 项目发票</p> |
    | 埃及电子发票 (EG)     | <p>销售账单</p><p>项目账单</p> | <p>发票模型映射 – 客户发票</p><p>发票模型映射 – 项目发票</p> |
    | 爱沙尼亚电子发票 (EE)     | <p>销售账单</p><p>项目账单</p> | <p>发票模型映射 – 客户发票</p><p>发票模型映射 – 项目发票</p> |
    | 芬兰电子发票 (FI)       | <p>销售账单</p><p>项目账单</p> | <p>发票模型映射 – 客户发票</p><p>发票模型映射 – 项目发票</p> |
    | 法国电子发票 (FR)       | <p>销售账单</p><p>项目账单</p> | <p>发票模型映射 – 客户发票</p><p>发票模型映射 – 项目发票</p> |
    | 德国电子发票 (DE)       | <p>销售账单</p><p>项目账单</p> | <p>发票模型映射 – 客户发票</p><p>发票模型映射 – 项目发票</p> |
    | FatturaPA (IT)                       | <p>销售账单</p><p>项目账单</p> | <p>发票模型映射 – 客户发票</p><p>发票模型映射 – 项目发票</p> |
    | 墨西哥 CFDI Interfactura (MX)       | <p>销售账单</p><p>装箱单</p><p>库存转移</p><p>付款补充</p> | 发票模型映射 – 客户发票 |
    | 荷兰电子发票 (NL)        | <p>销售账单</p><p>项目账单</p> | <p>发票模型映射 – 客户发票</p><p>发票模型映射 – 项目发票</p> |
    | 挪威电子发票 (NO)    | <p>销售账单</p><p>项目账单</p> | <p>发票模型映射 – 客户发票</p><p>发票模型映射 – 项目发票</p> |
    | 西班牙电子发票 (ES)      | <p>销售账单</p><p>项目账单</p> | <p>发票模型映射 – 客户发票</p><p>发票模型映射 – 项目发票</p> |
    | PEPPOL 电子发票            | <p>销售账单</p><p>项目账单</p> | <p>发票模型映射 – 客户发票</p><p>发票模型映射 – 项目发票</p> |


## <a name="country-specific-configuration-of-application-setup"></a>应用程序设置的国家/地区特定配置

根据国家或地区，应用程序设置可能需要特定配置。 

有关具体步骤，请参阅为您所在国家或地区提供的“入门”文档。

## <a name="deploy-the-electronic-invoicing-feature-to-service-environment"></a>将电子开票功能部署到服务环境

1. 在 **版本** 选项卡中，选择要部署的电子开票功能的版本。
2. 选择 **更改状态** \> **完成**。
3. 选择 **更改状态** \> **发布**。
4. 选择 **部署**。
5. 将 **部署到连接的应用程序** 选项设置为 **否**。
6. 将 **部署到服务环境** 选项设置为 **是**。
7. 在 **服务环境** 字段中，选择要在其中部署电子开票功能的电子开票服务环境。
8. 在 **开始日期** 字段中，选择电子开票功能必须在电子开票中生效的日期。
9. 选择 **确定**。

## <a name="deploy-the-electronic-invoicing-feature-to-connected-application"></a>将电子开票功能部署到连接的应用程序

1. 在 **版本** 选项卡上，选择要部署的电子开票功能的版本。
4. 选择 **部署**。
5. 将 **部署到连接的应用程序** 选项设置为 **是**。
6. 在 **连接应用程序** 字段上，选择与您的 Finance 或 Supply Chain Management 实例关联的连接。
7. 将 **部署到服务环境** 选项设置为 **否**。
10. 选择 **确定**。

## <a name="turn-on-the-electronic-invoicing-feature-in-finance-or-supply-chain-management"></a>在 Finance 或 Supply Chain Management 中打开电子开票功能

1. 登录到 Finance 或 Supply Chain Management，确认您位于正确的法人中。
2. 转到 **组织管理** \> **设置** \> **电子单据参数**。
3. 在 **功能** 选项卡上，选择特定于国家/地区的功能以打开 Finance 或 Supply Chain Management 的电子开票功能。 下表列出了可用于特定国家/地区的电子开票功能。 

    | 功能名称                                          | 国家/地区  |
    |-------------------------------------------------------|-----------------|
    | 奥地利电子发票 (AT)                     | 奥地利         |
    | 比利时电子发票 (BE)                       | 比利时         |
    | CFDI 墨西哥电子发票 (MX)                  | 墨西哥          |
    | 丹麦电子发票 (DK)                        | 丹麦         |
    | 荷兰电子发票 (NL)                         | 荷兰 |
    | 埃及电子发票 (EG)                      | 埃及           |
    | 爱沙尼亚电子发票 (EE)                      | 爱沙尼亚         |
    | 芬兰电子发票 (FI)                       | 芬兰         |
    | 法国电子发票 (FR)                        | 法国          |
    | 德国电子发票 (DE)                        | 德国         |
    | 意大利电子发票 (IT)                       | 意大利           |
    | NF-e 联邦 - 巴西电子发票 (BR)      | 巴西          |
    | NFS-e - 巴西服务(城市)电子账单   | 巴西          |
    | 挪威电子发票 (NO)                     | 挪威          |
    | PEPPOL 电子发票                             | 全局          |
    | 西班牙电子发票 (ES)                       | 西班牙           |

4. 选择 **保存**。

## <a name="issue-electronic-invoices"></a>开具电子发票

1. 转到 **组织管理** \> **定期** \> **电子单据** \> **提交电子单据**。
2. 在 **要包括的记录** 快速选项卡中，选择 **筛选**。
3. 选择 **添加** 将表名称添加到查询筛选器中。
4. 选择包含发票的表。

    > [!NOTE]
    > 表名称必须在本主题前面的[配置应用程序设置](#configure-the-application-setup)一节的表中列出。

5. 从要查询的表中选择字段名称。
6. 输入要用作查询条件的表名称和字段名称。
7. 重复步骤 5 和 6，向查询中添加更多字段和条件，然后选择 **确定**。
8. 选择 **确定**。

## <a name="view-submission-logs"></a>查看提交日志

1. 转到 **组织管理** \> **定期** \> **电子单据** \> **电子单据提交日志**。
2. 在 **文档类型** 字段中，选择包含发票的表。

    > [!NOTE]
    > 表名称必须在本主题前面的[配置应用程序设置](#configure-the-application-setup)一节的表中列出。

3. 在网格中选择一个发票，然后选择 **查询**\>**提交详细信息**。


## <a name="related-topics"></a>相关主题

- [电子开票概览](e-invoicing-service-overview.md)
- [开始使用电子开票服务管理](e-invoicing-get-started-service-administration.md)
- [开始使用适用于巴西的电子开票](e-invoicing-bra-get-started.md)
- [开始使用适用于墨西哥的电子开票](e-invoicing-mex-get-started.md)
- [开始使用适用于意大利的电子开票](e-invoicing-ita-get-started.md)
- [埃及的客户电子发票](emea-egy-e-invoices.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
