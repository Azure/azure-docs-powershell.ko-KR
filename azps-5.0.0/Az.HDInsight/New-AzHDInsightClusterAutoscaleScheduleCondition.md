---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 86276DF3-95E2-405F-BA46-F188B7AE3B9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterautoscaleschedulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleScheduleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleScheduleCondition.md
ms.openlocfilehash: 4f046344942e244d6bd220034f7cbe85c48681ef
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215363"
---
# <span data-ttu-id="ea500-101">New-AzHDInsightClusterAutoscaleScheduleCondition</span><span class="sxs-lookup"><span data-stu-id="ea500-101">New-AzHDInsightClusterAutoscaleScheduleCondition</span></span>

## <span data-ttu-id="ea500-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea500-102">SYNOPSIS</span></span>
<span data-ttu-id="ea500-103">일정 기반 자동 크기 조정 조건을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ea500-103">Creates Schedule-based autoscale condition.</span></span>

## <span data-ttu-id="ea500-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ea500-104">SYNTAX</span></span>

```
New-AzHDInsightClusterAutoscaleScheduleCondition -Time <DateTime> -WorkerNodeCount <Int32>
 -Day <AzureHDInsightDaysOfWeek[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea500-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ea500-105">DESCRIPTION</span></span>
<span data-ttu-id="ea500-106">**AzHDInsightClusterAutoscaleScheduleCondition** Cmdlet은 일정 기반 자동 크기 조정 조건을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ea500-106">The **New-AzHDInsightClusterAutoscaleScheduleCondition** cmdlet creates Schedule-based autoscale condition.</span></span>

## <span data-ttu-id="ea500-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ea500-107">EXAMPLES</span></span>

### <span data-ttu-id="ea500-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ea500-108">Example 1</span></span>
```powershell
PS C:\> New-AzHDInsightClusterAutoscaleScheduleCondition -Time 09:00 -WorkerNodeCount 5 -Day Monday,Wednesday
```

<span data-ttu-id="ea500-109">이 명령은 매 월요일, 수요일 09:00의 5 개 작업자 노드에 대 한 클러스터의 크기를 조정 하는 조건을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ea500-109">This command creates a condition where cluster autoscale to 5 worker nodes at 09:00 every Monday, Wednesday.</span></span>

### <span data-ttu-id="ea500-110">예제 2: 자동 크기 조정 조건으로 클러스터의 일정 기반 자동 크기 조정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea500-110">Example 2: Enable Schedule-based autoscale of a cluster with autoscale condition.</span></span>
```powershell
# create a autoscale condition
PS C:\> $condition=New-AzHDInsightClusterAutoscaleScheduleCondition -Time 09:00 -WorkerNodeCount 5 -Day Monday,Wednesday

# Set the cluster autoscale configuration
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Set-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName -Schedule -TimeZone "Pacific Standard Time" -Condition $condition
```

<span data-ttu-id="ea500-111">이 명령은 매 월요일, 수요일 09:00의 5 개 작업자 노드에 대 한 클러스터의 크기를 조정 하는 조건을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ea500-111">This command creates a condition where cluster autoscale to 5 worker nodes at 09:00 every Monday, Wednesday.</span></span>

## <span data-ttu-id="ea500-112">변수</span><span class="sxs-lookup"><span data-stu-id="ea500-112">PARAMETERS</span></span>

### <span data-ttu-id="ea500-113">일</span><span class="sxs-lookup"><span data-stu-id="ea500-113">-Day</span></span>
<span data-ttu-id="ea500-114">자동 크기 조정 일정 조건의 날짜를 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea500-114">Gets or sets the days of Autoscale schedule condition.</span></span>

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

### <span data-ttu-id="ea500-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea500-115">-DefaultProfile</span></span>
<span data-ttu-id="ea500-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ea500-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea500-117">타임</span><span class="sxs-lookup"><span data-stu-id="ea500-117">-Time</span></span>
<span data-ttu-id="ea500-118">자동 크기 조정 일정 조건의 시간을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea500-118">Gets or sets the time of Autoscale schedule condition.</span></span>

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

### <span data-ttu-id="ea500-119">-WorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="ea500-119">-WorkerNodeCount</span></span>
<span data-ttu-id="ea500-120">자동 크기 조정 일정 조건의 일정 노드 수를 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea500-120">Gets or sets the schedule workernode count of Autoscale schedule condition.</span></span>

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

### <span data-ttu-id="ea500-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea500-121">CommonParameters</span></span>
<span data-ttu-id="ea500-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea500-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea500-123">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ea500-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea500-124">입력</span><span class="sxs-lookup"><span data-stu-id="ea500-124">INPUTS</span></span>

### <span data-ttu-id="ea500-125">않아야</span><span class="sxs-lookup"><span data-stu-id="ea500-125">None</span></span>

## <span data-ttu-id="ea500-126">출력</span><span class="sxs-lookup"><span data-stu-id="ea500-126">OUTPUTS</span></span>

### <span data-ttu-id="ea500-127">AzureHDInsightAutoscaleCondition의. m m.</span><span class="sxs-lookup"><span data-stu-id="ea500-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition</span></span>

## <span data-ttu-id="ea500-128">상속자</span><span class="sxs-lookup"><span data-stu-id="ea500-128">NOTES</span></span>

## <span data-ttu-id="ea500-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ea500-129">RELATED LINKS</span></span>

<span data-ttu-id="ea500-130">[새로운 AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ea500-130">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
