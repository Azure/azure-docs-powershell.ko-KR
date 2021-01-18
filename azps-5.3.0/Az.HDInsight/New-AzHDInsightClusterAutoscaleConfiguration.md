---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 86276DF3-95E2-405F-BA46-F188B7AE3B9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleConfiguration.md
ms.openlocfilehash: c2d8e3c2f3da4ebd2d07d16965a24878af34e262
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492944"
---
# <span data-ttu-id="c044f-101">New-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="c044f-101">New-AzHDInsightClusterAutoscaleConfiguration</span></span>

## <span data-ttu-id="c044f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c044f-102">SYNOPSIS</span></span>
<span data-ttu-id="c044f-103">Azure HDInsight 클러스터의 자동 조정 구성을 설명하는 지속되지 않는 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c044f-103">Creates a non-persisted object that describes the autoscale configuration of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="c044f-104">구문</span><span class="sxs-lookup"><span data-stu-id="c044f-104">SYNTAX</span></span>

### <span data-ttu-id="c044f-105">LoadAutoscaleParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="c044f-105">LoadAutoscaleParameterSet (Default)</span></span>
```
New-AzHDInsightClusterAutoscaleConfiguration -MinWorkerNodeCount <Int32> -MaxWorkerNodeCount <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c044f-106">ScheduleAutoscaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="c044f-106">ScheduleAutoscaleParameterSet</span></span>
```
New-AzHDInsightClusterAutoscaleConfiguration -TimeZone <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c044f-107">설명</span><span class="sxs-lookup"><span data-stu-id="c044f-107">DESCRIPTION</span></span>
<span data-ttu-id="c044f-108">**New-AzHDInsightClusterAutoscaleConfiguration** cmdlet은 Azure HDInsight 클러스터의 자동 크기 조정 구성을 설명하는 비 지속형 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c044f-108">The cmdlet **New-AzHDInsightClusterAutoscaleConfiguration** creates a non-persisted object that describes the autoscale configuration of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="c044f-109">예제</span><span class="sxs-lookup"><span data-stu-id="c044f-109">EXAMPLES</span></span>

### <span data-ttu-id="c044f-110">예제 1: 부하 기반 자동 조정 구성을 설명하는 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="c044f-110">Example 1: Create an object which describes Load-based autoscale configuration</span></span>
```powershell
PS C:\> New-AzHDInsightClusterAutoscaleConfiguration -MinWorkerNodeCount 3 -MaxWorkerNodeCount 5
```

<span data-ttu-id="c044f-111">이 명령은 부하 기반 자동 조정 구성을 설명하는 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c044f-111">This command creates an object which describes Load-based autoscale configuration.</span></span>

### <span data-ttu-id="c044f-112">예제 2: 일정 기반 자동 조정 구성을 설명하는 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="c044f-112">Example 2: Create an object which describes Schedule-based autoscale configuration</span></span>
```powershell
# Create an autoscale condition firstly
PS C:\> $condition=New-AzHDInsightClusterAutoscaleScheduleCondition -Day Monday -Time 09:00 -WorkerNodeCount 5
PS C:\> New-AzHDInsightClusterAutoscaleConfiguration -TimeZone ([System.TimeZoneInfo]::Local).Id `
        -Condition $condition
```

<span data-ttu-id="c044f-113">이 명령은 일정 기반 자동 조정 구성을 설명하는 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c044f-113">This command creates an object which describes Schedule-based autoscale configuration.</span></span>

## <span data-ttu-id="c044f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c044f-114">PARAMETERS</span></span>

### <span data-ttu-id="c044f-115">-Condition</span><span class="sxs-lookup"><span data-stu-id="c044f-115">-Condition</span></span>
<span data-ttu-id="c044f-116">일정 기반 자동 조정의 조건을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="c044f-116">Gets or sets the condition of schedule-based autoscale.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]
Parameter Sets: ScheduleAutoscaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c044f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c044f-117">-DefaultProfile</span></span>
<span data-ttu-id="c044f-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c044f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c044f-119">-MaxWorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="c044f-119">-MaxWorkerNodeCount</span></span>
<span data-ttu-id="c044f-120">부하 기반 자동 조정의 최대 worknode 수를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="c044f-120">Gets or sets the maximal workernode count of load-based autoscale.</span></span>

```yaml
Type: System.Int32
Parameter Sets: LoadAutoscaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c044f-121">-MinWorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="c044f-121">-MinWorkerNodeCount</span></span>
<span data-ttu-id="c044f-122">부하 기반 자동 조정의 최소 Workernode 수를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="c044f-122">Gets or sets the minimal workernode count of load-based autoscale.</span></span>

```yaml
Type: System.Int32
Parameter Sets: LoadAutoscaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c044f-123">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="c044f-123">-TimeZone</span></span>
<span data-ttu-id="c044f-124">일정 기반 자동 조정의 표준 시간대를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="c044f-124">Gets or sets the time zone of schedule-based autoscale.</span></span>

```yaml
Type: System.String
Parameter Sets: ScheduleAutoscaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c044f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c044f-125">CommonParameters</span></span>
<span data-ttu-id="c044f-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c044f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c044f-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c044f-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c044f-128">입력</span><span class="sxs-lookup"><span data-stu-id="c044f-128">INPUTS</span></span>

### <span data-ttu-id="c044f-129">없음</span><span class="sxs-lookup"><span data-stu-id="c044f-129">None</span></span>

## <span data-ttu-id="c044f-130">출력</span><span class="sxs-lookup"><span data-stu-id="c044f-130">OUTPUTS</span></span>

### <span data-ttu-id="c044f-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale</span><span class="sxs-lookup"><span data-stu-id="c044f-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale</span></span>

## <span data-ttu-id="c044f-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c044f-132">NOTES</span></span>

## <span data-ttu-id="c044f-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c044f-133">RELATED LINKS</span></span>

<span data-ttu-id="c044f-134">[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="c044f-134">[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)
[Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md)
[Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
