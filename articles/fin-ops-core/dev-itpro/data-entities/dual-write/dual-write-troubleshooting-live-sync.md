---
title: 解决实时同步问题
description: 本文提供故障排除信息，可以帮助您解决实时同步问题。
author: RamaKrishnamoorthy
ms.date: 08/19/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: b6650c92d22aee5394460e4e32bfd0ad3a7698c7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289445"
---
# <a name="troubleshoot-live-synchronization-issues"></a>解决实时同步问题

[!include [banner](../../includes/banner.md)]



本文提供财务和运营应用与 Microsoft Dataverse 之间的双写入集成的疑难解答信息。 具体来说，提供可以帮助您解决实时同步问题的信息。

> [!IMPORTANT]
> 本文解决的某些问题可能需要系统管理员角色或 Azure Active Directory (Azure AD) 租户管理员凭据。 每一节说明是否需要特定角色或特定凭据。

## <a name="live-synchronization-shows-an-error-when-you-create-a-row"></a>实时同步在您创建行时显示错误

当您在财务和运营应用中创建行时，您可能会收到以下错误消息：

*\[{\\"error\\":{\\"code\\":\\"0x80072560\\",\\"message\\":\\"此用户不是组织的成员。\\"}}\]，远程服务器返回错误：(403) 已禁止。"}}".*

要解决此问题，请按照[系统要求和先决条件](requirements-and-prerequisites.md)中的步骤操作。 要完成这些步骤，在 Dataverse 中创建的双写入应用程序用户必须具有系统管理员角色。 默认的负责团队也必须具有系统管理员角色。

## <a name="live-synchronization-shows-an-error-when-you-try-to-save-table-data"></a>实时同步在您尝试保存表数据时显示错误

**解决此问题所需的角色：** 系统管理员

当您尝试在财务和运营应用中保存表数据时，您可能会收到以下错误消息：

*无法将更改保存到数据库。工作单元无法提交事务。无法将数据写入实体 uoms。写入 UnitOfMeasureEntity 失败，并显示错误消息“无法与实体 uoms 同步”。*

要解决此问题，请确保财务和运营应用和 Dataverse 中都存在必备的参考数据。 例如，客户记录属于特定客户组，请确保 Dataverse 中存在该客户组记录。

如果两处都存在数据，并且您已确认问题与数据无关，请按照以下步骤操作。

1. 使用 Excel 加载项打开 **DualWriteProjectConfigurationEntity** 实体。 若要使用加载项，请在财务和运营 Excel 加载项中启用设计模式，并将 **DualWriteProjectConfigurationEntity** 添加到工作表中。 有关详细信息，请参阅[使用 Excel 查看和更新实体数据](../../office-integration/use-excel-add-in.md)。
2. 选择并删除在双重写入映射和项目中有问题的记录。 每个双重写入映射将有两条记录。
3. 使用 Excel 加载项发布更改。 此步骤非常重要，因为它会从实体和基础表中删除记录。

## <a name="handle-read-or-write-privilege-errors-when-you-create-data-in-a-finance-and-operations-app"></a>在财务和运营应用中创建数据时处理读或写特权错误

当您在财务和运营应用中创建数据时，您可能会收到“错误请求”错误消息。

![“错误请求”错误消息的示例。](media/error_record_id_source.png)

若要解决此问题，您必须启用缺少的权限，方法是为映射的 Dynamics 365 Sales 或 Dynamics 365 Customer Service 业务单位的团队分配正确的安全角色。

1. 在财务和运营应用中，找到在数据集成连接集中映射的业务单位。

    ![组织映射。](media/mapped_business_unit.png)

2. 在 Customer Engagement 应用中，登录环境，转至 **设置 \> 安全**，然后找到映射业务单位的团队。

    ![映射业务单位的团队。](media/setting_security_page.png)

3. 打开团队的页面以进行编辑，然后选择 **管理角色**。

    ![管理角色按钮。](media/manage_team_roles.png)

