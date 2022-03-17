---
title: 试用分布式混合拓扑中的缩放单元
description: 本主题提供有关如何针对制造和仓库管理工作负荷试用云和边缘缩放单元的信息。
author: perlynne
ms.date: 03/03/2022
ms.topic: article
ms.search.form: ScaleUnitWorkloadsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-03-03
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 04fd79f3c582ae9ac51882f73410477efaa35496
ms.sourcegitcommit: b52ff5dfd32580121f74a5f262e5c2495e39d578
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/03/2022
ms.locfileid: "8376238"
---
# <a name="try-out-scale-units-in-a-distributed-hybrid-topology"></a>试用分布式混合拓扑中的缩放单元

[!include [banner](../includes/banner.md)]

试用分布式混合拓扑的过程很简单。 在第一个阶段中，您应该验证自定义以确保它们可在分布式拓扑中工作。 您有两个选项。

## <a name="option-1-evaluate-customizations-in-development-environments"></a>选项 1：在开发环境中评估自定义

在开始加入沙盒环境之前，建议您在开发设置中探索缩放单元，例如单盒环境（也称为第 1 层环境），以便您可以验证流程、自定义和解决方案。 在此阶段中，数据和自定义将应用到单盒环境。 您可以在单一环境中运行，该环境可以同时充当企业中心和缩放单元的角色。 或者，您可以使用两个开发环境，一个充当中心角色，另一个充当缩放单元角色。 此设置提供识别和修复问题的最佳方法。 最新的[提前访问 (PEAP) 版本](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxURUFWTjQzTzg0UUk5RkJHMDFEMVlSSDFEQy4u)也可以用于完成此阶段。

您应该使用[单盒开发环境的缩放单元部署工具](https://github.com/microsoft/SCMScaleUnitDevTools)安装和维护环境。 这些工具使您可以在一个或两个单盒环境中配置中心和缩放单元。 这些工具均作为二进制版本提供，并在 GitHub 上以源代码的形式提供。 研究项目 wiki，其中包括描述如何使用工具的[分步使用指南](https://github.com/microsoft/SCMScaleUnitDevTools/wiki/Step-by-step-usage-guide)。 如果您[使用本地业务数据 (LBD) 在自定义硬件上部署边缘缩放单元](cloud-edge-edge-scale-units-lbd.md)，则必须执行不同的流程。

## <a name="option-2-acquire-add-ins-and-deploy-in-your-sandbox-environments"></a>选项 2：获取加载项，并在沙盒环境中进行部署

要试用分布式混合拓扑，您必须有两个沙箱环境（第 2 层），一个包含您的数据（企业中心），另一个用于缩放单元，包含“空数据”。

您必须为至少一个云或边缘缩放单元获取加载项。 然后将在 [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/) 中授予相应的项目和环境插槽，以可以使用[缩放单元管理器门户](https://aka.ms/SCMSUM)部署缩放单元环境。

联系 Microsoft 支持部门请求启用沙盒环境。

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
