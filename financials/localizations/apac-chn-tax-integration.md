---
title: "配置中国的税务集成"
description: "本主题描述配置中国的税务集成的流程。"
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 265264
ms.assetid: e5dbbbe1-935f-4fb4-a014-447916051628
ms.search.region: China (PRC)
ms.author: leguo
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f7fd20ef0c78bc781f0ef9f17fc612723906ac78
ms.openlocfilehash: 7ed3f6af765ed26dc1d7b0b0208eb6038df6aacf
ms.lasthandoff: 03/31/2017


---

# <a name="configure-tax-integration-for-china"></a>配置中国的税务集成

[!include[banner](../includes/banner.md)]


本主题描述配置中国的税务集成的流程。

若要配置中国的税务集成，请完成以下任务。

1.  在**增值税发票描述**页中新建一个增值税发票描述。 例如，可能需要设置以下参数：
    -   将**增值税发票描述 ID** 设置为 InvoiceDescID01
    -   将**描述**设置为“详见销售清单”
    -   将**单位**设置为“箱子”

2.  在**税务集成模板**页中创建一个新税务集成模板。 可以设置导入或导出发票时使用的税务集成模板。 在税务集成模板中，可以指定以下信息：
    -   增值税代码
    -   最大发票金额
    -   金税发票的默认描述和单位
    -   是否包含普通增值税发票

下图是税务集成流程的示例。
[![IC666469](./media/ic666469.gif)](./media/ic666469.gif)

<a name="see-also"></a>请参阅
--------

[导入中国金税数据实体](apac-chn-import-golden-tax-data-entity.md)

[增值税客户发票的中国税务集成修改常见问题](apac-chn-tax-integration-vat-customer-invoices.md)