4. 在 **管理团队角色** 对话框中，分配具有为相关表读/写权限的角色，然后选择 **确定**。

## <a name="fix-synchronization-issues-in-an-environment-that-has-a-recently-changed-dataverse-environment"></a>在最近更改了 Dataverse 环境的环境中解决同步问题

**解决此问题所需的角色：** 系统管理员

当您在财务和运营应用中创建数据时，您可能会收到以下错误消息：

*{"entityName":"CustCustomerV3Entity","executionStatus":2,"fieldResponses":\[\],"recordResponses":\[{"errorMessage":"**无法为实体 CustCustomerV3Entity 生成有效负载**","logDateTime":"2019-08-27T18:51:52.5843124Z","verboseError":"有效负载创建失败，显示错误“URI 无效：此 URI 是空的”。"}\],"isErrorCountUpdated":true}*

下面是 Customer Engagement 应用中的错误消息：

> ISV 代码发生意外错误。 (ErrorType = ClientError) 插件发生意外异常 (Execute)：Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: System.Exception：无法处理实体帐户 -（连接尝试失败，因为连接方未在一段时间后正确响应，或由于连接的主机未能响应导致建立的连接失败。

如果在您尝试在财务和运营应用中创建数据时未正确重置 Dataverse 环境，将发生此错误。

> [!IMPORTANT]
> 如果您已重新链接环境，则必须先停止所有实体映射，然后才能继续执行缓解步骤。

若要解决此问题，您必须同时完成 Dataverse 和财务和运营应用中的步骤。

1. 在财务和运营应用中，执行以下步骤：

    1. 使用 Excel 加载项打开 **DualWriteProjectConfigurationEntity** 实体。 若要使用加载项，请在财务和运营 Excel 加载项中启用设计模式，并将 **DualWriteProjectConfigurationEntity** 添加到工作表中。 有关详细信息，请参阅[使用 Excel 查看和更新实体数据](../../office-integration/use-excel-add-in.md)。
    2. 选择并删除在双重写入映射和项目中有问题的记录。 每个双重写入映射将有两条记录。
    3. 使用 Excel 加载项发布更改。 此步骤非常重要，因为它会从实体和基础表中删除记录。
    4. 若要帮助防止重新链接财务和运营或 Dataverse 环境时出错，请确保未保留双重写入配置。

2. 在 Dataverse 中执行以下步骤：

    1. 登录您的 Dataverse 环境（例如 `https://*****.crm.dynamics.com/`）。
    2. 转到 **高级设置**\>**高级查找**。
    3. 选择 **双重写入运行时配置**。
    4. 选择要查看的列。
    5. 选择 **结果** 以查看配置。
    6. 删除所有实例。

3. 在财务和运营应用中，执行以下步骤：

    1. 使用 Excel 加载项打开 **DualWriteProjectConfigurationEntity** 实体。 若要使用加载项，请在财务和运营 Excel 加载项中启用设计模式，并将 **DualWriteProjectConfigurationEntity** 添加到工作表中。 有关详细信息，请参阅[使用 Excel 查看和更新实体数据](../../office-integration/use-excel-add-in.md)。
    2. 选择并删除在双重写入映射和项目中有问题的记录。 每个双重写入映射将有两条记录。
    3. 使用 Excel 加载项发布更改。 此步骤非常重要，因为它会从实体和基础表中删除记录。
    4. 若要帮助防止重新链接财务和运营或 Dataverse 环境时出错，请确保未保留双重写入配置。

## <a name="live-synchronization-error-after-you-do-a-full-database-copy"></a>执行数据库完全复制后发生实时同步错误

在运行从一个系统到另一个系统的数据库完全复制之后，运行数据库操作时，可能会收到以下错误消息：

*SecureConfig 组织 (???) 与实际 CRM 组织 (???) 不匹配。*

