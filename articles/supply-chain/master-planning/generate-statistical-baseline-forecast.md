---
title: "生成统计基准预测"
description: "本文提供有关用于需求预测计算的参数和筛选器的信息。"
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 72683
ms.assetid: 42190463-2a64-4f63-b653-10cac3df0692
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 93646e37ee511d433097bb284fccc73c230aee32
ms.contentlocale: zh-cn
ms.lasthandoff: 06/13/2017

---

# <a name="generate-a-statistical-baseline-forecast"></a>生成统计基准预测

[!include[banner](../includes/banner.md)]


本文提供有关用于需求预测计算的参数和筛选器的信息。 

在您创建基准预测时，必须首先指定在计算中使用的参数和筛选器。 例如，您可以创建基于指定公司和所选物料组去年、下个月的交易数据来估计需求的基准预测。 

若要生成需求预测，转到**主计划 &gt; 预测 &gt; 需求预测 &gt; 生成统计基线预测**。 

预测时段可以在预测生成时选择。 可用值：天、周和月。 

要为其生成预测的时段的数目在**预测区间**字段中设置。 

在将预测策略设置为**复制历史需求**时，忽略历史区间的结束。 此系统将在**预测区间**字段中指定的时段的数量复制到预测需求，从在**历史区间**下的**开始日期**字段中设置的日期开始。 通过复制某一日期前推的历史需求，生产计划人员可以通过两种方式为下一个季度制定计划：

-   通过复制去年相同季度的需求。
-   通过复制上一个季度的需求。

为了避免生产计划的混淆，特定预测时段数目可以锁定。 此数目在字段**锁定时限**中设置。 在**调整后的需求预测**页上，锁定时段的单元格将禁用，以给予不应更改的那些值以直观显示。 

基准需求预测的开始日期不必为当前日期或未来日期。 若要设置不同的开始日期，请使用**基准预测开始日期 - 开始日期**字段。 例如，在六月，用户可以生成明年的预测。 由于历史需求的结束和基准的开始之间的预测时段缺少，预测可能不准确。 如果您使用 Microsoft Dynamics 365 for Finance and Operations 需求预测服务，您可以有四种方法填补缺失。 您可以通过在**需求预测参数**页上设置 MISSING\_VALUE\_SUBSTITUTION 参数来选择需要的方法。 

**基准预测开始日期**  -  **开始日期**字段必须设置为预测时段的开始，例如，在美国，如果预测时段是周则为星期日。 此系统自动调整**基准预测开始日期**  -  **开始日期**字段为与预测时段的开始匹配。 

**基准预测开始日期**  -  **开始日期**字段可以设置为过去的日期。 换言之，可以生成过去的需求预测。 这很有用，因为它允许用户调整预测服务参数，以便过去生成的统计预测与实际历史需求匹配。 用户然后可以继续使用这些参数设置来生成将来的统计基准预测。 

如果选中**转移对需求预测进行的手动调整**复选框，在以前需求预测迭代进行的手动调整可以自动应用于新的基准预测。 如果清除此复选框，手动调整不添加到基准预测 – 但它们不删除。 对预测进行的手动调整只能在预测导入时删除，方法是通过清除**保存对基准需求预测进行的手动调整**复选框。 手动调整在授权时保存。 因此，如果用户对预测进行手动调整，但不授权预测返回 Finance and Operations，则更改将丢失。 有关手动调整以及它们的工作方式的详细信息，请参阅[授权已调整的预测](authorize-adjusted-forecast.md)。 

需求预测生成可以有名称和注释以帮助用户确定已生成的预测。 这些值在**统计基准预测生成历史记录**页的预测生成历史记录中可见。 

内部公司计划组、物料分配参数和其他筛选器可以在预测生成时应用。 它们可用于提高绩效或将数据拆分为可管理的区块。 不过，请注意，需求预测没有为不与内部公司计划组关联的任何物料分配参数的成员生成，即使物料分配参数在查询中选择。 

**提示**：在某些情况下，在生成需求预测时，用户可能会收到错误消息，或预测生成在没有会话日志的情况下完成。 这可能由于之前用于预测生成的查询中的残余数据而发生。 为了修复此问题，单击**选择**打开**查询**页，单击**重置**，然后重新生成基准预测。 

如果没有为大物料组生成预测，但是，例如，一次为一个物料或一个物料分配参数生成，那么为了达到更好的效果，您可以选中**主计划 - 设置 - 需求预测**  -  **需求预测参数 - Azure 机器学习**选项卡上的**使用请求响应模式**复选框。

<a name="see-also"></a>请参阅
--------

[需求预测设置](demand-forecasting-setup.md)

[对基准预测进行手动调整](manual-adjustments-baseline-forecast.md)

[授权调整后的需求预测](authorize-adjusted-forecast.md)



