--- 
title: "使用模型映射配置在数据库级别执行聚合计算 (ER)"
description: "此过程提供有关如何设计新电子申报 (ER) 模型映射配置和使用内置 ER 执行有效聚合计算的信息。"
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 74606b1378e94e8a6945a408520c8b68648970d8
ms.openlocfilehash: 3c3558d9e25dcfd56f3306e69884528d01324cbd
ms.contentlocale: zh-cn
ms.lasthandoff: 02/07/2018

---
# <a name="use-a-model-mapping-configuration-for-aggregate-calculations-at-the-database-leveler"></a><span data-ttu-id="52e97-103">使用模型映射配置在数据库级别执行聚合计算 (ER)</span><span class="sxs-lookup"><span data-stu-id="52e97-103">Use a model mapping configuration for aggregate calculations at the database level(ER)</span></span> 

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="52e97-104">此过程提供有关如何设计新电子申报 (ER) 模型映射配置和使用内置 ER 执行有效聚合计算的信息。</span><span class="sxs-lookup"><span data-stu-id="52e97-104">This procedure provides information about how to design a new Electronic reporting (ER) model mapping configuration and use built-in ER functions for efficient aggregate calculations.</span></span> <span data-ttu-id="52e97-105">在此过程中，您将创建示例公司“Litware 公司”的配置。</span><span class="sxs-lookup"><span data-stu-id="52e97-105">In this procedure you will create a configuration for the sample company, Litware, Inc.</span></span> 

<span data-ttu-id="52e97-106">此过程是为向其分配了系统管理员角色或电子申报开发人员角色的用户创建的。</span><span class="sxs-lookup"><span data-stu-id="52e97-106">This procedure is created for users with the assigned role of System administrator or Electronic reporting developer.</span></span> <span data-ttu-id="52e97-107">可使用任何数据集完成这些步骤。</span><span class="sxs-lookup"><span data-stu-id="52e97-107">These steps can be completed using any dataset.</span></span>

 <span data-ttu-id="52e97-108">为了完成这些步骤，您必须首先完成“ER 通过在数据库级别执行聚合计算改进这些计算的效率（第 1 部分：准备配置）”这一过程中的步骤。</span><span class="sxs-lookup"><span data-stu-id="52e97-108">To complete these steps, you must first complete the steps in the procedure, “ER improves the efficiency of aggregate calculations by performing them on database level (Part 1: Prepare configurations).”</span></span>

1. <span data-ttu-id="52e97-109">转到“组织管理”>“电子申报”>“配置”。</span><span class="sxs-lookup"><span data-stu-id="52e97-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="52e97-110">在树中，展开“内部统计模型”。</span><span class="sxs-lookup"><span data-stu-id="52e97-110">In the tree, expand 'Intrastat model'.</span></span>
3. <span data-ttu-id="52e97-111">在树中，选择“内部统计模型\内部统计示例映射”。</span><span class="sxs-lookup"><span data-stu-id="52e97-111">In the tree, select 'Intrastat model\Intrastat sample mapping'.</span></span>
4. <span data-ttu-id="52e97-112">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="52e97-112">Click Designer.</span></span>
5. <span data-ttu-id="52e97-113">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="52e97-113">Click Designer.</span></span>
6. <span data-ttu-id="52e97-114">在树结构中，选择“Dynamics 365 for Operations\表格记录”。</span><span class="sxs-lookup"><span data-stu-id="52e97-114">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
7. <span data-ttu-id="52e97-115">单击“添加根”。</span><span class="sxs-lookup"><span data-stu-id="52e97-115">Click Add root.</span></span>
    * <span data-ttu-id="52e97-116">添加表示您要分组的记录的新数据源。</span><span class="sxs-lookup"><span data-stu-id="52e97-116">Add a new data source representing records you want to group.</span></span>  
8. <span data-ttu-id="52e97-117">在“名称”字段中，键入“交易记录”。</span><span class="sxs-lookup"><span data-stu-id="52e97-117">In the Name field, type 'Transactions'.</span></span>
    * <span data-ttu-id="52e97-118">交易</span><span class="sxs-lookup"><span data-stu-id="52e97-118">Transactions</span></span>  
