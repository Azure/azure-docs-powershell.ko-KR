---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 1EA57372-6FA5-45C9-94A1-50D53830FC10
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchTask.md
ms.openlocfilehash: 7e9a7a5dbcb730bb5aa2be653b32ef4c9690e139
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93879974"
---
# <span data-ttu-id="faed7-101">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="faed7-101">Stop-AzBatchTask</span></span>

## <span data-ttu-id="faed7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="faed7-102">SYNOPSIS</span></span>
<span data-ttu-id="faed7-103">일괄 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="faed7-103">Stops a Batch task.</span></span>

## <span data-ttu-id="faed7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="faed7-104">SYNTAX</span></span>

### <span data-ttu-id="faed7-105">I</span><span class="sxs-lookup"><span data-stu-id="faed7-105">Id</span></span>
```
Stop-AzBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="faed7-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="faed7-106">InputObject</span></span>
```
Stop-AzBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="faed7-107">설명은</span><span class="sxs-lookup"><span data-stu-id="faed7-107">DESCRIPTION</span></span>
<span data-ttu-id="faed7-108">**AzBatchTask** Cmdlet은 Azure Batch 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="faed7-108">The **Stop-AzBatchTask** cmdlet stops an Azure Batch task.</span></span>

## <span data-ttu-id="faed7-109">예제의</span><span class="sxs-lookup"><span data-stu-id="faed7-109">EXAMPLES</span></span>

### <span data-ttu-id="faed7-110">예제 1: ID를 기준으로 일괄 작업 삭제</span><span class="sxs-lookup"><span data-stu-id="faed7-110">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Stop-AzBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="faed7-111">이 명령은 ID 작업이 있는 작업 아래에 id Task23 인 작업을 중지 합니다-000001.</span><span class="sxs-lookup"><span data-stu-id="faed7-111">This command stops a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="faed7-112">명령에서 확인 하 라는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="faed7-112">The command prompts you for confirmation.</span></span>
<span data-ttu-id="faed7-113">Get-AzBatchAccountKeys cmdlet을 사용 하 여 컨텍스트를 $Context 변수에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="faed7-113">Use the Get-AzBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="faed7-114">예제 2: 파이프라인을 사용 하 여 일괄 작업 중지</span><span class="sxs-lookup"><span data-stu-id="faed7-114">Example 2: Stop a Batch task by using the pipeline</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Stop-AzBatchTask -BatchContext $Context
```

<span data-ttu-id="faed7-115">이 명령은 Get-AzBatchTask cmdlet을 사용 하 여 ID 작업이 있는 작업에서 ID Task26 인 일괄 처리 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="faed7-115">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the Get-AzBatchTask cmdlet.</span></span>
<span data-ttu-id="faed7-116">이 명령은 파이프라인 연산자를 사용 하 여 해당 작업을 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="faed7-116">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="faed7-117">명령이 해당 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="faed7-117">The command stops that task.</span></span>

## <span data-ttu-id="faed7-118">변수</span><span class="sxs-lookup"><span data-stu-id="faed7-118">PARAMETERS</span></span>

### <span data-ttu-id="faed7-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="faed7-119">-BatchContext</span></span>
<span data-ttu-id="faed7-120">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="faed7-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="faed7-121">Get-AzBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="faed7-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="faed7-122">대신 공유 키 인증을 사용 하려면 Get-AzBatchAccountKeys cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="faed7-122">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="faed7-123">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="faed7-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="faed7-124">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="faed7-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="faed7-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="faed7-125">-DefaultProfile</span></span>
<span data-ttu-id="faed7-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="faed7-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="faed7-127">-Id</span><span class="sxs-lookup"><span data-stu-id="faed7-127">-Id</span></span>
<span data-ttu-id="faed7-128">이 cmdlet이 중지 하는 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="faed7-128">Specifies the ID of the task that this cmdlet stops.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="faed7-129">-JobId</span><span class="sxs-lookup"><span data-stu-id="faed7-129">-JobId</span></span>
<span data-ttu-id="faed7-130">작업을 포함 하는 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="faed7-130">Specifies the ID of the job that contains the task.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="faed7-131">-작업</span><span class="sxs-lookup"><span data-stu-id="faed7-131">-Task</span></span>
<span data-ttu-id="faed7-132">이 cmdlet이 중지 하는 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="faed7-132">Specifies the task that this cmdlet stops.</span></span>
<span data-ttu-id="faed7-133">**Pscloudtask** 개체를 가져오려면 Get-AzBatchTask cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="faed7-133">To obtain a **PSCloudTask** object, use the Get-AzBatchTask cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="faed7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="faed7-134">CommonParameters</span></span>
<span data-ttu-id="faed7-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="faed7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="faed7-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="faed7-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="faed7-137">입력</span><span class="sxs-lookup"><span data-stu-id="faed7-137">INPUTS</span></span>

### <span data-ttu-id="faed7-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="faed7-138">System.String</span></span>

### <span data-ttu-id="faed7-139">Microsoft.Azure.Commands.Batch. PSCloudTask에 대 한 모델</span><span class="sxs-lookup"><span data-stu-id="faed7-139">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="faed7-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="faed7-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="faed7-141">출력</span><span class="sxs-lookup"><span data-stu-id="faed7-141">OUTPUTS</span></span>

### <span data-ttu-id="faed7-142">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="faed7-142">System.Void</span></span>

## <span data-ttu-id="faed7-143">상속자</span><span class="sxs-lookup"><span data-stu-id="faed7-143">NOTES</span></span>

## <span data-ttu-id="faed7-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="faed7-144">RELATED LINKS</span></span>

[<span data-ttu-id="faed7-145">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="faed7-145">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="faed7-146">새로운 AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="faed7-146">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="faed7-147">제거-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="faed7-147">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="faed7-148">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="faed7-148">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