显示的错误消息来自双重写入运行时插件，目的是确保在一个系统中设置的双重写入配置不能在另一个系统中使用。

若要解决此问题，请在还原数据库后删除 **msdyn_dualwriteruntimeconfig** 表中的所有记录。 有关详细信息，请参阅[取消链接再重新链接双重写入环境](relink-environments.md)。

## <a name="live-synchronization-issues-that-are-caused-by-incorrect-query-filter-syntax-on-the-dual-write-maps"></a>双重写入映射中查询筛选器语法错误导致实时同步问题

即使双重写入映射筛选器的查询表达式在语法上是正确的，也可能无法正常工作。 筛选器表达式位于实体上，而不是位于查询对象的单个数据源上。 因此，生成的 SQL 查询不会返回预期结果。

下面是一个示例。

```dos
Query entity = PROJECTENTITY
Query expression = (ParentProject == "")
```

您可能希望筛选掉无父级的项目。但是，此筛选器无法工作，因为其已转换为类似以下示例的查询。

```sql
SELECT T1.RECID,T1.MODIFIEDDATETIME,T1.RECVERSION,T1.RECID,T1.DIMENSION,
T1.LOCATION,T1.PROJECTCONTROLLER,T1.PROJECTID,T1.PROJECTMANAGER,T1.REFERENCE,
T1.SALESMANAGER,T1.SCHEDULED,T1.RECVERSION#8,T1.RECVERSION#7,
T1.RECVERSION#6,T1.RECVERSION#5,T1.RECVERSION#4,T1.RECVERSION#3,
T1.RECVERSION#2,T1.RECID#8,T1.RECID#7,T1.RECID#6,T1.RECID#5,
T1.RECID#4,T1.RECID#3,T1.RECID#2,T1.PARTITION FROM PROJECTENTITY T1 
WHERE(((((((((((PARTITION=5637144576) AND (DATAAREAID=N'usmf')) AND 
((PARTITION#2=5637144576) OR (PARTITION#2 IS NULL))) AND 
((PARTITION#3=5637144576) OR (PARTITION#3 IS NULL))) AND 
((PARTITION#4=5637144576) OR (PARTITION#4 IS NULL))) AND 
((PARTITION#5=5637144576) OR (PARTITION#5 IS NULL))) AND 
((PARTITION#6=5637144576) OR (PARTITION#6 IS NULL))) AND 
((PARTITION#7=5637144576) OR (PARTITION#7 IS NULL))) AND 
((PARTITION#8=5637144576) OR (PARTITION#8 IS NULL))) AND 
((DATAAREAID#8=N'usmf') OR (DATAAREAID#8 IS NULL))) AND 
(PARENTPROJECT='')) 
ORDER BY T1.PROJECTID
```

实际结果是 `parentProject` 字段求值为 `null`。 但是，`null` 与空字符串不同。 由于此不匹配，查询筛选器不返回有效结果。

若要解决此问题，请按照以下步骤操作。

1. 添加可在扩展模型中添加，并受将 `null` 转换为空字符串的逻辑支持的计算列。

    ```dos
    SysComputedColumn::if(SysComputedColumn::isNullExpression(ParentProject), SysComputedColumn::returnLiteral(""), fieldName);
    ```

2. 对新计算列使用此筛选器，而不是对默认列使用。

若要在开发环境中评估此筛选器，可以使用下面的 X++ 代码验证结果。 将此代码作为独立程序运行。 可以将其用于在对双重写入映射使用适用于实体的不同类型筛选器之前，评估这些筛选器。 可以对数据库运行此查询，以评估差异。

```xpp
var entityName = "PROJECTENTITY";
var filterExpression = '(ParentProject == "")';
Query query = new Query();
query.literals(NoYes::Yes); 
QueryBuildDataSource qbd = query.addDataSource(tablename2id(entityName));
qbd.addRange(fieldname2id(qbd.table(),identifierStr(RecVersion))).value(filterExpression);
qbd.addSelectionField(fieldname2id(qbd.table(),identifierStr(RecId)));
QueryRun qRun = new QueryRun(query);
// This provides the actual sql statement to execute
var actualSqlStatement = query.getSQLStatement();
while(qRun.next())
{
    var rec = qRun.get(tableName2Id(entityName));
}
```