9. <span data-ttu-id="52e97-119">在“表”字段中，键入“内部统计”。</span><span class="sxs-lookup"><span data-stu-id="52e97-119">In the Table field, type 'Intrastat'.</span></span>
    * <span data-ttu-id="52e97-120">内部统计</span><span class="sxs-lookup"><span data-stu-id="52e97-120">Intrastat</span></span>  
10. <span data-ttu-id="52e97-121">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="52e97-121">Click OK.</span></span>
11. <span data-ttu-id="52e97-122">在树结构中，选择“功能\分组依据”。</span><span class="sxs-lookup"><span data-stu-id="52e97-122">In the tree, select 'Functions\Group by'.</span></span>
    * <span data-ttu-id="52e97-123">此数据源类型用于在运行时引入新数据源以分组记录、计算所需的合并。</span><span class="sxs-lookup"><span data-stu-id="52e97-123">This data source type is used to introduce a new data source at run-time to group records and to calculate required aggregations.</span></span>  
12. <span data-ttu-id="52e97-124">单击“添加根”。</span><span class="sxs-lookup"><span data-stu-id="52e97-124">Click Add root.</span></span>
13. <span data-ttu-id="52e97-125">在“名称”字段中，键入“TransactionsGroups”。</span><span class="sxs-lookup"><span data-stu-id="52e97-125">In the Name field, type 'TransactionsGroups'.</span></span>
    * <span data-ttu-id="52e97-126">TransactionsGroups</span><span class="sxs-lookup"><span data-stu-id="52e97-126">TransactionsGroups</span></span>  
14. <span data-ttu-id="52e97-127">单击“编辑分组依据”。</span><span class="sxs-lookup"><span data-stu-id="52e97-127">Click Edit group by.</span></span>
15. <span data-ttu-id="52e97-128">在树结构中，选择“交易记录”。</span><span class="sxs-lookup"><span data-stu-id="52e97-128">In the tree, select 'Transactions'.</span></span>
    * <span data-ttu-id="52e97-129">选择表示您要分组的记录的“记录列表”类型的已添加数据源。</span><span class="sxs-lookup"><span data-stu-id="52e97-129">Select the added data source of the ‘Record list’ type that represents the records that you want to group.</span></span>  
16. <span data-ttu-id="52e97-130">单击“将字段添加到”。</span><span class="sxs-lookup"><span data-stu-id="52e97-130">Click Add field to.</span></span>
17. <span data-ttu-id="52e97-131">单击“什么要分组”。</span><span class="sxs-lookup"><span data-stu-id="52e97-131">Click What to group.</span></span>
18. <span data-ttu-id="52e97-132">在树结构中，展开“交易记录”。</span><span class="sxs-lookup"><span data-stu-id="52e97-132">In the tree, expand 'Transactions'.</span></span>
19. <span data-ttu-id="52e97-133">在树结构中，选择“交易记录\指令”。</span><span class="sxs-lookup"><span data-stu-id="52e97-133">In the tree, select 'Transactions\Direction'.</span></span>
20. <span data-ttu-id="52e97-134">单击“将字段添加到”。</span><span class="sxs-lookup"><span data-stu-id="52e97-134">Click Add field to.</span></span>
21. <span data-ttu-id="52e97-135">单击“分组字段”。</span><span class="sxs-lookup"><span data-stu-id="52e97-135">Click Grouped fields.</span></span>
    * <span data-ttu-id="52e97-136">选择字段以指定分组级别。</span><span class="sxs-lookup"><span data-stu-id="52e97-136">Select the field to specify the grouping level.</span></span> <span data-ttu-id="52e97-137">基于此选择，数据源将在运行时返回与将在内部统计表中达到的指令代码数量同样多的交易记录组。</span><span class="sxs-lookup"><span data-stu-id="52e97-137">Based on this selection, the data source will return at run-time as many groups of transactions as there are direction codes that will be met in the Intrastat table.</span></span>  
22. <span data-ttu-id="52e97-138">在树中，选择“Transactions\Invoice amount(AmountMST)”。</span><span class="sxs-lookup"><span data-stu-id="52e97-138">In the tree, select 'Transactions\Invoice amount(AmountMST)'.</span></span>
    * <span data-ttu-id="52e97-139">选择字段以指定合并计算的源。</span><span class="sxs-lookup"><span data-stu-id="52e97-139">Select the field to specify the source for aggregation calculation.</span></span>  
