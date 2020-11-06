---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B4737AE8-F57C-4B95-B81E-74802EF8E7AE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJobSchedule.md
ms.openlocfilehash: 73d80d3547ea895e5cbd35b2d514d9a757164bed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537499"
---
# <span data-ttu-id="6fbaa-101">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="6fbaa-101">Disable-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="6fbaa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fbaa-102">SYNOPSIS</span></span>
<span data-ttu-id="6fbaa-103">일괄 작업 일정을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fbaa-103">Disables a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6fbaa-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6fbaa-104">SYNTAX</span></span>

```
Disable-AzureBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6fbaa-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6fbaa-105">DESCRIPTION</span></span>
<span data-ttu-id="6fbaa-106">**-AzureBatchJobSchedule** Cmdlet은 Azure 일괄 처리 작업 일정을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fbaa-106">The **Disable-AzureBatchJobSchedule** cmdlet disables an Azure Batch job schedule.</span></span>
<span data-ttu-id="6fbaa-107">일정을 사용 하지 않도록 설정 하면 해당 일정에 따라 작업이 생성 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6fbaa-107">If you disable a schedule, jobs are not created according to that schedule.</span></span>
<span data-ttu-id="6fbaa-108">나중에 비활성화 된 일정을 사용 하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6fbaa-108">You can enable a disabled schedule later.</span></span>

## <span data-ttu-id="6fbaa-109">예제의</span><span class="sxs-lookup"><span data-stu-id="6fbaa-109">EXAMPLES</span></span>

### <span data-ttu-id="6fbaa-110">예제 1: 작업 일정 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="6fbaa-110">Example 1: Disable a job schedule</span></span>
```
PS C:\>Disable-AzureBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="6fbaa-111">이 명령은 ID JobSchedule17 있는 작업 일정을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fbaa-111">This command disables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="6fbaa-112">$Context 변수에 컨텍스트를 할당 하려면 **Get-AzureRmBatchAccountKeys** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fbaa-112">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="6fbaa-113">변수</span><span class="sxs-lookup"><span data-stu-id="6fbaa-113">PARAMETERS</span></span>

### <span data-ttu-id="6fbaa-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="6fbaa-114">-BatchContext</span></span>
<span data-ttu-id="6fbaa-115">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fbaa-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="6fbaa-116">구독에 대 한 선택 키를 포함 하는 **Batchaccountcontext** 개체를 가져오려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fbaa-116">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="6fbaa-117">-Id</span><span class="sxs-lookup"><span data-stu-id="6fbaa-117">-Id</span></span>
<span data-ttu-id="6fbaa-118">이 cmdlet이 사용 하지 않도록 설정 하는 작업 일정의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fbaa-118">Specifies the ID of the job schedule that this cmdlet disables.</span></span>

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

### <span data-ttu-id="6fbaa-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fbaa-119">-DefaultProfile</span></span>
<span data-ttu-id="6fbaa-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6fbaa-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6fbaa-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fbaa-121">CommonParameters</span></span>
<span data-ttu-id="6fbaa-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fbaa-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fbaa-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fbaa-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fbaa-124">입력</span><span class="sxs-lookup"><span data-stu-id="6fbaa-124">INPUTS</span></span>

### <span data-ttu-id="6fbaa-125">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="6fbaa-125">BatchAccountContext</span></span>
<span data-ttu-id="6fbaa-126">' BatchContext ' 매개 변수는 파이프라인에서 ' BatchAccountContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fbaa-126">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="6fbaa-127">이름</span><span class="sxs-lookup"><span data-stu-id="6fbaa-127">String</span></span>
<span data-ttu-id="6fbaa-128">' I d ' 매개 변수는 파이프라인에서 ' String ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fbaa-128">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="6fbaa-129">출력</span><span class="sxs-lookup"><span data-stu-id="6fbaa-129">OUTPUTS</span></span>

## <span data-ttu-id="6fbaa-130">상속자</span><span class="sxs-lookup"><span data-stu-id="6fbaa-130">NOTES</span></span>

## <span data-ttu-id="6fbaa-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6fbaa-131">RELATED LINKS</span></span>

[<span data-ttu-id="6fbaa-132">-AzureBatchJobSchedule 사용</span><span class="sxs-lookup"><span data-stu-id="6fbaa-132">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="6fbaa-133">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="6fbaa-133">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="6fbaa-134">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="6fbaa-134">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="6fbaa-135">새-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="6fbaa-135">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="6fbaa-136">-AzureBatchJobSchedule 제거</span><span class="sxs-lookup"><span data-stu-id="6fbaa-136">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="6fbaa-137">중지-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="6fbaa-137">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="6fbaa-138">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6fbaa-138">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


