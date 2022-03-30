---
title: 升级到当事方和全球通讯簿模型
description: 本主题介绍如何将双重写入数据升级到当事方和全球通讯簿模型。
author: RamaKrishnamoorthy
ms.date: 03/10/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-31
ms.openlocfilehash: 95d272d9076f1ab25230e4efa98e321bdd618062
ms.sourcegitcommit: 6dc2b877cf8ea9185a07964ec05c5ddb7a78471b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/12/2022
ms.locfileid: "8407786"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a>升级到当事方和全球通讯簿模型

[!include [banner](../../includes/banner.md)]



[Microsoft Azure 数据工厂模板](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema)帮助您将采用双重写入的以下现有数据升级到当事方和全球通讯薄模型：**客户**、**联系人** 和 **供应商** 表中的数据，以及邮政和电子地址。

提供了以下三个数据工厂模板。 它们有助于协调 Finance and Operations 应用和 Customer Engagement 应用中的数据。

- **[当事方模板](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/arm_template.json)（将数据升级到双重写入的当事方 GAB 架构/arm_template.json）**- 此模板有助于升级与 **客户**、**联系人** 和 **供应商** 数据关联的 **当事方** 和 **联系人** 数据。
- **[当事方邮政地址模板](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/Upgrade%20to%20Party%20Postal%20Address%20-%20GAB/arm_template.json)（将数据升级到双重写入的当事方 GAB 架构/升级到当事方邮政地址 - GAB/arm_template.json）**- 此模板有助于升级与 **客户**、**联系人** 和 **供应商** 数据关联的邮政地址。
- **[当事方电子地址模板](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/Upgrade%20to%20Party%20Electronic%20Address%20-%20GAB/arm_template.json)（将数据升级到双重写入的当事方 GAB 架构/升级到当事方电子地址 - GAB/arm_template.json）**- 此模板有助于升级与 **客户**、**联系人** 和 **供应商** 数据关联的电子地址。

在流程结束时，将生成以下逗号分隔值 (.csv) 文件。

| 文件名 | 目的 |
|---|---|
| FONewParty.csv | 此文件有助于在 Finance and Operations 应用内创建新 **当事方** 记录。 |
| ImportFONewPostalAddressLocation.csv | 此文件有助于在 Finance and Operations 应用中创建新的 **邮政地址位置** 记录。 |
| ImportFONewPartyPostalAddress.csv | 此文件有助于在 Finance and Operations 应用中创建新的 **当事方邮政地址** 记录。 |
| ImportFONewPostalAddress.csv | 此文件有助于在 Finance and Operations 应用中创建新的 **邮政地址** 记录。 |
| ImportFONewElectronicAddress.csv | 此文件有助于在 Finance and Operations 应用中创建新的 **电子地址** 记录。 |

本主题说明如何使用数据工厂模板和升级数据。 如果没有任何自定义项，可以按原样使用模板。 但是，如果您有 **客户**、**联系人** 和 **供应商** 数据的自定义项，则必须按照本主题中的描述修改模板。

> [!IMPORTANT]
> 有关于运行当事方邮政地址和当事方电子地址模板的特殊说明。 您必须先运行当事方模板，然后运行当事方邮政地址模板，再运行当事方电子地址模板。 每个模板都旨在在单独的数据工厂中导入。

## <a name="prerequisites"></a>先决条件

在升级到当事方和全球通讯簿模型之前，必须满足以下先决条件：

