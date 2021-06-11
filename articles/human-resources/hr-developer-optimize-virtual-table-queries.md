---
title: 优化 Dataverse 虚拟表查询
description: 优化和解决 Dataverse 虚拟表查询的性能
author: andreabichsel
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-04-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 66fb9f2b50079b5eb4eb16da17b8a473d687d354
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054900"
---
# <a name="optimize-dataverse-virtual-table-queries"></a><span data-ttu-id="9aac1-103">优化 Dataverse 虚拟表查询</span><span class="sxs-lookup"><span data-stu-id="9aac1-103">Optimize Dataverse virtual table queries</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="issue"></a><span data-ttu-id="9aac1-104">签发</span><span class="sxs-lookup"><span data-stu-id="9aac1-104">Issue</span></span>

### <a name="overview"></a><span data-ttu-id="9aac1-105">概览</span><span class="sxs-lookup"><span data-stu-id="9aac1-105">Overview</span></span>

<span data-ttu-id="9aac1-106">当使用 Dataverse 虚拟表开发集成和与 Dynamics 365 Human Resources 的其他数据连接时，您可能会遇到针对虚拟表的查询的性能问题。</span><span class="sxs-lookup"><span data-stu-id="9aac1-106">When using Dataverse virtual tables to develop integrations and other data connections with Dynamics 365 Human Resources, you can experience performance issues with queries against the virtual tables.</span></span> <span data-ttu-id="9aac1-107">在各种客户端或接口上，可能会发生查询执行缓慢问题。</span><span class="sxs-lookup"><span data-stu-id="9aac1-107">The slow query execution can occur across various clients or interfaces.</span></span> <span data-ttu-id="9aac1-108">例如，在以下情况下，您可能会遇到此问题：</span><span class="sxs-lookup"><span data-stu-id="9aac1-108">For example, you may experience the issue in the following circumstances:</span></span>

- <span data-ttu-id="9aac1-109">当通过 Dataverse Web API 查询虚拟表时</span><span class="sxs-lookup"><span data-stu-id="9aac1-109">When querying a virtual table through the Dataverse Web API</span></span>
- <span data-ttu-id="9aac1-110">当针对虚拟表创建 Power App 时</span><span class="sxs-lookup"><span data-stu-id="9aac1-110">When creating a Power App against a virtual table</span></span>
- <span data-ttu-id="9aac1-111">当在虚拟表上生成 Power BI 报表时</span><span class="sxs-lookup"><span data-stu-id="9aac1-111">When building a Power BI report on a virtual table</span></span>

<span data-ttu-id="9aac1-112">所有这些接口都可能出现性能问题。</span><span class="sxs-lookup"><span data-stu-id="9aac1-112">All these interfaces have the potential to surface the performance issue.</span></span>

