---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 975B707C-5001-43ED-81AB-9BB6665135BA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJob.md
ms.openlocfilehash: 8893ed4002e576e257cd9b885d5773c5851edde0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532336"
---
# <span data-ttu-id="dd0c4-101">Stop-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="dd0c4-101">Stop-AzureBatchJob</span></span>

## <span data-ttu-id="dd0c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd0c4-102">SYNOPSIS</span></span>
<span data-ttu-id="dd0c4-103">일괄 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd0c4-103">Stops a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd0c4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dd0c4-104">SYNTAX</span></span>

```
Stop-AzureBatchJob [-Id] <String> [[-TerminateReason] <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd0c4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="dd0c4-105">DESCRIPTION</span></span>
<span data-ttu-id="dd0c4-106">**Stop-AzureBatchJob** Cmdlet은 Azure 일괄 처리 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd0c4-106">The **Stop-AzureBatchJob** cmdlet stops an Azure Batch job.</span></span>
<span data-ttu-id="dd0c4-107">이 명령은 작업을 완료 된 것으로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd0c4-107">This command marks the job as completed.</span></span>

## <span data-ttu-id="dd0c4-108">예제의</span><span class="sxs-lookup"><span data-stu-id="dd0c4-108">EXAMPLES</span></span>

### <span data-ttu-id="dd0c4-109">예제 1: 일괄 작업 중지</span><span class="sxs-lookup"><span data-stu-id="dd0c4-109">Example 1: Stop a Batch job</span></span>
```
PS C:\>Stop-AzureBatchJob -Id "Job-000001" -TerminateReason "No more tasks to run" -BatchContext $Context
```

<span data-ttu-id="dd0c4-110">이 명령은 ID 작업이 있는 작업을 중지 합니다-000001.</span><span class="sxs-lookup"><span data-stu-id="dd0c4-110">This command stops the job that has the ID Job-000001.</span></span>
<span data-ttu-id="dd0c4-111">명령은 작업을 중지 하도록 선택한 이유를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd0c4-111">The command specifies a reason that you chose to stop the job.</span></span>
<span data-ttu-id="dd0c4-112">Get-AzureRmBatchAccountKeys cmdlet을 사용 하 여 컨텍스트를 $Context 변수에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd0c4-112">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="dd0c4-113">변수</span><span class="sxs-lookup"><span data-stu-id="dd0c4-113">PARAMETERS</span></span>

### <span data-ttu-id="dd0c4-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="dd0c4-114">-BatchContext</span></span>
<span data-ttu-id="dd0c4-115">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd0c4-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="dd0c4-116">구독에 대 한 선택 키를 포함 하는 **Batchaccountcontext** 개체를 가져오려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd0c4-116">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="dd0c4-117">-Id</span><span class="sxs-lookup"><span data-stu-id="dd0c4-117">-Id</span></span>
<span data-ttu-id="dd0c4-118">이 cmdlet이 중지 하는 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd0c4-118">Specifies the ID of the job that this cmdlet stops.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd0c4-119">-TerminateReason</span><span class="sxs-lookup"><span data-stu-id="dd0c4-119">-TerminateReason</span></span>
<span data-ttu-id="dd0c4-120">작업을 중지 하기로 결정 한 이유를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd0c4-120">Specifies the reason that you decided to stop the job.</span></span>
<span data-ttu-id="dd0c4-121">이 cmdlet은이 텍스트를 작업의 **TerminateReason** 속성으로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd0c4-121">This cmdlet stores this text as the **TerminateReason** property of the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd0c4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd0c4-122">-DefaultProfile</span></span>
<span data-ttu-id="dd0c4-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dd0c4-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd0c4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd0c4-124">CommonParameters</span></span>
<span data-ttu-id="dd0c4-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd0c4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd0c4-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd0c4-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd0c4-127">입력</span><span class="sxs-lookup"><span data-stu-id="dd0c4-127">INPUTS</span></span>

### <span data-ttu-id="dd0c4-128">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="dd0c4-128">BatchAccountContext</span></span>
<span data-ttu-id="dd0c4-129">' BatchContext ' 매개 변수는 파이프라인에서 ' BatchAccountContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd0c4-129">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="dd0c4-130">이름</span><span class="sxs-lookup"><span data-stu-id="dd0c4-130">String</span></span>
<span data-ttu-id="dd0c4-131">' I d ' 매개 변수는 파이프라인에서 ' String ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd0c4-131">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="dd0c4-132">출력</span><span class="sxs-lookup"><span data-stu-id="dd0c4-132">OUTPUTS</span></span>

## <span data-ttu-id="dd0c4-133">상속자</span><span class="sxs-lookup"><span data-stu-id="dd0c4-133">NOTES</span></span>

## <span data-ttu-id="dd0c4-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dd0c4-134">RELATED LINKS</span></span>

[<span data-ttu-id="dd0c4-135">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="dd0c4-135">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="dd0c4-136">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="dd0c4-136">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="dd0c4-137">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="dd0c4-137">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="dd0c4-138">가져오기-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="dd0c4-138">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="dd0c4-139">새-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="dd0c4-139">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="dd0c4-140">-AzureBatchJob 제거</span><span class="sxs-lookup"><span data-stu-id="dd0c4-140">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="dd0c4-141">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="dd0c4-141">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


