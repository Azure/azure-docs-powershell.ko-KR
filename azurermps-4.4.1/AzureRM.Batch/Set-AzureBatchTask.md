---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 6A6D6C7D-EED7-4AD4-ACE6-BFA64404455E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchTask.md
ms.openlocfilehash: b572a7aefc3076671e78895f5fea531929858873
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535488"
---
# <span data-ttu-id="709bc-101">Set-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="709bc-101">Set-AzureBatchTask</span></span>

## <span data-ttu-id="709bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="709bc-102">SYNOPSIS</span></span>
<span data-ttu-id="709bc-103">작업의 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="709bc-103">Updates the properties of a task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="709bc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="709bc-104">SYNTAX</span></span>

```
Set-AzureBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="709bc-105">설명은</span><span class="sxs-lookup"><span data-stu-id="709bc-105">DESCRIPTION</span></span>
<span data-ttu-id="709bc-106">**Set-AzureBatchTask** Cmdlet은 Azure 일괄 처리 서비스에서 작업의 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="709bc-106">The **Set-AzureBatchTask** cmdlet updates the properties of a task in the Azure Batch service.</span></span>
<span data-ttu-id="709bc-107">**Pscloudtask** 개체를 가져오려면 Get-AzureBatchTask cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="709bc-107">Use the Get-AzureBatchTask cmdlet to get a **PSCloudTask** object.</span></span>
<span data-ttu-id="709bc-108">해당 개체의 속성을 수정한 다음 현재 cmdlet을 사용 하 여 일괄 처리 서비스에 대 한 변경 내용을 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="709bc-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="709bc-109">예제의</span><span class="sxs-lookup"><span data-stu-id="709bc-109">EXAMPLES</span></span>

### <span data-ttu-id="709bc-110">예제 1: 작업 업데이트</span><span class="sxs-lookup"><span data-stu-id="709bc-110">Example 1: Update a task</span></span>
```
PS C:\>$Task = Get-AzureBatchTask -JobId "Job16" -Id "Task22" -BatchContext $Context
PS C:\> $Constraints = New-Object Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints -ArgumentList @([TimeSpan}::FromDays(5), [TimeSpan]::FromDays(2), 3)
PS C:\> $Task.Constraints = $Constraints
PS C:\> Set-AzureBatchTask -Task $Task -BatchContext $Context
```

<span data-ttu-id="709bc-111">첫 번째 명령은 **가져오기-AzureBatchTask** 를 사용 하 여 작업을 가져온 다음 $Task 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="709bc-111">The first command gets a task by using **Get-AzureBatchTask** , and then stores it in the $Task variable.</span></span>

<span data-ttu-id="709bc-112">다음 두 명령은 $Task 작업의 제약 조건을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="709bc-112">The next two commands modify the constraints of the task in $Task.</span></span>

<span data-ttu-id="709bc-113">마지막 명령은 $Task의 로컬 개체와 일치 하도록 일괄 처리 서비스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="709bc-113">The final command updates the Batch service to match the local object in $Task.</span></span>

## <span data-ttu-id="709bc-114">변수</span><span class="sxs-lookup"><span data-stu-id="709bc-114">PARAMETERS</span></span>

### <span data-ttu-id="709bc-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="709bc-115">-BatchContext</span></span>
<span data-ttu-id="709bc-116">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="709bc-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="709bc-117">구독에 대 한 선택 키를 포함 하는 **Batchaccountcontext** 개체를 가져오려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="709bc-117">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="709bc-118">-작업</span><span class="sxs-lookup"><span data-stu-id="709bc-118">-Task</span></span>
<span data-ttu-id="709bc-119">이 cmdlet이 일괄 처리 서비스를 업데이트 하는 **Pscloudtask** 를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="709bc-119">Specifies the **PSCloudTask** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="709bc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="709bc-120">-DefaultProfile</span></span>
<span data-ttu-id="709bc-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="709bc-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="709bc-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="709bc-122">CommonParameters</span></span>
<span data-ttu-id="709bc-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="709bc-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="709bc-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="709bc-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="709bc-125">입력</span><span class="sxs-lookup"><span data-stu-id="709bc-125">INPUTS</span></span>

### <span data-ttu-id="709bc-126">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="709bc-126">BatchAccountContext</span></span>
<span data-ttu-id="709bc-127">' BatchContext ' 매개 변수는 파이프라인에서 ' BatchAccountContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="709bc-127">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="709bc-128">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="709bc-128">PSCloudTask</span></span>
<span data-ttu-id="709bc-129">' Task ' 매개 변수는 파이프라인에서 ' PSCloudTask ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="709bc-129">Parameter 'Task' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="709bc-130">출력</span><span class="sxs-lookup"><span data-stu-id="709bc-130">OUTPUTS</span></span>

## <span data-ttu-id="709bc-131">상속자</span><span class="sxs-lookup"><span data-stu-id="709bc-131">NOTES</span></span>

## <span data-ttu-id="709bc-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="709bc-132">RELATED LINKS</span></span>

[<span data-ttu-id="709bc-133">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="709bc-133">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="709bc-134">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="709bc-134">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="709bc-135">새-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="709bc-135">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="709bc-136">-AzureBatchTask 제거</span><span class="sxs-lookup"><span data-stu-id="709bc-136">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="709bc-137">중지-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="709bc-137">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)

[<span data-ttu-id="709bc-138">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="709bc-138">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


