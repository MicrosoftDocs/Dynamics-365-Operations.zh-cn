---
title: 使用扩展在税务集成中添加数据字段
description: 本主题说明如何使用 X++ 扩展在税务集成中添加数据字段。
author: qire
ms.date: 03/26/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: fdf112bbdd5245d19ab1d07cfcf94c58bf8208c5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830332"
---
# <a name="add-data-fields-in-the-tax-integration-by-using-extension"></a><span data-ttu-id="849db-103">使用扩展在税务集成中添加数据字段</span><span class="sxs-lookup"><span data-stu-id="849db-103">Add data fields in the tax integration by using extension</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="849db-104">本主题说明如何使用 X++ 扩展在税务集成中添加数据字段。</span><span class="sxs-lookup"><span data-stu-id="849db-104">This topic explains how to use X++ extensions to add data fields in the tax integration.</span></span> <span data-ttu-id="849db-105">这些字段可以扩展到税务服务的税务数据模型，并用于确定税码。</span><span class="sxs-lookup"><span data-stu-id="849db-105">These fields can be extended to the tax data model of the tax service and used to determine tax codes.</span></span> <span data-ttu-id="849db-106">有关详细信息，请参阅[在税务配置中添加数据字段](tax-service-add-data-fields-tax-configurations.md)。</span><span class="sxs-lookup"><span data-stu-id="849db-106">For more information, see [Add data fields in tax configurations](tax-service-add-data-fields-tax-configurations.md).</span></span>

## <a name="data-model"></a><span data-ttu-id="849db-107">数据模型</span><span class="sxs-lookup"><span data-stu-id="849db-107">Data model</span></span>

<span data-ttu-id="849db-108">数据模型中的数据由对象承载并由类实现。</span><span class="sxs-lookup"><span data-stu-id="849db-108">The data in the data model is carried by objects and implemented by classes.</span></span>

<span data-ttu-id="849db-109">下面是主要对象的列表：</span><span class="sxs-lookup"><span data-stu-id="849db-109">Here is a list of the major objects:</span></span>

* <span data-ttu-id="849db-110">AxClass/TaxIntegration **Document** Object</span><span class="sxs-lookup"><span data-stu-id="849db-110">AxClass/TaxIntegration **Document** Object</span></span>
* <span data-ttu-id="849db-111">AxClass/TaxIntegration **Line** Object</span><span class="sxs-lookup"><span data-stu-id="849db-111">AxClass/TaxIntegration **Line** Object</span></span>
* <span data-ttu-id="849db-112">AxClass/TaxIntegration **TaxLine** Object</span><span class="sxs-lookup"><span data-stu-id="849db-112">AxClass/TaxIntegration **TaxLine** Object</span></span>

<span data-ttu-id="849db-113">下图显示了这些对象之间的关系。</span><span class="sxs-lookup"><span data-stu-id="849db-113">The following illustration shows how these objects are related.</span></span>

<span data-ttu-id="849db-114">[![数据模型对象关系](./media/tax-service-customize-image1.png)](./media/tax-service-customize-image1.png)</span><span class="sxs-lookup"><span data-stu-id="849db-114">[![Data model object relationship](./media/tax-service-customize-image1.png)](./media/tax-service-customize-image1.png)</span></span>

<span data-ttu-id="849db-115">**单据** 对象可以包含许多 **行** 对象。</span><span class="sxs-lookup"><span data-stu-id="849db-115">A **Document** object can contain many **Line** objects.</span></span> <span data-ttu-id="849db-116">每个对象都包含税务服务的元数据。</span><span class="sxs-lookup"><span data-stu-id="849db-116">Each object contains metadata for the tax service.</span></span>

- <span data-ttu-id="849db-117">`TaxIntegrationDocumentObject` 具有 `originAddress` 元数据（包含有关源地址的信息）和 `includingTax` 元数据（指示行金额是否包含销售税）。</span><span class="sxs-lookup"><span data-stu-id="849db-117">`TaxIntegrationDocumentObject` has `originAddress` metadata, which contains information about the source address, and `includingTax` metadata, which indicates whether the line amount includes sales tax.</span></span>
- <span data-ttu-id="849db-118">`TaxIntegrationLineObject` 具有 `itemId`、`quantity` 和 `categoryId` 元数据。</span><span class="sxs-lookup"><span data-stu-id="849db-118">`TaxIntegrationLineObject` has `itemId`, `quantity`, and `categoryId` metadata.</span></span>

> [!NOTE]
> <span data-ttu-id="849db-119">`TaxIntegrationLineObject` 还实施 **费用** 对象。</span><span class="sxs-lookup"><span data-stu-id="849db-119">`TaxIntegrationLineObject` also implements **Charge** objects.</span></span>

## <a name="integration-flow"></a><span data-ttu-id="849db-120">集成流</span><span class="sxs-lookup"><span data-stu-id="849db-120">Integration flow</span></span>

