---
title: 存档库存交易记录
description: 本文介绍如何存档库存交易记录数据以帮助提高系统性能。
author: yufeihuang
ms.date: 05/10/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTransArchiveProcessForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-03-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: c63cdee862e2e22649a3eb58ae37597741770e14
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874092"
---
# <a name="archive-inventory-transactions"></a>存档库存交易记录

[!include [banner](../../includes/banner.md)]

随着时间的推移，库存交易记录表 (`InventTrans`) 会继续增长，消耗更多数据库空间。 因此，针对表进行的查询将逐渐变慢。 本文介绍如何使用 *库存交易记录存档* 功能来存档有关库存交易记录的数据，以帮助提高系统性能。

> [!NOTE]
> 只有财务更新的库存交易记录可以在选定的已关闭分类帐期间内存档。 要进行存档，财务更新的出站库存交易记录的发货状态必须为 *已售出*，而入站库存交易记录的收货状态必须为 *已购买*。

存档库存交易记录时，所有相关交易记录都将移至 `InventTransArchive` 表。 库存发货交易记录和库存收货交易记录基于物料 ID (`itemId`) 和库存维度 ID (`inventDimId`) 的组合分别存档，并被放入汇总发货和汇总收货交易记录中。

如果 `itemId` 和 `inventDimId` 组合仅包含一个收货或发货交易记录，该交易记录将不会被存档。

## <a name="turn-on-the-feature-in-your-system"></a>在系统中开启此功能

如果您的系统尚未包含本文中所述的功能，请转到 [功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)，打开 *库存交易记录存档* 功能。 请注意，此功能在启用后，无法禁用。

## <a name="things-to-consider-before-you-archive-inventory-transactions"></a>存档库存交易记录之前要考虑的事项

在归档库存交易记录之前，应考虑以下业务场景，因为它们会受到操作的影响：

- 当您审计相关文档（如采购订单行）中的库存交易记录时，它们将显示为已存档。 要查看已存档的交易记录，您必须转到 **库存管理 \> 定期任务 \> 清理 \> 库存交易记录存档**。
- 存档期间的库存结转无法取消。 您必须先撤消相关期间的库存交易记录存档，然后才可以取消库存结转。
- 存档期间无法执行标准成本转换。 您必须先撤消相关期间的库存交易记录存档，然后才可以执行标准成本转换。
- 存档库存交易记录时，源自库存交易记录的库存报表将受到影响。 这些报表包括库存帐龄报表和库存值报表。
- 如果库存预测在存档期间的时间范围内运行，可能会受到影响。

## <a name="prerequisites"></a>先决条件

库存交易记录只能在满足以下条件的期间存档：

- 分类帐期间必须已关闭。
- 库存结转必须在存档的到期日期或之后运行。
- 期间必须至少为存档起始日期之前一年。
- 不能进行任何现有的库存重新计算。

## <a name="archive-inventory-transactions"></a>存档库存交易记录

若要存档库存交易记录，请执行以下步骤。

1. 转到 **库存管理** \> **定期任务** \> **清理** \> **库存交易记录存档**。

    **库存交易记录存档** 页将出现，显示已存档流程记录的列表。

    ![库存交易存档页面。](media/archive-inventory-empty.png "库存交易记录存档页")

