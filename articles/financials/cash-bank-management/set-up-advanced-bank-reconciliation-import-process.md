---
title: "设置高级银行对帐导入流程"
description: "高级银行对帐功能让您可以导入电子银行对帐单，并可以将其与 Microsoft Dynamics 365 for Finance and Operations 中的银行交易记录自动对帐。 本文介绍如何设置银行对账单的导入功能。"
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 106853
ms.assetid: 45dae275-ea45-4c7e-b38f-89297c7b5352
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 7292767f48e94f01c50e12ab02a4483c53046ae9
ms.contentlocale: zh-cn
ms.lasthandoff: 03/26/2018

---

# <a name="set-up-the-advanced-bank-reconciliation-import-process"></a>设置高级银行对帐导入流程

[!include [banner](../includes/banner.md)]

高级银行对帐功能让您可以导入电子银行对帐单，并可以将其与 Microsoft Dynamics 365 for Finance and Operations 中的银行交易记录自动对帐。 本文介绍如何设置银行对账单的导入功能。 

银行对账单导入设置因您电子银行对账单的格式的不同而不同。 Finance and Operations 支持三个现成的银行对账单格式︰ISO20022、MT940 和 BAI2。

## <a name="sample-files"></a>示例文件
对于所有三种格式，您必须有将电子银行对账单的原始格式转换为 Finance and Operations 可以使用的格式的文件。 您可以在 Microsoft Visual Studio 中应用程序资源管理器的**资源**节点下找到所需资源文件。 找到文件后，将它们复制到一个已知位置，以便您可以更轻松地在设置流程中上载它们。

| 资源名称                                           | 文件名                            |
|---------------------------------------------------------|--------------------------------------|
| BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt              | BAI2CSV-to-BAI2XML.xslt              |
| BankStmtImport\_BAI2XML\_to\_Reconciliation\_xslt       | BAI2XML-to-Reconciliation.xslt       |
| BankStmtImport\_BankReconciliation\_to\_Composite\_xslt | BankReconciliation-to-Composite.xslt |
| BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt   | ISO20022XML-to-Reconciliation.xslt   |
| BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt            | MT940TXT-to-MT940XML.xslt            |
| BankStmtImport\_MT940XML\_to\_Reconciliation\_xslt      | MT940XML-to-Reconciliation.xslt      |
| BankStmtImport\_SampleBankCompositeEntity\_xml          | SampleBankCompositeEntity.xml        |

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a>银行对账单格式和技术布局的示例
下面是高级银行对帐导入文件技术布局定义的示例和三个相关银行对帐单示例文件：https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts  

| 技术布局定义                             | 银行对账单示例文件          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout                                   | MT940StatementExample                |
| DynamicsAXISO20022Layout                                | ISO20022StatementExample             |
| DynamicsAXBAI2Layout                                    | BAI2StatementExample                 |



## <a name="set-up-the-import-of-iso20022-bank-statements"></a>设置 ISO20022 银行对账单的导入
首先，您必须通过使用数据实体框架定义 ISO20022 银行对账单的银行对账单格式处理组。

1.  转到**工作区** &gt; **数据管理**。
2.  单击**导入**。
3.  为格式输入名称，如 **ISO20022**。
4.  将**源数据格式**字段设置为 **XML-元素**。
5.  将**实体名称**字段设置为**银行对账单**。
6.  若要上载导入文件，请单击**上载**，然后浏览以选择以前保存的 **SampleBankCompositeEntity.xml** 文件。
7.  银行对账单实体上载且映射完成后，请单击实体的**查看地图**操作。
8.  银行对账单实体是由四个单独的实体组成一个复合实体。 在列表中，选择 **BankStatementDocumentEntity**，然后单击**查看地图**操作。
9.  在**转换**选项卡上，单击**新建**。
10. 对于序列号 1，请单击**上载文件**，并选择以前保存的 **ISO20022XML-to-Reconciliation.xslt** 文件。 **注意︰** Finance and Operations 转换文件使用标准格式构建。 因为银行经常偏离这种格式，您可能必须更新要映射到您的银行帐单格式的转换文件。 <!-- For details about the expected format for ISO20022, see [Dynamics AX ISO20022 Layout](./media/dynamicsaxiso20022layout1.xlsx).-->
11. 单击**新建**。
12. 对于序列号 2，请单击**上载文件**，并选择以前保存的 **BankReconciliation-to-Composite.xslt** 文件。
13. 单击**应用转换**。

