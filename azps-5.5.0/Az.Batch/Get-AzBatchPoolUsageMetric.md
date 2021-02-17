---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 4B373447-3078-4C1F-932E-8337AB170DEB
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchpoolusagemetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolUsageMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolUsageMetric.md
ms.openlocfilehash: 1700e20318a502f32386638f94a9c5c86c271d7d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205253"
---
# <span data-ttu-id="854d3-101">Get-AzBatchPoolUsageMetric</span><span class="sxs-lookup"><span data-stu-id="854d3-101">Get-AzBatchPoolUsageMetric</span></span>

## <span data-ttu-id="854d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="854d3-102">SYNOPSIS</span></span>
<span data-ttu-id="854d3-103">Batch 계정에 대한 풀 사용 메트릭을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="854d3-103">Gets pool usage metrics for a Batch account.</span></span>

## <span data-ttu-id="854d3-104">구문</span><span class="sxs-lookup"><span data-stu-id="854d3-104">SYNTAX</span></span>

```
Get-AzBatchPoolUsageMetric [-StartTime <DateTime>] [-EndTime <DateTime>] [-Filter <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="854d3-105">설명</span><span class="sxs-lookup"><span data-stu-id="854d3-105">DESCRIPTION</span></span>
<span data-ttu-id="854d3-106">**Get-AzBatchPoolUsageMetric** cmdlet은 지정된 계정에 대한 개별 시간 간격 동안 풀에 의해 집계된 사용 메트릭을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="854d3-106">The **Get-AzBatchPoolUsageMetric** cmdlet gets the usage metrics, aggregated by pool across individual time intervals, for the specified account.</span></span>
<span data-ttu-id="854d3-107">특정 풀 및 시간 범위에 대한 통계를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="854d3-107">You can get the statistics for a specific pool and for a time range.</span></span>

## <span data-ttu-id="854d3-108">예제</span><span class="sxs-lookup"><span data-stu-id="854d3-108">EXAMPLES</span></span>

### <span data-ttu-id="854d3-109">예제 1: 시간 범위에 대한 풀 사용 메트릭을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="854d3-109">Example 1: Get pool usage metrics for a time range</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> $StartTime = Get-Date -Date "2016-05-16 00:00:00Z"
PS C:\> $EndTime = Get-Date -Date "2016-05-16 01:00:00Z"
PS C:\> Get-AzBatchPoolUsageMetric -StartTime $StartTime -EndTime $EndTime -BatchContext $context
DataEgressGiB      : 6.68875873088837E-06
DataIngressGiB     : 1.9485130906105E-05
EndTime            : 5/16/2016 12:30:00 AM
PoolId             : testpool1
StartTime          : 5/16/2016 12:00:00 AM
TotalCoreHours     : 8
VirtualMachineSize : standard_d4

DataEgressGiB      : 5.61587512493134E-06
DataIngressGiB     : 1.76150351762772E-05
EndTime            : 5/16/2016 12:30:00 AM
PoolId             : testpool2
StartTime          : 5/16/2016 12:00:00 AM
TotalCoreHours     : 12
VirtualMachineSize : standard_d4

DataEgressGiB      : 7.36676156520844E-06
DataIngressGiB     : 2.10804864764214E-05
EndTime            : 5/16/2016 1:00:00 AM
PoolId             : testpool1
StartTime          : 5/16/2016 12:30:00 AM
TotalCoreHours     : 7.99999999955555
VirtualMachineSize : standard_d4

DataEgressGiB      : 5.80586493015289E-06
DataIngressGiB     : 1.80602073669434E-05
EndTime            : 5/16/2016 1:00:00 AM
PoolId             : testpool2
StartTime          : 5/16/2016 12:30:00 AM
TotalCoreHours     : 11.9999999993333
VirtualMachineSize : standard_d4
```

<span data-ttu-id="854d3-110">첫 번째 명령은 **Get-AzBatchAccountKey를** 사용하여 ContosoBatchAccount라는 배치 계정에 대한 계정 키에 대한 개체 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="854d3-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="854d3-111">이 명령은 이 개체 참조를 $Context 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="854d3-111">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="854d3-112">다음 두 명령은 Get-Date cmdlet을 사용하여 **DateTime** 개체를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="854d3-112">The next two commands create **DateTime** objects by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="854d3-113">명령은 최종 명령에 사용할 $StartTime $EndTime 변수에 이러한 값을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="854d3-113">The commands store these values in the $StartTime and $EndTime variables for use with the final command.</span></span>
<span data-ttu-id="854d3-114">마지막 명령은 지정된 시작 및 종료 시간 사이의 시간 간격에 따라 풀별로 집계된 모든 풀 사용 메트릭을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="854d3-114">The final command returns all of the pool usage metrics, aggregated by pool, across time interval between the specified start and end times.</span></span>

### <span data-ttu-id="854d3-115">예제 2: 필터를 사용하여 풀 사용 메트릭을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="854d3-115">Example 2: Get pool usage metrics by using a filter</span></span>
```
PS C:\>Get-AzBatchPoolUsageMetric -Filter "poolId eq 'ContosoPool'" -BatchContext $Context
DataEgressGiB      : 9.0496614575386E-06
DataIngressGiB     : 2.60043889284134E-05
EndTime            : 5/16/2016 5:30:00 PM
PoolId             : MyPool
StartTime          : 5/16/2016 5:00:00 PM
TotalCoreHours     : 12
VirtualMachineSize : standard_d4
```

