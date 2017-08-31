--- 
title: "设置最小-最大补货流程"
description: "此过程显示设置使用最小/最大补货战略的新补货流程。"
author: perlynne
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 01a0c42c43a23234e0e355193f8dd7e8ee116f71
ms.contentlocale: zh-cn
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-a-min-max-replenishment-process"></a>设置最小-最大补货流程

[!include[task guide banner](../../includes/task-guide-banner.md)]

此过程显示设置使用最小/最大补货战略的新补货流程。 在库存低于最低水平时，将创建工作以在此位置补货。 过程还显示如何使用固定领料位置以允许补货，即使库存低于最低水平，以及如何使用批处理作业使补货流程定期运行。 这些任务通常由仓库管理员完成。 您可以使用注释中的示例值在 USMF 演示数据公司中运行此过程，或可以对您自己的数据运行它。 如果您使用自己的数据，请确保您有为仓库管理流程启用的仓库。


## <a name="create-a-fixed-picking-location"></a>创建固定领料库位
1. 转到“仓库管理”>“设置”>“仓库”>“固定货位”。
    * 这是最小-最大补货的可选任务，但是，如果您使用固定领料库位，这允许对存货进行补货，即使低于最低水平，因为系统可以确定哪些物料需要补货，即使没有任何剩余。  
2. 单击“新建”。
3. 在“物料编号”字段中，输入或选择一个值。
    * 如果您正在使用 USMF，可以选择物料 A0001。  
4. 在“站点”字段中，输入或选择一个值。
    * 如果您使用 USMF，您可以选择站点 2。  
5. 在“仓库”字段中，输入或选择一个值。
    * 如果您使用 USMF，您可以选择仓库 24。  
6. 在“位置”字段中，输入或选择一个值。
    * 如果您使用 USMF，您可以选择 CP-003。  
7. 关闭该页面。

## <a name="create-a-replenishment-location-directive"></a>创建补货位置指令
1. 转到“库存管理”>“设置”>“位置指令”。
    * 库位指令用于确定在补货流程中应从哪里领料。  
2. 在“工作订单类型”字段中，选择“补货”。
3. 单击“新建”。
4. 在“名称”字段中，键入一个值。
5. 在“工作类型”字段中，选择“领料”。
6. 在“站点”字段中，输入或选择一个值。
    * 如果您使用 USMF，您可以选择站点 2。  
7. 在“仓库”字段中，输入或选择一个值。
    * 如果您使用 USMF，您可以选择仓库 24。  
8. 单击“保存”。
9. 单击“新建”。
10. 在列表中，标记所选的行。
11. 在“截止数量”字段中，输入一个数字。
    * 例如，您可以将其设置为 9999。  
12. 选中“允许拆分”复选框。
    * 如果您选择此选项，工作创建流程将允许工作行数量跨多个位置分解。  
13. 单击“保存”。
14. 单击“新建”。
15. 在列表中，标记所选的行。
16. 在“名称”字段中，键入一个值。
17. 单击“保存”。
18. 单击“编辑查询”。
    * 您可以编辑此查询来添加限制，限制在补货流程中可以从哪里选择库存。 例如，可以是仓库应只从仓库的堆放区使用。  
19. 单击“确定”。
20. 关闭该页面。

## <a name="create-a-replenishment-work-template"></a>创建补货工作模板
1. 转到“仓库管理”>“设置”>“工作”>“工作模板”。
    * 工作模板用于指导系统必须如何创建最小/最大补货工作。 至少，必须具有用于领料和放置的工作模板行。 工作模板将显示无效，直到所有必要信息全部填充。  
2. 在“工作订单类型”字段中，选择“补货”。
3. 单击“新建”。
4. 在“工作模板”字段中，键入一个值。
5. 单击“保存”。
6. 单击“新建”。
7. 在“工作类型”字段中，选择“领料”。
8. 在“工作类 ID”字段中，输入或选择一个值。
    * 这应是与补货相关的工作类。 如果您正在使用 USMF，则选择“补货”。  
