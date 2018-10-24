---
title: "根据工作时数累积休假时间"
description: "此主题介绍如何配置休假计划以便基于工作时数累积休假时间。"
author: Jcart1106
manager: AnnBe
ms.date: 09/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2018-09-17
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: 1aae5797e37b846a38f957b02870e213da528a2d
ms.openlocfilehash: f6489b84c71f2ac5a492b2d19cf087a05de8a599
ms.contentlocale: zh-cn
ms.lasthandoff: 09/20/2018

---

# <a name="accrue-time-off-based-on-hours-worked"></a><span data-ttu-id="4392e-103">根据工作时数累积休假时间</span><span class="sxs-lookup"><span data-stu-id="4392e-103">Accrue time off based on hours worked</span></span>

[!include [banner](includes/banner.md)]


## <a name="overview"></a><span data-ttu-id="4392e-104">概览</span><span class="sxs-lookup"><span data-stu-id="4392e-104">Overview</span></span>

<span data-ttu-id="4392e-105">聘用小时员工的组织可根据工作时数奖励休假，而不是根据在职年限。</span><span class="sxs-lookup"><span data-stu-id="4392e-105">Organizations with hourly employees can award time off based on hours worked instead of tenure with the organization.</span></span> <span data-ttu-id="4392e-106">工作时数数据通常存储在考勤管理系统中。</span><span class="sxs-lookup"><span data-stu-id="4392e-106">The hours worked data is typically stored in a time and attendance system.</span></span> <span data-ttu-id="4392e-107">在 Talent: Core HR 中，可导入这些正常工时和加班工时并用作奖励员工的基数。</span><span class="sxs-lookup"><span data-stu-id="4392e-107">In Talent: Core HR, those regular and overtime hours worked can be imported and used as a basis for an employee's award.</span></span>

## <a name="leave-plans"></a><span data-ttu-id="4392e-108">休假计划</span><span class="sxs-lookup"><span data-stu-id="4392e-108">Leave plans</span></span>

<span data-ttu-id="4392e-109">在休假计划内，累积类型可以是服务月数或工作时数。</span><span class="sxs-lookup"><span data-stu-id="4392e-109">Within the leave plan, the accrual type can either be months of service or hours worked.</span></span> <span data-ttu-id="4392e-110">如果选择工作时数，则累积使用两种类型的时数：正常时数和加班时数。</span><span class="sxs-lookup"><span data-stu-id="4392e-110">When hours worked is selected, there are two types of hours to use for the accural: regular and overtime.</span></span>

<span data-ttu-id="4392e-111">若要将休假计划设置为使用工作时数，请执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="4392e-111">To set up a leave plan to use hours worked, follow these steps:</span></span>

1. <span data-ttu-id="4392e-112">在**休假和缺勤计划**页中，单击**创建新计划**。</span><span class="sxs-lookup"><span data-stu-id="4392e-112">On the **Leave and absence plans** page, click **Create new plan**.</span></span>
2. <span data-ttu-id="4392e-113">输入休假计划的名称。</span><span class="sxs-lookup"><span data-stu-id="4392e-113">Enter a name for your leave plan.</span></span>
3. <span data-ttu-id="4392e-114">选择计划的累积频率。</span><span class="sxs-lookup"><span data-stu-id="4392e-114">Select the accrual frequency for the plan.</span></span>
5. <span data-ttu-id="4392e-115">选择计划的开始日期。</span><span class="sxs-lookup"><span data-stu-id="4392e-115">Select the start date for the plan.</span></span>
6. <span data-ttu-id="4392e-116">选择累积期间基数，然后选择员工的具体日期（如果适用）。</span><span class="sxs-lookup"><span data-stu-id="4392e-116">Choose the accrual period basis and select the employee-specific date, if applicable.</span></span>
7. <span data-ttu-id="4392e-117">对于累积计划，为累积类型选择**工作时数**。</span><span class="sxs-lookup"><span data-stu-id="4392e-117">For the accrual schedule, select **Hours worked** for the accrual type.</span></span>
8. <span data-ttu-id="4392e-118">选择要用于累积的时数类型。</span><span class="sxs-lookup"><span data-stu-id="4392e-118">Select the type of hours to be used for the accrual.</span></span>
9. <span data-ttu-id="4392e-119">输入工作时数和关联的累积量、最小余额和最大结转或授权量。</span><span class="sxs-lookup"><span data-stu-id="4392e-119">Enter the number of hours worked and the associated accrual amount, minimum balance, and maximum carryforward or grant amount.</span></span>

