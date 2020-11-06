---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: E655684D-9601-4A0B-BB09-EFB787EB2B1B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobStatistics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobStatistics.md
ms.openlocfilehash: 03b7e3999fbc482223365b59867c02c75e9d5ba1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530806"
---
# <span data-ttu-id="d8c9b-101">Get-AzureBatchJobStatistics</span><span class="sxs-lookup"><span data-stu-id="d8c9b-101">Get-AzureBatchJobStatistics</span></span>

## <span data-ttu-id="d8c9b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8c9b-102">SYNOPSIS</span></span>
<span data-ttu-id="d8c9b-103">일괄 처리 계정에 대 한 작업 요약 통계를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d8c9b-103">Gets job summary statistics for a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8c9b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d8c9b-104">SYNTAX</span></span>

```
Get-AzureBatchJobStatistics -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d8c9b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d8c9b-105">DESCRIPTION</span></span>
<span data-ttu-id="d8c9b-106">**Get-AzureBatchJobStatistics** Cmdlet은 Azure Batch 계정의 모든 작업에 대 한 수명 요약 통계를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d8c9b-106">The **Get-AzureBatchJobStatistics** cmdlet gets lifetime summary statistics for all of the jobs in an Azure Batch account.</span></span>
<span data-ttu-id="d8c9b-107">통계는 계정 만들기부터 통계의 마지막 업데이트 시간까지 계정에 있던 모든 작업에 대해 집계 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d8c9b-107">Statistics are aggregated across all jobs that have ever existed in the account, from account creation to the last update time of the statistics.</span></span>

## <span data-ttu-id="d8c9b-108">예제의</span><span class="sxs-lookup"><span data-stu-id="d8c9b-108">EXAMPLES</span></span>

### <span data-ttu-id="d8c9b-109">예제 1: 모든 작업에 대 한 요약 통계 가져오기</span><span class="sxs-lookup"><span data-stu-id="d8c9b-109">Example 1: Get summary statistics for all jobs</span></span>
```
PS C:\>Get-AzureBatchJobStatistics -BatchContext $Context
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

<span data-ttu-id="d8c9b-110">첫 번째 명령은 **Get-AzureRmBatchAccountKeys** 를 사용 하 여 ContosoBatchAccount 라는 일괄 계정에 대 한 계정 키에 대 한 개체 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d8c9b-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="d8c9b-111">명령이이 개체 참조를 $Context 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8c9b-111">The command stores this object reference in the $Context variable.</span></span>

<span data-ttu-id="d8c9b-112">두 번째 명령은 모든 작업에 대 한 요약 통계를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d8c9b-112">The second command gets the summary statistics for all of the jobs.</span></span>
<span data-ttu-id="d8c9b-113">명령에서 첫 번째 명령의 $Context 값을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8c9b-113">The command uses the $Context value from the first command.</span></span>

## <span data-ttu-id="d8c9b-114">변수</span><span class="sxs-lookup"><span data-stu-id="d8c9b-114">PARAMETERS</span></span>

### <span data-ttu-id="d8c9b-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="d8c9b-115">-BatchContext</span></span>
<span data-ttu-id="d8c9b-116">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8c9b-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="d8c9b-117">구독에 대 한 선택 키를 포함 하는 **Batchaccountcontext** 개체를 가져오려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8c9b-117">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="d8c9b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8c9b-118">-DefaultProfile</span></span>
<span data-ttu-id="d8c9b-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d8c9b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8c9b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8c9b-120">CommonParameters</span></span>
<span data-ttu-id="d8c9b-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8c9b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8c9b-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8c9b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8c9b-123">입력</span><span class="sxs-lookup"><span data-stu-id="d8c9b-123">INPUTS</span></span>

### <span data-ttu-id="d8c9b-124">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="d8c9b-124">BatchAccountContext</span></span>
<span data-ttu-id="d8c9b-125">' BatchContext ' 매개 변수는 파이프라인에서 ' BatchAccountContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8c9b-125">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="d8c9b-126">출력</span><span class="sxs-lookup"><span data-stu-id="d8c9b-126">OUTPUTS</span></span>

### <span data-ttu-id="d8c9b-127">PSJobStatistics</span><span class="sxs-lookup"><span data-stu-id="d8c9b-127">PSJobStatistics</span></span>

## <span data-ttu-id="d8c9b-128">상속자</span><span class="sxs-lookup"><span data-stu-id="d8c9b-128">NOTES</span></span>

## <span data-ttu-id="d8c9b-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d8c9b-129">RELATED LINKS</span></span>

[<span data-ttu-id="d8c9b-130">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="d8c9b-130">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="d8c9b-131">Get-AzureBatchPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="d8c9b-131">Get-AzureBatchPoolStatistics</span></span>](./Get-AzureBatchPoolStatistics.md)

[<span data-ttu-id="d8c9b-132">Get-AzureBatchPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="d8c9b-132">Get-AzureBatchPoolUsageMetrics</span></span>](./Get-AzureBatchPoolUsageMetrics.md)


