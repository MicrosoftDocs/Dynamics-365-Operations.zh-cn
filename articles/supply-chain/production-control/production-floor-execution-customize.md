---
title: 自定义生产车间执行界面
description: 本主题说明如何为生产车间执行界面扩展当前窗体或创建新窗体和按钮。
author: johanhoffmann
ms.date: 05/04/2022
ms.topic: article
ms.search.form: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-11-08
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: ad5037442f27a5068b38613655591f1298808eac
ms.sourcegitcommit: 28537b32dbcdefb1359a90adc6781b73a2fd195e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/05/2022
ms.locfileid: "8712934"
---
# <a name="customize-the-production-floor-execution-interface"></a>自定义生产车间执行界面

[!include [banner](../includes/banner.md)]

开发人员可以为生产车间执行界面扩展当前窗体或创建自己的窗体和按钮。 为这些新元素添加代码后，管理员或车间经理可以使用标准配置控制轻松地将它们添加到界面中。

例如，如果主窗体中需要新列，以下是一些可能的解决方案：

- 扩展 `JmgProductionFloorExecutionMainGrid` 窗体，添加所需的字段。
- 创建新窗体，并将其添加为新的主视图（选项卡）。

## <a name="add-a-new-button-action"></a>添加新按钮（操作）

要添加新按钮（操作），请按照这些步骤创建一个实现自定义操作的类。

1. 创建一个名为 `<ExtensionPrefix>_JmgProductionFloorExecution<ActionName>Action` 的新类，其中：

    - `<ExtensionPrefix>` 唯一标识您的解决方案，通常使用您的公司名称。
    - `<ActionName>` 是类的唯一名称。 它通常标识操作的类型。

1. 新类必须扩展 `JmgProductionFloorExecutionAction` 类。
1. 替代所有必要的方法。

例如，请看一下以下类的代码：

- `JmgProductionFloorExecutionBreakAction` – 不需要任何记录的简单操作的类。
- `JmgProductionFloorExecutionReportFeedbackAction` – 提供更复杂功能的类。

完成后，新按钮（操作）将自动列在 Microsoft Dynamics 365 Supply Chain Management 的 **设计选项卡** 页面上。 在那里，您（或者管理员或车间经理）可以轻松地将其添加到主要或辅助工具栏中，就像您可以添加标准按钮一样。 有关说明，请参阅[设计生产车间执行界面](production-floor-execution-tabs.md)。

## <a name="add-a-new-main-view"></a>添加新的主视图

1. 创建一个具有所需元素和功能的新窗体。 请注意，此窗体是新窗体，不是扩展。 将窗体命名为 `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>`，其中：

    - `<ExtensionPrefix>` 唯一标识您的解决方案，通常使用您的公司名称。
    - `<FormName>` 是窗体的唯一名称。

1. 创建一个名为 `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>` 的菜单项。
1. 创建一个名为 `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>_Extension` 的扩展，其中通过将新菜单项添加到列表来扩展 `getMainMenuItemsList` 方法。 以下代码显示了一个示例。

    ```xpp
    [ExtensionOf(classStr(JmgProductionFloorExecutionMenuItemProvider))]
    public final class <ExtensionPrefix>_JmgProductionFloorExecutionForm<FormName>_Extension{
        static public List getMainMenuItemsList()
        {
            List menuItemList = next getMainMenuItemsList();
            menuItemList.addEnd(menuItemDisplayStr(<ExtensionPrefix>_JmgProductionFloorExecutionForm<FormName>));
            return menuItemList;
        }
    ```

完成后，新的主视图将自动列在 Supply Chain Management 中 **设计选项卡** 页面上的 **主视图** 组合框中。 在那里，您（或者管理员或车间经理）可以轻松地将其添加到新的或现有选项卡中，就像您可以添加标准的主视图一样。 有关说明，请参阅[设计生产车间执行界面](production-floor-execution-tabs.md)。

## <a name="add-a-details-view"></a>添加详细信息视图

1. 创建一个具有所需元素和功能的新窗体。 请注意，此窗体是新的，不是扩展。 将窗体命名为 `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>Detail`，其中： 

    - `<ExtensionPrefix>` 唯一标识您的解决方案，通常使用您的公司名称。
    - `<FormName>` 是窗体的唯一名称。

1. 创建一个名为 `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>Detail` 的菜单项。
1. 创建一个名为 `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>_Extension` 的扩展，其中通过将新菜单项添加到列表来扩展 `getDetailsMenuItemList` 方法。

完成后，新的详细信息视图将自动列在 Supply Chain Management 中 **设计选项卡** 页面上的 **详细信息视图** 组合框中。 在那里，您（或者管理员或车间经理）可以轻松地将其添加到新的或现有选项卡中，就像您可以添加标准详细信息视图一样。 有关说明，请参阅[设计生产车间执行界面](production-floor-execution-tabs.md)。

## <a name="add-a-numeric-keypad-to-a-form-or-dialog"></a>在窗体或对话中添加数字键盘

下面的示例显示了如何在窗体中添加数字键盘。

1. 每个窗体包含的数字键盘控制器的数量必须等于该窗体中数字键盘的数量。

    ```xpp
    private JmgProductionFloorExecutionNumpadController   numpadController1;
    private JmgProductionFloorExecutionNumpadController   numpadController2;
    private JmgProductionFloorExecutionNumpadController   numpadController3;
    ```

