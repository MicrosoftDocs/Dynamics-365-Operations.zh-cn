---
title: 流程指南框架
description: 本主题为正在 X++ 中扩展我们的仓库移动流程的开发人员提供有关流程指南框架的信息。
author: MarkusFogelberg
ms.date: 11/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2018-4-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: ecf4bf884bca80cabb066ae43d38cd9c0e159216
ms.sourcegitcommit: 614d79cba238e466d445767a7d0a012e785a9861
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/19/2021
ms.locfileid: "7651940"
---
# <a name="process-guide-framework"></a>流程指南框架

[!include [banner](../includes/banner.md)]

本主题为正在 X++ 中扩展仓库移动流程的开发人员提供有关流程指南框架的信息。 由于流程被分解为小步骤，因此可扩展仓库移动流程。 每个步骤的业务逻辑和用户界面构建已被提取到各个类，这带来了可扩展性。

## <a name="overview-of-the-existing-design"></a>现有设计概述

仓库移动执行流通过单个自定义服务终结点公开。 请求以 XML 字符串的形式从移动应用到达，该字符串包含移动应用中显示的用户界面的元数据以及用户输入的值。

收到请求后，第一步是反序列化此 XML。 **WHSMobileAppServiceXMLTranslator** 类将 XML 转换为包含控件信息和会话信息的容器。

在此之后，容器中的信息用于推断用户正在处理的仓库流程或即将开始的仓库流程（由 **WHSWorkExecuteMode** 枚举表示），并相应地实例化 **WHSWorkExecuteDisplay** 的派生类。 将调用 **displayform()** 方法，之后它执行以下操作：

-   处理来自用户的数据（委托给 **WHSRFControlData** 类，但某些流程通过替代 **processControl()** 方法实现特定逻辑）。

-   执行业务逻辑。

-   增加此步骤。

-   构建表示新用户界面的容器（通常使用 **build…()** 方法）。

然后，此容器将返回到转换器，转换器随后对 XML 进行序列化，并将其作为响应发回移动设备。

以下序列图显示了执行流的概览。 请注意，此图更多的是一个示意图，不是实际代码的 1:1 表示形式。

![流程示意图。](media/schematic-overview.png) 

### <a name="reason-for-the-redesign"></a>重新设计的原因

上述设计为构建移动流中使用的流程提供了一个非常简单的框架。 但是，如上所示，**displayform()** 方法需要承担多个责任。 它确实将它们委托给其他方法和类，但是在没有具体的类职责的情况下，它在类之间以不一致的方式完成。 此外，随着支持的场景数量有机地增长，其中一些类会变得非常复杂。 更有趣的是，其中一些类/方法被替代，而且在多种模式下重用。 结果是具有较高循环复杂度的极长方法。 这些在过去造成了维护问题。 修复这些方法中的 bug 具有风险且易于再次出现。
例如，**WhsWorkExecuteDisplay** 类中的 **processWorkLine()** 方法从多个流程（基本上在执行工作执行的任何地方）引用。

为了使这些可扩展，其中一种选择是将 **displayForm** 方法拆分为更小的方法并引入可扩展点。 但是，由于场景矩阵的原因，合作伙伴编写扩展并验证再现会具有挑战性。 不仅如此，由于缺乏上述结构化的责任分配，代码会随着时间的推移以不可预测的方式不断增长，对构建质量扩展构成挑战。

因此，重新设计是可持续的选择，其目标是明确定义具有独立职责的类。 一个类应该有一个责任，一个更改的理由和一个扩展的理由。

## <a name="design-overview"></a>设计概述

在重新设计的框架中，核心策略围绕两个原则：将执行流划分为具有明确定义职责的单个组件，以及在每个组件中具有明确定义的扩展点。

新框架的名称为“ProcessGuide”。 这是因为这些类的目的是引导用户完成业务流程（与富客户端相反，富客户端是一种基于窗体的体验，其用户在如何与数据交互或执行任务的顺序方面具有更大的灵活性）。

> [!NOTE]
> 一个值得注意的细节是有意忽略了“WHS”前缀。 虽然移动流程最初是为了仓库而引入的，但随后它们已经跨越界限，支持各个生产和库存管理流程。 因此，在框架的名称中排除了仓库引用。

要确定组件，第一步是查看“生产开始”流程（**WhsWorkExecuteDisplayProdStart** 类）。 下面是此流程的示意图。

![示意流程的图像。](media/production-start-process-schematic.png)

看一下控制流，以下是所需的组件：

-   要在整个业务流程中拼结的控制器。
-   负责执行流程中的步骤的步骤。
-   处理步骤中数据的数据处理器。
-   负责构建步骤的用户界面的页面构建器。
-   负责步骤转换的导航代理。
-   负责执行业务流程的类。