设置格式处理组后，下一步是定义 ISO20022 银行对账单的银行对账单格式规则。

1.  转到**现金和银行管理** &gt; **设置** &gt; **高级银行对帐设置** &gt; **银行对账单格式**。
2.  单击**新建**。
3.  指定对账单格式，如 **ISO20022**。
4.  输入格式名称。
5.  将**处理组**字段设置为之前定义的组，如 **ISO20022**。
6.  选中 **XML 文件**复选框。

最后一步是启用高级银行对帐并设置银行帐户的对账单格式。

1.  转 **“现金和银行管理** &gt; **银行帐户**。
2.  选择银行帐户并打开帐户以查看详细信息。
3.  在**对帐**选项卡上，设置**高级银行对帐**选项为**是**。
4.  将**对账单格式**字段设置为之前创建的格式，如 **ISO20022**。

## <a name="set-up-the-import-of-mt940-bank-statements"></a>设置 MT940 银行对账单的导入
首先，您必须通过使用数据实体框架定义 MT940 银行对账单的银行对账单格式处理组。

1.  转到**工作区** &gt; **数据管理**。
2.  单击**导入**。
3.  为格式输入名称，如 **MT940**。
4.  将**源数据格式**字段设置为 **XML-元素**。
5.  将**实体名称**字段设置为**银行对账单**。
6.  若要上载导入文件，请单击**上载**，然后浏览以选择以前保存的 **SampleBankCompositeEntity.xml** 文件。
7.  银行对账单实体上载且映射完成后，请单击实体的**查看地图**操作。
8.  银行对账单实体是由四个单独的实体组成一个复合实体。 在列表中，选择 **BankStatementDocumentEntity**，然后单击**查看地图**操作。
9.  在**转换**选项卡上，单击**新建**。
10. 对于序列号 1，请单击**上载文件**，并选择以前保存的 **MT940TXT-to-MT940XML.xslt** 文件。
11. 单击“**新建**”。
12. 对于序列号 2，请单击**上载文件**，并选择以前保存的 **MT940XML-to-Reconciliation.xslt** 文件。 **注意︰** Finance and Operations 转换文件使用标准格式构建。 因为银行经常偏离这种格式，您可能必须更新要映射到您的银行帐单格式的转换文件。 <!--- For details about the expected format for MT940, see [Dynamics AX MT940 Layout](./media/dynamicsaxmt940layout1.xlsx)-->
13. 单击**新建**。
14. 对于序列号 3，请单击**上载文件**，并选择以前保存的 **BankReconciliation-to-Composite.xslt** 文件。
15. 单击**应用转换**。

设置格式处理组后，下一步是定义 MT940 银行对账单的银行对账单格式规则。

1.  转到**现金和银行管理** &gt; **设置** &gt; **高级银行对帐设置** &gt; **银行对账单格式**。
2.  单击**新建**。
3.  指定对账单格式，如 **MT940**。
4.  输入格式名称。
5.  将**处理组**字段设置为之前定义的组，如 **MT940**。
6.  将**文件类型**字段设置为 **txt**。

最后一步是启用高级银行对帐并设置银行帐户的对账单格式。

