---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 67FB5D02-4F4B-4119-B3AC-0D205247253E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchTask.md
ms.openlocfilehash: 8e7636d83b953997ac1f9269e45fbf3c2278612f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711621"
---
# <span data-ttu-id="bdbac-101">Enable-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="bdbac-101">Enable-AzureBatchTask</span></span>

## <span data-ttu-id="bdbac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bdbac-102">SYNOPSIS</span></span>
<span data-ttu-id="bdbac-103">작업을 다시 활성화 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdbac-103">Reactivates a task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bdbac-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bdbac-104">SYNTAX</span></span>

### <span data-ttu-id="bdbac-105">I</span><span class="sxs-lookup"><span data-stu-id="bdbac-105">Id</span></span>
```
Enable-AzureBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdbac-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="bdbac-106">InputObject</span></span>
```
Enable-AzureBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bdbac-107">설명은</span><span class="sxs-lookup"><span data-stu-id="bdbac-107">DESCRIPTION</span></span>
<span data-ttu-id="bdbac-108">**-AzureBatchTask** Cmdlet을 사용 하 여 작업을 다시 활성화 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdbac-108">The **Enable-AzureBatchTask** cmdlet reactivates a task.</span></span>
<span data-ttu-id="bdbac-109">작업의 재시도 횟수가 모두 있는 경우이 cmdlet을 사용 하 여 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bdbac-109">If a task has exhausted its retry count, this cmdlet nevertheless enables it to run.</span></span>

## <span data-ttu-id="bdbac-110">예제의</span><span class="sxs-lookup"><span data-stu-id="bdbac-110">EXAMPLES</span></span>

### <span data-ttu-id="bdbac-111">예제 1: 작업 다시 활성화</span><span class="sxs-lookup"><span data-stu-id="bdbac-111">Example 1: Reactivate a task</span></span>
```
PS C:\>Enable-AzureBatchTask -JobId "Job7" -Id "Task2" -BatchContext $Context
```

<span data-ttu-id="bdbac-112">이 명령은 작업 Job7에서 작업 Task2를 다시 활성화 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdbac-112">This command reactivates the task Task2 in job Job7.</span></span>

### <span data-ttu-id="bdbac-113">예제 2: 파이프라인을 사용 하 여 작업 다시 활성화</span><span class="sxs-lookup"><span data-stu-id="bdbac-113">Example 2: Reactivate a task by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job8" -Id "Task3" -BatchContext $Context | Enable-AzureBatchTask -BatchContext $Context
```

<span data-ttu-id="bdbac-114">이 명령은 Get-AzureBatchTask cmdlet을 사용 하 여 ID Job8 있는 작업에서 ID Task3이 있는 일괄 처리 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bdbac-114">This command gets the Batch task that has the ID Task3 in the job that has the ID Job8 by using the Get-AzureBatchTask cmdlet.</span></span>
<span data-ttu-id="bdbac-115">이 명령은 파이프라인 연산자를 사용 하 여 해당 작업을 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdbac-115">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="bdbac-116">명령이 해당 작업을 다시 활성화 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdbac-116">The command reactivates that task.</span></span>

## <span data-ttu-id="bdbac-117">변수</span><span class="sxs-lookup"><span data-stu-id="bdbac-117">PARAMETERS</span></span>

### <span data-ttu-id="bdbac-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="bdbac-118">-BatchContext</span></span>
<span data-ttu-id="bdbac-119">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdbac-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="bdbac-120">구독에 대 한 선택 키를 포함 하는 **Batchaccountcontext** 개체를 가져오려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdbac-120">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="bdbac-121">-Id</span><span class="sxs-lookup"><span data-stu-id="bdbac-121">-Id</span></span>
<span data-ttu-id="bdbac-122">다시 활성화할 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdbac-122">Specifies the ID of the task to reactivate.</span></span>

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

### <span data-ttu-id="bdbac-123">-JobId</span><span class="sxs-lookup"><span data-stu-id="bdbac-123">-JobId</span></span>
<span data-ttu-id="bdbac-124">작업을 포함 하는 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdbac-124">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="bdbac-125">-작업</span><span class="sxs-lookup"><span data-stu-id="bdbac-125">-Task</span></span>
<span data-ttu-id="bdbac-126">이 cmdlet이 다시 활성화 하는 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdbac-126">Specifies the task that this cmdlet reactivates.</span></span>
<span data-ttu-id="bdbac-127">**Pscloudtask** 개체를 가져오려면 Get-AzureBatchTask cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdbac-127">To obtain a **PSCloudTask** object, use the Get-AzureBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="bdbac-128">-확인</span><span class="sxs-lookup"><span data-stu-id="bdbac-128">-Confirm</span></span>
<span data-ttu-id="bdbac-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdbac-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdbac-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdbac-130">-WhatIf</span></span>
<span data-ttu-id="bdbac-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="bdbac-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bdbac-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bdbac-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdbac-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdbac-133">-DefaultProfile</span></span>
<span data-ttu-id="bdbac-134">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bdbac-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bdbac-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdbac-135">CommonParameters</span></span>
<span data-ttu-id="bdbac-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdbac-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdbac-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdbac-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdbac-138">입력</span><span class="sxs-lookup"><span data-stu-id="bdbac-138">INPUTS</span></span>

### <span data-ttu-id="bdbac-139">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="bdbac-139">BatchAccountContext</span></span>
<span data-ttu-id="bdbac-140">' BatchContext ' 매개 변수는 파이프라인에서 ' BatchAccountContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdbac-140">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="bdbac-141">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="bdbac-141">PSCloudTask</span></span>
<span data-ttu-id="bdbac-142">' Task ' 매개 변수는 파이프라인에서 ' PSCloudTask ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdbac-142">Parameter 'Task' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="bdbac-143">출력</span><span class="sxs-lookup"><span data-stu-id="bdbac-143">OUTPUTS</span></span>

## <span data-ttu-id="bdbac-144">상속자</span><span class="sxs-lookup"><span data-stu-id="bdbac-144">NOTES</span></span>

## <span data-ttu-id="bdbac-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bdbac-145">RELATED LINKS</span></span>

[<span data-ttu-id="bdbac-146">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="bdbac-146">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="bdbac-147">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="bdbac-147">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="bdbac-148">새-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="bdbac-148">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="bdbac-149">-AzureBatchTask 제거</span><span class="sxs-lookup"><span data-stu-id="bdbac-149">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="bdbac-150">Set-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="bdbac-150">Set-AzureBatchTask</span></span>](./Set-AzureBatchTask.md)

[<span data-ttu-id="bdbac-151">중지-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="bdbac-151">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)


