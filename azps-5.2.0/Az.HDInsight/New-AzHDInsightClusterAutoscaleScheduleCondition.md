---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 86276DF3-95E2-405F-BA46-F188B7AE3B9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterautoscaleschedulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleScheduleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleScheduleCondition.md
ms.openlocfilehash: 4f046344942e244d6bd220034f7cbe85c48681ef
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328369"
---
# <span data-ttu-id="fdddb-101">New-AzHDInsightClusterAutoscaleScheduleCondition</span><span class="sxs-lookup"><span data-stu-id="fdddb-101">New-AzHDInsightClusterAutoscaleScheduleCondition</span></span>

## <span data-ttu-id="fdddb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fdddb-102">SYNOPSIS</span></span>
<span data-ttu-id="fdddb-103">일정 기반 자동 조정 조건을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fdddb-103">Creates Schedule-based autoscale condition.</span></span>

## <span data-ttu-id="fdddb-104">구문</span><span class="sxs-lookup"><span data-stu-id="fdddb-104">SYNTAX</span></span>

```
New-AzHDInsightClusterAutoscaleScheduleCondition -Time <DateTime> -WorkerNodeCount <Int32>
 -Day <AzureHDInsightDaysOfWeek[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fdddb-105">설명</span><span class="sxs-lookup"><span data-stu-id="fdddb-105">DESCRIPTION</span></span>
<span data-ttu-id="fdddb-106">**New-AzHDInsightClusterAutoscaleScheduleCondition cmdlet은** Schedule 기반 자동 크기 조정 조건을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fdddb-106">The **New-AzHDInsightClusterAutoscaleScheduleCondition** cmdlet creates Schedule-based autoscale condition.</span></span>

## <span data-ttu-id="fdddb-107">예제</span><span class="sxs-lookup"><span data-stu-id="fdddb-107">EXAMPLES</span></span>

### <span data-ttu-id="fdddb-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="fdddb-108">Example 1</span></span>
```powershell
PS C:\> New-AzHDInsightClusterAutoscaleScheduleCondition -Time 09:00 -WorkerNodeCount 5 -Day Monday,Wednesday
```

<span data-ttu-id="fdddb-109">이 명령은 매주 월요일, 수요일 09:00에 클러스터가 5개 작업 노드로 자동 조정되는 조건을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fdddb-109">This command creates a condition where cluster autoscale to 5 worker nodes at 09:00 every Monday, Wednesday.</span></span>

### <span data-ttu-id="fdddb-110">예제 2: 자동 조정 조건으로 클러스터의 일정 기반 자동 조정을 사용하도록 설정</span><span class="sxs-lookup"><span data-stu-id="fdddb-110">Example 2: Enable Schedule-based autoscale of a cluster with autoscale condition.</span></span>
```powershell
# create a autoscale condition
PS C:\> $condition=New-AzHDInsightClusterAutoscaleScheduleCondition -Time 09:00 -WorkerNodeCount 5 -Day Monday,Wednesday

# Set the cluster autoscale configuration
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Set-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName -Schedule -TimeZone "Pacific Standard Time" -Condition $condition
```

<span data-ttu-id="fdddb-111">이 명령은 매주 월요일, 수요일 09:00에 클러스터가 5개 작업 노드로 자동 조정되는 조건을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fdddb-111">This command creates a condition where cluster autoscale to 5 worker nodes at 09:00 every Monday, Wednesday.</span></span>

## <span data-ttu-id="fdddb-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fdddb-112">PARAMETERS</span></span>

### <span data-ttu-id="fdddb-113">-Day</span><span class="sxs-lookup"><span data-stu-id="fdddb-113">-Day</span></span>
<span data-ttu-id="fdddb-114">자동 조정 일정 조건을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="fdddb-114">Gets or sets the days of Autoscale schedule condition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightDaysOfWeek[]
Parameter Sets: (All)
Aliases:
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdddb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdddb-115">-DefaultProfile</span></span>
<span data-ttu-id="fdddb-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fdddb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdddb-117">-Time</span><span class="sxs-lookup"><span data-stu-id="fdddb-117">-Time</span></span>
<span data-ttu-id="fdddb-118">자동 조정 일정 조건을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="fdddb-118">Gets or sets the time of Autoscale schedule condition.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdddb-119">-WorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="fdddb-119">-WorkerNodeCount</span></span>
<span data-ttu-id="fdddb-120">자동 조정 일정 조건의 일정 Workernode 수를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="fdddb-120">Gets or sets the schedule workernode count of Autoscale schedule condition.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdddb-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdddb-121">CommonParameters</span></span>
<span data-ttu-id="fdddb-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fdddb-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdddb-123">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fdddb-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdddb-124">입력</span><span class="sxs-lookup"><span data-stu-id="fdddb-124">INPUTS</span></span>

### <span data-ttu-id="fdddb-125">없음</span><span class="sxs-lookup"><span data-stu-id="fdddb-125">None</span></span>

## <span data-ttu-id="fdddb-126">출력</span><span class="sxs-lookup"><span data-stu-id="fdddb-126">OUTPUTS</span></span>

### <span data-ttu-id="fdddb-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition</span><span class="sxs-lookup"><span data-stu-id="fdddb-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition</span></span>

## <span data-ttu-id="fdddb-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fdddb-128">NOTES</span></span>

## <span data-ttu-id="fdddb-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fdddb-129">RELATED LINKS</span></span>

<span data-ttu-id="fdddb-130">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="fdddb-130">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