23. <span data-ttu-id="52e97-140">单击“将字段添加到”。</span><span class="sxs-lookup"><span data-stu-id="52e97-140">Click Add field to.</span></span>
24. <span data-ttu-id="52e97-141">单击“合并字段”。</span><span class="sxs-lookup"><span data-stu-id="52e97-141">Click Aggregation fields.</span></span>
25. <span data-ttu-id="52e97-142">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="52e97-142">In the list, mark the selected row.</span></span>
26. <span data-ttu-id="52e97-143">在“方法”字段中选择“求和”。</span><span class="sxs-lookup"><span data-stu-id="52e97-143">In the Method field, select 'Sum'.</span></span>
    * <span data-ttu-id="52e97-144">选择合并类型。</span><span class="sxs-lookup"><span data-stu-id="52e97-144">Select the aggregation type.</span></span>  
27. <span data-ttu-id="52e97-145">在“名称”字段中键入“SumOfAmountMST”。</span><span class="sxs-lookup"><span data-stu-id="52e97-145">In the Name field, type 'SumOfAmountMST'.</span></span>
    * <span data-ttu-id="52e97-146">在配置的数据源中指定此合并的名称。</span><span class="sxs-lookup"><span data-stu-id="52e97-146">Specify the name of this aggregation in the configured data source.</span></span>  
28. <span data-ttu-id="52e97-147">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="52e97-147">Click Save.</span></span>
    * <span data-ttu-id="52e97-148">请注意，“执行位置”字段指示此分组将在运行时在 SQL 数据库中执行。</span><span class="sxs-lookup"><span data-stu-id="52e97-148">Note that the ‘Execution at’ field indicates that this grouping will be performed at run-time in the SQL database.</span></span>  
