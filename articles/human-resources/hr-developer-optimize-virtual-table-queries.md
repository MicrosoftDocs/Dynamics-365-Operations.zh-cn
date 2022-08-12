---
title: 优化 Dataverse 虚拟表查询
description: 优化和解决 Dataverse 虚拟表查询的性能
author: twheeloc
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-04-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1f379cd7783cc984666582d2c680a1db013627ce
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/29/2022
ms.locfileid: "9070163"
---
# <a name="optimize-dataverse-virtual-table-queries"></a>优化 Dataverse 虚拟表查询


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



## <a name="issue"></a>签发

### <a name="overview"></a>概览

当使用 Dataverse 虚拟表开发集成和与 Dynamics 365 Human Resources 的其他数据连接时，您可能会遇到针对虚拟表的查询的性能问题。 在各种客户端或接口上，可能会发生查询执行缓慢问题。 例如，在以下情况下，您可能会遇到此问题：

- 当通过 Dataverse Web API 查询虚拟表时
- 当针对虚拟表创建 Power App 时
- 当在虚拟表上生成 Power BI 报表时

所有这些接口都可能出现性能问题。

导致 Human Resources 的 Dataverse 虚拟表性能下降的原因之一是与表的[导航属性](/powerapps/developer/data-platform/webapi/web-api-types-operations#navigation-properties)相关的虚拟表的外键列。 当为虚拟表创建导航属性时，外键列会自动添加到表，以表示相关虚拟表的键列的键值。 例如，**_mshr_fk_person_id_value** 列将从 **mshr_dirpersonentity** 实体添加到具有外键属性的 **mshr_hcmworkerbaseentity** 实体。 由于这些外键列的值在表中的维护方式，提取值可能会对针对虚拟表的查询的性能产生负面影响。

### <a name="potential-symptoms"></a>潜在症状

在以下示例中您可能会看到此影响：针对工作人员 (**mshr_hcmworkerentity**) 或基本工作人员 (**mshr_hcmworkerbaseentity**) 实体的查询。 您可能会看到性能问题以几种不同的方式呈现：

- **查询执行缓慢**：针对虚拟表的查询可能会返回预期的结果，但完成查询执行的时间比预期要长。
- **查询超时**：查询可能会超时并返回以下错误：“已获取令牌以调用财务和运营，但财务和运营返回了类型 InternalServerError 的错误。”
- **意外错误**：查询可能返回错误类型 400，并具有以下消息：“发生意外错误。”

  ![HcmWorkerBaseEntity 上的错误类型 400。](./media/HcmWorkerBaseEntityErrorType400.png)

- **限制**：查询可能会过度使用服务器资源，并可能受到限制。 在这种情况下，查询返回以下错误：“已获取令牌以调用财务和运营，但财务和运营返回了类型 429 的错误。” 有关 Human Resources 中的限制的详细信息，请参阅[限制常见问题解答](./hr-admin-integration-throttling-faq.md)。

  ![HcmWorkerBaseEntity 上的错误类型 429。](./media/HcmWorkerBaseEntityErrorType429.png)

## <a name="resolution"></a>解决方法

### <a name="limit-the-number-of-columns-included-in-your-data-query"></a>限制数据查询中包含的列数

使用虚拟表，最有可能提高查询性能的方法之一是限制查询中选择的列数。 优化查询性能的一般指导是将查询中返回的列限制为仅所需的属性。 对于虚拟表上的外键列，尤其如此。 如果您不需要集成或报表的外键列中的值，则可以构造查询以仅选择所需的列，但不包括外键列。

#### <a name="selecting-columns-in-an-odata-query"></a>在 OData 查询中选择列

当通过 Dataverse Web API 查询虚拟表时，您可以使用 **$select** 系统查询选项限制查询中包括的列数，并定义需要为其返回结果的列。 为了最大限度地提高性能，请从查询中排除外键列（带有 **_mshr_FK_** 前缀的列）。

例如，针对 **mshr_hcmworkerbaseentity** 实体的以下查询将仅包括包含在 **$select** 查询选项子句中的列，不包括外键值。 与包含所有表列的查询相比，这可以显着提高性能。

```http
GET [Organization URI]/api/data/v9.1/mshr_hcmworkerbaseentities?$select=mshr_name, mshr_firstname, mshr_gender, mshr_partynumber, mshr_phoneticfirstname, mshr_deceaseddate, mshr_nationalitycountryregion, mshr_allowrehire, mshr_electroniclocationid, mshr_middlename, mshr_knownas, mshr_professionaltitle, mshr_nativelanguageid, mshr_disabledverificationdate, mshr_personalsuffix, mshr_lastnameprefix, mshr_personbirthcity, mshr_personaltitle, mshr_phoneticlastname, mshr_namesequencedisplayas, mshr_personbirthcountryregion, mshr_isdisabled, mshr_birthdate, mshr_professionalsuffix, mshr_isfulltimestudent, mshr_education, mshr_namealias, mshr_phoneticmiddlename, mshr_personnelnumber, mshr_hcmworkerbaseentityid, mshr_motherbirthcountryregion, mshr_fatherbirthcountryregion, mshr_lastname, mshr_languageid, mshr_partytype, mshr_ethnicoriginid, mshr_citizenshipcountryregion HTTP/1.1
Accept: application/json
OData-MaxVersion: 4.0
OData-Version: 4.0
```

当使用 **$expand** 查询选项通过导航属性将查询扩展到相关的虚拟表时，也应用限制所选列数的建议。 例如，以下查询包含 **mshr_hcmworkerbaseentity** 实体中的列以及 **mshr_dirpersonentity** 实体中的扩展列。 请注意，**$select** 查询选项也包括在 **$expand** 查询选项子句中。

```http
GET [Organization URI]/api/data/v9.1/mshr_hcmworkerbaseentities?$select=mshr_name, mshr_firstname, mshr_gender, mshr_partynumber, mshr_phoneticfirstname, mshr_deceaseddate, mshr_nationalitycountryregion, mshr_allowrehire, mshr_electroniclocationid, mshr_middlename, mshr_knownas&$expand=mshr_FK_Person_id($select=mshr_addressstreet, mshr_addresscity, mshr_addressstate, mshr_addresszipcode) HTTP/1.1
Accept: application/json
OData-MaxVersion: 4.0
OData-Version: 4.0
```

当使用通过 **$expand** 查询选项子句中的 **$select** 查询选项检索数据的此方法时，您通常会看到在实体之间的导航属性是多对一关系时，将显著提高性能。 当展开一对多关系时，您可能看不到查询执行时间的减少。 有关 Dataverse 虚拟表的关系定义的详细信息，请参阅[表关系](/powerapps/maker/data-platform/create-edit-entity-relationships)。

有关使用 Dataverse Web API 中的 **$select** 和 **$expand** 系统查询选项的详细信息，请参阅[使用查询检索相关实体记录](/powerapps/developer/data-platform/webapi/retrieve-related-entities-query)。

#### <a name="selecting-columns-in-power-bi"></a>在 Power BI 中选择列

当针对 Dataverse 虚拟表生成 Power BI 报表时，如果遇到前面提到的任何性能下降问题，您可以通过从在报表的表中选择的列中排除外键列来提高性能。 例如，如果如果您使用 Power BI Desktop 针对 **mshr_hcmworkerbaseentity** 实体创建报表，可以使用以下步骤选择要包括在报表查询中的列。

1. 在 Power BI Desktop 中，在操作功能区上，从 **获取数据** 下拉列表中选择 **更多...**。
2. 在 **获取数据** 窗口中，在搜索框中输入 **Common Data Service**，选择 **Common Data Service** 连接器，然后选择 **连接**。
3. 在 Common Data Service 窗口的 **服务器 URL** 字段中，输入您的 Dataverse 环境的组织 URI，然后选择 **确定**。
  
   ![输入您的 Dataverse 环境的 URI。](./media/PowerBIDataverseURLSetup.png)
  
4. 在“导航器”窗口中，展开 **实体** 节点。
5. 在搜索框中，输入 **mshr_hcmworkerbaseentity**，然后选择实体。
6. 选择 **转换数据**。
7. 在“Power Query 编辑器”窗口中，选择 **高级编辑器**。
8. 在 **高级编辑器** 窗口中，更新查询以使其如下所示，根据需要在数组中添加或删除任何列。

   ```
   let
     Source = Cds.Entities("[Your Organization URI]", [ReorderColumns=null, UseFormattedValue=null]),
     entities = Source{[Group="entities"]}[Data],
     mshr_hcmworkerbaseentities = entities{[EntitySetName="mshr_hcmworkerbaseentities"]}[Data],
     selectedWorkerBaseEntityColumns=Table.SelectColumns(mshr_hcmworkerbaseentities,{"mshr_name","mshr_partynumber", "mshr_professionaltitle","mshr_birthdate"})
   in
     selectedWorkerBaseEntityColumns
   ```
   ![在 Power Query 编辑器的高级编辑器中更新查询。](./media/HcmWorkerBaseEntityPowerQueryEditor.png)

9. 选择 **完成**。

   > [!NOTE]
   > 如果您之前在更新之前收到了来自查询的类型 429 的错误，则可能需要等待重试期间才能刷新查询，以使其成功完成。

10. 在 Power Query 编辑器操作功能区上单击 **关闭并应用**。

然后，您可以开始针对从虚拟表中选择的列生成 Power BI 报表。

#### <a name="selecting-columns-in-power-apps"></a>在 Power Apps 中选择列

类似于 Dataverse Web API 查询和 Power BI，您可以通过从应用中排除相关表的列来基于 Dataverse 虚拟表提高 Power Apps 的查询性能。 如果页面上已包含相关表中的任何列，则构造用于获取数据的请求 URL 将包含相关表的外键属性。 如[在 OData 查询中选择列](#selecting-columns-in-power-apps)的示例所示，这将导致额外的数据查找，从而降低性能。

若要解决此问题，您可以验证 Power App 的任何数据形式上没有包含相关表中的数据字段。

1. 在树视图窗格中，选择屏幕的数据窗体。
2. 在 **属性** 窗格中，在 **字段** 属性上选择 **编辑**。
3. 在 **数据** 窗格中，验证所有选定字段都不是数据源的虚拟表的字段。

例如，如果应用中页面上包括的一个数据字段引用另一个表，例如 **ThisItem.Worker.Name**，其中 **工作人员** 是相关表，则在提取数据时可能会降低性能。

您可以使用 [Power Apps 监视器](/powerapps/maker/monitor-overview)以确保查询中仅包含所需的列以获取 Power App 的数据。 您可以查看为 getRows 操作构造的 URL，以确保为应用选择的列最适用于检索数据。

![使用 Power Apps 监视器以分析 getData 操作。](./media/HcmWorkerBaseEntityPowerAppsMonitor.png)

### <a name="filtering-the-data-query"></a>筛选数据查询

提高查询执行性能的另一种方法是限制在查询结果中返回的记录数。 您可以通过筛选结果执行此操作，以确保仅接收所需的记录。

有关筛选查询数据的详细信息，请参阅[筛选结果](/powerapps/developer/data-platform/webapi/query-data-web-api#filter-results)。

### <a name="limiting-the-page-size-of-the-query"></a>限制查询的页面大小

如果要使用较大的数据集，您可以通过将 `odata.maxpagesize` 首选项标头添加到数据查询，将查询结果分为多个页面。

有关分页的详细信息，请参阅[指定要在页面中返回的实体数](/powerapps/developer/data-platform/webapi/query-data-web-api#specify-the-number-of-entities-to-return-in-a-page)。

## <a name="see-also"></a>请参阅

- [配置 Dataverse 虚拟表](hr-admin-integration-common-data-service-virtual-entities.md)
- [Human Resources 虚拟表常见问题](hr-admin-virtual-entity-faq.md)
- [限制常见问题](./hr-admin-integration-throttling-faq.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

