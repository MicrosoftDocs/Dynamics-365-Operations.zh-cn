--- 
title: "创建供应商帐户"
description: "该过程会显示如何创建供应商帐户，以及添加地址和联系信息。"
author: mkirknel
manager: AnnBe
ms.date: 06/06/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6ff2357d5266c45be2f403e463c72089d73db21b
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-vendor-account"></a>创建供应商帐户

[!include [task guide banner](../../includes/task-guide-banner.md)]

该过程会显示如何创建供应商帐户，以及添加地址和联系信息。 该过程不会显示如何填充所有字段，以用于采购和财务目的。 若要了解关于这些字段的更多信息，请阅读字段描述。 您可以使用演示数据公司 USMF，也可使用您自己的数据运行该过程。 供应商帐户通常由采购专业人员或应收账款人员创建。


## <a name="create-a-vendor-account"></a>创建供应商帐户
1. 转到“采购”>“供应商”>“所有供应商”。
2. 单击“新建”。
3. 在“供应商帐户”字段中，输入一个供应商帐户。
    * 值可以自动填充。 如果是这样，您可以跳过此步骤。  
    * 您可以为某个人或组织创建供应商帐户。 这将影响到哪些字段可用。 在此示例中，我们将为一个组织创建供应商帐户。   
4. 在“名称”字段中，输入或选择一个值。
    * 如果您的供应商在您的系统中是已登记的当事方，您可以使用下拉功能，在此字段中选择他们，并且新的供应商帐户将会继承已登记的地址和联系信息。  
5. 在“组”字段中，输入或选择一个值。
    * 供应商组用于对具有以下任何共同参数的供应商进行分组：“付款条款”、结算期间、库存过帐会计科目（包括销售税组）、默认会计科目、产品筛选器代码或供应预测配置。  
6. 在“员工数量”字段中，输入一个数字。
7. 在“组织数量”字段中，键入一个值。

## <a name="add-an-address"></a>添加地址
1. 展开“地址”部分。
2. 单击“添加”。
3. 在“用途”字段中，输入或选择一个值。
    * 您可以选择一个或多个用途。 这些用于为指定用途选择正确的地址。 例如，如果用途是“发票”，则在您发送发票时将使用该地址。  
4. 在“名称”或“描述”字段中，键入一个值。
5. 在“国家/地区”字段中，输入或选择一个值。
    * 输入地址详情。 您选定的国家/地区将确定您使用与该国家/地区对应的地址格式显示的字段。   
6. 单击“确定”。

## <a name="add-contact-information"></a>添加联系信息
1. 单击“添加”。
2. 在“描述”字段中，键入一个值。
3. 在“类型”字段中，选择一个选项。
4. 在“联系电话/地址”字段中，键入一个值。
    * 如果这是主要联系人，您可以选中“主要”复选框。  
5. 单击“保存”。
6. 关闭该页面。
7. 关闭该页面。


