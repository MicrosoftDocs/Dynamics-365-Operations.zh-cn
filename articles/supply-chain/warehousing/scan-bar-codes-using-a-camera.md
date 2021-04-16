---
title: 在仓库管理移动应用中使用相机扫描条码
description: 本主题介绍如何设置仓库管理移动应用以在移动设备上使用相机扫描条码。
author: MarkusFogelberg
ms.date: 01/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 2f61f9c45b95b730a7f1743963658ec00abfbb56
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831210"
---
# <a name="scan-bar-codes-using-a-camera-in-the-warehouse-management-mobile-app"></a><span data-ttu-id="2d697-103">在仓库管理移动应用中使用相机扫描条码</span><span class="sxs-lookup"><span data-stu-id="2d697-103">Scan bar codes using a camera in the Warehouse Management mobile app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2d697-104">本主题介绍如何设置仓库管理移动应用以在移动设备上使用相机扫描条码。</span><span class="sxs-lookup"><span data-stu-id="2d697-104">This topic explains how to set up the Warehouse Management mobile app to scan bar codes using a camera on a mobile device.</span></span>

## <a name="setup"></a><span data-ttu-id="2d697-105">设置</span><span class="sxs-lookup"><span data-stu-id="2d697-105">Setup</span></span>

<span data-ttu-id="2d697-106">在仓库管理移动应用的显示设置中，可选择是否应将相机用于条码扫描。</span><span class="sxs-lookup"><span data-stu-id="2d697-106">In the display settings of the Warehouse Management mobile app, you can select if the camera should be used for bar code scanning.</span></span> <span data-ttu-id="2d697-107">如果启用 **将摄像头用作扫描仪**，则可在将首选输入模式设置为 **扫描** 的每个输入字段中使用摄像头。</span><span class="sxs-lookup"><span data-stu-id="2d697-107">If you enable **Use the camera as scanner**, you can use the camera on every input field that has the preferred input mode set to **Scanning**.</span></span>

<span data-ttu-id="2d697-108">若要控制输入字段是否应可扫描，请将 **仓库应用字段名** 页面上的 **首选输入模式** 设置为 **扫描**。</span><span class="sxs-lookup"><span data-stu-id="2d697-108">To control whether an input field should be scannable, on the **Warehouse app field names** page, set **Preferred input mode** to **Scanning**.</span></span> <span data-ttu-id="2d697-109">选择此选项后，可在仓库管理移动应用中将相机用于扫描。</span><span class="sxs-lookup"><span data-stu-id="2d697-109">When this option is selected, a camera can be used for scanning in the Warehouse Management mobile app.</span></span> <span data-ttu-id="2d697-110">有关详细信息，请参阅[为仓库管理移动应用配置字段](configure-app-field-names-priorities-warehouse.md)。</span><span class="sxs-lookup"><span data-stu-id="2d697-110">For more information, see [Configure fields for the Warehouse Management mobile app](configure-app-field-names-priorities-warehouse.md).</span></span>

## <a name="supported-bar-code-formats"></a><span data-ttu-id="2d697-111">支持的条码格式</span><span class="sxs-lookup"><span data-stu-id="2d697-111">Supported bar code formats</span></span>

<span data-ttu-id="2d697-112">支持最常见的条码格式，包括 Code 128、Code 39、Code 93、EAN-8、EAN-13、UPC-E、UPC-A 和 QR 码。</span><span class="sxs-lookup"><span data-stu-id="2d697-112">The most common bar code formats are supported, including Code 128, Code 39, Code 93, EAN-8, EAN-13, UPC-E, UPC-A, and QR codes.</span></span>

## <a name="navigation"></a><span data-ttu-id="2d697-113">导航</span><span class="sxs-lookup"><span data-stu-id="2d697-113">Navigation</span></span>

<span data-ttu-id="2d697-114">在输入字段的 **首选输入模式** 设置为 *扫描* 的每个页面上，将启动相机页面。进入相机页面后，请使用以下选项进行导航：</span><span class="sxs-lookup"><span data-stu-id="2d697-114">The camera page will be initiated on each page where the input field has its **Preferred input mode** set to *Scanning*, when you are on the camera page use the following options to navigate:</span></span>

- <span data-ttu-id="2d697-115">选择后退按钮以返回到 **任务和详细信息** 页面。</span><span class="sxs-lookup"><span data-stu-id="2d697-115">Select the back button to go back to the **Task and details** page.</span></span>
- <span data-ttu-id="2d697-116">选择 **任务和详细信息** 页面上的铅笔以转到可手动键入输入的页面。</span><span class="sxs-lookup"><span data-stu-id="2d697-116">Select the pencil on the **Task and details** page to go to the page where you can type input manually.</span></span>
- <span data-ttu-id="2d697-117">选择 **任务和详细信息** 页面上的相机以返回到相机页面。</span><span class="sxs-lookup"><span data-stu-id="2d697-117">Select the camera on the **Task and details** page to go back to the camera page.</span></span>

<span data-ttu-id="2d697-118">在相机页面上，如果选择相机按钮，在尝试识别条码时页面将变暗。</span><span class="sxs-lookup"><span data-stu-id="2d697-118">On the camera page, when you select the camera button, it will appear dimmed while trying to identify a bar code.</span></span> <span data-ttu-id="2d697-119">如果条码在 5 秒钟内无法识别，此流程将超时，而相机按钮将再次变为可用。</span><span class="sxs-lookup"><span data-stu-id="2d697-119">If a bar code is not identified within 5 seconds, the process will time out and the camera button will become available again.</span></span> <span data-ttu-id="2d697-120">然后就可以再次尝试扫描条码。</span><span class="sxs-lookup"><span data-stu-id="2d697-120">You will then be able to try to scan a bar code again.</span></span>

<span data-ttu-id="2d697-121">将摄像头对准条码时，请让条码在括号内对齐，以达到最佳效果。</span><span class="sxs-lookup"><span data-stu-id="2d697-121">When you aim the camera at a bar code, keep the bar code aligned within the brackets for best result.</span></span> <span data-ttu-id="2d697-122">条码扫描成功后，将处理结果，并转到下一步。</span><span class="sxs-lookup"><span data-stu-id="2d697-122">When a bar code is scanned successfully, the result will be processed, and you will be taken to the next step.</span></span> <span data-ttu-id="2d697-123">如果下一步中又包含一个将首选输入模式设置为“扫描”的输入字段，将再次启动摄像头页面。</span><span class="sxs-lookup"><span data-stu-id="2d697-123">If the next step contains another input field with the preferred input mode set to Scanning, the camera page will start again.</span></span> <span data-ttu-id="2d697-124">如果下一步不是扫描字段，则不会启动摄像头页面。</span><span class="sxs-lookup"><span data-stu-id="2d697-124">If the next step is not a scanning field, then the camera page will not be initiated.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]