---
title: 为内部公司交易设置供应商、客户和物料
description: 本文介绍了如何为内部公司交易设置供应商、客户和物料
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: CustTable, VendTable, EcoResProductListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 4c928435a4e66832b09dbc805664934cfb1236be
ms.sourcegitcommit: b666289f5113d0a3fa2220fe337d5aacf07cbd92
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/08/2022
ms.locfileid: "8945746"
---
# <a name="set-up-vendors-customers-and-items-for-intercompany-trade"></a>为内部公司交易设置供应商、客户和物料

[!include [banner](../../includes/banner.md)]

若要您的组织为内部公司交易做好准备，您必须定义将与您进行内部交易的供应商和客户。 然后您必须将这些供应商和客户与您将购买或销售的物料关联。

1. 转到 **采购 \> 供应商 \> 所有供应商**。
1. 选择供应商以定义为内部公司供应商。
1. 在操作窗格上的 **常规** 选项卡中，选择 **内部公司**。
1. 为供应商帐户指定内部公司设置参数。 这些参数包括客户法人和帐户、销售订单策略、采购订单策略、值映射和采购协议和销售协议策略。 您还可以指定是使用其他法人中的供应商帐户还是客户帐户的基础数据值。
1. 转到 **产品信息管理 \> 产品 \> 已发布产品**。
1. 在 **已发布产品** 列表页，选择要分配给供应商的物料，以便该物料可用于内部公司交易。 对于每种物料，打开 **已发放产品详细信息** 页。 在 **购买** 选项卡的 **供应商** 字段中，键入该供应商的编号。
1. 转到 **应付帐款 \> 客户 \> 所有客户**。
1. 选择客户以定义为内部公司客户。
1. 在操作窗格上的 **常规** 选项卡中，选择 **内部公司**。
1. 为客户帐户指定内部公司设置参数。 这些参数包括供应商法人和帐户、采购订单策略、销售订单策略、值映射和销售协议和采购协议策略。 您还可以指定是使用其他法人中的客户帐户还是供应商帐户的基础数据值。
1. 设置内部公司参数后，关闭 **内部公司** 页面返回到所选客户详细信息。
1. 展开 **杂项详细信息** 快速选项卡，将 **创建内部公司订单** 设置为 *是*。 如果您还想要将订单直接发运给客户，将 **直接交货** 设置为 *是*。

    > [!NOTE]
    > 如果有些物料在组织内部有存货并可交运给客户，尽管有存货，您也可能不想自动创建内部公司订单。 要停用自动为可能有时有存货的物料生成订单，将 **创建内部公司订单** 设置为 *否*。

1. 如果您想要允许在销售订单中间接创建额外行，将 **创建间接订单行** 设置为 *是*。 然后用户可以从内部公司销售订单添加行到原始销售订单。

> [!WARNING]
> 如果允许间接创建订单行，则允许通过内部公司销售订单向原始销售订单添加行。 然后每个添加都通过交给客户进行处理，并将其添加到订单和发票。 此外，在销售中涉及的每个文档将自动打印和过帐。 用户没有收到有关添加的预警。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
