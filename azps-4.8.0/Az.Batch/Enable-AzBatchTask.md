---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 67FB5D02-4F4B-4119-B3AC-0D205247253E
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchTask.md
ms.openlocfilehash: 9979a0fa16b8cfbe59eb8412a76cbbebcb2fca4a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204086"
---
# <span data-ttu-id="0d4fb-101">Enable-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="0d4fb-101">Enable-AzBatchTask</span></span>

## <span data-ttu-id="0d4fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d4fb-102">SYNOPSIS</span></span>
<span data-ttu-id="0d4fb-103">작업을 다시 활성화 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d4fb-103">Reactivates a task.</span></span>

## <span data-ttu-id="0d4fb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0d4fb-104">SYNTAX</span></span>

### <span data-ttu-id="0d4fb-105">I</span><span class="sxs-lookup"><span data-stu-id="0d4fb-105">Id</span></span>
```
Enable-AzBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d4fb-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="0d4fb-106">InputObject</span></span>
```
Enable-AzBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d4fb-107">설명은</span><span class="sxs-lookup"><span data-stu-id="0d4fb-107">DESCRIPTION</span></span>
<span data-ttu-id="0d4fb-108">AzBatchTask cmdlet을 **사용** 하 여 작업을 다시 활성화 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d4fb-108">The **Enable-AzBatchTask** cmdlet reactivates a task.</span></span>
<span data-ttu-id="0d4fb-109">작업의 재시도 횟수가 모두 있는 경우이 cmdlet을 사용 하 여 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d4fb-109">If a task has exhausted its retry count, this cmdlet nevertheless enables it to run.</span></span>

## <span data-ttu-id="0d4fb-110">예제의</span><span class="sxs-lookup"><span data-stu-id="0d4fb-110">EXAMPLES</span></span>

### <span data-ttu-id="0d4fb-111">예제 1: 작업 다시 활성화</span><span class="sxs-lookup"><span data-stu-id="0d4fb-111">Example 1: Reactivate a task</span></span>
```
PS C:\>Enable-AzBatchTask -JobId "Job7" -Id "Task2" -BatchContext $Context
```

<span data-ttu-id="0d4fb-112">이 명령은 작업 Job7에서 작업 Task2를 다시 활성화 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d4fb-112">This command reactivates the task Task2 in job Job7.</span></span>

### <span data-ttu-id="0d4fb-113">예제 2: 파이프라인을 사용 하 여 작업 다시 활성화</span><span class="sxs-lookup"><span data-stu-id="0d4fb-113">Example 2: Reactivate a task by using the pipeline</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job8" -Id "Task3" -BatchContext $Context | Enable-AzBatchTask -BatchContext $Context
```

<span data-ttu-id="0d4fb-114">이 명령은 Get-AzBatchTask cmdlet을 사용 하 여 ID Job8 있는 작업에서 ID Task3이 있는 일괄 처리 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0d4fb-114">This command gets the Batch task that has the ID Task3 in the job that has the ID Job8 by using the Get-AzBatchTask cmdlet.</span></span>
<span data-ttu-id="0d4fb-115">이 명령은 파이프라인 연산자를 사용 하 여 해당 작업을 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d4fb-115">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="0d4fb-116">명령이 해당 작업을 다시 활성화 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d4fb-116">The command reactivates that task.</span></span>

## <span data-ttu-id="0d4fb-117">변수</span><span class="sxs-lookup"><span data-stu-id="0d4fb-117">PARAMETERS</span></span>

### <span data-ttu-id="0d4fb-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="0d4fb-118">-BatchContext</span></span>
<span data-ttu-id="0d4fb-119">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d4fb-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="0d4fb-120">Get-AzBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d4fb-120">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="0d4fb-121">대신 공유 키 인증을 사용 하려면 Get-AzBatchAccountKey cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0d4fb-121">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="0d4fb-122">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d4fb-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="0d4fb-123">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d4fb-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="0d4fb-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d4fb-124">-DefaultProfile</span></span>
<span data-ttu-id="0d4fb-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0d4fb-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d4fb-126">-Id</span><span class="sxs-lookup"><span data-stu-id="0d4fb-126">-Id</span></span>
<span data-ttu-id="0d4fb-127">다시 활성화할 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d4fb-127">Specifies the ID of the task to reactivate.</span></span>

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

### <span data-ttu-id="0d4fb-128">-JobId</span><span class="sxs-lookup"><span data-stu-id="0d4fb-128">-JobId</span></span>
<span data-ttu-id="0d4fb-129">작업을 포함 하는 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d4fb-129">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="0d4fb-130">-작업</span><span class="sxs-lookup"><span data-stu-id="0d4fb-130">-Task</span></span>
<span data-ttu-id="0d4fb-131">이 cmdlet이 다시 활성화 하는 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d4fb-131">Specifies the task that this cmdlet reactivates.</span></span>
<span data-ttu-id="0d4fb-132">**Pscloudtask** 개체를 가져오려면 Get-AzBatchTask cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d4fb-132">To obtain a **PSCloudTask** object, use the Get-AzBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="0d4fb-133">-확인</span><span class="sxs-lookup"><span data-stu-id="0d4fb-133">-Confirm</span></span>
<span data-ttu-id="0d4fb-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d4fb-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d4fb-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d4fb-135">-WhatIf</span></span>
<span data-ttu-id="0d4fb-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0d4fb-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d4fb-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0d4fb-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d4fb-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d4fb-138">CommonParameters</span></span>
<span data-ttu-id="0d4fb-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d4fb-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d4fb-140">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0d4fb-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d4fb-141">입력</span><span class="sxs-lookup"><span data-stu-id="0d4fb-141">INPUTS</span></span>

### <span data-ttu-id="0d4fb-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0d4fb-142">System.String</span></span>

### <span data-ttu-id="0d4fb-143">Microsoft.Azure.Commands.Batch. PSCloudTask에 대 한 모델</span><span class="sxs-lookup"><span data-stu-id="0d4fb-143">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="0d4fb-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="0d4fb-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="0d4fb-145">출력</span><span class="sxs-lookup"><span data-stu-id="0d4fb-145">OUTPUTS</span></span>

### <span data-ttu-id="0d4fb-146">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="0d4fb-146">System.Void</span></span>

## <span data-ttu-id="0d4fb-147">상속자</span><span class="sxs-lookup"><span data-stu-id="0d4fb-147">NOTES</span></span>

## <span data-ttu-id="0d4fb-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0d4fb-148">RELATED LINKS</span></span>

[<span data-ttu-id="0d4fb-149">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="0d4fb-149">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="0d4fb-150">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="0d4fb-150">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="0d4fb-151">새로운 AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="0d4fb-151">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="0d4fb-152">제거-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="0d4fb-152">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="0d4fb-153">Set-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="0d4fb-153">Set-AzBatchTask</span></span>](./Set-AzBatchTask.md)

[<span data-ttu-id="0d4fb-154">중지-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="0d4fb-154">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)


