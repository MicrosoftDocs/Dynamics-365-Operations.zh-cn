---
title: 电子开票设置
description: 本文概述了设置和配置电子开票的流程。
author: gionoder
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: de94843c1e98a8788375bd41def587a64baea07d
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272170"
---
# <a name="electronic-invoicing-setup"></a>电子开票设置

[!include [banner](../includes/banner.md)]

本文概述了设置和配置电子开票的流程。 您必须按照此处指定的顺序完成设置步骤。 如果某个步骤是必需的，但您跳过了它，此功能将无法正常工作，并且在后续步骤或您使用此功能时会多次出现失败。 

在开始之前，请确保所有主要组件均已正确设置，您已注册监管 Regulatory Configuration Service (RCS) 并且已有 RCS 实例，且已为您的 Microsoft Dynamics 365 Finance 或 Dynamics 365 Supply Chain Management 环境安装了电子开票加载项。 有关详细信息，请参阅[注册并安装电子开票](e-invoicing-install-add-in-microservices-lcs.md)。

接下来，设置电子开票完成工作所需的 Azure 资源。 有关详细信息，请参阅[设置电子开票的 Azure 资源](e-invoicing-set-up-azure-resources.md)。

配置主要组件后，使用 RCS 设置电子开票的主要逻辑组件。 首先，定义您将维护的服务环境的数量。 这样，您可以定义逻辑数据和配置分区，以确保您在开发或测试环境与生产环境之间有一个边界。 要以灵活的方式设置开发流程，您可能需要多个单独的开发和测试环境。 除了定义服务环境之外，还可以直接从 RCS 设置指向您的业务应用程序（如 Finance 或 Supply Chain Management）的链接，以设置电子开票正确操作所需的参数。 有关环境的详细信息，请参阅[服务环境](e-invoicing-service-environments.md)。

一切设置完成后，您可以创建自己的全球化功能，来定义处理电子单据和转换数据或从全局存储库导入文档的不同场景。 有关如何使用全球化功能的详细信息，请参阅[使用全球化功能](e-invoicing-working-globalization-features.md)。

如果您的场景需要与电子邮件或 SharePoint 集成来处理传入电子单据，请参阅[处理传入的电子单据](e-invoicing-process-incoming-electronic-documents.md)了解有关如何设置和使用这些渠道的信息。