<span data-ttu-id="849db-121">流中的数据由活动处理。</span><span class="sxs-lookup"><span data-stu-id="849db-121">The data in the flow is manipulated by activities.</span></span>

### <a name="key-activities"></a><span data-ttu-id="849db-122">关键活动</span><span class="sxs-lookup"><span data-stu-id="849db-122">Key activities</span></span>

* <span data-ttu-id="849db-123">AxClass/TaxIntegration **Calculation** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="849db-123">AxClass/TaxIntegration **Calculation** ActivityOnDocument</span></span>
* <span data-ttu-id="849db-124">AxClass/TaxIntegration **CurrencyExchange** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="849db-124">AxClass/TaxIntegration **CurrencyExchange** ActivityOnDocument</span></span>
* <span data-ttu-id="849db-125">AxClass/TaxIntegration **DataPersistence** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="849db-125">AxClass/TaxIntegration **DataPersistence** ActivityOnDocument</span></span>
* <span data-ttu-id="849db-126">AxClass/TaxIntegration **DataRetrieval** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="849db-126">AxClass/TaxIntegration **DataRetrieval** ActivityOnDocument</span></span>
* <span data-ttu-id="849db-127">AxClass/TaxIntegration **SettingRetrieval** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="849db-127">AxClass/TaxIntegration **SettingRetrieval** ActivityOnDocument</span></span>

<span data-ttu-id="849db-128">活动按以下顺序运行：</span><span class="sxs-lookup"><span data-stu-id="849db-128">Activities are run in the following order:</span></span>

1. <span data-ttu-id="849db-129">设置检索</span><span class="sxs-lookup"><span data-stu-id="849db-129">Setting Retrieval</span></span>
2. <span data-ttu-id="849db-130">数据检索</span><span class="sxs-lookup"><span data-stu-id="849db-130">Data Retrieval</span></span>
3. <span data-ttu-id="849db-131">计算服务</span><span class="sxs-lookup"><span data-stu-id="849db-131">Calculation Service</span></span>
4. <span data-ttu-id="849db-132">币种汇兑</span><span class="sxs-lookup"><span data-stu-id="849db-132">Currency Exchange</span></span>
5. <span data-ttu-id="849db-133">数据持久性</span><span class="sxs-lookup"><span data-stu-id="849db-133">Data Persistence</span></span>

<span data-ttu-id="849db-134">例如，在 **计算服务** 之前扩展 **数据检索**。</span><span class="sxs-lookup"><span data-stu-id="849db-134">For example, extend **Data Retrieval** before **Calculation Service**.</span></span>

#### <a name="data-retrieval-activities"></a><span data-ttu-id="849db-135">数据检索活动</span><span class="sxs-lookup"><span data-stu-id="849db-135">Data Retrieval activities</span></span>

<span data-ttu-id="849db-136">**数据检索** 活动从数据库中检索数据。</span><span class="sxs-lookup"><span data-stu-id="849db-136">**Data Retrieval** activities retrieve data from the database.</span></span> <span data-ttu-id="849db-137">不同事务的适配器可用于从不同的事务表中检索数据：</span><span class="sxs-lookup"><span data-stu-id="849db-137">Adapters for different transactions are available to retrieve data from different transaction tables:</span></span>

- <span data-ttu-id="849db-138">AxClass/TaxIntegration **PurchTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="849db-138">AxClass/TaxIntegration **PurchTable** DataRetrieval</span></span>
- <span data-ttu-id="849db-139">AxClass/TaxIntegration **PurchParmTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="849db-139">AxClass/TaxIntegration **PurchParmTable** DataRetrieval</span></span>
- <span data-ttu-id="849db-140">AxClass/TaxIntegration **PurchREQTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="849db-140">AxClass/TaxIntegration **PurchREQTable** DataRetrieval</span></span>
- <span data-ttu-id="849db-141">AxClass/TaxIntegration **PurchRFQTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="849db-141">AxClass/TaxIntegration **PurchRFQTable** DataRetrieval</span></span>
- <span data-ttu-id="849db-142">AxClass/TaxIntegration **VendInvoiceInfoTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="849db-142">AxClass/TaxIntegration **VendInvoiceInfoTable** DataRetrieval</span></span>
- <span data-ttu-id="849db-143">AxClass/TaxIntegration **SalesTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="849db-143">AxClass/TaxIntegration **SalesTable** DataRetrieval</span></span>
- <span data-ttu-id="849db-144">AxClass/TaxIntegration **SalesParm** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="849db-144">AxClass/TaxIntegration **SalesParm** DataRetrieval</span></span>

