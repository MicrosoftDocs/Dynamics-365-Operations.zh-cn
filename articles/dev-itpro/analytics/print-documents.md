---
title: "文档打印"
description: "在 Microsoft Dynamics 365 for Finance and Operations 中，可使用本地打印机或联网设备打印文档。 本文概述如何打印文档。"
author: TJVass
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: IT Pro, Application User
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.custom: 69161
ms.assetid: 7815bddd-c4f4-4bc3-a29b-315458065374
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 821d8927211d7ac3e479848c7e7bef9f650d4340
ms.openlocfilehash: 4fd20022ff91fedb6d0323e82fbe3c1acae38e48
ms.contentlocale: zh-cn
ms.lasthandoff: 08/13/2018

---

# <a name="document-printing"></a>文档打印

[!include [banner](../includes/banner.md)]

在 Microsoft Dynamics 365 for Finance and Operations 中，可使用本地打印机或联网设备打印文档。 本文概述如何打印文档。

## <a name="printing-overview"></a>打印概览

Microsoft Dynamics 365 for Finance and Operations 提供集成的设备和客户端应用程序，可用于轻松生成、存储和分发为业务活动提供支持的文档。 在 Finance and Operations 中，可使用本地打印机或联网设备打印文档。 此外，还可以将 Finance and Operations 页面和报表作为 PDF 文件或 Microsoft Office 文档直接从客户端导出。 最后，可通过分布式工作量使用网络资源直接从移动设备打印业务文档。 尽管打印要求可能各不相同，但是所有行业通常必须使用 Finance and Operations 创建业务文档的硬拷贝。 在网络设备上使用托管应用程序打印文档面临一些独有的挑战。 下面举了一些示例加以说明：

- 用户的设备上可能没有打印驱动程序。
- 用户的设备可能未连接到公司网络。

系统管理员可使用专用主机和执行一些简单的步骤配置部署，以便用户在网络设备上直接从业务应用程序进行打印。

### <a name="printing-scenarios-in-finance-and-operations-applications"></a>Finance and Operations 应用程序中的打印场景

下表介绍 Finance and Operations applications 中的三种主要的打印场景。

| 应用场景                        | 目标                                                      | 解决方案 |
|---------------------------------|-----------------------------------------------------------|----------|
| 1. 打印所见        | 打印浏览器中当前显示的内容。             | 将为浏览器生成“适合打印的”网页版本。 |
| 2. 交互式打印         | 在本地连接的设备上打印精确文档。 | 可导出报表的 PDF 版本并下载到浏览器。 |
| 3. 在网络设备上打印 | 将精确文档发送到域打印机设备。     | 将把精确文档发送到客户域中托管的服务器上运行的客户端应用程序。 |

由于解决方案因场景而异，所以 Finance and Operations 应用程序提供内置服务和工具，帮助用户达成目标：

- **场景 1** 受浏览器的 HTML5客户端呈现支持。
- **场景 2** 使用客户端应用程序和 Microsoft Office 365 服务。
- **场景 3** 需要客户端应用程序支持和 Microsoft Azure 中托管的服务支持。

除了部署到 Azure 订阅的平台，Finance and Operations 应用程序还为客户提供集成的第一方 Azure 应用程序，帮助客户轻松使用域托管的设备打印文档。

## <a name="service-overview"></a>服务概览
托管应用程序生成的文档在联网设备上等待打印时，存储在 Azure blob 存储中。 [文档路线选择代理](install-document-routing-agent.md)使用 Azure 身份验证建立通往 Azure 服务的安全通道。

**执行序列**

1. 报表由 Microsoft SQL Server Reporting Services (SSRS) 生成，存储在 Azure blob 存储中。 附加的打印机设置随文档一起存储。
2. 文档路线选择代理查询 Azure 服务总线队列以查找有效作业。
3. 文档由文档路线选择代理下载并假托到网络打印机。

客户可使用基于客户端的解决方案管理打印需求的规模。 打印工作量繁重的客户可安装多个文档路线选择代理来增加并行打印操作的数量。 不过，有些客户只需极少量的文档路线选择代理安装即可处理其预期的打印需求。

### <a name="service-components-for-network-printing"></a>网络打印的服务组件

下图显示有助于为网络打印操作提供支持的基本组件。

[![网络打印的服务组件\_2016](./media/service-components-for-network-printing_2016.png)](./media/service-components-for-network-printing_2016.png)

请注意，可将一台打印机与多个文档路线选择代理关联。 为了解析打印机首选项，托管服务使用用于唯一标识每台网络打印机的网络路径。 因此，即使一台打印机被多个客户端注册，也会在 Finance and Operations 应用程序中的打印机列表内显示为单项选择。

