---
title: 设置高级银行对帐导入流程
description: 高级银行对帐功能让您可以导入电子银行对帐单，并可以将其与 Microsoft Dynamics 365 Finance 中的银行交易记录自动对帐。 本文介绍如何设置银行对账单的导入功能。
author: panolte
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: roschlom
ms.custom: 106853
ms.assetid: 45dae275-ea45-4c7e-b38f-89297c7b5352
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 22d173f6ced2af3e8023bd40f70ca70728c3a0a7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834972"
---
# <a name="set-up-the-advanced-bank-reconciliation-import-process"></a>设置高级银行对帐导入流程

[!include [banner](../includes/banner.md)]

高级银行对帐功能让您可以导入电子银行对帐单，并可以将其与 Dynamics 365 Finance 中的银行交易记录自动对帐。 本文介绍如何设置银行对账单的导入功能。 

银行对账单导入设置因您电子银行对账单的格式的不同而不同。 Finance 支持三个现成的银行对账单格式︰ISO20022、MT940 和 BAI2。

## <a name="set-time-zone-preference"></a>设置时区首选项
配置银行对帐单导入设置时，务必注意将导入的银行对帐单文件内的日期时间数据的时区。 默认假设所有日期和时间值均为协调世界时 (UTC)，因此导入数据时不应用时区转换。 

提供了一个选项，用于指定导入数据时要使用的时区。 此选项位于每个 **源数据格式详细信息** 页（**数据管理工作区 > 配置数据源 > 选择数据格式 > 区域设置** 快速选项卡）中的 **时区首选项** 字段内。 您输入的这个时区首选项将应用于所有使用该源数据格式的导入。 可根据从多个时区导入数据的需要创建任意数量的数据源格式。  

此时区可能与用户或公司的时区不同，因此请务必分辨清楚日期和时间数据正在使用哪个时区。 建议在设置时区首选项时注意以下事项。 

 - 时区首选项将应用于所有使用该源数据格式的导入。 可根据处理从多个时区导入数据的需要创建任意数量的数据源格式。 
 
 - 时区首选项应该是导入文件中的日期和时间数据的本地时区。 
 
 - 日期和时间数据的时区可能与用户或公司的时区不同。
 
 - 用户可以使用 **用户选项** 调整自己的时区。

请注意，导入银行对帐单时，以下操作可帮助将潜在的日期和时间冲突降到最少。 

 - 避免更改已经导入了对帐单的任何银行帐户的时区首选项。 因为时区调整，更改时区首选项可能会影响新对帐单相对现有对帐单的排序。 
 
 - 查看所有使用所选数据源格式的导入。 为该格式指定的时区首选项将应用于所有使用该格式的导入项目。 验证时区首选项适合所有使用该格式的导入项目。

## <a name="sample-files"></a>示例文件
对于所有三种格式，您必须有将电子银行对帐单的原始格式转换为 Finance 可以使用的格式的文件。 您可以在 Microsoft Visual Studio 中应用程序资源管理器的 **资源** 节点下找到所需资源文件。 找到文件后，将它们复制到一个已知位置，以便您可以更轻松地在设置流程中上载它们。

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
下面是高级银行对帐导入文件技术布局定义的示例和三个相关银行对帐单示例文件：[导入文件示例](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)  

