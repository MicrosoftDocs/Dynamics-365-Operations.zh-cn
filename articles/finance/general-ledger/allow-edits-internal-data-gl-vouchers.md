---
title: 允许编辑总帐凭证上的内部数据
description: 本文提供有关如何编辑总帐凭证上的内部数据的信息。
author: kweekley
ms.date: 08/01/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 6e346c6ff881d3a33743196b45247493fd19ed1d
ms.sourcegitcommit: adadbc6e355e2ad68a1f6af26a1be1f89dc8eec6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/22/2022
ms.locfileid: "9573243"
---
# <a name="allow-edits-to-internal-data-on-general-ledger-vouchers"></a>允许编辑总帐凭证上的内部数据

[!include[banner](../includes/banner.md)]


当您将会计条目过帐到总帐时，**说明** 字段通常用于存储内部注释或文档。 如果信息不正确，则会导致混淆，并使期末结帐更加困难。 利用此功能，会计经理或会计主管可以通过编辑总帐中已过帐凭证上的 **说明** 字段来修复错误。

对总帐中已过帐凭证的更改仅限于内部性质的数据。 此功能绝不允许您编辑数据，如金额、过帐日期、会计帐户和交易货币。 更改该数据将影响财务报表的外部报告，并且只能通过新总帐凭证来进行更改。

> [!NOTE]
> 对于 Dynamics 365 Finance 版本 10.0.29，此功能仅限于编辑 **说明** 字段。

## <a name="edit-internal-data-on-general-ledger-vouchers"></a>编辑总帐凭证上的内部数据

您必须先在 **功能管理** 工作区中启用 **允许编辑总帐凭证上的内部数据** 功能，然后才能编辑总帐凭证上的内部数据。
启用此功能后，将编辑已过帐凭证的用户必须分配给会计经理或会计主管角色。 您还可以通过自定义安全角色向其他角色添加权限。

只允许从凭证交易页中执行编辑流程。

1. 转到 **总帐** > **查询和报表** > **凭证交易**。
2. 在 **SysQuery** 对话框中，输入搜索条件以选择凭证。
3. 选择要编辑的凭证的行，然后选择 **编辑凭证** > **编辑内部凭证数据**。

    [![凭证交易页面。](./media/voucher-transactions-page.png)](./media/voucher-transactions-page.png)
    
在 **编辑内部凭证数据** 页面上，针对所选的每个行显示了以下数据：
  
  - 分类帐帐户
  - 帐户名称
  - 凭证
  - 当前描述
  - 新建描述

    [![日记帐凭证。](./media/edit-internal-voucher-data.png)](./media/edit-internal-voucher-data.png)
    
> [!NOTE]
> 只能编辑 **新的描述** 字段。 默认情况下，该值与 **当前描述** 字段的值匹配，因此您可以快速修复描述中的小错误。

4. 修改每行上的 **新的描述** 字段，或从每行中删除描述。

   或者，如果必须使用相同的值更新多个行，请按照以下步骤操作：

      1. 选择要编辑的行，然后选择 **批量更新所选记录**。
      2. 在 **要编辑的字段** 字段中，选择要编辑的字段。 当前，查找仅包含 **新的描述** 字段。
      3. 在 **新值** 字段中，输入新的描述。
      4. 选择 **更新**。 所有选定记录均使用新值进行更新。

      [![“批量更新所选记录”对话框。](./media/bulk-update-selected-records.png)](./media/bulk-update-selected-records.png)
    
5. 在 **编辑原因** 字段中，输入注释以解释进行编辑的原因。 此注释显示在 **凭证编辑的审核线索** 页面上。

   可以对同一凭证进行多次编辑，并且将跟踪每项编辑。

## <a name="audit-trail-of-voucher-edits"></a>凭证编辑的审计线索

专门维护了审核线索以跟踪通过此功能进行的更改。 您可以用两种方式访问凭证编辑的审核线索：

  - 转到 **总帐** > **查询和报表** > **凭证交易**。 在 **凭证查询** 页面上，选择 **编辑凭证** > **凭证编辑的审核线索**。 仅显示所选凭证记录的审核线索。 
   
    通过以这种方式打开查询，您可以专注于对单个凭证记录进行的所有编辑。
  
  - 转到**总帐** > **定期任务** > **凭证编辑的审核线索**。 在对话框中，输入条件以指定您要查看其编辑审核线索的凭证。 若要查看所有凭证的审核线索，请将条件留空，然后选择 **确定**。 
    
    通过以这种方式打开查询，您可以筛选在特定日期或由特定用户进行的编辑。

**编辑的审核线索** 页面显示了以下信息：

- **创建日期和时间** - 编辑的日期和时间。
- **编辑原因** - 用户输入的进行编辑的原因。
- **创建者** – 进行编辑的用户。

若要查看每个审核线索的详细信息，请向下钻取到 **创建日期和时间** 值。 **查看已编辑的凭证属性** 页面显示与原始编辑页相同的信息，包括上一个描述和更新的描述。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
