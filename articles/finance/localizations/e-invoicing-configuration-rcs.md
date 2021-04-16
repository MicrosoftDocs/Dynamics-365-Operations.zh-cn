---
title: 在 Regulatory Configuration Services (RCS) 中配置电子开票
description: 本主题说明如何在 Dynamics 365 Regulatory Configuration Services (RCS) 中配置电子开票。
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
ms.openlocfilehash: 9958091db4a3d7ce0b625e5adc8e2a6b37878618
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840236"
---
# <a name="configure-electronic-invoicing-in-regulatory-configuration-services-rcs"></a>在 Regulatory Configuration Services (RCS) 中配置电子开票

[!include [banner](../includes/banner.md)]

本主题提供有关 Dynamics 365 Regulatory Configuration Services (RCS) 中电子开票的配置功能的信息。

通过配置功能，电子开票可帮助您满足电子发票的业务和法规要求，而无需进行任何编码。 而且，在电子发票必须由 Web 服务以电子方式审核的情况下，配置功能还可以帮助您满足与 Web 服务交换消息的要求，无需编写任何代码。

## <a name="electronic-reporting"></a>电子报告

电子报告 (ER) 支持电子开票。

数据模型映射和格式是可配置的组件，可通过 ER 创建和维护，在电子开票中使用。 ER 格式设计器是用于创建和维护文件格式的工具。 用于配置电子开票功能。

有关详细信息，请参阅[电子报告 (ER) 概述](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md)。

## <a name="electronic-invoicing-features"></a>电子开票功能

电子开票功能负责通过电子开票生成电子发票。 它们封装配置规则，使用它们来处理 Microsoft Dynamics 365 Finance 和 Dynamics 365 Supply Chain Management 发送到电子开票和电子发票的数据。

这些功能还支持需要符合文件格式规范且输出是独立电子文件的场景。 在大多数情况下，文件格式规范由税务主管机构发布。

最后，这些功能还支持与税务主管机构或某些认可方托管的外部 Web 服务交换消息，并支持请求授权或在电子发票中增加审核戳记。

### <a name="availability-of-electronic-invoicing-features"></a>电子开票功能的可用性

电子开票功能的可用性取决于国家或地区。 虽然有些功能已正式发布，但其他功能仍处于预览阶段。

#### <a name="preview-features"></a>预览功能

下表显示了当前处于预览阶段的电子开票功能。

| 国家/地区 | 功能名称                         | 业务文档 |
|----------------|--------------------------------------|-------------------|
| 奥地利        | 奥地利电子发票 (AT)    | 销售发票和项目发票 |
| 比利时        | 比利时电子发票 (BE)      | 销售发票和项目发票 |
| 巴西         | 巴西 NF-e (BR)                  | 会计单据模型 55，更正单、取消和弃用 |
| 巴西         | 巴西 NFS-e ABRASF 库里蒂巴 (BR) | 服务会计单据 |
| 丹麦        | 丹麦电子发票 (DK)       | 销售发票和项目发票 |
| 埃及          | 埃及电子发票 (EG) | 销售发票和项目发票 |
| 爱沙尼亚        | 爱沙尼亚电子发票 (EE)     | 销售发票和项目发票 |
| 芬兰        | 芬兰电子发票 (FI)      | 销售发票和项目发票 |
| 法国         | 法国电子发票 (FR)       | 销售发票和项目发票 |
| 德国        | 德国电子发票 (DE)       | 销售发票和项目发票 |
| 意大利          | FatturaPA (IT)                       | 销售发票和项目发票 |
| 墨西哥         | 墨西哥 CFDI (MX)                    | 销售发票、装箱单、库存转移、付款补充和取消 |
| 荷兰    | 荷兰电子发票 (NL)        | 销售发票和项目发票 |
| 挪威         | 挪威电子发票 (NO)    | 销售发票和项目发票 |
| 西班牙          | 西班牙电子发票 (ES)      | 销售发票和项目发票 |
| 欧洲         | PEPPOL 电子发票            | PEPPOL 销售发票和项目发票 |