| 技术布局定义                             | 银行对账单示例文件          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout                                   | [MT940StatementExample](//download.microsoft.com/download/2/d/c/2dcc4e55-ddc8-4a74-b79c-250fae201c3c/mt940StatementExample.txt)                |
| DynamicsAXISO20022Layout                                | [ISO20022StatementExample](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdownload.microsoft.com%2Fdownload%2F1%2F5%2F5%2F155d84ed-c250-48f3-b0b1-c5a431e7855b%2FISO20022-MultipleStatements.xml&data=04%7C01%7CRobert.Schlomann%40microsoft.com%7C30d0c233cb6546547d0a08d8f4965edc%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637528273956712775%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=3VzvLZK%2BO8PjuI7XVdC6rD2j3nUJfteo7zFp%2B1s9BwM%3D&reserved=0)             |
| DynamicsAXBAI2Layout                                    | [BAI2StatementExample](//download.microsoft.com/download/1/1/6/11693f57-bfc1-4993-a274-5fb978be70fa/BAI2StatementExample.txt)                 |



## <a name="set-up-the-import-of-iso20022-bank-statements"></a>设置 ISO20022 银行对账单的导入
首先，您必须通过使用数据实体框架定义 ISO20022 银行对账单的银行对账单格式处理组。

1.  转到 **工作区** &gt; **数据管理**。
2.  单击 **导入**。
3.  为格式输入名称，如 **ISO20022**。
4.  将 **源数据格式** 字段设置为 **XML-元素**。
5.  将 **实体名称** 字段设置为 **银行对账单**。
6.  若要上载导入文件，请单击 **上载**，然后浏览以选择以前保存的 **SampleBankCompositeEntity.xml** 文件。
7.  银行对账单实体上载且映射完成后，请单击实体的 **查看地图** 操作。
8.  银行对账单实体是由四个单独的实体组成一个复合实体。 在列表中，选择 **BankStatementDocumentEntity**，然后单击 **查看地图** 操作。
9.  在 **转换** 选项卡上，单击 **新建**。
10. 对于序列号 1，请单击 **上载文件**，并选择以前保存的 **ISO20022XML-to-Reconciliation.xslt** 文件。 **注意︰** 转换文件使用标准格式构建。 因为银行经常偏离这种格式，您可能必须更新要映射到您的银行帐单格式的转换文件。 <!-- For details about the expected format for ISO20022, see [Dynamics AX ISO20022 Layout](./media/dynamicsaxiso20022layout1.xlsx).-->
11. 单击 **新建**。
12. 对于序列号 2，请单击 **上载文件**，并选择以前保存的 **BankReconciliation-to-Composite.xslt** 文件。
13. 单击 **应用转换**。

设置格式处理组后，下一步是定义 ISO20022 银行对账单的银行对账单格式规则。

1.  转到 **现金和银行管理** &gt; **设置** &gt; **高级银行对帐设置** &gt; **银行对账单格式**。
2.  单击 **新建**。
3.  指定对账单格式，如 **ISO20022**。
4.  输入格式名称。
5.  将 **处理组** 字段设置为之前定义的组，如 **ISO20022**。
6.  选中 **XML 文件** 复选框。

最后一步是启用高级银行对帐并设置银行帐户的对账单格式。

1.  转 **现金和银行管理** &gt; **银行帐户**。
2.  选择银行帐户并打开帐户以查看详细信息。
3.  在 **对帐** 选项卡上，设置 **高级银行对帐** 选项为 **是**。
4.  将 **对账单格式** 字段设置为之前创建的格式，如 **ISO20022**。

## <a name="set-up-the-import-of-mt940-bank-statements"></a>设置 MT940 银行对账单的导入
首先，您必须通过使用数据实体框架定义 MT940 银行对账单的银行对账单格式处理组。

1.  转到 **工作区** &gt; **数据管理**。
2.  单击 **导入**。
3.  为格式输入名称，如 **MT940**。
4.  将 **源数据格式** 字段设置为 **XML-元素**。
5.  将 **实体名称** 字段设置为 **银行对账单**。
6.  若要上载导入文件，请单击 **上载**，然后浏览以选择以前保存的 **SampleBankCompositeEntity.xml** 文件。
7.  银行对账单实体上载且映射完成后，请单击实体的 **查看地图** 操作。
8.  银行对账单实体是由四个单独的实体组成一个复合实体。 在列表中，选择 **BankStatementDocumentEntity**，然后单击 **查看地图** 操作。
9.  在 **转换** 选项卡上，单击 **新建**。
10. 对于序列号 1，请单击 **上载文件**，并选择以前保存的 **MT940TXT-to-MT940XML.xslt** 文件。
11. 单击 **新建**。
12. 对于序列号 2，请单击 **上载文件**，并选择以前保存的 **MT940XML-to-Reconciliation.xslt** 文件。 **注意︰** 转换文件使用标准格式构建。 因为银行经常偏离这种格式，您可能必须更新要映射到您的银行帐单格式的转换文件。 <!--- For details about the expected format for MT940, see [Dynamics AX MT940 Layout](./media/dynamicsaxmt940layout1.xlsx)-->
13. 单击 **新建**。
14. 对于序列号 3，请单击 **上载文件**，并选择以前保存的 **BankReconciliation-to-Composite.xslt** 文件。
15. 单击 **应用转换**。

设置格式处理组后，下一步是定义 MT940 银行对账单的银行对账单格式规则。

1.  转到 **现金和银行管理** &gt; **设置** &gt; **高级银行对帐设置** &gt; **银行对账单格式**。
2.  单击 **新建**。
3.  指定对账单格式，如 **MT940**。
4.  输入格式名称。
5.  将 **处理组** 字段设置为之前定义的组，如 **MT940**。
6.  将 **文件类型** 字段设置为 **txt**。

最后一步是启用高级银行对帐并设置银行帐户的对账单格式。

1.  转 **现金和银行管理** &gt; **银行帐户**。
2.  选择银行帐户并打开帐户以查看详细信息。
3.  在 **对帐** 选项卡上，设置 **高级银行对帐** 选项为 **是**。
4.  当提示您确认您的选择并启用高级银行对帐时，请单击 **确定**。
5.  将 **对账单格式** 字段设置为之前创建的格式，如 **MT940**。

## <a name="set-up-the-import-of-bai2-bank-statements"></a>设置 BAI2 银行对账单的导入
首先，您必须通过使用数据实体框架定义 BAI2 银行对账单的银行对账单格式处理组。

1.  转到 **工作区** &gt; **数据管理**。
2.  单击 **导入**。
3.  为格式输入名称，如 **BAI2**。
4.  将 **源数据格式** 字段设置为 **XML-元素**。
5.  将 **实体名称** 字段设置为 **银行对账单**。
6.  若要上载导入文件，请单击 **上载**，然后浏览以选择以前保存的 **SampleBankCompositeEntity.xml** 文件。
7.  银行对账单实体上载且映射完成后，请单击实体的 **查看地图** 操作。
8.  银行对账单实体是由四个单独的实体组成一个复合实体。 在列表中，选择 **BankStatementDocumentEntity**，然后单击 **查看地图** 操作。
9.  在 **转换** 选项卡上，单击 **新建**。
10. 对于序列号 1，请单击 **上载文件**，并选择以前保存的 **BAI2CSV-to-BAI2XML.xslt** 文件。
11. 单击 **新建**。
12. 对于序列号 2，请单击 **上载文件**，并选择以前保存的 **BAI2XML-to-Reconciliation.xslt** 文件。 **注意︰** 转换文件使用标准格式构建。 因为银行经常偏离这种格式，您可能必须更新要映射到您的银行帐单格式的转换文件。 <!--- For details about the expected format for BAI2, see [Dynamics AX BAI2 Layout](./media/dynamicsaxbai2layout1.xlsx).-->
13. 单击 **新建**。
14. 对于序列号 3，请单击 **上载文件**，并选择以前保存的 **BankReconciliation-to-Composite.xslt** 文件。
15. 单击 **应用转换**。

设置格式处理组后，下一步是定义 BAI2 银行对账单的银行对账单格式规则。

1.  转到 **现金和银行管理** &gt; **设置** &gt; **高级银行对帐设置** &gt; **银行对账单格式**。
2.  单击 **新建**。
3.  指定对账单格式，如 **BAI2**。
4.  输入格式名称。
5.  将 **处理组** 字段设置为之前定义的组，如 **BAI2**。
6.  将 **文件类型** 字段设置为 **txt**。

最后一步是启用高级银行对帐并设置银行帐户的对账单格式。

1.  转 **现金和银行管理** &gt; **银行帐户**。
2.  选择银行帐户并打开帐户以查看详细信息。
3.  在 **对帐** 选项卡上，设置 **高级银行对帐** 选项为 **是**。
4.  当提示您确认您的选择并启用高级银行对帐时，请单击 **确定**。
5.  将 **对账单格式** 字段设置为之前创建的格式，如 **BAI2**。

## <a name="test-the-bank-statement-import"></a>测试银行对账单导入
最后一步是测试您是否可以导入银行对账单。

1.  转 **现金和银行管理** &gt; **银行帐户**。
2.  选择为其启用高级银行对帐功能的银行帐户。
3.  在 **对帐** 选项卡上，单击 **银行对账单**。
4.  在 **银行对账单** 页面上，单击 **导入对账单**。
5.  将 **银行帐户** 字段设置为所选银行帐户。 **对账单格式** 字段会自动设置，根据银行帐户的设置。
6.  单击 **浏览**，然后选择您的电子银行对账单文件。
7.  单击 **上载**。
8.  单击 **OK**。

如果导入成功，您将收到一条消息，指出您的对账单被导入。 如果导入不成功，在 **数据管理** 工作区，在 **作业历史记录** 部分，找到该作业。 单击作业的 **执行详细信息** 打开 **执行摘要** 页，然后单击 **查看执行日志** 查看导入错误。





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
