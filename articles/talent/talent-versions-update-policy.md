---
title: Talent 系统要求
description: 此主题列出了 Dynamics 365 Talent 的要求。
author: andreabichsel
manager: AnnBe
ms.date: 10/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 509827d5736887f56e7754a0760af7dea76277f7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460432"
---
# <a name="talent-system-requirements"></a>Talent 系统要求

[!include [banner](includes/banner.md)]

本主题介绍 Microsoft Dynamics 365 Talent（包括 Attract 和 Onboard）的要求。 还概述支持 Talent 的国家和地区，以及有关 Talent 数据的语言和本地化的信息。 此外，本主题还提供 Talent 的更新策略。

## <a name="supported-web-browsers"></a>支持的 Web 浏览器

Microsoft Dynamics 365 Talent 可在指定操作系统上运行的以下任一 Web 浏览器中运行： 

*   Windows 10 上的 Microsoft Edge（最新公开提供的版本）
*   Windows 10、Windows 8.1 或 Windows 7 上的 Internet Explorer 11
*   Google Chrome（最新公开提供的版本）
*   Apple Safari（最新公开提供的版本）

要查看每个 Web 浏览器的最新版本，请转至软件制造商的网站。 

> [!NOTE]
> * 若要捕获从任务录制器生成的图像并插入到 Microsoft Word 文档中，必须安装 Chrome 扩展。 
> * Workflow Editor 作为 ClickOnce 应用程序启动。 只有 Microsoft Edge 和 Internet Explorer（在支持的 Microsoft Windows 版本上）才支持 ClickOnce 应用程序。 Workflow Editor ClickOnce 应用程序需要 64 位兼容操作系统。
> * 若要预览 PDF 文件，我们建议您使用现代浏览器，如 Windows 10 上的 Microsoft Edge（最新公开提供的版本）或 Windows 10、Windows 8.1、Windows 8、Windows 7 或 Google Nexus 10 平板电脑上的 Google Chrome（最新公开提供的版本）。
>   网络要求
> * Dynamics 365 Talent 适用于延迟等于或低于 250-300 毫秒 (ms) 的网络。 该延迟是从浏览器客户端到托管 Talent 的 Microsoft Azure 数据中心的延迟。 建议在 [www.azurespeed.com](https://www.azurespeed.com "Azure 延迟测试") 测试网络延迟。
> * Talent 带宽要求取决于您的方案。 大多数典型方案要求带宽超过每秒 50 千字节 (KBps)。
> 
> [!WARNING]
> 请勿通过将用户数乘以最低带宽要求来计算客户端位置的带宽要求。 给定位置的并行使用很难计算。 对于注重带宽要求的客户，请使用 Talent 的试用版本。

## <a name="supported-microsoft-office-applications"></a>支持的 Microsoft Office 应用程序

* 若要运行 Microsoft Excel 和 Word 加载项，必须安装适用于 Windows 或 Mac 的 Microsoft Office 2016。 有关版本要求的更多详细信息，请参阅 [Office 集成疑难解答](../dev-itpro/office-integration/office-integration-troubleshooting.md "Office 集成疑难解答")。
* 若要查看“导出到 Excel”或“导出到 Word”功能生成的文档，必须安装 Microsoft Office 2007 或更高版本。

## <a name="regional-availability-languages-and-localization"></a>地区可用性、语言和本地化

可在 [Microsoft Dynamics 365 全球可用性](https://docs.microsoft.com/dynamics365/get-started/availability)中下载 Talent 支持的国家、地区和语言的 PDF 文件。 

> [!NOTE]
> 由于用户界面已本地化为其他语言，所以所有用户数据使用输入语言存储。 可以使用其他语言创建电子邮件和模板，但是目前日程安排信息之类数据仅提供英文版。

如果您是开发人员，并且有效期创建国家或地区特定的自定义项，或者有兴趣为 Microsoft 目前尚未支持的国家或地区创建解决方案，请参阅[全球化](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region)。

