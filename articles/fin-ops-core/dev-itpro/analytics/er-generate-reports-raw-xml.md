---
title: 通过添加原始 XML 格式的内容创建报表
description: 可以设计电子申报 (ER) 格式以生成 XML 格式的传出单据。
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 21449b8684256c5ddf6d710175b3724c300da428
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2019
ms.locfileid: "2181396"
---
# <a name="generate-reports-by-adding-content-as-raw-xml"></a>通过将内容添加为原始 XML 生成报告

[!include[banner](../includes/banner.md)]

可使用新的**原始 XML** 格式元素设计电子申报 (ER) 格式，以生成 XML 格式的传出单据。 在某些情况下，您可能出于下面的一项或多项原因，向这些报表添加原始 XML 数据。

- 将原始 XML 用于报表的最初设计和不间断的维护更为方便，因为可以通过执行运行时表达式自动生成 XML 结构。 因此，不必在设计时为多个格式元素确定多个绑定。 如果在生成报告时，使用的数据源中包含可用于创建 XML 元素的信息，这就有可能。
- 其他方法不能使用以前收到并存储在系统中的 XML 内容填充报表。 例如，生成的 XML 响应可能必须包含以前发送的 XML 请求的内容。
- 没有其他方法可以基于字符的数字代码将字符插入生成的单据中。 对于某些语言和字符来说。不存在这种代码。 例如，希腊字母 rho (ρ) 和 HTML 实体代码（如 \&eacute）；对于 *e* 来说，就有重音符 (é)。

> [!NOTE]
> 请注意，此框架不控制通过使用**原始 XML** 格式元素放入生成的单据中的 XML 内容是否正确。

若要了解有关此功能的详细信息，请播放 **ER 使用原始 XML 数据生成 XML 报表（第 1 部分：设计数据模型）** 和 **ER 使用原始 XML 数据生成 XML 报表（第 2 部分：设计和运行报表）** 任务指南，这些任务指南属于 **7.5.4.3 获取/开发 IT 服务/解决方案 (10677)** 业务流程，可以从 [Microsoft 下载中心](https://go.microsoft.com/fwlink/?linkid=874684)下载。 这些任务指南引导您完成配置 ER 格式以将原始 XML 数据插入生成的文件中这一过程。