+ 您必须具有 [Azure 订阅](https://portal.azure.com/)。
+ 您必须有权访问[模板](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema)。
+ 您必须是现有的双写入客户。

## <a name="prepare-for-the-upgrade"></a>准备升级

升级需要满足以下先决条件：

+ **完全同步：** 对于 **帐户（客户）**、**联系人** 和 **供应商** 表，Finance and Operations 环境和 Customer Engagement 环境都处于完全同步状态。
+ **集成密钥**：Customer Engagement 应用中的 **帐户（客户）**、**联系人** 和 **供应商** 表使用现成的集成密钥。 如果已自定义集成密钥，必须自定义模板。
+ **当事方编号：** 将升级的所有 **帐户（客户）**、**联系人** 和 **供应商** 记录都具有当事方编号。 将忽略没有当事方编号的记录。 如果要升级这些记录，请在开始升级流程之前，向其添加当事方编号。
+ **系统中断：** 在升级流程期间，您必须使 Finance and Operations 环境和 Customer Engagement 环境脱机。
+ **快照**：拍摄 Finance and Operations 和 Customer Engagement 应用的快照。 如果必须，则可以使用快照还原以前的状态。

## <a name="deployment"></a>部署

1. 从 [Dynamics-365-FastTrack-Implementation-Assets](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema) 下载模板。
2. 登录 [Azure 门户](https://portal.azure.com/)。
3. 创建[资源组](/azure/azure-resource-manager/management/manage-resource-groups-portal)。
4. 在创建的资源组中创建[存储帐户](/azure/storage/common/storage-account-create?tabs=azure-portal)。
5. 在创建的资源组中创建[数据工厂](/azure/data-factory/quickstart-create-data-factory-portal)。
6. 打开数据工厂，然后选择 **创作和监视** 磁贴。
7. 在 **管理** 选项卡上，选择 **ARM 模板**。
8. 选择 **导入 ARM 模板** 以导入 **当事方** 模板。
9. 将模板导入到数据工厂中。 为 **项目详细信息** 和 **实例详细信息** 输入以下值。

    | 字段 | 值 |
    |---|---|
    | 预订 | Azure 预订 |
    | 资源组 | 提供在其下创建存储帐户的相同资源。 |
    | 区域 | 区域 |
    | 工厂名称 | 工厂名称 |
    | FO Linked Service_service Principal Key | 应用程序的密钥 |
    | Azure Blob Storage_connection String | Azure Blob 存储连接字符串 |
    | Dynamics Crm Linked Service_password | 您指定为用户名的用户帐户的密码 |
    | FO Linked Service_properties_type Properties_url | `https://sampledynamics.sandbox-operationsdynamics.com/data` |
    | FO Linked Service_properties_type Properties_tenant | 关于您的应用程序所在租户的信息（域名或租户 ID） |
    | FO Linked Service_properties_type Properties_aad Resource Id | `https://sampledynamics.sandboxoperationsdynamics.com` |
    | FO Linked Service_properties_type Properties_service Principal Id | 应用程序的客户端 ID |
    | Dynamics Crm Linked Service_properties_type Properties_username | 用于连接到 Dynamics 365 的用户名 |

    有关详细信息，请参阅以下主题：

    - [手动提升每个环境的资源管理器模板](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment)
    - [链接服务属性](/azure/data-factory/connector-dynamics-ax#linked-service-properties)
    - [使用 Azure 数据工厂复制数据](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)

10. 部署后，验证数据工厂的数据集、数据流和链接服务。

    ![数据集、数据流和链接服务。](media/data-factory-validate.png)

11. 转到 **管理**。 在 **连接** 下，选择 **链接服务**。 然后选择 **DynamicsCrmLinkedService**。 在 **编辑链接服务 (Dynamics CRM)** 对话框中，输入以下值。

    | 字段 | 值 |
    |---|---|
    | Name | DynamicsCrmLinkedService |
    | 说明 | 要与 CRM 实例连接以提取实体数据的链接服务 |
    | 通过集成运行时连接 | AutoResolvelntegrationRuntime |
    | 部署类型 | 联机 |
    | 服务 URI | `https://<organization-name>.crm[x].dynamics.com` |
    | 身份验证类型 | Office365 |
    | 用户名 | |
    | 密码或 Azure 密钥保管库 | 密码 |
    | 密码 | |

## <a name="prepare-to-run-the-data-factory-templates"></a>准备运行数据工厂模板

本节描述运行当事方邮政地址和当事方电子地址数据工厂模板之前所需进行的设置。

### <a name="setup-to-run-the-party-postal-address-template"></a>设置以运行当事方邮政地址模板

1. 登录到 Customer Engagement 应用，然后转到 **设置** \> **个性化设置**。 然后，在 **常规** 选项卡上为系统管理员帐户配置时区设置。 时区必须采用协调世界时 (UTC) 格式，才能更新 Finance and Operations 应用中邮政地址的“生效日期”和“失效日期”。

    ![系统管理员帐户的时区设置。](media/ADF-1.png)

2. 在“数据工厂中 **管理** 选项卡上的 **全局参数** 下面，创建以下全局参数。

    | 编号 | Name | 类型 | 值 |
    |---|---|---|---|
    | 1 | PostalAddressIdPrefix | 字符串 | 此参数将序列号作为前缀追加到新创建的邮寄地址。 请务必提供与 Finance and Operations 应用和 Customer Engagement 应用中的邮政地址不冲突的字符串。 例如，使用 **ADF-PAD-**。 |

    ![在“管理”选项卡上创建的 PostalAddressIdPrefix 全局参数。](media/ADF-2.png)

3. 当您完成时，选择 **全部发布**。

    ![“全部发布”按钮。](media/ADF-3.png)

### <a name="setup-to-run-the-party-electronic-address-template"></a>设置以运行当事方电子地址模板

1. 在“数据工厂中 **管理** 选项卡上的 **全局参数** 下面，创建以下全局参数。

    | 编号 | Name | 类型 | 值 |
    |---|---|---|---|
    | 1 | IsFOSource | 布尔型 | 此参数确定在发生冲突时将替换哪些主要系统地址。 如果值为 **true**，则 Finance and Operations 应用中的主要地址将替换 Customer Engagement 应用中的主要地址。 如果值为 **false**，则 Customer Engagement 应用中的主要地址将替换 Finance and Operations 应用中的主要地址。 |
    | 2 | ElectronicAddressIdPrefix | 字符串 | 此参数将序列号作为前缀追加到新创建的电子地址。 请务必提供与 Finance and Operations 应用和 Customer Engagement 应用中的电子地址不冲突的字符串。 例如，使用 **ADF-EAD-**。 |

    ![在“管理”选项卡上创建的 IsFOSource 和 ElectronicAddressIdPrefix 全局参数。](media/ADF-4.png)

2. 当您完成时，选择 **全部发布**。

## <a name="run-the-templates"></a>运行模板

1. 停止以下使用财务和运营应用的 **当事方**、**客户**、**联系人** 和 **供应商** 双重写入映射。

    + CDS 当事方 (msdyn_parties) 
    + 客户 V3 (accounts)
    + 客户 V3（联系人）
    + CDS 联系人 V2（联系人）
    + CDS 联系人 V2（联系人）
    + 供应商 V2 (msdyn_vendor)
    + 联系人 V2 (msdyn_contactforparties)
    + CDS 当事方邮寄地址位置 (msdyn_partypostaladdresses)
    + CDS 邮寄地址历史记录 V2 (msdyn_postaladdresses)
    + CDS 邮寄地址位置 (msdyn_postaladdresscollections)
    + 当事方联系人 V3 (msdyn_partyelectronicaddresses)

2. 确保从 Dataverse 的 **msdy_dualwriteruntimeconfig** 表中删除地图。
3. 从 AppSource 中安装[双重写入当事方和全球通讯簿解决方案](https://aka.ms/dual-write-gab)。
4. 在 Finance and Operations 应用中，如果以下表包含数据，则针对它们运行 **初始同步**。

    + 称呼
    + 人员特点类型
    + 结束语
    + 联系人职务
    + 决策角色
    + 忠诚度级别

5. 在 Customer Engagement 应用中，禁用以下插件步骤：

    + 帐户更新

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity：帐户的更新
        + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes：帐户的更新

    + 联系人更新

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity：联系人的更新
        + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact：联系人的更新

    + msdyn_party 更新

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity：msdyn_party 的更新

    + msdyn_vendor 更新

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity：msdyn_vendor 的更新

    + Customeraddress

        + 创建

            + Microsoft.Dynamics.GABExtended.Plugins.CreatePartyAddress：创建 customeraddress

        + 更新

            + Microsoft.Dynamics.GABExtended.Plugins.CreatePartyAddress：更新 customeraddress

        + 删除

            + Microsoft.Dynamics.GABExtended.Plugins.DeleteCustomerAddress：删除 customeraddress

    + msdyn_partypostaladdress

        + 创建

            + Microsoft.Dynamics.GABExtended.Plugins.CreateCustomerAddress：创建 msdyn_partypostaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.PartyPostalAddress：创建 msdyn_partypostaladdress

        + 更新

            + Microsoft.Dynamics.GABExtended.Plugins.CreateCustomerAddress：更新 msdyn_partypostaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.PartyPostalAddress：更新 msdyn_partypostaladdress

    + msdyn_postaladdress

        + 创建

            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddress：创建 msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddressPostCreate：创建 msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.UpdateCustomerAddress：创建 msdyn_postaladdress

        + 更新

            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddressUpdate：更新 msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.UpdateCustomerAddress：更新 msdyn_postaladdress

    + msdyn_partyelectronicaddress

        + 创建

            + Microsoft.Dynamics.GABExtended.Plugins.PartyElectronicAddressSync：创建 msdyn_partyelectronicaddress

        + 更新

            + Microsoft.Dynamics.GABExtended.Plugins.PartyElectronicAddressSync：更新 msdyn_partyelectronicaddress

        + 删除

            + Microsoft.Dynamics.GABExtended.Plugins.DeletePartyElectronicAddressSync：删除 msdyn_partyelectronicaddress

6. 在 Customer Engagement 应用中，禁用以下工作流：

    + 在“客户”表中创建供应商
    + 在“客户”表中创建供应商
    + 在“联系人”表中创建个人类型的供应商
    + 在“供应商”表中创建“个人”类型的供应商
    + 在“客户”表中更新供应商
    + 在“供应商”表中更新供应商
    + 在“联系人”表中更新“个人”类型的供应商
    + 在“供应商”表中更新“个人”类型的供应商

7. 在数据工厂中，通过选择 **立即触发** 运行模板，如下图所示。 根据数据量，此流程可能需要几个小时才能完成。

    ![运行模板。](media/data-factory-trigger.png)

    > [!NOTE]
    > 如果您有 **客户**、**联系人** 和 **供应商** 的自定义，则必须修改模板。

8. 将新 **当事方** 记录导入到 Finance and Operations 应用中。

    1. 从 Azure Blob 存储中下载 **FONewParty.csv** 文件。 路径为 **partybootstrapping/output/FONewParty.csv**。
    2. 将 **FONewParty.csv** 文件转换为 Excel 文件并将 Excel 文件导入到 Finance and Operations 应用中。 或者，如果 CSV 导入适合您，您可以直接导入 .csv 文件。 根据数据量，此步骤可能需要几个小时才能完成。 有关详细信息，请参阅[数据导入和导出作业概述](../data-import-export-job.md)。

    ![正在导入 Dataverse 当事方记录。](media/data-factory-import-party.png)

9. 在数据工厂中，一个接一个地运行当事方邮政地址和当事方电子地址模板。

    + 当事方邮政地址模板将更新 Customer Engagement 应用中的所有邮政地址记录，并将它们与相应的 **客户**、**联系人** 和 **供应商** 记录相关联。 它还生成三个 .csv 文件：ImportFONewPostalAddressLocation.csv、ImportFONewPartyPostalAddress.csv 和 ImportFONewPostalAddress.csv。
    + 当事方电子地址模板将更新 Customer Engagement 应用中的所有电子地址，并将它们与相应的 **客户**、**联系人** 和 **供应商** 记录相关联。 它还生成一个 .csv 文件：ImportFONewElectronicAddress.csv。

    ![运行当事方邮政地址和当事方电子地址模板。](media/ADF-7.png)

10. 要使用此数据更新 Finance and Operations 应用，您必须将 .csv 文件转换为 Excel 工作簿，并[将其导入到 Finance and Operations 应用中](/data-entities/data-import-export-job)。 或者，如果 CSV 导入适合您，您可以直接导入 .csv 文件。 根据数据量，此步骤可能需要几个小时才能完成。

    ![导入成功。](media/ADF-8.png)

11. 在 Customer Engagement 应用中，启用以下插件步骤：

    + 帐户更新

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity：帐户的更新
        + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes：帐户的更新

    + 联系人更新

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity：联系人的更新
        + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact：联系人的更新

    + msdyn_party 更新

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity：msdyn_party 的更新

    + msdyn_vendor 更新

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity：msdyn_vendor 的更新

    + msdyn_partypostaladdress

        + 创建

            + Microsoft.Dynamics.GABExtended.Plugins.CreateCustomerAddress：创建 msdyn_partypostaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.PartyPostalAddress：创建 msdyn_partypostaladdress

        + 更新

            + Microsoft.Dynamics.GABExtended.Plugins.CreateCustomerAddress：更新 msdyn_partypostaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.PartyPostalAddress：更新 msdyn_partypostaladdress

    + msdyn_postaladdress

        + 创建

            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddress：创建 msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddressPostCreate：创建 msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.UpdateCustomerAddress：创建 msdyn_postaladdress

        + 更新

            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddressUpdate：更新 msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.UpdateCustomerAddress：更新 msdyn_postaladdress
 
    + msdyn_partyelectronicaddress

        + 创建

            + Microsoft.Dynamics.GABExtended.Plugins.PartyElectronicAddressSync：创建 msdyn_partyelectronicaddress

        + 更新

            + Microsoft.Dynamics.GABExtended.Plugins.PartyElectronicAddressSync：更新 msdyn_partyelectronicaddress

        + 删除

            + Microsoft.Dynamics.GABExtended.Plugins.DeletePartyElectronicAddressSync：删除 msdyn_partyelectronicaddress

12. 在 Customer Engagement 应用中，如果以前停用了以下工作流，请激活它们：

    + 在“客户”表中创建供应商
    + 在“客户”表中创建供应商
    + 在“联系人”表中创建个人类型的供应商
    + 在“供应商”表中创建“个人”类型的供应商
    + 在“客户”表中更新供应商
    + 在“供应商”表中更新供应商
    + 在“联系人”表中更新“个人”类型的供应商
    + 在“供应商”表中更新“个人”类型的供应商

13. 运行与 **当事方** 相关的地图，如[当事方和全球通讯簿](party-gab.md)中所述。

## <a name="explanation-of-the-data-factory-templates"></a>数据工厂模板的说明

此节将指导您完成每个数据工厂模板中的步骤。

### <a name="steps-in-the-party-template"></a>当事方模板中的步骤

1. 步骤 1 到 6 标识为双重写入启用的公司并为其生成筛选器子句。
2. 步骤 7-1 到 7-9 从 Finance and Operations 应用和 Customer Engagement 应用检索数据，并暂存该数据以进行升级。
3. 步骤 8 到 9 在 Finance and Operations 应用与 Customer Engagement 应用之间比较 **客户**、**联系人** 和 **供应商** 记录的当事方编号。 将跳过没有当事方编号的任何记录。
4. 步骤 10 会为必须在 Customer Engagement 应用和 Finance and Operations 应用中创建的当事方记录生成两个 .csv 文件。

    - **FOCDSParty.csv** - 该文件包含两个系统的所有当事方记录，无论是否为双重写入启用了公司。
    - **FONewParty.csv** - 此文件包含 Dataverse 了解的当事方记录的子集（例如，**目标客户** 类型的客户）。

5. 步骤 11 将在 Customer Engagement 应用中创建当事方。
6. 步骤 12 将从 Customer Engagement 应用中检索当事方的全局唯一标识符 (GUID)，并暂存它们，以便它们在后续步骤中能够与 **客户**、**联系人** 和 **供应商** 记录关联。
7. 步骤 13 将 **客户**、**联系人** 和 **供应商** 记录与当事方 GUID 关联。
8. 步骤 14-1 到 14-3 使用当事方 GUID 更新 Customer Engagement 中的 **客户**、**联系人** 和 **供应商** 记录。
9. 步骤 15-1 到 15-3 针对 **客户**、**联系人** 和 **供应商** 记录准备 **当事方的联系人** 记录。
10. 步骤 16-1 到 16-7 检索参考数据，如称呼和人员特点类型，并将其与 **当事方的联系人** 记录关联。
11. 步骤 17 针对 **客户**、**联系人** 和 **供应商** 记录合并 **当事方的联系人** 记录。
12. 步骤 18 将 **当事方的联系人** 记录导入到 Customer Engagement 应用中。

### <a name="steps-in-the-party-postal-address-template"></a>当事方邮政地址模板中的步骤

1. 步骤 1-1 到 1-10 从 Finance and Operations 应用和 Customer Engagement 应用检索数据，并暂存该数据以进行升级。
2. 步骤 2 通过加入邮政地址和当事方邮政地址，在 Finance and Operations 应用中使邮政地址数据非规范化。
3. 步骤 3 删除 Customer Engagement 应用中客户、联系人和供应商地址数据重复项，并合并客户、联系人和供应商地址数据。
4. 步骤 4 为 Finance and Operations 应用创建 .csv 文件，以创建基于客户、联系人和供应商地址的新地址数据。
5. 步骤 5-1 为 Customer Engagement 应用创建 .csv 文件，以根据 Finance and Operations 应用和 Customer Engagement 应用创建所有地址数据。
6. 步骤 5-2 将 .csv 文件转换为 Finance and Operations 导入格式以手动导入。

    - ImportFONewPostalAddressLocation.csv
    - ImportFONewPartyPostalAddress.csv
    - ImportFONewPostalAddress.csv

7. 步骤 6 将邮寄地址集合数据导入到 Customer Engagement 应用中。
8. 步骤 7 从 Customer Engagement 应用中检索邮寄地址集合数据。
9. 步骤 8 创建客户地址数据并关联邮政地址集合 ID。
10. 步骤 9-1 到 9-2 将当事方和邮政地址集合 ID 与邮政地址和当事方邮政地址关联。
11. 步骤 10-1 到 10-3 将客户地址、邮政地址和当事方邮政地址导入到 Customer Engagement 应用中。

### <a name="steps-in-the-party-electronic-address-template"></a>当事方电子地址模板中的步骤

1. 步骤 1-1 到 1-5 从 Finance and Operations 应用和 Customer Engagement 应用检索数据，并暂存该数据以进行升级。
2. 步骤 2 在 Customer Engagement 应用中合并客户、联系人和供应商实体的电子地址。
3. 步骤 3 合并 Customer Engagement 应用和 Finance and Operations 应用中的主要电子地址数据。
4. 步骤 4 创建 .csv 文件。

    - 根据客户、联系人和供应商地址针对 Finance and Operations 应用创建新电子地址数据。
    - 根据 Finance and Operations 应用中的电子地址、客户、联系人和供应商地址，针对 Customer Engagement 应用创建新电子地址数据。

5. 步骤 5-1 将电子地址导入到 Customer Engagement 应用中。
6. 步骤 5-2 创建 .csv 文件以在 Customer Engagement 应用更新客户和联系人的主要地址。
7. 步骤 6-1 到 6-2 将客户和联系人主要地址导入到 Customer Engagement 应用中。

## <a name="troubleshooting"></a>疑难解答

1. 如果流程失败，请重新运行数据工厂。 从失败的活动开始。
2. 数据工厂生成的一些文件可用于数据验证。
3. 数据工厂基于 .csv 文件运行。 因此，如果任何字段值中包含逗号，则可能会干扰结果。 必须从字段值中删除所有逗号。
4. **监视** 选项卡提供有关所有步骤和已处理的数据的信息。 选择特定步骤以对其进行调试。

    ![监视选项卡。](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a>了解有关模板的详细信息

有关模板的详细信息，请参阅 [Azure 数据工厂模板自述文件注释](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md)。
