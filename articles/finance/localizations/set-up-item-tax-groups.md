---
title: 设置物料税组
description: 本文说明如何在税款计算服务中设置物料税组。
author: wangchen
ms.date: 11/30/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-10-26
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: 3bc705bc8173ad2bc8ef883e6dc80b0a187314ad
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846454"
---
# <a name="set-up-item-tax-groups"></a>设置物料税组

[!include [banner](../includes/banner.md)]

本文说明如何在税款计算服务中设置物料税组。 另外还说明了如何设置物料税组适用性规则矩阵和配置矩阵中的行。

税款计算服务中的物料税组概念类似于 Microsoft Dynamics 365 Finance 中的物料销售税组概念。 它们是税代码组。 税款计算服务使用税组和物料税组的交集来确定税代码。

> [!IMPORTANT]
> 税款计算服务中的物料税组设置是不知道法人的。 您只能在 Regulatory Configuration Service (RCS) 中完成此设置一次。 当您在 Finance 中启用税款计算服务时，所选法人的物料税组将自动同步。

## <a name="set-up-an-item-tax-group"></a>设置物料税组 

按照以下步骤设置物料税组。

1. 登录 [Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/)。
2. 转到 **工作区** \> **全球化功能** \> **税款计算**。
3. 选择要设置的功能和版本，然后选择 **编辑**。
4. 在 **常规** 选项卡上，选择 **配置版本**。
5. 在 **物料税组** 选项卡上，选择 **管理列**。 如果您是第一次设置物料税组，**管理列** 对话框中的字段会自动设置。
6. 在左侧列表中，展开 **行** 节点，选中 **物料税组** 复选框。

    ![在“管理列”对话框中的“行”节点下选择的物料税组。](media/select-item-tax-group.png)

7. 选择向右箭头按钮将 **物料税组** 添加到右侧的 **所选列** 列表。

    ![添加到“所选列”列表的“物料税组”。](media/add-item-tax-group.png)

8. 选择 **确定**。

## <a name="configure-an-item-tax-group"></a>配置物料税组

设置物料税组后，将创建适用性规则矩阵。 您可以将行添加到矩阵来配置物料税组。

1. 在 **物料税组** 选项卡上，选择 **添加**。
2. 在 **物料税组** 字段中，输入物料税组的名称。

    > [!IMPORTANT]
    > 我们建议您将物料税组的名称限制为 10 个字符。 此名称将与 Finance 同步，Finance 对物料销售税组的名称限制为 10 个字符。

3. 在 **税代码** 字段中，选中要包含在物料税组中的每个税代码的复选框。 您可以在一个物料税组中包含多个税代码。

    ![在“税代码”字段中选择的多个税代码。](media/multiple-tax-codes-selection.png)

4. 重复步骤 1 到 3 添加更多物料税组。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
