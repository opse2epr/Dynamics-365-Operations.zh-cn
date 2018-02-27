---
title: "固定资产前滚报表"
description: "本主题说明如何使用固定资产前滚报表。"
author: saraschi2
manager: 
ms.date: 01/08/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 23021
ms.assetid: d7e86f72-95db-4423-9b04-761e9536a959
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-12-20
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 7a81697a8e90fb6b0695a02db0868f5708fdbddf
ms.contentlocale: zh-cn
ms.lasthandoff: 02/07/2018

---
# <a name="fixed-assets-roll-forward-report"></a><span data-ttu-id="3dd0f-103">固定资产前滚报表</span><span class="sxs-lookup"><span data-stu-id="3dd0f-103">Fixed assets roll forward report</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="3dd0f-104">**固定资产前滚**报表以通俗易懂的 Microsoft Excel 格式提供期间结帐、财务报表和报税所需的详细固定资产数据。</span><span class="sxs-lookup"><span data-stu-id="3dd0f-104">The **Fixed assets roll forward** report provides, in an easy-to-read Microsoft Excel format, the detailed fixed asset data that you require for period closing, financial statements, and tax reporting.</span></span> <span data-ttu-id="3dd0f-105">该报表中包含固定资产的期初余额和期末余额，期间的评估变动，以及该期间发生的任何新资产购置和处置。</span><span class="sxs-lookup"><span data-stu-id="3dd0f-105">The report includes start and end balances for fixed assets, together with valuation movements for the period, and any new asset acquisitions and disposals that occurred during the period.</span></span> <span data-ttu-id="3dd0f-106">将为单个固定资产报告数据，还将为固定资产组和法人汇总价值。</span><span class="sxs-lookup"><span data-stu-id="3dd0f-106">Data is reported for individual fixed assets, and values are also summarized for fixed asset groups and the legal entity.</span></span>

<span data-ttu-id="3dd0f-107">**固定资产前滚**报表使用电子申报 (ER) 框架。</span><span class="sxs-lookup"><span data-stu-id="3dd0f-107">The **Fixed assets roll forward** report uses the Electronic reporting (ER) framework.</span></span> <span data-ttu-id="3dd0f-108">必须先从 Microsoft Dynamics Lifecycle Services (LCS) 导入固定资产模型和固定资产前滚配置，才能运行该报表。</span><span class="sxs-lookup"><span data-stu-id="3dd0f-108">Before you can run the report, the Fixed assets model and Fixed asset roll-forward configurations must be imported from Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="3dd0f-109">有关说明，请参阅[从 Lifecycle Services 下载电子申报配置](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs)。</span><span class="sxs-lookup"><span data-stu-id="3dd0f-109">For instructions, see [Download Electronic reporting configurations from Lifecycle Services](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs).</span></span>

<span data-ttu-id="3dd0f-110">此报表在 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 7.3 中提供，或作为 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition（2017 年 7 月）的修补程序提供。</span><span class="sxs-lookup"><span data-stu-id="3dd0f-110">This report is available in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3, or as a hotfix for Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017).</span></span> <span data-ttu-id="3dd0f-111">必须为安装了 2017 年 7 月版本的环境应用三个修补程序：</span><span class="sxs-lookup"><span data-stu-id="3dd0f-111">Three hotfixes must be applied to environments that have the July 2017 release:</span></span>

- <span data-ttu-id="3dd0f-112">**KB 4041754：**不能从 LCS 下载电子申报 (ER) 配置，因为应用了平台更新包后不适用于当前应用程序版本。</span><span class="sxs-lookup"><span data-stu-id="3dd0f-112">**KB 4041754:** Electronic reporting (ER) configuration can't be downloaded from LCS as not applicable for the current application version after applying the platform update package</span></span>
- <span data-ttu-id="3dd0f-113">**KB 4056107：**电子申报 (GER) 累积更新 5</span><span class="sxs-lookup"><span data-stu-id="3dd0f-113">**KB 4056107:** Electronic reporting (GER) cumulative update 5</span></span>
- <span data-ttu-id="3dd0f-114">**KB 4056353：**固定资产对帐单报表和附注报表不满足 GAAP 和 IFRS 中的要求</span><span class="sxs-lookup"><span data-stu-id="3dd0f-114">**KB 4056353:** Fixed assets Statement and Notes reports don't meet the requirements in GAAP and IFRS</span></span>