### <a name="configurable-components-of-electronic-invoicing-features"></a>电子开票功能的可配置组件

电子开票功能由以下几组可配置组件组成：

- **格式** – 格式让您可以配置当电子单据成为电子发票时电子开票必须生成的内容。 格式包括电子发票的格式配置，以及当需要与外部 Web 服务通信时用于提交请求和接收响应的文件和消息的格式配置。
- **操作** – 操作让您可以配置电子开票如何将 Finance 和 Supply Chain Management 提交的电子单据转换为电子发票。
- **适用性规则** – 适用性规则让您可以配置电子开票在处理电子开票功能时必须考虑的上下文。
- **变量** – 变量让您可以配置对构造配置逻辑的支持。 变量可以用作执行特定操作的值的输入。 或者，还可以用作 Finance 和 Supply Chain Management 与电子开票之间的值的交换。
- **电子单据模型映射** – 电子单据模型映射可让您配置 ER 模型映射。 此模型映射定义提交电子单据时集成到电子开票中的摘要发票的数据映射。
- **发票上下文模型** – 发票上下文模型让您可以配置 ER 发票上下文模型并定义电子开票功能的上下文。
- **响应类型** – 响应类型让您可以配置由于进行电子发票处理，电子开票必须在 Finance 和 Supply Chain Management 中更新的内容。

### <a name="formats"></a>格式

以下列表显示了可用于电子开票功能的 ER 格式配置。

#### <a name="austrian-at-electronic-invoices-sales-and-project-invoices-for-austria"></a>奥地利 (AT) 电子发票：奥地利的销售和项目发票

- OIOUBL 销售发票
- OIOUBL 项目发票
- OIOUBL 销售贷方通知单
- OIOUBL 项目贷方通知单

#### <a name="belgian-be-electronic-invoice-sales-and-project-invoices-for-belgium"></a>比利时 (BE) 电子发票：比利时的销售和项目发票

- UBL 销售发票 BE
- UBL 项目发票 BE
- UBL 项目贷方通知单 BE
- UBL 销售贷方通知单 BE

#### <a name="brazilian-br-nf-e-nf-e-federal-brazil"></a>巴西 (BR) NF-e：NF-e 联邦（巴西）

- NF-e 提交导出格式 (BR)
- NF-e 更正单导出格式 (BR)
- NF-e 取消导出格式 (BR)
- NF-e 弃用导出格式 (BR)

#### <a name="brazilian-nfs-e-br-nfs-e-abrasf-curitiba-city"></a>巴西 NFS-e (BR)：NFS-e ABRASF 库里蒂巴市

- NFS-e ABRASF 库里蒂巴 (BR)
- NFS-e ABRASF 查询库里蒂巴 (BR)

#### <a name="danish-dk-electronic-invoice-sales-and-project-invoices-for-denmark"></a>丹麦 (DK) 电子发票：丹麦的销售和项目发票

- OIOUBL 销售发票
- OIOUBL 项目发票
- OIOUBL 销售贷方通知单
- OIOUBL 项目贷方通知单

#### <a name="dutch-nl-electronic-invoice-sales-and-project-invoices-for-netherlands"></a>荷兰 (NL) 电子发票：荷兰的销售和项目发票

- UBL 销售发票 NL
- UBL 项目发票 NL
- UBL 项目贷方通知单 NL
- UBL 销售贷方通知单 NL

#### <a name="egyptian-eg-electronic-invoice-sales-and-project-invoices-for-egypt"></a>埃及 (EG) 电子发票：埃及的销售和项目发票

- 销售发票 (EG)（开票）
- 项目发票 (EG)（开票）

#### <a name="estonian-ee-electronic-invoice-sales-and-project-invoices-for-estonia"></a>爱沙尼亚 (EE) 电子发票：爱沙尼亚的销售和项目发票

- 销售发票 (EE)
- 项目发票 (EE)

#### <a name="finnish-fi-electronic-invoice-sales-and-project-invoices-for-finland"></a>芬兰 (FI) 电子发票：芬兰的销售和项目发票

- 销售发票 (FI)
- 项目发票 (FI)

