---
title: 设置零售对账单的编号规则
description: 本文介绍如何在 Microsoft Dynamics 365 Commerce 中配置零售对帐单所需的编号规则。
author: analpert
ms.date: 04/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: analpert
ms.search.validFrom: 2022-04-12
ms.openlocfilehash: 5c4eb872ec2151a9f4ac5462ad43dd03a6705487
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879995"
---
# <a name="set-up-number-sequences-for-retail-statements"></a>设置零售对账单的编号规则

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

本文介绍如何在 Microsoft Dynamics 365 Commerce 中配置零售对帐单所需的编号规则。

Dynamics 365 Commerce 中使用了两种类型的零售对帐单： 

- 应该经常创建和过帐 **交易对帐单**。 它们用于将商店中的所有非财务交易过帐到 Dynamics 365 Commerce Headquarters。 
- 每个工作日都应该创建和过帐一次 **财务报表**。 这些报表仅包括已通过 P 作业上传到 Commerce Headquarters 的零售商店的结束班次。

## <a name="configure-a-number-sequence-for-statement-posting"></a>配置对帐单过帐的编号规则

在您完成零售商店的设置后，在 Commerce Headquarters 中，您必须配置一个唯一编号规则，该编号规则将在对帐单创建过程中用于对帐单。

要在 Commerce Headquarters 中配置对帐单过帐的编号规则，请按照下列步骤操作。

1. 转到 **组织管理 \> 编号规则 \> 编号规则**。
1. 选择 **新建 \> 编号规则** 创建新记录。
1. 在 **标识** 快速选项卡上的 **编号规则代码** 字段中，输入编号规则代码。
1. 在 **编号规则名称** 字段中，输入一个名称。
1. 在 **范围参数** 快速选项卡上的 **范围** 字段中，选择 **运营单位**。
1. 在 **运营单位** 字段中，选择将用于编号规则的商店。
1. 在 **客户细分** 快速选项卡上，定义客户细分。
1. 在 **参考** 快速选项卡上，将 **区域** 字段设置为 **零售商店**。
1. 将 **引用** 字段设置为 **对帐单编号**，然后选择 **确定**。

    ![“编号规则”页上的“标识”、“范围参数”、“客户细分”和“引用”快速选项卡。](media/retail-statements-num-seq-setup-01.png)

1. 在 **常规** 快速选项卡上的 **编号分配** 部分中，更新 **最小** 和 **最大** 字段，以便它们与您在 **段** 快速选项卡上定义的 **字母数字** 段长度匹配。
1. 在 **性能** 快速选项卡上，我们建议您将 **预分配** 选项设置为 **是**，将 **编号数量** 字段设置为 **25**。

    ![“编号规则”页上的“常规”和“性能”快速选项卡。](media/retail-statements-num-seq-setup-02.png)

1. 在操作窗格上，选择 **保存** 以保存您的更改并关闭页面。