1. 设置每个数字键盘控制器的行为，并将每个数字键盘控制器连接到一个数字键盘窗体部件。

    ```xpp
    /// <summary>
    /// Initializes all numpad controllers, defines their behavior and connects them with numpad form parts.
    /// </summary>
    public void initializeNumpadController()
    {
        numpadController1 = new JmgProductionFloorExecutionNumpadController();
        numpadController1.getValueFromNumpadDelegate += eventhandler(this.setQuanityValueFromNumpad_1);
        QuantityNumpad1.getPartFormRun().setNumpadController(numpadController1);
    
        numpadController2 = new JmgProductionFloorExecutionNumpadController();
        numpadController2.parmNumpadEnabled(false);
        numpadController2.parmNumpadValue(333.56);
        numpadController2.getValueFromNumpadDelegate += eventhandler(this.setQuanityValueFromNumpad_2);
        QuantityNumpad2.getPartFormRun().setNumpadController(numpadController2);
    }
    ```

## <a name="use-a-numeric-keypad-as-a-pop-up-dialog"></a>作为弹出对话使用数字键盘

以下示例显示了一种为弹出对话设置数字键盘控制器的方法。

```xpp
private void setupNumpadController()
{
    numpadController = new JmgProductionFloorExecutionNumpadController();
    numpadController.parmShouldNumpadShowOkCancelButtons(true);
    numpadController.setNumpadValueToParentFormDelegate += eventhandler(this.setQtyValueFromNumpad);
}
```

以下示例显示了一种调用数字键盘弹出对话的方法。

```xpp
Args args = new Args();
args.name(formstr(JmgProductionFloorExecutionNumpad));
args.menuItemName(menuItemDisplayStr(JmgProductionFloorExecutionNumpad));
args.caller(element);
Object formRun = classfactory.formRunClass(args);
formRun.init();
formRun.setNumpadController(numpadController);
numpadController.setValueToNumpad(333.56);
formRun.run();
```

## <a name="add-a-date-and-time-controls-to-a-form-or-dialog"></a>向窗体或对话框添加日期和时间控件

此部分介绍如何将日期和时间控件添加到窗体或对话框。 触摸友好的日期和时间控件使工作人员能够指定日期和时间。 以下屏幕截图显示了控件通常在页面上的显示方式。 时间控件提供 12 小时和 24 小时两种版本；显示的版本将遵循为运行界面所使用的用户帐户设置的首选项。

![日期控件示例。](media/pfe-customize-date-control.png "日期控件示例")

![12 小时时钟的时间控件示例。](media/pfe-customize-time-control-12h.png "12 小时时钟的时间控件示例")

![24 小时时钟的时间控件示例。](media/pfe-customize-time-control-24h.png "24 小时时钟的时间控件示例")

以下过程显示了一个如何将日期和时间控件添加到窗体的示例。

1. 为窗体应包含的每个日期和时间控件将控制器添加到窗体。 （控制器的数量必须等于窗体中的日期和时间控件数。）

    ```xpp
    private JmgProductionFloorExecutionDateTimeController  dateFromController; 
    private JmgProductionFloorExecutionDateTimeController  dateToController; 
    private JmgProductionFloorExecutionDateTimeController  timeFromController; 
    private JmgProductionFloorExecutionDateTimeController  timeToController;
    ```

1. 声明所需的变量（`utcdatetime` 类型）。

    ```xpp
    private utcdatetime fromDateTime;
    private utcdatetime toDateTime;
    ```

1. 创建日期/时间将由日期/时间控件进行更新的方法。 以下示例显示了一种这样的方法。

    ```xpp
    private void setFromDateTime(utcdatetime _value)
        {
            fromDateTime = _value;
        }
    ```

1. 设置每个日期时间控制器的行为，并将每个控制器连接到一个窗体部件。 以下示例显示了如何为开始日期和开始时间控件设置数据。 您可以为结束日期和结束时间控件添加类似的代码（未显示）。

    ```xpp
    /// <summary>
    /// Initializes all date and time controllers, defines their behavior, and connects them with the form parts.
    /// </summary>
    private void initializeDateControlControllers()
    {
        dateFromController = new JmgProductionFloorExecutionDateTimeController();
        dateFromController.setDateControlValueToCallerFormDelegate += eventhandler(this.setFromDateTime);
        dateFromController.parmDateTimeValue(fromDateTime);
    
        timeFromController = new JmgProductionFloorExecutionDateTimeController();
        timeFromController.setDateControlValueToCallerFormDelegate += eventhandler(this.setFromDateTime);
        timeFromController.parmDateTimeValue(fromDateTime);
        
        DateFromFormPart.getPartFormRun().setDateControlController(dateFromController, timeFromController);
        TimeFromFormPart.getPartFormRun().setTimeControlController(timeFromController, dateFromController);
        
        ...

    }
    ```

    如果您只需要一个日期控件，则可以跳过时间控件设置，而只需设置日期控件，如下例所示：

    ```xpp
    {
        dateFromController = new JmgProductionFloorExecutionDateTimeController();
        dateFromController.setDateControlValueToCallerFormDelegate += eventhandler(this.setFromDateTime);
        dateFromController.parmDateTimeValue(fromDateTime);
    
        DateFromFormPart.getPartFormRun().setDateControlController(dateFromController, null);
    }
    ```

## <a name="additional-resources"></a>其他资源

- [设计生产车间执行界面的样式](production-floor-execution-styles.md)
- [设计生产车间执行界面](production-floor-execution-tabs.md)