<span data-ttu-id="849db-145">在这些 **数据检索** 活动中，将数据从数据库复制到 `TaxIntegrationDocumentObject` 和 `TaxIntegrationLineObject`。</span><span class="sxs-lookup"><span data-stu-id="849db-145">In these **Data Retrieval** activities, data is copied from the database to `TaxIntegrationDocumentObject` and `TaxIntegrationLineObject`.</span></span> <span data-ttu-id="849db-146">因为所有这些活动扩展相同的抽象模板类，所以它们具有通用方法。</span><span class="sxs-lookup"><span data-stu-id="849db-146">Because all these activities extend the same abstract template class, they have common methods.</span></span>

#### <a name="calculation-service-activities"></a><span data-ttu-id="849db-147">计算服务活动</span><span class="sxs-lookup"><span data-stu-id="849db-147">Calculation Service activities</span></span>

<span data-ttu-id="849db-148">**计算服务** 活动是税务服务和税务集成之间的链接。</span><span class="sxs-lookup"><span data-stu-id="849db-148">The **Calculation Service** activity is the link between the tax service and the tax integration.</span></span> <span data-ttu-id="849db-149">此活动负责以下功能：</span><span class="sxs-lookup"><span data-stu-id="849db-149">This activity is responsible for the following functions:</span></span>

1. <span data-ttu-id="849db-150">构造请求。</span><span class="sxs-lookup"><span data-stu-id="849db-150">Construct the request.</span></span>
2. <span data-ttu-id="849db-151">将请求过帐到税务服务。</span><span class="sxs-lookup"><span data-stu-id="849db-151">Post the request to the tax service.</span></span>
3. <span data-ttu-id="849db-152">从税务服务获得响应。</span><span class="sxs-lookup"><span data-stu-id="849db-152">Get the response from the tax service.</span></span>
4. <span data-ttu-id="849db-153">分析响应。</span><span class="sxs-lookup"><span data-stu-id="849db-153">Parse the response.</span></span>

<span data-ttu-id="849db-154">添加到请求的数据字段将与其他元数据一起过帐。</span><span class="sxs-lookup"><span data-stu-id="849db-154">A data field that you add to the request will be posted together with other metadata.</span></span> 

## <a name="extension-implementation"></a><span data-ttu-id="849db-155">扩展实施</span><span class="sxs-lookup"><span data-stu-id="849db-155">Extension implementation</span></span>

<span data-ttu-id="849db-156">本部分提供说明如何实施扩展的详细步骤。</span><span class="sxs-lookup"><span data-stu-id="849db-156">This section provides detailed steps that explain how to implement the extension.</span></span> <span data-ttu-id="849db-157">它使用 **成本中心** 和 **项目** 财务维度作为示例。</span><span class="sxs-lookup"><span data-stu-id="849db-157">It uses the **Cost center** and **Project** financial dimensions as examples.</span></span>

### <a name="step-1-add-the-data-variable-in-the-object-class"></a><span data-ttu-id="849db-158">步骤 1.</span><span class="sxs-lookup"><span data-stu-id="849db-158">Step 1.</span></span> <span data-ttu-id="849db-159">在对象类中添加数据变量</span><span class="sxs-lookup"><span data-stu-id="849db-159">Add the data variable in the object class</span></span>

<span data-ttu-id="849db-160">对象类包含数据变量和数据的 getter/setter 方法。</span><span class="sxs-lookup"><span data-stu-id="849db-160">The object class contains the data variable and getter/setter methods for the data.</span></span> <span data-ttu-id="849db-161">将数据字段添加到 `TaxIntegrationDocumentObject` 或 `TaxIntegrationLineObject`，具体取决于字段的级别。</span><span class="sxs-lookup"><span data-stu-id="849db-161">Add the data field to either `TaxIntegrationDocumentObject` or `TaxIntegrationLineObject`, depending on the level of the field.</span></span> <span data-ttu-id="849db-162">以下示例使用行级别，文件名是 `TaxIntegrationLineObject_Extension.xpp`。</span><span class="sxs-lookup"><span data-stu-id="849db-162">The following example uses the line level, and the file name is `TaxIntegrationLineObject_Extension.xpp`.</span></span>

> [!NOTE]
> <span data-ttu-id="849db-163">如果要添加的数据字段位于文档级别，将文件名更改为 `TaxIntegrationDocumentObject_Extension.xpp`。</span><span class="sxs-lookup"><span data-stu-id="849db-163">If the data field that you're adding is at the document level, change the file name to `TaxIntegrationDocumentObject_Extension.xpp`.</span></span>

```X++
[ExtensionOf(classStr(TaxIntegrationLineObject))]
final class TaxIntegrationLineObject_Extension
{
    private OMOperatingUnitNumber costCenter;
    private ProjId projectId;

    /// <summary>
    /// Gets a costCenter.
    /// </summary>
    /// <returns>The cost center.</returns>
    public final OMOperatingUnitNumber getCostCenter()
    {
        return this.costCenter;
    }

    /// <summary>
    /// Sets the cost center.
    /// </summary>
    /// <param name = "_value">The cost center.</param>
    public final void setCostCenter(OMOperatingUnitNumber _value)
    {
        this.costCenter = _value;
    }

    /// <summary>
    /// Gets a project ID.
    /// </summary>
    /// <returns>The project ID.</returns>
    public final ProjId getProjectId()
    {
        return this.projectId;
    }

    /// <summary>
    /// Sets the project ID.
    /// </summary>
    /// <param name = "_value">The project ID.</param>
    public final void setProjectId(ProjId _value)
    {
        this.projectId = _value;
    }
}
```