在上面的流程图中，如果您从步骤 1 开始处理上一步的数据，然后以构建 UI 结束，那么数据将在下一步中继续处理。 这在连续的步骤之间引入了紧密耦合，因此，我们新的高级示意图将如下面这样：

![高级示意流程的图像。](media/high-level-schematic.png)

以下是重新设计的流程中的关键组件：

-   **ProcessGuideController** - 此类协调业务流程的整体执行。 它定义实例化步骤和导航代理的程序，它们随后构成流程执行，以及取消或退出流程的清理逻辑。

-   **ProcessGuideStep** - 此类表示业务流程中的一个步骤。 此类包含实例化页面构建器、操作和数据处理器的程序的定义，并负责以正确的顺序调用它们。

-   **ProcessGuideNavigationAgent** - 此类负责步骤之间的导航。 当一个步骤完成时，导航代理负责定义下一步并将上一步中可能需要传达的任何参数传递到下一个步骤。

-   **ProcessGuidePageBuilder** - 此类负责实例化用户界面。

-   **ProcessGuideAction** - 此类表示一个操作，向用户显示为一个按钮。

-   **ProcessGuideDataProcessor** - 此类负责处理字段中用户输入的数据。

## <a name="execution-flow"></a>执行流

执行流的起始点保持不变。 因此，请求仍通过相同的终结点到达，然后将 XML 反序列化到容器中。 此容器随后传递到 **getNextFormState()**。

有三个重要的类需要注意：

-  **ProcessGuideSessionState** – 此类包含会话状态信息 – 模式、传递、控制器和正在执行的步骤等。

-  **ProcessGuidePage** – 此类包含用户界面元数据的强类型表示形式。

-  **ProcessGuideRequest** – 此类包含以上两个类作为成员，是从移动设备收到的请求的强类型表示形式。

这些类使用容器信息创建（状态和用户输入的控制数据）。 这提供了一种类型安全的方式来访问和操作值。 与流程期间容器的重复访问相比，这将在可读性和性能方面带来好处。

会话状态信息用于实例化正确的 **ProcessGuideController** 类。 实例化后，将调用 **ProcessGuideController** 类中的 **createResponse()**。 此方法是流程指南逻辑的入口点，执行后将返回响应（在 **ProcessGuideResponse** 类中表示）。 然后，响应将转换回容器并退回旧逻辑，这随后会将其序列化为 XML 并将响应发送回移动设备。

接下来，控制器需要找到要执行的下一步。 如果这是新流程的开始，控制器将调用 **initialStep()** 获取流程中的第一步。 之后，将调用 **ProcessGuideStep** 中的 **execute()** 方法。 然后，此方法将实例化一个 **ProcessGuidePageBuilder** 类并调用 **buildPage()**，后者将随一个 **ProcessGuidePage** 对象一起返回，该对象是要呈现给用户的用户界面的虚拟表示形式。 然后，此步骤会将结果发送回控制器，控制器随后会保存当前会话状态，然后以 **ProcessGuideResponse** 类的形式将结果返回到 **getNextFormState()**。 之后，响应将转换回容器，随后序列化为 XML，然后将响应发回移动设备。

以下序列图说明了此控制流。 请注意，这是最常见的控制流，为解释设计进行了简化。

![简化的控制流。](media/control-flow.png)

当用户通过单击按钮（或扫描一个值 – 通常会触发默认操作）在移动设备上执行操作时 – 请求通过相同的路由到达 **ProcessGuideController** 类中的 **createResponse()** 方法。 不过，这一次，控制器从会话状态信息中知道用户处于哪个步骤。 因此，它实例化相应的 **ProcessGuideStep** 类并调用执行方法。 **ProcessGuideStep** 继而读取用户调用的操作名称，然后实例化相应的 **ProcessGuideAction** 类并调用 **execute()**。

**ProcessGuideAction** 类负责执行特定操作，但存在两个值得注意的例外。

第一个是 **ProcessGuideOKAction** 类。 此操作意味着用户想要确认并在流程中向前推进。 据此 - 此方法实际上会对 ProcessGuideStep 类执行回调，这意味着此步骤将调用 **ProcessGuideDataProcessor** 中的 **processData()**。 这将处理用户输入的数据，然后更新步骤的状态并将结果发送回控制器。 根据处理器的结果，此步骤将调用页面构建器来构建适当的用户界面或将步骤的状态设置为已完成。 这将反映在下面序列图的上半部分。

另一个例外是取消操作，它在 **ProcessGuideCancelResetProcessAction** 和 **ProcessGuideCancelExitProcessAction** 类中实现。 这些操作表示取消流程并返回流程开始或完全退出流程的意图。 与 **确定** 操作类似，这些操作也执行对步骤的回调，向 **ProcessGuideController** 发出意图信号。 然后，控制器执行必要的状态变量清理，并将控制移至流程的初始步骤或完全终止流程。

