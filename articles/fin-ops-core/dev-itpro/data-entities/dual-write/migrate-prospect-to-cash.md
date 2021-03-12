---
title: 将“目标客户到现金”数据从数据集成器迁移到双写入
description: 本主题介绍如何将“目标客户到现金”数据从数据集成器迁移到双写入。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.search.validFrom: 2021-01-04
ms.openlocfilehash: f1478f0246e7f1ff8bd72232cbaf4c2034cf4edb
ms.sourcegitcommit: 6af7b37b1c8950ad706e684cc13a79e662985b34
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/14/2021
ms.locfileid: "4959838"
---
# <a name="migrate-prospect-to-cash-data-from-data-integrator-to-dual-write"></a>将“目标客户到现金”数据从数据集成器迁移到双写入

[!include [banner](../../includes/banner.md)]

要将“目标客户到现金”数据从数据集成器迁移到双写入，请按照以下步骤操作。

1. 运行“目标客户到现金”数据集成器作业，执行最后一次完全同步。 这样，您可以确保两个系统（Finance and Operations 应用和客户互动应用）具有所有数据。
2. 为帮助防止潜在的数据丢失，将“目标客户到现金”数据从 Microsoft Dynamics 365 Sales 导出到 Excel 文件或逗号分隔值 (CSV) 文件。 从以下实体导出数据：

    - [科目](#account-table)
    - [联系人](#contact-table)
    - [账单](#invoice-table)
    - 发票产品
    - [订单](#order-table)
    - [订单产品](#order-products-table)
    - [产品](#products-table)
    - [报价](#quote-and-quote-product-tables)
    - [报价单产品](#quote-and-quote-product-tables)

3. 从 Sales 环境中卸载“目标客户到现金”解决方案。 此步骤将删除“目标客户到现金”解决方案引入的列和相应的数据。
4. 安装双写入解决方案。
5. 为一个或多个法人在 Finance and Operations 应用和客户互动应用之间创建双写入连接。
6. 启用双写入表映射，然后为所需的参考数据运行初始同步。 （有关详细信息，请参阅[初始同步注意事项](initial-sync-guidance.md)。）所需数据的示例包括客户组、付款期限和付款计划。 不要为需要初始化的表启用双写入映射，如客户、报价单、报价单行、订单和订单行表。
7. 在客户互动应用中，转到 **高级设置 \> 系统设置 \> 数据管理 \> 重复检测规则**，禁用所有规则。
8. 初始化步骤 2 中列出的表。 有关说明，请参阅本主题的其余章节。
9. 打开 Finance and Operations 应用，启用表映射，如客户、报价单、报价单行、订单和订单行表映射。 然后运行初始同步。 （有关详细信息，请参阅[初始同步注意事项](initial-sync-guidance.md)。）此流程将同步来自 Finance and Operations 应用的其他信息，如处理状态、装运地址和账单地址、站点和仓库。

## <a name="account-table"></a>客户表

1. 在 **公司** 列中，输入公司名称，如 **USMF**。
2. 在 **关系类型** 列中，输入 **客户** 作为静态值。 您可能不想在业务逻辑中将每个客户记录分类为客户。
3. 在 **客户组 ID** 列中，从 Finance and Operations 应用输入客户组编号。 “目标客户到现金”解决方案的默认值为 **10**。
4. 如果您使用的是“目标客户到现金”解决方案，没有任何 **客户编号** 自定义项，请在 **当事方编号** 列中输入 **客户编号** 值。 如果有自定义项，并且您不知道当事方编号，请从 Finance and Operations 应用提取此信息。

## <a name="contact-table"></a>联系人表

1. 在 **公司** 列中，输入公司名称，如 **USMF**。
2. 根据 CSV 文件中的 **IsActiveCustomer** 值设置以下列：

    - 如果 **IsActiveCustomer** 在 CSV 文件中设置为 **是**，则将 **适售** 列设置为 **是**。 在 **客户组 ID** 列中，从 Finance and Operations 应用输入客户组编号。 “目标客户到现金”解决方案的默认值为 **10**。
    - 如果 **IsActiveCustomer** 在 CSV 文件中设置为 **否**，则将 **适售** 列设置为 **否**，并将 **联系人** 列设置为 **客户**。

3. 如果您使用的是“目标客户到现金”解决方案，没有对 **联系人编号** 的任何自定义项，请设置以下列：

    - 将联系人编号从 CSV 文件 (**msdynce\_contactnumber**) 迁移到 **联系人** 表 (**msdyn\_contactnumber**) 中的联系人编号。
    - 使用 **当事方编号** 列中 **联系人编号** 表中的值。
    - 使用 **客户编号/联系人 ID** 列中 **联系人编号** 表中的值。

## <a name="invoice-table"></a>发票表

由于 **发票** 表中的数据被设计为单向流动，即从 Finance and Operations 应用到客户互动应用，所以不需要初始化。 运行初始同步，将所有必需的数据从 Finance and Operations 应用迁移到客户互动应用。 有关详细信息，请参阅[初始同步注意事项](initial-sync-guidance.md)。

## <a name="order-table"></a>订单表

1. 在 **公司** 列中，输入公司名称，如 **USMF**。
2. 将 CSV 文件中的 **订单 ID** 列的值复制到 **销售订单编号** 列。
3. 将 CSV 文件中的 **客户** 列的值复制到 **发票客户编号** 列。
4. 将 CSV 文件中的 **运达国家/地区** 列的值复制到 **运达国家/地区** 列。 此值的示例包括 **US** 和 **美国**。
5. 设置 **要求收货日期** 列。 如果您没有使用收货日期，请使用 CSV 文件中的 **要求交货日期**、**履行日期** 和 **提交日期** 列。 此值的一个示例是 **2020-03-27T00:00:00Z**。
6. 设置 **语言** 列。 此值的一个示例是 **en-us**。
7. 使用 **基于物料** 列设置 **订单类型** 列。

## <a name="order-products-table"></a>订单产品表

- 在 **公司** 列中，输入公司名称，如 **USMF**。

## <a name="products-table"></a>产品表

由于 **产品** 表中的数据被设计为单向流动，即从 Finance and Operations 应用到客户互动应用，所以不需要初始化。 运行初始同步，将所有必需的数据从 Finance and Operations 应用迁移到客户互动应用。 有关详细信息，请参阅[初始同步注意事项](initial-sync-guidance.md)。

## <a name="quote-and-quote-product-tables"></a>报价单和报价单产品表

对于 **报价单** 表，请按照本主题前面的[订单表](#order-table)一节的说明操作。 对于 **报价单产品** 表，请按照[订单产品表](#order-products-table)一节的说明操作。
