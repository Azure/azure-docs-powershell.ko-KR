---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 8188C617-4895-4B43-8D3B-FA6FC5B868DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchpoolstatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolStatistic.md
ms.openlocfilehash: 49aa971dcc9d46f5a063042cbcdf8ca449c41e94
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197108"
---
# <span data-ttu-id="ba96b-101">Get-AzBatchPoolStatistic</span><span class="sxs-lookup"><span data-stu-id="ba96b-101">Get-AzBatchPoolStatistic</span></span>

## <span data-ttu-id="ba96b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba96b-102">SYNOPSIS</span></span>
<span data-ttu-id="ba96b-103">Batch 계정에 대한 풀 요약 통계를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ba96b-103">Gets pool summary statistics for a Batch account.</span></span>

## <span data-ttu-id="ba96b-104">구문</span><span class="sxs-lookup"><span data-stu-id="ba96b-104">SYNTAX</span></span>

```
Get-AzBatchPoolStatistic -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ba96b-105">설명</span><span class="sxs-lookup"><span data-stu-id="ba96b-105">DESCRIPTION</span></span>
<span data-ttu-id="ba96b-106">**Get-AzBatchPoolStatistic** cmdlet은 지정된 계정의 모든 풀에 대한 수명 통계를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ba96b-106">The **Get-AzBatchPoolStatistic** cmdlet gets the lifetime statistics for all of the pools in the specified account.</span></span>
<span data-ttu-id="ba96b-107">통계는 계정 생성부터 통계의 마지막 업데이트 시간까지 계정에 존재하는 모든 풀에서 집계됩니다.</span><span class="sxs-lookup"><span data-stu-id="ba96b-107">Statistics are aggregated across all pools that have ever existed in the account, from account creation to the last update time of the statistics.</span></span>

## <span data-ttu-id="ba96b-108">예제</span><span class="sxs-lookup"><span data-stu-id="ba96b-108">EXAMPLES</span></span>

### <span data-ttu-id="ba96b-109">예제 1: 계정의 모든 풀에 대한 리소스 통계를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ba96b-109">Example 1: Get resource statistics of all pools in an account</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> $PoolStatistics = Get-AzBatchPoolStatistic -BatchContext $Context
PS C:\> $PoolStatistics.ResourceStatistics
AverageCpuPercentage : 0.351232518750755
AverageDiskGiB       : 55.2569014701165
AverageMemoryGiB     : 2.87273772318252
DiskReadGiB          : 45.1326256990433
DiskReadIOps         : 878278
DiskWriteGiB         : 1230.72120628133
DiskWriteIOps        : 176832212
LastUpdateTime       : 5/16/2016 4:30:00 PM
NetworkReadGiB       : 29.3502839952707
NetworkWriteGiB      : 25.5208827350289
PeakDiskGiB          : 21.9638671875
PeakMemoryGiB        : 1.11184692382813
StartTime            : 2/10/2016 7:07:24 PM
```

<span data-ttu-id="ba96b-110">첫 번째 명령은 **Get-AzBatchAccountKey를** 사용하여 ContosoBatchAccount라는 배치 계정에 대한 계정 키에 대한 개체 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ba96b-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="ba96b-111">이 명령은 이 개체 참조를 $Context 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="ba96b-111">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="ba96b-112">두 번째 명령은 지정된 계정의 모든 풀에 대한 통계를 인용한 다음, 해당 풀을 $PoolStatistics.</span><span class="sxs-lookup"><span data-stu-id="ba96b-112">The second command gets the statistics of all of the pools in the specified account, and then stores them in the $PoolStatistics.</span></span>
<span data-ttu-id="ba96b-113">마지막 명령은 리소스의 **ResourceStatistics** 속성을 $PoolStatistics.</span><span class="sxs-lookup"><span data-stu-id="ba96b-113">The final command displays the **ResourceStatistics** property of $PoolStatistics.</span></span>

## <span data-ttu-id="ba96b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ba96b-114">PARAMETERS</span></span>

### <span data-ttu-id="ba96b-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="ba96b-115">-BatchContext</span></span>
<span data-ttu-id="ba96b-116">이 cmdlet이 Batch 서비스와 상호 작용하는 데 사용하는 **BatchAccountContext** 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ba96b-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ba96b-117">Get-AzBatchAccount cmdlet을 사용하여 BatchAccountContext를 얻으면 Batch 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="ba96b-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="ba96b-118">대신 공유 키 인증을 사용 Get-AzBatchAccountKey 키가 채워진 BatchAccountContext 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ba96b-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="ba96b-119">공유 키 인증을 사용하는 경우 기본 액세스 키가 기본적으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="ba96b-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="ba96b-120">사용할 키를 변경하기 위해 BatchAccountContext.KeyInUse 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="ba96b-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="ba96b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba96b-121">-DefaultProfile</span></span>
<span data-ttu-id="ba96b-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ba96b-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba96b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba96b-123">CommonParameters</span></span>
<span data-ttu-id="ba96b-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ba96b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba96b-125">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ba96b-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba96b-126">입력</span><span class="sxs-lookup"><span data-stu-id="ba96b-126">INPUTS</span></span>

### <span data-ttu-id="ba96b-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ba96b-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="ba96b-128">출력</span><span class="sxs-lookup"><span data-stu-id="ba96b-128">OUTPUTS</span></span>

### <span data-ttu-id="ba96b-129">Microsoft.Azure.Commands.Batch. Models.PSPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="ba96b-129">Microsoft.Azure.Commands.Batch.Models.PSPoolStatistics</span></span>

## <span data-ttu-id="ba96b-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ba96b-130">NOTES</span></span>

## <span data-ttu-id="ba96b-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ba96b-131">RELATED LINKS</span></span>

[<span data-ttu-id="ba96b-132">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="ba96b-132">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="ba96b-133">Get-AzBatchPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="ba96b-133">Get-AzBatchPoolUsageMetrics</span></span>](./Get-AzBatchPoolUsageMetric.md)

[<span data-ttu-id="ba96b-134">Get-AzBatchJobStatistic</span><span class="sxs-lookup"><span data-stu-id="ba96b-134">Get-AzBatchJobStatistic</span></span>](./Get-AzBatchJobStatistic.md)
