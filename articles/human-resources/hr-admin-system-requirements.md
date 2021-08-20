---
title: 系统要求
description: 本文介绍 Microsoft Dynamics 365 Human Resources 的要求。
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 52ef0176926fd6c5c5d2bc852080dde5273d05d0f2edd20e091d97c71e503dce
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6761084"
---
# <a name="system-requirements"></a>系统要求

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本文介绍 Microsoft Dynamics 365 Human Resources 的要求。 还概述支持 Human Resources 的国家和地区，以及有关 Human Resources 数据的语言和本地化的信息。

## <a name="supported-web-browsers"></a>支持的 Web 浏览器

Human Resources 可在指定操作系统上运行的以下任一 Web 浏览器中运行： 

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
> * Human Resources 适用于延迟等于或低于 250-300 毫秒 (ms) 的网络。 该延迟是从浏览器客户端到托管 Human Resources 的 Microsoft Azure 数据中心的延迟。 建议在以下位置测试网络延迟：[www.azurespeed.com](https://www.azurespeed.com "Azure 延迟测试")。
> * Human Resources 带宽要求取决于您的方案。 大多数典型方案要求带宽超过每秒 50 千字节 (KBps)。
> 
> [!WARNING]
> 请勿通过将用户数乘以最低带宽要求来计算客户端位置的带宽要求。 给定位置的并行使用很难计算。 对于注重带宽要求的客户，请使用 Human Resources 的试用版本。

## <a name="supported-microsoft-office-applications"></a>支持的 Microsoft Office 应用程序

* 若要运行 Microsoft Excel 和 Word 加载项，必须安装适用于 Windows 或 Mac 的 Microsoft Office 2016。 有关版本要求的更多详细信息，请参阅 [Office 集成疑难解答](../fin-ops-core/dev-itpro/office-integration/office-integration-troubleshooting.md "Office 集成疑难解答")。
* 若要查看“导出到 Excel”或“导出到 Word”功能生成的文档，必须安装 Microsoft Office 2007 或更高版本。

## <a name="regional-availability-languages-and-localization"></a>地区可用性、语言和本地化

可在 [Microsoft Dynamics 365 全球可用性](/dynamics365/get-started/availability)中下载 Human Resources 支持的国家、地区和语言的 PDF 文件。 

> [!NOTE]
> 由于用户界面已本地化为其他语言，所以所有用户数据使用输入语言存储。 可以使用其他语言创建电子邮件和模板，但是目前日程安排信息之类数据仅提供英文版。

如果您是开发人员，并且有效期创建国家或地区特定的自定义项，或者有兴趣为 Microsoft 目前尚未支持的国家或地区创建解决方案，请参阅[全球化](/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region)。


[!INCLUDE[footer-include](../includes/footer-banner.md)]