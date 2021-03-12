---
title: 在仓库应用中使用摄像头扫描条码
description: 本主题介绍如何设置仓库应用以在移动设备上使用摄像头扫描条码。
author: MarkusFogelberg
manager: tfehr
ms.date: 01/03/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 71ec15b2568eefd8bea99e64c258a65461a7ad95
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965621"
---
# <a name="scan-bar-codes-using-a-camera-in-the-warehouse-app"></a><span data-ttu-id="7148a-103">在仓库应用中使用摄像头扫描条码</span><span class="sxs-lookup"><span data-stu-id="7148a-103">Scan bar codes using a camera in the warehouse app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7148a-104">本主题介绍如何设置仓库应用以在移动设备上使用摄像头扫描条码。</span><span class="sxs-lookup"><span data-stu-id="7148a-104">This topic explains how to set up the warehouse app to scan bar codes using a camera on a mobile device.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="7148a-105">先决条件</span><span class="sxs-lookup"><span data-stu-id="7148a-105">Prerequisites</span></span>
<span data-ttu-id="7148a-106">若要使用此功能，需要安装仓库应用版本 1.2.0.0，并且设备必须有摄像头。</span><span class="sxs-lookup"><span data-stu-id="7148a-106">To use this feature, you need to have version 1.2.0.0 of the warehouse app installed, and your device must have a camera.</span></span> <span data-ttu-id="7148a-107">更新后打开该应用程序时，系统将提示您允许此应用程序使用摄像头。</span><span class="sxs-lookup"><span data-stu-id="7148a-107">When you open the app after updating, you will be prompted to allow the app to use the camera.</span></span> <span data-ttu-id="7148a-108">如果设备没有摄像头，将不显示此提示，而您则不能将摄像头用作扫描仪。</span><span class="sxs-lookup"><span data-stu-id="7148a-108">If your device doesn’t have a camera, no prompt will be shown, and you will not be able to use a camera as a scanner.</span></span> 

## <a name="setup"></a><span data-ttu-id="7148a-109">设置</span><span class="sxs-lookup"><span data-stu-id="7148a-109">Setup</span></span>
<span data-ttu-id="7148a-110">在仓库应用的“显示”设置中，可选择是否应将摄像头用于执行条码扫描。</span><span class="sxs-lookup"><span data-stu-id="7148a-110">In the Display settings of the warehouse application, you can select if the camera should be used for bar code scanning.</span></span> <span data-ttu-id="7148a-111">如果启用 **将摄像头用作扫描仪**，则可在将首选输入模式设置为 **扫描** 的每个输入字段中使用摄像头。</span><span class="sxs-lookup"><span data-stu-id="7148a-111">If you enable **Use the camera as scanner**, you can use the camera on every input field that has the preferred input mode set to **Scanning**.</span></span> 

<span data-ttu-id="7148a-112">若要控制输入字段是否应可扫描，请将 **仓库应用字段名** 页面上的 **首选输入模式** 设置为 **扫描**。</span><span class="sxs-lookup"><span data-stu-id="7148a-112">To control whether an input field should be scannable, on the **Warehouse app field names** page, set **Preferred input mode** to **Scanning**.</span></span> <span data-ttu-id="7148a-113">选择此选项之后，可在仓库应用中将摄像头用于扫描。</span><span class="sxs-lookup"><span data-stu-id="7148a-113">When this option is selected, a camera can be used for scanning in the warehouse app.</span></span> <span data-ttu-id="7148a-114">有关如何配置 Warehousing 中的应用程序字段名的信息，请参阅[配置仓库应用中的应用字段名](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse)。</span><span class="sxs-lookup"><span data-stu-id="7148a-114">For information about how to configure app field names in Warehousing, see [Configure app field names in warehouse app](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse).</span></span>

## <a name="supported-bar-code-formats"></a><span data-ttu-id="7148a-115">支持的条码格式</span><span class="sxs-lookup"><span data-stu-id="7148a-115">Supported bar code formats</span></span>
<span data-ttu-id="7148a-116">支持最常见的条码格式，包括 Code 128、Code 39、Code 93、EAN-8、EAN-13、UPC-E、UPC-A 和 QR 码。</span><span class="sxs-lookup"><span data-stu-id="7148a-116">The most common bar code formats are supported, including Code 128, Code 39, Code 93, EAN-8, EAN-13, UPC-E, UPC-A, and QR codes.</span></span> 

