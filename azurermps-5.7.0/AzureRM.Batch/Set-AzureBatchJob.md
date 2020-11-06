---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 75483BC7-440A-437B-9EDE-D270D87CF3C5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJob.md
ms.openlocfilehash: a878002c509fd2a895f61a97af1bef2afebc3691
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535304"
---
# <span data-ttu-id="26b3a-101">Set-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="26b3a-101">Set-AzureBatchJob</span></span>

## <span data-ttu-id="26b3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26b3a-102">SYNOPSIS</span></span>
<span data-ttu-id="26b3a-103">일괄 작업을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="26b3a-103">Updates a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26b3a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="26b3a-104">SYNTAX</span></span>

```
Set-AzureBatchJob [-Job] <PSCloudJob> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26b3a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="26b3a-105">DESCRIPTION</span></span>
<span data-ttu-id="26b3a-106">**Set-AzureBatchJob** Cmdlet은 Azure 일괄 처리 작업을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="26b3a-106">The **Set-AzureBatchJob** cmdlet updates an Azure Batch job.</span></span>
<span data-ttu-id="26b3a-107">**Pscloudjob** 개체를 가져오려면 Get-AzureBatchJob cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="26b3a-107">Use the Get-AzureBatchJob cmdlet to get a **PSCloudJob** object.</span></span>
<span data-ttu-id="26b3a-108">해당 개체의 속성을 수정한 다음 현재 cmdlet을 사용 하 여 일괄 처리 서비스에 대 한 변경 내용을 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="26b3a-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="26b3a-109">예제의</span><span class="sxs-lookup"><span data-stu-id="26b3a-109">EXAMPLES</span></span>

### <span data-ttu-id="26b3a-110">예제 1: 작업 업데이트</span><span class="sxs-lookup"><span data-stu-id="26b3a-110">Example 1: Update a job</span></span>
```
PS C:\>$Job = Get-AzureBatchJob -Id "Job17" -BatchContext $Context
PS C:\> $Job.Priority = 1
PS C:\> Set-AzureBatchJob -Job $Job -BatchContext $Context
```

<span data-ttu-id="26b3a-111">첫 번째 명령은 **가져오기-AzureBatchJob** 을 사용 하 여 풀을 가져온 다음 $Job 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="26b3a-111">The first command gets a pool by using **Get-AzureBatchJob** , and then stores it in the $Job variable.</span></span>

<span data-ttu-id="26b3a-112">두 번째 명령은 $Job 개체에 대 한 우선 순위 사양을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26b3a-112">The second command modifies the priority specification on the $Job object.</span></span>

<span data-ttu-id="26b3a-113">마지막 명령은 $Job의 로컬 개체와 일치 하도록 일괄 처리 서비스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="26b3a-113">The final command updates the Batch service to match the local object in $Job.</span></span>

## <span data-ttu-id="26b3a-114">변수</span><span class="sxs-lookup"><span data-stu-id="26b3a-114">PARAMETERS</span></span>

### <span data-ttu-id="26b3a-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="26b3a-115">-BatchContext</span></span>
<span data-ttu-id="26b3a-116">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26b3a-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="26b3a-117">Get-AzureRmBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="26b3a-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="26b3a-118">대신 공유 키 인증을 사용 하려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="26b3a-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="26b3a-119">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="26b3a-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="26b3a-120">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26b3a-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="26b3a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26b3a-121">-DefaultProfile</span></span>
<span data-ttu-id="26b3a-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="26b3a-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26b3a-123">-작업</span><span class="sxs-lookup"><span data-stu-id="26b3a-123">-Job</span></span>
<span data-ttu-id="26b3a-124">이 cmdlet이 일괄 처리 서비스를 업데이트 하는 **Pscloudjob** 을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26b3a-124">Specifies a **PSCloudJob** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: PSCloudJob
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="26b3a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26b3a-125">CommonParameters</span></span>
<span data-ttu-id="26b3a-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="26b3a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26b3a-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26b3a-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26b3a-128">입력</span><span class="sxs-lookup"><span data-stu-id="26b3a-128">INPUTS</span></span>

### <span data-ttu-id="26b3a-129">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="26b3a-129">BatchAccountContext</span></span>
<span data-ttu-id="26b3a-130">' BatchContext ' 매개 변수는 파이프라인에서 ' BatchAccountContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="26b3a-130">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="26b3a-131">PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="26b3a-131">PSCloudJob</span></span>
<span data-ttu-id="26b3a-132">' Job ' 매개 변수는 파이프라인에서 ' PSCloudJob ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="26b3a-132">Parameter 'Job' accepts value of type 'PSCloudJob' from the pipeline</span></span>

## <span data-ttu-id="26b3a-133">출력</span><span class="sxs-lookup"><span data-stu-id="26b3a-133">OUTPUTS</span></span>

## <span data-ttu-id="26b3a-134">상속자</span><span class="sxs-lookup"><span data-stu-id="26b3a-134">NOTES</span></span>

## <span data-ttu-id="26b3a-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="26b3a-135">RELATED LINKS</span></span>

[<span data-ttu-id="26b3a-136">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="26b3a-136">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="26b3a-137">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="26b3a-137">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="26b3a-138">가져오기-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="26b3a-138">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="26b3a-139">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="26b3a-139">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="26b3a-140">새-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="26b3a-140">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="26b3a-141">-AzureBatchJob 제거</span><span class="sxs-lookup"><span data-stu-id="26b3a-141">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="26b3a-142">중지-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="26b3a-142">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="26b3a-143">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="26b3a-143">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


