---
title: 监视和管理 IoT 智能
description: 本主题说明如何监视和管理 IoT 智能。
author: robinarh
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: ''
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 05aee9865dc90c97e026d5c05fa2032fc0625f7a
ms.sourcegitcommit: f64fce03ec52f844b05a9e8cac286cb201385002
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/16/2020
ms.locfileid: "3597400"
---
# <a name="monitor-and-manage-iot-intelligence"></a><span data-ttu-id="f4172-103">监视和管理 IoT 智能</span><span class="sxs-lookup"><span data-stu-id="f4172-103">Monitor and manage IoT Intelligence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f4172-104">本主题说明如何监视和管理 IoT 智能。</span><span class="sxs-lookup"><span data-stu-id="f4172-104">This topic explains how to monitor and manage IoT Intelligence.</span></span>

## <a name="monitor-scenarios-in-microsoft-dynamics-365-supply-chain-management"></a><a id="monitor-scenarios"></a><span data-ttu-id="f4172-105">在Microsoft Dynamics 365 Supply Chain Management 中监视方案</span><span class="sxs-lookup"><span data-stu-id="f4172-105">Monitor scenarios in Microsoft Dynamics 365 Supply Chain Management</span></span>

<span data-ttu-id="f4172-106">可以从多个位置监视 IoT 智能处理：</span><span class="sxs-lookup"><span data-stu-id="f4172-106">You can monitor IoT Intelligence processing from several places:</span></span>

+ <span data-ttu-id="f4172-107">**模块 \> 生产控制 \> 查询和报表 \> IoT 智能 \> 通知** – 查看未解决通知列表。</span><span class="sxs-lookup"><span data-stu-id="f4172-107">**Modules \> Production control \> Inquiries and reports \> IoT Intelligence \> Notifications** – View the list of unresolved notifications.</span></span>
+ <span data-ttu-id="f4172-108">**模块 \> 生产控制 \> 查询和报表 \> IoT 智能 \> 已关闭通知** – 查看已解决或隐藏通知列表。</span><span class="sxs-lookup"><span data-stu-id="f4172-108">**Modules \> Production control \> Inquiries and reports \> IoT Intelligence \> Closed notifications** – View the list of notifications that have been resolved or dismissed.</span></span>
+ <span data-ttu-id="f4172-109">**模块 \> 生产控制 \> 查询和报表 \> IoT 智能 \> 指标键** – 查看**资源状态**时间系列图表的指标键。</span><span class="sxs-lookup"><span data-stu-id="f4172-109">**Modules \> Production control \> Inquiries and reports \> IoT Intelligence \> Metric keys** – View the metric keys for the **Resource Status** times series charts.</span></span>
+ <span data-ttu-id="f4172-110">**模块 \> 生产控制 \> 制造执行 \> 资源状态** – 使用**配置**对话框跟踪特定度量。</span><span class="sxs-lookup"><span data-stu-id="f4172-110">**Modules \> Production control \> Manufacturing execution \> Resource status** – Track specific metrics by using the **Configure** dialog box.</span></span> <span data-ttu-id="f4172-111">如果方案检测到异常，通知将显示该异常的详细信息。</span><span class="sxs-lookup"><span data-stu-id="f4172-111">If a scenario detects an exception, a notification shows the details of the exception.</span></span>
+ <span data-ttu-id="f4172-112">**工作区 \> 生产车间管理 \> 通知** – 查看未解决通知列表。</span><span class="sxs-lookup"><span data-stu-id="f4172-112">**Workspaces \> Production floor management \> Notifications** – View the list of unresolved notifications.</span></span>

## <a name="modify-a-running-iot-intelligence-scenario"></a><span data-ttu-id="f4172-113">修改正在运行的 IoT 智能方案</span><span class="sxs-lookup"><span data-stu-id="f4172-113">Modify a running IoT Intelligence scenario</span></span>

<span data-ttu-id="f4172-114">运行方案时，可以进行以下更改：</span><span class="sxs-lookup"><span data-stu-id="f4172-114">When a scenario is running, you can make these changes:</span></span>

+ <span data-ttu-id="f4172-115">添加新传感器架构定义。</span><span class="sxs-lookup"><span data-stu-id="f4172-115">Add new sensor schema definitions.</span></span>
+ <span data-ttu-id="f4172-116">选择新信号数据值。</span><span class="sxs-lookup"><span data-stu-id="f4172-116">Select new signal data values.</span></span>
+ <span data-ttu-id="f4172-117">取消选择现有信号数据值。</span><span class="sxs-lookup"><span data-stu-id="f4172-117">Cancel the selection of existing signal data values.</span></span>
+ <span data-ttu-id="f4172-118">添加和映射新信号数据值。</span><span class="sxs-lookup"><span data-stu-id="f4172-118">Add and map new signal data values.</span></span>
+ <span data-ttu-id="f4172-119">更新阈值。</span><span class="sxs-lookup"><span data-stu-id="f4172-119">Update threshold values.</span></span>

<span data-ttu-id="f4172-120">运行方案时，不能进行以下更改：</span><span class="sxs-lookup"><span data-stu-id="f4172-120">When a scenario is running, these changes are prohibited:</span></span>

+ <span data-ttu-id="f4172-121">删除或修改已启用方案当前使用的任何架构定义。</span><span class="sxs-lookup"><span data-stu-id="f4172-121">Delete or modify any schema definitions that are currently consumed by an enabled scenario.</span></span>
+ <span data-ttu-id="f4172-122">更改所启用方案的所选架构路径。</span><span class="sxs-lookup"><span data-stu-id="f4172-122">Change the enabled scenario's selected schema paths.</span></span>

## <a name="simulation-options"></a><span data-ttu-id="f4172-123">模拟选项</span><span class="sxs-lookup"><span data-stu-id="f4172-123">Simulation options</span></span>

<span data-ttu-id="f4172-124">您可以模拟工厂机器信号。</span><span class="sxs-lookup"><span data-stu-id="f4172-124">You can simulate factory machine signals.</span></span> <span data-ttu-id="f4172-125">有关详细信息，请参阅以下主题：</span><span class="sxs-lookup"><span data-stu-id="f4172-125">For more information, see these topics:</span></span>

+ [<span data-ttu-id="f4172-126">将 IoT DevKit AZ3166 连接到 Azure IoT 中心</span><span class="sxs-lookup"><span data-stu-id="f4172-126">Connect IoT DevKit AZ3166 to Azure IoT Hub</span></span>](https://docs.microsoft.com/azure/iot-hub/iot-hub-arduino-iot-devkit-az3166-get-started)
+ [<span data-ttu-id="f4172-127">将 Raspberry Pi 联机模拟器连接到 Azure IoT 中心 (Node.js)</span><span class="sxs-lookup"><span data-stu-id="f4172-127">Connect Raspberry Pi online simulator to Azure IoT Hub (Node.js)</span></span>](https://docs.microsoft.com/azure/iot-hub/iot-hub-raspberry-pi-web-simulator-get-started)
+ [<span data-ttu-id="f4172-128">设备模拟解决方案加速器概述</span><span class="sxs-lookup"><span data-stu-id="f4172-128">Device Simulation solution accelerator overview</span></span>](https://docs.microsoft.com/azure/iot-accelerators/iot-accelerators-device-simulation-overview)
