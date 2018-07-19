---
title: "预订销售价"
description: "在您创建某一预订时，销售价将从在“销售价(预订)”窗体中创建的销售价设置中导出。"
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMASalespriceSubscription
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: d9d462121915ce3f800581a9540dc1ef8f6e785f
ms.contentlocale: zh-cn
ms.lasthandoff: 05/08/2018

---

# <a name="subscription-sales-prices"></a><span data-ttu-id="43e85-103">预订销售价</span><span class="sxs-lookup"><span data-stu-id="43e85-103">Subscription sales prices</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="43e85-104">在您创建某一预订时，销售价将从在**销售价(预订)** 窗体中创建的销售价设置中导出。</span><span class="sxs-lookup"><span data-stu-id="43e85-104">When you create a subscription, the sales price is derived from the sales price setup that was created in the **Sales price (subscription)** form.</span></span>

<span data-ttu-id="43e85-105">在**销售价(预订)** 窗体中，您可以为特定的预订创建销售价，或者可以创建更广泛应用的销售价。</span><span class="sxs-lookup"><span data-stu-id="43e85-105">In the **Sales price (subscription)** form, you can create sales prices for a specific subscription or you can create sales prices that apply more broadly.</span></span> <span data-ttu-id="43e85-106">对于要应用于某一预订的销售价，预订的期间代码和币种必须与期间代码和该销售价的币种相同。</span><span class="sxs-lookup"><span data-stu-id="43e85-106">For a sales price to be applied to a subscription, the period code and the currency of the subscription must be identical to the period code and the currency of the sales price.</span></span>