#### <a name="french-fr-electronic-invoice-sales-and-project-invoices-for-france"></a>法国 (FR) 电子发票：法国的销售和项目发票

- UBL 销售发票 FR
- UBL 项目发票 FR
- UBL 项目贷方通知单 FR
- UBL 销售贷方通知单 FR

#### <a name="german-de-electronic-invoice-sales-and-project-invoices-for-germany"></a>德国 (DE) 电子发票：德国的销售和项目发票

- 销售发票 (DE)
- 项目发票 (DE)

#### <a name="italian-it-electronic-invoice-sales-and-project-invoices-for-italy"></a>意大利 (IT) 电子发票：意大利的销售和项目发票

- 销售发票 (IT)
- 项目发票 (IT)

#### <a name="mexican-mx-cfdi-cfdi-for-mexico"></a>墨西哥 (MX) CFDI：墨西哥的 CFDI

- CFDI 发票格式 (MX)
- CFDI 装箱单 (MX)
- CFDI 库存转移 (MX)
- CFDI 付款格式 (MX)
- CFDI 发票取消格式 (MX)

#### <a name="norwegian-no-electronic-invoice-sales-and-project-invoices-for-norway"></a>挪威 (NO) 电子发票：挪威的销售和项目发票

- OIOUBL 销售发票
- OIOUBL 项目发票
- OIOUBL 销售贷方通知单
- OIOUBL 项目贷方通知单

#### <a name="peppol-electronic-invoice-peppol-sales-and-project-invoices"></a>PEPPOL 电子发票：PEPPOL 销售和项目发票

- PEPPOL 销售发票
- PEPPOL 项目发票
- PEPPOL 销售贷方通知单
- PEPPOL 项目贷方通知单

#### <a name="spanish-es-electronic-invoice-sales-and-project-invoices-for-spain"></a>西班牙 (ES) 电子发票：西班牙的销售和项目发票

- 销售发票 (ES)
- 项目发票 (ES)

### <a name="actions"></a>操作​​

下表列出了可用操作，以及这些操作当前是正式发布还是仍处于预览阶段。

| 行为                                        | 说明                                                                  | 可用性         |
|-----------------------------------------------|------------------------------------------------------------------------------|----------------------|
| 转换文档                            | 运行电子报告格式来转换文档。                   | 正式发布  |
| 对 xml 文档签名                             | 使用数字签名对 xml 文档进行签名。                                   | 预览模式           |
| 对埃及税务主管机构的 json 文档签名 | 使用数字签名对埃及税务主管机构的 json 文档签名。       | 正式发布  |
| 与埃及 ETA 服务集成           | 与埃及税务主管机构通信。                                     | 正式发布  |
| 调用巴西 SEFAZ 服务                  | 与巴西 SEFAZ 服务集成以提交会计单据。       | 预览模式           |
| 调用墨西哥 PAC 服务                      | 与墨西哥 PAC 服务集成以提交 CFDI。                      | 预览模式           |
| 处理响应                              | 分析从 Web 服务调用收到的响应。                     | 正式发布  |
| 使用 MS Power Automate                         | 与 Microsoft Power Automate 内置流集成。                       | 预览模式           |

## <a name="configuration-providers"></a>配置提供方

配置提供者提供电子开票功能及其 ER 组件，如模型映射、格式配置和上下文模型。 他们在关联的全局存储库中发布电子开票功能和 ER 组件。 从那里，其他组织可以下载这些功能。

在通过 RCS 配置电子开票功能之前，您必须在 **电子报告** 模块中将自己的组织配置为配置提供者。 有关如何将配置提供者设置为 **活动** 的信息，请参阅[创建配置提供者并将其标记为活动](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md)。

## <a name="viewing-electronic-invoicing-features-in-the-global-repository"></a>查看全局存储库中的电子开票功能

要浏览特定配置提供者的全局存储库中可用的电子开票功能，请同步组织的 RCS 实例。 完成同步后，可用电子开票功能的列表将更新。

## <a name="importing-electronic-invoicing-features"></a>导入电子开票功能

