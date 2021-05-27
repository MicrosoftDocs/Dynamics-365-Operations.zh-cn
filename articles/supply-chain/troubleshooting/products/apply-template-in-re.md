---
title: 您不能将模板应用于已发布产品
description: 您不能将模板应用于已发布产品。
author: t-benebo
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: EcoResProductDetailsExtended
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1ad6efdced9bce924fbf5bc207c92fa2c3a6c79d
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026296"
---
# <a name="you-cant-apply-a-template-to-create-a-released-product"></a><span data-ttu-id="1e35a-103">您不能应用模板来创建已发布产品</span><span class="sxs-lookup"><span data-stu-id="1e35a-103">You can't apply a template to create a released product</span></span>

<span data-ttu-id="1e35a-104">知识库编号：4612097</span><span class="sxs-lookup"><span data-stu-id="1e35a-104">KB number: 4612097</span></span>

## <a name="symptoms"></a><span data-ttu-id="1e35a-105">故障特征</span><span class="sxs-lookup"><span data-stu-id="1e35a-105">Symptoms</span></span>

<span data-ttu-id="1e35a-106">使用 **新建已发布产品** 对话框创建新的已发布产品时，可以选择一个模板。</span><span class="sxs-lookup"><span data-stu-id="1e35a-106">When you create a new released product by using the **New released product** dialog box, you can select a template.</span></span> <span data-ttu-id="1e35a-107">模板应会为新的已发布产品的很多字段提供默认设置。</span><span class="sxs-lookup"><span data-stu-id="1e35a-107">The template is supposed to provide default settings for many fields of the new released product.</span></span> <span data-ttu-id="1e35a-108">但是，选择模板后部分或全部字段并未设置。</span><span class="sxs-lookup"><span data-stu-id="1e35a-108">However, some or all of the fields aren't set after you select the template.</span></span>

## <a name="cause"></a><span data-ttu-id="1e35a-109">原因</span><span class="sxs-lookup"><span data-stu-id="1e35a-109">Cause</span></span>

<span data-ttu-id="1e35a-110">通过 Microsoft Dynamics 365 Supply Chain Management 中的很多页面，您都可以创建模板来为这些页面上显示的记录建立初始设置。</span><span class="sxs-lookup"><span data-stu-id="1e35a-110">Many pages in Microsoft Dynamics 365 Supply Chain Management let you create a template that establishes initial settings for the records that are shown on those pages.</span></span> <span data-ttu-id="1e35a-111">您可以通过在操作窗格的 **选项** 选项卡上选择 **记录信息** 来创建一个模板。</span><span class="sxs-lookup"><span data-stu-id="1e35a-111">You can create one of these templates by selecting **Record info** on the **Options** tab of the Action Pane.</span></span> <span data-ttu-id="1e35a-112">不过，已发布产品比大多数其他类型的记录要复杂得多。</span><span class="sxs-lookup"><span data-stu-id="1e35a-112">However, released products are much more complex than most other types of records.</span></span> <span data-ttu-id="1e35a-113">虽然您可以在 **已发布产品** 页上选择 **记录信息** 来创建模板，并且可以在创建已发布产品时选择该模板，但是此模板不会为新的已发布产品提供预期的字段值。</span><span class="sxs-lookup"><span data-stu-id="1e35a-113">Although you can select **Record info** on the **Released products** page to create a template, and although you can select that template when you create a released product, the template won't provide the expected field values for the new released product.</span></span> <span data-ttu-id="1e35a-114">因此，您不能为已发布产品使用“记录信息”模板。</span><span class="sxs-lookup"><span data-stu-id="1e35a-114">Therefore, you can't use "record info" templates for released products.</span></span> <span data-ttu-id="1e35a-115">而是必须创建专用的产品模板。</span><span class="sxs-lookup"><span data-stu-id="1e35a-115">Instead, you must create dedicated product templates.</span></span>

## <a name="resolution"></a><span data-ttu-id="1e35a-116">解决方法</span><span class="sxs-lookup"><span data-stu-id="1e35a-116">Resolution</span></span>

<span data-ttu-id="1e35a-117">要创建产品模板，使用操作窗格的 **产品** 选项卡上的 **模板** 菜单，不要使用 **选项** 选项卡上的 **记录信息** 按钮。</span><span class="sxs-lookup"><span data-stu-id="1e35a-117">To create a product template, use the **Template** menu on the **Product** tab of the Action Pane, not the **Record info** button on the **Options** tab.</span></span>

1. <span data-ttu-id="1e35a-118">转到 **产品信息管理 \> 产品 \> 已发布产品**。</span><span class="sxs-lookup"><span data-stu-id="1e35a-118">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="1e35a-119">在操作窗格上，在 **产品** 选项卡上的 **新建** 组中，选择 **模板**，然后视情况选择 **创建个人模板** 或 **创建共享模板**。</span><span class="sxs-lookup"><span data-stu-id="1e35a-119">On the Action Pane, on the **Product** tab, in the **New** group, select **Template**, and then select either **Create personal template** or **Create shared template**, as appropriate.</span></span>
