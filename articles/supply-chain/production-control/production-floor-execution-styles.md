---
title: 为生产车间执行界面设计样式
description: 本主题介绍如何配置窗体控件，以将默认生产车间执行样式应用于它们。
author: johanhoffmann
ms.date: 11/08/2021
ms.topic: article
ms.search.form: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-02-22
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: ef39dc6414f0afdadd4a4b5a41e1fb1fe60e4974
ms.sourcegitcommit: bc9e75c38e192664cde226ed3a94df5a0b304369
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/10/2021
ms.locfileid: "7790882"
---
# <a name="style-the-production-floor-execution-interface"></a>为生产车间执行界面设计样式

[!include [banner](../includes/banner.md)]

本主题介绍如何配置窗体控件，以将默认生产车间执行样式应用于它们。

## <a name="forms-and-dialogs"></a>窗体和对话

仅当满足以下要求时，才能将样式应用于窗体或对话：

- 如果窗体应类似于现有报告进度窗体，窗体或对话的名称必须以 `JmgProductionFloorExecutionCustomInputDialog` 开头。
- 窗体或对话可以包含详细信息窗体部件。 要对其应用样式，详细信息窗体部件的名称必须以 `JmgProductionFloorExecutionCustomDetailsDialog` 开头。
- 如果窗体或对话应具有简单视图，简单视图的名称必须以 `JmgProductionFloorExecutionCustomDialog` 开头。 具有简单视图的窗体示例包括开始窗体和间接活动窗体。
- 对话中的所有控件都必须按照本主题中的描述配置。

> [!IMPORTANT]
> 此列表前两个要点中提到的功能需要 Supply Chain Management 版本 10.0.19 或更高版本。

只有满足以下要求，才能将样式应用于对话中的 **确定** 按钮：

- 此按钮包含在一个窗体组中。
- 组名称以 `OkButtonGroup` 开头。

只有满足以下要求，才能将样式应用于对话框中的 **取消** 按钮：

- 此按钮包含在一个窗体组中。
- 组名称以 `CancelButtonGroup` 开头。

### <a name="header"></a>页眉

下图显示了一个典型的窗体或对话标头。

![典型窗体或对话标头。](media/pfe-styles-header.png "典型窗体或对话标头")

在 Visual Studio 中，标头是通过使用如下图所示的结构创建的。

![创建标头的典型代码结构。](media/pfe-styles-header-code-structure.png "创建标头的典型代码结构")

要将文本添加到标头中，请使用如下例所示的代码。

```xpp
private void setCaption()
{
    HeaderFieldWithSeparatorText1.text("Report Progress");
    HeaderFieldWithSeparatorText2.text(ProdId);

    …

    HeaderFieldText.text(OprNum);
}
```

编写标头代码时，请应用以下规则：

- 主要组的名称必须是 `TableRowHeaderGroup`。
- 每个文本块（由项目符号分隔）必须以 `HeaderFieldWithSeparatorText` 开头。
- 最后一个文本名称必须以 `HeaderFieldText` 开头。
- 可以跳过 `CaptionImage`。

### <a name="progress-indicator"></a>进度指示器

您可以包含一个进度指示器，它显示在标头的右侧。 下图显示了一个进度指示器。

![典型进度指示器。](media/pfe-styles-header-progress.png "典型进度指示器")

要显示进度指示器，文本字段必须命名为 `ShowProgress`。

## <a name="grid"></a>网格

样式会自动应用。 不需要特定配置。

网格应该具有 `TabularView` 样式，且必须替代自定义窗体上的 `run()` 方法，因为尚不支持新网格。 添加以下代码。

```xpp
public void run()
{
    super();
    // To opt out a page from the new grid
    this.forceLegacyGrid();
}
```

要在主视图中刷新数据，您可能需要在操作的 `click` 方法中使用类似 `this.parmParentForm().updateLayout();` 的内容。 （例如，请看一下 `JmgProductionFloorExecutionReportFeedbackAction` 类。）只需确保在新窗体 (`formCaller.parmDataSource(this.dataSource(1));`) 的 `init` 方法中设置了 `parmDataSource`。 例如，请看一下 `JmgProductionFloorExecutionMainGrid` 窗体。

## <a name="card-view"></a>卡视图

只有满足以下要求，才能将样式应用于卡视图控件：

- 每个卡视图都包含在一个窗体组中。
- 组名以 `CardGroup` 开头（例如，`CardGroupJobsView`）。

下图显示了一个内部没有控件的卡视图。

![没有元素的卡视图。](media/pfe-styles-empty-card.png)

下图显示了其中包含控件的卡视图。

![带有显示 Hz 的元素的卡。](media/pfe-styles-elements.png)

