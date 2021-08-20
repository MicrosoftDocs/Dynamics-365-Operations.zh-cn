---
title: 重新打印和取消波次标签
description: 本主题说明如何取消和重新打印现有波次标签。
author: perlynne
ms.date: 07/09/2020
ms.topic: article
ms.search.form: WHSWaveLabel, WHSWaveLabelTemplate, WHSWaveLabelLayoutRow, WHSWaveTableListPage, WHSWorkException, WHSMobileDisplayWaveLabelListLookup, WHSWaveLabelLayout, WHSWaveLabelType, WHSWaveLabelTemplateGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-07-09
ms.dyn365.ops.version: 10.0.2
ms.openlocfilehash: c07bb53787ba49e4e6010802fc8c9b43ea6b2d6b3bec49096efd9832140d4d9e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6736495"
---
# <a name="reprint-and-void-wave-labels"></a>重新打印和取消波次标签

[!include [banner](../includes/banner.md)]

本主题说明如何管理通过波次处理生成的标签。 （有关详细说明和配置说明，请参阅[配置波次标签打印](../warehousing/configure-wave-label-printing.md)。）

您可以随时重新打印波次标签。 例如，如果现有标签丢失或损坏，您可能必须打印一个标签。 或者，如果整个波次标签系列的数量和/或组成发生变化（例如，由于库存短缺或其他原因），仓库工作人员或主管可能必须重新打印整卷标签。 很多时候，即使仅货箱数量改变，也必须重新打印整卷标签，以保持每个标签的“货箱 X/Y”部分的总数量准确。

重新打印波次标签功能支持以下功能：

- 从仓库应用和富客户端重新打印标签。
- 取消标签，同时重新打印标签。 （例如，在领料短缺情景中嵌入了取消标签功能。）
- 清除波次标签历史记录。

本主题提供了一组方案，通过示例演示如何使用重新打印波次标签功能。

> [!IMPORTANT]
> 要演练本主题提供的方案，您必须首先打开并配置相关的波次打印功能，如[配置波次标签打印](../warehousing/configure-wave-label-printing.md)中所述。 本主题中的几种方案还需要您首先完成该主题中的方案以生成必备的示例数据。

## <a name="scenario-1-reprint-labels-from-the-web-client"></a>方案 1：从 Web 客户端重新打印标签

您可以从以下页面查看和重新打印波次标签。 在每页的“操作窗格”上的 **装运** 选项卡上，在 **相关信息** 组中，选择 **波次标签**。

- 所有装运 \> 装运详细信息
- 所有负荷 \> 负荷详细信息
- 所有波次
- 波次标签
- 波次标签历史记录

要从 Web 客户端重新打印波次标签，请按照下列步骤操作。

1. 转到 **仓库管理 \> 出站波次 \> 装运波次 \> 所有波次**。
1. 选择要重新打印标签的波次。
1. 在“操作窗格”的 **波次** 选项卡上，在 **打印** 组中，选择 **波次标签**。
1. 执行以下其中一个或全部两个步骤：

    - 要重新打印标签，在 **打印机名称** 字段中选择一个打印机。 （如果只想要更新波次标签详细信息，不重新打印标签，则将此字段留为空白。）
    - 要更新标签，选中 **更新波次标签详细信息** 复选框。 （如果只想要重新打印上一个标签，则不选中此复选框。）

    > [!NOTE]
    > 每次打印或重新打印波次标签时，其数据都会通过适当的波次标签布局转换，所有占位符都将替换为实际值。 生成的字符串将作为波次标签历史记录中的记录存储。 如果清除了 **更新波次标签详细信息** 复选框，在重新打印标签时将使用存储的 Zebra 编程语言 (ZPL) 数据。 如果选中了 **更新波次标签详细信息** 复选框，将生成一个新字符串。 现有波次标签也会重新计算，任何多余标签（例如，如果相关工作行被取消或修改）都将标记为 **已取消**，不会重新打印。

1. 选择 **确定** 确认您的选择。

## <a name="scenario-2-reprint-labels-from-the-warehousing-app"></a>方案 2：从仓库应用重新打印标签

此方案通常用于标签卷丢失或损坏的情况。 其中提供了一个示例，演示如何设置移动设备菜单项，让工作人员可以重新打印单个和多个标签。 然后演示在移动设备上工作时如何使用这些新菜单项。

### <a name="set-up-the-required-menu-items-and-menu-for-the-mobile-device"></a>设置移动设备所需的菜单项和菜单

您必须先设置菜单项以提供此功能，然后将这些项添加到仓库应用菜单中，然后工作人员才能够从移动设备重新打印标签。

