---
title: "托运"
description: "本主题介绍如何使用入站托运库存流程。"
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ConsignmentDraftReplenishmentOrderJournal, ConsignmentProductReceiptLines, ConsignmentReplenishmentOrder, ConsignmentVendorPortalOnHand, InventJournalOwnershipChange, InventOnHandItemListPage, PurchTable, PurchVendorPortalConfirmedOrders
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 220834
ms.assetid: 3c9d6de4-45d4-459a-aef7-0d9ad2c22b3a
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: d9dcdd63649d6dbff96efe2eec7cad34025ab2ee
ms.lasthandoff: 03/31/2017


---

# <a name="consignment"></a>托运

[!include[banner](../includes/banner.md)]


本主题介绍如何使用入站托运库存流程。

托运库存是由供应商所拥有，但存储在您的站点的库存。 在您准备好消耗或使用库存时，您接过库存的所有权。 本主题包括关于如何在不创建总帐交易记录的情况下实际接收供应商拥有的现有库存，如何开始可以实际预留供应商拥有的库存的生产流程。 以及如何更改原材料所有权以便能够在生产订单处理中处理消耗量的信息。 还提供了关于供应商如何使用供应商协作界面监控库存消耗量的一些信息。 有关如何启用和配置入站托运流程的信息，请参阅“[设置托运](set-up-consignment.md)”。

## <a name="overview-of-the-consignment-process"></a>托运流程概述
在此示例场景中，公司 USMF 与供应商 US-104 订立了关于原材料 M9211CI 的托运协议。

1.  USMF 中的某个人员基于预期需求量手动创建托运补货订单。 为供应商 US-104 创建订单，并且为物料 MS9211CI 添加行。
2.  供应商获得关于预期交货的信息。 这可以通过以下三种方式中的其中一种进行：
    -   USMF 中的某个工作人员向供应商发送订单信息。
    -   供应商可以使用供应商协作界面监控预期现有库存。
    -   USMF 的某个工作人员筛选“**现有库存**”页面上的数据，以仅显示收货状态为“**已订购**”的供应商 US-104 的记录，然后将此信息发送给供应商。

3.  库存从 US-104 传递到 USMF。
4.  在物料到达 USMF 后，使用物料收货更新托运补货订单。 仅记录供应商拥有的库存的实际数量。 为创建总帐交易记录，因为库存仍然归供应商所有。
5.  供应商使用“**现有托运库存**”页面监控实际现有库存。
6.  现在实际库存为现有量，生产流程预留供应商拥有的库存，开始要消耗原材料 M9211CI 的成品的生产订单。
7.  在今天的生产中要消耗的预留的原材料的所有者从 US-104 更改为 USMF。 这通过库存所有权更改日记帐完成。 此流程创建采购订单，其中“**来源**”字段设置为“**托运**”。
8.  供应商在“**从托运库存接收的产品**”页面上监控消耗量（所有权变更），并且基于两家公司间的协议开具发票。
9.  生产流程通过生产领料单消耗原材料。 实际预留自动更新，以反映现有库存量归 USMF 所有。
10. 来自 US-104 的发票对照处理库存所有权更改日记帐时自动生成的采购订单进行处理。 对消耗的库存向供应商 US-104 付款。

USMF 执行其他定期流程：

-   使用转移日记帐处理供应商拥有的库存在不同仓库之间的物理移动。
-   使用“**物料盘点**”日记帐更新实际库存现有量。 如果供应商有权限这样做，供应商也可以使用盘点更新现有库存量。

供应商 US-104 可以通过“**现有托运库存**”页面监控更新。

## <a name="consignment-replenishment-orders"></a>托运补货订单
托运补货订单是通过记录已订购的库存交易记录请求和跟踪记录供应商计划在特定的日期间隔内交货的产品库存量的文档。 通常，这基于特定产品的预测和实际需求。 要对照托运补货订单收货的库存仍然归供应商所有。 仅记录与实际收货有关的产品拥有更新，因此不会发生总帐交易记录更新。 “**所有者**”维度用于分隔与供应商拥有的库存有关和与接收法人拥有的库存有关的信息。 托运补货订单行只要是行未接收或取消全部数量，便具有**未结订单**的状态。 已接收或取消全部数量后，状态更改为**已完成**。 可以使用登记流程和收货更新流程记录与托运补货订单有关的实际现有库存量。 登记可作为物料到达流程的一部分或通过手动更新订单行完成。 使用收货更新流程时，在收货日记帐中进行记录，可用来向供应商确认收货。 

[![托运补货订单](./media/consignment-replenishment-order.png)](./media/consignment-replenishment-order.png)

## <a name="inventory-ownership-change-journal"></a>库存所有权更改日记帐
将库存所有者从供应商更改为接收法人的流程通过库存所有者更改日记帐完成。 不会对日记帐创建任何预期库存交易记录。 仅创建与过帐的日记帐有关的库存交易记录。 过帐日记帐时：

-   使用具有“**已售出**”状态的“**所有权更改**”引用发放供应商拥有的库存。
-   消耗物料的法人使用通过采购订单物料收据更新的库存交易接收现有库存量。 这将订单的状态设置为“**已接收**”。 用于托运的采购订单的“**来源**”字段设置为“**托运**”。

不可能在创建订单后在托运采购订单行上更新数量。 

[![库存所有权更改日记帐](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)

## <a name="vendor-collaboration-in-consignment-processes"></a>托运流程中的供应商协作
供应商协作界面有三页与入站托运流程有关：

-   **销售托运库存**的**采购订单** - 显示与托运流程中的所有权更改有关的详细的采购订单信息。
-   **从托运库存接收的产品** - 显示在所有权更改流程中进行物料收货更新的物料和数量信息。
-   **现有托运库存** - 显示预期交货及在客户站点已经实际可用的托运物料的信息。




