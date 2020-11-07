---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 67FB5D02-4F4B-4119-B3AC-0D205247253E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/enable-azurebatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchTask.md
ms.openlocfilehash: 09e2c8dd4ce1eab68eb2a4237e022034696f9769
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93704036"
---
# <span data-ttu-id="c1ed7-101">Enable-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="c1ed7-101">Enable-AzureBatchTask</span></span>

## <span data-ttu-id="c1ed7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1ed7-102">SYNOPSIS</span></span>
<span data-ttu-id="c1ed7-103">작업을 다시 활성화 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1ed7-103">Reactivates a task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1ed7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c1ed7-104">SYNTAX</span></span>

### <span data-ttu-id="c1ed7-105">I</span><span class="sxs-lookup"><span data-stu-id="c1ed7-105">Id</span></span>
```
Enable-AzureBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1ed7-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="c1ed7-106">InputObject</span></span>
```
Enable-AzureBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1ed7-107">설명은</span><span class="sxs-lookup"><span data-stu-id="c1ed7-107">DESCRIPTION</span></span>
<span data-ttu-id="c1ed7-108">**-AzureBatchTask** Cmdlet을 사용 하 여 작업을 다시 활성화 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1ed7-108">The **Enable-AzureBatchTask** cmdlet reactivates a task.</span></span>
<span data-ttu-id="c1ed7-109">작업의 재시도 횟수가 모두 있는 경우이 cmdlet을 사용 하 여 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c1ed7-109">If a task has exhausted its retry count, this cmdlet nevertheless enables it to run.</span></span>

## <span data-ttu-id="c1ed7-110">예제의</span><span class="sxs-lookup"><span data-stu-id="c1ed7-110">EXAMPLES</span></span>

### <span data-ttu-id="c1ed7-111">예제 1: 작업 다시 활성화</span><span class="sxs-lookup"><span data-stu-id="c1ed7-111">Example 1: Reactivate a task</span></span>
```
PS C:\>Enable-AzureBatchTask -JobId "Job7" -Id "Task2" -BatchContext $Context
```

<span data-ttu-id="c1ed7-112">이 명령은 작업 Job7에서 작업 Task2를 다시 활성화 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1ed7-112">This command reactivates the task Task2 in job Job7.</span></span>

### <span data-ttu-id="c1ed7-113">예제 2: 파이프라인을 사용 하 여 작업 다시 활성화</span><span class="sxs-lookup"><span data-stu-id="c1ed7-113">Example 2: Reactivate a task by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job8" -Id "Task3" -BatchContext $Context | Enable-AzureBatchTask -BatchContext $Context
```

<span data-ttu-id="c1ed7-114">이 명령은 Get-AzureBatchTask cmdlet을 사용 하 여 ID Job8 있는 작업에서 ID Task3이 있는 일괄 처리 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c1ed7-114">This command gets the Batch task that has the ID Task3 in the job that has the ID Job8 by using the Get-AzureBatchTask cmdlet.</span></span>
<span data-ttu-id="c1ed7-115">이 명령은 파이프라인 연산자를 사용 하 여 해당 작업을 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1ed7-115">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c1ed7-116">명령이 해당 작업을 다시 활성화 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1ed7-116">The command reactivates that task.</span></span>

## <span data-ttu-id="c1ed7-117">변수</span><span class="sxs-lookup"><span data-stu-id="c1ed7-117">PARAMETERS</span></span>

### <span data-ttu-id="c1ed7-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="c1ed7-118">-BatchContext</span></span>
<span data-ttu-id="c1ed7-119">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1ed7-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c1ed7-120">Get-AzureRmBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c1ed7-120">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="c1ed7-121">대신 공유 키 인증을 사용 하려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c1ed7-121">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="c1ed7-122">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c1ed7-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="c1ed7-123">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1ed7-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="c1ed7-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1ed7-124">-DefaultProfile</span></span>
<span data-ttu-id="c1ed7-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c1ed7-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1ed7-126">-Id</span><span class="sxs-lookup"><span data-stu-id="c1ed7-126">-Id</span></span>
<span data-ttu-id="c1ed7-127">다시 활성화할 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1ed7-127">Specifies the ID of the task to reactivate.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1ed7-128">-JobId</span><span class="sxs-lookup"><span data-stu-id="c1ed7-128">-JobId</span></span>
<span data-ttu-id="c1ed7-129">작업을 포함 하는 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1ed7-129">Specifies the ID of the job that contains the task.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1ed7-130">-작업</span><span class="sxs-lookup"><span data-stu-id="c1ed7-130">-Task</span></span>
<span data-ttu-id="c1ed7-131">이 cmdlet이 다시 활성화 하는 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1ed7-131">Specifies the task that this cmdlet reactivates.</span></span>
<span data-ttu-id="c1ed7-132">**Pscloudtask** 개체를 가져오려면 Get-AzureBatchTask cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1ed7-132">To obtain a **PSCloudTask** object, use the Get-AzureBatchTask cmdlet.</span></span>

```yaml
Type: PSCloudTask
Parameter Sets: InputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1ed7-133">-확인</span><span class="sxs-lookup"><span data-stu-id="c1ed7-133">-Confirm</span></span>
<span data-ttu-id="c1ed7-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1ed7-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1ed7-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1ed7-135">-WhatIf</span></span>
<span data-ttu-id="c1ed7-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c1ed7-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1ed7-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c1ed7-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1ed7-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1ed7-138">CommonParameters</span></span>
<span data-ttu-id="c1ed7-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1ed7-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1ed7-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1ed7-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1ed7-141">입력</span><span class="sxs-lookup"><span data-stu-id="c1ed7-141">INPUTS</span></span>

### <span data-ttu-id="c1ed7-142">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c1ed7-142">BatchAccountContext</span></span>
<span data-ttu-id="c1ed7-143">' BatchContext ' 매개 변수는 파이프라인에서 ' BatchAccountContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1ed7-143">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="c1ed7-144">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="c1ed7-144">PSCloudTask</span></span>
<span data-ttu-id="c1ed7-145">' Task ' 매개 변수는 파이프라인에서 ' PSCloudTask ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1ed7-145">Parameter 'Task' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="c1ed7-146">출력</span><span class="sxs-lookup"><span data-stu-id="c1ed7-146">OUTPUTS</span></span>

## <span data-ttu-id="c1ed7-147">상속자</span><span class="sxs-lookup"><span data-stu-id="c1ed7-147">NOTES</span></span>

## <span data-ttu-id="c1ed7-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c1ed7-148">RELATED LINKS</span></span>

[<span data-ttu-id="c1ed7-149">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="c1ed7-149">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="c1ed7-150">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="c1ed7-150">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="c1ed7-151">새-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="c1ed7-151">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="c1ed7-152">-AzureBatchTask 제거</span><span class="sxs-lookup"><span data-stu-id="c1ed7-152">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="c1ed7-153">Set-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="c1ed7-153">Set-AzureBatchTask</span></span>](./Set-AzureBatchTask.md)

[<span data-ttu-id="c1ed7-154">중지-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="c1ed7-154">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)