![带有维护请求元素的卡。](media/pfe-styles-elements-maintenance.png)

## <a name="business-card"></a>名片

只有满足以下要求，才能将样式应用于名片控件：

- 每个名片都包含在一个窗体组中。
- 组名以 `BusinessCardGroup` 开头（例如，`BusinessCardGroupJobsList`）。

在名片上设置以下属性：

- **Style**：*列表*
- **Extended style**：*cardList*
- **Multi Select**：*否*
- **Show Col Labels**：*否*

![名片。](media/pfe-styles-business-card.png)

## <a name="radio-button"></a>单选按钮

只有满足以下要求，才能将样式应用于单选按钮：

- 每个单选按钮都包含在一个窗体组中。
- 组名称以 `RadioTextBelow` 或 `RadioTextRight` 开头，具体取决于您希望文本出现的位置。

在单选按钮上设置以下属性：

- **Toggle button**：*检查*
- **Toggle value：** 如果应选择单选按钮，为 *开*；否则为 *关*

下图显示了一个文本出现在单选按钮下方的示例。

![下面显示文本的单选按钮。](media/pfe-styles-radio-text-below.png)

下图显示了一个文本出现在单选按钮右侧的示例。

![右侧显示文本的单选按钮。](media/pfe-styles-radio-text-right.png)

### <a name="radio-buttons-in-internet-explorer"></a>Internet Explorer 中的单选按钮

Internet Explorer 不支持单选按钮样式。 下图显示了 Internet Explorer 中的单选按钮的外观。

![Internet Explorer 中的单选按钮。](media/pfe-styles-browser.png)

## <a name="buttons"></a>按钮

只有满足以下要求，才能将样式应用于按钮：

- 每组按钮都包含在一个窗体组中。 组中的所有按钮将具有相同的样式。
- 对组名称没有要求。

在按钮上设置以下属性：

- **Button Display**：*TextWithImageLeft*
- **Normal Image：** 此属性不能为空。 例如，使用 *CoffeeScript*。
- **Text：** 此属性不能为空。 例如，使用 *开始休息*。
- **Width**：*Auto* 或 *SizeToContent*
- **Height**：*Auto* 或 *SizeToContent*

### <a name="primary-button"></a>主要按钮

只有满足以下要求，才能将样式应用于主要按钮：

- 此按钮包含在一个窗体组中。
- 组名称以 `DefaultButtonGroup` 或 `PrimaryButtonGroup` 开头（例如，`DefaultButtonGroup10`）。

![主要按钮。](media/pfe-styles-first.png)

### <a name="secondary-button"></a>次要按钮

只有满足以下要求，才能将样式应用于次要按钮：

- 此按钮包含在一个窗体组中。
- 组名称为 **右面板**，或组名称以 `SecondaryButtonGroup` 开头。

![次要按钮。](media/pfe-styles-second.png)

### <a name="third-group-button"></a>第三组按钮

只有满足以下要求，才能将样式应用于第三组按钮：

- 此按钮包含在一个窗体组中。
- 组名称为 **左面板**，或组名称以 `ThirdButtonGroup` 开头。

![第三组按钮。](media/pfe-styles-third.png)

### <a name="fourth-group-button"></a>第四组按钮

只有满足以下要求，才能将样式应用于第四组按钮：

- 此按钮包含在一个窗体组中。
- 组名称以 `FourthButtonGroup` 开头。

在此按钮上设置以下属性：

- **Button Display**：*TextOnly*
- **Normal Image：** 此属性必须为空。
- **Text：** 此属性不能为空。 例如，使用 *查看* 或 *编辑*。
- **Width**：*Auto*
- **Height**：*Auto*

![第四组按钮。](media/pfe-styles-fourth.png)

### <a name="flat-button"></a>扁平按钮

只有满足以下要求，才能将样式应用于扁平按钮：

- 此按钮包含在一个窗体组中。
- 组名称以 `FlatButtonGroup` 开头。

在此按钮上设置以下属性：

- **Button Display**：*ImageOnly*
- **Normal Image：** 此属性不能为空。 例如，使用 *CoffeeScript*。
- **Text：** 此属性必须为空。
- **Width**：*Auto* 或 *SizeToContent*
- **Height**：*Auto* 或 *SizeToContent*

![扁平按钮。](media/pfe-styles-flat-button.png)

### <a name="continue-button"></a>继续按钮

只有满足以下要求，才能将样式应用于继续按钮：

- 此按钮包含在一个窗体组中。
- 组名称以 `ContinueButtonGroup` 开头。

在此按钮上设置以下属性：

- **Button Display**：*ImageOnly*
- **Normal Image**：*Forward*
- **Text：** 此属性必须为空。
- **Width**：*Auto* 或 *SizeToContent*
- **Height**：*Auto* 或 *SizeToContent*