<span data-ttu-id="4392e-120">工作时数计划的累积处理使用累积频率及累积期间基数来确定要累积的时数。</span><span class="sxs-lookup"><span data-stu-id="4392e-120">Accrual processing for hours worked plans uses the accrual frequency, along with the accrual period basis, to determine the hours to be accrued.</span></span>

## <a name="annual-accrual-frequency"></a><span data-ttu-id="4392e-121">年累积频率</span><span class="sxs-lookup"><span data-stu-id="4392e-121">Annual accrual frequency</span></span>

| <span data-ttu-id="4392e-122">累积奖励日期</span><span class="sxs-lookup"><span data-stu-id="4392e-122">Accrual award date</span></span>    | <span data-ttu-id="4392e-123">工作时数层</span><span class="sxs-lookup"><span data-stu-id="4392e-123">Hours worked tier</span></span>    | <span data-ttu-id="4392e-124">应计金额</span><span class="sxs-lookup"><span data-stu-id="4392e-124">Accrual amount</span></span>        | <span data-ttu-id="4392e-125">工作时数日期</span><span class="sxs-lookup"><span data-stu-id="4392e-125">Hours worked dates</span></span>   | <span data-ttu-id="4392e-126">工作时数累积</span><span class="sxs-lookup"><span data-stu-id="4392e-126">Hours worked actuals</span></span>| <span data-ttu-id="4392e-127">奖励</span><span class="sxs-lookup"><span data-stu-id="4392e-127">Award</span></span>               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| <span data-ttu-id="4392e-128">12/31/2018</span><span class="sxs-lookup"><span data-stu-id="4392e-128">12/31/2018</span></span>            | <span data-ttu-id="4392e-129">2080</span><span class="sxs-lookup"><span data-stu-id="4392e-129">2080</span></span>                 | <span data-ttu-id="4392e-130">144</span><span class="sxs-lookup"><span data-stu-id="4392e-130">144</span></span>                   | <span data-ttu-id="4392e-131">1/1/2018-12/31/2018</span><span class="sxs-lookup"><span data-stu-id="4392e-131">1/1/2018-12/31/2018</span></span>  | <span data-ttu-id="4392e-132">2085</span><span class="sxs-lookup"><span data-stu-id="4392e-132">2085</span></span>                | <span data-ttu-id="4392e-133">144</span><span class="sxs-lookup"><span data-stu-id="4392e-133">144</span></span>                 |        
| <span data-ttu-id="4392e-134">12/31/2018</span><span class="sxs-lookup"><span data-stu-id="4392e-134">12/31/2018</span></span>            | <span data-ttu-id="4392e-135">2080</span><span class="sxs-lookup"><span data-stu-id="4392e-135">2080</span></span>                 | <span data-ttu-id="4392e-136">144</span><span class="sxs-lookup"><span data-stu-id="4392e-136">144</span></span>                   | <span data-ttu-id="4392e-137">1/1/2018-12/31/2018</span><span class="sxs-lookup"><span data-stu-id="4392e-137">1/1/2018-12/31/2018</span></span>  | <span data-ttu-id="4392e-138">2000</span><span class="sxs-lookup"><span data-stu-id="4392e-138">2000</span></span>                | <span data-ttu-id="4392e-139">0</span><span class="sxs-lookup"><span data-stu-id="4392e-139">0</span></span>                 |


## <a name="monthly-accrual-frequency"></a><span data-ttu-id="4392e-140">月累积频率</span><span class="sxs-lookup"><span data-stu-id="4392e-140">Monthly accrual frequency</span></span>