<span data-ttu-id="854d3-116">이 명령은 ContosoPool이라는 풀에 대한 사용 메트릭을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="854d3-116">This command returns the usage metrics for pool named ContosoPool.</span></span>
<span data-ttu-id="854d3-117">이 명령은 해당 풀을 지정하는 필터 문자열을 지정하고 이전 예제와 $Context 값을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="854d3-117">The command specifies a filter string to specify that pool, and uses the same $Context value as the previous example.</span></span>

## <span data-ttu-id="854d3-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="854d3-118">PARAMETERS</span></span>

### <span data-ttu-id="854d3-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="854d3-119">-BatchContext</span></span>
<span data-ttu-id="854d3-120">이 cmdlet이 Batch 서비스와 상호 작용하는 데 사용하는 **BatchAccountContext** 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="854d3-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="854d3-121">Get-AzBatchAccount cmdlet을 사용하여 BatchAccountContext를 얻을 경우 Batch 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="854d3-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="854d3-122">대신 공유 키 인증을 사용 Get-AzBatchAccountKey 키가 채워진 BatchAccountContext 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="854d3-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="854d3-123">공유 키 인증을 사용하는 경우 기본 액세스 키가 기본적으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="854d3-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="854d3-124">사용할 키를 변경하기 위해 BatchAccountContext.KeyInUse 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="854d3-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="854d3-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="854d3-125">-DefaultProfile</span></span>
<span data-ttu-id="854d3-126">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="854d3-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="854d3-127">-EndTime</span><span class="sxs-lookup"><span data-stu-id="854d3-127">-EndTime</span></span>
<span data-ttu-id="854d3-128">이 cmdlet이 사용 메트릭을 얻을 시간 범위의 끝을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="854d3-128">Specifies the end of a time range for which this cmdlet gets usage metrics.</span></span>
<span data-ttu-id="854d3-129">최소 2시간 전에 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="854d3-129">Specify a time at least two hours earlier.</span></span>
<span data-ttu-id="854d3-130">종료 시간을 지정하지 않으면 이 cmdlet은 현재 사용 가능한 마지막 집계 간격을 사용하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="854d3-130">If you do not specify an end time, this cmdlet uses the last aggregation interval currently available.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="854d3-131">-Filter</span><span class="sxs-lookup"><span data-stu-id="854d3-131">-Filter</span></span>
<span data-ttu-id="854d3-132">이 cmdlet이 반환하는 메트릭을 필터링하는 데 사용할 OData 필터 절을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="854d3-132">Specifies an OData filter clause to use to filter the metrics that this cmdlet returns.</span></span>
<span data-ttu-id="854d3-133">유일한 유효한 속성은 **문자열 값이 있는 poolId입니다.**</span><span class="sxs-lookup"><span data-stu-id="854d3-133">The only valid property is **poolId** with a string value.</span></span>
<span data-ttu-id="854d3-134">가능한 작업은 eq, ge, gt, le, lt, startswith입니다.</span><span class="sxs-lookup"><span data-stu-id="854d3-134">Possible operations are the following: eq, ge, gt, le, lt, startswith.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="854d3-135">-StartTime</span><span class="sxs-lookup"><span data-stu-id="854d3-135">-StartTime</span></span>
<span data-ttu-id="854d3-136">이 cmdlet이 사용 메트릭을 얻을 시간 범위의 시작을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="854d3-136">Specifies the start of a time range for which this cmdlet gets usage metrics.</span></span>
<span data-ttu-id="854d3-137">최소 2시간 반 전에 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="854d3-137">Specify a time at least two and a half hours earlier.</span></span>
<span data-ttu-id="854d3-138">시작 시간을 지정하지 않으면 이 cmdlet은 현재 사용할 수 있는 마지막 집계 간격을 사용하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="854d3-138">If you do not specify a start time, this cmdlet uses the last aggregation interval currently available.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="854d3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="854d3-139">CommonParameters</span></span>
<span data-ttu-id="854d3-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="854d3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="854d3-141">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="854d3-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="854d3-142">입력</span><span class="sxs-lookup"><span data-stu-id="854d3-142">INPUTS</span></span>

### <span data-ttu-id="854d3-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="854d3-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="854d3-144">출력</span><span class="sxs-lookup"><span data-stu-id="854d3-144">OUTPUTS</span></span>

### <span data-ttu-id="854d3-145">Microsoft.Azure.Commands.Batch. Models.PSPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="854d3-145">Microsoft.Azure.Commands.Batch.Models.PSPoolUsageMetrics</span></span>

## <span data-ttu-id="854d3-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="854d3-146">NOTES</span></span>

## <span data-ttu-id="854d3-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="854d3-147">RELATED LINKS</span></span>

[<span data-ttu-id="854d3-148">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="854d3-148">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="854d3-149">Get-AzBatchPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="854d3-149">Get-AzBatchPoolStatistics</span></span>](./Get-AzBatchPoolStatistic.md)

[<span data-ttu-id="854d3-150">Get-AzBatchJobStatistics</span><span class="sxs-lookup"><span data-stu-id="854d3-150">Get-AzBatchJobStatistics</span></span>](./Get-AzBatchJobStatistic.md)
