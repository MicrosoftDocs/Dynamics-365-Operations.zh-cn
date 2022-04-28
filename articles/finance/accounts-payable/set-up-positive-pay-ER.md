---
title: 使用电子报告设置和生成付款确认文件
description: 本主题说明如何使用电子报告设置付款确认。
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
ms.openlocfilehash: 43dd1a9cba1fe8df5cff26fe76af7e2957a0d6a4
ms.sourcegitcommit: cf7d4af11bf85638ee831a28ea5ee1a1e041a675
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/04/2022
ms.locfileid: "8544460"
---
# <a name="set-up-positive-pay-files-by-using-electronic-reporting"></a>使用电子报告设置付款确认文件

设置付款确认以生成提供给银行的支票电子列表。 然后，当支票提交给银行时，银行将支票与支票的列表进行对比。 如果支票与列表中的支票相匹配，银行将清算支票。 如果支票与列表中的支票不匹配，银行将保留支票以供审查。

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

1. 转到 **现金和银行管理 \> 银行帐户 \> 银行帐户**。
2. 打开银行帐户。
3. 在 **常规** 快速选项卡上，将 **付款确认格式** 字段设置为之前创建的格式。
4. 将 **付款确认开始日期** 字段设置为当前日期。

## <a name="generate-a-positive-pay-file"></a>生成付款确认文件

1. 转到 **现金和银行管理 \> 银行帐户 \> 银行帐户**。
2. 打开为其设置付款确认的银行帐户。
3. 选择 **管理付款 \> 付款确认 \> 付款确认文件**。
4. 设置 **截止日期** 字段。 在此日期之前生成的支票将包括在内。

将下载生成的 XML 文件。