| <span data-ttu-id="4392e-141">累积奖励日期</span><span class="sxs-lookup"><span data-stu-id="4392e-141">Accrual award date</span></span>    | <span data-ttu-id="4392e-142">工作时数层</span><span class="sxs-lookup"><span data-stu-id="4392e-142">Hours worked tier</span></span>    | <span data-ttu-id="4392e-143">应计金额</span><span class="sxs-lookup"><span data-stu-id="4392e-143">Accrual amount</span></span>        | <span data-ttu-id="4392e-144">工作时数日期</span><span class="sxs-lookup"><span data-stu-id="4392e-144">Hours worked dates</span></span>   | <span data-ttu-id="4392e-145">工作时数累积</span><span class="sxs-lookup"><span data-stu-id="4392e-145">Hours worked actuals</span></span>| <span data-ttu-id="4392e-146">奖励</span><span class="sxs-lookup"><span data-stu-id="4392e-146">Award</span></span>               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| <span data-ttu-id="4392e-147">8/31/2018</span><span class="sxs-lookup"><span data-stu-id="4392e-147">8/31/2018</span></span>             | <span data-ttu-id="4392e-148">160</span><span class="sxs-lookup"><span data-stu-id="4392e-148">160</span></span>                  | <span data-ttu-id="4392e-149">12</span><span class="sxs-lookup"><span data-stu-id="4392e-149">12</span></span>                    | <span data-ttu-id="4392e-150">8/1/2018-8/31/2018</span><span class="sxs-lookup"><span data-stu-id="4392e-150">8/1/2018-8/31/2018</span></span>   | <span data-ttu-id="4392e-151">184</span><span class="sxs-lookup"><span data-stu-id="4392e-151">184</span></span>                 | <span data-ttu-id="4392e-152">12</span><span class="sxs-lookup"><span data-stu-id="4392e-152">12</span></span>                  |        
| <span data-ttu-id="4392e-153">8/31/2018</span><span class="sxs-lookup"><span data-stu-id="4392e-153">8/31/2018</span></span>             | <span data-ttu-id="4392e-154">160</span><span class="sxs-lookup"><span data-stu-id="4392e-154">160</span></span>                  | <span data-ttu-id="4392e-155">3</span><span class="sxs-lookup"><span data-stu-id="4392e-155">3</span></span>                     | <span data-ttu-id="4392e-156">8/1/2018-8/31/2018</span><span class="sxs-lookup"><span data-stu-id="4392e-156">8/1/2018-8/31/2018</span></span>   | <span data-ttu-id="4392e-157">184</span><span class="sxs-lookup"><span data-stu-id="4392e-157">184</span></span>                 | <span data-ttu-id="4392e-158">3</span><span class="sxs-lookup"><span data-stu-id="4392e-158">3</span></span>                   |

## <a name="semi-monthly-accrual-frequency"></a><span data-ttu-id="4392e-159">半月累积频率</span><span class="sxs-lookup"><span data-stu-id="4392e-159">Semi-monthly accrual frequency</span></span>