<span data-ttu-id="43e85-107">如果预订和销售价的期间代码和币种完全相同，则将基于在下表中列出的优先级选择预订销售价。</span><span class="sxs-lookup"><span data-stu-id="43e85-107">If the period code and currency are identical for the subscription and the sales price, subscription sales prices are selected on the basis of the priorities listed in the following table.</span></span> <span data-ttu-id="43e85-108">表中的空电池表示空字段，X 表示值等于从其生成交易记录的预订中的值。</span><span class="sxs-lookup"><span data-stu-id="43e85-108">A blank cell in the table indicates an empty field and an X indicates a value that is equal to the value in the subscription from which the transaction is generated.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="43e85-109">优先级 </span><span class="sxs-lookup"><span data-stu-id="43e85-109">Priority</span></span></p></th>
<th><p><span data-ttu-id="43e85-110"><strong>类别</strong></span><span class="sxs-lookup"><span data-stu-id="43e85-110"><strong>Category</strong></span></span></p></th>
<th><p><span data-ttu-id="43e85-111"><strong>项目 ID</strong></span><span class="sxs-lookup"><span data-stu-id="43e85-111"><strong>Project ID</strong></span></span></p></th>
<th><p><span data-ttu-id="43e85-112"><strong>预订</strong></span><span class="sxs-lookup"><span data-stu-id="43e85-112"><strong>Subscription</strong></span></span></p></th>
<th><p><span data-ttu-id="43e85-113"><strong>销售币种</strong></span><span class="sxs-lookup"><span data-stu-id="43e85-113"><strong>Sales currency</strong></span></span></p></th>
<th><p><span data-ttu-id="43e85-114"><strong>期间代码</strong></span><span class="sxs-lookup"><span data-stu-id="43e85-114"><strong>Period code</strong></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="43e85-115">1</span><span class="sxs-lookup"><span data-stu-id="43e85-115">1</span></span></p></td>
<td><p><span data-ttu-id="43e85-116">X</span><span class="sxs-lookup"><span data-stu-id="43e85-116">X</span></span></p></td>
<td><p><span data-ttu-id="43e85-117">X</span><span class="sxs-lookup"><span data-stu-id="43e85-117">X</span></span></p></td>
<td><p><span data-ttu-id="43e85-118">X</span><span class="sxs-lookup"><span data-stu-id="43e85-118">X</span></span></p></td>
<td><p><span data-ttu-id="43e85-119">X</span><span class="sxs-lookup"><span data-stu-id="43e85-119">X</span></span></p></td>
<td><p><span data-ttu-id="43e85-120">X</span><span class="sxs-lookup"><span data-stu-id="43e85-120">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43e85-121">2</span><span class="sxs-lookup"><span data-stu-id="43e85-121">2</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="43e85-122">X</span><span class="sxs-lookup"><span data-stu-id="43e85-122">X</span></span></p></td>
<td><p><span data-ttu-id="43e85-123">X</span><span class="sxs-lookup"><span data-stu-id="43e85-123">X</span></span></p></td>
<td><p><span data-ttu-id="43e85-124">X</span><span class="sxs-lookup"><span data-stu-id="43e85-124">X</span></span></p></td>
<td><p><span data-ttu-id="43e85-125">X</span><span class="sxs-lookup"><span data-stu-id="43e85-125">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43e85-126">3</span><span class="sxs-lookup"><span data-stu-id="43e85-126">3</span></span></p></td>
<td><p><span data-ttu-id="43e85-127">X</span><span class="sxs-lookup"><span data-stu-id="43e85-127">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="43e85-128">X</span><span class="sxs-lookup"><span data-stu-id="43e85-128">X</span></span></p></td>
<td><p><span data-ttu-id="43e85-129">X</span><span class="sxs-lookup"><span data-stu-id="43e85-129">X</span></span></p></td>
<td><p><span data-ttu-id="43e85-130">X</span><span class="sxs-lookup"><span data-stu-id="43e85-130">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43e85-131">4</span><span class="sxs-lookup"><span data-stu-id="43e85-131">4</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="43e85-132">X</span><span class="sxs-lookup"><span data-stu-id="43e85-132">X</span></span></p></td>
<td><p><span data-ttu-id="43e85-133">X</span><span class="sxs-lookup"><span data-stu-id="43e85-133">X</span></span></p></td>
<td><p><span data-ttu-id="43e85-134">X</span><span class="sxs-lookup"><span data-stu-id="43e85-134">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43e85-135">5</span><span class="sxs-lookup"><span data-stu-id="43e85-135">5</span></span></p></td>
<td><p><span data-ttu-id="43e85-136">X</span><span class="sxs-lookup"><span data-stu-id="43e85-136">X</span></span></p></td>
<td><p><span data-ttu-id="43e85-137">X</span><span class="sxs-lookup"><span data-stu-id="43e85-137">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="43e85-138">X</span><span class="sxs-lookup"><span data-stu-id="43e85-138">X</span></span></p></td>
<td><p><span data-ttu-id="43e85-139">X</span><span class="sxs-lookup"><span data-stu-id="43e85-139">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43e85-140">6</span><span class="sxs-lookup"><span data-stu-id="43e85-140">6</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="43e85-141">X</span><span class="sxs-lookup"><span data-stu-id="43e85-141">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="43e85-142">X</span><span class="sxs-lookup"><span data-stu-id="43e85-142">X</span></span></p></td>
<td><p><span data-ttu-id="43e85-143">X</span><span class="sxs-lookup"><span data-stu-id="43e85-143">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43e85-144">7</span><span class="sxs-lookup"><span data-stu-id="43e85-144">7</span></span></p></td>
<td><p><span data-ttu-id="43e85-145">X</span><span class="sxs-lookup"><span data-stu-id="43e85-145">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="43e85-146">X</span><span class="sxs-lookup"><span data-stu-id="43e85-146">X</span></span></p></td>
<td><p><span data-ttu-id="43e85-147">X</span><span class="sxs-lookup"><span data-stu-id="43e85-147">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43e85-148">8</span><span class="sxs-lookup"><span data-stu-id="43e85-148">8</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="43e85-149">X</span><span class="sxs-lookup"><span data-stu-id="43e85-149">X</span></span></p></td>
<td><p><span data-ttu-id="43e85-150">X</span><span class="sxs-lookup"><span data-stu-id="43e85-150">X</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="43e85-151">在创建预订费用时，具有最高详细级别的销售价（如上表中所述）将选作预订销售价。</span><span class="sxs-lookup"><span data-stu-id="43e85-151">When a subscription fee is created, the sales price with the greatest level of detail, as noted in the table above, is selected as the subscription sales price.</span></span>

