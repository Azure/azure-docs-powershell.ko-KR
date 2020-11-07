---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: E655684D-9601-4A0B-BB09-EFB787EB2B1B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchjobstatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobStatistic.md
ms.openlocfilehash: b2c62cf91410e2604875df6f82237445e153f6aa
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93879937"
---
# <span data-ttu-id="833a5-101">Get-AzBatchJobStatistic</span><span class="sxs-lookup"><span data-stu-id="833a5-101">Get-AzBatchJobStatistic</span></span>

## <span data-ttu-id="833a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="833a5-102">SYNOPSIS</span></span>
<span data-ttu-id="833a5-103">일괄 처리 계정에 대 한 작업 요약 통계를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="833a5-103">Gets job summary statistics for a Batch account.</span></span>

## <span data-ttu-id="833a5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="833a5-104">SYNTAX</span></span>

```
Get-AzBatchJobStatistic -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="833a5-105">설명은</span><span class="sxs-lookup"><span data-stu-id="833a5-105">DESCRIPTION</span></span>
<span data-ttu-id="833a5-106">**AzBatchJobStatistic** Cmdlet은 Azure Batch 계정에 있는 모든 작업에 대 한 수명 요약 통계를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="833a5-106">The **Get-AzBatchJobStatistic** cmdlet gets lifetime summary statistics for all of the jobs in an Azure Batch account.</span></span>
<span data-ttu-id="833a5-107">통계는 계정 만들기부터 통계의 마지막 업데이트 시간까지 계정에 있던 모든 작업에 대해 집계 됩니다.</span><span class="sxs-lookup"><span data-stu-id="833a5-107">Statistics are aggregated across all jobs that have ever existed in the account, from account creation to the last update time of the statistics.</span></span>

## <span data-ttu-id="833a5-108">예제의</span><span class="sxs-lookup"><span data-stu-id="833a5-108">EXAMPLES</span></span>

### <span data-ttu-id="833a5-109">예제 1: 모든 작업에 대 한 요약 통계 가져오기</span><span class="sxs-lookup"><span data-stu-id="833a5-109">Example 1: Get summary statistics for all jobs</span></span>
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

<span data-ttu-id="833a5-110">첫 번째 명령은 **Get-AzBatchAccountKeys** 를 사용 하 여 ContosoBatchAccount 라는 일괄 계정에 대 한 계정 키에 대 한 개체 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="833a5-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKeys**.</span></span>
<span data-ttu-id="833a5-111">명령이이 개체 참조를 $Context 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="833a5-111">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="833a5-112">두 번째 명령은 모든 작업에 대 한 요약 통계를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="833a5-112">The second command gets the summary statistics for all of the jobs.</span></span>
<span data-ttu-id="833a5-113">명령에서 첫 번째 명령의 $Context 값을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="833a5-113">The command uses the $Context value from the first command.</span></span>

## <span data-ttu-id="833a5-114">변수</span><span class="sxs-lookup"><span data-stu-id="833a5-114">PARAMETERS</span></span>

### <span data-ttu-id="833a5-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="833a5-115">-BatchContext</span></span>
<span data-ttu-id="833a5-116">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="833a5-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="833a5-117">Get-AzBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="833a5-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="833a5-118">대신 공유 키 인증을 사용 하려면 Get-AzBatchAccountKeys cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="833a5-118">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="833a5-119">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="833a5-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="833a5-120">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="833a5-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="833a5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="833a5-121">-DefaultProfile</span></span>
<span data-ttu-id="833a5-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="833a5-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="833a5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="833a5-123">CommonParameters</span></span>
<span data-ttu-id="833a5-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="833a5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="833a5-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="833a5-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="833a5-126">입력</span><span class="sxs-lookup"><span data-stu-id="833a5-126">INPUTS</span></span>

### <span data-ttu-id="833a5-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="833a5-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="833a5-128">출력</span><span class="sxs-lookup"><span data-stu-id="833a5-128">OUTPUTS</span></span>

### <span data-ttu-id="833a5-129">Microsoft.Azure.Commands.Batch. PSJobStatistics</span><span class="sxs-lookup"><span data-stu-id="833a5-129">Microsoft.Azure.Commands.Batch.Models.PSJobStatistics</span></span>

## <span data-ttu-id="833a5-130">상속자</span><span class="sxs-lookup"><span data-stu-id="833a5-130">NOTES</span></span>

## <span data-ttu-id="833a5-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="833a5-131">RELATED LINKS</span></span>

[<span data-ttu-id="833a5-132">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="833a5-132">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="833a5-133">Get-AzBatchPoolStatistic</span><span class="sxs-lookup"><span data-stu-id="833a5-133">Get-AzBatchPoolStatistic</span></span>](./Get-AzBatchPoolStatistic.md)

[<span data-ttu-id="833a5-134">Get-AzBatchPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="833a5-134">Get-AzBatchPoolUsageMetrics</span></span>](./Get-AzBatchPoolUsageMetric.md)