## <a name="navigation"></a><span data-ttu-id="7148a-117">导航</span><span class="sxs-lookup"><span data-stu-id="7148a-117">Navigation</span></span>
<span data-ttu-id="7148a-118">在输入字段的首选输入模式设置为“扫描”的每个页面上，将启动摄像头页面。进入“摄像头”页面后，请使用以下选项进行导航：</span><span class="sxs-lookup"><span data-stu-id="7148a-118">The camera page will be initiated on each page where the input field has the preferred input mode set to Scanning, when you are on the Camera page use the following options to navigate:</span></span>
- <span data-ttu-id="7148a-119">单击后退按钮将返回到“任务和详细信息”页面。</span><span class="sxs-lookup"><span data-stu-id="7148a-119">Click the back button to go back to the Task and details page.</span></span> 
- <span data-ttu-id="7148a-120">单击“任务和详细信息”页面上的铅笔将转到可手动键入输入的页面。</span><span class="sxs-lookup"><span data-stu-id="7148a-120">Click the pencil on the Task and details page to go to the page where you can type input manually.</span></span>
- <span data-ttu-id="7148a-121">单击“任务和详细信息”页面上的摄像头将返回到“摄像头”页面。</span><span class="sxs-lookup"><span data-stu-id="7148a-121">Click the camera on the Task and details page to go back to the Camera page.</span></span> 

| <span data-ttu-id="7148a-122">“任务和详细信息”页</span><span class="sxs-lookup"><span data-stu-id="7148a-122">Task and details page</span></span> | <span data-ttu-id="7148a-123">“摄像头”页</span><span class="sxs-lookup"><span data-stu-id="7148a-123">Camera page</span></span> | 
| :---------------------: | :--------------------: |
| ![扫描示例任务详细信息的摄像头页面](./media/camera-scanning-example-task-detail-page50.png)          | ![扫描示例的摄像头页面缩小](./media/camera-scanning-example-camera-page50.png)          |

<span data-ttu-id="7148a-126">在摄像头页面中，如果单击“摄像头”按钮，尝试识别条码时页面将变暗。</span><span class="sxs-lookup"><span data-stu-id="7148a-126">On the camera page, when you click the Camera button, it will appear dimmed while trying to identify a bar code.</span></span> <span data-ttu-id="7148a-127">如果条码在 5 秒钟内无法识别，此过程将超时，而“摄像头”按钮将再次变为可用。</span><span class="sxs-lookup"><span data-stu-id="7148a-127">If a bar code is not identified within 5 seconds, the process will time out and the Camera button will become available again.</span></span> <span data-ttu-id="7148a-128">然后就可以再次尝试扫描条码。</span><span class="sxs-lookup"><span data-stu-id="7148a-128">You will then be able to try to scan a bar code again.</span></span>

<span data-ttu-id="7148a-129">将摄像头对准条码时，请让条码在括号内对齐，以达到最佳效果。</span><span class="sxs-lookup"><span data-stu-id="7148a-129">When you aim the camera at a bar code, keep the bar code aligned within the brackets for best result.</span></span> <span data-ttu-id="7148a-130">条码扫描成功后，将处理结果，并转到下一步。</span><span class="sxs-lookup"><span data-stu-id="7148a-130">When a bar code is scanned successfully, the result will be processed, and you will be taken to the next step.</span></span> <span data-ttu-id="7148a-131">如果下一步中又包含一个将首选输入模式设置为“扫描”的输入字段，将再次启动摄像头页面。</span><span class="sxs-lookup"><span data-stu-id="7148a-131">If the next step contains another input field with the preferred input mode set to Scanning, the camera page will start again.</span></span> <span data-ttu-id="7148a-132">如果下一步不是扫描字段，则不会启动摄像头页面。</span><span class="sxs-lookup"><span data-stu-id="7148a-132">If the next step is not a scanning field, then the camera page will not be initiated.</span></span>