## <a name="update-and-index-subscription-sales-prices"></a><span data-ttu-id="43e85-152">对预订销售价进行更新并编制索引</span><span class="sxs-lookup"><span data-stu-id="43e85-152">Update and index subscription sales prices</span></span>

<span data-ttu-id="43e85-153">您可以通过更新基价或指数，更新预订销售价。</span><span class="sxs-lookup"><span data-stu-id="43e85-153">You can update the subscription sales price by updating the base price or the index.</span></span> <span data-ttu-id="43e85-154">您可以按百分比更新，或者更新为新值。</span><span class="sxs-lookup"><span data-stu-id="43e85-154">You can update by a percentage or to a new value.</span></span>

## <a name="subscription-fee-sales-prices"></a><span data-ttu-id="43e85-155">预订费用销售价</span><span class="sxs-lookup"><span data-stu-id="43e85-155">Subscription fee sales prices</span></span>

<span data-ttu-id="43e85-156">在您创建预订费用时，销售价将基于预订的销售价设置。</span><span class="sxs-lookup"><span data-stu-id="43e85-156">When you create a subscription fee, the sales price is based on the sales price setup of the subscription.</span></span> <span data-ttu-id="43e85-157">您可以通过预订价格设置来使用基价，或者可以创建指数形式的销售价。</span><span class="sxs-lookup"><span data-stu-id="43e85-157">You can either use the base price from the subscription price setup or create indexed sales prices.</span></span>

## <a name="example"></a><span data-ttu-id="43e85-158">示例</span><span class="sxs-lookup"><span data-stu-id="43e85-158">Example</span></span>

<span data-ttu-id="43e85-159">您想要为新项目 9030 设置 EUR 500 的预订销售价。</span><span class="sxs-lookup"><span data-stu-id="43e85-159">You want to set up subscription sales prices of EUR 500 for a new project 9030.</span></span> <span data-ttu-id="43e85-160">在**销售价(预订)** 窗体中，可按照下表所示创建预订销售价。</span><span class="sxs-lookup"><span data-stu-id="43e85-160">In the **Sales price (subscription)** form, you create a subscription sales price line as indicated in the following table.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="43e85-161">生效日期</span><span class="sxs-lookup"><span data-stu-id="43e85-161">Valid from</span></span></p></th>
<th><p><span data-ttu-id="43e85-162">类别</span><span class="sxs-lookup"><span data-stu-id="43e85-162">Category</span></span></p></th>
<th><p><span data-ttu-id="43e85-163">项目</span><span class="sxs-lookup"><span data-stu-id="43e85-163">Project</span></span></p></th>
<th><p><span data-ttu-id="43e85-164">预订</span><span class="sxs-lookup"><span data-stu-id="43e85-164">Subscription</span></span></p></th>
<th><p><span data-ttu-id="43e85-165">期间代码</span><span class="sxs-lookup"><span data-stu-id="43e85-165">Period code</span></span></p></th>
<th><p><span data-ttu-id="43e85-166">销售币种</span><span class="sxs-lookup"><span data-stu-id="43e85-166">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="43e85-167">销售价</span><span class="sxs-lookup"><span data-stu-id="43e85-167">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="43e85-168">28-08-2006</span><span class="sxs-lookup"><span data-stu-id="43e85-168">28-08-2006</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="43e85-169">9030</span><span class="sxs-lookup"><span data-stu-id="43e85-169">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="43e85-170">月</span><span class="sxs-lookup"><span data-stu-id="43e85-170">Month</span></span></p></td>
<td><p><span data-ttu-id="43e85-171">欧元</span><span class="sxs-lookup"><span data-stu-id="43e85-171">EUR</span></span></p></td>
<td><p><span data-ttu-id="43e85-172">500</span><span class="sxs-lookup"><span data-stu-id="43e85-172">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="43e85-173">请注意，**类别**字段和**预订**字段为空。</span><span class="sxs-lookup"><span data-stu-id="43e85-173">Note that the **Category** and **Subscription** fields are empty.</span></span>

