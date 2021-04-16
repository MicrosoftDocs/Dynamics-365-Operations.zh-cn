---
title: 在 RCS 全局知识库中停用配置
description: 本主题描述如何在 RCS 全局知识库中停用配置。
author: JaneA07
ms.date: 02/17/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2021-02-02
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 25ad0744e7c3320505c13c465d440b6a364da47c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840284"
---
# <a name="discontinue-configurations-in-the-rcs-global-repository"></a>在 RCS 全局知识库中停用配置

[!include [banner](../includes/banner.md)]

本主题描述如何在 RCS 全局知识库中停用配置。 以前，只能删除不再需要的配置。 但是，您现在可以在 RCS 全局知识库中将已发布的配置标记为 **已停用**。 使用此功能，您还可以执行以下操作： 
 
 - 计划停用配置时提供预先通知。
 - 包括有关替换配置的适用详细信息。
 - 为特定配置设置一个 **支持截止日期**，以通知用户何时停用该配置。

停用配置版本时，可以指定以下可选信息：

  - **替换配置**
  - **替换配置版本**
  - **自由文本注释**：使用此字段可提供文档链接或参考
  - **支持截止日期**：此字段提供当前配置/版本的建议支持截止日期。 此日期必须手动更新。
  
要停用配置，请完成以下步骤。 

1. 通过将 **所有版本** 设置为 **是**，选择在一次操作中是要停用单个版本，还是要停用具有相同设置的所有版本。 
2. 将 **停用** 参数设置为 **是**。
3. 选择 **确定** 以停用配置。 保存更改时，将填充 **停用日期** 字段。

![停用配置信息](media/Discontinue-details-2.png)
  
您可以将配置恢复为 **共享**，或者可以随时调整停用信息。 如果您共享配置，请指定 **支持截止日期** 以及与停用有关的所有其他信息，以表明您计划将来停用。

如果您要共享有关计划停用的信息，则在实际停用配置之前，用户可以预填写与替换有关的所有字段，但可以将 **停用** 参数设置为 **否**。

> [!NOTE]
> 停用不限制配置的相关操作。 您可以继续导入、运行或导出配置，这些字段仅供参考。

## <a name="finance-supports-displaying-this-information-starting-in-version-10014"></a>财务支持从版本 10.0.14 开始显示此信息

从版本 10.0.14 开始，Dynamics 365 Finance 支持显示停用信息。 在 **全局知识库** 页面上，您可以查看与停用有关的最新信息。 默认情况下，停用的配置会被过滤掉。
  
**导入的配置** (ERSolutionTable) 页面显示导入时已经停用的配置。 对于在导入后停用的那些配置，可以通过运行 **导入配置更新** 作业来同步停用信息。


