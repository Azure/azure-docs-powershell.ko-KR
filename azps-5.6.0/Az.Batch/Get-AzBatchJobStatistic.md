---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: E655684D-9601-4A0B-BB09-EFB787EB2B1B
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchjobstatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobStatistic.md
ms.openlocfilehash: ec52f8b48433e52e86551a8346f4ec9a61b5727d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987023"
---
# <span data-ttu-id="50f90-101">Get-AzBatchJobStatistic</span><span class="sxs-lookup"><span data-stu-id="50f90-101">Get-AzBatchJobStatistic</span></span>

## <span data-ttu-id="50f90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50f90-102">SYNOPSIS</span></span>
<span data-ttu-id="50f90-103">Batch 계정에 대한 작업 요약 통계를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="50f90-103">Gets job summary statistics for a Batch account.</span></span>

## <span data-ttu-id="50f90-104">구문</span><span class="sxs-lookup"><span data-stu-id="50f90-104">SYNTAX</span></span>

```
Get-AzBatchJobStatistic -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="50f90-105">설명</span><span class="sxs-lookup"><span data-stu-id="50f90-105">DESCRIPTION</span></span>
<span data-ttu-id="50f90-106">**Get-AzBatchJobStatistic** cmdlet은 Azure Batch 계정의 모든 작업의 수명 요약 통계를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="50f90-106">The **Get-AzBatchJobStatistic** cmdlet gets lifetime summary statistics for all of the jobs in an Azure Batch account.</span></span>
<span data-ttu-id="50f90-107">통계는 계정 생성에서 통계의 마지막 업데이트 시간까지 계정에 있는 모든 작업에서 집계됩니다.</span><span class="sxs-lookup"><span data-stu-id="50f90-107">Statistics are aggregated across all jobs that have ever existed in the account, from account creation to the last update time of the statistics.</span></span>

## <span data-ttu-id="50f90-108">예제</span><span class="sxs-lookup"><span data-stu-id="50f90-108">EXAMPLES</span></span>

### <span data-ttu-id="50f90-109">예제 1: 모든 작업의 요약 통계를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="50f90-109">Example 1: Get summary statistics for all jobs</span></span>
```
PS C:\>Get-AzBatchJobStatistic -BatchContext $Context
FailedTaskCount    : 330
KernelCpuTime      : 00:24:31.8440000
LastUpdateTime     : 5/16/2016 6:00:00 PM
ReadIOGiB          : 38.1271341182292
ReadIOps           : 26546054
StartTime          : 11/3/2015 9:47:14 PM
SucceededTaskCount : 766
TaskRetryCount     : 0
Url                : https://accountname.westus.batch.azure.com/lifetimejobstats
UserCpuTime        : 20:55:50.3200000
WaitTime           : 03:54:49.8530000
WallClockTime      : 20:55:50.3200000
WriteIOGiB         : 0.159623090177774
WriteIOps          : 146946
```

<span data-ttu-id="50f90-110">첫 번째 명령은 **Get-AzBatchAccountKey를 사용하여 ContosoBatchAccount라는** 일괄 처리 계정에 대한 계정 키에 대한 개체 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="50f90-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="50f90-111">명령은 이 개체 참조를 $Context 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="50f90-111">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="50f90-112">두 번째 명령은 모든 작업의 요약 통계를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="50f90-112">The second command gets the summary statistics for all of the jobs.</span></span>
<span data-ttu-id="50f90-113">명령은 첫 $Context 값을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="50f90-113">The command uses the $Context value from the first command.</span></span>

## <span data-ttu-id="50f90-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="50f90-114">PARAMETERS</span></span>

### <span data-ttu-id="50f90-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="50f90-115">-BatchContext</span></span>
<span data-ttu-id="50f90-116">Batch 서비스와 상호 작용하는 데 이 cmdlet이 사용하는 **BatchAccountContext** 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="50f90-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="50f90-117">Get-AzBatchAccount cmdlet을 사용하여 BatchAccountContext를 얻으면 Batch 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="50f90-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="50f90-118">대신 공유 키 인증을 사용 Get-AzBatchAccountKey cmdlet을 사용하여 액세스 키가 채워진 BatchAccountContext 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="50f90-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="50f90-119">공유 키 인증을 사용하는 경우 기본 액세스 키는 기본적으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="50f90-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="50f90-120">사용할 키를 변경하기 위해 BatchAccountContext.KeyInUse 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="50f90-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="50f90-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50f90-121">-DefaultProfile</span></span>
<span data-ttu-id="50f90-122">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="50f90-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50f90-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50f90-123">CommonParameters</span></span>
<span data-ttu-id="50f90-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="50f90-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50f90-125">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="50f90-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50f90-126">입력</span><span class="sxs-lookup"><span data-stu-id="50f90-126">INPUTS</span></span>

### <span data-ttu-id="50f90-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="50f90-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="50f90-128">출력</span><span class="sxs-lookup"><span data-stu-id="50f90-128">OUTPUTS</span></span>

### <span data-ttu-id="50f90-129">Microsoft.Azure.Commands.Bat. Models.PSJobStatistics</span><span class="sxs-lookup"><span data-stu-id="50f90-129">Microsoft.Azure.Commands.Batch.Models.PSJobStatistics</span></span>

## <span data-ttu-id="50f90-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="50f90-130">NOTES</span></span>

## <span data-ttu-id="50f90-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="50f90-131">RELATED LINKS</span></span>

[<span data-ttu-id="50f90-132">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="50f90-132">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="50f90-133">Get-AzBatchPoolStatistic</span><span class="sxs-lookup"><span data-stu-id="50f90-133">Get-AzBatchPoolStatistic</span></span>](./Get-AzBatchPoolStatistic.md)

[<span data-ttu-id="50f90-134">Get-AzBatchPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="50f90-134">Get-AzBatchPoolUsageMetrics</span></span>](./Get-AzBatchPoolUsageMetric.md)
