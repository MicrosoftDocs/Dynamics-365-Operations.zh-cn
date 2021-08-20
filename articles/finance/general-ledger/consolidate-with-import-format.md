---
title: 用于合并的导入格式
description: 本主题提供有关合并多个法人的财务数据时使用的导入格式的详细信息。
author: jinniew
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 6d25ebfedfe748dfa262c1d4b0671539e6150a0f9f05dfca42e87f23486fbb19
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6746408"
---
# <a name="import-format-for-consolidation"></a>用于合并的导入格式

[!include [banner](../includes/banner.md)]

本主题提供有关合并多个法人的财务数据时使用的导入格式的详细信息。 导入格式必须保存为文本 (.txt) 文件。

## <a name="import-format"></a>导入格式

下表列出了在导入期间进行合并时应使用的导入格式。

| 记录表 | 格式 | 说明 |
|--------------|---------|-------|
| 1            | 170150, Goodwill, 4 | <ul><li>记录表</li><li>源主科目 ID</li><li>主科目行</li><li>主科目类型</li></ul> |
| 2            | 110130, 2015/01/01, 1, USD, 0,0,80699.39,0,1 | <ul><li>主科目 ID</li><li>交易日期</li><li>会计期间类型（**0** = 期初，**1** = 运营，**2** = 期末）</li><li>交易币种</li><li>借方或贷方（**0** = 借方，**1** = 贷方）</li><li>过帐层</li><li>交易金额</li><li>数量</li><li>本地 RecID（交易的模糊的唯一 int64 值）</li></ul> |
| 3            | USMF0000009, 2017/01/01, FY2017, 1, 2017,01,01, 602200, USD, 6053.6.0 | <ul><li>条目编号（预算标题交易编号）</li><li>预算标题的默认日期</li><li>预算模型 ID</li><li>预算类型（**1** - 原始预算，**2** - 转移，**3** - 修订，**4** - 保留款，**5** - 预留款，**6** - 结转预算，**7** - 项目，**8** - 固定资产，**9** - 需求预测，**10** - 供应预测，**11** - 分摊，**12** - 初步预算。）</li><li>行的日期</li><li>行的主科目 ID</li><li>行的币种代码</li><li>行的金额，以交易货币为单位</li><li>行的预算类型（费用或收入）的枚举整数值</li></ul> |
| 4            | DEMF | RecordCompany 是源法人。 |
| 5            | 110130, 2015/01/01, 1, USD, 0,0,80699.39,0,1 | <ul><li>主帐户 ID</li><li>交易日期</li><li>会计期间类型（0 期初，1 运营，2 期末）</li><li>交易币种</li><li>借方或贷方（0 代表借方，1 代表贷方）</li><li>过帐层</li><li>交易记录金额</li><li>数量</li><li>本地 recid（交易的模糊的唯一 int64 值）</li></ul>  |
| 6            | BusinessUnit, 1 部门, 2 | 段顺序中定义的财务维度属性。<p>您可以使用 **导出** 页来验证属性是如何定义的。</p> |
| 7            | 002,1,658 | <ul><li>财务维度值</li><li>财务维度，作为 RecordDimensions 中提供的索引</li><li>与 RecordTrans 或 RecordTrans2 中唯一记录 ID 关联的模糊的唯一记录 ID</li></ul> |
| 8            | 002,1,1 | <ul><li>与 RecordBudget 中的交易关联的维度值</li><li>财务维度，作为 RecordDimensions 中提供的索引</li><li>与文件中交易行的顺序一致的模糊行记录 ID</li></ul> |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
