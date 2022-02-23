---
title: 现金管理改进
description: 本主题介绍适用于 Dynamics 365 Commerce 的 POS 中的现金管理改进。
author: anpurush
manager: AnnBe
ms.date: 05/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-21
ms.dyn365.ops.version: ''
ms.openlocfilehash: 0c561c39dfcbfa739c5a22394c05191e7f9bc107
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410451"
---
# <a name="cash-management-improvements"></a>现金管理改进

[!include [banner](includes/banner.md)]


现金管理是一个面向实体商店零售商的关键功能。 零售商希望为自己的商店安装系统来对现金及其在商店中不同收银机和出纳之间的变动进行完全跟踪和会计问责。 必须可以对帐任何差额和确定会计责任。


Microsoft Dynamics 365 Commerce 的销售点 (POS) 应用程序中包含现金管理功能。 但是，在低于 10.0.3 的 Retail 版本中，现金管理功能不够强大，无法完全跟踪商店中的现金变动。 尽管零售商可以对帐商店的现金，如果存在现金差异，就不能准确判断会计责任。


在 Retail 版本 10.0.3 及更高版本中，零售商可以跟踪对现金的处理。 进行此项跟踪期间，零售商可以定义金库，开展双方现金交易记录，以及对帐现金管理交易记录。

## <a name="set-up-traceability-and-define-safes"></a>设置可跟踪性和定义金库

若要设置新的现金管理功能，请执行下列步骤为商店配置功能配置文件。

1. 转到 **Retail 和 Commerce \> 渠道设置 \> POS 设置 \> POS 配置文件 \> 功能配置文件**，然后选择与您要改进以实现现金管理功能的商店关联的功能配置文件。
2. 在功能配置文件的 **功能** 快速选项卡上的 **高级现金管理** 下，将 **启用现金跟踪** 选项设置为 **是**。
3. 若要设置金库，请转至 **Retail 和 Commerce \> 渠道 \> 商店 \> 所有商店**，然后选择商店。
4. 在 **商店** 页操作窗格中 **设置** 选项卡的 **设置** 组中，选择 **金库**。 可使用此选项为商店定义和维护多个金库。
4. 必须先运行 **1070 渠道配置** 配送计划作业以将这些配置同步到渠道数据库，才能使用此功能。

## <a name="additional-cash-management-changes"></a>其他现金管理更改

在 Retail 版本 10.0.3 及更高版本中，还提供了下列与现金交易记录有关的功能：

- 用户在收到“声明初始金额”提示时必须输入现金来源。 用户可以搜索商店中定义的可用金库，并选择正在取出现金的金库，以便将其放到收银机中。
- 将提示执行“取钱”操作的用户在未结“浮动条目”交易记录列表中选择此操作针对的交易记录。 如果系统中不存在相应浮动条目，用户可以创建无链接的取钱交易记录。
- “浮点条目”操作将提示用户在未结“取钱”交易记录列表中选择浮动条目此操作针对的交易记录。 如果系统中不存在相应取钱，用户可以创建无链接的浮动条目交易记录。
- 将提示进行“金库投箱”的用户选择现金投入的金库。
- 对于商店中定义的金库，用户可以管理清点起始金额、执行浮动条目、取钱和进行银行投箱之类操作。
- 对于拥有相应用户权限的用户，“管理班次”操作将显示活动、已暂停和直接结束的班次的现金余额。
- 若要为一个班次或多个班次的现金交易记录对帐，请选择要对帐的班次，然后选择 **对帐**。 打开的视图中将通过单独的选项卡显示已对帐交易记录和未对帐交易记录的列表。 用户可在此视图中选择未对帐的交易记录并为其对帐，或选择以前对帐过的交易记录并取消对帐。
- 对帐期间，如果所选交易记录不平衡，用户必须输入不平衡对帐的原因说明。 用户可以选择一个交易记录并为其对帐，同时添加所需的相关原因说明。
- 用户继续为交易记录继续对帐和取消对帐，直到班次结束。 班次结束后，不能对交易记录进行取消对帐。
- 当用户选择结束班次时，Commerce 将验证班次中是否没有未对帐的现金管理交易记录。 如果有未对帐的交易记录，用户就不能结束班次。
