---
title: 改进预测模型
description: 本主题介绍可用于改善预测模型性能的功能。
author: ShivamPandey-msft
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: de753eda43cb358dfa9edc76f102d4b268291b4e
ms.sourcegitcommit: 822aea26c5da259efe11ff3b3dc4cf1598425689
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/16/2021
ms.locfileid: "7386430"
---
# <a name="improve-the-prediction-model"></a>改进预测模型

[!include [banner](../includes/banner.md)]

本主题介绍可用于改善预测模型性能的功能。 您开始在 Microsoft Dynamics 365 Finance 中的 **客户付款预测** 工作区中开始改进模型。 然后在 AI Builder 中完成改进步骤。

## <a name="select-historical-outcomes"></a>选择历史结果

您首先选择三种可能的发票结果中的一个或多个：**按时**、**逾期** 和 **严重逾期**。 应选择所有三个结果。 如果您清除任何结果的选择，发票将被从训练过程中筛选掉，并且预测的准确性将降低。

[![确认结果。](./media/confirm-3-outcomes.png)](./media/confirm-3-outcomes.png)

如果您的组织仅需要两个结果，则将 **逾期** 和 **严重逾期** 阈值设置为 0（零）天。 这样，您可以有效地将预测折叠为二进制状态 **按时** 或 **逾期**。

## <a name="select-fields"></a>选择字段

当您选择要包含在模型中的字段时，请注意列表包含了映射到 Azure 数据湖中的数据的 Microsoft Dataverse 表中的所有可用字段。 **不** 应选择其中一些字段。 不应选择的字段属于以下三类之一：

- 该字段是 Dataverse 表的必填字段，但在数据湖中没有其支持数据。
- 该字段是一个 ID，因此对于机器学习功能没有意义。
- 该字段表示在预测期间将不可用的信息。

以下各节显示了可用于发票和客户实体的字段，并列出了 **不** 应选中进行训练的字段。 为每个字段指定的类别是指前面列表中的类别。
 
### <a name="invoice-dataverse-table"></a>发票 Dataverse 表

下图显示可用于发票表的字段。

[![发票表的可用字段。](./media/available-fields.png)](./media/available-fields.png)

不应选择以下字段进行训练：

- **发票科目**（类别 2）
- **已结**（类别 3）– 此字段用于筛选要训练的发票（已结）和预测（未结）。
- **名称**（类别 1）
- **源 Id**（类别 2）
- **源记录**（类别 2）
- **源表**（类别 2）

### <a name="customer-dataverse-table"></a>客户 Dataverse 表

下图显示可用于客户表的字段。

[![客户表的可用字段。](./media/related-entities.png)](./media/related-entities.png)

不应选择以下字段进行训练：

- **行唯一键**（类别 2）

## <a name="filters"></a>筛选器

您可以通过为发票上或客户表中的字段设置筛选条件来筛选用于培训的发票。 例如，您可以设置一个阈值以仅包括总金额等于或超过特定金额的发票。 或者，您可以排除与特定客户组中的客户关联的发票。

有关筛选数据的详细信息，请参阅[创建预测模型](https://docs.microsoft.com/ai-builder/prediction-create-model#filter-your-data)。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
