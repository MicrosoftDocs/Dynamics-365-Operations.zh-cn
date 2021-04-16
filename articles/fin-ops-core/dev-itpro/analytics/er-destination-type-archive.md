---
title: 存档 ER 目标类型
description: 本主题提供有关如何为电子报告 (ER) 格式的每个文件夹或文件组件配置存档目标的信息。
author: NickSelin
ms.date: 11/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 18c662fee0cedaa55f63ffeb25b0d61ee7baffda
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753520"
---
# <a name="archive-er-destination-type"></a>存档 ER 目标类型

[!include [banner](../includes/banner.md)]

您可以为配置为生成出站文档的电子报告 (ER) 格式的每个 **文件夹** 或 **文件** 组件配置存档目标。 根据目标设置，将生成的文档存储为 ER 作业列表的记录附件。 若要查看结果，请转到 **组织管理** \> **电子申报** \> **电子申报作业**。

您可以使用此选项将生成的文档发送到 Microsoft SharePoint 文件夹或 Microsoft Azure Storage。 将 **已启用** 设置为 **是** 以将输出发送到由所选文档类型定义的目标。 仅组设置为 **文件** 的文档类型可供选择。 您在 **组织管理** \> **文档管理** \> **文档类型** 中定义文档[类型](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types)。 ER 目标的配置与文档管理系统的配置相同。

[![文档类型页面](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)

位置确定文件保存的位置。 启用 **存档** 目标之后，可将结果保存到作业存档中。 可以在 **组织管理** \> **电子申报** \> **电子申报存档作业** 中查看结果。

> [!NOTE]
> 通过导航到 **组织管理** \> **工作区** \> **电子报告** \> **电子报告参数**，为作业存档选择票据类型。 有关详细信息，请参阅[配置电子报告 (ER) 框架](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup)。

## <a name="sharepoint"></a>SharePoint

您可以在指定的 SharePoint 文件夹中保存文件。 要定义默认的 SharePoint 服务器，请转到 **组织管理** \> **文档管理** \> **文档管理参数**。 在 **SharePoint** 选项卡上，配置 SharePoint 件夹。 然后，您可以选择它作为保存 ER 输出的文件夹。 必须在此文档类型中选择 **SharePoint** 位置。

[![选择 SharePoint 文件夹](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)

## <a name="azure-storage"></a>Azure 储存

将文档类型位置设置为 **Azure 存储** 时，您可以将文件保存到 Azure 存储中。

> [!NOTE] 
> ER 框架将文件永久存储在 Azure Blob 存储中，这与数据管理框架不同，后者对必须处理的文档实施 7 天保留策略。 有关详细信息，请参阅[用于获取消息状态的 API](../data-entities/recurring-integrations.md#api-for-getting-message-status) 和 [状态检查 API](../data-entities/data-management-api.md#status-check-api)。 只要必须，与 ER 相关的文件都将作为应用程序表记录的附件存储在 Azure Blob 存储中。 单个文件将与该文件附加到的应用程序表记录一起从 Azure Blob 存储中删除。

## <a name="additional-resources"></a>其他资源

- [电子报告 (ER) 概览](general-electronic-reporting.md)
- [电子报告 (ER) 目标](electronic-reporting-destinations.md)
- [配置文档管理](../../fin-ops/organization-administration/configure-document-management.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]