步骤完成后，如果步骤的状态设置为 **已完成**，控制器将实例化 **ProcessGuideNavigationAgent**，这将返回下一步的名称。 然后，控制器实例化此步骤并调用 **execute()** 方法 – 循环继续。 最常见的是，新步骤调用相应的 **ProcessGuidePageBuilder** 来构建用户界面，以将下一个屏幕呈现给用户，其之后将被发回。 下面序列图的下半部分描述了此流。

![序列图。](media/sequence-diagram.png)

## <a name="building-a-new-process-using-the-processguide-framework"></a>使用 ProcessGuide 框架构建新流程

解释控制流的最佳方法是使用应用程序中存在的示例 – 生产开始流程。

## <a name="overview-of-the-production-start-process"></a>生产开始流程概述

我们从了解此流程流开始。 在第一步中，系统会提示用户输入生产订单 ID。

![提示输入生产 ID。](media/production-id-prompt.png)

当用户输入生产订单 ID 时，将验证订单编号。 运行的一些验证基于订单所在仓库是否与用户登录的是同一仓库，以及订单的状态。 如果验证失败，将向用户显示错误消息。 如果验证成功，将向用户显示生产订单和物料的详细信息。

用户可以选择取消来返回到流程开始处，也可以单击 **确定** 进行确认。 在后一种情况下，生产订单设置为 **已开始** 状态，相应的日记帐将过帐，控制返回第一步，并向用户显示“工作已完成”消息。


## <a name="creating-the-controller"></a>创建控制器

构建业务流程的第一步是创建控制器类，从实现控制器默认行为的 **ProcessGuideController** 抽象类扩展而来。 新的类名称是 **ProdProcessGuideProductionStartController**，使用 **StartProdOrder** 的 **WHSWorkExecuteMode** 值修饰。 将使用与 **WHSWorkExecuteDisplay** 类中使用的相同的基于 **SysExtension** 的实例化，这将在用户为此模式执行菜单项时帮助实例化控制器。

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode::StartProdOrder)]
public class ProdProcessGuideProductionStartController extends ProcessGuideController
```

> [!NOTE]
> 此类的命名模式为 **\<FunctionalArea\>ProcessGuide\<Businessprocessname\>Controller**。 这是用于控制器类的模式，将扩展到其他类。


## <a name="building-the-first-step"></a>构建第一步

接下来，要定义第一步，您要创建 **ProdProcessGuidePromptProductionIdStep** 类，从 **ProcessGuideStep** 扩展。

实例化类的任务将被委托给一个步骤工厂，其由 **ProcessGuideController** 基类调用。 工厂的默认实现基于名称实例化步骤。 因此，要将 **ProdProcessGuidePromptProductionIdStep** 实例化为控制器中的第一步，您必须做两件事：

-   使用 **ProcessGuideStepName** 属性修饰 **ProdProcessGuidePromptProductionIdStep** 类。

    ```xpp
    [ProcessGuideStepName(classStr(ProdProcessGuidePromptProductionIdStep))] public class ProdProcessGuidePromptProductionIdStep extends ProcessGuideStep
    ```

-   在控制器类中，实现抽象方法 **initialStepName()** 以返回步骤名称。

    ```xpp
    protected final ProcessGuideStepName initialStepName()
    {
        return classStr(ProdProcessGuidePromptProductionIdStep);
    }
    ````   
    
> [!NOTE]
> **ProcessGuideStepName** 属性中的值不需要与上面显示的类名完全匹配。 但是，如果实现，则可以在使用类时在交叉引用周围实现一致性和类型安全。 建议使用此命名约定。
>
> 基于 **ProcessGuideStepName** 的步骤的实例化在 **ProcessGuideStepDefaultFactory** 类中实现。 在极少数情况下，您需要不同的策略来实例化步骤，您需要执行以下操作：
> -   创建一个继承自 **ProcessGuidStepAbstractFactory** 的新工厂类。
> -   或者，创建一个实现 **ProcessGuideIStepCreationParameters** 接口的新参数类，其中包含工厂需要的参数。
> -   在您的控制器类中，替代 **stepFactory()** 和 **stepCreationParameters()** 方法以返回上述工厂和参数。

下一步是实现 **ProdProcessGuidePromptProductionIdStep** 类的功能。 您需要实现用于构建用户界面、处理用户输入的数据以及确定步骤何时完成的逻辑。

### <a name="building-the-user-interface-for-the-first-step"></a>为第一步构建用户界面

用户界面使用从 **ProcessGuidePageBuilder** 抽象类继承的类构建。 对于此步骤，命名此类以表示其功能 – **ProdProcessGuidePromptProductionIdPageBuilder**。

