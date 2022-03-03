---
title: 使用扩展在税务集成中添加数据字段
description: 本主题说明如何使用 X++ 扩展在税务集成中添加数据字段。
author: qire
ms.date: 02/17/2022
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: acbe8070424febf24883362448ea56857d9d72d9
ms.sourcegitcommit: 68114cc54af88be9a3a1a368d5964876e68e8c60
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/17/2022
ms.locfileid: "8323515"
---
# <a name="add-data-fields-in-the-tax-integration-by-using-extension"></a>使用扩展在税务集成中添加数据字段

[!include [banner](../includes/banner.md)]


本主题说明如何使用 X++ 扩展在税务集成中添加数据字段。 这些字段可以扩展到税务服务的税务数据模型，并用于确定税码。 有关详细信息，请参阅[在税务配置中添加数据字段](tax-service-add-data-fields-tax-configurations.md)。

## <a name="data-model"></a>数据模型

数据模型中的数据由对象承载并由类实现。

下面是主要对象的列表：

* AxClass/TaxIntegration **Document** Object
* AxClass/TaxIntegration **Line** Object
* AxClass/TaxIntegration **TaxLine** Object

下图显示了这些对象之间的关系。

[![数据模型对象关系。](./media/tax-service-customize-image1.png)](./media/tax-service-customize-image1.png)

**单据** 对象可以包含许多 **行** 对象。 每个对象都包含税务服务的元数据。

- `TaxIntegrationDocumentObject` 具有 `originAddress` 元数据（包含有关源地址的信息）和 `includingTax` 元数据（指示行金额是否包含销售税）。
- `TaxIntegrationLineObject` 具有 `itemId`、`quantity` 和 `categoryId` 元数据。

> [!NOTE]
> `TaxIntegrationLineObject` 还实施 **费用** 对象。

## <a name="integration-flow"></a>集成流

流中的数据由活动处理。

### <a name="key-activities"></a>关键活动

* AxClass/TaxIntegration **Calculation** ActivityOnDocument
* AxClass/TaxIntegration **CurrencyExchange** ActivityOnDocument
* AxClass/TaxIntegration **DataPersistence** ActivityOnDocument
* AxClass/TaxIntegration **DataRetrieval** ActivityOnDocument
* AxClass/TaxIntegration **SettingRetrieval** ActivityOnDocument

活动按以下顺序运行：

1. 设置检索
2. 数据检索
3. 计算服务
4. 币种汇兑
5. 数据持久性

例如，在 **计算服务** 之前扩展 **数据检索**。

#### <a name="data-retrieval-activities"></a>数据检索活动

**数据检索** 活动从数据库中检索数据。 不同事务的适配器可用于从不同的事务表中检索数据：

- AxClass/TaxIntegration **PurchTable** DataRetrieval
- AxClass/TaxIntegration **PurchParmTable** DataRetrieval
- AxClass/TaxIntegration **PurchREQTable** DataRetrieval
- AxClass/TaxIntegration **PurchRFQTable** DataRetrieval
- AxClass/TaxIntegration **VendInvoiceInfoTable** DataRetrieval
- AxClass/TaxIntegration **SalesTable** DataRetrieval
- AxClass/TaxIntegration **SalesParm** DataRetrieval

在这些 **数据检索** 活动中，将数据从数据库复制到 `TaxIntegrationDocumentObject` 和 `TaxIntegrationLineObject`。 因为所有这些活动扩展相同的抽象模板类，所以它们具有通用方法。

#### <a name="calculation-service-activities"></a>计算服务活动

**计算服务** 活动是税务服务和税务集成之间的链接。 此活动负责以下功能：

1. 构造请求。
2. 将请求过帐到税务服务。
3. 从税务服务获得响应。
4. 分析响应。

添加到请求的数据字段将与其他元数据一起过帐。 

## <a name="extension-implementation"></a>扩展实施

