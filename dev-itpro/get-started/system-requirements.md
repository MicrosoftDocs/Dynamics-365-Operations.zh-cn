---
title: "系统要求"
description: "此主题列出当前版本中的系统要求工序的 Microsoft Dynamics 365。"
author: sericks007
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: Core
ms.custom: 55651
ms.assetid: e564d51d-42d3-47c5-b388-93b8219c692a
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
translationtype: Human Translation
ms.sourcegitcommit: c8c96dc9705688308dd4a5c720700ddc17657d75
ms.openlocfilehash: 9220c093d3f6d6700127c93651db4083be300311
ms.lasthandoff: 03/31/2017


---

# <a name="system-requirements"></a>系统要求

此主题列出当前版本中的系统要求工序的 Microsoft Dynamics 365。

<a name="supported-web-browsers"></a>支持的 Web 浏览器
----------------------

工序 Web 应用程序的 Microsoft Dynamics 365 在指定的行动的系统运行可以运行在以下任何网页/网站/web 浏览器：

-   Microsoft 边缘 (最新的公共版本) 可用在 Windows 上 10
-   Windows 10、Windows 8.1 或 Windows 7 上的 Internet Explorer 11
-   谷歌镶边 (最新的公共版本) 可用在 Windows 上 10，Windows 8.1，Windows 8、Windows 谷歌 7 或 10 连结平板
-   Apple 徒步出差队 (最新的公共可用在"操作系统版本) Mac X 10.10 (优胜美地)，10.11 (El) 或 Capitan 10.12 (山脉)，或 Apple iPad

要查看每个 Web 浏览器的最新版本，请转至软件制造商的网站。 **注意：**

-   若要捕捉来自任务录制器生成，并包括它们在 Microsoft Word 文档的图像，必须安装有镶边扩展名。 <!---For instructions about how to install the extension, see [Screenshot Extension setup](/dynamics365/operations/dev-itpro/user-interface/task-recorder).-->
-   工作流作为 ClickOnce 编辑器启动应用程序。 只有边缘和 Microsoft Internet Explorer 支持一 (" Microsoft Windows 的版本 ClickOnce) 支持应用程序。 工作流 ClickOnce 编辑器应用程序要求一个 64 位操作系统兼容。
-   财务报告的启动报表设计器 ClickOnce 作为应用程序。 它要求的一个 64 位操作系统兼容。 如果您使用镶边，必须安装 ClickOnce 扩展名以便下载报表设计器客户。 如果将隐姓氏埋名的模式的镶边，请确保 ClickOnce 扩展为隐姓氏埋名的模式也会启用。

### <a name="supported-web-browsers-for-retail-cloud-pos"></a>Retail Cloud POS 支持的 Web 浏览器

Dynamics 365 的零售 POS 操作的云在指定的行动的系统运行可以运行在以下任何网页/网站/web 浏览器：

-   Microsoft 边缘 (最新的公共版本) 可用在 Windows 上 10
-   Windows 10、Windows 8.1 或 Windows 7 上的 Internet Explorer 11
-   为铬 (最新的公共版本) 可用在 Windows 上 10，Windows 8.1、Windows 7

## <a name="network-requirements"></a>网络需求
-   工序的 Dynamics 365 为 150 少于毫秒延迟的网络 (ms) 设计。 这是从浏览器客户的延期到 Microsoft Azure 数据中心工序该主机 Dynamics 365。 我们建议您在<http://www.azurespeed.com>延迟测试网络。
-   Dynamics 365 的带宽需求工序的依赖于您的项目。 大多数典型情况要求带宽 50 多千字节每秒 (Kbps)。 但是，由为具有更高净载重量需求的情况，如包括全面的自定义工作区或方案，详细带宽建议。

一般来说，工序的 Dynamics 365 为 Internet 优化。 往返的客户数量从一个浏览器的 Azure 的数据中心的很小一些，并将整个的净载重量压缩。 **警告：**将{{要：by}}通过将用户的数量计算从客户位置的带宽需求与最低带宽的需求。 特定位置的并发使用很困难计算。 对于关注带宽要求的客户，因此为工序请使用一版本预览 Dynamics 365。

## <a name="net-framework-requirements"></a>.NET Framework 需求
工序的 Dynamics 365 为所有需要 .NET Framework 版本 4.6.2 后，单击应用程序文档，例如工艺路线代理。 有关设置说明，请参阅 SQL 安装 .NET Framework [] (https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx)。

## <a name="supported-microsoft-office-applications"></a>支持的 Microsoft Office 应用程序
-   若要运行 Microsoft Excel 短语和加载项，您必须拥有 Windows 的安装 Microsoft Office 2016 或 Mac。 有关更详细信息，请参阅需求有关版本 [] (/dynamics365/operations/dev Office 集成故障排除 itpro/office 集成 integration/office 故障排除。)
-   若要查看到由生成的 Excel 导出或短语导出功能的文档，必须对于 Microsoft Office 设置的 2007 或更晚的日期。

## <a name="retail-modern-pos-requirements"></a>Retail Modern POS 要求
### <a name="supported-operating-systems"></a>支持的操作系统

-   Retail Modern POS 应用程序为 32 位，不过，在和 x86 后 x64 体系结构中运行。
-   Retail Modern POS 在 Windows 上 10 同意，仅支持企业和企业分支长期服务的 (LTSB) 编辑。

### <a name="minimum-system-requirements"></a>最小的系统要求

-   支持的最小数量为 1280 × 1024 解决方法。
-   Retail Modern POS 运行的计算机必须满足以下要求：
    -   它必须具有，至少运行，在不少于 2 千兆赫的 (GHz) 双重核心处理程序。
    -   它必须具有，至少，(GB) 3 GB RAM，1.5。
    -   它必须能够访问 Internet。

## <a name="retail-hardware-station-requirements"></a>Retail 硬件工作站需求
### <a name="supported-operating-systems"></a>支持的操作系统

-   Retail 硬件工作站应用程序为 32 位，不过，在和 x86 后 x64 体系结构中运行。
-   Retail 硬件工作站支持：在以下操作系统
    -   Windows 7 专业版企业、最终**注释和编辑：只有当，Internet Explorer 11 上系统，手动设置** Windows 7 支持。
    -   Windows 8.1 更新 1 专业的、企业和嵌入的编辑
    -   Windows 10 同意，企业和企业 LTSB 编辑

### <a name="minimum-system-requirements"></a>最小的系统要求

计算机必须遵守所有系统要求提供了安装和使用以下项：

-   Internet 信息服务 (IIS)
-   第三方硬件

## <a name="retail-store-scale-unit-requirements"></a>Retail Store 秤需求单位
### <a name="supported-operating-systems"></a>支持的操作系统

-   Retail Store 秤单位应用程序为 32 位，不过，在和 x86 后 x64 体系结构中运行。
-   Retail Store 秤单位。以下操作系统支持：
    -   Windows 7 专业版企业、终端和编辑
    -   Windows 8.1 更新 1 专业的、企业和嵌入的编辑
    -   Windows 10 同意，企业和企业 LTSB 编辑

### <a name="minimum-system-requirements"></a>最小的系统要求

-   4 GB RAM，1.5
-   1.6 GHz 高峰 CPU 速度。核心 (两核心是最小数量。)
-   至少 10 GB 可用空间 (通道数据库可能需要数空格。)

### <a name="recommended-system-requirements"></a>建议使用的系统要求

-   6 GB RAM，1.5
-   2.4 GHz 或视同 i7 () 高峰 CPU 速度。核心 (荐使用四个核心。)
-   至少 10 GB 可用空间 (通道数据库可能需要数空格。)

## <a name="requirements-for-development-on-local-vms"></a>开发 VMs 本机的需求。
有关开发的需求的信息在本地的 (VMs) 虚拟机，请参阅 [] (/dynamics365/operations/dev VM 本地运行 itpro/dev tools/access 在针对 instances#vm 是运行)。

<a name="see-also"></a>请参阅
--------

[时得到评估复制工序的/dynamics365/operations/dev] (itpro/dev 评估) 复制 tools/get Dynamics /dynamics365/operations/dev