## <a name="data-from-finance-and-operations-apps-isnt-synced-to-dataverse"></a>财务和运营应用中的数据未同步到 Dataverse

在实时同步期间，您可能会遇到以下问题：只有部分数据从财务和运营应用同步到 Dataverse，或者数据根本不同步。

> [!NOTE]
> 您必须在开发期间解决此问题。

在开始修复问题之前，请检查以下先决条件：

+ 请确保在单个交易记录范围内写入自定义更改。
+ 业务事件和双重写入框架不处理 `doinsert()`/`doUpdate()` 和 `recordset()` 运算或带有 `skipBusinessEvents(true)` 标记的记录。 如果您的代码在这些函数内，将不会触发双重写入。
+ 必须为映射的数据源注册业务事件。 某些数据源可能使用外部联接，并且可能在财务和运营应用中标记为只读。 不跟踪这些数据源。
+ 仅当对映射的字段进行修改，才会触发更改。 修改未映射的字段不会触发双重写入。
+ 确保筛选器评估提供有效结果。

### <a name="troubleshooting-steps"></a>疑难解答步骤

1. 检查双重写入管理页面上的字段映射。 如果字段未从财务和运营应用映射到 Dataverse，则将不会跟踪该字段。 例如，在下图中，**说明** 字段从 Dataverse 跟踪，而不是从财务和运营应用跟踪。 将不会跟踪在财务和运营应用内对该字段所做的更改。

    ![跟踪的字段。](media/live-sync-troubleshooting-1.png)

2. 确定是否在业务事件定义中跟踪数据源。 例如，在下图中，将不跟踪是否对 **DefaultDimensionDAVs** 表和基础表中的字段进行了更改。 将不跟踪使用外部联接的数据源和标记为只读的数据源。

    ![不跟踪的字段。](media/live-sync-troubleshooting-2.png)

3. 确定 **BUSINESSEVENTSDEFINITION** 表中是否显示映射表字段，如下图中所示。 如果在查询结果中找不到要查找的字段，说明双重写入不会触发该字段。

    ![表中跟踪的字段。](media/live-sync-troubleshooting-3.png)

### <a name="sample-scenario"></a>示例场景

在财务和运营应用中，已更新联系人记录的地址，但对地址的更改未同步到 Dataverse。 出现此情况的原因是，**BusinessEventsDefinition** 表中的所有记录都没有受影响表和实体的组合。 特别是，**LogisticsPostalAddress** 表不是 **smmContactpersonCDSV2Entity** 实体的直接数据源。 **smmContactpersonCDSV2Entity** 实体有 **smmContactPersonV2Entity** 充当数据源，而 **smmContactPersonV2Entity** 则有 **LogisticsPostalAddressBaseEntity** 充当数据源。 **LogisticsPostalAddress** 表是 **LogisticsPostalAddressBaseEntity** 的数据源。

类似情况可能会出现在某些非标准模式中，例如，财务和运营应用中正在修改的表未明确链接到其所在实体中。 例如，在 **smmContactPersonCDSV2Entity** 实体中计算主地址数据。 双重写入框架尝试确定如何将对基础表的更改映射回实体。 此方法通常足够。 但是，在某些情况下，链接非常复杂，以至于您必须具体处理。 必须确保相关表的 **RecId** 在实体上直接可用。 然后添加一个静态方法来监视表的更改。

例如，查看 **smmContactPersonCDSV2Entity::getEntityDataSourceToFieldMapping()** 方法。 为了应对此情况，已修改了 **CustCustomerV3entity** 和 **VendVendorV2Entity**。