本部分提供说明如何实施扩展的详细步骤。 它使用 **成本中心** 和 **项目** 财务维度作为示例。

### <a name="step-1-add-the-data-variable-in-the-object-class"></a>步骤 1. 在对象类中添加数据变量

对象类包含数据变量和数据的 getter/setter 方法。 将数据字段添加到 `TaxIntegrationDocumentObject` 或 `TaxIntegrationLineObject`，具体取决于字段的级别。 以下示例使用行级别，文件名是 `TaxIntegrationLineObject_Extension.xpp`。

> [!NOTE]
> 如果要添加的数据字段位于文档级别，将文件名更改为 `TaxIntegrationDocumentObject_Extension.xpp`。

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

**成本中心** 和 **项目** 将添加为私有变量。 为这些数据字段创建 getter 和 setter 方法以处理数据。

### <a name="step-2-retrieve-data-from-the-database"></a>步骤 2. 从数据库检索数据

指定事务，并扩展适当的适配器类以检索数据。 例如，如果您使用 **采购订单** 事务，必须扩展 `TaxIntegrationPurchTableDataRetrieval` 和 `TaxIntegrationVendInvoiceInfoTableDataRetrieval`。 

> [!NOTE]
> `TaxIntegrationPurchParmTableDataRetrieval` 继承自 `TaxIntegrationPurchTableDataRetrieval`。 它不应该更改，除非 `purchTable` 和 `purchParmTable` 表的逻辑不同。

如果应该为所有事务添加数据字段，扩展所有 `DataRetrieval` 类。

因为所有 **数据检索** 活动扩展相同的模板类，类结构、变量和方法类似。

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

以下示例显示使用 `PurchTable` 表时的基础结构。

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

当调用 `CopyToDocument` 方法时，`this.purchTable` 缓冲已存在。 此方法的目的是使用在 `DocumentObject` 类中创建的 setter 方法将所有所需数据从 `this.purchTable` 复制到 `document` 对象。

同样，`this.purchLine` 缓冲已存在于 `CopyToLine` 方法中。 此方法的目的是使用在 `LineObject` 类中创建的 setter 方法将所有所需数据从 `this.purchLine` 复制到 `_line` 对象。

最直接的方法是扩展 `CopyToDocument` 和 `CopyToLine` 方法。 但是，我们建议您首先尝试 `copyToDocumentFromHeaderTable` 和 `copyToLineFromLineTable` 方法。 如果它们不按您的要求工作，请实施自己的方法，并在 `CopyToDocument` 和 `CopyToLine` 中调用它。 在以下三种常见情况下，您可能会使用此方法：

- 必填字段在 `PurchTable` 或 `PurchLine` 中。 在这种情况下，您可以扩展 `copyToDocumentFromHeaderTable` 和 `copyToLineFromLineTable`。 下面是示例代码。

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

- 所需数据不在事务的默认表中。 但是，默认表存在一些联接关系，并且大多数行上都需要该字段。 在这种情况下，替换 `getDocumentQueryObject` 或 `getLineObject` 以通过联接关系查询表。 在以下示例中，**现在交货** 字段在行级别与销售订单集成。

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

    在此示例中，声明 `mcrSalesLineDropShipment` 缓冲，并在 `getLineQueryObject` 中定义查询。 查询使用关系 `MCRSalesLineDropShipment.SalesLine == SalesLine.RecId`。 当在这种情况下扩展时，可以将 `getLineQueryObject` 替换为您自己的构造查询对象。 但是，请注意以下几点：

    * 因为 `getLineQueryObject` 方法的返回值是 `SysDaQueryObject`，因此您必须使用 SysDa 方法构造此对象。
    * 无法删除现有表。

- 所需数据通过复杂的联接关系与事务表相关，或者该关系不是一对一 (1:1)，而是一对多 (1:N)。 在这种情况下，事情变得有些复杂。 这种情况适用于财务维度的示例。 

    在这种情况下，您可以实施自己的方法来检索数据。 下面是 `TaxIntegrationPurchTableDataRetrieval_Extension.xpp` 文件中的示例代码。

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

