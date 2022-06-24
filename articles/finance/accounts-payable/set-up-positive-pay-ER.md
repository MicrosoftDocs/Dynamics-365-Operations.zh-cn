---
title: 使用电子报告设置和生成付款确认文件
description: 本文说明如何使用电子报告设置付款确认。
author: panolte
ms.date: 03/20/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankPositivePayFormat
audience: Application User
ms.reviewer: twheeloc
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 491048c7274ba6bb52e0a4b7a6ea5cd0f5ff4741
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878209"
---
# <a name="set-up-positive-pay-files-by-using-electronic-reporting"></a>使用电子报告设置付款确认文件

本文说明如何使用电子报告设置付款确认和生成付款确认文件。

> [!NOTE] 
> 在使用 **生成银行付款确认文件** 功能之前，您将需要先刷新实体列表。
> 转到 **数据管理 > 导入/导出 > 框架参数**  
> **实体设置** 快速选项卡，选择 **刷新实体列表**。


设置付款确认以生成提供给银行的支票电子列表。 当支票提交给银行时，银行将支票与支票的列表进行对比。 如果支票与列表中的支票相匹配，银行将清算支票。 如果支票与列表中的支票不匹配，银行将保留支票以供审查。

## <a name="security-for-positive-pay-files"></a>付款确认文件的安全
付款确认文件可以包含有关收款人和支票金额的敏感信息。 因此，请您务必自文件生成时便使用相应的安全措施，直到它们由银行接收。 付款确认文件下载到您的 Web 浏览器指定的位置。 由于付款确认文件可能包含敏感信息，务必确保仅授权用户可以在 Microsoft Dynamics 365 Finance 中生成和查看此信息。 请使用下表帮助您确定所需权限。

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>任务</th>
<th>特权</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>从<strong>银行帐户</strong>列表页或<strong>银行帐户</strong>页生成付款确认文件。</td>
<td><ul>
<li><strong>维护银行付款确认信息</strong> (BankPositivePayProcess)</li>
<li><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</li>
</ul></td>
</tr>
<tr class="even">
<td>从<strong>生成付款确认文件</strong>页生成多个法人和银行帐户的付款确认文件。</td>
<td><ul>
<li><strong>维护银行付款确认信息</strong> (BankPositivePayProcess)</li>
<li><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</li>
</ul></td>
</tr>
<tr class="odd">
<td>在<strong>付款确认文件摘要</strong>页查看付款确认文件。</td>
<td><strong>查看多个法人的银行付款确认信息</strong> (BankPositivePayView)</td>
</tr>
<tr class="even">
<td>在<strong>付款确认文件摘要</strong>页确认银行付款确认文件。</td>
<td><strong>确认付款确认文件</strong> (BankPositivePayConfirm)</td>
</tr>
<tr class="odd">
<td>在<strong>付款确认文件摘要</strong>页撤回银行付款确认文件。</td>
<td><strong>撤回付款确认文件</strong> (BankPositivePayRecall)</td>
</tr>
</tbody>
</table>

## <a name="set-up-the-electronic-reporting-configuration"></a>设置电子报告配置

1. 转到 **工作区 \> 电子报告**。
2. 在 **Microsoft** 配置提供商的磁贴中，选择 **存储库**。
3. 选择 **全局**，然后选择 **打开**。
4. 如果必须建立与存储库的连接，选择对话框中的蓝色链接。
5. 在配置列表中，查找并选择 **付款确认模型 \> 付款确认格式**。
6. 在 **版本** 快速选项卡上，选择最新版本，然后选择 **导入**。

## <a name="set-up-a-positive-pay-format"></a>设置付款确认格式

1. 转到 **现金和银行管理 \> 设置 \> 付款确认格式**。
2. 选择 **新建**。
3. 设置 **付款格式** 和 **描述** 字段。
4. 选中 **一般电子导出格式** 复选框。
5. 将 **导出格式配置** 字段设置为 **付款确认格式**。

## <a name="assign-a-positive-pay-format-to-a-bank-account"></a>将付款确认格式分配到银行帐户
对于您想要生成付款确认信息的每个银行帐户，您必须分配在前一部分中指定的付款确认格式。 在银行帐户页上，选择与银行帐户对应的付款确认格式。 在 **付款确认开始日期** 字段中，输入第一个日期以生成付款确认文件。 

>[!Important]
> 在 **付款确认开始日期** 字段中输入日期。 如果将其留空，则生成的第一个付款确认文件将包括已为此银行帐户创建的所有支票。

1. 转到 **现金和银行管理 \> 银行帐户 \> 银行帐户**。
2. 打开银行帐户。
3. 在 **常规** 快速选项卡上，将 **付款确认格式** 字段设置为之前创建的格式。
4. 将 **付款确认开始日期** 字段设置为当前日期。

## <a name="assign-a-number-sequence-for-positive-pay-files"></a>分配付款确认文件的编号规则
每个付款确认文件必须具有唯一编号。 在 **现金和银行管理参数** 页的 **编号规则** 选项卡上，为付款确认文件创建编号规则。

## <a name="generate-a-positive-pay-file-for-a-single-bank-account"></a>生成单个银行帐户的付款确认文件
您可以生成用于一个法人或一个银行帐户的付款确认文件。 有关如何同时生成用于多个法人和银行帐户的付款确认文件，请参阅下一部分。 若要生成单个法人和单个银行帐户的付款确认文件，从 **银行帐户** 页打开 **生成付款确认文件** 对话框。 在字段 **截止日期** 中，输入在付款确认文件中的最后支票日期。 所有在该支票日期结束前未包括在一个付款确认文件中的支票将包括在该文件中。

1. 转到 **现金和银行管理 \> 银行帐户 \> 银行帐户**。
2. 打开为其设置付款确认的银行帐户。
3. 选择 **管理付款 \> 付款确认 \> 付款确认文件**。
4. 设置 **截止日期** 字段。 在此日期之前生成的支票将包括在内。

## <a name="generate-a-positive-pay-file-for-multiple-bank-accounts"></a>生成多个银行帐户的付款确认文件
若要生成多个银行帐户的付款确认文件，使用 **付款确认文件** 定期任务。 选择文件的付款确认格式，并指定是为所有法人还是所选法人生成文件。 您还可以为使用指定的付款确认格式的所有银行帐户或为所选银行帐户生成付款确认文件。 在字段 **截止日期** 中，输入在付款确认文件中的最后支票日期。 所有在该支票日期结束前未包括在一个付款确认文件中的支票将包括在该文件中。

## <a name="view-the-results-of-positive-pay-file-generation"></a>查看付款确认文件的生成结果
在付款确认文件生成后，您可以在 **付款确认文件摘要** 页上查看结果。 若要查看单个支票的详细信息，转到 **付款确认文件详细信息** 页。

## <a name="confirm-a-positive-pay-file"></a>确认付款确认文件
当付款确认文件中列出的支票支付后，您将从银行收到一个确认编号。 然后，您可以确认付款确认文件。 在 **付款确认文件** 页上，选择状态为 **已创建** 的付款确认文件，然后选择 **输入确认** 操作。 在确认付款确认文件时，记录您从银行收到的确认编号。

## <a name="recall-a-positive-pay-file"></a>撤回付款确认文件
如果您必须更改付款确认文件，您可以撤消它。 在 **付款确认文件** 页上，选择状态为 **已创建** 的付款确认文件，然后选择 **撤回** 操作。 对于付款确认文件中的每一张支票，将重置指示该支票是否包括在一个付款确认文件中的字段。 然后，您可以创建包括已撤消支票的新的付款确认文件。


将下载生成的 XML 文件。