类的实例化机制类似于从控制器实例化步骤的方式。 

-   使用 **ProcessGuidePageBuilderName** 属性修饰 **ProdProcessGuidePromptProductionIdPageBuilder** 类。

    ```xpp
    [ProcessGuidePageBuilderName(classStr(ProdProcessGuidePromptProductionIdPageBuilder))] public class ProdProcessGuidePromptProductionIdPageBuilder extends ProcessGuidePageBuilder
    ```

-   在 **ProdProcessGuidePromptProductionIdStep** 类中，实现抽象方法 **pageBuilderName()** 以返回此名称。

    ```xpp
    protected final ProcessGuidePageBuilderName pageBuilderName()
    {
        return classStr(ProdProcessGuidePromptProductionIdPageBuilder);
    }
    ```    

> [!TIP]
> 与步骤工厂类似，还有为页面构建器工厂实现的抽象工厂模式。 因此，在极少数情况下，您需要不同的策略来实例化页面构建器，您可以执行以下操作：
> - 创建一个继承自 **ProcessGuidePageBuilderAbstractFactory** 的新工厂类。
> - 或者，创建一个实现 **ProcessGuideIPageBuilderCreationParameters** 接口的新参数类，其中包含工厂需要的参数。
> - 在您的步骤类中，替代 **pageBuilderFactory()** 和 **pageBuilderCreationParameters()** 方法以返回上述工厂和参数。

要实现用户界面，您需要一个包含一个文本框的页面，用于输入生产订单 ID，以及一个 **确定** 按钮和一个 **取消** 按钮。 **取消** 按钮应退出流程。

要实现这一点，您需要替代 **ProdProcessGuidePromptProductionIdPageBuilder** 类中的两个方法：

-   使用 **addDataControls()** 方法添加文本框。

    ```xpp
    protected final void addDataControls(ProcessGuidePage _page)
    {
        _page.addTextBox(ProcessGuideDataTypeNames::ProdId, "@SYS4398", extendedTypeNum(ProdId));
    }
    ```   

-   使用 **addActionControls()** 方法添加 **确定** 和 **取消** 按钮。

    ```xpp
    protected final void addActionControls(ProcessGuidePage _page)
    {
        #ProcessGuideActionNames
        _page.addButton(step.createAction(#ActionOK), true);
        _page.addButton(step.createAction(#ActionCancelExitProcess));
    }
    ``` 

这将添加数据控件，后跟按钮。 但是，如果您想构建一个带有散布数据控件和按钮的屏幕，您可以替代 **addControls()** 方法以获得灵活性。

另一个需要考虑的场景是如何在验证失败的情况下重建页面，例如，如果用户输入了错误的生产订单 ID。 **ProcessGuidePageBuilder** 基类实现默认行为，其将重建用户界面、清除扫描值并添加带有错误消息的错误控件。 由于这是您要使用的默认行为，所以您无需添加任何代码来处理错误。

> [!TIP]
> 如果您想针对错误情况实现自定义 UI 行为，您可以替代一个或多个方法 **rebuildFromRequestPage()**、**isErrorState()** 和 **reuseRequestPageOnError()**。

### <a name="processing-the-user-entered-data-in-the-first-step"></a>处理第一步中用户输入的数据

数据的处理在 **ProcessGuideDataProcessorDefault** 类中完成，此类继而调用旧的 **WhsRfControlData** 类。 无需更改此默认行为，**WhsRfControlData** 已具有验证 **ProdId** 字段的逻辑，因此您无需编写任何逻辑来处理此问题。 如果验证逻辑需要扩展，请考虑使用基于 **WhsControl** 的扩展机制。

### <a name="determine-if-the-first-step-is-complete"></a>确定第一步是否完成

验证成功后，就可以将此步骤标记为已完成。 这在基类中完成，但是，您需要实现条件来确定步骤完成。 以下替代方法负责完成此任务。

```xpp
protected final boolean isComplete()
{
    WhsrfPassthrough pass = controller.parmSessionState().parmPass();
    ProdId prodId = pass.lookup(ProcessGuideDataTypeNames::ProdId);
        return (prodId != '');
}
```   

### <a name="step-two-view-order-details-and-confirm"></a>第二步：查看订单详细信息并确认

在流程的第二步中，用户会看到一个屏幕，其中包含有关订单的详细信息。 用户可以单击 **确定** 按钮确认开始生产订单，也可以单击 **取消** 返回流程开始处。 对于此示例，将此步骤命名为 **ProdProcessGuideConfirmProductionOrderStep**，将页面构建器类命名为 **ProdProcessGuideConfirmProductionOrderPageBuilder**。

ProdProcessGuideConfirmProductionOrderStep 类看起来像下面这样。