| <span data-ttu-id="4392e-160">累积奖励日期</span><span class="sxs-lookup"><span data-stu-id="4392e-160">Accrual award date</span></span>    | <span data-ttu-id="4392e-161">工作时数层</span><span class="sxs-lookup"><span data-stu-id="4392e-161">Hours worked tier</span></span>    | <span data-ttu-id="4392e-162">应计金额</span><span class="sxs-lookup"><span data-stu-id="4392e-162">Accrual amount</span></span>        | <span data-ttu-id="4392e-163">工作时数日期</span><span class="sxs-lookup"><span data-stu-id="4392e-163">Hours worked dates</span></span>   | <span data-ttu-id="4392e-164">工作时数累积</span><span class="sxs-lookup"><span data-stu-id="4392e-164">Hours worked actuals</span></span>| <span data-ttu-id="4392e-165">奖励</span><span class="sxs-lookup"><span data-stu-id="4392e-165">Award</span></span>               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| <span data-ttu-id="4392e-166">8/31/2018</span><span class="sxs-lookup"><span data-stu-id="4392e-166">8/31/2018</span></span>             | <span data-ttu-id="4392e-167">80</span><span class="sxs-lookup"><span data-stu-id="4392e-167">80</span></span>                   | <span data-ttu-id="4392e-168">6</span><span class="sxs-lookup"><span data-stu-id="4392e-168">6</span></span>                     | <span data-ttu-id="4392e-169">8/16/2018-8/31/2018</span><span class="sxs-lookup"><span data-stu-id="4392e-169">8/16/2018-8/31/2018</span></span>  | <span data-ttu-id="4392e-170">81</span><span class="sxs-lookup"><span data-stu-id="4392e-170">81</span></span>                  | <span data-ttu-id="4392e-171">6</span><span class="sxs-lookup"><span data-stu-id="4392e-171">6</span></span>                  |        
| <span data-ttu-id="4392e-172">8/31/2018</span><span class="sxs-lookup"><span data-stu-id="4392e-172">8/31/2018</span></span>             | <span data-ttu-id="4392e-173">80</span><span class="sxs-lookup"><span data-stu-id="4392e-173">80</span></span>                   | <span data-ttu-id="4392e-174">6</span><span class="sxs-lookup"><span data-stu-id="4392e-174">6</span></span>                     | <span data-ttu-id="4392e-175">8/16/2018-8/31/2018</span><span class="sxs-lookup"><span data-stu-id="4392e-175">8/16/2018-8/31/2018</span></span>  | <span data-ttu-id="4392e-176">75</span><span class="sxs-lookup"><span data-stu-id="4392e-176">75</span></span>                  | <span data-ttu-id="4392e-177">0</span><span class="sxs-lookup"><span data-stu-id="4392e-177">0</span></span>                   |

## <a name="weekly-accrual-frequency"></a><span data-ttu-id="4392e-178">周累积频率</span><span class="sxs-lookup"><span data-stu-id="4392e-178">Weekly accrual frequency</span></span>

| <span data-ttu-id="4392e-179">累积奖励日期</span><span class="sxs-lookup"><span data-stu-id="4392e-179">Accrual award date</span></span>    | <span data-ttu-id="4392e-180">工作时数层</span><span class="sxs-lookup"><span data-stu-id="4392e-180">Hours worked tier</span></span>    | <span data-ttu-id="4392e-181">应计金额</span><span class="sxs-lookup"><span data-stu-id="4392e-181">Accrual amount</span></span>        | <span data-ttu-id="4392e-182">工作时数日期</span><span class="sxs-lookup"><span data-stu-id="4392e-182">Hours worked dates</span></span>   | <span data-ttu-id="4392e-183">工作时数累积</span><span class="sxs-lookup"><span data-stu-id="4392e-183">Hours worked actuals</span></span>| <span data-ttu-id="4392e-184">奖励</span><span class="sxs-lookup"><span data-stu-id="4392e-184">Award</span></span>               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| <span data-ttu-id="4392e-185">8/31/2018</span><span class="sxs-lookup"><span data-stu-id="4392e-185">8/31/2018</span></span>             | <span data-ttu-id="4392e-186">40</span><span class="sxs-lookup"><span data-stu-id="4392e-186">40</span></span>                   | <span data-ttu-id="4392e-187">3</span><span class="sxs-lookup"><span data-stu-id="4392e-187">3</span></span>                     | <span data-ttu-id="4392e-188">8/27/2018-8/31/2018</span><span class="sxs-lookup"><span data-stu-id="4392e-188">8/27/2018-8/31/2018</span></span>  | <span data-ttu-id="4392e-189">42</span><span class="sxs-lookup"><span data-stu-id="4392e-189">42</span></span>                  | <span data-ttu-id="4392e-190">3</span><span class="sxs-lookup"><span data-stu-id="4392e-190">3</span></span>                  |        
| <span data-ttu-id="4392e-191">8/31/2018</span><span class="sxs-lookup"><span data-stu-id="4392e-191">8/31/2018</span></span>             | <span data-ttu-id="4392e-192">40</span><span class="sxs-lookup"><span data-stu-id="4392e-192">40</span></span>                   | <span data-ttu-id="4392e-193">3</span><span class="sxs-lookup"><span data-stu-id="4392e-193">3</span></span>                     | <span data-ttu-id="4392e-194">8/27/2018-8/31/2018</span><span class="sxs-lookup"><span data-stu-id="4392e-194">8/27/2018-8/31/2018</span></span>  | <span data-ttu-id="4392e-195">35</span><span class="sxs-lookup"><span data-stu-id="4392e-195">35</span></span>                  | <span data-ttu-id="4392e-196">0</span><span class="sxs-lookup"><span data-stu-id="4392e-196">0</span></span>                   |