<span data-ttu-id="849db-164">**成本中心** 和 **项目** 将添加为私有变量。</span><span class="sxs-lookup"><span data-stu-id="849db-164">**Cost center** and **Project** are added as private variables.</span></span> <span data-ttu-id="849db-165">为这些数据字段创建 getter 和 setter 方法以处理数据。</span><span class="sxs-lookup"><span data-stu-id="849db-165">Create getter and setter methods for these data fields to manipulate the data.</span></span>

### <a name="step-2-retrieve-data-from-the-database"></a><span data-ttu-id="849db-166">步骤 2.</span><span class="sxs-lookup"><span data-stu-id="849db-166">Step 2.</span></span> <span data-ttu-id="849db-167">从数据库检索数据</span><span class="sxs-lookup"><span data-stu-id="849db-167">Retrieve data from the database</span></span>

<span data-ttu-id="849db-168">指定事务，并扩展适当的适配器类以检索数据。</span><span class="sxs-lookup"><span data-stu-id="849db-168">Specify the transaction, and extend the appropriate adapter classes to retrieve the data.</span></span> <span data-ttu-id="849db-169">例如，如果您使用 **采购订单** 事务，必须扩展 `TaxIntegrationPurchTableDataRetrieval` 和 `TaxIntegrationVendInvoiceInfoTableDataRetrieval`。</span><span class="sxs-lookup"><span data-stu-id="849db-169">For example, if you use a **Purchase order** transaction, you must extend `TaxIntegrationPurchTableDataRetrieval` and `TaxIntegrationVendInvoiceInfoTableDataRetrieval`.</span></span> 

> [!NOTE]
> <span data-ttu-id="849db-170">`TaxIntegrationPurchParmTableDataRetrieval` 继承自 `TaxIntegrationPurchTableDataRetrieval`。</span><span class="sxs-lookup"><span data-stu-id="849db-170">`TaxIntegrationPurchParmTableDataRetrieval` is inherited from `TaxIntegrationPurchTableDataRetrieval`.</span></span> <span data-ttu-id="849db-171">它不应该更改，除非 `purchTable` 和 `purchParmTable` 表的逻辑不同。</span><span class="sxs-lookup"><span data-stu-id="849db-171">It should not be changed unless the logic of the `purchTable` and `purchParmTable` tables differs.</span></span>

<span data-ttu-id="849db-172">如果应该为所有事务添加数据字段，扩展所有 `DataRetrieval` 类。</span><span class="sxs-lookup"><span data-stu-id="849db-172">If the data field should be added for all transactions, extend all `DataRetrieval` classes.</span></span>

<span data-ttu-id="849db-173">因为所有 **数据检索** 活动扩展相同的模板类，类结构、变量和方法类似。</span><span class="sxs-lookup"><span data-stu-id="849db-173">Because all **Data Retrieval** activities extend the same template class, the class structures, variables, and methods are similar.</span></span>

```X++
protected TaxIntegrationDocumentObject document;

/// <summary>
/// Copies to the document.
/// </summary>
protected abstract void copyToDocument()
{
    // It is recommended to implement as:
    //
    // this.copyToDocumentByDefault();
    // this.copyToDocumentFromHeaderTable();
    // this.copyAddressToDocument();
}
 
/// <summary>
/// Copies to the current line of the document.
/// </summary>
/// <param name = "_line">The current line of the document.</param>
protected abstract void copyToLine(TaxIntegrationLineObject _line)
{
    // It is recommended to implement as:
    //
    // this.copyToLineByDefault(_line);
    // this.copyToLineFromLineTable(_line);
    // this.copyQuantityAndTransactionAmountToLine(_line);
    // this.copyAddressToLine(_line);
    // this.copyToLineFromHeaderTable(_line);
}
```

<span data-ttu-id="849db-174">以下示例显示使用 `PurchTable` 表时的基础结构。</span><span class="sxs-lookup"><span data-stu-id="849db-174">The following example shows the basic structure when the `PurchTable` table is used.</span></span>

```X++
public class TaxIntegrationPurchTableDataRetrieval extends TaxIntegrationAbstractDataRetrievalTemplate
{
    protected PurchTable purchTable;
    protected PurchLine purchLine;

    // Query builder methods
    [Replaceable]
    protected SysDaQueryObject getDocumentQueryObject()
    [Replaceable]
    protected SysDaQueryObject getLineQueryObject()
    [Replaceable]
    protected SysDaQueryObject getDocumentChargeQueryObject()
    [Replaceable]
    protected SysDaQueryObject getLineChargeQueryObject()

    // Data retrieval methods
    protected void copyToDocument()
    protected void copyToDocumentFromHeaderTable()
    protected void copyToLine(TaxIntegrationLineObject _line)
    protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
    ...
}
```