#### <a name="create-new-mobile-device-menu-items"></a>创建新的移动设备菜单项

按照以下步骤为从仓库应用重新打印标签创建新的菜单项集合。

1. 转到 **仓库管理 \> 设置 \> 移动设备 \> 移动设备菜单项**。
1. 创建一个菜单项，并为其设置以下值：

    - **菜单项名称**：*重新打印单个波次标签*
    - **标题**：*重新打印单个波次标签*
    - **模式**：*间接*
    - **活动代码**：*Reprint single wave label*

1. 创建第二个菜单项，并为其设置以下值：

    - **菜单项名称**：*重新打印标签（项）*
    - **标题**：*重新打印波次标签（项）*
    - **模式**：*间接*
    - **活动代码**：*Reprint multiple wave labels*
    - **显示工作列表分组筛选器**：*是*
    - **系统分组字段**：*ShipmentID*
    - **系统分组标签**：*装运 ID*
    - **打印模式**：*产品*

1. 在“操作窗格”上，选择 **字段列表** 打开一个页面，您可以在其中选择将显示以帮助工作人员识别正确的标签卷的字段。
1. 最多可以显示七个字段。 使用下拉列表选择在每个可用位置显示的字段。 将不需要的任何字段留空。 

    下面是一个示例：

    - **显示字段**：*LabelItemId*
    - **显示字段 2**：*LabelItemName*
    - **显示字段 3**：*InventQty*
    - **显示字段 4**：*LabelUnitId*

1. 关闭该页面。
1. 创建第三个菜单项，并为其设置以下值：

    - **菜单项名称**：*重新打印标签（枚举）*
    - **标题**：*重新打印波次标签（枚举）*
    - **模式**：*间接**
    - **活动代码**：*Reprint multiple wave labels*
    - **显示工作列表分组筛选器**：*是*
    - **系统分组字段**：*ShipmentID*
    - **系统分组标签**：*装运 ID*
    - **打印模式**：*枚举*

1. 在“操作窗格”上，选择 **字段列表**，然后使用下拉列表选择将显示以帮助工作人员识别正确的标签卷的字段（例如，*LabelItemId*、*LabelItemName*、*InventQty*、*LabelUnitId* 和 *NumberOfLabels*）。
1. 关闭该页面。
1. 创建第四个菜单项，并为其设置以下值：

    - **菜单项名称**：*重新打印标签（最后一个）*
    - **标题**：*重新打印波次标签（最后一个）*
    - **模式**：*间接*
    - **活动代码**：*Reprint multiple wave labels*
    - **显示工作列表分组筛选器**：*是*
    - **系统分组字段**：*ShipmentID*
    - **系统分组标签**：*装运 ID*
    - **打印模式**：*最后一个合格波次标签 ID*

1. 在“操作窗格”上，选择 **字段列表**，然后使用下拉列表选择将显示以帮助工作人员识别正确的标签卷的字段（例如，*LabelItemId*、*LabelItemName*、*InventQty*、*LabelUnitId* 和 *NumberOfLabels*）。
1. 关闭该页面。

#### <a name="set-up-the-mobile-device-menu"></a>设置移动设备菜单

请按照以下步骤将新菜单项添加到仓库应用菜单。

1. 转到 **仓库管理 \> 设置 \> 移动设备 \> 移动设备菜单**。
1. 选择一个现有 **出站** 菜单。
1. 在左侧的列表中，找到刚才创建的重新打印菜单项，然后使用向右箭头按钮将其添加到右侧的列表中。
1. 关闭该页面。

### <a name="use-cases"></a>用例

此处提供的用例提供了一些示例，演示如何使用您设置的各个移动设备菜单项来让工作人员能够重新打印波次标签。

在演练这些用例之前，必须具备以下先决条件：

- 必须已安装演示数据，并且必须选择 **USMF** 法人。
- 必须配置波次标签打印，并且必须生成一些标签，如[配置波次标签打印](../warehousing/configure-wave-label-printing.md)中所述。

#### <a name="use-case-21-a-single-wave-label-is-scratched-and-must-be-reprinted"></a>用例 2.1：单个波次标签被刮花，必须重新打印。

1. 以访问仓库 *62* 的用户身份登录仓库应用。 （在标准演示数据中，您可以使用用户 ID *62* 和密码 *1* 登录。）
1. 转到 **出站 \> 重新打印单个波次标签**。
1. 输入或扫描波次标签 ID。
1. 选择重新打印要使用的打印机。
1. 选择 **确定** 确认操作。

