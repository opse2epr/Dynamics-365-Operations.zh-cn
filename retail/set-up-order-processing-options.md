---
title: "设置订单处理选项"
description: "本主题提供有关如何使用 Microsoft Dynamics 365 for Operations - Retai 来处理呼叫中心的订单的信息。"
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 78973
ms.assetid: 09fca083-ac0d-4f30-baf2-bb00a626be12
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: eb62073fdfa50576d2c613594f3d85cbc0b322f6
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-order-processing-options"></a>设置订单处理选项

[!include[banner](includes/banner.md)]


本主题提供有关如何使用 Microsoft Dynamics 365 for Operations - Retai 来处理呼叫中心的订单的信息。 

Dynamics 365 for Operations 中的零售和商业支持多个零售渠道，如在线商店、实体商店和呼叫中心。 在呼叫中心中，工作人员通过电话从客户那儿接单并创建销售订单。 此主题描述了如何创建呼叫中心和配置呼叫中心选项。 每个呼叫中心可以拥有自己的用户、付款方式、价格组、财务维度和交货方式。 当您创建呼叫中心时，可以配置这些选项。 **重要说明：**在当前 Dynamics AX 用户创建销售订单时，必须先将用户作为呼叫中心用户分配给呼叫中心，然后才能使用呼叫中心工作流。 您可以使用**“呼叫中心”**页来启用或禁用对呼叫中心唯一的功能组。 可启用以下功能组：

-   **订单完成** - 此组包括与**“销售订单”**页上的付款和订单完成相关的功能。
-   **直接销售** - 此组包括与源代码、脚本和目录请求相关的功能。

在呼叫中心设置中启用这些功能后，与呼叫中心关联的用户便可在**“销售订单”**页上使用它们。 在可以使用这些功能之前，大多数功能都需要进行其他设置。 将图像和脚本作为特定呼叫中心的直接销售设置的一部分启用。 如果启用这些功能，则将在**“销售订单”**页的“速见表”窗格中显示脚本和产品图像。 显示为产品设置的默认图像。 可在目录的上下文中配置物料、目录或客户的脚本。 呼叫中心订单会显示有关特定订单行的价格的派生方式的其他详细信息。 例如，此类订单显示已应用的折扣。 您在**应收帐款** &gt; **设置** &gt; **应收帐款参数** &gt; **价格** &gt; **价格详细信息**中启用此功能。 您可以从**“销售订单行”**下拉列表中访问**“价格详细信息”**页。 您可使用用于实施审计的订单事件跟踪，来查看在订单生命周期中对订单执行的操作或跟踪特定用户的操作。 例如，您可记录每次用户创建销售订单时的操作、暂停订单、覆盖费用或更新订单行。 您可设置订单事件以跟踪特定期间内针对特定用户、用户组或所有用户的操作。 您可以通过从某个文档的页面上的操作窗格打开**“订单事件”**页来查看对该文档执行的操作。 您可以在**销售和市场营销** &gt; **设置** &gt; **事件** &gt; **订单事件**中配置订单事件。 当客户的订单无法准时交货时，公司可以自动向客户发送通知电子邮件，解释订单状态并向客户提供取消该订单的机会。 如果延期超过指定阈值，订单会自动取消。 可以按指定的时间间隔发送最多三封电子邮件：

1.  **第一个取消通知** – 客户可以取消订单。
2.  **第二个取消通知** – 客户可以取消订单。
3.  **最终取消通知** – 系统取消订单并通知客户已取消。

您可以不将自动通知和取消过程告知客户和产品。 当您向订单中添加一个物料时将触发毛利率预警。 预警包含有关物料的重要信息，例如，价格毛利和物料获利度。 您可以使用此信息决定当您向销售订单中添加一个物料时价格撤消是否合理。 例如，您可以设置贸易利润的阈值来指定高于某个物料的成本 40% 或更多的阈值是可接受的，而高于成本 20% 至 39% 的阈值是有问题的。 在此情况下，任何具有 20% 至 39% 的阈值的物料将触发警告。 任何具有高于成本不到 20% 的阈值的物料无法销售，并且无法调整物料价格。 您可以在**应收帐款** &gt; **设置** &gt; **应收帐款参数** &gt; **利润预警**中配置利润预警。 在您设置基于默认规则时的销售税分配时，可以确定地址要素的匹配优先顺序。 例如，您可以指定按邮政编码匹配销售税组优先于按州匹配销售税组。 在您输入新的客户地址记录时，将基于客户的地址如何与默认规则和您定义的优先顺序匹配自动分配销售税组。 您可以在**“总帐参数”**页上配置此功能。