<span data-ttu-id="43e85-174">然后，您创建以下预订。</span><span class="sxs-lookup"><span data-stu-id="43e85-174">You then create the following subscriptions.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="43e85-175">服务预订</span><span class="sxs-lookup"><span data-stu-id="43e85-175">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="43e85-176">项目</span><span class="sxs-lookup"><span data-stu-id="43e85-176">Project</span></span></p></th>
<th><p><span data-ttu-id="43e85-177">预订组</span><span class="sxs-lookup"><span data-stu-id="43e85-177">Subscription group</span></span></p></th>
<th><p><span data-ttu-id="43e85-178">类别</span><span class="sxs-lookup"><span data-stu-id="43e85-178">Category</span></span></p></th>
<th><p><span data-ttu-id="43e85-179">币种</span><span class="sxs-lookup"><span data-stu-id="43e85-179">Currency</span></span></p></th>
<th><p><span data-ttu-id="43e85-180">期间代码</span><span class="sxs-lookup"><span data-stu-id="43e85-180">Period code</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="43e85-181">00020_135</span><span class="sxs-lookup"><span data-stu-id="43e85-181">00020_135</span></span></p></td>
<td><p><span data-ttu-id="43e85-182">9030</span><span class="sxs-lookup"><span data-stu-id="43e85-182">9030</span></span></p></td>
<td><p><span data-ttu-id="43e85-183">Sub1</span><span class="sxs-lookup"><span data-stu-id="43e85-183">Sub1</span></span></p></td>
<td><p><span data-ttu-id="43e85-184">SubCat1</span><span class="sxs-lookup"><span data-stu-id="43e85-184">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="43e85-185">欧元</span><span class="sxs-lookup"><span data-stu-id="43e85-185">EUR</span></span></p></td>
<td><p><span data-ttu-id="43e85-186">每月</span><span class="sxs-lookup"><span data-stu-id="43e85-186">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43e85-187">00021_135</span><span class="sxs-lookup"><span data-stu-id="43e85-187">00021_135</span></span></p></td>
<td><p><span data-ttu-id="43e85-188">9030</span><span class="sxs-lookup"><span data-stu-id="43e85-188">9030</span></span></p></td>
<td><p><span data-ttu-id="43e85-189">Sub1</span><span class="sxs-lookup"><span data-stu-id="43e85-189">Sub1</span></span></p></td>
<td><p><span data-ttu-id="43e85-190">SubCat2</span><span class="sxs-lookup"><span data-stu-id="43e85-190">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="43e85-191">欧元</span><span class="sxs-lookup"><span data-stu-id="43e85-191">EUR</span></span></p></td>
<td><p><span data-ttu-id="43e85-192">每月</span><span class="sxs-lookup"><span data-stu-id="43e85-192">Monthly</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="43e85-193">现在，您为预订组 Sub1 中的两个预订都创建了预订费用：</span><span class="sxs-lookup"><span data-stu-id="43e85-193">Now you create subscription fees for both subscriptions in the subscription group Sub1:</span></span>

1.  <span data-ttu-id="43e85-194">单击**服务管理** \> **设置** \> **服务预订** \> **预订组**。</span><span class="sxs-lookup"><span data-stu-id="43e85-194">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups**.</span></span>

2.  <span data-ttu-id="43e85-195">在**预订组**窗体中，单击**功能** \> **创建预订费用**。</span><span class="sxs-lookup"><span data-stu-id="43e85-195">In the **Subscription groups** form, click **Function** \> **Create subscription fee**.</span></span>

3.  <span data-ttu-id="43e85-196">在**创建预订费用**窗体中，输入相应信息。</span><span class="sxs-lookup"><span data-stu-id="43e85-196">In the **Create subscription fee** form, enter the appropriate information.</span></span> <span data-ttu-id="43e85-197">有关详细信息，请参阅[创建预订费用交易记录](create-subscription-fee-transactions.md)。</span><span class="sxs-lookup"><span data-stu-id="43e85-197">For more information, see [Create subscription fee transactions](create-subscription-fee-transactions.md).</span></span>