<span data-ttu-id="849db-175">当调用 `CopyToDocument` 方法时，`this.purchTable` 缓冲已存在。</span><span class="sxs-lookup"><span data-stu-id="849db-175">When the `CopyToDocument` method is called, the `this.purchTable` buffer already exists.</span></span> <span data-ttu-id="849db-176">此方法的目的是使用在 `DocumentObject` 类中创建的 setter 方法将所有所需数据从 `this.purchTable` 复制到 `document` 对象。</span><span class="sxs-lookup"><span data-stu-id="849db-176">The purpose of this method is to copy all the required data from `this.purchTable` to the `document` object by using the setter method that was created in the `DocumentObject` class.</span></span>

<span data-ttu-id="849db-177">同样，`this.purchLine` 缓冲已存在于 `CopyToLine` 方法中。</span><span class="sxs-lookup"><span data-stu-id="849db-177">Likewise, a `this.purchLine` buffer already exists in the `CopyToLine` method.</span></span> <span data-ttu-id="849db-178">此方法的目的是使用在 `LineObject` 类中创建的 setter 方法将所有所需数据从 `this.purchLine` 复制到 `_line` 对象。</span><span class="sxs-lookup"><span data-stu-id="849db-178">The purpose of this method is to copy all the required data from `this.purchLine` to the `_line` object by using the setter method that was created in the `LineObject` class.</span></span>

<span data-ttu-id="849db-179">最直接的方法是扩展 `CopyToDocument` 和 `CopyToLine` 方法。</span><span class="sxs-lookup"><span data-stu-id="849db-179">The most straightforward approach is to extend the `CopyToDocument` and `CopyToLine` methods.</span></span> <span data-ttu-id="849db-180">但是，我们建议您首先尝试 `copyToDocumentFromHeaderTable` 和 `copyToLineFromLineTable` 方法。</span><span class="sxs-lookup"><span data-stu-id="849db-180">However, we recommend that you try the `copyToDocumentFromHeaderTable` and `copyToLineFromLineTable` methods first.</span></span> <span data-ttu-id="849db-181">如果它们不按您的要求工作，请实施自己的方法，并在 `CopyToDocument` 和 `CopyToLine` 中调用它。</span><span class="sxs-lookup"><span data-stu-id="849db-181">If they don't work as you require, implement your own method, and call it in `CopyToDocument` and `CopyToLine`.</span></span> <span data-ttu-id="849db-182">在以下三种常见情况下，您可能会使用此方法：</span><span class="sxs-lookup"><span data-stu-id="849db-182">There are three common situations where you might use this approach:</span></span>

- <span data-ttu-id="849db-183">必填字段在 `PurchTable` 或 `PurchLine` 中。</span><span class="sxs-lookup"><span data-stu-id="849db-183">The required field is in `PurchTable` or `PurchLine`.</span></span> <span data-ttu-id="849db-184">在这种情况下，您可以扩展 `copyToDocumentFromHeaderTable` 和 `copyToLineFromLineTable`。</span><span class="sxs-lookup"><span data-stu-id="849db-184">In this situation, you can extend `copyToDocumentFromHeaderTable` and `copyToLineFromLineTable`.</span></span> <span data-ttu-id="849db-185">下面是示例代码。</span><span class="sxs-lookup"><span data-stu-id="849db-185">Here is the sample code.</span></span>

    ```X++
    /// <summary>
    /// Copies to the current line of the document from.
    /// </summary>
    /// <param name = "_line">The current line of the document.</param>
    protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
    {
        next copyToLineFromLineTable(_line);
        // if we already added XXX in TaxIntegrationLineObject
        _line.setXXX(this.purchLine.XXX);
    }
    ```

