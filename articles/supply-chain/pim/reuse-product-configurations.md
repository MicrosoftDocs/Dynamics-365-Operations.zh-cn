---
title: 重复使用产品配置
description: 可以指定要自动重用产品的现有配置。 然后，当用户完成配置会话后，系统会验证匹配用户选择的配置是否存在。 如果找到匹配配置，则再用配置 ID、相应的物料清单 (BOM) 以及路径。
author: cvocph
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: 201813
ms.assetid: 4985e308-7824-41fc-83fd-fd0bdae888e3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 21dc25b878ff65b57b060fe3d74b5d120fa4b5cd
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5260591"
---
# <a name="reuse-product-configurations"></a><span data-ttu-id="29694-105">重复使用产品配置</span><span class="sxs-lookup"><span data-stu-id="29694-105">Reuse product configurations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="29694-106">可以指定要自动重用产品的现有配置。</span><span class="sxs-lookup"><span data-stu-id="29694-106">You can specify that you want to automatically reuse an existing configuration for a product.</span></span> <span data-ttu-id="29694-107">然后，当用户完成配置会话后，系统会验证匹配用户选择的配置是否存在。</span><span class="sxs-lookup"><span data-stu-id="29694-107">Then, when a user has completed a configuration session, the system verifies whether a configuration that matches the user’s selections already exists.</span></span> <span data-ttu-id="29694-108">如果找到匹配配置，则再用配置 ID、相应的物料清单 (BOM) 以及路径。</span><span class="sxs-lookup"><span data-stu-id="29694-108">If a matching configuration is found, the configuration ID, corresponding bill of materials (BOM), and route are reused.</span></span>

<a name="requirements-for-reusing-configurations"></a><span data-ttu-id="29694-109">要再用配置的要求</span><span class="sxs-lookup"><span data-stu-id="29694-109">Requirements for reusing configurations</span></span>
---------------------------------------

<span data-ttu-id="29694-110">若要启用将重复使用的配置，必须在 **产品配置模型详细信息** 页上指定组件和属性的以下信息：</span><span class="sxs-lookup"><span data-stu-id="29694-110">To enable configurations to be reused, you must specify the following information for the components and attributes on the **Product configuration model details** page:</span></span>

-   <span data-ttu-id="29694-111">**组件和子组件** - 在 **常规** 快速选项卡上，在 **重复使用配置** 字段中，选择 **是**。</span><span class="sxs-lookup"><span data-stu-id="29694-111">**Components and subcomponents** – On the **General** FastTab, in the **Reuse configurations** field, select **Yes**.</span></span>
-   <span data-ttu-id="29694-112">**属性** – 在 **属性** 快速选项卡上，选择 **包括在重复使用中** 选项。</span><span class="sxs-lookup"><span data-stu-id="29694-112">**Attributes** – On the **Attributes** FastTab, select the **Include in reuse** option.</span></span> <span data-ttu-id="29694-113">仅在相关组件启用重复使用时才显示此选项。</span><span class="sxs-lookup"><span data-stu-id="29694-113">This option appears only when the related component is enabled for reuse.</span></span> <span data-ttu-id="29694-114">如果未选择要重复使用的任何属性，则始终重复使用该配置，这与配置会话期间的用户选择无关。</span><span class="sxs-lookup"><span data-stu-id="29694-114">If you don't select any attributes for reuse, the configuration is always reused, regardless of the user’s selections during a configuration session.</span></span> <span data-ttu-id="29694-115">现有配置中的属性值必须匹配用户的选择。</span><span class="sxs-lookup"><span data-stu-id="29694-115">The attribute values in the existing configuration must match the user’s selections.</span></span> <span data-ttu-id="29694-116">例如，如果在配置会话期间，用户选择颜色为 **蓝色**，则系统将验证组件的现有配置是否具有蓝色。</span><span class="sxs-lookup"><span data-stu-id="29694-116">For example, if the user selects **Blue** as the color during a configuration session, the system verifies whether an existing configuration of the component has the color blue.</span></span>

## <a name="resetting-configuration-reuse"></a><span data-ttu-id="29694-117">重置配置重复使用</span><span class="sxs-lookup"><span data-stu-id="29694-117">Resetting configuration reuse</span></span>
<span data-ttu-id="29694-118">在您重置配置重复使用后，不再考虑以前创建的配置。</span><span class="sxs-lookup"><span data-stu-id="29694-118">When you reset configuration reuse, previously created configurations are no longer considered.</span></span> <span data-ttu-id="29694-119">更改物料清单或工艺路线，但不更改相关属性时，您可能要重置配置重复使用。</span><span class="sxs-lookup"><span data-stu-id="29694-119">You might want to reset configuration reuse if the BOM or route was changed, but no related attributes were changed.</span></span> <span data-ttu-id="29694-120">在该组件的 **常规** 快速选项卡上重置配置重复使用。</span><span class="sxs-lookup"><span data-stu-id="29694-120">You reset configuration reuse on the **General** FastTab for the component.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]