1.  转 **“现金和银行管理** &gt; **银行帐户**。
2.  选择银行帐户并打开帐户以查看详细信息。
3.  在**对帐**选项卡上，设置**高级银行对帐**选项为**是**。
4.  当提示您确认您的选择并启用高级银行对帐时，请单击**确定**。
5.  将**对账单格式**字段设置为之前创建的格式，如 **MT940**。

## <a name="set-up-the-import-of-bai2-bank-statements"></a>设置 BAI2 银行对账单的导入
首先，您必须通过使用数据实体框架定义 BAI2 银行对账单的银行对账单格式处理组。

1.  转到**工作区** &gt; **数据管理**。
2.  单击**导入**。
3.  为格式输入名称，如 **BAI2**。
4.  将**源数据格式**字段设置为 **XML-元素**。
5.  将**实体名称**字段设置为**银行对账单**。
6.  若要上载导入文件，请单击**上载**，然后浏览以选择以前保存的 **SampleBankCompositeEntity.xml** 文件。
7.  银行对账单实体上载且映射完成后，请单击实体的**查看地图**操作。
8.  银行对账单实体是由四个单独的实体组成一个复合实体。 在列表中，选择 **BankStatementDocumentEntity**，然后单击**查看地图**操作。
9.  在**转换**选项卡上，单击**新建**。
10. 对于序列号 1，请单击**上载文件**，并选择以前保存的 **BAI2CSV-to-BAI2XML.xslt** 文件。
11. 单击“**新建**”。
12. 对于序列号 2，请单击**上载文件**，并选择以前保存的 **BAI2XML-to-Reconciliation.xslt** 文件。 **注意︰** Finance and Operations 转换文件使用标准格式构建。 因为银行经常偏离这种格式，您可能必须更新要映射到您的银行帐单格式的转换文件。 <!--- For details about the expected format for BAI2, see [Dynamics AX BAI2 Layout](./media/dynamicsaxbai2layout1.xlsx).-->
13. 单击**新建**。
14. 对于序列号 3，请单击**上载文件**，并选择以前保存的 **BankReconciliation-to-Composite.xslt** 文件。
15. 单击**应用转换**。

设置格式处理组后，下一步是定义 BAI2 银行对账单的银行对账单格式规则。

1.  转到**现金和银行管理** &gt; **设置** &gt; **高级银行对帐设置** &gt; **银行对账单格式**。
2.  单击**新建**。
3.  指定对账单格式，如 **BAI2**。
4.  输入格式名称。
5.  将**处理组**字段设置为之前定义的组，如 **BAI2**。
6.  将**文件类型**字段设置为 **txt**。

最后一步是启用高级银行对帐并设置银行帐户的对账单格式。

1.  转 **“现金和银行管理** &gt; **银行帐户**。
2.  选择银行帐户并打开帐户以查看详细信息。
3.  在**对帐**选项卡上，设置**高级银行对帐**选项为**是**。
4.  当提示您确认您的选择并启用高级银行对帐时，请单击**确定**。
5.  将**对账单格式**字段设置为之前创建的格式，如 **BAI2**。

## <a name="test-the-bank-statement-import"></a>测试银行对账单导入
最后一步是测试您是否可以导入银行对账单。

1.  转 **“现金和银行管理** &gt; **银行帐户**。
2.  选择为其启用高级银行对帐功能的银行帐户。
3.  在**对帐**选项卡上，单击**银行对账单**。
4.  在**银行对账单**页面上，单击**导入对账单**。
5.  将**银行帐户**字段设置为所选银行帐户。 **对账单格式**字段会自动设置，根据银行帐户的设置。
6.  单击**浏览**，然后选择您的电子银行对账单文件。
7.  单击“**上载**”。
8.  单击“**OK**”。

如果导入成功，您将收到一条消息，指出您的对账单被导入。 如果导入不成功，在**数据管理**工作区，在**作业历史记录**部分，找到该作业。 单击作业的**执行详细信息**打开**执行摘要**页，然后单击**查看执行日志**查看导入错误。