## <a name="employee-assigned-leave-plans"></a><span data-ttu-id="4392e-197">员工指定了休假计划</span><span class="sxs-lookup"><span data-stu-id="4392e-197">Employee assigned leave plans</span></span>

<span data-ttu-id="4392e-198">如果员工指定了休假计划，则为工作时数定义为累积类型的计划显示工时的层基准和类型。</span><span class="sxs-lookup"><span data-stu-id="4392e-198">In the employee's assigned leave plans, the tier basis and type of hours is displayed for plans where hours worked is defined as the accrual type.</span></span> <span data-ttu-id="4392e-199">对于活动计划，还将显示截止当前日期累积期间的累积工作时数供参考。</span><span class="sxs-lookup"><span data-stu-id="4392e-199">For active plans, the actual hours worked for the accrual periods as of the current date is also displayed for reference.</span></span> 

## <a name="loading-data"></a><span data-ttu-id="4392e-200">正在加载数据</span><span class="sxs-lookup"><span data-stu-id="4392e-200">Loading data</span></span>

<span data-ttu-id="4392e-201">可通过使用数据管理中的休假和缺勤工作时数实体导入累积时数。</span><span class="sxs-lookup"><span data-stu-id="4392e-201">Actual hours can be imported by using the Leave and absence hours worked entity in data management.</span></span> <span data-ttu-id="4392e-202">如果在使用工作日历，导入将验证正常工作时数是否不超过日历定义的当天计划时数。</span><span class="sxs-lookup"><span data-stu-id="4392e-202">If you are using working time calendars, the import will validate that regular hours worked doesn't exceed the scheduled hours in a day defined by the calendar.</span></span> <span data-ttu-id="4392e-203">导入还将验证给定日期的工作时数是否不超过 24 个小时。</span><span class="sxs-lookup"><span data-stu-id="4392e-203">The import also validates that the hours worked for a given day doesn't exceed 24 hours.</span></span> 

<span data-ttu-id="4392e-204">需要以下信息才能导入要在休假时间累积过程中使用的累积时数：</span><span class="sxs-lookup"><span data-stu-id="4392e-204">The following information is needed to import actual hours to be used in the leave accrual process:</span></span>

+ <span data-ttu-id="4392e-205">人员编号</span><span class="sxs-lookup"><span data-stu-id="4392e-205">Personnel number</span></span> 
+ <span data-ttu-id="4392e-206">工作日期</span><span class="sxs-lookup"><span data-stu-id="4392e-206">Date worked</span></span>
+ <span data-ttu-id="4392e-207">类型</span><span class="sxs-lookup"><span data-stu-id="4392e-207">Type</span></span>
+ <span data-ttu-id="4392e-208">工时</span><span class="sxs-lookup"><span data-stu-id="4392e-208">Hours</span></span>

<span data-ttu-id="4392e-209">一个日期只能与一种类型关联。</span><span class="sxs-lookup"><span data-stu-id="4392e-209">A single date can only have one of each type associated with it.</span></span>

