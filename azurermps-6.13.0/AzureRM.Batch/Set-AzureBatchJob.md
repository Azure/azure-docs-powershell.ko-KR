---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 75483BC7-440A-437B-9EDE-D270D87CF3C5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJob.md
ms.openlocfilehash: 3baaa7296ab0fdd2c1dcab606b2896b11e5773f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526284"
---
# <span data-ttu-id="0ce2f-101">Set-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="0ce2f-101">Set-AzureBatchJob</span></span>

## <span data-ttu-id="0ce2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ce2f-102">SYNOPSIS</span></span>
<span data-ttu-id="0ce2f-103">일괄 작업을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ce2f-103">Updates a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ce2f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0ce2f-104">SYNTAX</span></span>

```
Set-AzureBatchJob [-Job] <PSCloudJob> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ce2f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0ce2f-105">DESCRIPTION</span></span>
<span data-ttu-id="0ce2f-106">**Set-AzureBatchJob** Cmdlet은 Azure 일괄 처리 작업을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ce2f-106">The **Set-AzureBatchJob** cmdlet updates an Azure Batch job.</span></span>
<span data-ttu-id="0ce2f-107">**Pscloudjob** 개체를 가져오려면 Get-AzureBatchJob cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ce2f-107">Use the Get-AzureBatchJob cmdlet to get a **PSCloudJob** object.</span></span>
<span data-ttu-id="0ce2f-108">해당 개체의 속성을 수정한 다음 현재 cmdlet을 사용 하 여 일괄 처리 서비스에 대 한 변경 내용을 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="0ce2f-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="0ce2f-109">예제의</span><span class="sxs-lookup"><span data-stu-id="0ce2f-109">EXAMPLES</span></span>

### <span data-ttu-id="0ce2f-110">예제 1: 작업 업데이트</span><span class="sxs-lookup"><span data-stu-id="0ce2f-110">Example 1: Update a job</span></span>
```
PS C:\>$Job = Get-AzureBatchJob -Id "Job17" -BatchContext $Context
PS C:\> $Job.Priority = 1
PS C:\> Set-AzureBatchJob -Job $Job -BatchContext $Context
```

<span data-ttu-id="0ce2f-111">첫 번째 명령은 **가져오기-AzureBatchJob** 을 사용 하 여 풀을 가져온 다음 $Job 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ce2f-111">The first command gets a pool by using **Get-AzureBatchJob** , and then stores it in the $Job variable.</span></span>
<span data-ttu-id="0ce2f-112">두 번째 명령은 $Job 개체에 대 한 우선 순위 사양을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ce2f-112">The second command modifies the priority specification on the $Job object.</span></span>
<span data-ttu-id="0ce2f-113">마지막 명령은 $Job의 로컬 개체와 일치 하도록 일괄 처리 서비스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ce2f-113">The final command updates the Batch service to match the local object in $Job.</span></span>

## <span data-ttu-id="0ce2f-114">변수</span><span class="sxs-lookup"><span data-stu-id="0ce2f-114">PARAMETERS</span></span>

### <span data-ttu-id="0ce2f-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="0ce2f-115">-BatchContext</span></span>
<span data-ttu-id="0ce2f-116">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ce2f-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="0ce2f-117">Get-AzureRmBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0ce2f-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="0ce2f-118">대신 공유 키 인증을 사용 하려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0ce2f-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="0ce2f-119">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0ce2f-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="0ce2f-120">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ce2f-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="0ce2f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ce2f-121">-DefaultProfile</span></span>
<span data-ttu-id="0ce2f-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0ce2f-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ce2f-123">-작업</span><span class="sxs-lookup"><span data-stu-id="0ce2f-123">-Job</span></span>
<span data-ttu-id="0ce2f-124">이 cmdlet이 일괄 처리 서비스를 업데이트 하는 **Pscloudjob** 을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ce2f-124">Specifies a **PSCloudJob** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0ce2f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ce2f-125">CommonParameters</span></span>
<span data-ttu-id="0ce2f-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ce2f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ce2f-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ce2f-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ce2f-128">입력</span><span class="sxs-lookup"><span data-stu-id="0ce2f-128">INPUTS</span></span>

### <span data-ttu-id="0ce2f-129">Microsoft.Azure.Commands.Batch. PSCloudJob 모델</span><span class="sxs-lookup"><span data-stu-id="0ce2f-129">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>
<span data-ttu-id="0ce2f-130">매개 변수: Job (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0ce2f-130">Parameters: Job (ByValue)</span></span>

### <span data-ttu-id="0ce2f-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="0ce2f-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="0ce2f-132">매개 변수: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0ce2f-132">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="0ce2f-133">출력</span><span class="sxs-lookup"><span data-stu-id="0ce2f-133">OUTPUTS</span></span>

### <span data-ttu-id="0ce2f-134">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="0ce2f-134">System.Void</span></span>

## <span data-ttu-id="0ce2f-135">상속자</span><span class="sxs-lookup"><span data-stu-id="0ce2f-135">NOTES</span></span>

## <span data-ttu-id="0ce2f-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0ce2f-136">RELATED LINKS</span></span>

[<span data-ttu-id="0ce2f-137">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="0ce2f-137">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="0ce2f-138">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="0ce2f-138">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="0ce2f-139">가져오기-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="0ce2f-139">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="0ce2f-140">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="0ce2f-140">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="0ce2f-141">새-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="0ce2f-141">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="0ce2f-142">-AzureBatchJob 제거</span><span class="sxs-lookup"><span data-stu-id="0ce2f-142">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="0ce2f-143">중지-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="0ce2f-143">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="0ce2f-144">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="0ce2f-144">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


