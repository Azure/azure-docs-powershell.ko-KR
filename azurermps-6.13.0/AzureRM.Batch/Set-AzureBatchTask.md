---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 6A6D6C7D-EED7-4AD4-ACE6-BFA64404455E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchTask.md
ms.openlocfilehash: bae5f2b075f8d4f2fa579b38bdccf160cd46caad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702122"
---
# <span data-ttu-id="4cc3e-101">Set-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="4cc3e-101">Set-AzureBatchTask</span></span>

## <span data-ttu-id="4cc3e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4cc3e-102">SYNOPSIS</span></span>
<span data-ttu-id="4cc3e-103">작업의 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3e-103">Updates the properties of a task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4cc3e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4cc3e-104">SYNTAX</span></span>

```
Set-AzureBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4cc3e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4cc3e-105">DESCRIPTION</span></span>
<span data-ttu-id="4cc3e-106">**Set-AzureBatchTask** Cmdlet은 Azure 일괄 처리 서비스에서 작업의 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3e-106">The **Set-AzureBatchTask** cmdlet updates the properties of a task in the Azure Batch service.</span></span>
<span data-ttu-id="4cc3e-107">**Pscloudtask** 개체를 가져오려면 Get-AzureBatchTask cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3e-107">Use the Get-AzureBatchTask cmdlet to get a **PSCloudTask** object.</span></span>
<span data-ttu-id="4cc3e-108">해당 개체의 속성을 수정한 다음 현재 cmdlet을 사용 하 여 일괄 처리 서비스에 대 한 변경 내용을 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3e-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="4cc3e-109">예제의</span><span class="sxs-lookup"><span data-stu-id="4cc3e-109">EXAMPLES</span></span>

### <span data-ttu-id="4cc3e-110">예제 1: 작업 업데이트</span><span class="sxs-lookup"><span data-stu-id="4cc3e-110">Example 1: Update a task</span></span>
```
PS C:\>$Task = Get-AzureBatchTask -JobId "Job16" -Id "Task22" -BatchContext $Context
PS C:\> $Constraints = New-Object Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints -ArgumentList @([TimeSpan}::FromDays(5), [TimeSpan]::FromDays(2), 3)
PS C:\> $Task.Constraints = $Constraints
PS C:\> Set-AzureBatchTask -Task $Task -BatchContext $Context
```

<span data-ttu-id="4cc3e-111">첫 번째 명령은 **가져오기-AzureBatchTask** 를 사용 하 여 작업을 가져온 다음 $Task 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3e-111">The first command gets a task by using **Get-AzureBatchTask** , and then stores it in the $Task variable.</span></span>
<span data-ttu-id="4cc3e-112">다음 두 명령은 $Task 작업의 제약 조건을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3e-112">The next two commands modify the constraints of the task in $Task.</span></span>
<span data-ttu-id="4cc3e-113">마지막 명령은 $Task의 로컬 개체와 일치 하도록 일괄 처리 서비스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3e-113">The final command updates the Batch service to match the local object in $Task.</span></span>

## <span data-ttu-id="4cc3e-114">변수</span><span class="sxs-lookup"><span data-stu-id="4cc3e-114">PARAMETERS</span></span>

### <span data-ttu-id="4cc3e-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="4cc3e-115">-BatchContext</span></span>
<span data-ttu-id="4cc3e-116">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3e-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="4cc3e-117">Get-AzureRmBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3e-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="4cc3e-118">대신 공유 키 인증을 사용 하려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3e-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="4cc3e-119">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3e-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="4cc3e-120">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3e-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="4cc3e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cc3e-121">-DefaultProfile</span></span>
<span data-ttu-id="4cc3e-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3e-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4cc3e-123">-작업</span><span class="sxs-lookup"><span data-stu-id="4cc3e-123">-Task</span></span>
<span data-ttu-id="4cc3e-124">이 cmdlet이 일괄 처리 서비스를 업데이트 하는 **Pscloudtask** 를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3e-124">Specifies the **PSCloudTask** to which this cmdlet updates the Batch service.</span></span>

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

### <span data-ttu-id="4cc3e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cc3e-125">CommonParameters</span></span>
<span data-ttu-id="4cc3e-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cc3e-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cc3e-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cc3e-128">입력</span><span class="sxs-lookup"><span data-stu-id="4cc3e-128">INPUTS</span></span>

### <span data-ttu-id="4cc3e-129">Microsoft.Azure.Commands.Batch. PSCloudTask에 대 한 모델</span><span class="sxs-lookup"><span data-stu-id="4cc3e-129">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>
<span data-ttu-id="4cc3e-130">매개 변수: 작업 (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4cc3e-130">Parameters: Task (ByValue)</span></span>

### <span data-ttu-id="4cc3e-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="4cc3e-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="4cc3e-132">매개 변수: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4cc3e-132">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="4cc3e-133">출력</span><span class="sxs-lookup"><span data-stu-id="4cc3e-133">OUTPUTS</span></span>

### <span data-ttu-id="4cc3e-134">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="4cc3e-134">System.Void</span></span>

## <span data-ttu-id="4cc3e-135">상속자</span><span class="sxs-lookup"><span data-stu-id="4cc3e-135">NOTES</span></span>

## <span data-ttu-id="4cc3e-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4cc3e-136">RELATED LINKS</span></span>

[<span data-ttu-id="4cc3e-137">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="4cc3e-137">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="4cc3e-138">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="4cc3e-138">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="4cc3e-139">새-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="4cc3e-139">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="4cc3e-140">-AzureBatchTask 제거</span><span class="sxs-lookup"><span data-stu-id="4cc3e-140">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="4cc3e-141">중지-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="4cc3e-141">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)

[<span data-ttu-id="4cc3e-142">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="4cc3e-142">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)

