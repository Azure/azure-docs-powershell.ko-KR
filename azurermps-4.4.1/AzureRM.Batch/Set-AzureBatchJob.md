---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 75483BC7-440A-437B-9EDE-D270D87CF3C5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJob.md
ms.openlocfilehash: eb15991e0bf7aefd60b53dbb02785a1b2004cb22
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537472"
---
# <span data-ttu-id="cac24-101">Set-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="cac24-101">Set-AzureBatchJob</span></span>

## <span data-ttu-id="cac24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cac24-102">SYNOPSIS</span></span>
<span data-ttu-id="cac24-103">일괄 작업을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="cac24-103">Updates a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cac24-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cac24-104">SYNTAX</span></span>

```
Set-AzureBatchJob [-Job] <PSCloudJob> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cac24-105">설명은</span><span class="sxs-lookup"><span data-stu-id="cac24-105">DESCRIPTION</span></span>
<span data-ttu-id="cac24-106">**Set-AzureBatchJob** Cmdlet은 Azure 일괄 처리 작업을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="cac24-106">The **Set-AzureBatchJob** cmdlet updates an Azure Batch job.</span></span>
<span data-ttu-id="cac24-107">**Pscloudjob** 개체를 가져오려면 Get-AzureBatchJob cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cac24-107">Use the Get-AzureBatchJob cmdlet to get a **PSCloudJob** object.</span></span>
<span data-ttu-id="cac24-108">해당 개체의 속성을 수정한 다음 현재 cmdlet을 사용 하 여 일괄 처리 서비스에 대 한 변경 내용을 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="cac24-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="cac24-109">예제의</span><span class="sxs-lookup"><span data-stu-id="cac24-109">EXAMPLES</span></span>

### <span data-ttu-id="cac24-110">예제 1: 작업 업데이트</span><span class="sxs-lookup"><span data-stu-id="cac24-110">Example 1: Update a job</span></span>
```
PS C:\>$Job = Get-AzureBatchJob -Id "Job17" -BatchContext $Context
PS C:\> $Job.Priority = 1
PS C:\> Set-AzureBatchJob -Job $Job -BatchContext $Context
```

<span data-ttu-id="cac24-111">첫 번째 명령은 **가져오기-AzureBatchJob** 을 사용 하 여 풀을 가져온 다음 $Job 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="cac24-111">The first command gets a pool by using **Get-AzureBatchJob** , and then stores it in the $Job variable.</span></span>

<span data-ttu-id="cac24-112">두 번째 명령은 $Job 개체에 대 한 우선 순위 사양을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cac24-112">The second command modifies the priority specification on the $Job object.</span></span>

<span data-ttu-id="cac24-113">마지막 명령은 $Job의 로컬 개체와 일치 하도록 일괄 처리 서비스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="cac24-113">The final command updates the Batch service to match the local object in $Job.</span></span>

## <span data-ttu-id="cac24-114">변수</span><span class="sxs-lookup"><span data-stu-id="cac24-114">PARAMETERS</span></span>

### <span data-ttu-id="cac24-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="cac24-115">-BatchContext</span></span>
<span data-ttu-id="cac24-116">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cac24-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="cac24-117">구독에 대 한 선택 키를 포함 하는 **Batchaccountcontext** 개체를 가져오려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cac24-117">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="cac24-118">-작업</span><span class="sxs-lookup"><span data-stu-id="cac24-118">-Job</span></span>
<span data-ttu-id="cac24-119">이 cmdlet이 일괄 처리 서비스를 업데이트 하는 **Pscloudjob** 을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cac24-119">Specifies a **PSCloudJob** to which this cmdlet updates the Batch service.</span></span>

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

### <span data-ttu-id="cac24-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cac24-120">-DefaultProfile</span></span>
<span data-ttu-id="cac24-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cac24-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cac24-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cac24-122">CommonParameters</span></span>
<span data-ttu-id="cac24-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cac24-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cac24-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cac24-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cac24-125">입력</span><span class="sxs-lookup"><span data-stu-id="cac24-125">INPUTS</span></span>

### <span data-ttu-id="cac24-126">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="cac24-126">BatchAccountContext</span></span>
<span data-ttu-id="cac24-127">' BatchContext ' 매개 변수는 파이프라인에서 ' BatchAccountContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cac24-127">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="cac24-128">PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="cac24-128">PSCloudJob</span></span>
<span data-ttu-id="cac24-129">' Job ' 매개 변수는 파이프라인에서 ' PSCloudJob ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cac24-129">Parameter 'Job' accepts value of type 'PSCloudJob' from the pipeline</span></span>

## <span data-ttu-id="cac24-130">출력</span><span class="sxs-lookup"><span data-stu-id="cac24-130">OUTPUTS</span></span>

## <span data-ttu-id="cac24-131">상속자</span><span class="sxs-lookup"><span data-stu-id="cac24-131">NOTES</span></span>

## <span data-ttu-id="cac24-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cac24-132">RELATED LINKS</span></span>

[<span data-ttu-id="cac24-133">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="cac24-133">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="cac24-134">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="cac24-134">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="cac24-135">가져오기-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="cac24-135">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="cac24-136">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="cac24-136">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="cac24-137">새-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="cac24-137">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="cac24-138">-AzureBatchJob 제거</span><span class="sxs-lookup"><span data-stu-id="cac24-138">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="cac24-139">중지-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="cac24-139">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="cac24-140">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cac24-140">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