29. <span data-ttu-id="52e97-149">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="52e97-149">Close the page.</span></span>
30. <span data-ttu-id="52e97-150">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="52e97-150">Click OK.</span></span>
31. <span data-ttu-id="52e97-151">在树中，展开“合计”。</span><span class="sxs-lookup"><span data-stu-id="52e97-151">In the tree, expand 'Totals'.</span></span>
32. <span data-ttu-id="52e97-152">在树中，展开“TransactionsGroups”。</span><span class="sxs-lookup"><span data-stu-id="52e97-152">In the tree, expand 'TransactionsGroups'.</span></span>
33. <span data-ttu-id="52e97-153">在树结构中，展开“TransactionsGroups\aggregated”。</span><span class="sxs-lookup"><span data-stu-id="52e97-153">In the tree, expand 'TransactionsGroups\aggregated'.</span></span>
34. <span data-ttu-id="52e97-154">在树中，选择“TransactionsGroups\aggregated\SumOfAmountMST”。</span><span class="sxs-lookup"><span data-stu-id="52e97-154">In the tree, select 'TransactionsGroups\aggregated\SumOfAmountMST'.</span></span>
35. <span data-ttu-id="52e97-155">在树中，选择“Totals\Total invoice value(TotalInvoiceValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$AmountMSTRounded')”。</span><span class="sxs-lookup"><span data-stu-id="52e97-155">In the tree, select 'Totals\Total invoice value(TotalInvoiceValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$AmountMSTRounded')'.</span></span>
36. <span data-ttu-id="52e97-156">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="52e97-156">Click Bind.</span></span>
    * <span data-ttu-id="52e97-157">基于此设置，此数据源将计算每个交易记录组的“AmountMST”字段值的总和。</span><span class="sxs-lookup"><span data-stu-id="52e97-157">Based on this setting, this data source will calculate the sum of values of the ‘AmountMST’ field for each groups of transactions.</span></span> <span data-ttu-id="52e97-158">此合并计算可作为 TransactionsGroups.aggregated.TotalAmount 项目提供。</span><span class="sxs-lookup"><span data-stu-id="52e97-158">This aggregation calculation will be available as TransactionsGroups.aggregated.TotalAmount item.</span></span>  
37. <span data-ttu-id="52e97-159">在树中，展开“TransactionsGroups”。</span><span class="sxs-lookup"><span data-stu-id="52e97-159">In the tree, expand 'TransactionsGroups'.</span></span>
38. <span data-ttu-id="52e97-160">在树中，选择“TransactionsGroups”。</span><span class="sxs-lookup"><span data-stu-id="52e97-160">In the tree, select 'TransactionsGroups'.</span></span>
39. <span data-ttu-id="52e97-161">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="52e97-161">Click Edit.</span></span>
40. <span data-ttu-id="52e97-162">单击“编辑分组依据”。</span><span class="sxs-lookup"><span data-stu-id="52e97-162">Click Edit group by.</span></span>
41. <span data-ttu-id="52e97-163">在树结构中，展开“交易记录”。</span><span class="sxs-lookup"><span data-stu-id="52e97-163">In the tree, expand 'Transactions'.</span></span>
42. <span data-ttu-id="52e97-164">在树中，选择“Transactions\Invoice amount(AmountMST)”。</span><span class="sxs-lookup"><span data-stu-id="52e97-164">In the tree, select 'Transactions\Invoice amount(AmountMST)'.</span></span>
43. <span data-ttu-id="52e97-165">单击“将字段添加到”。</span><span class="sxs-lookup"><span data-stu-id="52e97-165">Click Add field to.</span></span>
44. <span data-ttu-id="52e97-166">单击“合并字段”。</span><span class="sxs-lookup"><span data-stu-id="52e97-166">Click Aggregation fields.</span></span>
45. <span data-ttu-id="52e97-167">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="52e97-167">In the list, mark the selected row.</span></span>
46. <span data-ttu-id="52e97-168">在“方法”字段中选择“最大值”。</span><span class="sxs-lookup"><span data-stu-id="52e97-168">In the Method field, select 'Max'.</span></span>
47. <span data-ttu-id="52e97-169">在“名称”字段中键入“MaxOfAmountMST”。</span><span class="sxs-lookup"><span data-stu-id="52e97-169">In the Name field, type 'MaxOfAmountMST'.</span></span>
48. <span data-ttu-id="52e97-170">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="52e97-170">Click Save.</span></span>
    * <span data-ttu-id="52e97-171">目前，GROUPBY 数据源的执行可以转换到具有某些限制的 SQL 数据库级别。</span><span class="sxs-lookup"><span data-stu-id="52e97-171">Currently, the execution of GROUPBY data sources can be translated to the SQL database level with some limitations.</span></span> <span data-ttu-id="52e97-172">转换可用于“记录列表”类型的数据源或表示为使用 FILTER 函数的表达式的数据源。</span><span class="sxs-lookup"><span data-stu-id="52e97-172">Translation can be done for either data sources of the ‘Record list’ type or data sources represented as an expression using the FILTER function.</span></span> <span data-ttu-id="52e97-173">当为单个分组记录字段只配置了一个合并时，也可以执行。</span><span class="sxs-lookup"><span data-stu-id="52e97-173">It can also be done when the only one aggregation is configured for a single field of the grouping records.</span></span>  
    * <span data-ttu-id="52e97-174">请注意，即使为 AmountMST 字段配置了多个合并，“执行位置”字段仍然指示此分组在运行时在 SQL 数据库中执行。</span><span class="sxs-lookup"><span data-stu-id="52e97-174">Note that even though more than one aggregation was configured for the AmountMST field, the ‘Execution at’ field still indicates that this grouping will be performed at run-time in the SQL database.</span></span> <span data-ttu-id="52e97-175">这是因为只有一个合并绑定到数据模型项目，并用于在运行时从此数据源拉取数据。</span><span class="sxs-lookup"><span data-stu-id="52e97-175">This is because only one aggregation is bound to the data model item and will be used at run-time to pull data from this data source.</span></span>  
49. <span data-ttu-id="52e97-176">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="52e97-176">Close the page.</span></span>
50. <span data-ttu-id="52e97-177">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="52e97-177">Click OK.</span></span>
51. <span data-ttu-id="52e97-178">在树中，展开“TransactionsGroups”。</span><span class="sxs-lookup"><span data-stu-id="52e97-178">In the tree, expand 'TransactionsGroups'.</span></span>
52. <span data-ttu-id="52e97-179">在树结构中，展开“TransactionsGroups\aggregated”。</span><span class="sxs-lookup"><span data-stu-id="52e97-179">In the tree, expand 'TransactionsGroups\aggregated'.</span></span>
53. <span data-ttu-id="52e97-180">在树中，选择“TransactionsGroups\aggregated\MaxOfAmountMST”。</span><span class="sxs-lookup"><span data-stu-id="52e97-180">In the tree, select 'TransactionsGroups\aggregated\MaxOfAmountMST'.</span></span>
54. <span data-ttu-id="52e97-181">在树中，选择“Totals\Total statistical value(TotalStatisticalValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$StatisticalValueRounded')”。</span><span class="sxs-lookup"><span data-stu-id="52e97-181">In the tree, select 'Totals\Total statistical value(TotalStatisticalValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$StatisticalValueRounded')'.</span></span>
55. <span data-ttu-id="52e97-182">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="52e97-182">Click Bind.</span></span>
56. <span data-ttu-id="52e97-183">在树中，展开“TransactionsGroups”。</span><span class="sxs-lookup"><span data-stu-id="52e97-183">In the tree, expand 'TransactionsGroups'.</span></span>
57. <span data-ttu-id="52e97-184">在树中，选择“TransactionsGroups”。</span><span class="sxs-lookup"><span data-stu-id="52e97-184">In the tree, select 'TransactionsGroups'.</span></span>
58. <span data-ttu-id="52e97-185">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="52e97-185">Click Edit.</span></span>
59. <span data-ttu-id="52e97-186">单击“编辑分组依据”。</span><span class="sxs-lookup"><span data-stu-id="52e97-186">Click Edit group by.</span></span>
    * <span data-ttu-id="52e97-187">请注意，“执行位置”字段指示此分组将在运行时在内存中执行，因为同一个字段的两个合并均绑定到数据模型项目。</span><span class="sxs-lookup"><span data-stu-id="52e97-187">Note that the ‘Execution at’ field indicates that this grouping will be performed at run-time in memory because both aggregations of the same field are bound to the data model items.</span></span>   
60. <span data-ttu-id="52e97-188">在列表中，标记或取消标记所有行。</span><span class="sxs-lookup"><span data-stu-id="52e97-188">In the list, mark or unmark all rows.</span></span>
61. <span data-ttu-id="52e97-189">单击“删除”。</span><span class="sxs-lookup"><span data-stu-id="52e97-189">Click Delete.</span></span>
62. <span data-ttu-id="52e97-190">单击“是”。</span><span class="sxs-lookup"><span data-stu-id="52e97-190">Click Yes.</span></span>
63. <span data-ttu-id="52e97-191">单击“删除”。</span><span class="sxs-lookup"><span data-stu-id="52e97-191">Click Delete.</span></span>
64. <span data-ttu-id="52e97-192">单击“是”。</span><span class="sxs-lookup"><span data-stu-id="52e97-192">Click Yes.</span></span>
65. <span data-ttu-id="52e97-193">单击“将字段添加到”。</span><span class="sxs-lookup"><span data-stu-id="52e97-193">Click Add field to.</span></span>
66. <span data-ttu-id="52e97-194">单击“什么要分组”。</span><span class="sxs-lookup"><span data-stu-id="52e97-194">Click What to group.</span></span>
67. <span data-ttu-id="52e97-195">在树中，展开“Commodity record(Intrastat)”。</span><span class="sxs-lookup"><span data-stu-id="52e97-195">In the tree, expand 'Commodity record(Intrastat)'.</span></span>
68. <span data-ttu-id="52e97-196">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="52e97-196">Click Save.</span></span>
    * <span data-ttu-id="52e97-197">请注意，“执行位置”字段指示此分组将在运行时在内存中执行，即使未定义合并，且所选的“表记录”类型的数据源引用同一个“内部统计”表。</span><span class="sxs-lookup"><span data-stu-id="52e97-197">Note that the ‘Execution at’ field indicates that this grouping will be performed at run-time in memory even though there are no aggregations defined and the selected data source of ‘Table records’ type refers to the same ‘Intrastat’ table.</span></span> <span data-ttu-id="52e97-198">原因在于数据源包含一些不能转换为 SQL 数据库级别的已计算字段。</span><span class="sxs-lookup"><span data-stu-id="52e97-198">This is because the data source contains some calculated fields which can’t yet be translated to the SQL database level.</span></span>  

