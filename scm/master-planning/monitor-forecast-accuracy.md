---
title: "监控预测准确性"
description: "本文介绍 Microsoft Dynamics 365 for Operations 计算的预测准确性的类型，并说明如何可以查看准确性值。"
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: d3f88a4fa54217cea909c54955de05e2175db0cd
ms.lasthandoff: 03/29/2017


---

# <a name="monitor-forecast-accuracy"></a>监控预测准确性

[!include[banner](../includes/banner.md)]


本文介绍 Microsoft Dynamics 365 for Operations 计算的预测准确性的类型，并说明如何可以查看准确性值。

Dynamics 365 for Operations 计算以下类型的预测准确性：

-   历史预测准确性，通过比较主计划使用的历史预测和历史需求。 若要查看历史预测准确性的值（绝对值和百分比值），请单击**需求预测详细信息**页的**显示准确性**。
-   用于生成预测的预测模型的估计精确性。 您可以在**需求预测详细信息**页的**模型详细信息 - MAPE** 下查看准确率百分比。 

**注意：**如果您使用 Dynamics 365 for Operations 需求预测 Microsoft Azure 机器学习服务，内部模型准确性的计算基于测试数据集。 若要指定测试数据集的规模，请在**需求预测参数**页上设置参数 **TEST\_SET\_SIZE\_PERCENT**。 例如，如果您将该值设置为 **20**，历史数据的最后 20% 将用于计算内部模型准确性。


<a name="see-also"></a>请参阅
--------

[授权调整后的需求预测](authorize-adjusted-forecast.md)

[在计算需求预测时，需从历史交易记录数据中删除离群值](remove-historical-outliers-calculating-demand-forecast.md)



