---
title: 使用电子报告设置高级银行对帐导入
description: 本文说明如何使用电子报告设置高级银行对帐导入流程。
author: angelad116
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
ms.openlocfilehash: bfc1c2021387ed35e6ccb513167e896eddef2eaf
ms.sourcegitcommit: ea79bf014bbf495ac8e28db29502c8bd85a75f32
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/11/2022
ms.locfileid: "9759592"
---
# <a name="set-up-advanced-bank-reconciliation-import-by-using-electronic-reporting"></a>使用电子报告设置高级银行对帐导入

[!include [banner](../includes/banner.md)]

高级银行对帐功能让您可以导入电子银行对帐单，并可以将其与 Microsoft Dynamics 365 Finance 中的银行交易记录自动对帐。 本文介绍如何设置银行对账单的导入功能。 银行对账单导入设置因您电子银行对账单的格式的不同而不同。 Microsoft Dynamics 365 Finance 支持三种银行对帐单格式︰ISO20022、MT940 和 BAI2。 

## <a name="set-up-the-electronic-reporting-configuration"></a>设置电子报告配置

1. 转到 **工作区 \> 电子报告**。
2. 在 **Microsoft** 配置提供商的磁贴中，选择 **存储库**。
3. 选择 **全局**，然后选择 **打开**。
4. 如果必须建立与存储库的连接，选择对话框中的蓝色链接。
5. 在配置列表中，找到 **高级银行对帐单模型 \> ABR BAI2 格式**。
6. 选择 **BAI2** 格式。
7. 在 **版本** 快速选项卡上，选择最新版本，然后选择 **导入**。

>[!NOTE]
>**BAI2 银行对帐单模型** 以后将弃用。 

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


## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a>银行对账单格式和技术布局的示例
下面是高级银行对帐导入文件技术布局定义的示例和三个相关银行对帐单示例文件：[导入文件示例](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)  

| 技术布局定义                             | 银行对账单示例文件          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout | [MT940StatementExample](//download.microsoft.com/download/2/d/c/2dcc4e55-ddc8-4a74-b79c-250fae201c3c/mt940StatementExample.txt)     |
| DynamicsAXISO20022Layout | [ISO20022StatementExample](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdownload.microsoft.com%2Fdownload%2F1%2F5%2F5%2F155d84ed-c250-48f3-b0b1-c5a431e7855b%2FISO20022-MultipleStatements.xml&data=04%7C01%7CRobert.Schlomann%40microsoft.com%7C30d0c233cb6546547d0a08d8f4965edc%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637528273956712775%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=3VzvLZK%2BO8PjuI7XVdC6rD2j3nUJfteo7zFp%2B1s9BwM%3D&reserved=0)             |
| DynamicsAXBAI2Layout    | [BAI2StatementExample](//download.microsoft.com/download/1/1/6/11693f57-bfc1-4993-a274-5fb978be70fa/BAI2StatementExample.txt)     |