### <a name="step-3-add-data-to-the-request"></a>步骤 3. 将数据添加到请求

扩展 `copyToTaxableDocumentHeaderWrapperFromTaxIntegrationDocumentObject` 或 `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` 以将数据添加到请求。 下面是 `TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp` 文件中的示例代码。

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

在此代码中，`_destination` 是用于生成过帐请求的包装器对象，`_source` 是 `TaxIntegrationLineObject` 对象。

> [!NOTE]
> 定义在请求窗体中用作 **private const str** 的密钥。 此字符串应与主题[在税务配置中添加数据字段](tax-service-add-data-fields-tax-configurations.md)中添加的度量名称完全相同。
> 使用 **SetField** 方法设置 **copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine** 方法中的字段。 第二个参数的数据类型应为 **字符串**。 如果数据类型不是 **字符串**，请进行转换。
> 如果扩展了 X++ **枚举类型**，请注意它的值、标签和名称之间的区别。
> 
>   - 枚举的值是整数。
>   - 枚举的标签可能因首选语言而异。 不要使用 **enum2Str** 将枚举类型转换为字符串。
>   - 推荐使用枚举的名称，因为它是固定的。 **enum2Symbol** 可用于将枚举转换为它的名称。 税务配置中添加的枚举值应与枚举名称完全相同。

## <a name="model-dependency"></a>模型依赖项

要成功构建项目，请将以下引用模型添加到模型依赖项中：

- ApplicationPlatform
- ApplicationSuite
- 税引擎
- 维度（如果使用财务维度）
- 代码中引用的其他必要模型

## <a name="validation"></a>验证

完成前面的步骤后，您可以验证您的更改。

1. 在 Finance 中，转到 **应付帐款**，将 **&debug=vs%2CconfirmExit&** 添加到 URL。 例如，https://usnconeboxax1aos.cloud.onebox.dynamics.com/?cmp=DEMF&mi=PurchTableListPage&debug=vs%2CconfirmExit&。 最后的 **&** 是必不可少的。
2. 打开 **采购订单** 页面，选择 **新建** 创建采购订单。
3. 设置自定义字段的值，然后选择 **销售税**。 将自动下载带有前缀 **TaxServiceTroubleshootingLog** 的故障排除文件。 此文件包含过帐到税款计算服务的交易信息。 
4. 检查添加的自定义字段是否存在于 **税务服务计算输入 JSON** 部分，以及值是否正确。 如果值不正确，请仔细检查此文档中的步骤。

文件示例：

```
===Tax service calculation input JSON:===
{
  "TaxableDocument": {
    "Header": [
      {
        "Lines": [
          {
            "Line Type": "Normal",
            "Item Code": "",
            "Item Type": "Item",
            "Quantity": 0.0,
            "Amount": 1000.0,
            "Currency": "EUR",
            "Transaction Date": "2022-1-26T00:00:00",
            ...
            /// The new fields added at line level
            "Cost Center": "003",
            "Project": "Proj-123"
          }
        ],
        "Amount include tax": true,
        "Business Process": "Journal",
        "Currency": "",
        "Vendor Account": "DE-001",
        "Vendor Invoice Account": "DE-001",
        ...
        // The new fields added at header level, no new fields in this example
        ...
      }
    ]
  },
}
...
```

## <a name="appendix"></a>附录

本附录显示了用于在行级别集成财务维度 **成本中心** 和 **项目** 的完整示例代码。

### <a name="taxintegrationlineobject_extensionxpp"></a>TaxIntegrationLineObject_Extension.xpp

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

### <a name="taxintegrationpurchtabledataretrieval_extensionxpp"></a>TaxIntegrationPurchTableDataRetrieval_Extension.xpp

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

### <a name="taxintegrationcalculationactivityondocument_calculationservice_extensionxpp"></a>TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp

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