- <span data-ttu-id="849db-186">所需数据不在事务的默认表中。</span><span class="sxs-lookup"><span data-stu-id="849db-186">The required data isn't in the default table of the transaction.</span></span> <span data-ttu-id="849db-187">但是，默认表存在一些联接关系，并且大多数行上都需要该字段。</span><span class="sxs-lookup"><span data-stu-id="849db-187">However, there are some join relationships with the default table, and the field is required on most lines.</span></span> <span data-ttu-id="849db-188">在这种情况下，替换 `getDocumentQueryObject` 或 `getLineObject` 以通过联接关系查询表。</span><span class="sxs-lookup"><span data-stu-id="849db-188">In this situation, replace `getDocumentQueryObject` or `getLineObject` to query the table by join relationship.</span></span> <span data-ttu-id="849db-189">在以下示例中，**现在交货** 字段在行级别与销售订单集成。</span><span class="sxs-lookup"><span data-stu-id="849db-189">In the following example, the **Deliver Now** field is integrated with the sales order at the line level.</span></span>

    ```X++
    public class TaxIntegrationSalesTableDataRetrieval
    {
        protected MCRSalesLineDropShipment mcrSalesLineDropShipment;

        /// <summary>
        /// Gets the query for the lines of the document.
        /// </summary>
        /// <returns>The query for the lines of the document</returns>
        [Replaceable]
        protected SysDaQueryObject getLineQueryObject()
        {
            return SysDaQueryObjectBuilder::from(this.salesLine)
                .where(this.salesLine, fieldStr(SalesLine, SalesId)).isEqualToLiteral(this.salesTable.SalesId)
                .outerJoin(this.mcrSalesLineDropShipment)
                .where(this.mcrSalesLineDropShipment, fieldStr(MCRSalesLineDropShipment, SalesLine)).isEqualTo(this.salesLine, fieldStr(SalesLine, RecId))
                .toSysDaQueryObject();
        }
    }
    ```

    <span data-ttu-id="849db-190">在此示例中，声明 `mcrSalesLineDropShipment` 缓冲，并在 `getLineQueryObject` 中定义查询。</span><span class="sxs-lookup"><span data-stu-id="849db-190">In this example, a `mcrSalesLineDropShipment` buffer is declared, and the query is defined in `getLineQueryObject`.</span></span> <span data-ttu-id="849db-191">查询使用关系 `MCRSalesLineDropShipment.SalesLine == SalesLine.RecId`。</span><span class="sxs-lookup"><span data-stu-id="849db-191">The query uses the relationship `MCRSalesLineDropShipment.SalesLine == SalesLine.RecId`.</span></span> <span data-ttu-id="849db-192">当在这种情况下扩展时，可以将 `getLineQueryObject` 替换为您自己的构造查询对象。</span><span class="sxs-lookup"><span data-stu-id="849db-192">While you're extending in this situation, you can replace `getLineQueryObject` with your own constructed query object.</span></span> <span data-ttu-id="849db-193">但是，请注意以下几点：</span><span class="sxs-lookup"><span data-stu-id="849db-193">However, note the following points:</span></span>

    * <span data-ttu-id="849db-194">因为 `getLineQueryObject` 方法的返回值是 `SysDaQueryObject`，因此您必须使用 SysDa 方法构造此对象。</span><span class="sxs-lookup"><span data-stu-id="849db-194">Because the return value of the `getLineQueryObject` method is `SysDaQueryObject`, you must construct this object by using the SysDa approach.</span></span>
    * <span data-ttu-id="849db-195">无法删除现有表。</span><span class="sxs-lookup"><span data-stu-id="849db-195">Can't remove existed table.</span></span>

- <span data-ttu-id="849db-196">所需数据通过复杂的联接关系与事务表相关，或者该关系不是一对一 (1:1)，而是一对多 (1:N)。</span><span class="sxs-lookup"><span data-stu-id="849db-196">The required data is related to the transaction table by a complicated join relationship, or the relation isn't one to one (1:1) but one to many (1:N).</span></span> <span data-ttu-id="849db-197">在这种情况下，事情变得有些复杂。</span><span class="sxs-lookup"><span data-stu-id="849db-197">In this situation, things become a little complicated.</span></span> <span data-ttu-id="849db-198">这种情况适用于财务维度的示例。</span><span class="sxs-lookup"><span data-stu-id="849db-198">This situation applies to the example of financial dimensions.</span></span> 

    <span data-ttu-id="849db-199">在这种情况下，您可以实施自己的方法来检索数据。</span><span class="sxs-lookup"><span data-stu-id="849db-199">In this situation, you can implement your own method to retrieve the data.</span></span> <span data-ttu-id="849db-200">下面是 `TaxIntegrationPurchTableDataRetrieval_Extension.xpp` 文件中的示例代码。</span><span class="sxs-lookup"><span data-stu-id="849db-200">Here is the sample code in the `TaxIntegrationPurchTableDataRetrieval_Extension.xpp` file.</span></span>

    ```X++
    [ExtensionOf(classStr(TaxIntegrationPurchTableDataRetrieval))]
    final class TaxIntegrationPurchTableDataRetrieval_Extension
    {
        private const str CostCenterKey = 'CostCenter';
        private const str ProjectKey = 'Project';

        /// <summary>
        /// Copies to the current line of the document from.
        /// </summary>
        /// <param name = "_line">The current line of the document.</param>
        protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
        {
            Map dimensionAttributeMap = this.getDimensionAttributeMapByDefaultDimension(this.purchline.DefaultDimension);
            if (dimensionAttributeMap.exists(CostCenterKey))
            {
                _line.setCostCenter(dimensionAttributeMap.lookup(CostCenterKey));
            }
            if (dimensionAttributeMap.exists(ProjectKey))
            {
                _line.setProjectId(dimensionAttributeMap.lookup(ProjectKey));
            }
            next copyToLineFromLineTable(_line);
        }
        private Map getDimensionAttributeMapByDefaultDimension(RefRecId _defaultDimension)
        {
            DimensionAttribute dimensionAttribute;
            DimensionAttributeValue dimensionAttributeValue;
            DimensionAttributeValueSetItem dimensionAttributeValueSetItem;
            Map ret = new Map(Types::String, Types::String);

            select Name, RecId from dimensionAttribute
                join dimensionAttributeValue
                    where dimensionAttributeValue.dimensionAttribute == dimensionAttribute.RecId
                join DimensionAttributeValueSetItem
                    where DimensionAttributeValueSetItem.DimensionAttributeValue == DimensionAttributeValue.RecId
                        && DimensionAttributeValueSetItem.DimensionAttributeValueSet == _defaultDimension;

            while(dimensionAttribute.RecId)
            {
                ret.insert(dimensionAttribute.Name, dimensionAttributeValue.DisplayValue);
                next dimensionAttribute;
            }
            return ret;
        }
    }
    ```

