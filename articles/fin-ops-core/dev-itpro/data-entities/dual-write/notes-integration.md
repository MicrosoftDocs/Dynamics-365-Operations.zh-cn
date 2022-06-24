---
title: 注释集成
description: 本文介绍双写入过程中的注释数据集成。
author: RamaKrishnamoorthy
ms.date: 02/22/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 8e1444aa311bb2dc74705a3791e58c3187ecd8ea
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8876706"
---
# <a name="note-integration"></a>注释集成

[!include [banner](../../includes/banner.md)]



在业务流程中，Microsoft Dynamics 365 用户经常会收集有关其客户的信息。 此信息记录为活动和注释。 本文介绍双写入过程中的注释数据集成。

可以通过以下方式对客户信息进行分类：

+ **Dynamics 365 用户代表客户处理的可操作信息** – 例如，Contoso（Dynamics 365 用户）正在进行游戏节目。 Contoso 的一位客户（一位客户）希望参加游戏节目。 客户要求 Contoso 员工为其预订游戏节目中的广告位。 预订在 Contoso 的活动参与者日历中进行。
+ **Dynamics 365 用户的可操作信息** – 例如，购买 Surface 设备的客户输入特殊说明，指明该设备在交付前应进行礼品包装。 这些说明是可操作信息，应由负责包装的 Contoso 员工进行处理。
+ **非可操作性信息** – 例如，客户访问了 Contoso 商店，并且在与售货员交谈期间表达了 *Halo* 游戏和游戏配件方面的兴趣。 售货员记录了此信息。 然后，产品推荐引擎使用此信息向客户提供建议。

通常，可操作性信息在财务和运营应用和客户互动应用中作为 *活动* 捕获。 非可操作性信息在财务和运营应用中作为 *注释* 捕获，在客户互动应用中作为 *批注* 捕获。

> [!TIP]
> 尽管注释适用于非可操作信息，但如果您想使用它们来存储和处理可操作信息，则应用不会阻止您这么做。

Microsoft 当前正在发布注释集成功能。 （活动集成功能将在稍后发布。）注释集成适用于客户、供应商、销售订单和采购订单。

## <a name="create-a-note-in-a-customer-engagement-app"></a>在 Customer Engagement 应用中创建注释

要在客户互动应用中创建注释，然后将其同步到财务和运营应用，请按照以下步骤操作。

1. 在 Customer Engagement 应用中，打开客户的帐户记录。
2. 在 **时间线** 窗格中，选择加号 (**+**)，然后选择 **注释** 以创建注释。

    ![在 Customer Engagement 应用中创建注释。](media/notes-ce-1.png)

3. 输入标题和描述，然后选择 **添加注释**。

    ![输入标题和描述。](media/notes-ce-2.png)

    新注释将添加到客户时间线中。

    ![客户时间线上的新注释。](media/notes-ce-3.png)

4. 登录到财务和运营应用，然后打开相同的客户记录。 请注意右上角的 **附件** 按钮（回形针符号）表示该记录具有附件。

    ![关于附件的通知。](media/notes-ce-4.png)

5. 选择 **附件** 按钮以打开 **附件** 页。 您应该查找在 Customer Engagement 应用中创建的注释。

    ![来自 Customer Engagement 应用的注释。](media/notes-ce-5.png)

注释的任何更新都会在财务和运营应用和客户互动应用之间来回同步。

## <a name="create-a-note-in-a-finance-and-operations-app"></a>在财务和运营应用中创建注释

您还可以在财务和运营应用中创建注释，然后它将同步到客户互动应用。

要在财务和运营应用中创建注释，然后将其同步到客户互动应用，请按照以下步骤操作。

1. 在财务和运营应用中，在 **附件** 页面上选择 **新建** \> **注释**。

    ![在财务和运营应用中创建注释。](media/notes-fo-1.png)

2. 输入标题和一组简要说明，然后选择 **保存**。

    ![输入标题和说明。](media/notes-fo-2.png)

3. 在 Customer Engagement 应用中，更新记录。 您应该会在时间线上找到新注释。

    ![Customer Engagement 应用中时间线上的新注释。](media/notes-fo-3.png)

您可以将注释归类为内部注释或外部注释。

- 在财务和运营应用的 **附件** 页上，打开注释，然后在 **限制** 字段中，选择 **内部** 或 **外部**。

    ![限制字段。](media/notes-fo-4.png)

您还可以创建 URL。

1. 在财务和运营应用中，在 **附件** 页面上选择 **新建** \> **URL**。
2. 输入标题和 URL。
3. 在 **限制** 字段中，选择 **内部** 或 **外部**。

    ![在财务和运营应用中创建 URL。](media/notes-fo-5.png)

4. 选择 **保存**。

    由于 Customer Engagement 应用没有 URL 类型，因此该 URL 已与双重写入功能集成为注释。

    ![Customer Engagement 应用中显示为注释的 URL。](media/notes-ce-6.png)

> [!NOTE]
> 不支持文件附件。

## <a name="templates"></a>模板

注释集成包括表映射的集合，这些映射在数据交互期间协同工作，如下表所示。

| 财务和运营应用 | Customer engagement 应用 | Description |
|----------------------------|-------------------------|-------------|
| [客户附件](mapping-reference.md#230) | 批注 | 使用纯文本和 URL 来捕获客户特定信息的企业（针对组织和个人）。 |
| [供应商单据附件](mapping-reference.md#231) | 批注 | 使用纯文本和 URL 来捕获供应商特定信息的企业（针对组织和个人）。 |
| [销售订单头文档附件](mapping-reference.md#229) | 批注 | 使用纯文本和 URL 来捕获销售订单特定信息的企业。 |
| [采购订单头文档附件](mapping-reference.md#232) | 批注 | 使用纯文本和 URL 来捕获采购订单特定信息的企业。 |

## <a name="limitations"></a>限制

安装注释解决方案后，无法卸载它。 

有关更多信息，请参见[双重写入映射参考](mapping-reference.md)。
