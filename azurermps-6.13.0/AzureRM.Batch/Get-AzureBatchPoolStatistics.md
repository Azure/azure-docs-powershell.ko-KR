---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 8188C617-4895-4B43-8D3B-FA6FC5B868DD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchpoolstatistics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPoolStatistics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPoolStatistics.md
ms.openlocfilehash: 0f6bee54c5abf795a49148e7c2d93707b45ba9a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532516"
---
# <span data-ttu-id="ec97d-101">Get-AzureBatchPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="ec97d-101">Get-AzureBatchPoolStatistics</span></span>

## <span data-ttu-id="ec97d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec97d-102">SYNOPSIS</span></span>
<span data-ttu-id="ec97d-103">일괄 처리 계정에 대 한 풀 요약 통계를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ec97d-103">Gets pool summary statistics for a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec97d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ec97d-104">SYNTAX</span></span>

```
Get-AzureBatchPoolStatistics -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ec97d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ec97d-105">DESCRIPTION</span></span>
<span data-ttu-id="ec97d-106">**Get-AzureBatchPoolStatistics** cmdlet은 지정 된 계정의 모든 풀에 대 한 수명 통계를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ec97d-106">The **Get-AzureBatchPoolStatistics** cmdlet gets the lifetime statistics for all of the pools in the specified account.</span></span>
<span data-ttu-id="ec97d-107">통계는 계정 만들기부터 통계의 마지막 업데이트 시간까지 계정에 있던 모든 풀에 대해 집계 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec97d-107">Statistics are aggregated across all pools that have ever existed in the account, from account creation to the last update time of the statistics.</span></span>

## <span data-ttu-id="ec97d-108">예제의</span><span class="sxs-lookup"><span data-stu-id="ec97d-108">EXAMPLES</span></span>

### <span data-ttu-id="ec97d-109">예제 1: 계정의 모든 풀에 대 한 리소스 통계 가져오기</span><span class="sxs-lookup"><span data-stu-id="ec97d-109">Example 1: Get resource statistics of all pools in an account</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $PoolStatistics = Get-AzureBatchPoolStatistics -BatchContext $Context
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

<span data-ttu-id="ec97d-110">첫 번째 명령은 **Get-AzureRmBatchAccountKeys** 를 사용 하 여 ContosoBatchAccount 라는 일괄 계정에 대 한 계정 키에 대 한 개체 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ec97d-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="ec97d-111">명령이이 개체 참조를 $Context 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec97d-111">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="ec97d-112">두 번째 명령은 지정 된 계정에 있는 모든 풀의 통계를 가져온 다음 $PoolStatistics에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec97d-112">The second command gets the statistics of all of the pools in the specified account, and then stores them in the $PoolStatistics.</span></span>
<span data-ttu-id="ec97d-113">마지막 명령은 $PoolStatistics의 **ResourceStatistics** 속성을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec97d-113">The final command displays the **ResourceStatistics** property of $PoolStatistics.</span></span>

## <span data-ttu-id="ec97d-114">변수</span><span class="sxs-lookup"><span data-stu-id="ec97d-114">PARAMETERS</span></span>

### <span data-ttu-id="ec97d-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="ec97d-115">-BatchContext</span></span>
<span data-ttu-id="ec97d-116">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec97d-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ec97d-117">Get-AzureRmBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec97d-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="ec97d-118">대신 공유 키 인증을 사용 하려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ec97d-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="ec97d-119">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec97d-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="ec97d-120">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec97d-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="ec97d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec97d-121">-DefaultProfile</span></span>
<span data-ttu-id="ec97d-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ec97d-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec97d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec97d-123">CommonParameters</span></span>
<span data-ttu-id="ec97d-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec97d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec97d-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec97d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec97d-126">입력</span><span class="sxs-lookup"><span data-stu-id="ec97d-126">INPUTS</span></span>

### <span data-ttu-id="ec97d-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ec97d-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="ec97d-128">매개 변수: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ec97d-128">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="ec97d-129">출력</span><span class="sxs-lookup"><span data-stu-id="ec97d-129">OUTPUTS</span></span>

### <span data-ttu-id="ec97d-130">Microsoft.Azure.Commands.Batch. PSPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="ec97d-130">Microsoft.Azure.Commands.Batch.Models.PSPoolStatistics</span></span>

## <span data-ttu-id="ec97d-131">상속자</span><span class="sxs-lookup"><span data-stu-id="ec97d-131">NOTES</span></span>

## <span data-ttu-id="ec97d-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ec97d-132">RELATED LINKS</span></span>

[<span data-ttu-id="ec97d-133">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="ec97d-133">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="ec97d-134">Get-AzureBatchPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="ec97d-134">Get-AzureBatchPoolUsageMetrics</span></span>](./Get-AzureBatchPoolUsageMetrics.md)

[<span data-ttu-id="ec97d-135">가져오기-AzureBatchJobStatistics</span><span class="sxs-lookup"><span data-stu-id="ec97d-135">Get-AzureBatchJobStatistics</span></span>](./Get-AzureBatchJobStatistics.md)


