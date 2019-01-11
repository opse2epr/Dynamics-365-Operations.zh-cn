---
title: "将任务指南保存到 LCS 并重新播放它们"
description: "本主题说明如何将任务指南保存到 Microsoft Dynamics Lifecycle Services (LCS) 然后重新播放它们。"
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 40b4c3154a04a557b8a670e1f1ae3722c71122fe
ms.contentlocale: zh-cn
ms.lasthandoff: 12/04/2018

---

# <a name="save-task-guides-to-lcs-and-replay-them"></a><span data-ttu-id="ab306-103">将任务指南保存到 LCS 并重新播放它们</span><span class="sxs-lookup"><span data-stu-id="ab306-103">Save task guides to LCS and replay them</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ab306-104">**环境详细信息**</span><span class="sxs-lookup"><span data-stu-id="ab306-104">**Environment details**</span></span> 

<span data-ttu-id="ab306-105">Microsoft Dynamics 365 for Talent 通过 Microsoft Dynamics Lifecycle Services (LCS) 部署</span><span class="sxs-lookup"><span data-stu-id="ab306-105">Microsoft Dynamics 365 for Talent, which was deployed via Microsoft Dynamics Lifecycle Services (LCS)</span></span>

<span data-ttu-id="ab306-106">**发货**</span><span class="sxs-lookup"><span data-stu-id="ab306-106">**Issue**</span></span>

<span data-ttu-id="ab306-107">客户希望将新任务录制保存到其 LCS 项目，然后重新播放保存的任务指南。</span><span class="sxs-lookup"><span data-stu-id="ab306-107">The customer wants to save new task recordings to his or her LCS project, and then replay the saved task guides.</span></span>

<span data-ttu-id="ab306-108">**分辨率**</span><span class="sxs-lookup"><span data-stu-id="ab306-108">**Resolution**</span></span>

<span data-ttu-id="ab306-109">请执行以下步骤将任务录制保存到 LCS。</span><span class="sxs-lookup"><span data-stu-id="ab306-109">Follow these steps to save a task recording to LCS.</span></span>

1. <span data-ttu-id="ab306-110">登录到 LCS，并选择项目。</span><span class="sxs-lookup"><span data-stu-id="ab306-110">Sign in to LCS, and select the project.</span></span>
2. <span data-ttu-id="ab306-111">选择**业务流程建模器**磁贴。</span><span class="sxs-lookup"><span data-stu-id="ab306-111">Select the **Business process modeler** tile.</span></span>
3. <span data-ttu-id="ab306-112">在“更新的 BPM 体验”中查看此页面。</span><span class="sxs-lookup"><span data-stu-id="ab306-112">View the page in the "Updated BPM experience."</span></span>
4. <span data-ttu-id="ab306-113">选择库，然后选择**复制**。</span><span class="sxs-lookup"><span data-stu-id="ab306-113">Select a library, and then select **Copy**.</span></span>
5. <span data-ttu-id="ab306-114">为业务流程建模器 (BPM) 模型输入一个名称。</span><span class="sxs-lookup"><span data-stu-id="ab306-114">Enter a name for the Business process modeler (BPM) model.</span></span>
6. <span data-ttu-id="ab306-115">从 LCS 登录 Talent。</span><span class="sxs-lookup"><span data-stu-id="ab306-115">Sign in to Talent from LCS.</span></span>
7. <span data-ttu-id="ab306-116">在**搜索**字段中，输入**帮助**。</span><span class="sxs-lookup"><span data-stu-id="ab306-116">In the **Search** field, enter **help**.</span></span> <span data-ttu-id="ab306-117">Lifecycle Services 帮助将打开。</span><span class="sxs-lookup"><span data-stu-id="ab306-117">Lifecycle Services Help is opened.</span></span>
8. <span data-ttu-id="ab306-118">选择 Lifecycle Services 帮助配置的**刷新**按钮。</span><span class="sxs-lookup"><span data-stu-id="ab306-118">Select the **Refresh** button for Lifecycle Services Help configuration.</span></span>

    <span data-ttu-id="ab306-119">您的新 BPM 库应会出现，它应是活动的。</span><span class="sxs-lookup"><span data-stu-id="ab306-119">Your new BPM library should appear, and it should be active.</span></span>

9. <span data-ttu-id="ab306-120">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="ab306-120">Close the page.</span></span>
10. <span data-ttu-id="ab306-121">创建任务录制。</span><span class="sxs-lookup"><span data-stu-id="ab306-121">Create a task recording.</span></span>
11. <span data-ttu-id="ab306-122">当您完成时，选择**保存到 Lifecycle Services**。</span><span class="sxs-lookup"><span data-stu-id="ab306-122">When you've finished, select **Save to Lifecycle Services**.</span></span>

    ![保存到 Lifecycle Services](media/task-guides.png)

12. <span data-ttu-id="ab306-124">选择要保存任务录制的 BPM 库和节点。</span><span class="sxs-lookup"><span data-stu-id="ab306-124">Select the BPM library and node to save the task recording to.</span></span>

<span data-ttu-id="ab306-125">执行以下步骤从 LCS 重新播放任务指南。</span><span class="sxs-lookup"><span data-stu-id="ab306-125">Follow these steps to replay a task guide from LCS.</span></span>

1. <span data-ttu-id="ab306-126">启动任务录制器</span><span class="sxs-lookup"><span data-stu-id="ab306-126">Start Task recorder.</span></span>
2. <span data-ttu-id="ab306-127">选择**从 LCS 打开**。</span><span class="sxs-lookup"><span data-stu-id="ab306-127">Select **Open from LCS**.</span></span>
3. <span data-ttu-id="ab306-128">选择包含保存的任务指南的库和 BPM 节点。</span><span class="sxs-lookup"><span data-stu-id="ab306-128">Select the library and the BPM node that have the saved task guide.</span></span>
4. <span data-ttu-id="ab306-129">打开任务指南。</span><span class="sxs-lookup"><span data-stu-id="ab306-129">Open the task guide.</span></span>
