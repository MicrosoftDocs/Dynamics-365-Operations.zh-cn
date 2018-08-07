--- 
title: "使用物料到达日记帐登记启用了高级仓库的物料"
description: "此过程说明了在使用高级仓库管理流程时如何使用物料到达日记帐登记物料。"
author: ShylaThompson
manager: AnnBe
ms.date: 02/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 050d1fcbc59d9bb3253bfed2433987285423b334
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="register-items-for-an-advanced-warehousing-enabled-item-using-an-item-arrival-journal"></a>使用物料到达日记帐登记启用了高级仓库的物料

[!include [task guide banner](../../includes/task-guide-banner.md)]

此过程说明了在使用高级仓库管理流程时如何使用物料到达日记帐登记物料。 这将通常由一个收料员完成。 

您可以使用 USMF 公司演示数据，也可使用您自己的数据运行该过程。 在开始本指南前，您需要使用未结采购订单行以确认采购订单。 该行上的物料必须进行存储，并且不可使用产品变型，亦不能具有跟踪维度。 并且该物料需要与启用仓库维度组的仓库管理流程关联。 使用的仓库必须启用可供仓库管理流程使用，并且用于接收的库位必须受牌照控制。 如果您使用 USMF，您可以使用公司帐户 1001、仓库 51 和物料 M9200 来创建采购订单。 

记下创建的采购订单的编号，以及用于采购订单行的物料编号库位。


## <a name="create-an-item-arrival-journal-header"></a>创建一个物料到达日记帐标题
1. 转到“物料到达”。
2. 单击“新建”。
3. 在“名称”字段中，键入一个值。
    * 如果您正在使用 USMF，可以键入 WHS。 如果您正在使用其他数据，您选择的日记帐名称必须具有以下属性：“检查领料库位”必须设置为“否”，以及“检验管理”必须设置为“否”。  
4. 在“编号”字段中，输入一个值。
5. 在“站点”字段中，输入一个值。
    * 选择您为采购订单行使用的站点。 这将用作默认值，将默认为日记帐中的所有行。 如果您在 USMF 中使用仓库 51，则选择站点 5。  
6. 在“仓库”字段中，键入一个值。
    * 为所选站点选择有效的仓库。 这将用作默认值，将默认为日记帐中的所有行。 如果您在 USMF 中使用示例值，则选择 51。  
7. 在“地点”字段中，键入一个值。
    * 在所选仓库中选择一个有效库位。 该库位必须与受牌照控制的库位资料有关。 这将用作默认值，将默认为日记帐中的所有行。 如果您在 USMF 中使用示例值，则选择“散装 - 008”。  
8. 右键单击牌照字段的下拉箭头，然后选择“查看详细信息”。
9. 单击“新建”。
10. 在“牌照”字段中，键入一个值。
    * 记录数值。  
11. 单击“保存”。
12. 关闭该页面。
13. 在“牌照”字段中，键入一个值。
    * 输入您刚创建牌照的值。 这将用作默认值，将默认为日记帐中的所有行。  
14. 单击“确定”。

## <a name="add-a-line"></a>添加行
1. 单击“添加行”。
2. 在“项目编号”字段中，输入一个值。
    * 输入您在采购订单行使用的物料编号。  
3. 在“数量”字段中，输入一个数字。
    * 输入您想要登记的数量。  
    * 日期字段确定此现有数量的物料将记入库存的日期。  
    * 如果可从提供的信息个别识别，系统将会自动填充批次 ID。 否则将必须手动添加。 此为必填字段，其将此登记链接到特定原始凭证行。  

## <a name="complete-the-registration"></a>完成登记
1. 单击“验证”。
    * 这会检查准备好供过帐的日记帐。 如果验证失败，需要修复错误才能过帐日记帐。  
2. 单击“确定”。
    * 单击“确定”后，请检查消息。 应该有条消息告知日记帐过帐成功。  
3. 单击“过帐”。
4. 单击“确定”。
    * 单击“确定”后，请检查消息栏。 应该有条消息告知操作成功。  
5. 关闭该页面。