```xpp
[ProcessGuideStepName(classStr(ProdProcessGuideConfirmProductionOrderStep))]
public class ProdProcessGuideConfirmProductionOrderStep extends ProcessGuideStep
{
    protected final ProcessGuidePageBuilderName pageBuilderName()
    {
        return classStr(ProdProcessGuideConfirmProductionOrderPageBuilder);
     }
}
```     

由于用户没有在此处输入任何值，因此您无需替代 **isComplete()** 方法。 此步骤在用户单击 **确定** 时完成。

页面构建器类将替代 **addDataControls()** 方法来添加三个标签。 第一个标签显示生产订单 ID，第二个包含物料信息（如物料 ID、维度或描述），第三个包含数量和度量单位。

**addActionControls()** 然后被替代以添加 2 个按钮 – **确定** 按钮和取消流程并返回到流程开始处的 **取消** 按钮。

```xpp
/// <summary>
/// The <c>ProdProcessGuideConfirmProductionOrderPageBuilder</c> builds a page that allows the user to see details of a production order
/// and then confirm.
/// </summary>
[ProcessGuidePageBuilderName(classStr(ProdProcessGuideConfirmProductionOrderPageBuilder))]
public class ProdProcessGuideConfirmProductionOrderPageBuilder extends ProcessGuidePageBuilder
{
    protected void addDataControls(ProcessGuidePage _page)
    {
        WhsrfPassthrough pass = controller.parmSessionState().parmPass();
        ProdTable prodTable = ProdTable::find(pass.lookup(ProcessGuideDataTypeNames::ProdId));
        UnitOfMeasureSymbol inventUOM = InventTableModule::find(prodTable.ItemId, ModuleInventPurchSales::Invent).UnitId;
        
        _page.addLabel(ProcessGuideDataTypeNames::ProdIdLabelName, strFmt("@WAX1684", prodTable.ProdId), extendedTypeNum(ProdId));
        _page.addLabel(ProcessGuideDataTypeNames::ItemInfo, this.generateItemInfoForProdId(pass.lookup(ProcessGuideDataTypeNames::ProdId)), extendedTypeNum(WHSRFUndefinedDataType));
        _page.addLabel(ProcessGuideDataTypeNames::QtyLabelName, strFmt("@WAX1685", WHSWorkExecuteDisplay::num2StrDisplay(ProdUpdStartUp::proposalStartUpQty(prodTable.ProdId)), inventUOM), extendedTypeNum(WHSRFQuantityAndUOM));

        if (PdsGlobal::pdsIsCWItem(prodTable.ItemId))
        {
            _page.addLabel(ProcessGuideDataTypeNames::InventQtyLabelName, strFmt("@WAX1685", WHSWorkExecuteDisplay::num2StrDisplay(ProdUpdStartUp::pdsCWProposalStartupQty(prodTable.ProdId)), PdsCatchWeightItem::pdsCWUnitId(prodTable.ItemId)), extendedTypeNum(WHSRFQuantityAndUOM));
        }
    }

    protected void addActionControls(ProcessGuidePage _page)
    {
        #ProcessGuideActionNames
        _page.addButton(step.createAction(#ActionOK), true);
        _page.addButton(step.createAction(#ActionCancelResetProcess));
    }
```

> [!NOTE]
> 您可以使用应用程序资源管理器在本主题中找到 X++ 方法的相同源代码。 筛选类名称，然后右键单击类名称，选择 **查看代码**。

### <a name="step-3-start-the-production-order"></a>步骤 3：开始生产订单

第三步是执行开始生产订单的业务逻辑。 此步骤与前面的步骤有些不同，此步骤没有用户界面。 此步骤在用户在上一步中单击 **确定** 时静默执行。

**ProcessGuideStepWithoutPrompt** 抽象类实现此类步骤的默认行为。 因此，当前步骤应该扩展 **ProcessGuideStepWithoutPrompt** 类并替代 **doExecute()** 方法。

下面的代码示例显示了此类和 **doExecute()** 方法的实现。 此方法只是从会话状态中检索订单 ID 和用户 ID，并调用该方法来开始此生产订单。

```xpp
/// <summary>
/// The <c>ProdProcessGuideStartProductionOrderStep</c> represents a step that starts a production order.
/// </summary>
[ProcessGuideStepName(classStr(ProdProcessGuideStartProductionOrderStep))]
public class ProdProcessGuideStartProductionOrderStep extends ProcessGuideStepWithoutPrompt
{
    protected final void doExecute()
    {
        WhsrfPassthrough pass = controller.parmSessionState().parmPass();
        WHSUserId userId = pass.lookup(ProcessGuideDataTypeNames::UserId);
        ProdTable prodTable = ProdTable::find(pass.lookup(ProcessGuideDataTypeNames::ProdId));
        WhsWorkExecute workExecute = WhsWorkExecute::construct();
        workExecute.prodStartUp(prodTable.ProdId, ProdUpdStartUp::proposalStartUpQty(prodTable.ProdId), userId);

        this.addProcessCompletionMessage();

        super();
    }

}
```