<span data-ttu-id="3dd0f-115">下表说明报表中的可用字段。</span><span class="sxs-lookup"><span data-stu-id="3dd0f-115">The following table describes the fields that are available on the report.</span></span>

| <span data-ttu-id="3dd0f-116">字段</span><span class="sxs-lookup"><span data-stu-id="3dd0f-116">Field</span></span>                                       | <span data-ttu-id="3dd0f-117">说明</span><span class="sxs-lookup"><span data-stu-id="3dd0f-117">Description</span></span> |
|---------------------------------------------|-------------|
| <span data-ttu-id="3dd0f-118">余额：期初</span><span class="sxs-lookup"><span data-stu-id="3dd0f-118">Balances: Opening</span></span>                           | <span data-ttu-id="3dd0f-119">报表中指定的“开始”日期的固定资产帐面净值。</span><span class="sxs-lookup"><span data-stu-id="3dd0f-119">The fixed asset net book value as of the "from" date that is specified on the report.</span></span> |
| <span data-ttu-id="3dd0f-120">余额：期末</span><span class="sxs-lookup"><span data-stu-id="3dd0f-120">Balances: Closing</span></span>                           | <span data-ttu-id="3dd0f-121">报表中指定的“结束”日期的固定资产帐面净值。</span><span class="sxs-lookup"><span data-stu-id="3dd0f-121">The fixed asset net book value as of the "to" date that is specified on the report.</span></span> |
| <span data-ttu-id="3dd0f-122">购置：期初值</span><span class="sxs-lookup"><span data-stu-id="3dd0f-122">Acquisitions: Opening value</span></span>                 | <span data-ttu-id="3dd0f-123">截止报表中指定的“开始”日期的类型为**购置**和**购置调整**的所有交易记录的总和。</span><span class="sxs-lookup"><span data-stu-id="3dd0f-123">The sum of all transactions of the **Acquisition** and **Acquisition adjustment** types up to the "from" date that is specified on the report.</span></span> |
| <span data-ttu-id="3dd0f-124">购置：期间购置</span><span class="sxs-lookup"><span data-stu-id="3dd0f-124">Acquisitions: Period acquisitions</span></span>           | <span data-ttu-id="3dd0f-125">报表的日期范围内过帐且类型为**购置**和**购置调整**的所有交易记录的总和。</span><span class="sxs-lookup"><span data-stu-id="3dd0f-125">The sum of all transactions of the **Acquisition** and **Acquisition adjustment** types that were posted during the date range for the report.</span></span> |
| <span data-ttu-id="3dd0f-126">购置：期间处置</span><span class="sxs-lookup"><span data-stu-id="3dd0f-126">Acquisitions: Period disposals</span></span>              | <span data-ttu-id="3dd0f-127">报表的日期范围内过帐且具有处置交易记录的所有购置冲销的总和。</span><span class="sxs-lookup"><span data-stu-id="3dd0f-127">The sum of all acquisition reversals that were posted that had a disposal transaction during the date range for the report.</span></span> |
| <span data-ttu-id="3dd0f-128">购置：期末值</span><span class="sxs-lookup"><span data-stu-id="3dd0f-128">Acquisitions: Closing value</span></span>                 | <span data-ttu-id="3dd0f-129">截止报表中指定的“结束”日期的类型为**购置**和**购置调整**的所有交易记录的总和。</span><span class="sxs-lookup"><span data-stu-id="3dd0f-129">The sum of all transactions of the **Acquisition** and **Acquisition adjustment** types up to the "to" date that is specified on the report.</span></span> |
| <span data-ttu-id="3dd0f-130">折旧：期初值</span><span class="sxs-lookup"><span data-stu-id="3dd0f-130">Depreciations: Opening value</span></span>                | <span data-ttu-id="3dd0f-131">截止报表中指定的“开始”日期的类型为**折旧**、**折旧调整**、**特殊折旧补偿**和**特别折旧**的所有交易记录的总和。</span><span class="sxs-lookup"><span data-stu-id="3dd0f-131">The sum of all transactions of the **Depreciation**, **Depreciation adjustment**, **Special depreciation allowance**, and **Extraordinary depreciation** types up to the "from" date that is specified on the report.</span></span> |
| <span data-ttu-id="3dd0f-132">折旧：期间折旧</span><span class="sxs-lookup"><span data-stu-id="3dd0f-132">Depreciations: Period depreciations</span></span>         | <span data-ttu-id="3dd0f-133">报表的日期范围内过帐且类型为**折旧**、**折旧调整**和**特别折旧**的所有交易记录的总和。</span><span class="sxs-lookup"><span data-stu-id="3dd0f-133">The sum of all transactions of the **Depreciation**, **Depreciation adjustment**, and **Extraordinary depreciation** types that were posted during the date range for the report.</span></span> |
| <span data-ttu-id="3dd0f-134">折旧：期间特殊折旧</span><span class="sxs-lookup"><span data-stu-id="3dd0f-134">Depreciations: Period special depreciations</span></span> | <span data-ttu-id="3dd0f-135">报表的日期范围内过帐且类型为**特殊折旧补偿**的所有交易记录的总和。</span><span class="sxs-lookup"><span data-stu-id="3dd0f-135">The sum of all transactions of the **Special depreciation allowance** type that were posted during the date range for the report.</span></span> |
| <span data-ttu-id="3dd0f-136">折旧：期间处置</span><span class="sxs-lookup"><span data-stu-id="3dd0f-136">Depreciations: Period disposals</span></span>             | <span data-ttu-id="3dd0f-137">报表的日期范围内过帐且具有处置交易记录的所有折旧冲销的总和。</span><span class="sxs-lookup"><span data-stu-id="3dd0f-137">The sum of all depreciation reversals that were posted that had a disposal transaction during the date range for the report.</span></span> |
| <span data-ttu-id="3dd0f-138">折旧：期末值</span><span class="sxs-lookup"><span data-stu-id="3dd0f-138">Depreciations: Closing value</span></span>                | <span data-ttu-id="3dd0f-139">截止报表中指定的“结束”日期的类型为**折旧**、**折旧调整**、**特殊折旧补偿**和**特别折旧**的所有交易记录的总和。</span><span class="sxs-lookup"><span data-stu-id="3dd0f-139">The sum of all transactions of the **Depreciation**, **Depreciation adjustment**, **Special depreciation allowance**, and **Extraordinary depreciation** types up to the "to" date that is specified on the report.</span></span> |
| <span data-ttu-id="3dd0f-140">调高/调低：期初值</span><span class="sxs-lookup"><span data-stu-id="3dd0f-140">Write-ups/Write downs: Opening value</span></span>        | <span data-ttu-id="3dd0f-141">截止报表中指定的“开始”日期的类型为**调高**、**调低**和**重估**的所有交易记录的总和。</span><span class="sxs-lookup"><span data-stu-id="3dd0f-141">The sum of all transactions of the **Write up adjustment**, **Write down adjustment**, and **Revaluation** types up to the "from" date that is specified on the report.</span></span> |
| <span data-ttu-id="3dd0f-142">调高/调低：期间调高</span><span class="sxs-lookup"><span data-stu-id="3dd0f-142">Write-ups/Write downs: Period write ups</span></span>     | <span data-ttu-id="3dd0f-143">报表的日期范围内过帐且类型为**调高**的所有交易记录的总和。</span><span class="sxs-lookup"><span data-stu-id="3dd0f-143">The sum of all transactions of the **Write up adjustment** type that were posted during the date range for the report.</span></span> |
| <span data-ttu-id="3dd0f-144">调高/调低：期间调低</span><span class="sxs-lookup"><span data-stu-id="3dd0f-144">Write-ups/Write downs: Period write downs</span></span>   | <span data-ttu-id="3dd0f-145">报表的日期范围内过帐且类型为**调低**的所有交易记录的总和。</span><span class="sxs-lookup"><span data-stu-id="3dd0f-145">The sum of all transactions of the **Write down adjustment** type that were posted during the date range for the report.</span></span> |
| <span data-ttu-id="3dd0f-146">调高/调低：期间重估</span><span class="sxs-lookup"><span data-stu-id="3dd0f-146">Write-ups/Write downs: Period revaluations</span></span>  | <span data-ttu-id="3dd0f-147">报表的日期范围内过帐且类型为**重估**的所有交易记录的总和。</span><span class="sxs-lookup"><span data-stu-id="3dd0f-147">The sum of all transactions of the **Revaluation** type that were posted during the date range for the report.</span></span> |
| <span data-ttu-id="3dd0f-148">调高/调低：期间处置</span><span class="sxs-lookup"><span data-stu-id="3dd0f-148">Write-ups/Write downs: Period disposals</span></span>     | <span data-ttu-id="3dd0f-149">报表的日期范围内过帐且具有处置交易记录的所有调高、调低和重估冲销的总和。</span><span class="sxs-lookup"><span data-stu-id="3dd0f-149">The sum of all write-up, write-down, and revaluation reversals that were posted that had a disposal transaction during the date range for the report.</span></span> |
| <span data-ttu-id="3dd0f-150">调高/调低：期末值</span><span class="sxs-lookup"><span data-stu-id="3dd0f-150">Write-ups/Write downs: Closing value</span></span>        | <span data-ttu-id="3dd0f-151">截止报表中指定的“结束”日期的类型为**调高**、**调低**和**重估**的所有交易记录的总和。</span><span class="sxs-lookup"><span data-stu-id="3dd0f-151">The sum of all transactions of the **Write up adjustment**, **Write down adjustment**, and **Revaluation** types up to the "to" date that is specified on the report.</span></span> |
| <span data-ttu-id="3dd0f-152">处置：处置日期</span><span class="sxs-lookup"><span data-stu-id="3dd0f-152">Disposals: Disposal date</span></span>                    | <span data-ttu-id="3dd0f-153">固定资产帐簿的处置日期。</span><span class="sxs-lookup"><span data-stu-id="3dd0f-153">The disposal date for the fixed asset book.</span></span> |
| <span data-ttu-id="3dd0f-154">处置：处置时的帐面净值</span><span class="sxs-lookup"><span data-stu-id="3dd0f-154">Disposals: Net book value at disposal</span></span>       | <span data-ttu-id="3dd0f-155">处置时固定资产帐簿的帐面净值。</span><span class="sxs-lookup"><span data-stu-id="3dd0f-155">The net book value of the fixed asset book at the time of disposal.</span></span> |
| <span data-ttu-id="3dd0f-156">处置：销售值</span><span class="sxs-lookup"><span data-stu-id="3dd0f-156">Disposals: Sale value</span></span>                       | <span data-ttu-id="3dd0f-157">具有处置 - 销售交易记录的固定资产帐簿的销售值。</span><span class="sxs-lookup"><span data-stu-id="3dd0f-157">The sales value for the fixed asset book with a disposal – sale transaction.</span></span> |
| <span data-ttu-id="3dd0f-158">处置：损耗值</span><span class="sxs-lookup"><span data-stu-id="3dd0f-158">Disposals: Scrap value</span></span>                      | <span data-ttu-id="3dd0f-159">具有处置 - 损耗交易记录的固定资产帐簿的损耗值。</span><span class="sxs-lookup"><span data-stu-id="3dd0f-159">The scrap value for the fixed asset book with a disposal – scrap transaction.</span></span> |
| <span data-ttu-id="3dd0f-160">处置：损益</span><span class="sxs-lookup"><span data-stu-id="3dd0f-160">Disposals: Profit/Loss</span></span>                      | <span data-ttu-id="3dd0f-161">作为固定资产帐簿的处置交易记录一部分计算的损益值。</span><span class="sxs-lookup"><span data-stu-id="3dd0f-161">The profit or loss value that is calculated as part of the disposal transaction for the fixed asset book.</span></span> |
