---
title: 在 Finance 和 Supply Chain Management 中开具电子发票
description: 本主题说明如何通过电子开票附加产品在 Microsoft Dynamics 365 Finance 和 Dynamics 365 Supply Chain Management 中开具电子发票。
author: gionoder
manager: AnnBe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 187f5a20d088b4fcd7af2a6576357a69c2efc2c6
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104349"
---
# <a name="issue-electronic-invoices-in-finance-and-supply-chain-management"></a>在 Finance 和 Supply Chain Management 中开具电子发票

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

本主题说明如何通过电子开票附加产品在 Microsoft Dynamics 365 Finance 和 Dynamics 365 Supply Chain Management 中开具电子发票。


## <a name="feature-activation"></a>功能激活

要开始通过电子开票附加产品开具电子发票，必须激活 Finance 和 Supply Chain Management 中的功能引用。

每个功能引用对应于一个特定的电子开票功能，该功能符合某个国家/地区的电子开票要求。

下表显示了电子开票附加产品支持的功能引用的列表。

| 功能引用 | 姓名                                              | 国家/地区 |
|-------------------|---------------------------------------------------|----------------|
| BR-00053          | NF-e 联邦 - 巴西电子发票       | 巴西         |
| BR-00095          | NFS-e 巴西电子发票               | 巴西         |
| DK-00001          | 向公共部门开具电子发票 (OIOUBL) – DK    | 丹麦        |
| EG-00008          | 针对埃及的电子开单                             | 埃及          |
| ES-00025          | 向公共部门开具的电子发票           | 西班牙          |
| EUR-00023         | 向公共部门开具的欧盟电子发票       | 欧洲         |
| ITA-00036         | IT - 向公共部门开具电子发票 (FatturaPA) | 意大利          |
| MX-00010          | 电子开单 CFDI                                  | 墨西哥         |
| MX-00016          | 电子开票 CFDI - 取消流程           | 墨西哥         |

在存在支持国家/地区本地化范围的旧版电子开票功能的情况下，激活功能引用可以通过电子开票附加产品开具电子发票，同时关闭前一个功能。

## <a name="submit-electronic-documents"></a>提交电子单据

提交电子单据的流程表示 Finance 和 Supply Chain Management 与电子开票附加产品之间的单点通信。 在每个提交事件期间，通信流都是双向的：

- **从 Finance 和 Supply Chain Management 到电子开票附加产品** – Finance 和 Supply Chain Management 将摘要发票发送到电子开票附加产品。 根据需要，它们还发送配置为电子开票功能一部分的变量内容。
- **从电子开票附加产品到 Finance 和 Supply Chain Management** – 根据电子开票功能，Finance 和 Supply Chain Management 从电子开票附加产品接收有关先前提交的发票处理结果的更新。 另外还接收配置为电子开票功能一部分的变量内容。

要将电子单据提交到电子开票附加产品，在 Finance 和 Supply Chain Management 中，转到 **组织管理 &gt; 定期 &gt; 电子单据 &gt; 提交电子单据**。

起点是一个已过帐的发票。 此发票可以来自不同的来源，如销售订单、项目发票或普通发票。

提交流程可以手动运行，也可以在后台运行。

- **手动执行** – 对于手动执行，必须使用 **筛选器** 选项定义必须提交的文档范围。 在 **筛选器** 页上，您可以配置自己的查询来选择必须提交的已过帐发票。 选择之后，您必须手动开始执行处理并等待它完成运行。 处理完成后，操作中心中的消息将显示已成功提交的电子单据数。
- **后台执行** – 后台执行运行，无需您登录或让提交对话框保持打开。 您可以计划流程的运行并定义执行频率。

## <a name="view-the-submission-logs"></a>查看提交日志

在 Finance 和 Supply Chain Management 中，您可以使用提交日志来查看处理向电子开票附加产品的提交的结果。 转到 **组织管理 &gt; 定期 &gt; 电子单据 &gt; 电子单据提交**，然后 **文档类型** 字段中，选择一个值来筛选日志显示的发票类型。

有三个可能的提交状态：

- **已计划** – 电子开票附加产品已从 Finance 和 Supply Chain Management 收到提交，电子开票功能正在进行处理。
- **已完成** – 电子开票附加产品已成功处理电子开票功能，因为它被配置为运行该功能。
- **失败** – 电子开票附加产品在处理电子开票功能期间遇到错误或因异常停止。

> [!IMPORTANT]
> 提交状态是指电子开票附加产品对电子开票功能执行的处理的状态。 不是电子发票本身的最终状态。
>
> 例如，如果必须将电子发票提交到外部 Web 服务进行审核，提交状态可能是 **已完成**，但是电子发票的状态可能是 **已拒绝**。 在此例中，电子开票附加产品可以成功处理电子开票功能，因为它被配置为处理该功能。 但是，电子发票被拒绝，因为它不符合 Web 服务为发票审核设定的条件。

提交日志包括以下附加功能：

- **提交详细信息** – 查看主要提交的详细信息。 可视化显示在电子开票功能中配置的操作的完整执行日志。 另外还允许用户下载在处理过程中创建的文件。 在发票必须由外部 Web 服务审核的情况下，它让用户可以查看发票的状态。
- **相关提交** – 查看子提交的详细信息。
- **取消提交** – 此功能在必须由外部 Web 服务审核电子发票的情况下启用特殊提交流程。 它指示电子开票附加产品向 Web 服务发送一条特定消息，用于取消 Web 服务数据库中已审核电子发票的状态。
- **重新提交文档** – 重新提交已经提交到电子开票附加产品的电子单据。 将在 **提交详细信息** 页创建全新的日志。
- **发送相关提交**


[!INCLUDE[footer-include](../../includes/footer-banner.md)]