若要解决此问题，请按照以下步骤操作。

1. 向 **smmContactPersonV2Entity** 实体添加一个 **PrimaryPostalAddressRecId** 字段。 将其设为内部字段。

    ![字段已添加到 smmContactPersonV2Entity 实体。](media/Troubleshoot_live_sync_issue_1.png)

2. 将同一个字段添加到 **smmContactPersonCDSV2Entity** 实体中。

    ![字段已添加到 smmContactPersonCDSV2Entity 实体。](media/Troubleshoot_live_sync_issue_2.png)

3. 将以下方法添加到 **smmContactPersonCDSV2Entity** 类。

    ```xpp
    public static container getEntityDataSourceToFieldMapping(container mapping)
    {
        mapping += [[tablestr(smmContactPersonCDSV2Entity), tablenum(LogisticsPostalAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryPostalAddressRecId)]];
        return mapping;
    }
    ```

4. 同步数据库，然后生成应用程序。
5. 停止在 **smmContactPersonCDSV2Entity** 实体上创建的所有双重写入映射。
6. 启动映射。 您应该会看到您已通过使用其中的 **refentityname** 值等于 **BusinessEventsDefinition** 表中的 **smmContactPersonCDSV2Entity** 的行的 **RefTableName** 列跟踪的新表（此示例中为 **LogisticsPostalAddress**）。

## <a name="error-when-you-create-a-record-where-multiple-records-are-sent-from-a-finance-and-operations-app-to-dataverse-in-the-same-batch"></a>创建的记录中有多条记录在同一批处理中从财务和运营应用发送到 Dataverse 时出错

对于任何交易记录，财务和运营应用都将在批处理中创建数据，并将其作为批处理发送到 Dataverse。 如果两条记录作为同一个交易记录的组成部分创建，并且彼此引用，您可能会在财务和运营应用中收到如下示例的错误消息：

*无法向 aaa_fundingsources 实体写入数据。无法查找值为 {PC00...} 的 ebecsfs_contracts。无法查找值为 {PC00...} 的 aaa_fundingsources。写入 aaa_fundingsources 失败，错误消息为：异常消息：远程服务器返回了错误：(400) 错误请求。*

若要解决此问题，请在财务和运营应用中创建实体关系，以指示这两个实体彼此相关，并且相关记录将在同一条交易记录中处理。

## <a name="enable-verbose-logging-of-error-messages"></a>启用错误消息详细日志记录

在财务和运营应用中，您可能会遇到与 Dataverse 环境有关的错误。 错误消息中可能不包含消息的全文或其他相关数据。 若要获取详细信息，请启用详细日志记录，方法是在财务和运营应用中的所有项目配置内设置 **DualWriteProjectConfigurationEntity** 实体上存在的 **IsDebugMode** 标志。