![继续按钮。](media/pfe-styles-continue-button.png)

## <a name="combo-box"></a>组合框

组合框是三个控件的组合：输入控件、清除输入控件的按钮和运行搜索的按钮。

只有满足以下要求，才能将样式应用于组合框：

- 组合框包含在窗体组中。
- 组名称以 `Combobox` 开头。
- 在组内，第一个控件是 `AxFormStringControl` 控件。 此控件显示当前值，是用户输入所需值的地方。
- 第二个控件是 `CommonButton` 控件，其名称以 `ClearButton` 开头。 此按钮必须包含使用 `enable` 属性来显示或隐藏按钮的代码。 例如，要在用户在输入控件中键入信息时显示或隐藏 **清除** 按钮，可以使用以下代码。

    ```xpp
    public void textChange()
    {
        super();
        ClearButtonSerial.enabled(this.text()? true : false);
    }
    ```

    您应该有一个在输入控件中设置数据的方法。 在该方法中启用 **清除** 按钮。 下面是一个示例。

    ```xpp
    public void setSerialId(str _serialId)
    {
        JmgTmpJobBundleProdFeedback.InventSerial = _serialId;
        ClearButtonSerial.enabled(_serialId? true : false);

        if (_serialId)
        {
            this.addSerialNumber();
        }
    }
    ```

    为 **清除** 按钮的 `clicked` 方法使用以下代码。

    ```xpp
    public void clicked()
    {
        element.setSerialId('');
        InventSerialId.setFocus(); // set focus back to the input box
    }
    ```

    当使用 `init` 方法初始化窗体时，设置输入控件 `AxFormStringControl` 的值。 如果此值不为空，启用 **清除** 按钮。 如果此值为空，禁用 **清除** 按钮。

- 第三个控件是 `CommonButton` 控件，其名称以 `SearchButton` 开头。

下图显示了两个组合框控件。 左边的组合框有一个空文本框，禁用了 **清除** 按钮。 右边的组合框在文本框中有文本，**清除** 按钮启用。

![带和不带“清除”按钮的组合框。](media/pfe-styles-combo.png)

## <a name="quick-filter"></a>快速筛选器

快速筛选器控件将搜索字段添加到页面。 您可以将样式应用于快速筛选器，但需要满足以下要求：

- 快速筛选器包含在窗体组中。
- 组名称以 `SearchInputGroup` 开头。
- 在组内，第一个控件是 `QuickFilter` 控件。 （此控件是用户输入搜索字符串的位置。）
- 第二个控件是名为 `NumberOfResults` 的 `FormStaticTextControl`。 （此控件是可选的。 如果包含，将显示找到的物料数。）
- 第三个控件是 `CommonButton` 控件，其名称以 `ClearButton` 开头。

下图显示了两个快速筛选器控件。 左边的快速筛选器有一个空的快速筛选器，结果数不可见。 右边的快速筛选器包含搜索字符串，显示结果数。

![带和不带搜索字符串的快速筛选器控件的示例。](media/pfe-styles-quick-filter.png "带和不带搜索字符串的快速筛选器控件的示例")

## <a name="center-align-elements-on-a-tab"></a>选项卡上的居中对齐元素

要在选项卡的中心对齐元素，组名称必须以 `TabContentGroup` 开头，并且组必须具有以下属性：

- **Width Mode：**`SizeToAvailable`
- **Height Mode：**`SizeToAvailable`

## <a name="align-a-grid-detail-part-and-quick-filter"></a>对齐网格、详细信息部件和快速筛选器

要排列自定义网格、详细信息部件和快速筛选器，使其与标准设计相似，请在将它们放在一起时记住以下几点：

- 如果网格具有快速筛选器，网格和快速筛选器都应位于名称以 `GridGroup` 开头的组内。
- 要将样式应用到详细信息部件，组名称必须以 `DetailInformationGroup` 开头。

下图显示了一个典型网格，其中在右侧包含了一个快速筛选器和一个详细信息部件。

![包含快速筛选器和详细信息部件的典型网格。](media/pfe-styles-align-grid.png "包含快速筛选器和详细信息部件的典型网格")

在 Visual Studio 中，网格、详细信息部件和快速筛选器可以使用如下图所示的结构创建。

![对齐网格、详细信息部件和快速筛选器的典型代码结构。](media/pfe-styles-header-code-structure2.png "对齐网格、详细信息部件和快速筛选器的典型代码结构")

## <a name="additional-resources"></a>其他资源

- [自定义生产车间执行界面](production-floor-execution-customize.md)
- [设计生产车间执行界面](production-floor-execution-tabs.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