#### <a name="use-case-22-several-labels-for-boxes-of-the-same-item-were-damaged-and-must-be-reprinted-each-label-has-a-product-bar-code-but-no-enumeration-or-sscc-number"></a>用例 2.2：同一物料的箱子的几个标签损坏，必须重新打印。 每个标签都有产品条码，但没有枚举或 SSCC 编号。

1. 以有权访问仓库 *62* 的用户身份登录仓库应用。 （在标准演示数据中，您可以使用用户 ID *62* 和密码 *1* 登录。）
1. 转到 **出站 \> 重新打印标签(项)**。
1. 输入或扫描装运 ID。
1. 选择具有正确标签卷要从其重新打印的磁贴。
1. 从现有标签扫描产品条码以确认选择了正确的行。
1. 输入要重新打印的标签数。
1. 选择重新打印要使用的打印机。
1. 选择 **确定** 确认操作。

#### <a name="use-case-23-several-labels-for-boxes-werent-printed-because-of-a-printer-jam-because-the-labels-have-enumeration-you-can-define-the-carton-range-to-reprint"></a>用例 2.3：由于打印机卡纸，箱子的几个标签没有打印。 因为标签具有枚举，所以您可以定义要重新打印的货箱范围。

1. 以有权访问仓库 *62* 的用户身份登录仓库应用。 （在标准演示数据中，您可以使用用户 ID *62* 和密码 *1* 登录。）
1. 转到 **出站 \> 重新打印标签(枚举)**。
1. 输入或扫描装运 ID。
1. 选择具有正确标签卷要从其重新打印的磁贴。
1. 输入要重新打印标签的第一个货箱。
1. 输入要重新打印标签的最后一个货箱。 或者，将此字段保留为空白以重新打印指定的第一个货箱之后的所有货箱的标签。
1. 选择重新打印要使用的打印机。
1. 选择 **确定** 确认操作。

#### <a name="use-case-24-several-labels-for-boxes-werent-printed-because-of-a-printer-jam-the-last-good-label-has-a-wave-label-id-that-is-printed-as-a-bar-code"></a>用例 2.4：由于打印机卡纸，箱子的几个标签没有打印。 最后一个合格标签的波次标签 ID 被打印为条码。

1. 以有权访问仓库 *62* 的用户身份登录仓库应用。 （在标准演示数据中，您可以使用用户 ID *62* 和密码 *1* 登录。）
1. 转到 **出站 \> 重新打印标签(最后一个)**。
1. 输入或扫描装运 ID。
1. 选择具有正确标签卷要从其重新打印的磁贴。
1. 输入或扫描最后一个合格波次标签的波次标签 ID。 应用会将序列中的下一个标签识别为要为其重新打印标签的第一个货箱。
1. 输入要重新打印标签的最后一个货箱。 或者，将此字段保留为空白以重新打印指定的第一个货箱之后的所有货箱的标签。
1. 选择重新打印要使用的打印机。
1. 选择 **确定** 确认操作。

## <a name="scenario-3-short-pick-and-reprint"></a>方案 3：领料短缺并重新打印

在演练此方案之前，必须具备以下先决条件：

- 必须已安装演示数据，并且必须选择 **USMF** 法人。
- 必须配置波次标签打印，并且必须生成一些标签，如[配置波次标签打印](../warehousing/configure-wave-label-printing.md)中所述。

### <a name="set-up-work-exceptions"></a>设置工作异常

工作异常控制领料短缺行为。 请按照以下步骤设置工作异常。

1. 转到 **仓库管理 \> 设置 \> 工作 \> 工作异常**。
1. 创建一个具有以下设置的记录：

    - **工作异常代码**：*Short pick and print*
    - **异常类型**：*领料短缺*
    - **建议波次标签重新打印**：*是*

### <a name="void-and-reprint-after-a-short-pick"></a>领料短缺后取消并重新打印

1. 以有权访问仓库 *62* 的用户身份登录仓库应用。 （在标准演示数据中，您可以使用用户 ID *62* 和密码 *1* 登录。）
1. 打开最初打印波次标签时创建的销售订单工作的工作处理流程。
1. 选择 **领料短缺**。
1. 选择您为此方案创建的工作异常代码。
1. 如果您选择了正确的异常，**取消并重新打印** 复选框应该可用。 选择此框并确认。 确认后，将根据更改的工作行数量重新计算由 **标签生成 ID** 字段标识的标签卷序列。 然后在指定打印机上重新打印。

## <a name="additional-resources"></a>其他资源

- [波次标签打印](configure-wave-label-printing.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]