1. 使用 Excel 加载项打开 **DualWriteProjectConfigurationEntity** 实体。 若要使用加载项，请在财务和运营 Excel 加载项中启用设计模式，并将 **DualWriteProjectConfigurationEntity** 添加到工作表中。 有关详细信息，请参阅[使用 Excel 查看和更新实体数据](../../office-integration/use-excel-add-in.md)。
2. 将项目的 **IsDebugMode** 标志设置为 **是**。
3. 运行场景。
4. 详细日志在 **DualWriteErrorLog** 表中提供。 若要使用表浏览器查找数据，请使用以下 URL：`https://XXXaos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=DualWriteErrorLog`。
5. 若要在调试模式下捕获更多日志，请安装 [KB 4595434（用于解决双重写入实时同步期间传播空值之一错误的修补程序）](https://fix.lcs.dynamics.com/Issue/Details?kb=4595434&bugId=527820&dbType=3&qc=c29ce15a80e6b3b4c01a722d9bdae1d7e71aa3662a044cfd0b765f736cfa98e9)中的更新。

## <a name="error-when-you-add-an-address-for-a-customer-or-contact"></a>为客户或联系人添加地址时出错

在财务和运营应用或 Dataverse 中尝试为客户或联系人添加地址时，可能会收到以下错误消息：

*无法向实体 msdyn_partypostaladdresses 写入数据。写入 DirPartyPostalAddressLocationCDSEntity 失败，错误消息为“请求失败，状态代码为 BadRequest，CDS 错误代码为： 0x80040265；响应消息为：插件中出错。已存在属性值为“位置 ID”的记录。实体键“位置 ID 键”需要这组属性包含唯一值。请选择唯一值并重试。*

若要解决此问题，请安装双重写入业务流程包版本 (2.2.2.60)，以便将定义 **地址** 表中的键定义为如下表中所示。

| 属性 | 值 |
|---|---|
| 显示名称 | **位置键** |
| 姓名 | **msdyn_locationkey** |
| 字段 | **msdyn_locationid**、**parentid** |
| 状态 | **可用** |
| 系统作业 | 空白 |

## <a name="error-when-you-add-a-customer-in-dataverse"></a>在 Dataverse 中添加客户时出错

当您尝试在 Dataverse 应用中添加客户时，您可能会收到以下错误消息：

*“RecordError0”：“实体 Customers V3 的写入失败，发生了未知异常 - 未找到当事方类型为‘组织’的当事方记录”}。*

在 Dataverse 中创建客户时，将生成新的当事方编号。 如果将客户记录与当事方一起同步到财务和运营应用，但是已经有一条具有其他当事方编号的客户记录时，将显示此错误消息。

若要解决此问题，请通过查找当事方查找客户。 如果不存在该客户，请新建一条客户记录。 如果确实存在该客户，请使用现有当事方创建新客户记录。

## <a name="error-when-you-create-a-new-customer-vendor-or-contact-in-dataverse"></a>在 Dataverse 中新建客户、供应商或联系人时出错

在 Dataverse 应用中尝试新建客户、供应商或联系人时，可能会收到以下错误消息：

*无法将当事方的类型从“DirOrganization”更新为“DirPerson”，应该改为先删除现有当事方，再插入新类型的当事方。*

在 Dataverse 中，**msdyn_party** 表内有编号规则。 如果在 Dataverse 中创建客户，将创建一个新的当事方（例如，类型为 **组织** 的 **Party-001**）。 此数据将发送到财务和运营应用。 如果重置 Dataverse 环境，或者将财务和运营环境链接到其他 Dataverse 环境，再在 Dataverse 中创建一条新的联系人记录，将创建一个以 **Party-001** 开头的新当事方值。 这次，创建的第三方记录将为 **Party-001**，并且其类型为 **个人**。 同步此数据时，财务和运营应用将显示前面的错误消息，因为已存在类型为 **组织** 的当事方记录 **Party-001**。

若要解决此问题，请在 Dataverse 中将 **msdyn_party** 表的 **msdyn_partynumber** 字段的自动编号规则更改为其他自动编号规则。

## <a name="performance-issue-with-customer-or-contact-mappings"></a>客户或联系人映射发生性能问题

您可能可以通过自定义（**CustCustomerV3Entity** 实体中的）**getEntityDataSourceToFieldMapping** 方法和（**smmContactPersonCDSV2Entity** 实体中的）**getEntityDataSourceToFieldMapping** 方法，稍微提高客户和联系人的实时同步性能。 这些自定义项会减少 **BusinessEventsDefinition** 表中的记录数量。 同样，记录数量的减少会导致引发的事件的数量减少。

**CustCustomerV3Entity** 实体中的 **getEntityDataSourceToFieldMapping** 方法可以确保客户的电子地址或邮寄地址更新会触发业务事件，从而将更新后的数据发送到 Dataverse 中。 如果不使用所有字段，并且双重写入中不需要信息，请注释掉方法中的相应行。 此方法中添加的每个跟踪字段和表都将在 **BusinessEventsDefinition** 表中为跟踪表和跟踪实体的组合创建一条记录。