1. 在操作窗格上，选择 **库存交易记录存档** 创建库存交易记录存档。
1. 在 **库存交易记录存档** 对话框中，在 **参数** 快速选项卡上，设置以下字段：

    - **已关闭分类帐期间中的开始日期** – 选择要包括在存档中的最早的交易记录日期。
    - **已关闭分类帐期间中的结束日期** – 选择要包括在存档中的最晚的交易记录日期。

    ![库存交易存档对话框。](media/archive-inventory-dates.png "库存交易记录存档对话框")

    > [!NOTE]
    > 只有满足[先决条件](#prerequisites)的期间才可以选择。

1. 在 **在后台运行** 快速选项卡上，根据需要设置批处理详细信息。 按照 Microsoft Dynamics 365 Supply Chain Management 中批处理作业的通常步骤操作。
1. 选择 **确定**。
1. 您将收到一条消息，提示您确认您希望继续。 仔细阅读消息，如果您希望继续，选择 **是**。

    您将收到一条消息，指出您的库存交易记录存档作业已添加到批处理队列中。 此作业现在将开始存档所选期间的库存交易记录。

## <a name="view-archived-inventory-transactions"></a>查看已存档的库存交易记录

**库存交易记录存档** 页将显示完整存档历史记录。 网格中的每一行显示存档创建日期、创建存档的用户以及存档的状态等信息。

![库存交易存档页面上的存档历史记录。](media/archive-inventory-full.png "库存交易记录存档页上的存档历史记录")

在页面顶部的下拉列表中，选择以下值之一以筛选显示在网格中的存档：

- **活动** – 仅显示活动存档，不显示已撤消的存档。
- **所有** – 显示所有存档，包括活动和已撤消存档。

对于网格中的每个存档，将提供以下信息：

- **活动** – 指示存档处于活动状态的复选标记。
- **开始日期** – 可以包含在存档中的最早交易记录的日期。
- **结束日期** – 可以包含在存档中的最近交易记录的日期。
- **计划者** – 创建存档的用户帐户。
- **执行日期** – 存档创建的日期。
- **撤消** – 指示存档已撤消的复选标记。
- **停止当前更新** – 指示存档正在进行，但已暂停的复选标记。
- **状态** – 存档的处理状态。 可能的值为 *等待*、*进行中* 和 *已完成*。

网格上方的工具栏提供以下按钮，可用于处理选定的存档：

- **已存档的交易记录** – 查看所选存档的全部详细信息。 出现的 **已存档的交易记录** 页将显示存档中的所有交易记录。

    ![已存档的交易页面。](media/archive-inventory-transactions.png "已存档的交易记录页")

    要在 **已存档的交易记录** 页上查看有关特定交易记录的详细信息，请在网格中选择它，然后在操作窗格上，选择 **已存档的交易记录详细信息**。 出现的 **已存档的交易记录详细信息** 页将显示分类帐过帐、相关子分类帐参考和财务维度等信息。

- **暂停存档** – 暂停当前正在处理的选定存档。 暂停仅在生成存档任务后生效。 因此，暂停生效之前可能会有短暂的延迟。 如果存档已暂停，**停止当前更新** 字段中会出现一个复选标记。
- **恢复存档** – 恢复当前暂停的选定存档的处理。
- **撤消** – 撤消所选择的存档。 仅当存档的 **状态** 字段设置为 *已完成* 时，才可以撤消存档。 如果存档已撤消，**撤消** 字段中会出现一个复选标记。

## <a name="extend-your-code-to-support-custom-fields"></a>扩展代码以支持自定义字段

如果表 `InventTrans` 包含一个或多个自定义字段，则可能需要扩展代码以支持它们，具体取决于它们的命名方式。

- 如果 `InventTrans` 表中的自定义字段与 `InventtransArchive` 表中自动具有相同的字段名称，则表示 1:1 映射了它们。 因此，您可以只将自定义字段放入 `inventTrans` 表的 `InventoryArchiveFields`字段组中。
- 如果 `InventTrans` 表中的自定义字段名称与 `InventtransArchive` 表中的字段名称不匹配，则需要添加代码以映射它们。 例如，如果您有一个名为 `InventTrans.CreatedDateTime` 的系统字段，则必须在 `InventTransArchive` 表中创建一个具有不同名称的字段（例如 `InventtransArchive.InventTransCreatedDateTime`），并将扩展添加到 `InventTransArchiveProcessTask` 和  `InventTransArchiveSqlStatementHelper` 类，如以下示例代码所示。

以下示例代码显示了一个关于如何将所需扩展添加到 `InventTransArchiveProcessTask` 类的示例。

```xpp
[ExtensionOf(classStr(InventTransArchiveProcessTask))]
Final class InventTransArchiveProcessTask_Extension
{

    protected void addInventTransFields(SysDaSelection _selectionObject)
    {
        _selectionObject.add(fieldStr(InventTrans, ModifiedBy))
            .add(fieldStr(InventTrans, CreatedBy)).add(fieldStr(InventTrans, CreatedDateTime));

        next addInventTransFields(_selectionObject);
    }


    protected void addInventTransArchiveFields(SysDaSelection _selectionObject)
    {
        _selectionObject.add(fieldStr(InventTransArchive, InventTransModifiedBy))
            .add(fieldStr(InventTransArchive, InventTransCreatedBy)).add(fieldStr(InventTransArchive, InventTransCreatedDateTime));

        next addInventTransArchiveFields(_selectionObject);
    }
}
```

以下示例代码显示了一个关于如何将所需扩展添加到 `InventTransArchiveSqlStatementHelper` 类的示例。

```xpp
[ExtensionOf(classStr(InventTransArchiveSqlStatementHelper))]
final class InventTransArchiveSqlStatementHelper_Extension
{
    private str     inventTransModifiedBy;  
    private str     inventTransCreatedBy;
    private str     inventTransCreatedDateTime;

    protected void initialize()
    {
        next initialize();
        inventTransModifiedBy = new SysDictField(tablenum(InventTrans), fieldNum(InventTrans, ModifiedBy)).name(DbBackend::Sql);
        inventTransCreatedDateTime = new SysDictField(tablenum(InventTrans), fieldNum(InventTrans, CreatedDateTime)).name(DbBackend::Sql);
        inventTransCreatedBy = new SysDictField(tablenum(InventTrans), fieldNum(InventTrans, CreatedBy)).name(DbBackend::Sql);
    }

    protected str buildInventTransArchiveSelectionFieldsStatement()
    {
        str     ret;

        ret = next buildInventTransArchiveSelectionFieldsStatement();
        
        if (inventTransModifiedBy)
        {
            ret += ',';
            ret += strFmt('%1',  new SysDictField(tablenum(InventTransArchive), fieldNum(InventTransArchive, InventTransModifiedBy)).name(DbBackend::Sql));
        }

        if (inventTransCreatedBy)
        {
            ret += ',';
            ret += strFmt('%1',  new SysDictField(tablenum(InventTransArchive), fieldNum(InventTransArchive, InventTransCreatedBy)).name(DbBackend::Sql));
        }

        if (inventTransCreatedDateTime)
        {
            ret += ',';
            ret += strFmt('%1',  new SysDictField(tablenum(InventTransArchive), fieldNum(InventTransArchive, InventTransCreatedDateTime)).name(DbBackend::Sql));
        }

        return ret;
    }

    protected str buildInventTransTargetFieldsStatement()
    {
        str     ret;

        ret = next buildInventTransTargetFieldsStatement();

        if (inventTransModifiedBy)
        {
            ret += ',';
            ret += strFmt('%1', inventTransModifiedBy);
        }

        if (inventTransCreatedBy)
        {
            ret += ',';
            ret += strFmt('%1', inventTransCreatedBy);
        }

        if (inventTransCreatedDateTime)
        {
            ret += ',';
            ret += strFmt('%1', inventTransCreatedDateTime);
        }

        return ret;
    }
}
```
