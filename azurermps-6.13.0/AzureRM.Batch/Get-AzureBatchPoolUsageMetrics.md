---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 4B373447-3078-4C1F-932E-8337AB170DEB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchpoolusagemetrics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPoolUsageMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPoolUsageMetrics.md
ms.openlocfilehash: 881e5d1cbd188589f4e0e28384ecf926b3495233
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703177"
---
# <span data-ttu-id="0ba0e-101">Get-AzureBatchPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="0ba0e-101">Get-AzureBatchPoolUsageMetrics</span></span>

## <span data-ttu-id="0ba0e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ba0e-102">SYNOPSIS</span></span>
<span data-ttu-id="0ba0e-103">일괄 처리 계정에 대 한 풀 사용 메트릭을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0ba0e-103">Gets pool usage metrics for a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ba0e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0ba0e-104">SYNTAX</span></span>

```
Get-AzureBatchPoolUsageMetrics [-StartTime <DateTime>] [-EndTime <DateTime>] [-Filter <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ba0e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0ba0e-105">DESCRIPTION</span></span>
<span data-ttu-id="0ba0e-106">**AzureBatchPoolUsageMetrics** cmdlet은 지정 된 계정에 대해 개별 시간 간격을 기준으로 집계 된 사용 메트릭을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0ba0e-106">The **Get-AzureBatchPoolUsageMetrics** cmdlet gets the usage metrics, aggregated by pool across individual time intervals, for the specified account.</span></span>
<span data-ttu-id="0ba0e-107">특정 풀 및 시간 범위에 대 한 통계를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0ba0e-107">You can get the statistics for a specific pool and for a time range.</span></span>

## <span data-ttu-id="0ba0e-108">예제의</span><span class="sxs-lookup"><span data-stu-id="0ba0e-108">EXAMPLES</span></span>

### <span data-ttu-id="0ba0e-109">예제 1: 시간 범위에 대 한 풀 사용 메트릭 가져오기</span><span class="sxs-lookup"><span data-stu-id="0ba0e-109">Example 1: Get pool usage metrics for a time range</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $StartTime = Get-Date -Date "2016-05-16 00:00:00Z"
PS C:\> $EndTime = Get-Date -Date "2016-05-16 01:00:00Z"
PS C:\> Get-AzureBatchPoolUsageMetrics -StartTime $StartTime -EndTime $EndTime -BatchContext $context
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

<span data-ttu-id="0ba0e-110">첫 번째 명령은 **Get-AzureRmBatchAccountKeys** 를 사용 하 여 ContosoBatchAccount 라는 일괄 계정에 대 한 계정 키에 대 한 개체 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0ba0e-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="0ba0e-111">명령이이 개체 참조를 $Context 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ba0e-111">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="0ba0e-112">다음 두 명령은 Get-Date cmdlet을 사용 하 여 **DateTime** 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0ba0e-112">The next two commands create **DateTime** objects by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="0ba0e-113">명령에서는 이러한 값을 $StartTime 및 $EndTime 변수에 저장 하 고 마지막 명령에 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ba0e-113">The commands store these values in the $StartTime and $EndTime variables for use with the final command.</span></span>
<span data-ttu-id="0ba0e-114">마지막 명령은 지정 된 시작 시간과 종료 시간 사이의 시간 간격에 따라 풀을 기준으로 집계 된 모든 풀 사용 메트릭을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ba0e-114">The final command returns all of the pool usage metrics, aggregated by pool, across time interval between the specified start and end times.</span></span>

### <span data-ttu-id="0ba0e-115">예제 2: 필터를 사용 하 여 풀 사용 메트릭 가져오기</span><span class="sxs-lookup"><span data-stu-id="0ba0e-115">Example 2: Get pool usage metrics by using a filter</span></span>
```
PS C:\>Get-AzureBatchPoolUsageMetrics -Filter "poolId eq 'ContosoPool'" -BatchContext $Context
DataEgressGiB      : 9.0496614575386E-06
DataIngressGiB     : 2.60043889284134E-05
EndTime            : 5/16/2016 5:30:00 PM
PoolId             : MyPool
StartTime          : 5/16/2016 5:00:00 PM
TotalCoreHours     : 12
VirtualMachineSize : standard_d4
```

<span data-ttu-id="0ba0e-116">이 명령은 ContosoPool 이라는 풀에 대 한 사용 메트릭을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ba0e-116">This command returns the usage metrics for pool named ContosoPool.</span></span>
<span data-ttu-id="0ba0e-117">명령은 해당 풀을 지정 하는 필터 문자열을 지정 하 고 이전 예제와 동일한 $Context 값을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ba0e-117">The command specifies a filter string to specify that pool, and uses the same $Context value as the previous example.</span></span>

## <span data-ttu-id="0ba0e-118">변수</span><span class="sxs-lookup"><span data-stu-id="0ba0e-118">PARAMETERS</span></span>

### <span data-ttu-id="0ba0e-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="0ba0e-119">-BatchContext</span></span>
<span data-ttu-id="0ba0e-120">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ba0e-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="0ba0e-121">Get-AzureRmBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0ba0e-121">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="0ba0e-122">대신 공유 키 인증을 사용 하려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0ba0e-122">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="0ba0e-123">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0ba0e-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="0ba0e-124">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ba0e-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="0ba0e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ba0e-125">-DefaultProfile</span></span>
<span data-ttu-id="0ba0e-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0ba0e-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ba0e-127">-EndTime</span><span class="sxs-lookup"><span data-stu-id="0ba0e-127">-EndTime</span></span>
<span data-ttu-id="0ba0e-128">이 cmdlet이 사용 메트릭을 가져오는 시간 범위의 끝을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ba0e-128">Specifies the end of a time range for which this cmdlet gets usage metrics.</span></span>
<span data-ttu-id="0ba0e-129">시간을 2 시간 이상으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ba0e-129">Specify a time at least two hours earlier.</span></span>
<span data-ttu-id="0ba0e-130">종료 시간을 지정 하지 않으면이 cmdlet은 현재 사용 가능한 마지막 집계 간격을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ba0e-130">If you do not specify an end time, this cmdlet uses the last aggregation interval currently available.</span></span>

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

### <span data-ttu-id="0ba0e-131">-필터</span><span class="sxs-lookup"><span data-stu-id="0ba0e-131">-Filter</span></span>
<span data-ttu-id="0ba0e-132">이 cmdlet이 retruns 하는 메트릭을 필터링 하는 데 사용할 OData 필터 절을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ba0e-132">Specifies an OData filter clause to use to filter the metrics that this cmdlet retruns.</span></span>
<span data-ttu-id="0ba0e-133">유일한 유효한 속성은 문자열 값으로 **poolId** 입니다.</span><span class="sxs-lookup"><span data-stu-id="0ba0e-133">The only valid property is **poolId** with a string value.</span></span>
<span data-ttu-id="0ba0e-134">사용할 수 있는 작업은 eq, ge, gt, le, lt, startswith입니다.</span><span class="sxs-lookup"><span data-stu-id="0ba0e-134">Possible operations are the following: eq, ge, gt, le, lt, startswith.</span></span>

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

### <span data-ttu-id="0ba0e-135">-StartTime</span><span class="sxs-lookup"><span data-stu-id="0ba0e-135">-StartTime</span></span>
<span data-ttu-id="0ba0e-136">이 cmdlet이 사용 메트릭을 가져오는 시간 범위의 시작을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ba0e-136">Specifies the start of a time range for which this cmdlet gets usage metrics.</span></span>
<span data-ttu-id="0ba0e-137">시간을 최소 2 분에서 0.5 시간으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ba0e-137">Specify a time at least two and a half hours earlier.</span></span>
<span data-ttu-id="0ba0e-138">시작 시간을 지정 하지 않으면이 cmdlet은 현재 사용 가능한 마지막 집계 간격을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ba0e-138">If you do not specify a start time, this cmdlet uses the last aggregation interval currently available.</span></span>

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

### <span data-ttu-id="0ba0e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ba0e-139">CommonParameters</span></span>
<span data-ttu-id="0ba0e-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ba0e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ba0e-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ba0e-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ba0e-142">입력</span><span class="sxs-lookup"><span data-stu-id="0ba0e-142">INPUTS</span></span>

### <span data-ttu-id="0ba0e-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="0ba0e-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="0ba0e-144">매개 변수: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0ba0e-144">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="0ba0e-145">출력</span><span class="sxs-lookup"><span data-stu-id="0ba0e-145">OUTPUTS</span></span>

### <span data-ttu-id="0ba0e-146">Microsoft.Azure.Commands.Batch. PSPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="0ba0e-146">Microsoft.Azure.Commands.Batch.Models.PSPoolUsageMetrics</span></span>

## <span data-ttu-id="0ba0e-147">상속자</span><span class="sxs-lookup"><span data-stu-id="0ba0e-147">NOTES</span></span>

## <span data-ttu-id="0ba0e-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0ba0e-148">RELATED LINKS</span></span>

[<span data-ttu-id="0ba0e-149">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="0ba0e-149">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="0ba0e-150">Get-AzureBatchPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="0ba0e-150">Get-AzureBatchPoolStatistics</span></span>](./Get-AzureBatchPoolStatistics.md)

[<span data-ttu-id="0ba0e-151">가져오기-AzureBatchJobStatistics</span><span class="sxs-lookup"><span data-stu-id="0ba0e-151">Get-AzureBatchJobStatistics</span></span>](./Get-AzureBatchJobStatistics.md)