<span data-ttu-id="9aac1-113">导致 Human Resources 的 Dataverse 虚拟表性能下降的原因之一是与表的[导航属性](/powerapps/developer/data-platform/webapi/web-api-types-operations#navigation-properties)相关的虚拟表的外键列。</span><span class="sxs-lookup"><span data-stu-id="9aac1-113">One cause of slow performance with Dataverse virtual tables for Human Resources is the foreign key columns of the virtual table related to the table's [navigation properties](/powerapps/developer/data-platform/webapi/web-api-types-operations#navigation-properties).</span></span> <span data-ttu-id="9aac1-114">当为虚拟表创建导航属性时，外键列会自动添加到表，以表示相关虚拟表的键列的键值。</span><span class="sxs-lookup"><span data-stu-id="9aac1-114">When navigation properties are created for a virtual table, a foreign key column is automatically added to the table to represent the value of the key for the related virtual table's key column.</span></span> <span data-ttu-id="9aac1-115">例如，**_mshr_fk_person_id_value** 列将从 **mshr_dirpersonentity** 实体添加到具有外键属性的 **mshr_hcmworkerbaseentity** 实体。</span><span class="sxs-lookup"><span data-stu-id="9aac1-115">For example, the **_mshr_fk_person_id_value** column is added to the **mshr_hcmworkerbaseentity** entity with the foreign key property from the **mshr_dirpersonentity** entity.</span></span> <span data-ttu-id="9aac1-116">由于这些外键列的值在表中的维护方式，提取值可能会对针对虚拟表的查询的性能产生负面影响。</span><span class="sxs-lookup"><span data-stu-id="9aac1-116">Because of how the values for these foreign key columns are maintained in a table, fetching the values can have a negative impact on the performance of a query against the virtual table.</span></span>

### <a name="potential-symptoms"></a><span data-ttu-id="9aac1-117">潜在症状</span><span class="sxs-lookup"><span data-stu-id="9aac1-117">Potential symptoms</span></span>

<span data-ttu-id="9aac1-118">在以下示例中您可能会看到此影响：针对工作人员 (**mshr_hcmworkerentity**) 或基本工作人员 (**mshr_hcmworkerbaseentity**) 实体的查询。</span><span class="sxs-lookup"><span data-stu-id="9aac1-118">An example where you may see this impact is in queries against the Worker (**mshr_hcmworkerentity**) or Base worker (**mshr_hcmworkerbaseentity**) entity.</span></span> <span data-ttu-id="9aac1-119">您可能会看到性能问题以几种不同的方式呈现：</span><span class="sxs-lookup"><span data-stu-id="9aac1-119">You may see the performance issue manifest itself in a few different ways:</span></span>

- <span data-ttu-id="9aac1-120">**查询执行缓慢**：针对虚拟表的查询可能会返回预期的结果，但完成查询执行的时间比预期要长。</span><span class="sxs-lookup"><span data-stu-id="9aac1-120">**Slow query execution**: The query against the virtual table may return the expected results, but take longer than expected to complete execution of the query.</span></span>
- <span data-ttu-id="9aac1-121">**查询超时**：查询可能会超时并返回以下错误：“已获取令牌以调用 Finance and Operations，但 Finance and Operations 返回了类型 InternalServerError 的错误。”</span><span class="sxs-lookup"><span data-stu-id="9aac1-121">**Query timeout**: The query may time out and return the following error: "A token was obtained to call Finance and Operations, but Finance and Operations returned an error of type InternalServerError."</span></span>
- <span data-ttu-id="9aac1-122">**意外错误**：查询可能返回错误类型 400，并具有以下消息：“发生意外错误。”</span><span class="sxs-lookup"><span data-stu-id="9aac1-122">**Unexpected error**: The query may return an error type 400 with the following message: "An unexpected error occurred."</span></span>

  ![HcmWorkerBaseEntity 上的错误类型 400](./media/HcmWorkerBaseEntityErrorType400.png)

- <span data-ttu-id="9aac1-124">**限制**：查询可能会过度使用服务器资源，并可能受到限制。</span><span class="sxs-lookup"><span data-stu-id="9aac1-124">**Throttling**: The query may overuse server resources, and become subject to throttling.</span></span> <span data-ttu-id="9aac1-125">在这种情况下，查询返回以下错误：“已获取令牌以调用 Finance and Operations，但 Finance and Operations 返回了类型 429 的错误。”</span><span class="sxs-lookup"><span data-stu-id="9aac1-125">In this case, the query returns the following error: "A token was obtained to call Finance and Operations, but Finance and Operations returned an error of type 429."</span></span> <span data-ttu-id="9aac1-126">有关 Human Resources 中的限制的详细信息，请参阅[限制常见问题解答](./hr-admin-integration-throttling-faq.md)。</span><span class="sxs-lookup"><span data-stu-id="9aac1-126">For more information in throttling in Human Resources, see [Throttling FAQ](./hr-admin-integration-throttling-faq.md).</span></span>

  ![HcmWorkerBaseEntity 上的错误类型 429](./media/HcmWorkerBaseEntityErrorType429.png)

## <a name="resolution"></a><span data-ttu-id="9aac1-128">解决方法</span><span class="sxs-lookup"><span data-stu-id="9aac1-128">Resolution</span></span>

### <a name="limit-the-number-of-columns-included-in-your-data-query"></a><span data-ttu-id="9aac1-129">限制数据查询中包含的列数</span><span class="sxs-lookup"><span data-stu-id="9aac1-129">Limit the number of columns included in your data query</span></span>

<span data-ttu-id="9aac1-130">使用虚拟表，最有可能提高查询性能的方法之一是限制查询中选择的列数。</span><span class="sxs-lookup"><span data-stu-id="9aac1-130">With virtual tables, one of the methods with the greatest potential to improve query performance is to limit the number of columns selected in the query.</span></span> <span data-ttu-id="9aac1-131">优化查询性能的一般指导是将查询中返回的列限制为仅所需的属性。</span><span class="sxs-lookup"><span data-stu-id="9aac1-131">The general guidance for optimizing query performance is to limit the columns returned in your query to only those properties that you need.</span></span> <span data-ttu-id="9aac1-132">对于虚拟表上的外键列，尤其如此。</span><span class="sxs-lookup"><span data-stu-id="9aac1-132">This is particularly true with the foreign key columns on virtual tables.</span></span> <span data-ttu-id="9aac1-133">如果您不需要集成或报表的外键列中的值，则可以构造查询以仅选择所需的列，但不包括外键列。</span><span class="sxs-lookup"><span data-stu-id="9aac1-133">If you don't need the values in the foreign key columns for your integration or report, then structure the query to select only the columns you need, excluding the foreign key columns.</span></span>

#### <a name="selecting-columns-in-an-odata-query"></a><span data-ttu-id="9aac1-134">在 OData 查询中选择列</span><span class="sxs-lookup"><span data-stu-id="9aac1-134">Selecting columns in an OData query</span></span>

<span data-ttu-id="9aac1-135">当通过 Dataverse Web API 查询虚拟表时，您可以使用 **$select** 系统查询选项限制查询中包括的列数，并定义需要为其返回结果的列。</span><span class="sxs-lookup"><span data-stu-id="9aac1-135">When querying a virtual table through the Dataverse Web API, you can limit the number of columns included in the query by using the **$select** system query option, and define the columns for which you need results returned.</span></span> <span data-ttu-id="9aac1-136">为了最大限度地提高性能，请从查询中排除外键列（带有 **_mshr_FK_** 前缀的列）。</span><span class="sxs-lookup"><span data-stu-id="9aac1-136">To maximize performance, exclude foreign key columns (those with the **_mshr_FK_** prefix) from the query.</span></span>

<span data-ttu-id="9aac1-137">例如，针对 **mshr_hcmworkerbaseentity** 实体的以下查询将仅包括包含在 **$select** 查询选项子句中的列，不包括外键值。</span><span class="sxs-lookup"><span data-stu-id="9aac1-137">For example, the following query against the **mshr_hcmworkerbaseentity** entity will include only the columns included in the **$select** query option clause, excluding foreign key values.</span></span> <span data-ttu-id="9aac1-138">与包含所有表列的查询相比，这可以显着提高性能。</span><span class="sxs-lookup"><span data-stu-id="9aac1-138">This provides significant improvements in performance over a query that includes all table columns.</span></span>

```http
GET [Organization URI]/api/data/v9.1/mshr_hcmworkerbaseentities?$select=mshr_name, mshr_firstname, mshr_gender, mshr_partynumber, mshr_phoneticfirstname, mshr_deceaseddate, mshr_nationalitycountryregion, mshr_allowrehire, mshr_electroniclocationid, mshr_middlename, mshr_knownas, mshr_professionaltitle, mshr_nativelanguageid, mshr_disabledverificationdate, mshr_personalsuffix, mshr_lastnameprefix, mshr_personbirthcity, mshr_personaltitle, mshr_phoneticlastname, mshr_namesequencedisplayas, mshr_personbirthcountryregion, mshr_isdisabled, mshr_birthdate, mshr_professionalsuffix, mshr_isfulltimestudent, mshr_education, mshr_namealias, mshr_phoneticmiddlename, mshr_personnelnumber, mshr_hcmworkerbaseentityid, mshr_motherbirthcountryregion, mshr_fatherbirthcountryregion, mshr_lastname, mshr_languageid, mshr_partytype, mshr_ethnicoriginid, mshr_citizenshipcountryregion HTTP/1.1
Accept: application/json
OData-MaxVersion: 4.0
OData-Version: 4.0
```

<span data-ttu-id="9aac1-139">当使用 **$expand** 查询选项通过导航属性将查询扩展到相关的虚拟表时，也应用限制所选列数的建议。</span><span class="sxs-lookup"><span data-stu-id="9aac1-139">The recommendation to limit the number of columns selected also applies when using the **$expand** query option to expand the query to related virtual tables through navigation properties.</span></span> <span data-ttu-id="9aac1-140">例如，以下查询包含 **mshr_hcmworkerbaseentity** 实体中的列以及 **mshr_dirpersonentity** 实体中的扩展列。</span><span class="sxs-lookup"><span data-stu-id="9aac1-140">For example, the following query includes columns from the **mshr_hcmworkerbaseentity** entity with expanded columns from the **mshr_dirpersonentity** entity.</span></span> <span data-ttu-id="9aac1-141">请注意，**$select** 查询选项也包括在 **$expand** 查询选项子句中。</span><span class="sxs-lookup"><span data-stu-id="9aac1-141">Note that the **$select** query option is also included in the **$expand** query option clause.</span></span>

```http
GET [Organization URI]/api/data/v9.1/mshr_hcmworkerbaseentities?$select=mshr_name, mshr_firstname, mshr_gender, mshr_partynumber, mshr_phoneticfirstname, mshr_deceaseddate, mshr_nationalitycountryregion, mshr_allowrehire, mshr_electroniclocationid, mshr_middlename, mshr_knownas&$expand=mshr_FK_Person_id($select=mshr_addressstreet, mshr_addresscity, mshr_addressstate, mshr_addresszipcode) HTTP/1.1
Accept: application/json
OData-MaxVersion: 4.0
OData-Version: 4.0
```

<span data-ttu-id="9aac1-142">当使用通过 **$expand** 查询选项子句中的 **$select** 查询选项检索数据的此方法时，您通常会看到在实体之间的导航属性是多对一关系时，将显著提高性能。</span><span class="sxs-lookup"><span data-stu-id="9aac1-142">When using this method of retrieving data with the **$select** query option in the **$expand** query option clause, you will typically see greater performance improvements when the navigation property between the entities is a many-to-one relationship.</span></span> <span data-ttu-id="9aac1-143">当展开一对多关系时，您可能看不到查询执行时间的减少。</span><span class="sxs-lookup"><span data-stu-id="9aac1-143">You may not see the same decrease in query execution time when expanding a one-to-many relationship.</span></span> <span data-ttu-id="9aac1-144">有关 Dataverse 虚拟表的关系定义的详细信息，请参阅[表关系](/powerapps/maker/data-platform/create-edit-entity-relationships)。</span><span class="sxs-lookup"><span data-stu-id="9aac1-144">For more information on relationship definition for Dataverse virtual tables, see [Table relationships](/powerapps/maker/data-platform/create-edit-entity-relationships).</span></span>

<span data-ttu-id="9aac1-145">有关使用 Dataverse Web API 中的 **$select** 和 **$expand** 系统查询选项的详细信息，请参阅[使用查询检索相关实体记录](/powerapps/developer/data-platform/webapi/retrieve-related-entities-query)。</span><span class="sxs-lookup"><span data-stu-id="9aac1-145">For more information on using the **$select** and **$expand** system query options in the Dataverse Web API, see [Retrieve related entity records with a query](/powerapps/developer/data-platform/webapi/retrieve-related-entities-query).</span></span>

#### <a name="selecting-columns-in-power-bi"></a><span data-ttu-id="9aac1-146">在 Power BI 中选择列</span><span class="sxs-lookup"><span data-stu-id="9aac1-146">Selecting columns in Power BI</span></span>

<span data-ttu-id="9aac1-147">当针对 Dataverse 虚拟表生成 Power BI 报表时，如果遇到前面提到的任何性能下降问题，您可以通过从在报表的表中选择的列中排除外键列来提高性能。</span><span class="sxs-lookup"><span data-stu-id="9aac1-147">If you experience any of the aforementioned indications of slow performance when building a Power BI report against a Dataverse virtual table, you can improve the performance by excluding foreign key columns from the columns selected from the table for the report.</span></span> <span data-ttu-id="9aac1-148">例如，如果如果您使用 Power BI Desktop 针对 **mshr_hcmworkerbaseentity** 实体创建报表，可以使用以下步骤选择要包括在报表查询中的列。</span><span class="sxs-lookup"><span data-stu-id="9aac1-148">For example, if you are using Power BI Desktop to create a report against the **mshr_hcmworkerbaseentity** entity, you can use the following steps to select the columns you want included in the report query.</span></span>

1. <span data-ttu-id="9aac1-149">在 Power BI Desktop 中，在操作功能区上，从 **获取数据** 下拉列表中选择 **更多...**。</span><span class="sxs-lookup"><span data-stu-id="9aac1-149">In Power BI Desktop, select **More...** from the **Get data** drop-down list on the action ribbon.</span></span>
2. <span data-ttu-id="9aac1-150">在 **获取数据** 窗口中，在搜索框中输入 **Common Data Service**，选择 **Common Data Service** 连接器，然后选择 **连接**。</span><span class="sxs-lookup"><span data-stu-id="9aac1-150">In the **Get Data** window, enter **Common Data Service** in the search box, select the **Common Data Service** connector, and select **Connect**.</span></span>
3. <span data-ttu-id="9aac1-151">在 Common Data Service 窗口的 **服务器 URL** 字段中，输入您的 Dataverse 环境的组织 URI，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="9aac1-151">In the **Server Url** field of the Common Data Service window, enter the organization URI for your Dataverse environment, and select **OK**.</span></span>
  
   ![输入您的 Dataverse 环境的 URI](./media/PowerBIDataverseURLSetup.png)
  
4. <span data-ttu-id="9aac1-153">在“导航器”窗口中，展开 **实体** 节点。</span><span class="sxs-lookup"><span data-stu-id="9aac1-153">In the Navigator window, expand the **Entities** node.</span></span>
5. <span data-ttu-id="9aac1-154">在搜索框中，输入 **mshr_hcmworkerbaseentity**，然后选择实体。</span><span class="sxs-lookup"><span data-stu-id="9aac1-154">In the search box, enter **mshr_hcmworkerbaseentity**, and select the entity.</span></span>
6. <span data-ttu-id="9aac1-155">选择 **转换数据**。</span><span class="sxs-lookup"><span data-stu-id="9aac1-155">Select **Transform Data**.</span></span>
7. <span data-ttu-id="9aac1-156">在“Power Query 编辑器”窗口中，选择 **高级编辑器**。</span><span class="sxs-lookup"><span data-stu-id="9aac1-156">In the Power Query Editor window, select **Advanced Editor**.</span></span>
8. <span data-ttu-id="9aac1-157">在 **高级编辑器** 窗口中，更新查询以使其如下所示，根据需要在数组中添加或删除任何列。</span><span class="sxs-lookup"><span data-stu-id="9aac1-157">In the **Advanced Editor** window, update the query to look like the below, adding or removing any columns to the array as needed.</span></span>

   ```
   let
     Source = Cds.Entities("[Your Organization URI]", [ReorderColumns=null, UseFormattedValue=null]),
     entities = Source{[Group="entities"]}[Data],
     mshr_hcmworkerbaseentities = entities{[EntitySetName="mshr_hcmworkerbaseentities"]}[Data],
     selectedWorkerBaseEntityColumns=Table.SelectColumns(mshr_hcmworkerbaseentities,{"mshr_name","mshr_partynumber", "mshr_professionaltitle","mshr_birthdate"})
   in
     selectedWorkerBaseEntityColumns
   ```
   ![在 Power Query 编辑器的高级编辑器中更新查询](./media/HcmWorkerBaseEntityPowerQueryEditor.png)

9. <span data-ttu-id="9aac1-159">选择 **完成**。</span><span class="sxs-lookup"><span data-stu-id="9aac1-159">Select **Done**.</span></span>

   > [!NOTE]
   > <span data-ttu-id="9aac1-160">如果您之前在更新之前收到了来自查询的类型 429 的错误，则可能需要等待重试期间才能刷新查询，以使其成功完成。</span><span class="sxs-lookup"><span data-stu-id="9aac1-160">If you previously received an error of type 429 from the query prior to updating, you may need to wait for the retry period prior to refreshing the query for it to complete successully.</span></span>

10. <span data-ttu-id="9aac1-161">在 Power Query 编辑器操作功能区上单击 **关闭并应用**。</span><span class="sxs-lookup"><span data-stu-id="9aac1-161">Click **Close & Apply** on the Power Query Editor action ribbon.</span></span>

<span data-ttu-id="9aac1-162">然后，您可以开始针对从虚拟表中选择的列生成 Power BI 报表。</span><span class="sxs-lookup"><span data-stu-id="9aac1-162">You're then able to begin building your Power BI report against the columns selected from the virtual table.</span></span>

#### <a name="selecting-columns-in-power-apps"></a><span data-ttu-id="9aac1-163">在 Power Apps 中选择列</span><span class="sxs-lookup"><span data-stu-id="9aac1-163">Selecting columns in Power Apps</span></span>

<span data-ttu-id="9aac1-164">类似于 Dataverse Web API 查询和 Power BI，您可以通过从应用中排除相关表的列来基于 Dataverse 虚拟表提高 Power Apps 的查询性能。</span><span class="sxs-lookup"><span data-stu-id="9aac1-164">Similar to Dataverse Web API queries and Power BI, you can improve query performance for Power Apps based on Dataverse virtual tables by excluding columns of related tables from your app.</span></span> <span data-ttu-id="9aac1-165">如果页面上已包含相关表中的任何列，则构造用于获取数据的请求 URL 将包含相关表的外键属性。</span><span class="sxs-lookup"><span data-stu-id="9aac1-165">If any columns from a related table have been included on a page, then the request URL constructed to fetch the data will include foreign key properties of the related table.</span></span> <span data-ttu-id="9aac1-166">如[在 OData 查询中选择列](#selecting-columns-in-power-apps)的示例所示，这将导致额外的数据查找，从而降低性能。</span><span class="sxs-lookup"><span data-stu-id="9aac1-166">This, as in the examples of [Selecting columns in an OData Query](#selecting-columns-in-power-apps) above, reduces performance by causing additional data lookups.</span></span>

<span data-ttu-id="9aac1-167">若要解决此问题，您可以验证 Power App 的任何数据形式上没有包含相关表中的数据字段。</span><span class="sxs-lookup"><span data-stu-id="9aac1-167">To work around this, you can validate that no data fields from related tables have been included on any data form of your Power App.</span></span>

1. <span data-ttu-id="9aac1-168">在树视图窗格中，选择屏幕的数据窗体。</span><span class="sxs-lookup"><span data-stu-id="9aac1-168">In the Tree view pane, select the data form for the screen.</span></span>
2. <span data-ttu-id="9aac1-169">在 **属性** 窗格中，在 **字段** 属性上选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="9aac1-169">In the **Properties** pane, select **Edit** on the **Fields** property.</span></span>
3. <span data-ttu-id="9aac1-170">在 **数据** 窗格中，验证所有选定字段都不是数据源的虚拟表的字段。</span><span class="sxs-lookup"><span data-stu-id="9aac1-170">In the **Data** pane, verify that none of the selected fields are fields of the virtual table of the data source.</span></span>

<span data-ttu-id="9aac1-171">例如，如果应用中页面上包括的一个数据字段引用另一个表，例如 **ThisItem.Worker.Name**，其中 **工作人员** 是相关表，则在提取数据时可能会降低性能。</span><span class="sxs-lookup"><span data-stu-id="9aac1-171">For example, if one of the data fields included on a page in the app references another table, such as **ThisItem.Worker.Name**, where **Worker** is the related table, there is a potential for reduced performance in fetching the data.</span></span>

<span data-ttu-id="9aac1-172">您可以使用 [Power Apps 监视器](/powerapps/maker/monitor-overview)以确保查询中仅包含所需的列以获取 Power App 的数据。</span><span class="sxs-lookup"><span data-stu-id="9aac1-172">You can use the [Power Apps Monitor](/powerapps/maker/monitor-overview) to ensure that only the columns you need are being included in the query to get the data for the Power App.</span></span> <span data-ttu-id="9aac1-173">您可以查看为 getRows 操作构造的 URL，以确保为应用选择的列最适用于检索数据。</span><span class="sxs-lookup"><span data-stu-id="9aac1-173">You can view the URL constructed for the getRows operation to ensure the columns you have selected for your app will be optimal for retrieving the data.</span></span>

![使用 Power Apps 监视器以分析 getData 操作](./media/HcmWorkerBaseEntityPowerAppsMonitor.png)

### <a name="filtering-the-data-query"></a><span data-ttu-id="9aac1-175">筛选数据查询</span><span class="sxs-lookup"><span data-stu-id="9aac1-175">Filtering the data query</span></span>

<span data-ttu-id="9aac1-176">提高查询执行性能的另一种方法是限制在查询结果中返回的记录数。</span><span class="sxs-lookup"><span data-stu-id="9aac1-176">Another method for improving query execution performance is to limit the number of records returned in the query results.</span></span> <span data-ttu-id="9aac1-177">您可以通过筛选结果执行此操作，以确保仅接收所需的记录。</span><span class="sxs-lookup"><span data-stu-id="9aac1-177">You can do this by filtering the results to ensure that you are only receiving the records you need.</span></span>

<span data-ttu-id="9aac1-178">有关筛选查询数据的详细信息，请参阅[筛选结果](/powerapps/developer/data-platform/webapi/query-data-web-api#filter-results)。</span><span class="sxs-lookup"><span data-stu-id="9aac1-178">See [Filter results](/powerapps/developer/data-platform/webapi/query-data-web-api#filter-results) for more information on filtering query data.</span></span>

### <a name="limiting-the-page-size-of-the-query"></a><span data-ttu-id="9aac1-179">限制查询的页面大小</span><span class="sxs-lookup"><span data-stu-id="9aac1-179">Limiting the page size of the query</span></span>

<span data-ttu-id="9aac1-180">如果要使用较大的数据集，您可以通过将 `odata.maxpagesize` 首选项标头添加到数据查询，将查询结果分为多个页面。</span><span class="sxs-lookup"><span data-stu-id="9aac1-180">If you're working with large data sets, you can divide query results into multiple pages by adding the `odata.maxpagesize` preference header to data queries.</span></span>

<span data-ttu-id="9aac1-181">有关分页的详细信息，请参阅[指定要在页面中返回的实体数](/powerapps/developer/data-platform/webapi/query-data-web-api#specify-the-number-of-entities-to-return-in-a-page)。</span><span class="sxs-lookup"><span data-stu-id="9aac1-181">For more information on paging, see [Specify the number of entities to return in a page](/powerapps/developer/data-platform/webapi/query-data-web-api#specify-the-number-of-entities-to-return-in-a-page).</span></span>

## <a name="see-also"></a><span data-ttu-id="9aac1-182">请参阅</span><span class="sxs-lookup"><span data-stu-id="9aac1-182">See also</span></span>

- [<span data-ttu-id="9aac1-183">配置 Dataverse 虚拟表</span><span class="sxs-lookup"><span data-stu-id="9aac1-183">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)
- [<span data-ttu-id="9aac1-184">Human Resources 虚拟表常见问题</span><span class="sxs-lookup"><span data-stu-id="9aac1-184">Human Resources virtual tables FAQ</span></span>](hr-admin-virtual-entity-faq.md)
- [<span data-ttu-id="9aac1-185">限制常见问题</span><span class="sxs-lookup"><span data-stu-id="9aac1-185">Throttling FAQ</span></span>](./hr-admin-integration-throttling-faq.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]