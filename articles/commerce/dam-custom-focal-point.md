---
title: 自定义图像焦点
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 站点构建器中自定义图像焦点。
author: psimolin
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 9c8fc9a1f944d24aff3ab2923ca2715209a674e4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972924"
---
# <a name="customize-image-focal-points"></a><span data-ttu-id="c752d-103">自定义图像焦点</span><span class="sxs-lookup"><span data-stu-id="c752d-103">Customize image focal points</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c752d-104">此主题介绍如何在 Microsoft Dynamics 365 Commerce 站点构建器中自定义图像焦点。</span><span class="sxs-lookup"><span data-stu-id="c752d-104">This topic describes how to customize image focal points in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="c752d-105">概览</span><span class="sxs-lookup"><span data-stu-id="c752d-105">Overview</span></span>

<span data-ttu-id="c752d-106">将图像上传到 Commerce 站点构建器的媒体库中之后，系统将尝试确定该图像的焦点。</span><span class="sxs-lookup"><span data-stu-id="c752d-106">When an image is uploaded to the Commerce site builder Media Library, the system attempts to determine the focal point of the image.</span></span> <span data-ttu-id="c752d-107">例如，如果图像中有一个人，系统将默认把焦点设置为这个人的面部。</span><span class="sxs-lookup"><span data-stu-id="c752d-107">For example, if the image has a person on it, the system will set the focal point to the face of the person by default.</span></span> <span data-ttu-id="c752d-108">在大多数情况下，自动设置的焦点适合所有视区，但是有时您可能希望调整焦点，以确保始终显示图像的特定部分。</span><span class="sxs-lookup"><span data-stu-id="c752d-108">In most cases the automatically set focal point works well for all viewports, but sometimes you may want to adjust the focal point to ensure that a specific part of the image is always visible.</span></span>

### <a name="define-a-custom-focal-point-for-an-image"></a><span data-ttu-id="c752d-109">为图像定义自定义焦点</span><span class="sxs-lookup"><span data-stu-id="c752d-109">Define a custom focal point for an image</span></span>

<span data-ttu-id="c752d-110">若要为图像定义自定义焦点，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="c752d-110">To define a custom focal point for an image, follow these steps.</span></span>

1. <span data-ttu-id="c752d-111">在 Commerce 站点构建器的左侧导航窗格中，选择 **媒体库**。</span><span class="sxs-lookup"><span data-stu-id="c752d-111">In the left navigation pane of Commerce site builder, select **Media Library**.</span></span>
1. <span data-ttu-id="c752d-112">在主窗口中，选择要修改的图像。</span><span class="sxs-lookup"><span data-stu-id="c752d-112">In the main window, select the image you want to modify.</span></span>
1. <span data-ttu-id="c752d-113">在命令栏中，选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="c752d-113">On the command bar, select **Edit**.</span></span>
1. <span data-ttu-id="c752d-114">选择图像以进入 **编辑模式**。</span><span class="sxs-lookup"><span data-stu-id="c752d-114">Select the image to enter **Edit Mode**.</span></span>
1. <span data-ttu-id="c752d-115">在 **编辑模式** 下，选择 **更改焦点**。</span><span class="sxs-lookup"><span data-stu-id="c752d-115">Under **Edit Mode**, select **Change Focal Point**.</span></span> <span data-ttu-id="c752d-116">图像上方将显示一个圆形焦点控件。</span><span class="sxs-lookup"><span data-stu-id="c752d-116">A circular focal point control appears over the image.</span></span>
1. <span data-ttu-id="c752d-117">选择该焦点控件将其移到所需焦点上方。</span><span class="sxs-lookup"><span data-stu-id="c752d-117">Select the focal point control to move it over the desired focal point.</span></span>
1. <span data-ttu-id="c752d-118">完成后，在命令栏中选择 **保存**，然后选择 **完成编辑**。</span><span class="sxs-lookup"><span data-stu-id="c752d-118">When you're done, on the command bar select **Save**, and then select **Finish editing**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c752d-119">其他资源</span><span class="sxs-lookup"><span data-stu-id="c752d-119">Additional resources</span></span>

[<span data-ttu-id="c752d-120">数字资产管理概览</span><span class="sxs-lookup"><span data-stu-id="c752d-120">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="c752d-121">上传图像</span><span class="sxs-lookup"><span data-stu-id="c752d-121">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="c752d-122">上传视频</span><span class="sxs-lookup"><span data-stu-id="c752d-122">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="c752d-123">上传文件</span><span class="sxs-lookup"><span data-stu-id="c752d-123">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="c752d-124">裁剪图像</span><span class="sxs-lookup"><span data-stu-id="c752d-124">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="c752d-125">上传和提供静态文件</span><span class="sxs-lookup"><span data-stu-id="c752d-125">Upload and serve static files</span></span>](upload-serve-static-files.md)
