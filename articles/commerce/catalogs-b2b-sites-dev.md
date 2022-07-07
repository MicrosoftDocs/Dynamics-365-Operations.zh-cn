---
title: B2B Commerce 目录自定义项的可扩展性影响
description: 本文介绍 Microsoft Dynamics 365 Commerce 中 B2B 的 Commerce 目录功能的可扩展性影响。
author: ashishmsft
ms.date: 04/28/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-02-28
ms.openlocfilehash: a9abdb5ea702917a745c3156f774aade757c159e
ms.sourcegitcommit: 6616b969afd6beb11a79d8e740560bf00016ea7f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/17/2022
ms.locfileid: "9027246"
---
# <a name="extensibility-impact-of-commerce-catalogs-for-b2b-customizations"></a>B2B Commerce 目录自定义项的可扩展性影响

[!include [banner](includes/banner.md)]

本文介绍 Microsoft Dynamics 365 Commerce 中 **B2B 的 Commerce 目录** 功能的可扩展性影响。

如果您有兴趣将目录上下文扩展到自定义场景，您的自定义项可能需要更新。 此更新遵循客户必须遵循的标准流程，因为他们的自定义项可能不会在升级完成后自动支持最新功能。 如果您的自定义项在体验中包含任何新功能或 Bug 修复，我们建议您相应地更新自定义代码。 此更新类似于 Microsoft 可能对核心代码所做的更改。

查看随后的自定义案例以确定是否必须更新您的自定义项。

> [!NOTE]
> - 所有商品化应用编程接口 (API) 都应该能够感知目录。 因此，传递 **CatalogID** 参数至关重要。
> - 默认目录 (**CatalogID**=**0**) 不是登录的企业到企业 (B2B) 用户的有效目录。 因此，传递“0”或使用默认值的所有 API 调用都将失败，因为站点用户无权访问目录 0。 要获得正确的体验，必须更新客户 API 调用，以便它们传递在目录选择器中选择的目录 ID。 如果您使用默认值，并且用户切换目录，则网站应提供所选目录的数据。 因此，为了匹配从核心 Commerce 代码运行的 API，自定义 API 应传递所选目录。

以下自定义案例需要开发更新：

- **案例 1：** 客户介绍了他们自己的[数据操作](e-commerce-extensibility/data-actions.md)，该操作将调用与产品相关的 API 或数据操作。 必须执行以下更新步骤：

    1. 如果数据操作使用直接 API 调用，请更新数据操作以使其传递目录 ID，如以下示例图所示。

        ![更新了传递目录 ID 的数据操作。](./media/customization1_a.png)

    1. 如果数据操作在自定义项中调用其他与产品相关的数据操作，则必须更新该代码，以便它传递一些新参数，例如 **requestContext**。 **requestContext** 参数用于检索当前目录 ID，如以下示例说明中所示。

        ![更新了传递新参数的数据操作。](./media/customization1_b.png)

- **案例 2：** 客户具有[覆盖的数据操作](e-commerce-extensibility/data-action-overrides.md)。 必须执行以下更新步骤：

    - 像案例 1 一样更新数据操作。

- **案例 3：** 客户具有视图扩展、脚本注入器模块或[克隆模块](e-commerce-extensibility/modules-overview.md#clone-a-module-library-module)，其中包括对 API 或数据操作的调用。 必须执行以下更新步骤：

    - 像案例 1 一样更新代码，如以下示例说明中所示。

       ![更新了传递新参数的代码。](./media/customization3.png)

- **案例 4：** 客户使用 **getById** API 调用。 必须执行以下更新步骤：

    - 改为切换到 **getByIds** API 调用，因为 **getById** APT 调用具有一些限制，并且不支持目录感知。

- **案例 5：** 客户具有数据操作，用于检索可能来自不同目录的多个产品的信息。 必须执行以下更新步骤：

    - 按目录 ID 拆分 API 调用。 例如，对于购物车 API，购物车可能包含来自不同目录的产品。 产品行应按目录 ID 分组，并且它们应分别针对每个目录调用此 API，如以下示例说明中所示。

        ![更新了按目录 ID 对产品线进行分组的数据操作。](./media/customization5.png)

## <a name="additional-resources"></a>其他资源

[为 B2B 站点创建 Commerce 目录](catalogs-b2b-sites.md)

[B2B 常见问题解答的 Commerce 目录](catalogs-b2b-sites-FAQ.md)
