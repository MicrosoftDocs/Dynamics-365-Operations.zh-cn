---
title: 升级到当事方和全球通讯簿模型
description: 本主题介绍如何将双重写入数据升级到当事方和全球通讯簿模型。
author: RamaKrishnamoorthy
ms.date: 03/31/2021
ms.topic: article
ms.service: dynamics-ax-applications
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-31
ms.openlocfilehash: 76e64d483e833782733277a64d8dc37cbeba6130
ms.sourcegitcommit: 011468a6cffea8641bebc2922e0676d9f44b36fc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/06/2021
ms.locfileid: "5857362"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a>升级到当事方和全球通讯簿模型

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

[Azure 数据工厂模板](https://aka.ms/dual-write-gab-adf)帮助您将采用双重写入的现有 **帐户**、**联系人** 和 **供应商** 表数据升级到当事方和全球通讯薄模型。 模板将对帐 Finance and Operations 应用和 Customer Engagement 应用程序中的数据。 在流程结束时，**当事方** 记录的 **当事方** 和 **联系人** 字段将创建，并与在 Customer Engagement 应用程序中的 **帐户**、**联系人** 和 **供应商** 记录相关联。 将生成 .csv 文件 (`FONewParty.csv`) 以在 Finance and Operations 应用内创建新 **当事方** 记录。 本主题提供使用数据工厂模板和升级数据的说明。

如果没有任何自定义，可以按原样使用模板。 如果您有 **帐户**、**联系人** 和 **供应商** 的自定义，则必须使用以下说明修改模板。

> [!Note]
> 该模板可帮助仅升级 **当事方** 数据。 在将来的版本中，将包括邮寄地址和电子地址。

## <a name="prerequisites"></a>先决条件

需要以下先决条件：

+ [Azure 预订](https://portal.azure.com/)
+ [模板访问权限](https://aka.ms/dual-write-gab-adf)
+ 您是现有的双重写入客户。

## <a name="prepare-for-the-upgrade"></a>准备升级

+ **完全同步**：两种环境对于 **帐户(客户)**、**联系人** 和 **供应商** 均处于完全同步状态。
+ **集成密钥**：Customer Engagement 应用中的 **帐户(客户)**、**联系人** 和 **供应商** 表使用现成提供的集成密钥。 如果已自定义集成密钥，必须自定义模板。
+ **当事方编号**：将升级的所有 **帐户(客户)**、**联系人** 和 **供应商** 记录都具有 **当事方** 编号。 将忽略没有 **当事方** 编号的记录。 如果要升级这些记录，请在开始升级流程之前，向其添加 **当事方** 编号。
+ **系统中断**：在升级流程期间，您必须使 Finance and Operations 和 Customer Engagement 环境脱机。
+ **快照**：拍摄 Finance and Operations 和 Customer Engagement 应用的快照。 如果需要，使用快照还原以前的状态。

## <a name="deployment"></a>部署

1. 从 [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf) 下载模板。

2. 登录到 [Microsoft Azure](https://portal.azure.com/)。

3. 创建[资源组](https://docs.microsoft.com/azure/azure-resource-manager/management/manage-resource-groups-portal)。

4. 在创建的资源组中创建[存储帐户](https://docs.microsoft.com/azure/storage/common/storage-account-create?tabs=azure-portal)。

5. 在创建的上述资源组中创建[数据工厂](https://docs.microsoft.com/azure/data-factory/quickstart-create-data-factory-portal)。

6. 打开数据工厂，然后选择 **创作和监视** 磁贴。

7. 在 **管理** 选项卡上，选择 **ARM 模板**。

8. 选择 **导入 ARM 模板** 以导入 **当事方** 模板。

9. 将模板导入到数据工厂中。 为 **项目详细信息** 和 **实例详细信息** 输入以下值。

    字段 | 值
    ---|---
    预订 | Azure 预订
    资源组 | 提供在其下创建存储帐户的相同资源。
    区域 | 指定区域。
    工厂名称 | 指定工厂名称。
    FO Linked Service_service Principal Key | 指定应用程序的密钥。
    Azure Blob Storage_connection String | Azure Blob 存储连接字符串。
    Dynamics Crm Linked Service_password | 您指定为用户名的用户帐户的密码。
    FO Linked Service_properties_type Properties_url  | `https://sampledynamics.sandbox-operationsdynamics.com/data`
    FO Linked Service_properties_type Properties_tenant | 指定您的应用程序所在的租户信息（域名或租户 ID）。
    FO Linked Service_properties_type Properties_aad Resource Id | `https://sampledynamics.sandboxoperationsdynamics.com`
    FO Linked Service_properties_type Properties_service Principal Id | 指定应用程序的客户端 ID。
    Dynamics Crm Linked Service_properties_type Properties_username | 连接到 Dynamics 的用户名。

    有关详细信息，请参阅[手动提升每个环境的资源管理器模板](https://docs.microsoft.com/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment)、[链接服务属性](https://docs.microsoft.com/azure/data-factory/connector-dynamics-ax#linked-service-properties)和[使用 Azure 数据工厂复制数据](https://docs.microsoft.com/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)

10. 部署后，验证数据工厂的数据集、数据流和链接服务。

   ![数据集、数据流和链接服务](media/data-factory-validate.png)

11. 导航到 **管理**。 在 **连接** 下，选择 **链接服务**。 选择 **DynamicsCrmLinkedService**。 在 **编辑链接服务 (Dynamics CRM)** 窗体中，输入以下值：

    字段 | 值
    ---|---
    姓名 | DynamicsCrmLinkedService
    说明 | 要与 CRM 实例连接以提取实体数据的链接服务
    通过集成运行时连接 | AutoResolvelntegrationRuntime
    部署类型 | 联机
    服务 URI | `https://<organization-name>.crm[x].dynamics.com`
    身份验证类型 | Office365
    用户名 |
    密码或 Azure 密钥保管库 | 密码
    密码 |

## <a name="run-the-template"></a>运行模板

1. 使用 Finance and Operations 应用停止以下 **帐户**、**联系人** 和 **供应商** 双重写入。

    + 客户 V3 (accounts)
    + 客户 V3（联系人）
    + CDS 联系人 V2（联系人）
    + CDS 联系人 V2（联系人）
    + 供应商 V2 (msdyn_vendor)

2. 确保从 Dataverse 的 `msdy_dualwriteruntimeconfig` 表中删除地图。

3. 从 AppSource 中安装[双重写入当事方和全球通讯簿解决方案](https://aka.ms/dual-write-gab)。

4. 在 Finance and Operations 应用中，如果以下表包含数据，则针对它们运行 **初始同步**。

    + 称呼
    + 人员特点类型
    + 结束语
    + 联系人职务
    + 决策角色
    + 忠诚度级别

5. 在 Customer Engagement 应用中，禁用以下插件步骤。

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

    ![触发器运行](media/data-factory-trigger.png)

    > [!NOTE]
    > 如果您有 **帐户**、**联系人** 和 **供应商** 的自定义，则必须修改模板。

8. 在 Finance and Operations 应用中导入新 **当事方** 记录。

    + 从 Azure Blob 存储中下载 `FONewParty.csv` 文件。 路径为 `partybootstrapping/output/FONewParty.csv`。
    + 将 `FONewParty.csv` 文件转换为 Excel 文件并将 Excel 文件导入到 Finance and Operations 应用中。  如果 csv 导入适合您，您可以直接导入 csv 文件。 导入可能需要几个小时才能运行，具体取决于数据量。 有关详细信息，请参阅[数据导入和导出作业概述](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-import-export-job)。

    ![导入 Datavers 当事方记录](media/data-factory-import-party.png)

9. 在 Customer Engagement 应用中，启用以下插件步骤：

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

10. 在 Customer Engagement 应用中，如果您在前面的步骤中停用了以下工作流，请激活它们：

    + 在“客户”表中创建供应商
    + 在“客户”表中创建供应商
    + 在“联系人”表中创建个人类型的供应商
    + 在“供应商”表中创建“个人”类型的供应商
    + 在“客户”表中更新供应商
    + 在“供应商”表中更新供应商
    + 在“联系人”表中更新“个人”类型的供应商
    + 在“供应商”表中更新“个人”类型的供应商

11. 运行与 **当事方** 相关的地图，如[当事方和全球通讯簿](party-gab.md)中所示。

## <a name="troubleshooting"></a>疑难解答

1. 如果流程失败，从失败的活动开始重新运行数据工厂。
2. 某些文件由可用于数据验证目的的数据工厂生成。
3. 基于以逗号分隔的 csv 文件运行数据工厂。 如果字段值带有逗号，则可能会干扰结果。 您需要删除逗号。
4. **监视** 选项卡提供有关所有步骤和已处理的数据的信息。 选择特定步骤以对其进行调试。

    ![监视选项卡](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a>了解有关模板的详细信息

您可以在 [readme.md](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md) 文件中找到模板的注释。