| <span data-ttu-id="4392e-210">PERSONNELNUMBER</span><span class="sxs-lookup"><span data-stu-id="4392e-210">PERSONNELNUMBER</span></span>       | <span data-ttu-id="4392e-211">DATEWORKED</span><span class="sxs-lookup"><span data-stu-id="4392e-211">DATEWORKED</span></span>           | <span data-ttu-id="4392e-212">类型</span><span class="sxs-lookup"><span data-stu-id="4392e-212">TYPE</span></span>                  | <span data-ttu-id="4392e-213">HOURS</span><span class="sxs-lookup"><span data-stu-id="4392e-213">HOURS</span></span>                |
| --------------------- | -------------------- | --------------------- | -------------------- |
| <span data-ttu-id="4392e-214">000337</span><span class="sxs-lookup"><span data-stu-id="4392e-214">000337</span></span>                | <span data-ttu-id="4392e-215">8/6/2018</span><span class="sxs-lookup"><span data-stu-id="4392e-215">8/6/2018</span></span>             | <span data-ttu-id="4392e-216">常规</span><span class="sxs-lookup"><span data-stu-id="4392e-216">Regular</span></span>               | <span data-ttu-id="4392e-217">8</span><span class="sxs-lookup"><span data-stu-id="4392e-217">8</span></span>                    |       
| <span data-ttu-id="4392e-218">000337</span><span class="sxs-lookup"><span data-stu-id="4392e-218">000337</span></span>                | <span data-ttu-id="4392e-219">8/7/2018</span><span class="sxs-lookup"><span data-stu-id="4392e-219">8/7/2018</span></span>             | <span data-ttu-id="4392e-220">常规</span><span class="sxs-lookup"><span data-stu-id="4392e-220">Regular</span></span>               | <span data-ttu-id="4392e-221">8</span><span class="sxs-lookup"><span data-stu-id="4392e-221">8</span></span>                    |
| <span data-ttu-id="4392e-222">000337</span><span class="sxs-lookup"><span data-stu-id="4392e-222">000337</span></span>                | <span data-ttu-id="4392e-223">8/7/2018</span><span class="sxs-lookup"><span data-stu-id="4392e-223">8/7/2018</span></span>             | <span data-ttu-id="4392e-224">加班</span><span class="sxs-lookup"><span data-stu-id="4392e-224">Overtime</span></span>              | <span data-ttu-id="4392e-225">3</span><span class="sxs-lookup"><span data-stu-id="4392e-225">3</span></span>                    |
| <span data-ttu-id="4392e-226">000337</span><span class="sxs-lookup"><span data-stu-id="4392e-226">000337</span></span>                | <span data-ttu-id="4392e-227">8/8/2018</span><span class="sxs-lookup"><span data-stu-id="4392e-227">8/8/2018</span></span>             | <span data-ttu-id="4392e-228">常规</span><span class="sxs-lookup"><span data-stu-id="4392e-228">Regular</span></span>               | <span data-ttu-id="4392e-229">8</span><span class="sxs-lookup"><span data-stu-id="4392e-229">8</span></span>                    |
| <span data-ttu-id="4392e-230">000337</span><span class="sxs-lookup"><span data-stu-id="4392e-230">000337</span></span>                | <span data-ttu-id="4392e-231">8/7/2018</span><span class="sxs-lookup"><span data-stu-id="4392e-231">8/7/2018</span></span>             | <span data-ttu-id="4392e-232">常规</span><span class="sxs-lookup"><span data-stu-id="4392e-232">Regular</span></span>               | <span data-ttu-id="4392e-233">8</span><span class="sxs-lookup"><span data-stu-id="4392e-233">8</span></span>                    |
| <span data-ttu-id="4392e-234">000337</span><span class="sxs-lookup"><span data-stu-id="4392e-234">000337</span></span>                | <span data-ttu-id="4392e-235">8/9/2018</span><span class="sxs-lookup"><span data-stu-id="4392e-235">8/9/2018</span></span>             | <span data-ttu-id="4392e-236">常规</span><span class="sxs-lookup"><span data-stu-id="4392e-236">Regular</span></span>               | <span data-ttu-id="4392e-237">8</span><span class="sxs-lookup"><span data-stu-id="4392e-237">8</span></span>                    |
