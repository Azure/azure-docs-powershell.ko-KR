---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 86276DF3-95E2-405F-BA46-F188B7AE3B9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleConfiguration.md
ms.openlocfilehash: c2d8e3c2f3da4ebd2d07d16965a24878af34e262
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215364"
---
# <span data-ttu-id="89600-101">New-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="89600-101">New-AzHDInsightClusterAutoscaleConfiguration</span></span>

## <span data-ttu-id="89600-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89600-102">SYNOPSIS</span></span>
<span data-ttu-id="89600-103">Azure HDInsight 클러스터의 자동 크기 조정 구성을 설명 하는 비지속형 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="89600-103">Creates a non-persisted object that describes the autoscale configuration of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="89600-104">구문과</span><span class="sxs-lookup"><span data-stu-id="89600-104">SYNTAX</span></span>

### <span data-ttu-id="89600-105">LoadAutoscaleParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="89600-105">LoadAutoscaleParameterSet (Default)</span></span>
```
New-AzHDInsightClusterAutoscaleConfiguration -MinWorkerNodeCount <Int32> -MaxWorkerNodeCount <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89600-106">ScheduleAutoscaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="89600-106">ScheduleAutoscaleParameterSet</span></span>
```
New-AzHDInsightClusterAutoscaleConfiguration -TimeZone <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89600-107">설명은</span><span class="sxs-lookup"><span data-stu-id="89600-107">DESCRIPTION</span></span>
<span data-ttu-id="89600-108">Cmdlet **AzHDInsightClusterAutoscaleConfiguration** 는 Azure HDInsight 클러스터의 자동 크기 조정 구성을 설명 하는 비지속형 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="89600-108">The cmdlet **New-AzHDInsightClusterAutoscaleConfiguration** creates a non-persisted object that describes the autoscale configuration of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="89600-109">예제의</span><span class="sxs-lookup"><span data-stu-id="89600-109">EXAMPLES</span></span>

### <span data-ttu-id="89600-110">예제 1: 부하 기반 자동 크기 조정 구성을 설명 하는 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="89600-110">Example 1: Create an object which describes Load-based autoscale configuration</span></span>
```powershell
PS C:\> New-AzHDInsightClusterAutoscaleConfiguration -MinWorkerNodeCount 3 -MaxWorkerNodeCount 5
```

<span data-ttu-id="89600-111">이 명령은 부하 기반 자동 크기 조정 구성을 설명 하는 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="89600-111">This command creates an object which describes Load-based autoscale configuration.</span></span>

### <span data-ttu-id="89600-112">예제 2: 일정 기반 자동 크기 조정 구성을 설명 하는 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="89600-112">Example 2: Create an object which describes Schedule-based autoscale configuration</span></span>
```powershell
# Create an autoscale condition firstly
PS C:\> $condition=New-AzHDInsightClusterAutoscaleScheduleCondition -Day Monday -Time 09:00 -WorkerNodeCount 5
PS C:\> New-AzHDInsightClusterAutoscaleConfiguration -TimeZone ([System.TimeZoneInfo]::Local).Id `
        -Condition $condition
```

<span data-ttu-id="89600-113">이 명령은 일정 기반 자동 크기 조정 구성을 설명 하는 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="89600-113">This command creates an object which describes Schedule-based autoscale configuration.</span></span>

## <span data-ttu-id="89600-114">변수</span><span class="sxs-lookup"><span data-stu-id="89600-114">PARAMETERS</span></span>

### <span data-ttu-id="89600-115">-조건</span><span class="sxs-lookup"><span data-stu-id="89600-115">-Condition</span></span>
<span data-ttu-id="89600-116">일정 기반 자동 크기 조정 조건을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89600-116">Gets or sets the condition of schedule-based autoscale.</span></span>

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

### <span data-ttu-id="89600-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89600-117">-DefaultProfile</span></span>
<span data-ttu-id="89600-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="89600-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89600-119">-MaxWorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="89600-119">-MaxWorkerNodeCount</span></span>
<span data-ttu-id="89600-120">부하 기반 자동 크기 조정의 최대 작업 노드 수를 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89600-120">Gets or sets the maximal workernode count of load-based autoscale.</span></span>

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

### <span data-ttu-id="89600-121">-MinWorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="89600-121">-MinWorkerNodeCount</span></span>
<span data-ttu-id="89600-122">부하 기반 자동 크기 조정의 최소 작업 노드 수를 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89600-122">Gets or sets the minimal workernode count of load-based autoscale.</span></span>

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

### <span data-ttu-id="89600-123">-표준 시간대</span><span class="sxs-lookup"><span data-stu-id="89600-123">-TimeZone</span></span>
<span data-ttu-id="89600-124">일정 기반 자동 크기 조정의 표준 시간대를 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89600-124">Gets or sets the time zone of schedule-based autoscale.</span></span>

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

### <span data-ttu-id="89600-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89600-125">CommonParameters</span></span>
<span data-ttu-id="89600-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="89600-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89600-127">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="89600-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89600-128">입력</span><span class="sxs-lookup"><span data-stu-id="89600-128">INPUTS</span></span>

### <span data-ttu-id="89600-129">않아야</span><span class="sxs-lookup"><span data-stu-id="89600-129">None</span></span>

## <span data-ttu-id="89600-130">출력</span><span class="sxs-lookup"><span data-stu-id="89600-130">OUTPUTS</span></span>

### <span data-ttu-id="89600-131">AzureHDInsightAutoscale의. m m.</span><span class="sxs-lookup"><span data-stu-id="89600-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale</span></span>

## <span data-ttu-id="89600-132">상속자</span><span class="sxs-lookup"><span data-stu-id="89600-132">NOTES</span></span>

## <span data-ttu-id="89600-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="89600-133">RELATED LINKS</span></span>

<span data-ttu-id="89600-134">[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md) 
 [제거-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="89600-134">[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)
[Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md)
[Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