```xpp
public static container getEntityDataSourceToFieldMapping(container mapping)
{
    mapping += [
        [tablestr(DirPartyBaseEntity), tablenum(LogisticsPostalAddress), fieldstr(CustCustomerV3Entity, AddressRecordId)],
        [identifierstr(DirPartyBaseEntity), tablenum(LogisticsElectronicAddress), fieldstr(CustCustomerV3Entity, PrimaryContactURLRecordId)],
        [identifierstr(DirPartyBaseEntity1), tablenum(LogisticsElectronicAddress), fieldstr(CustCustomerV3Entity, PrimaryContactPhoneRecordId)],
        [identifierstr(DirPartyBaseEntity2), tablenum(LogisticsElectronicAddress), fieldstr(CustCustomerV3Entity, PrimaryContactEmailRecordId)],
        [identifierstr(DirPartyBaseEntity3), tablenum(LogisticsElectronicAddress), fieldstr(CustCustomerV3Entity, PrimaryContactFaxRecordId)],
        [identifierstr(DirPartyBaseEntity4), tablenum(DirPartyLocation), fieldstr(CustCustomerV3Entity, DirPartyLocationRecordId)],
        [identifierstr(DirPartyBaseEntity5), tablenum(LogisticsPostalAddress), fieldstr(CustCustomerV3Entity, InvoiceAddressRecordId)],
        [identifierstr(DirPartyBaseEntity6), tablenum(LogisticsPostalAddress), fieldstr(CustCustomerV3Entity, DeliveryAddressRecordId)],
        [identifierStr(DirPartyBaseEntity7), tablenum(DirPartyTable), fieldstr(CustCustomerV3Entity, PartyRecordId)]];
    return mapping;
}
```

同样，**smmContactPersonCDSV2Entity** 实体中的 **getEntityDataSourceToFieldMapping** 方法可以确保对更新联系人的电子地址或邮寄地址的任何更新都将触发业务事件，从而将更新后的数据发送到 Dataverse 中。 在此方法中，您可以注释掉不使用的任何字段的行。

```xpp
public static container getEntityDataSourceToFieldMapping(container mapping)
{
    mapping += [
        [tablestr(DirPartyBaseEntity), tablenum(LogisticsPostalAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryPostalAddressRecId)],
        [identifierStr(DirPartyBaseEntity), tablenum(DirPartyTable), fieldstr(smmContactPersonCDSV2Entity, PrimaryAddressLocation)],
        [identifierStr(DirPartyBaseEntity1), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactEmailRecordId)],
        [identifierStr(DirPartyBaseEntity2), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactFaxRecordId)],
        [identifierStr(DirPartyBaseEntity3), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactPhoneRecordId)],
        [identifierStr(DirPartyBaseEntity4), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactFacebookRecordId)],
        [identifierStr(DirPartyBaseEntity5), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactTwitterRecordId)],
        [identifierStr(DirPartyBaseEntity6), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactURLRecordId)],
        [identifierStr(DirPartyBaseEntity7), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactLinkedInRecordId)],
        [identifierStr(DirPartyBaseEntity8), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactTelexRecordId)],
        [identifierStr(DirPartyBaseEntity9), tablenum(DirPartyTable), fieldstr(smmContactPersonCDSV2Entity, PartyRecordId)]];
    return mapping;
}
```

更新方法后，请执行以下步骤。

1. 同步数据库，然后生成应用程序。
2. 停止 **smmContactPersonCDSV2Entity** 和 **CustCustomerV3Entity** 实体上的所有双重写入映射。
3. 启动映射。 您应该会发现 **smmContactPersonCDSV2Entity** 与 **CustCustomerV3Entity** 实体和 **BusinessEventsDefinition** 表中的记录减少，并且性能可能稍微提升。

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