<span data-ttu-id="43e85-198">为两个预订创建具有 EUR 500 销售价的费用，如下表中所示。</span><span class="sxs-lookup"><span data-stu-id="43e85-198">Subscription fees that have a sales price of EUR 500 are created for both subscriptions, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="43e85-199">项目日期</span><span class="sxs-lookup"><span data-stu-id="43e85-199">Project date</span></span></p></th>
<th><p><span data-ttu-id="43e85-200">服务预订</span><span class="sxs-lookup"><span data-stu-id="43e85-200">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="43e85-201">项目</span><span class="sxs-lookup"><span data-stu-id="43e85-201">Project</span></span></p></th>
<th><p><span data-ttu-id="43e85-202">类别</span><span class="sxs-lookup"><span data-stu-id="43e85-202">Category</span></span></p></th>
<th><p><span data-ttu-id="43e85-203">开始日期</span><span class="sxs-lookup"><span data-stu-id="43e85-203">Start date</span></span></p></th>
<th><p><span data-ttu-id="43e85-204">结束日期</span><span class="sxs-lookup"><span data-stu-id="43e85-204">End date</span></span></p></th>
<th><p><span data-ttu-id="43e85-205">销售币种</span><span class="sxs-lookup"><span data-stu-id="43e85-205">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="43e85-206">销售价</span><span class="sxs-lookup"><span data-stu-id="43e85-206">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="43e85-207">28-08-2006</span><span class="sxs-lookup"><span data-stu-id="43e85-207">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="43e85-208">00020_135</span><span class="sxs-lookup"><span data-stu-id="43e85-208">00020_135</span></span></p></td>
<td><p><span data-ttu-id="43e85-209">9030</span><span class="sxs-lookup"><span data-stu-id="43e85-209">9030</span></span></p></td>
<td><p><span data-ttu-id="43e85-210">SubCat1</span><span class="sxs-lookup"><span data-stu-id="43e85-210">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="43e85-211">01-01-2007</span><span class="sxs-lookup"><span data-stu-id="43e85-211">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="43e85-212">31-03-2007</span><span class="sxs-lookup"><span data-stu-id="43e85-212">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="43e85-213">欧元</span><span class="sxs-lookup"><span data-stu-id="43e85-213">EUR</span></span></p></td>
<td><p><span data-ttu-id="43e85-214">500</span><span class="sxs-lookup"><span data-stu-id="43e85-214">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43e85-215">28-08-2006</span><span class="sxs-lookup"><span data-stu-id="43e85-215">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="43e85-216">00021_135</span><span class="sxs-lookup"><span data-stu-id="43e85-216">00021_135</span></span></p></td>
<td><p><span data-ttu-id="43e85-217">9030</span><span class="sxs-lookup"><span data-stu-id="43e85-217">9030</span></span></p></td>
<td><p><span data-ttu-id="43e85-218">SubCat2</span><span class="sxs-lookup"><span data-stu-id="43e85-218">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="43e85-219">01-01-2007</span><span class="sxs-lookup"><span data-stu-id="43e85-219">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="43e85-220">31-03-2007</span><span class="sxs-lookup"><span data-stu-id="43e85-220">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="43e85-221">欧元</span><span class="sxs-lookup"><span data-stu-id="43e85-221">EUR</span></span></p></td>
<td><p><span data-ttu-id="43e85-222">500</span><span class="sxs-lookup"><span data-stu-id="43e85-222">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="43e85-223">以后，您决定要为项目 9030 的类别 SubCat1 指定销售价。</span><span class="sxs-lookup"><span data-stu-id="43e85-223">Later, you decide that you want to specify sales prices for the category SubCat1 for project 9030.</span></span> <span data-ttu-id="43e85-224">因此，您创建一个新的销售价行，该行具有针对项目 9030 和费用类别 SubCat1 的组合的 EUR 550 的销售价。</span><span class="sxs-lookup"><span data-stu-id="43e85-224">Therefore, you create a new sales price line that has a sales price of EUR 550 for the combination of project 9030 and fee category SubCat1.</span></span> <span data-ttu-id="43e85-225">现在项目 9030 存在两个预订销售价行，如下表中所示。</span><span class="sxs-lookup"><span data-stu-id="43e85-225">There are now two subscription sales price lines for project 9030, as shown in the following table.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="43e85-226">生效日期</span><span class="sxs-lookup"><span data-stu-id="43e85-226">Valid from</span></span></p></th>
<th><p><span data-ttu-id="43e85-227">类别</span><span class="sxs-lookup"><span data-stu-id="43e85-227">Category</span></span></p></th>
<th><p><span data-ttu-id="43e85-228">项目</span><span class="sxs-lookup"><span data-stu-id="43e85-228">Project</span></span></p></th>
<th><p><span data-ttu-id="43e85-229">预订</span><span class="sxs-lookup"><span data-stu-id="43e85-229">Subscription</span></span></p></th>
<th><p><span data-ttu-id="43e85-230">期间代码</span><span class="sxs-lookup"><span data-stu-id="43e85-230">Period code</span></span></p></th>
<th><p><span data-ttu-id="43e85-231">货币</span><span class="sxs-lookup"><span data-stu-id="43e85-231">Currency</span></span></p></th>
<th><p><span data-ttu-id="43e85-232">销售价</span><span class="sxs-lookup"><span data-stu-id="43e85-232">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="43e85-233">28-08-2007</span><span class="sxs-lookup"><span data-stu-id="43e85-233">28-08-2007</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="43e85-234">9030</span><span class="sxs-lookup"><span data-stu-id="43e85-234">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="43e85-235">月</span><span class="sxs-lookup"><span data-stu-id="43e85-235">Month</span></span></p></td>
<td><p><span data-ttu-id="43e85-236">欧元</span><span class="sxs-lookup"><span data-stu-id="43e85-236">EUR</span></span></p></td>
<td><p><span data-ttu-id="43e85-237">500</span><span class="sxs-lookup"><span data-stu-id="43e85-237">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43e85-238">28-08-2007</span><span class="sxs-lookup"><span data-stu-id="43e85-238">28-08-2007</span></span></p></td>
<td><p><span data-ttu-id="43e85-239">SubCat1</span><span class="sxs-lookup"><span data-stu-id="43e85-239">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="43e85-240">9030</span><span class="sxs-lookup"><span data-stu-id="43e85-240">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="43e85-241">月</span><span class="sxs-lookup"><span data-stu-id="43e85-241">Month</span></span></p></td>
<td><p><span data-ttu-id="43e85-242">欧元</span><span class="sxs-lookup"><span data-stu-id="43e85-242">EUR</span></span></p></td>
<td><p><span data-ttu-id="43e85-243">550</span><span class="sxs-lookup"><span data-stu-id="43e85-243">550</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="43e85-244">您重复执行上述过程，以便为预订组 Sub1 中的两个预订都创建预订费用。</span><span class="sxs-lookup"><span data-stu-id="43e85-244">You repeat the procedure described above to create subscription fees for both subscriptions in the subscription group Sub1.</span></span> <span data-ttu-id="43e85-245">下表显示为每个预订创建的附加到该预订组的交易记录。</span><span class="sxs-lookup"><span data-stu-id="43e85-245">The following table shows the transactions that are created for each subscription that is attached to the subscription group.</span></span>

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="43e85-246">项目日期</span><span class="sxs-lookup"><span data-stu-id="43e85-246">Project date</span></span></p></th>
<th><p><span data-ttu-id="43e85-247">预订</span><span class="sxs-lookup"><span data-stu-id="43e85-247">Subscription</span></span></p></th>
<th><p><span data-ttu-id="43e85-248">项目</span><span class="sxs-lookup"><span data-stu-id="43e85-248">Project</span></span></p></th>
<th><p><span data-ttu-id="43e85-249">类别</span><span class="sxs-lookup"><span data-stu-id="43e85-249">Category</span></span></p></th>
<th><p><span data-ttu-id="43e85-250">开始日期</span><span class="sxs-lookup"><span data-stu-id="43e85-250">Start date</span></span></p></th>
<th><p><span data-ttu-id="43e85-251">结束日期</span><span class="sxs-lookup"><span data-stu-id="43e85-251">End date</span></span></p></th>
<th><p><span data-ttu-id="43e85-252">销售币种</span><span class="sxs-lookup"><span data-stu-id="43e85-252">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="43e85-253">销售价</span><span class="sxs-lookup"><span data-stu-id="43e85-253">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="43e85-254">28-07-2007</span><span class="sxs-lookup"><span data-stu-id="43e85-254">28-07-2007</span></span></p></td>
<td><p><span data-ttu-id="43e85-255">00020_135</span><span class="sxs-lookup"><span data-stu-id="43e85-255">00020_135</span></span></p></td>
<td><p><span data-ttu-id="43e85-256">9030</span><span class="sxs-lookup"><span data-stu-id="43e85-256">9030</span></span></p></td>
<td><p><span data-ttu-id="43e85-257">SubCat1</span><span class="sxs-lookup"><span data-stu-id="43e85-257">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="43e85-258">01-01-2008</span><span class="sxs-lookup"><span data-stu-id="43e85-258">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="43e85-259">31-03-2008</span><span class="sxs-lookup"><span data-stu-id="43e85-259">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="43e85-260">欧元</span><span class="sxs-lookup"><span data-stu-id="43e85-260">EUR</span></span></p></td>
<td><p><span data-ttu-id="43e85-261">550</span><span class="sxs-lookup"><span data-stu-id="43e85-261">550</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43e85-262">28-07-2008</span><span class="sxs-lookup"><span data-stu-id="43e85-262">28-07-2008</span></span></p></td>
<td><p><span data-ttu-id="43e85-263">00021_135</span><span class="sxs-lookup"><span data-stu-id="43e85-263">00021_135</span></span></p></td>
<td><p><span data-ttu-id="43e85-264">9030</span><span class="sxs-lookup"><span data-stu-id="43e85-264">9030</span></span></p></td>
<td><p><span data-ttu-id="43e85-265">SubCat2</span><span class="sxs-lookup"><span data-stu-id="43e85-265">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="43e85-266">01-01-2008</span><span class="sxs-lookup"><span data-stu-id="43e85-266">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="43e85-267">31-03-2008</span><span class="sxs-lookup"><span data-stu-id="43e85-267">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="43e85-268">欧元</span><span class="sxs-lookup"><span data-stu-id="43e85-268">EUR</span></span></p></td>
<td><p><span data-ttu-id="43e85-269">500</span><span class="sxs-lookup"><span data-stu-id="43e85-269">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="43e85-270">在预订 00020\_135 的第一个交易记录中，EUR 550 的销售价从为特定项目和类别的组合设置的预订销售价中导出。</span><span class="sxs-lookup"><span data-stu-id="43e85-270">In the first transaction for subscription 00020\_135, the sales price of EUR 550 derives from the subscription sales price that is set up for the combination of the specific project and category.</span></span> <span data-ttu-id="43e85-271">在预订 00021\_135 的第二个交易记录中，EUR 500 的销售价用作项目预订销售价，因为不存在为项目 9030 和类别 SubCat2 的组合设置的价格。</span><span class="sxs-lookup"><span data-stu-id="43e85-271">In the second transaction for subscription 00021\_135, the sales price of EUR 500 is used as the project subscription sales price because there is no price set up for the combination of project 9030 and category SubCat2.</span></span>

## <a name="see-also"></a><span data-ttu-id="43e85-272">请参阅</span><span class="sxs-lookup"><span data-stu-id="43e85-272">See also</span></span>

[<span data-ttu-id="43e85-273">对预订销售价进行更新并编制索引</span><span class="sxs-lookup"><span data-stu-id="43e85-273">Update and index subscription sales prices</span></span>](update-and-index-subscription-sales-prices.md)

  


