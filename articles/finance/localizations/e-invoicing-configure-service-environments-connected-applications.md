---
title: 配置服务环境和已连接的应用程序
description: 本文提供有关如何配置您的服务环境和已连接应用程序的信息。
author: dkalyuzh
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: c1bb3f784148f04c01223ac4e280a18bacfe0e51
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853213"
---
# <a name="configure-service-environments-and-connected-applications"></a>配置服务环境和已连接的应用程序

[!include [banner](../includes/banner.md)]

本文提供有关如何配置您的服务环境和已连接应用程序的信息。 此过程有三个步骤。 步骤 1 是必需的，步骤 2 和 3 是可选的。

## <a name="step-1-create-a-service-environment"></a>步骤 1：创建服务环境

创建服务环境时，定义可以向其部署全球化功能的用户列表。 或者，对于某些场景，定义可以与电子开票服务通信的外部应用程序列表。 如果您将在场景中使用编号规则，请进行设置。

要完成此步骤，请参阅[服务环境](e-invoicing-service-environments.md)。

## <a name="step-2-add-certificates-and-secrets"></a>步骤 2：添加证书和机密

添加对 Microsoft Azure 密钥保管库和机密的引用以在您的场景中使用。 如果处理管道中的操作使用证书和机密进行数字签名或与外部 Web 服务通信，此步骤则是必需的。

要完成此步骤，请参阅[客户证书和机密](e-invoicing-customer-certificates-secrets.md)。

## <a name="step-3-configure-connected-applications"></a>步骤 3：配置连接的应用程序

要在 Dynamics 365 Finance 或 Dynamics 365 Supply Chain Management 应用程序与电子开票之间建立通信，您必须配置 Finance 或 Supply Chain Management 以构建对电子开票服务的调用，并以可以转换为所需电子格式的统一结构准备业务数据。 应用程序还必须正确处理来自服务的响应。 您可以直接在 Finance 或 Supply Chain Management 环境中完成此配置，也可以在 Regulatory Configuration Service (RCS) 中完成。 如果您在 RCS 中完成配置，可以将其部署到您的 Finance 或 Supply Chain Management 环境中。 在此步骤中，您将注册连接的应用程序以进行参数部署。

要完成此步骤，请参阅[已连接的应用程序](e-invoicing-connected-applications.md)。
