---
title: 在供应商设计之间切换
description: 本主题介绍如何在 Finance and Operations 应用与 Dataverse 之间切换供应商数据集成。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 78d4c547f544d95c66490e5610374a5c4598b266
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565591"
---
# <a name="switch-between-vendor-designs"></a>在供应商设计之间切换

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



## <a name="vendor-data-flow"></a>供应商数据流 

如果您选择使用 **客户** 表来存储 **组织** 类型的供应商，使用 **联系人** 表来存储 **个人** 类型的供应商，请配置以下工作流。 否则，不需要此配置。

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a>对“组织”类型的供应商使用扩展的供应商设计

**Dynamics365FinanceExtended** 解决方案包包含以下工作流程模板。 您将为每个模板创建工作流。

+ 在“客户”表中创建供应商
+ 在“供应商”表中创建供应商
+ 在“客户”表中更新供应商
+ 在“供应商”表中更新供应商

要使用工作流程模板创建新的工作流程，请按照以下步骤操作。

1. 为 **供应商** 表创建工作流程，然后选择 **在“客户”表中创建供应商** 工作流程模板。 然后选择 **确定**。 此工作流处理 **客户** 表的供应商创建方案。

    ![在“客户”表中创建供应商工作流程](media/create_process.png)

2. 为 **供应商** 表创建工作流程，然后选择 **在“客户”表中更新供应商** 工作流程模板。 然后选择 **确定**。 此工作流处理 **客户** 表的供应商更新方案。
3. 为 **客户** 表创建工作流程，然后选择 **在“供应商”表中创建供应商** 工作流程模板。
4. 为 **客户** 表创建工作流程，然后选择 **在“供应商”表中更新供应商** 工作流程模板。
5. 您可以根据需要将工作流配置为实时工作流或后台工作流。 要将工作流配置为后台工作流，请选择 **转换为后台工作流**。

    ![“转换为后台工作流”按钮](media/background_workflow.png)

6. 启用您为 **客户** 和 **供应商** 表创建的工作流，以开始使用 **客户** 表存储 **组织** 类型的供应商信息。

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a>对“个人”类型的供应商使用扩展的供应商设计

**Dynamics365FinanceExtended** 解决方案包包含以下工作流程模板。 您将为每个模板创建工作流。

+ 在“供应商”表中创建“个人”类型的供应商
+ 在“联系人”表中创建“个人”类型的供应商
+ 在“联系人”表中更新“个人”类型的供应商
+ 在“供应商”表中更新“个人”类型的供应商

要使用工作流程模板创建新的工作流程，请按照以下步骤操作。

1. 为 **供应商** 表创建工作流程，然后选择 **在“联系人”表中创建“个人”类型的供应商** 工作流程模板。 然后选择 **确定**。 此工作流处理 **联系人** 表的供应商创建方案。
2. 为 **供应商** 表创建工作流程，然后选择 **在“联系人”表中更新“个人”类型的供应商** 工作流程模板。 然后选择 **确定**。 此工作流处理 **联系人** 表的供应商更新方案。
3. 为 **联系人** 表创建工作流程，然后选择 **在“供应商”表中创建“个人”类型的供应商** 模板。
4. 为 **联系人** 表创建工作流程，然后选择 **在“供应商”表中更新“个人”类型的供应商** 模板。
5. 您可以根据需要将工作流配置为实时工作流或后台工作流。 要将工作流配置为后台工作流，请选择 **转换为后台工作流**。
6. 启用您在 **联系人** 和 **供应商** 表上创建的工作流，以开始使用 **联系人** 表存储 **个人** 类型的供应商信息。


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]