9. 单击“新建”。
10. 在列表中，标记所选的行。
11. 在“工作类型”字段中，选择“放置”。
12. 在“工作类 ID”字段中，输入或选择一个值。
13. 单击“保存”。
14. 关闭该页面。

## <a name="create-a-new-replenishment-template"></a>创建新的补货模板
1. 转到“仓库管理”>“设置”>“补货”>“补货模板”。
    * 补货模板用于定义物料和数量以及补货位置。  
2. 单击“新建”。
3. 在“补货模板”字段中，键入一个值。
    * 为模板指定一个名称以指示它是用于最小/最大补货。  
4. 在“描述”字段中，键入一个值。
5. 选择“允许波次需求使用未预留的数量”复选框。
    * 如果选择此选项，将支持波次需求补货消耗与最小/最大补货相关的数量。 例如，如果最小/最大补货工作不立即处理，为了避免创建不必要的需求补货工作，这可能很有用。  
6. 单击“新建”。
7. 在“序列号”字段中，输入一个数字。
8. 在“描述”字段中，键入一个值。
9. 在列表中，标记所选的行。
10. 在“补货单位”字段中，输入或选择一个值。
    * 例如，选择 pcs。 此设置是强制的。 它允许您对比在此模板中为最小和最大库存水平指定的单位，指定补货工作的不同度量单位。  
11. 在“工作模板”字段中，输入或选择一个值。
    * 选择您之前创建的工作模板。  
12. 在“最小数量”字段中，输入一个数字。
    * 选择应触发补货的最小数量。 例如，设置此数量为 50。 如果您在固定位置补货，且“仅对空的固定货位补货”选项设置为“是”，可以将此设置保留为零。 我们还建议您出于绩效原因选择“仅对固定货位补货”选项。  
13. 在“最大数量”字段中，输入一个数字。
    * 例如，则此设置为 100。  
14. 在“单位”字段中，输入或选择一个值。
    * 为最小和最大数量分配单位。 例如，设置此数量为 pcs。  
15. 选择“仅对空的固定货位补货”复选框。
    * 选择此复选框以对固定位置为空时补货。 否则，只有具有现有数量的位置进行补货。  
16. 选择“仅对固定货位补货”复选框。
17. 单击“选择产品”。
    * 这是定义应补货哪些产品的位置。 如果选择“固定领料位置”选项，还需要在此查询中定义位置。 变型特定查询可用，产品特定查询也可用。  
18. 选择“物料行”。
19. 在“标准”字段中，输入一个值。
    * 选择应在固定位置补货的物料。 例如，键入 A* 可以选择所有以 A 开头的物料编号。  
20. 单击“添加”。
    * 添加位置实体（除非已经存在）可以将补货工作限制到特定仓库区域内的固定领料库位。  
21. 在列表中，标记所选的行。
22. 将“表”字段设置为“位置”。
23. 在“字段”字段中，选择“位置模板 ID”。
24. 在“标准”字段中，输入或选择一个值。
25. 单击“确定”。
26. 关闭该页面。

## <a name="set-the-replenishment-process-to-run-as-a-batch-job"></a>设置补货流程以将其作为批处理作业运行
1. 转到“仓库管理”>“补货”>“补货”。
    * 补货页允许您设置补货作为批处理作业运行，或者要求手动开始。  
2. 单击“筛选器”。
3. 在列表中，标记所选的行。
4. 在“标准”字段中，输入或选择一个值。
5. 单击“确定”。
6. 展开“后台运行”部分。
7. 设置“批处理”选项为“是”。
8. 单击“重复执行”。
9. 选择“无结束日期”选项。
10. 设置重复执行模式。
    * 例如，选择“天”。  
11. 单击“确定”。
12. 单击“确定”。

