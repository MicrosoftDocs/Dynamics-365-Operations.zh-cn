---
title: 预订销售价
description: 在您创建某一预订时，销售价将从在“销售价(预订)”窗体中创建的销售价设置中导出。
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASalespriceSubscription
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5e18690f7e9b790ecbd0ac0de1955fc95ab1f082
ms.sourcegitcommit: 2ebea3cbddfa0a5ef0e0fd13d3693da6152bc288
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/30/2019
ms.locfileid: "352152"
---
# <a name="subscription-sales-prices"></a>预订销售价   

[!include [banner](../includes/banner.md)]


在您创建某一预订时，销售价将从在**销售价(预订)** 窗体中创建的销售价设置中导出。

在**销售价(预订)** 窗体中，您可以为特定的预订创建销售价，或者可以创建更广泛应用的销售价。 对于要应用于某一预订的销售价，预订的期间代码和币种必须与期间代码和该销售价的币种相同。

如果预订和销售价的期间代码和币种完全相同，则将基于在下表中列出的优先级选择预订销售价。 表中的空电池表示空字段，X 表示值等于从其生成交易记录的预订中的值。

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p>优先级 </p></th>
<th><p><strong>类别</strong></p></th>
<th><p><strong>项目 ID</strong></p></th>
<th><p><strong>预订</strong></p></th>
<th><p><strong>销售币种</strong></p></th>
<th><p><strong>期间代码</strong></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="even">
<td><p>4</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="odd">
<td><p>5</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="even">
<td><p>6</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="odd">
<td><p>7</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="even">
<td><p>8</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
</tbody>
</table>


在创建预订费用时，具有最高详细级别的销售价（如上表中所述）将选作预订销售价。

## <a name="update-and-index-subscription-sales-prices"></a>对预订销售价进行更新并编制索引

您可以通过更新基价或指数，更新预订销售价。 您可以按百分比更新，或者更新为新值。

## <a name="subscription-fee-sales-prices"></a>预订费用销售价

在您创建预订费用时，销售价将基于预订的销售价设置。 您可以通过预订价格设置来使用基价，或者可以创建指数形式的销售价。

## <a name="example"></a>示例

您想要为新项目 9030 设置 EUR 500 的预订销售价。 在**销售价(预订)** 窗体中，可按照下表所示创建预订销售价。

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><p>生效日期</p></th>
<th><p>类别</p></th>
<th><p>项目</p></th>
<th><p>预订</p></th>
<th><p>期间代码</p></th>
<th><p>销售币种</p></th>
<th><p>销售价</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>28-08-2006</p></td>
<td></td>
<td><p>9030</p></td>
<td></td>
<td><p>月</p></td>
<td><p>欧元</p></td>
<td><p>500</p></td>
</tr>
</tbody>
</table>


请注意，**类别**字段和**预订**字段为空。

然后，您创建以下预订。

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p>服务预订</p></th>
<th><p>项目</p></th>
<th><p>预订组</p></th>
<th><p>类别</p></th>
<th><p>币种</p></th>
<th><p>期间代码</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>00020_135</p></td>
<td><p>9030</p></td>
<td><p>Sub1</p></td>
<td><p>SubCat1</p></td>
<td><p>欧元</p></td>
<td><p>每月</p></td>
</tr>
<tr class="even">
<td><p>00021_135</p></td>
<td><p>9030</p></td>
<td><p>Sub1</p></td>
<td><p>SubCat2</p></td>
<td><p>欧元</p></td>
<td><p>每月</p></td>
</tr>
</tbody>
</table>


现在，您为预订组 Sub1 中的两个预订都创建了预订费用：

1.  单击**服务管理** \> **设置** \> **服务预订** \> **预订组**。

2.  在**预订组**窗体中，单击**功能** \> **创建预订费用**。

3.  在**创建预订费用**窗体中，输入相应信息。 有关详细信息，请参阅[创建预订费用交易记录](create-subscription-fee-transactions.md)。

为两个预订创建具有 EUR 500 销售价的费用，如下表中所示。

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p>项目日期</p></th>
<th><p>服务预订</p></th>
<th><p>项目</p></th>
<th><p>类别</p></th>
<th><p>开始日期</p></th>
<th><p>结束日期</p></th>
<th><p>销售币种</p></th>
<th><p>销售价</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>28-08-2006</p></td>
<td><p>00020_135</p></td>
<td><p>9030</p></td>
<td><p>SubCat1</p></td>
<td><p>01-01-2007</p></td>
<td><p>31-03-2007</p></td>
<td><p>欧元</p></td>
<td><p>500</p></td>
</tr>
<tr class="even">
<td><p>28-08-2006</p></td>
<td><p>00021_135</p></td>
<td><p>9030</p></td>
<td><p>SubCat2</p></td>
<td><p>01-01-2007</p></td>
<td><p>31-03-2007</p></td>
<td><p>欧元</p></td>
<td><p>500</p></td>
</tr>
</tbody>
</table>


以后，您决定要为项目 9030 的类别 SubCat1 指定销售价。 因此，您创建一个新的销售价行，该行具有针对项目 9030 和费用类别 SubCat1 的组合的 EUR 550 的销售价。 现在项目 9030 存在两个预订销售价行，如下表中所示。

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><p>生效日期</p></th>
<th><p>类别</p></th>
<th><p>项目</p></th>
<th><p>预订</p></th>
<th><p>期间代码</p></th>
<th><p>货币</p></th>
<th><p>销售价</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>28-08-2007</p></td>
<td></td>
<td><p>9030</p></td>
<td></td>
<td><p>月</p></td>
<td><p>欧元</p></td>
<td><p>500</p></td>
</tr>
<tr class="even">
<td><p>28-08-2007</p></td>
<td><p>SubCat1</p></td>
<td><p>9030</p></td>
<td></td>
<td><p>月</p></td>
<td><p>欧元</p></td>
<td><p>550</p></td>
</tr>
</tbody>
</table>


您重复执行上述过程，以便为预订组 Sub1 中的两个预订都创建预订费用。 下表显示为每个预订创建的附加到该预订组的交易记录。

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p>项目日期</p></th>
<th><p>预订</p></th>
<th><p>项目</p></th>
<th><p>类别</p></th>
<th><p>开始日期</p></th>
<th><p>结束日期</p></th>
<th><p>销售币种</p></th>
<th><p>销售价</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>28-07-2007</p></td>
<td><p>00020_135</p></td>
<td><p>9030</p></td>
<td><p>SubCat1</p></td>
<td><p>01-01-2008</p></td>
<td><p>31-03-2008</p></td>
<td><p>欧元</p></td>
<td><p>550</p></td>
</tr>
<tr class="even">
<td><p>28-07-2008</p></td>
<td><p>00021_135</p></td>
<td><p>9030</p></td>
<td><p>SubCat2</p></td>
<td><p>01-01-2008</p></td>
<td><p>31-03-2008</p></td>
<td><p>欧元</p></td>
<td><p>500</p></td>
</tr>
</tbody>
</table>


在预订 00020\_135 的第一个交易记录中，EUR 550 的销售价从为特定项目和类别的组合设置的预订销售价中导出。 在预订 00021\_135 的第二个交易记录中，EUR 500 的销售价用作项目预订销售价，因为不存在为项目 9030 和类别 SubCat2 的组合设置的价格。

## <a name="see-also"></a>请参阅

[对预订销售价进行更新并编制索引](update-and-index-subscription-sales-prices.md)

  


