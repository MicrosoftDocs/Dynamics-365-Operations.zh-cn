---
title: 设计新的 ER 解决方案打印 ZPL 标签
description: 本主题介绍如何设计新的电子报告 (ER) 解决方案来打印 Zebra 编程语言 (ZPL) 标签。
author: NickSelin
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2022-02-01
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: c1bedf1184b45741102000fa68c8d662c7383301
ms.sourcegitcommit: 2977e92a76211875421e608555311c363cfbdc25
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/16/2022
ms.locfileid: "8612340"
---
# <a name="design-a-new-er-solution-to-print-zpl-labels"></a>设计新的 ER 解决方案打印 ZPL 标签

[!include [banner](../includes/banner.md)]


本主题说明系统管理员、电子报告开发人员或电子报告功能顾问角色的用户如何配置[电子报告 (ER)](general-electronic-reporting.md) 框架的参数，设计新的 ER 解决方案所需的 ER [配置](general-electronic-reporting.md#Configuration)来访问仓库管理系统的数据，并以 Zebra 编程语言 (ZPL) II 格式生成自定义仓库位置标签。 这些步骤可以在 **USRT** 公司完成。

## <a name="business-scenario"></a>业务方案

您代表一家在 Microsoft Dynamics 365 Finance 中实施仓库管理的公司。 每个仓库位置都必须贴有包含条码的不干胶标签。 仓库工作人员将使用手持条码阅读器来扫描条码。

所有仓库位置都已在上线前活动的范围内标出。 但是，如果现有标签损坏或重新配置仓库货架，您还必须能够按需打印仓库位置标签。 使用最近发布的 ER 功能，您可以配置新的 ER 解决方案，让仓库主管将标签直接打印到热敏标签打印机。

## <a name="configure-the-er-framework"></a>配置 ER 框架

按照[配置电子报告框架](er-quick-start2-customize-report.md#ConfigureFramework)中的步骤设置最低限度的电子报告参数集。 在开始使用 ER 框架设计新 ER 解决方案之前，您必须完成此设置。

## <a name="design-a-domain-specific-data-model"></a>设计域特定数据模型

为仓库管理域创建一个包含[数据模型](er-overview-components.md#data-model-component)组件的新 ER 配置。 此数据模型将在以后您设计 ER 格式以生成仓库位置标签时用作数据源。

### <a name="import-a-data-model-configuration"></a>导入数据模型配置

按照以下步骤从 Microsoft 提供的 XML 文件导入所需的数据模型。 或者，您可以创建自己的数据模型，如下一节所述。

1. 下载 [Warehouse model.version.1.xml](https://download.microsoft.com/download/9/f/1/9f136e9b-bf5f-403a-b089-a2b2ed1da2ba/Warehouse-model.version.1.xml) 文件，并将其保存到本地计算机。
2. 转到 **组织管理** \> **工作区** \> **电子申报**。
3. 在 **电子报告** 工作区中，选择 **报告配置**。
4. 在 **配置** 页上的操作窗格中，选择 **交换** \> **从 XML 文件加载**。
5. 选择 **浏览**，然后找到并选择 **Warehouse model.version.1.xml** 文件。
6. 选择 **确定** 导入配置。

![“配置”页面上导入的 ER 数据模型配置。](./media/er-design-zpl-labels-imported-model.png)

### <a name="create-a-data-model-configuration"></a>创建数据模型配置

您可以从头开始创建数据模型，而不是导入 Microsoft 提供的数据模型文件。 有关显示如何完成此任务的示例，请参阅[创建新数据模型配置](er-quick-start1-new-solution.md#DesignDataModel)。

### <a name="review-the-data-model"></a>查看数据模型

您可以在 **数据模型设计器** 页面上查看已配置数据模型的可编辑版本。

![数据模型设计器页面上 ER 数据模型的结构。](./media/er-design-zpl-labels-model.png)

## <a name="design-a-model-mapping-for-the-configured-data-model"></a>为配置的数据模型设计模型映射

作为电子报告开发人员角色的用户，您必须为仓库数据模型创建一个新的 ER 配置，其中包含[模型映射](er-overview-components.md#model-mapping-component)组件。 此组件实现为 Dynamics 365 Finance 配置的数据模型，并且特定于该应用。 您必须配置此组件来指定将用于在运行时使用应用程序数据填充配置的数据模型的应用程序对象。 要完成此任务，您必须了解仓库管理业务域的数据结构在 Finance 中是如何实现的。

### <a name="import-a-model-mapping-configuration"></a>导入模型映射配置

按照以下步骤从 Microsoft 提供的 XML 文件导入所需的模型映射。 或者，您可以创建自己的模型映射，如下一节所述。

1. 下载 [Warehouse model mapping.version.1.1.xml](https://download.microsoft.com/download/1/c/c/1cc94d28-3d90-4ffd-a118-77d6c322904f/Warehouse-model-mapping.version.1.1.xml) 文件，并将其保存到本地计算机。
2. 转到 **组织管理** \> **工作区** \> **电子申报**。
3. 在 **电子报告** 工作区中，选择 **报告配置**。
4. 在 **配置** 页上的操作窗格中，选择 **交换** \> **从 XML 文件加载**。
5. 选择 **浏览**，然后找到并选择 **Warehouse model mapping.version.1.1.xml** 文件。
6. 选择 **确定** 导入配置。

![“配置”页面上导入的 ER 模型映射配置。](./media/er-design-zpl-labels-imported-mapping.png)

### <a name="create-a-model-mapping-configuration"></a>创建模型映射配置

您可以从头开始创建模型映射，而不是导入 Microsoft 提供的模型映射文件。 有关显示如何完成此任务的示例，请参阅[创建新模型映射配置](er-quick-start1-new-solution.md#CreateModelMapping)。

### <a name="review-the-model-mapping"></a>查看模型映射

您可以在 **模型映射设计器** 页面上查看已配置模型映射的可编辑版本。

![模型映射设计器页面上 ER 模型映射的结构。](./media/er-design-zpl-labels-mapping.png)

## <a name="design-a-format"></a>设计格式

作为电子报告功能顾问角色的用户，您必须创建一个新的 ER 配置，其中包含[格式](er-overview-components.md#format-component)组件。 要配置此组件，您将使用 ZPL II 代码来指定仓库位置标签的布局。

### <a name="import-a-format-configuration"></a>导入格式配置

按照以下步骤从 Microsoft 提供的 XML 文件导入所需的格式。 或者，您可以创建自己的格式，如下一节所述。

1. 下载 [Warehouse location labels.version.1.1.xml](https://download.microsoft.com/download/5/7/5/5758b551-69a5-45bd-a2b2-21c3db73a6fc/Warehouse-location-labels.version.1.1.xml) 文件，并将其保存到本地计算机。
2. 转到 **组织管理** \> **工作区** \> **电子申报**。
3. 在 **电子报告** 工作区中，选择 **报告配置**。
4. 在 **配置** 页上的操作窗格中，选择 **交换** \> **从 XML 文件加载**。
5. 选择 **浏览**，然后找到并选择 **Warehouse location labels.version.1.1.xml** 文件。
6. 选择 **确定** 导入配置。

![“配置”页面上导入的 ER 格式配置。](./media/er-design-zpl-labels-imported-format.png)

### <a name="create-a-format-configuration"></a>创建格式配置

您可以从头开始创建格式，而不是导入 Microsoft 提供的格式文件。 有关显示如何完成此任务的示例，请参阅[创建新格式配置](er-quick-start1-new-solution.md#FormatCreate)。

### <a name="review-the-format"></a>查看格式

您可以在 **格式设计器** 页面上查看已配置格式的可编辑版本。

![格式设计器页面上 ER 格式的结构。](./media/er-design-zpl-labels-format.png)

此格式的 `model.Location.Label` 数据源配置为生成包含以下信息的标签：

- 文本形式的仓库标题
- 条码形式的仓库标题
- 位置标题
- 校验位

在数据源的 **公式设计器** 页面上，用于生成标签的 ER 公式包含一个 `CONCATENATE` 函数，该函数将信息组合到所需的布局中。

![公式设计器页面上数据源的公式。](./media/er-design-zpl-labels-review-formula.png)

> [!TIP]
> 标签布局经过设计，以使位置标题和校验位在标签的中心对齐。 但是，ZPL II 不支持条码在中心对齐。 因此，`model.Location.Warehouse.Alignment` 数据源的公式用于在标签中心对齐条码。 此公式根据仓库标题中的字符数计算条码的左偏移量。

## <a name="prepare-your-environment-for-previewing-generated-labels"></a>准备您的环境以预览生成的标签

以下示例为 ZPL 标签使用打印机模拟器应用程序在屏幕上显示生成标签的预览。 请按照以下步骤启用此选项。

1. 为 **仓库位置标签** ER 格式添加[打印机](er-destination-type-print.md) ER 目标，并将其配置为将生成的标签从 Finance 发送到[文档路线选择代理 (DRA)](install-document-routing-agent.md)。
2. 安装和配置 DRA 以将生成的标签从 Finance 传递到可从当前工作站访问的本地打印机。
3. 为当前工作站添加本地打印机，并将其配置为将生成的标签从 DRA 传递到打印机模拟器应用程序。
4. 作为 Chrome Web 浏览器的扩展安装打印机模拟器应用程序，并将其配置为将生成的标签从本地打印机传递到 Web 服务，该服务将呈现生成的标签并将它们返回到打印机模拟器进行预览。

<table>
<tbody>
<tr align="center">
<td>
<p>Finance</p>
<p>ER 报表</p>
<p>打印机目标</p>
</td>
<td><img src="./media/er-design-zpl-labels-flow1.png" alt="Data flow direction: from Finance to the DRA."></td>
<td>文档路线选择代理</td>
<td><img src="./media/er-design-zpl-labels-flow1.png" alt="Data flow direction: from the DRA to a local printer."></td>
<td>本地打印机</td>
<td><img src="./media/er-design-zpl-labels-flow1.png" alt="Data flow direction: from a local printer to a printer emulator."></td>
<td>打印机模拟器</td>
<td><img src="./media/er-design-zpl-labels-flow2.png" alt="Data flow direction: from a printer emulator to a rendering web service and then back to the printer emulator."></td>
<td>呈现 Web 服务</td>
</td>
</tr>
</tbody>
</table>

### <a name="install-and-configure-a-printer-emulator-application"></a>安装和配置打印机模拟器应用程序

将 ZPL 呈现引擎的打印机模拟器应用程序添加到您的 Chrome Web 浏览器。 此示例使用基于 [Labelary ZPL Web 服务](http://labelary.com/service.html)的 [Zpl 打印机](https://chrome.google.com/webstore/detail/zpl-printer/phoidlklenidapnijkabnfdgmadlcmjo)模拟器。 打印机模拟器应用程序会将生成的 ZPL 格式的标签从本地打印机传递到 Web 服务，然后将标签作为 PDF 或 PNG 文件返回以供预览。

1. 在 Chrome Web 商店中，找到并选择您要使用的打印机模拟器应用程序。 然后选择 **添加到 Chrome** 将其添加到 Chrome Web 浏览器。

    ![从 Chrome Web 商店将打印机模拟器应用程序添加到 Chrome Web 浏览器。](./media/er-design-zpl-labels-add-app.png)

2. 选择 **启动应用**，从 Chrome Web 浏览器运行打印机模拟器应用程序。

    ![从 Chrome Web 浏览器运行打印机模拟器应用程序。](./media/er-design-zpl-labels-run-app.png)

3. 配置正在运行的应用程序：

    1. 关闭应用程序。
    2. 在打印机设置中，将主机设置为 **127.0.0.1**。
    3. 将端口设置为 **9100**。

        ![配置打印机模拟器应用程序。](./media/er-design-zpl-labels-configure-app.png)

    4. 重新打开应用程序。 您应该会收到一条消息，指出打印机已在指定的主机和端口上启动。

        ![打印机模拟器应用程序已重新打开。](./media/er-design-zpl-labels-turn-on-app.png)

> [!NOTE]
> 由于本示例中使用的打印机模拟器应用程序依赖于 Web 服务来呈现标签，因此请确保您的安全设置允许您与服务进行通信。 否则，应用程序不会收到呈现的标签，这些标签将不能提供预览。

### <a name="add-and-configure-a-local-printer"></a>添加和配置本地打印机

[添加新的本地打印机](https://support.microsoft.com/windows/install-a-printer-in-windows-10-cc0724cf-793e-3542-d1ff-727e4978638b)，当前设备可以使用它将生成的标签从 DRA 传递到打印机模拟器应用程序。

1. 在 Windows 中，选择 **开始** \> **设置** \> **设备** \> **打印机和扫描仪**。
2. 选择 **打印机和扫描仪设置**。
3. 对于 **添加打印机或扫描仪**，**添加设备**。
4. 如果显示 **我需要的打印机不在列表中**，选择 **手动添加**。
5. 在 **按其他选项查找打印机** 字段中，选择 **通过手动设置添加本地打印机或网络打印机**。
6. 在 **选择打印机端口** 字段中，选择 **创建新端口**，然后按照以下步骤操作：

    1. 在 **端口类型** 字段中，选择 **标准 TCP/IP 端口**。
    2. 在 **主机名或 IP 地址** 字段中，输入 **127.0.0.1**。
    3. 在 **端口名称** 字段中，输入 **ZPL**。
    4. 等待 **检测 TCP/IP 端口** 操作完成。
    5. 在 **设备类型** 字段中，选择 **自定义**，然后选择 **设置**。
    6. 确保指定了以下端口设置：

        - **端口名称：** ZPL
        - **打印机名称或 IP 地址：** 127.0.0.1
        - **协议：** 原始
        - **端口号：** 9100

7. 在 **安装打印机驱动程序** 字段中，选择 **通用/仅文本**。
8. 在 **打印机名称** 字段中，输入 **ZebraPrinter**。

![为当前设备添加本地打印机。](./media/er-design-zpl-labels-configure-printer.png)

### <a name="install-and-configure-the-dra"></a>安装和配置 DRA

准备 DRA 以将生成的标签从 Finance 传递到配置的本地打印机。

1. [安装 DRA](install-document-routing-agent.md#install-the-document-routing-agent)。
2. [配置 DRA](install-document-routing-agent.md#configure-the-document-routing-agent)。
3. 在 DRA 中[注册本地打印机](install-document-routing-agent.md#register-network-printers)。
4. 在 Finance 环境中[激活本地打印机](install-document-routing-agent.md#administer-network-printers)。

![准备 DRA 以打印生成的标签。](./media/er-design-zpl-labels-configure-dra.png)

### <a name="configure-the-er-destination"></a>配置 ER 目标

准备 ER 目标以将生成的标签从 Finance 传递到 DRA。

1. 转到 **组织管理** \> **电子报告** \> **电子报告目标**。
2. 在 **电子报告目标** 页面的操作窗格上，选择 **新建**。
3. 在 **引用** 字段中，选择 **仓库位置标签**。
4. 在 **文件目标** 快速选项卡上，选择 **新建**。
5. 在 **名称** 字段中，输入 **标签**。
6. 在 **文件组件名称** 字段中，选择 **报表**。
7. 选择 **设置**。
8. 在 **目标设置** 对话框的 **打印机** 选项卡上，将 **已启用** 选项设置为 **是**。
9. 在 **打印机名称** 字段中，选择 **ZebraPrinter**。
10. 在 **文档路线类型** 字段中，选择 **ZPL**。
11. 选择 **确定**。

![在电子报告目标页面上为仓库位置标签格式配置 ER 目标。](./media/er-design-zpl-labels-configure-destination.png)

## <a name="review-warehouse-locations"></a>查看仓库位置

1. 转到 **仓库管理** \> **设置** \> **仓库** \> **位置**。
2. 在 **位置** 页面上，进行筛选以仅查看在 **校验位** 字段中具有值的位置。

![在“位置”页面上查看仓库位置。](./media/er-design-zpl-labels-review-locations.png)

## <a name="print-warehouse-location-labels"></a>打印仓库位置标签

1. 转到 **组织管理** \> **电子申报** \> **配置**。
2. 在 **配置** 页面，在配置树中，展开 **仓库模型**，然后选择 **仓库位置标签**。
3. 在操作窗格上，选择 **运行**。
4. 在 **电子报表参数** 对话框的 **要包括的记录** 选项卡上，选择 **筛选器**。
5. 在 **范围** 选项卡上，找到 **表** 字段设置为 **位置**、**字段** 字段设置为 **位置** 的行。 在 **条件** 字段中，输入 **LPEnabled**。
6. 选择 **确定**。
7. 选择 **确定**。 将生成一个标签，显示在打印机模拟器应用程序的预览页面上。

![在 Zpl 打印机模拟器应用程序的预览页面上查看生成的标签。](./media/er-design-zpl-labels-preview-label.png)

## <a name="modify-the-layout-of-a-label"></a>修改标签的布局

您可以更改仓库位置标签的当前布局。 以下示例显示如何更改布局以使生成的标签包含位置配置文件 ID。

1. 转到 **组织管理** \> **电子申报** \> **配置**。
2. 将 **将目标用于草稿状态** [ER 用户参数](electronic-reporting-destinations.md#applicability)设置为 **是**。
3. 在 **配置** 页面，在配置树中，展开 **仓库模型**，然后选择 **仓库位置标签**。
4. 选择 **设计器**。
5. 在 **格式设计器** 页上的 **映射** 选项卡上，选择 `model.Location.Label` 数据源。
6. 在 **数据源属性** 对话框中，选择 **编辑** \> **编辑公式**。
7. 在 **公式设计器** 页面上，在 **公式** 字段中，查看用于生成标签的 ER 公式。

    ```vb
    CONCATENATE(
    "^XA",CrLf,
    "^CF0,30,30^FO0,30^FB800,1,0,C,0^FD",Warehouse,"\&^FS",CrLf,
    "^BY2,2,50^FT",@.Warehouse.Alignment,",126^BCN,,N,N,N,A^FD",Warehouse,"\&^FS",CrLf,
    "^FO0,150^FB800,1,0,C,0^FD",@.Name,"\&^FS",CrLf,
    "^CF0,20,20^FO0,200^FB800,1,0,C,0^FD",@.CheckDigits,"\&^FS",CrLf,
    "^XZ")
    ```

8. 更新公式以将位置配置文件 ID 添加到生成的标签。

    ```vb
    CONCATENATE(
    "^XA",CrLf,
    "^CF0,30,30^FO0,30^FB800,1,0,C,0^FD",Warehouse,"\&^FS",CrLf,
    "^BY2,2,50^FT",@.Warehouse.Alignment,",126^BCN,,N,N,N,A^FD",Warehouse,"\&^FS",CrLf,
    "^FO0,150^FB800,1,0,C,0^FD",@.Name,"\&^FS",CrLf,
    "^CF0,20,20^FO0,200^FB800,1,0,C,0^FD",@.CheckDigits,"\&^FS",CrLf,
    "^CF0,40,40^FO0,240^FB800,1,0,C,0^FD",@.ProfileID,"\&^FS",CrLf,
    "^XZ")
    ```

9. 选择 **保存**。
10. 选择 **确定**。
11. 在操作窗格上，选择 **运行**。
12. 在 **电子报表参数** 对话框的 **要包括的记录** 选项卡上，选择 **筛选器**。
13. 在 **范围** 选项卡上，找到 **表** 字段设置为 **位置**、**字段** 字段设置为 **位置** 的行。 在 **条件** 字段中，输入 **Bay**。
14. 选择 **确定**。
15. 选择 **确定**。 将生成一个标签，显示在打印机模拟器应用程序的预览页面上。

![在 Zpl 打印机模拟器应用程序的预览页面上查看包含位置配置文件 ID 的生成标签。](./media/er-design-zpl-labels-preview-label2.png)

## <a name="encoding"></a>编码

> [!NOTE]
> 您必须同步可编辑 ER 格式的 **Common\\File** 组件的编码设置和设计后的标签的适当设置。 **Common\\File** 组件的 **[Encoding](er-suppress-bom-characters.md)** 字段的值不应与用于控制标签编码的 ZPL 命令相矛盾（例如，`^CI` 命令）。 ER 不验证是否同步了这些设置。

## <a name="additional-resources"></a>其他资源

[打印机目标](er-destination-type-print.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