如果出现异常，框架异常处理逻辑将确保流程回滚到上一步。

> [!NOTE]
> 对 **addProcessCompletionMessage()** 的调用将“工作已完成”消息添加到导航参数中。 下一步（假设其具有用户界面）将显示此消息。 基类处理此逻辑，实现此行为无需向流程类添加特定代码。


### <a name="building-the-navigation-through-the-steps"></a>构建步骤导航

**ProcessGuideController** 基类实例化 **ProcessGuideNavigationAgentDefault** 类，此类依赖于预定义的导航路由，即源和目标步骤的简单映射。 对于生产开始场景，由于没有条件分支，此实现已足够。 因此，您只需替代 **initializeNavigationRoute()** 方法来定义导航路由。

```xpp
    protected ProcessGuideNavigationRoute initializeNavigationRoute()
    {
        ProcessGuideNavigationRoute navigationRoute = new ProcessGuideNavigationRoute();
        navigationRoute.addFollowingStep(classStr(ProdProcessGuidePromptProductionIdStep), classStr(ProdProcessGuideConfirmProductionOrderStep));
        navigationRoute.addFollowingStep(classStr(ProdProcessGuideConfirmProductionOrderStep), classStr(ProdProcessGuideStartProductionOrderStep));
        navigationRoute.addFollowingStep(classStr(ProdProcessGuideStartProductionOrderStep), classStr(ProdProcessGuidePromptProductionIdStep));

        return navigationRoute;
    }
```

有些流程会存在条件分支（基于用户操作或任何其他条件）。 此类流程需要执行以下操作：

-   实现从 **ProcessGuideNavigationAgent** 类继承的特定导航代理。

-   实现从 **ProcessGuideNavigationAgentAbstractFactory** 类继承的特定导航代理工厂，包含根据当前步骤、会话状态、用户操作或其他逻辑实例化正确导航代理的逻辑。

-   或者，替代控制器类中的 **navigationAgentCreationParameters()** 以传递合适的参数。

-   替代控制器中的 **navigationAgentFactory()** 以实例化上面创建的导航代理工厂。

### <a name="action-classes"></a>操作类

操作类表示用户操作，因此本示例使用 **确定** 操作来显示操作是如何创建的。

```xpp
[ProcessGuideActionName(#ActionOK)]
public class ProcessGuideOKAction extends ProcessGuideAction
{
    public final str label()
    {
        return "@SYS5473";
     }
     protected final void doExecute()
     {
        step.executeOKAction();
      }
}
```    

此类必须实现 2 个抽象方法：

-   **label()**，返回要显示在与此操作关联的按钮控件中的标签。

-   **doExecute()**，执行操作。 如前所述，**确定** 按钮只是执行对步骤的回调。 但是，其他操作在此处可能有更复杂的逻辑。

这些操作使用基于 **ProcessGuideActionName** 属性的 **SysExtension** 框架实例化。 类似于页面构建器的实例化，步骤类将实现默认操作工厂，并可以替代它。 页面构建器将添加类似的按钮控件。

```xpp
_page.addButton(step.createAction(#ActionOK), true);
```

这样做时，它会要求步骤为传递的名称创建一个操作类，并将该操作与按钮联系。

### <a name="summary"></a>汇总

要总结本主题说明的所有内容，以下是整个流程所需代码的综合摘要：

1.  **ProdProcessGuideProductionStartController**

    1.  替代 **initialStepName()** 以提供第一步的名称。
    2.  替代 **initializeNavigationRoute()** 以构造导航映射。

        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuideProductionStartController</c> class is the controller class for the production order start process guide.
        /// </summary>
        [WHSWorkExecuteMode(WHSWorkExecuteMode::StartProdOrder)]
        public class ProdProcessGuideProductionStartController extends ProcessGuideController
        {
            protected ProcessGuideStepName initialStepName()
            {
                return classStr(ProdProcessGuidePromptProductionIdStep);
            }

            protected ProcessGuideNavigationRoute initializeNavigationRoute()
            {
                ProcessGuideNavigationRoute navigationRoute = new ProcessGuideNavigationRoute();
                navigationRoute.addFollowingStep(classStr(ProdProcessGuidePromptProductionIdStep), classStr(ProdProcessGuideConfirmProductionOrderStep));
                navigationRoute.addFollowingStep(classStr(ProdProcessGuideConfirmProductionOrderStep), classStr(ProdProcessGuideStartProductionOrderStep));
                navigationRoute.addFollowingStep(classStr(ProdProcessGuideStartProductionOrderStep), classStr(ProdProcessGuidePromptProductionIdStep));

                return navigationRoute;
            }

        }
        ```

2.  **ProdProcessGuidePromptProductionIdStep**

    1.  替代 **isComplete()** 以指定步骤何时被视为完成。
    2.  替代 **pageBuilderName()** 以指定要使用的页面构建器。

        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuidePromptProductionIdStep</c> represents a step that 
        /// that prompts the user for a production order id.
        /// </summary>
        [ProcessGuideStepName(classStr(ProdProcessGuidePromptProductionIdStep))]
        public class ProdProcessGuidePromptProductionIdStep extends ProcessGuideStep
        {
            protected boolean isComplete()
            {
                WhsrfPassthrough pass = controller.parmSessionState().parmPass();
                ProdId prodId = pass.lookup(ProcessGuideDataTypeNames::ProdId);

                return (prodId != '');
            }

            protected ProcessGuidePageBuilderName pageBuilderName()
            {
                return classStr(ProdProcessGuidePromptProductionIdPageBuilder);
            }

        }
        ```