在使用或配置电子开票功能之前，必须将它们导入组织的 RCS 实例。 导入操作将创建功能的本地副本，并将功能使用的所有 ER 项目（例如，格式配置和模型配置）复制到组织的 RCS 实例。

您可以从任何配置提供者导入电子开票功能。

## <a name="creating-electronic-invoicing-features"></a>创建电子开票功能

您可以从头创建电子开票功能，也可以从另一个电子开票功能派生。

从头创建电子开票功能时，必须手动添加 ER 组件（例如，功能版本配置和其他配置，如功能版本设置和应用程序设置）。 通过从另一个功能派生来创建功能时，新功能将继承原始功能的所有配置。 

## <a name="electronic-invoicing-feature-version"></a>电子开票功能版本

电子开票功能已版本化。 新版本创建时，版本号会自动递增。 可以为新版本定义“生效开始”日期。

电子开票功能版本采用的生命周期最多包含以下三种状态：

- **草稿** – 如果功能版本处于此状态，您可以编辑其配置属性及其任何项目（例如，文件格式配置）。
- **完成** – 如果功能版本处于此状态，说明该功能版本已发布到与您的组织关联的全局存储库中。 您不能再编辑功能版本或任何 ER 组件。
- **已发布** – 如果功能版本处于此状态，说明该功能版本已发布到电子开票。 您不能再编辑功能版本或任何 ER 组件。

### <a name="feature-configurations"></a>功能配置

功能配置保留电子开票功能使用的所有 ER 格式配置。 电子开票功能在处理期间使用的所有电子文件都来自已添加到该功能的功能配置中的格式配置。

从功能配置，您可以访问 ER 格式设计器，这是用于创建格式配置的 ER 工具。

### <a name="feature-setup"></a>功能设置

功能设置与功能配置结合使用。 每个功能设置都封装了一组提供预期行为的操作、适用性规则和变量，让电子开票功能可以满足电子发票的特定要求。

### <a name="application-setup"></a>应用程序设置

应用程序设置必须与先前创建的已连接应用程序关联。

通过应用程序设置，您可以配置必须在 Finance 和 Supply Chain Management 中进行的电子开票功能的那一部分。 不论是什么电子开票功能，都至少必须有三个可配置组件：

- **表名称** – Finance 和 Supply Chain Management 中的实体，保留过帐的发票，电子开票功能基于此实体。
- **上下文** – 通过 ER 配置的发票上下文模型的名称。
- **业务文档映射** – 通过 ER 配置的发票映射模型的名称。

> [!IMPORTANT]
> 可以在 Finance 和 Supply Chain Management 中查看在应用程序设置中输入的配置。 转到 **组织管理 \> 设置 \> 电子单据参数**。 在 **电子单据** 选项卡上，选择 **部署**，然后选择 **相连应用程序** 选项。

### <a name="deploying-feature-versions"></a>部署功能版本

在 RCS 中，您使用 **部署** 命令定向发布电子开票功能版本。 选择 **部署**，然后选择以下选项之一定义部署目标： 

- **服务环境** – 当部署的目标是服务环境时，电子开票功能版本将发布到服务环境。 然后，电子开票就可以接收和处理 Finance 和 Supply Chain Management 发送的电子单据。
- **相连应用程序** – 当部署的目标是相连应用程序时，由应用程序安装程序提供的配置将写入先前与之关联的 Finance 和 Supply Chain Management 实例中。

仅状态为 **已完成** 的电子开票功能版本可以部署到服务环境或连接的应用程序。

### <a name="removing-feature-versions"></a>删除功能版本

在 RCS 中，您使用 **取消部署** 命令从电子开票中的服务环境中删除特定的电子开票功能版本。

> [!IMPORTANT]
> **取消部署** 命令仅在服务环境中有效。 它不会从连接的应用程序中删除电子开票功能版本。

### <a name="rebasing-electronic-invoicing-features"></a>重定电子开票功能

当一个电子开票功能是从另一个电子开票功能派生而来时，**重定** 命令使用原始功能中引入的更改来更新派生功能。

## <a name="additional-resources"></a>其他资源

- [在 Finance 和 Supply Chain Management 中开具电子发票](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