### <a name="step-3-add-data-to-the-request"></a><span data-ttu-id="849db-201">步骤 3.</span><span class="sxs-lookup"><span data-stu-id="849db-201">Step 3.</span></span> <span data-ttu-id="849db-202">将数据添加到请求</span><span class="sxs-lookup"><span data-stu-id="849db-202">Add data to the request</span></span>

<span data-ttu-id="849db-203">扩展 `copyToTaxableDocumentHeaderWrapperFromTaxIntegrationDocumentObject` 或 `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` 以将数据添加到请求。</span><span class="sxs-lookup"><span data-stu-id="849db-203">Extend the `copyToTaxableDocumentHeaderWrapperFromTaxIntegrationDocumentObject` or `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` method to add data to the request.</span></span> <span data-ttu-id="849db-204">下面是 `TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp` 文件中的示例代码。</span><span class="sxs-lookup"><span data-stu-id="849db-204">Here is the sample code in the `TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp` file.</span></span>

```X++
[ExtensionOf(classStr(TaxIntegrationCalculationActivityOnDocument_CalculationService))]
final static class TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension
{
    // Define key for the form in post request
    private const str IOCostCenter = 'Cost Center';
    private const str IOProject = 'Project';

    /// <summary>
    /// Copies to <c>TaxableDocumentLineWrapper</c> from <c>TaxIntegrationLineObject</c> by line.
    /// </summary>
    /// <param name = "_destination"><c>TaxableDocumentLineWrapper</c>.</param>
    /// <param name = "_source"><c>TaxIntegrationLineObject</c>.</param>
    protected static void copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(Microsoft.Dynamics.TaxCalculation.ApiContracts.TaxableDocumentLineWrapper _destination, TaxIntegrationLineObject _source)
    {
        next copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(_destination, _source);
        // Set the field we need to integrated for tax service
        _destination.SetField(IOCostCenter, _source.getCostCenter());
        _destination.SetField(IOProject, _source.getProjectId());
    }
}
```

<span data-ttu-id="849db-205">在此代码中，`_destination` 是用于生成过帐请求的包装器对象，`_source` 是 `TaxIntegrationLineObject` 对象。</span><span class="sxs-lookup"><span data-stu-id="849db-205">In this code, `_destination` is the wrapper object that is used to generate the post request, and `_source` is the `TaxIntegrationLineObject` object.</span></span> 

> [!NOTE]
> * <span data-ttu-id="849db-206">定义在请求窗体中用作 `private const str` 的密钥。</span><span class="sxs-lookup"><span data-stu-id="849db-206">Define the key that is used in the request form as `private const str`.</span></span>
> * <span data-ttu-id="849db-207">使用 `SetField` 方法在 `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` 方法中设置字段。</span><span class="sxs-lookup"><span data-stu-id="849db-207">Set the field in the `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` method by using the `SetField` method.</span></span> <span data-ttu-id="849db-208">第二个参数的数据类型应为 `string`。</span><span class="sxs-lookup"><span data-stu-id="849db-208">The data type of the second parameter should be `string`.</span></span> <span data-ttu-id="849db-209">如果数据类型不是 `string`，将其转换为 `string`。</span><span class="sxs-lookup"><span data-stu-id="849db-209">If the data type isn't `string`, convert it to `string`.</span></span>

## <a name="appendix"></a><span data-ttu-id="849db-210">附录</span><span class="sxs-lookup"><span data-stu-id="849db-210">Appendix</span></span>

<span data-ttu-id="849db-211">本附录显示了用于在行级别集成财务维度（**成本中心** 和 **项目**）的完整示例代码。</span><span class="sxs-lookup"><span data-stu-id="849db-211">This appendix shows the complete sample code for the integration of financial dimensions (**Cost center** and **Project**) at the line level.</span></span>