3.  **ProdProcessGuidePromptProductionIdPageBuilder**

    1.  替代 **addDataControls()** 以添加 **Prod ID** 文本框。
    2.  替代 **addActionControls()** 以添加 **确定** 和 **取消** 按钮。
        
        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuidePromptProductionIdPageBuilder</c> class builds a page 
        /// that prompts the user for a production order id.
        /// </summary>
        [ProcessGuidePageBuilderName(classStr(ProdProcessGuidePromptProductionIdPageBuilder))]
        public class ProdProcessGuidePromptProductionIdPageBuilder extends ProcessGuidePageBuilder
        {
            protected void addDataControls(ProcessGuidePage _page)
            {
                _page.addTextBox(ProcessGuideDataTypeNames::ProdId, "@SYS4398", extendedTypeNum(ProdId));
            }

            protected void addActionControls(ProcessGuidePage _page)
            {
                #ProcessGuideActionNames
                _page.addButton(step.createAction(#ActionOK), true);
                _page.addButton(step.createAction(#ActionCancelExitProcess));
            }

        }
        ```

4.  **ProdProcessGuideConfirmProductionOrderStep**

    1.  替代 **pageBuilderName()** 以指定要使用的页面构建器。
        
        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuideConfirmProductionOrderStep</c> class represents the step for viewing production order
        /// details and confirming the same.
        /// </summary>
        [ProcessGuideStepName(classStr(ProdProcessGuideConfirmProductionOrderStep))]
        public class ProdProcessGuideConfirmProductionOrderStep extends ProcessGuideStep
        {    
            protected ProcessGuidePageBuilderName pageBuilderName()
            {
                return classStr(ProdProcessGuideConfirmProductionOrderPageBuilder);
            }

        }
        ```

3.  **ProdProcessGuideConfirmProductionOrderPageBuilder**

    1.  替代 **addDataControls()** 以添加订单、物料和数量信息标签。

    2.  替代 **addActionControls()** 以添加 **确定** 和 **取消** 按钮。
        
        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuideConfirmProductionOrderPageBuilder</c> builds a page that allows the user to see details of a production order
        /// and then confirm.
        /// </summary>
        [ProcessGuidePageBuilderName(classStr(ProdProcessGuideConfirmProductionOrderPageBuilder))]
        public class ProdProcessGuideConfirmProductionOrderPageBuilder extends ProcessGuidePageBuilder
        {
            protected void addDataControls(ProcessGuidePage _page)
            {
                WhsrfPassthrough pass = controller.parmSessionState().parmPass();
                ProdTable prodTable = ProdTable::find(pass.lookup(ProcessGuideDataTypeNames::ProdId));
                UnitOfMeasureSymbol inventUOM = InventTableModule::find(prodTable.ItemId, ModuleInventPurchSales::Invent).UnitId;

                _page.addLabel(ProcessGuideDataTypeNames::ProdIdLabelName, strFmt("@WAX1684", prodTable.ProdId), extendedTypeNum(ProdId));
                _page.addLabel(ProcessGuideDataTypeNames::ItemInfo, this.generateItemInfoForProdId(pass.lookup(ProcessGuideDataTypeNames::ProdId)), extendedTypeNum(WHSRFUndefinedDataType));
                _page.addLabel(ProcessGuideDataTypeNames::QtyLabelName, strFmt("@WAX1685", WHSWorkExecuteDisplay::num2StrDisplay(ProdUpdStartUp::proposalStartUpQty(prodTable.ProdId)), inventUOM), extendedTypeNum(WHSRFQuantityAndUOM));

                if (PdsGlobal::pdsIsCWItem(prodTable.ItemId))
                {
                    _page.addLabel(ProcessGuideDataTypeNames::InventQtyLabelName, strFmt("@WAX1685", WHSWorkExecuteDisplay::num2StrDisplay(ProdUpdStartUp::pdsCWProposalStartupQty(prodTable.ProdId)), PdsCatchWeightItem::pdsCWUnitId(prodTable.ItemId)), extendedTypeNum(WHSRFQuantityAndUOM));
                }
            }

            protected void addActionControls(ProcessGuidePage _page)
            {
                #ProcessGuideActionNames
                _page.addButton(step.createAction(#ActionOK), true);
                _page.addButton(step.createAction(#ActionCancelResetProcess));
            }

        ```

        > [!NOTE]
        > 用于生成物料信息标签的 **generateItemInfoForProdId()** 方法不在本主题中。 此方法查询几个表来获取物料 ID、描述和维度。 如果您想要更好地了解 **generateItemInfoForProdId()**，请了解一下源代码。

4.  **ProdProcessGuideStartProductionOrderStep**

    1.  替代 **doExecute()** 以执行生产开始流程并添加流程完成消息。

        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuideStartProductionOrderStep</c> represents a step that starts a production order.
        /// </summary>
        [ProcessGuideStepName(classStr(ProdProcessGuideStartProductionOrderStep))]
        public class ProdProcessGuideStartProductionOrderStep extends ProcessGuideStepWithoutPrompt
        {
            protected final void doExecute()
            {
                WhsrfPassthrough pass = controller.parmSessionState().parmPass();
                WHSUserId userId = pass.lookup(ProcessGuideDataTypeNames::UserId);
                ProdTable prodTable = ProdTable::find(pass.lookup(ProcessGuideDataTypeNames::ProdId));
                WhsWorkExecute workExecute = WhsWorkExecute::construct();
                workExecute.prodStartUp(prodTable.ProdId, ProdUpdStartUp::proposalStartUpQty(prodTable.ProdId), userId);

                this.addProcessCompletionMessage();

                super();
            }

        }
        ```

> [!NOTE]
> 请注意，很多常见模式（错误时重新生成 UI、设置流程完成消息、**确定** 和 **取消** 行为）已移至框架中 – 让应用程序开发人员不需要编写样板代码，这些代码既易出错，又存在跨流程行为不一致的风险。 不过，在场景需要偏离通用路径的情况下，应用程序开发人员可以选择替代合适的方法 – 但这是一种既明确又可跟踪的有意偏离。


### <a name="extending-a-business-process"></a>扩展业务流程

到目前为止，本主题重点介绍了如何使用 **ProcessGuide** 框架构建新流程。 在最后一节中，您将找到一些有关如何扩展此业务流程的示例。

### <a name="add-a-step-in-a-flow-using-processguidenavigationagentdefault"></a>在流中添加步骤（使用 ProcessGuideNavigationAgentDefault）

扩展位置：

-   流程的 **ProcessGuideController** 类的子级。

如何扩展：

-   扩展控制器类中的 **initializeNavigationRoute()** 方法，并调用 **ProcessGuideNavigationRoute** 类中的 **addFollowingStep()**。

### <a name="add-a-step-in-a-flow-using-custom-navigation-agent"></a>在流中添加步骤（使用自定义导航代理）

扩展位置：

-   **ProdProcessGuideNavigationAgentFactory/ProdProcessGuideNavigationAgent** 的子级。

如何扩展：

-   创建返回所需步骤名称的 **ProcessGuideNavigationAgent** 的新子类。

-   创建从有条件地返回上面创建的导航代理的 **ProcessGuideNavigationAgentFactory** 派生的新类。

-   扩展控制器类中的 **navigationAgentFactory()** 方法以返回上面创建的工厂。

### <a name="add-a-new-control-in-the-ui-of-an-existing-step"></a>在现有步骤的 UI 中添加新控件 

扩展位置：

-   步骤的 **ProdProcessGuidePageBuilder** 的子级。

如何扩展：

-   扩展 **addDataControls()** 方法并添加其他控件。

### <a name="complete-overhaul-of-the-user-interface-in-an-existing-step"></a>在现有步骤中完成对用户界面的彻底检查

扩展位置：

-   **ProdProcessGuideStep** 的子级。

如何扩展：

-   创建 **ProdProcessGuidePageBuilder** 类的新子类，并实现所需的用户界面。

-   扩展步骤类中的 **pageBuildeName()** 方法以返回上面创建的类的 **ProcessGuidePageBuilderNameAttribute**。

### <a name="alter-logic-when-a-step-is-considered-complete"></a>更改将步骤视为完成时的逻辑

扩展位置：

-   **ProdProcessGuideStep** 的子级。

如何扩展：

-   扩展 **isComplete()** 方法以构建其他逻辑。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]