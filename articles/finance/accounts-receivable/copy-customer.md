---
title: 使用共享的编号规则复制客户
description: 本文将介绍如何使用共享的编号规则将客户复制到另一个法人但却保持相同的客户 ID。
author: abruer
ms.date: 08/31/2018
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: CustTable
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 54639356007198f256f0d80fce9bfa2013f7b2b7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899976"
---
# <a name="copy-customers-by-using-shared-number-sequences"></a>使用共享的编号规则复制客户

[!include [banner](../includes/banner.md)]

您可以使用共享的编号规则分配客户 ID。 利用共享的编号规则，您还可以将客户从一个法人复制到另一个法人，但却在这两个法人中使用相同的客户 ID。

## <a name="setup"></a>设置

使用共享的编号规则分配客户 ID 时会激活此功能。 您必须在要将客户复制到的每个法人中使用相同的编号规则。 您可以在 **应收帐款参数** 页上为每个法人更改客户编号规则。 选择 **应收帐款** \> **参数**，然后选择 **编号规则** 选项卡。

您还可以为每个客户组设置客户编号规则。 还必须共享这些编号规则。 首先使用客户组的编号规则。 如果没有为客户组指定编号规则，则使用在 **应收帐款参数** 页上指定的编号规则。

如果您使用手动客户 ID，也可以在法人之间复制客户。 但是，如果您尝试将客户复制到已存在客户 ID 的法人，则不会启动复制过程。

## <a name="copy-a-customer"></a>复制客户

要复制客户，请选择 **所有客户** 列表页面上的 **新建** 以打开 **创建客户** 对话框。 请注意，系统未立即分配新的客户 ID。 此行为与先前版本中的行为不同。 由于您尚未选择客户组，因此系统无法确定要使用的正确编号规则。 此外，系统无法确定您是要尝试创建新客户还是复制客户。 因此，在对话框底部选择 **保存** 之前，不会分配客户 ID。

如果您要创建新客户，则可以像往常一样继续填写所有字段。 在完成并选择 **保存** 时，您将会发现系统自动分配了客户 ID。 或者，您将发现对手动编号规则使用了手动客户 ID。

要复制客户，请在 **名称** 字段中输入一个或多个能代表所查找客户的字符。 搜索对话框会显示可能代表所寻找客户的当事方列表。 当您选择其中一个当事方时，对话框右侧会显示附加信息：

- **常规** 选项卡显示当事方的电话号码和地址。
- **角色** 选项卡显示所选当事方可能具有的角色，以及该当事方具有每种角色所在的法人。
- **税务登记 ID** 选项卡显示分配给当事方的税务登记 ID。

只有在当事方具有客户角色时，并且仅当该当事方在非当前法人中具有该角色时，您才能复制该当事方。 在您查找满足这些标准的当事方时，请执行以下步骤。

1. **复制客户** 选项将会出现。 默认情况下，此选项设置为 **否**。 要将客户复制到当前法人，请将此选项设置为 **是**。 
2. **法人** 字段将会出现。 选择要从其中复制客户的法人。 如果客户只存在于一个法人中，则默认情况下此字段会设置为该法人。
3. 选择 **选择**。 此时会创建新客户。

## <a name="validation"></a>验证

复制客户时，系统会尝试保存新客户信息。 系统会运行验证以验证复制的数据是否完好。 对于每项失败的验证，您都会收到一条错误消息。 错误消息说明了必须更新哪些信息。 在修复所有验证错误之前，无法保存客户的副本。

## <a name="copy-a-customer-by-using-tax-exempt-number-search-feature"></a>使用免税编号搜索功能复制客户

您还可以使用 **所有客户** 页面操作窗格上 **客户** 选项卡内 **登记** 组中的免税编号搜索功能来复制客户。 出现的 **免税编号搜索** 对话框会显示免税编号、客户 ID、客户名称以及使用免税 ID 的法人。 只有当客户在非当前法人中时，您才能复制客户。 在选择满足此标准的客户后，请执行以下步骤。

1. **复制客户** 选项将会出现。 默认情况下，此选项设置为 **否**。 要将客户复制到当前法人，请将此选项设置为 **是**。 
2. 选择 **选择**。 此时会创建新客户。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
