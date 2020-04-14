---
title: 费用收据处理
description: 本主题提供有关收据的光学字符识别 (OCR) 处理的信息。 此功能适合在 Microsoft Dynamics 365 Finance 中创建费用报表时改善用户体验。
author: stsporen
manager: AnnBe
ms.date: 11/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 49cdfeac8cda9f1ddd3aca61f902f00f30f3485b
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154032"
---
# <a name="expense-receipt-processing"></a>支出收据处理

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


通过为收据引入光学字符识别 (OCR) 处理，费用录入得到了增强。 此功能适合在创建费用报表时改善用户体验。

## <a name="key-features"></a>主要功能

- 从收据中提取商户名称、日期和总金额。
- 该功能尝试将未附加的收据与未附加的费用交易记录匹配。
- 用户可以根据收据创建手动输入的费用交易记录。

## <a name="usage-examples"></a>用法示例

- **自动附加创建费用报表时包括信用卡交易记录的收据。**

    1. 打开**费用管理**工作区。
    2. 在**收据**选项卡上，验证是否存在未附加的收据。 您也可以在**收据**选项卡上上传收据。
    3. 在**费用**选项卡上，验证是否存在未附加的费用。 通常，费用管理员会从信用卡提供商处导入这些费用。
    4. 选择**新建费用报表**。 请注意，当您创建费用报表时，现在还可以包括费用和收据。 如果同时添加费用和收据，则会触发按费用自动匹配收据。

- **创建费用，或匹配收据中的费用。**

    1. 在费用报表中的**收据**选项卡上，选择**添加收据**来附加收据。
    2. 在上传的收据图像下面，注意**创建**和**匹配**选项。

        - 选择**创建**以创建手动输入的费用交易记录并填写从收据中提取的值。
        - 如果选择**匹配**，系统会尝试将现有费用与收据进行匹配。

## <a name="installation"></a>安装

此功能与**已重构的费用报表**功能联合使用，有助于简化费用体验。

要使用这些高级费用功能，请安装 Microsoft Dynamics 365 Finance 费用管理服务加载项，然后在实例中打开这些功能。 您可以在 Microsoft Dynamics Lifecycle Services (LCS) 中从您的项目访问加载项。

1. 登录到 LCS，然后打开所需的环境。
2. 转到**完整详细信息**。
3. 选择**维护**，或向下滚动到**环境加载项**快速选项卡。
4. 选择**安装新加载项**。
5. 选择**费用管理服务**。
6. 按照安装指南操作，并同意条款和条件。
7. 选择**安装**。

在**功能管理**工作区中，开启以下功能：

- 已重构的费用报表
- 自动匹配并从收据创建支出

开启这些功能时，将执行以下操作：

- 现有**费用管理**工作区已替换为新工作区。
- 为费用字段可见性添加一个新菜单项。
- 您仍然可以打开以前的**费用报告**页面，方法是转到**费用管理 > 我的费用 > 费用报告**。
- 工作流和所有审核仍然会将您带到现有费用报表页。
- 收据将通过 Microsoft Azure Cognitive Services 务得到处理，并且将提取和添加元数据。
- 添加了一个选项，使您可以创建一个包含匹配的未附加收据的费用报表。
- 添加到费用报告中的选项使您可以从收据创建费用行，或尝试将现有收据与现有费用行进行匹配。

有关已重构的费用报表功能的更多信息，请参见[已重构的费用报表](ExpenseWorkspaceNew.md)。

## <a name="frequently-asked-questions"></a>常见问题

**Microsoft 是否将我的数据用于其模型？**

否，Microsoft 已经为其收据处理服务建立了通用机器学习模型。 此模型并不基于您上传的收据。

**在哪里可以使用和处理此功能？**

目前，支持在美国使用。

**我的收据去哪里了？**

Finance 将与 Cognitive Services 联系以提取字段数据。 进行处理时，Cognitive Services 将您的收据副本最多保留 24 小时。 处理完成后，Cognitive Services 将删除收据。 收据仍存储在 Finance 中。

有关更多信息，请参见[使用 Form Recognizer 的新功能实现收据了解](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/)。
