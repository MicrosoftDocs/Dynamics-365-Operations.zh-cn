---
title: 在 Finance 和 Supply Chain Management 中开具电子发票
description: 本主题说明如何通过电子开票在 Microsoft Dynamics 365 Finance 和 Dynamics 365 Supply Chain Management 中开具电子发票。
author: gionoder
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 24909c2a2505724c159e939535c1d57cb66e48629862bebb32b3d72c0eb06c97
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6752118"
---
# <a name="issue-electronic-invoices-in-finance-and-supply-chain-management"></a>在 Finance 和 Supply Chain Management 中签发电子账单

[!include [banner](../includes/banner.md)]

本主题说明如何通过电子开票在 Microsoft Dynamics 365 Finance 和 Dynamics 365 Supply Chain Management 中开具电子发票。


## <a name="feature-activation"></a>功能激活

若要通过电子开票开具电子发票，必须激活 Finance 和 Supply Chain Management 中的相应功能。

每个功能都对应于一个特定的电子开票功能，该功能符合某个国家/地区的电子开票要求。

下表显示了电子开票可能支持的功能的列表。

| 姓名                                              | 国家/地区 |
|---------------------------------------------------|----------------|
|奥地利电子账单                        |奥地利         |
|比利时电子账单                         |比利时         |
|NF-e (联邦) - 电子账单(巴西)       |巴西          |
|NFS-e - 巴西服务(城市)电子账单|巴西          |
|丹麦电子账单                          |丹麦         |
|埃及电子账单                        |埃及           |
|爱沙尼亚电子账单                        |爱沙尼亚         |
|芬兰电子账单                         |芬兰         |
|法国电子账单                          |法国          |
|德国电子账单                          |德国         |
|PEPPOL - 全球电子账单                 |全局          |
|意大利电子账单                         |意大利           |
|CFDI - 墨西哥电子账单                  |墨西哥          |
|荷兰电子账单                           |荷兰     |
|挪威电子账单                       |挪威          |
|西班牙电子账单                         |西班牙           |

在存在国家/地区本地化范围内支持的旧版电子开票功能时，如果激活其中一项功能，则会关闭旧功能，并允许通过电子开票开具电子发票。

> [!IMPORTANT]
> 启用电子开票集成功能后，默认情况下将关闭新电子开票体验。 您可以使用功能概念使用特定于国家/地区的功能选择性地为法人启用新体验。 **全局** 选项针对表中未明确列出的其余县/地区控制新体验。

## <a name="submit-electronic-documents"></a>提交电子单据

提交电子单据的流程表示 Finance 和 Supply Chain Management 与电子开票之间的单点通信。 在每个提交事件期间，通信流都是双向的：

- **从 Finance 和 Supply Chain Management 到电子开票** – Finance 和 Supply Chain Management 将摘要发票发送到电子开票。 根据需要，它们还发送配置为电子开票功能一部分的变量内容。
- **从电子开票到 Finance 和 Supply Chain Management** – 根据电子开票功能，Finance 和 Supply Chain Management 从电子开票接收有关先前提交的发票处理结果的更新。 另外还接收配置为电子开票功能一部分的变量内容。

若要将电子单据提交到电子开票，在 Finance 和 Supply Chain Management 中，转到 **组织管理 &gt; 定期 &gt; 电子单据 &gt; 提交电子单据**。

起点是一个已过帐的发票。 此发票可以来自不同的来源，如销售订单、项目发票或普通发票。

提交流程可以手动运行，也可以在后台运行。

- **手动执行** – 对于手动执行，必须使用 **筛选器** 选项定义必须提交的文档范围。 在 **筛选器** 页上，您可以配置自己的查询来选择必须提交的已过帐发票。 选择之后，您必须手动开始执行处理并等待它完成运行。 处理完成后，操作中心中的消息将显示已成功提交的电子单据数。
- **后台执行** – 后台执行运行，无需您登录或让提交对话框保持打开。 您可以计划流程的运行并定义执行频率。

## <a name="view-the-submission-logs"></a>查看提交日志

在 Finance 和 Supply Chain Management 中，您可以使用提交日志来查看处理向电子开票的提交的结果。 转到 **组织管理 &gt; 定期 &gt; 电子单据 &gt; 电子单据提交**，然后 **文档类型** 字段中，选择一个值来筛选日志显示的发票类型。

有三个可能的提交状态：

- **已计划** – 电子开票已从 Finance 和 Supply Chain Management 接收提交，电子开票功能正在进行处理。
- **已完成** – 电子开票已成功处理电子开票功能，因为它已配置为运行该功能。
- **失败** – 电子开票在处理电子开票功能期间遇到错误或因异常而停止。

> [!IMPORTANT]
> 提交状态是指电子开票对电子开票功能执行的处理的状态。 不是电子发票本身的最终状态。
>
> 例如，如果必须将电子发票提交到外部 Web 服务进行审核，提交状态可能是 **已完成**，但是电子发票的状态可能是 **已拒绝**。 在这种情况下，电子开票可以成功处理电子开票功能，因为它已配置为处理该功能。 但是，电子发票被拒绝，因为它不符合 Web 服务为发票审核设定的条件。

提交日志包括以下附加功能：

- **提交详细信息** – 查看主要提交的详细信息。 可视化显示在电子开票功能中配置的操作的完整执行日志。 另外还允许用户下载在处理过程中创建的文件。 在发票必须由外部 Web 服务审核的情况下，它让用户可以查看发票的状态。
- **相关提交** – 查看子提交的详细信息。
- **取消提交** – 此功能在必须由外部 Web 服务审核电子发票的情况下启用特殊提交流程。 它指示电子开票向 Web 服务发送一条特定消息，用于取消 Web 服务数据库中已审核电子发票的状态。
- **重新提交单据** – 重新提交已经提交到电子开票的电子单据。 将在 **提交详细信息** 页面上创建新日志。
- **发送相关提交**


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
