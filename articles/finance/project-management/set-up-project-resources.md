---
title: 设置项目资源
description: 本主题提供有关设置或请求项目资源的信息。
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c882e23794e3937f85b3e73774b36deaf28ac3ed
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760488"
---
# <a name="set-up-project-resources"></a>设置项目资源

[!include [banner](../includes/banner.md)]

您必须设置日历并将其与员工或工作人员关联。 该日历用于计划项目和预留给该项目的资源的工作时间。 在日历设置期间，项目经理可以作为资源优化的一部分执行资源均衡。 基于日历安排，可以对资源设定限制。 可以在**日历**页中设置日历。

将工作人员设置为项目资源时，可以从您为其设置资源的公司中工作的工作人员中进行选择。 或者也可以从您的组织中的其他公司中选择工作人员。 这些工作人员被称为内部公司资源。

以下过程阐述了如何将工作人员设置为贵公司中的项目资源以及如何设置内部公司项目资源。

## <a name="set-up-a-worker-as-a-project-resource"></a>将工作人员设置为项目资源

1. 在**工作人员**页的**工作人员**列表内，选择您添加为项目资源的工作人员，然后打开工作人员记录。
2. 在操作窗格中，选择**项目** &gt; **设置** &gt; **项目设置**。
3. 选择日历，然后关闭页面。

您还可以将资源的默认项目指定为预分配类型。 当资源经理或项目经理知道资源将提前处理哪些项目时，可以使用预分配。 预分配还可以基于项目赞助者或客户的请求。 要预分配一个项目，在**分配项目**页上，在**项目**选项卡上，在**其余项目**列表中，选择相应的项目。

## <a name="set-up-an-intercompany-resource"></a>设置内部公司资源

将工作人员设置为内部公司资源时，必须完成借出公司和借入公司中的设置。

### <a name="in-the-lending-company"></a>在借出公司中

1. 在 Finance 中，验证已选择借出公司，然后完成上一部分“将工作人员设置为项目资源”中的过程。
2. 在**内部公司会计**页，选择**新建**。
3. 在**法人 ID** 字段中，选择借出公司。 根据需要填写其余字段，然后选择**保存**。
4. 在**转让价格**页，选择**新建**。
5. 在**借入实体**字段中，选择适当的公司。
6. 如果要仅借给借入公司您在此部分开始时创建的资源，请在**资源**字段中选择您创建的资源的名称。 如果要将公司内的所有资源都提供给借入公司，请将**资源**字段保留为空。
7. 在**项目管理与核算参数**页的**内部公司**选项卡上，将**启用公司间资源计划编制和工时单**选项设置为**是**。

### <a name="in-the-borrowing-company"></a>在借入公司中

- 在**资源列表**页上的搜索筛选器中，输入您为借出公司创建的资源名称，以验证借入公司的资源列表中是否包含此名称。

## <a name="request-project-resources"></a>请求项目资源
项目资源计划功能仅支持资源经理为约定或项目分配雇用资源。 若要启用此功能，请完成以下任务，或验证是否已完成这些任务：

- 设置编号规则。
- 设置项目管理与核算工作流。
- 启用资源请求工作流。

完成前面的任务后，可以根据需要完成下面的任务：

- 从软性预订雇用资源创建资源请求。
- 监控资源请求。
- 实施资源请求。
- 从 WBS 请求雇用资源。
- 在不请求雇用资源的情况下为项目预订资源。
