---
title: 导入供应商目录
description: 此主题介绍供应商目录数据导入流程。
author: mkirknel
manager: tfehr
ms.date: 03/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendProspectiveVendorRegistrationRequests, CatVendorCatalogDetails, CatVendorCatalogReleaseApprovedProducts, CatVendorCMRDetails, CatVendorCatalogProductPerCompanyStatus, CatVendorMaintenanceEventLog, CatVendorCatalogReviewTool, CatVendorCatalogFileUpload, CatVendorCatalogMaintenanceRequest, CatVendorCatalogFileInLegalEntity, CatVendorCatalogSchema, CatVendorCatalogFilePreviewPane, CatVendorCatalogImportParameter
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: mkirknel
ms.search.validFrom: 2018-04-20
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 7ed2c50b28fdbd1baf4caa0a8a7f2f05d6a53fd6
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4423419"
---
# <a name="import-vendor-catalogs"></a>导入供应商目录

[!include[banner](../includes/banner.md)]

## <a name="vendor-catalogs-import"></a>供应商目录导入

在 Dynamics 365 Supply Chain Management 中，采购专员可以创建和维护公司员工的目录以在订购供内部使用的物料和服务时使用。 若要创建采购目录，您可以通过导入产品目录数据或通过将产品目录数据手动添加到基础产品，添加要向员工提供的物料和服务。 

可以上传客户从 Microsoft Dynamics 365 客户端提交的目录数据。

在目录维护请求 (CMR) 文件的窗体中，供应商提交给您的产品数据必须是 XML 文件格式。 CMR 文件应包含供应商向贵公司提供的产品的详细信息。

## <a name="import-vendor-catalog-data"></a>导入供应商目录数据

若要导入供应商目录数据，您必须完成以下任务：

1. 在数据管理工作区（已在其中定义了数据映射规则）中设置一个项目。 选择 **数据管理**，然后选择 **设置数据项目的角色**。

2. 设置采购类别层次结构，并将您的供应商分配到采购类别。 如果您使用了商品代码，则添加这些商品代码到采购类别中。 有关设置采购类别层次结构的信息，请参阅[设置采购类别层次结构](../procurement/tasks/set-up-procurement-category-hierarchy.md)。

3. 配置目录导入的供应商。 选择供应商，然后选择 **采购**  >  **设置**  >  **配置目录导入的供应商**。

4. 配置目录导入的工作流。 创建一个 CMR 文件模板，然后将其与供应商共享。

5. 选择 **采购** \> **通用** \> **目录** \> **供应商目录** 以创建供应商目录。 在此目录中对您从供应商处接收的目录维护请求 (CMR) 文件进行分组。 

6. 上载 CMR 文件。

7. 复查、审核或拒绝供应商目录中的产品。 将把这些产品自动映射到采购类别。 

将已审核的产品添加到基础产品，并将它们发放给所选的法人。 只有已审核的产品能添加到采购目录。

## <a name="generate-a-catalog-import-file-template"></a>生成目录导入文件模板

目录导入文件模板是您用于为供应商产品创建的 CMR 文件的 XSD 文件。 您可以使用 CMR 文件创建新的目录，替换现有目录或修改现有的目录。

1. 选择 **采购** \> **目录** \> **供应商目录**，然后双击要使用的目录。

2. 下载一个当前目录导入模板（XSD 文件）。 在 **更新目录** 页 **操作窗格** 上 **目录** 选项卡的 **相关信息** 组中，单击 **生成目录模板**，然后选择 **采购类别**。

    - 可使用 **采购类别** 选项生成包括供应商授权提供产品的采购类别的目录模板。

3. 在 **另存为** 对话框中，选择要存储目录文件模板和保存该文件的位置。

有关更多信息和示例，请参阅以下博客文章：[Dynamics AX 中的供应商目录](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/05/25/vendor-catalogs-in-dynamics-ax/)。
