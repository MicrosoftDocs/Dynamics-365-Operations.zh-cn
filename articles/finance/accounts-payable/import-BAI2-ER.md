---
title: 使用电子报告设置高级银行对帐导入
description: 本主题说明如何使用电子报告为 BAI2 对帐单设置高级银行对帐导入流程。
author: panolte
ms.date: 03/30/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: twheeloc
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.25
ms.openlocfilehash: 39f1d8ba561ab0e36346f1dfb4f70df318c92a37
ms.sourcegitcommit: cf7d4af11bf85638ee831a28ea5ee1a1e041a675
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/04/2022
ms.locfileid: "8544464"
---
# <a name="set-up-advanced-bank-reconciliation-import-by-using-electronic-reporting"></a>使用电子报告设置高级银行对帐导入

[!include [banner](../includes/banner.md)]

高级银行对帐功能让您可以导入电子银行对帐单，并可以将其与 Microsoft Dynamics 365 Finance 中的银行交易记录自动对帐。 本主题介绍如何设置 BAI2 银行对帐单的导入功能。

## <a name="set-up-the-electronic-reporting-configuration"></a>设置电子报告配置

1. 转到 **工作区 \> 电子报告**。
2. 在 **Microsoft** 配置提供商的磁贴中，选择 **存储库**。
3. 选择 **全局**，然后选择 **打开**。
4. 如果必须建立与存储库的连接，选择对话框中的蓝色链接。
5. 在配置列表中，找到 **银行对帐单模型 \> BAI2 银行对帐单模型**。
6. 选择 **BAI2** 格式。
7. 在 **版本** 快速选项卡上，选择最新版本，然后选择 **导入**。

## <a name="set-up-the-bank-statement-format"></a>设置银行对帐单格式

1. 转到 **现金和银行管理 \> 设置 \> 高级银行对帐设置 \> 银行对帐单格式**。
2. 选择 **新建**。
3. 设置 **对帐单格式** 和 **名称** 字段。
4. 选中 **一般电子导入格式** 复选框。
5. 将 **导入格式配置** 字段设置为 **BAI2** 格式。

## <a name="set-up-the-bank-account"></a>设置银行帐户

1. 转至 **现金和银行管理 \> 银行帐户 \> 银行帐户**。
2. 打开银行帐户。
3. 在 **对帐** 快速选项卡上，设置 **高级银行对帐** 选项为 **是**。
4. 将 **对账单格式** 字段设置为之前创建的 **BAI2** 格式。

## <a name="import-the-bank-statement"></a>导入银行对帐单

1. 转到 **现金和银行管理 \> 银行对帐单对帐 \> 银行对帐单**。
2. 在 **银行对帐单** 页面的顶部，选择 **导入对帐单**。
3. 将 **银行帐户** 字段设置为对帐单中的银行帐户。
4. 将 **对账单格式** 字段设置为之前创建的 **BAI2** 格式。
5. 选择 **浏览**，选择 **BAI** 文件。
6. 选择 **上载**。
7. 选择 **确定** 导入所选文件。
