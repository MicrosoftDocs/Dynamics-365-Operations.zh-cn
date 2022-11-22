---
title: 创建成本元素
description: 可通过几种方法在成本核算中创建成本要素。
author: kfend
ms.date: 08/29/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: CAMDimension, CAMAXMainAccountDimensionMemberProviderConfiguration, CAMDimensionMember
ms.openlocfilehash: 0254f486816e852bcda52f90fe4da65c413c7032
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779681"
---
# <a name="create-cost-elements"></a>创建成本元素 

[!include [banner](../../includes/banner.md)]

可通过几种方法在成本核算中创建成本要素。 此过程显示如何通过数据连接器导入主科目来创建成本要素。 用于创建该过程的是演示公司 USMF。 此过程针对 Dynamics 365 for Operations 版本 1611 中增加的成本核算功能。


## <a name="create-new-cost-elements"></a>新建成本要素
1. 转到 **成本核算 > 维度 > 成本要素维度**。
2. 单击 **新建**。
3. 在 **名称** 字段中，键入一个值。
4. 在 **维度成员的数据连接器** 字段中，输入或选择一个值。
5. 在 **描述** 字段中，键入一个值。
6. 单击 **保存**。

## <a name="configure-the-data-connector"></a>配置数据连接器
1. 单击 **配置维度成员提供方**。
2. 在 **会计科目表** 字段中，输入或选择一个值。
    * 选择 **共享** 使用共享的会计科目表。  
3. 单击 **新建**。
4. 在列表中，标记所选的行。
    * 可以为科目应用筛选器以满足条件。  
5. 在 **源主科目** 字段中，输入或选择一个值。
6. 在 **目标主科目** 字段中，输入或选择一个值。
7. 单击 **确定**。

## <a name="import-main-accounts"></a>导入主科目
1. 单击 **导入维度成员**。
    * 将把主科目导入成本核算并用作成本要素。  
2. 单击 **确定**。

## <a name="view-the-imported-accounts-as-cost-elements"></a>将导入的科目作为成本要素查看
1. 单击 **查看维度成员**。
    * 将导入的会计科目作为成本可流向的业务中的成本要素查看。  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