### <a name="taxintegrationlineobject_extensionxpp"></a><span data-ttu-id="849db-212">TaxIntegrationLineObject_Extension.xpp</span><span class="sxs-lookup"><span data-stu-id="849db-212">TaxIntegrationLineObject_Extension.xpp</span></span>

```X++
[ExtensionOf(classStr(TaxIntegrationLineObject))]
final class TaxIntegrationLineObject_Extension
{
    private OMOperatingUnitNumber costCenter;
    private ProjId projectId;

    /// <summary>
    /// Gets a costCenter.
    /// </summary>
    /// <returns>The cost center.</returns>
    public final OMOperatingUnitNumber getCostCenter()
    {
        return this.costCenter;
    }

    /// <summary>
    /// Sets the cost center.
    /// </summary>
    /// <param name = "_value">The cost center.</param>
    public final void setCostCenter(OMOperatingUnitNumber _value)
    {
        this.costCenter = _value;
    }

    /// <summary>
    /// Gets a project ID.
    /// </summary>
    /// <returns>The project ID.</returns>
    public final ProjId getProjectId()
    {
        return this.projectId;
    }

    /// <summary>
    /// Sets the project ID.
    /// </summary>
    /// <param name = "_value">The project ID.</param>
    public final void setProjectId(ProjId _value)
    {
        this.projectId = _value;
    }
}
```

### <a name="taxintegrationpurchtabledataretrieval_extensionxpp"></a><span data-ttu-id="849db-213">TaxIntegrationPurchTableDataRetrieval_Extension.xpp</span><span class="sxs-lookup"><span data-stu-id="849db-213">TaxIntegrationPurchTableDataRetrieval_Extension.xpp</span></span>

```X++
[ExtensionOf(classStr(TaxIntegrationPurchTableDataRetrieval))]
final class TaxIntegrationPurchTableDataRetrieval_Extension
{
    private const str CostCenterKey = 'CostCenter';
    private const str ProjectKey = 'Project';

    /// <summary>
    /// Copies to the current line of the document from.
    /// </summary>
    /// <param name = "_line">The current line of the document.</param>
    protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
    {
        Map dimensionAttributeMap = this.getDimensionAttributeMapByDefaultDimension(this.purchline.DefaultDimension);
        if (dimensionAttributeMap.exists(CostCenterKey))
        {
            _line.setCostCenter(dimensionAttributeMap.lookup(CostCenterKey));
        }
        if (dimensionAttributeMap.exists(ProjectKey))
        {
            _line.setProjectId(dimensionAttributeMap.lookup(ProjectKey));
        }
        next copyToLineFromLineTable(_line);
    }
    private Map getDimensionAttributeMapByDefaultDimension(RefRecId _defaultDimension)
    {
        DimensionAttribute dimensionAttribute;
        DimensionAttributeValue dimensionAttributeValue;
        DimensionAttributeValueSetItem dimensionAttributeValueSetItem;
        Map ret = new Map(Types::String, Types::String);
        select Name, RecId from dimensionAttribute
            join dimensionAttributeValue
                where dimensionAttributeValue.dimensionAttribute == dimensionAttribute.RecId
            join DimensionAttributeValueSetItem
                where DimensionAttributeValueSetItem.DimensionAttributeValue == DimensionAttributeValue.RecId
                    && DimensionAttributeValueSetItem.DimensionAttributeValueSet == _defaultDimension;
        while(dimensionAttribute.RecId)
        {
            ret.insert(dimensionAttribute.Name, dimensionAttributeValue.DisplayValue);
            next dimensionAttribute;
        }
        return ret;
    }
}
```

### <a name="taxintegrationcalculationactivityondocument_calculationservice_extensionxpp"></a><span data-ttu-id="849db-214">TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp</span><span class="sxs-lookup"><span data-stu-id="849db-214">TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp</span></span>

```X++
[ExtensionOf(classStr(TaxIntegrationCalculationActivityOnDocument_CalculationService))]
final static class TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension
{
    // Define key for the form in post request
    private const str IOCostCenter = 'Cost Center';
    private const str IOProject = 'Project';

    /// <summary>
    /// Copies to <c>TaxableDocumentLineWrapper</c> from <c>TaxIntegrationLineObject</c> by line.
    /// </summary>
    /// <param name = "_destination"><c>TaxableDocumentLineWrapper</c>.</param>
    /// <param name = "_source"><c>TaxIntegrationLineObject</c>.</param>
    protected static void copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(Microsoft.Dynamics.TaxCalculation.ApiContracts.TaxableDocumentLineWrapper _destination, TaxIntegrationLineObject _source)
    {
        next copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(_destination, _source);
        // Set the field we need to integrated for tax service
        _destination.SetField(IOCostCenter, _source.getCostCenter());
        _destination.SetField(IOProject, _source.getProjectId());
    }
}
```
