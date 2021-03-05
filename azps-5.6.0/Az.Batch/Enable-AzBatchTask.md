---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 67FB5D02-4F4B-4119-B3AC-0D205247253E
online version: https://docs.microsoft.com/powershell/module/az.batch/enable-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchTask.md
ms.openlocfilehash: 902c7ab5f6125716e03e846a4f1ebc3925aae43f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988507"
---
# <span data-ttu-id="fd213-101">Enable-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="fd213-101">Enable-AzBatchTask</span></span>

## <span data-ttu-id="fd213-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd213-102">SYNOPSIS</span></span>
<span data-ttu-id="fd213-103">작업을 다시 활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="fd213-103">Reactivates a task.</span></span>

## <span data-ttu-id="fd213-104">구문</span><span class="sxs-lookup"><span data-stu-id="fd213-104">SYNTAX</span></span>

### <span data-ttu-id="fd213-105">ID</span><span class="sxs-lookup"><span data-stu-id="fd213-105">Id</span></span>
```
Enable-AzBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd213-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="fd213-106">InputObject</span></span>
```
Enable-AzBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd213-107">설명</span><span class="sxs-lookup"><span data-stu-id="fd213-107">DESCRIPTION</span></span>
<span data-ttu-id="fd213-108">**Enable-AzBatchTask** cmdlet이 작업을 다시 활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="fd213-108">The **Enable-AzBatchTask** cmdlet reactivates a task.</span></span>
<span data-ttu-id="fd213-109">태스크가 재시도 수를 소진한 경우 이 cmdlet을 사용하면 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd213-109">If a task has exhausted its retry count, this cmdlet nevertheless enables it to run.</span></span>

## <span data-ttu-id="fd213-110">예제</span><span class="sxs-lookup"><span data-stu-id="fd213-110">EXAMPLES</span></span>

### <span data-ttu-id="fd213-111">예제 1: 작업 다시 활성화</span><span class="sxs-lookup"><span data-stu-id="fd213-111">Example 1: Reactivate a task</span></span>
```
PS C:\>Enable-AzBatchTask -JobId "Job7" -Id "Task2" -BatchContext $Context
```

<span data-ttu-id="fd213-112">이 명령은 job Job7에서 Task2 작업을 다시 활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="fd213-112">This command reactivates the task Task2 in job Job7.</span></span>

### <span data-ttu-id="fd213-113">예제 2: 파이프라인을 사용하여 작업 다시 활성화</span><span class="sxs-lookup"><span data-stu-id="fd213-113">Example 2: Reactivate a task by using the pipeline</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job8" -Id "Task3" -BatchContext $Context | Enable-AzBatchTask -BatchContext $Context
```

<span data-ttu-id="fd213-114">이 명령은 id Job8이 있는 작업에 id Task3가 있는 batch 작업을 Get-AzBatchTask cmdlet을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="fd213-114">This command gets the Batch task that has the ID Task3 in the job that has the ID Job8 by using the Get-AzBatchTask cmdlet.</span></span>
<span data-ttu-id="fd213-115">명령은 파이프라인 연산자를 사용하여 현재 cmdlet에 이 작업을 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="fd213-115">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="fd213-116">명령은 이 작업을 다시 활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="fd213-116">The command reactivates that task.</span></span>

## <span data-ttu-id="fd213-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="fd213-117">PARAMETERS</span></span>

### <span data-ttu-id="fd213-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="fd213-118">-BatchContext</span></span>
<span data-ttu-id="fd213-119">Batch 서비스와 상호 작용하는 데 이 cmdlet이 사용하는 **BatchAccountContext** 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fd213-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="fd213-120">Get-AzBatchAccount cmdlet을 사용하여 BatchAccountContext를 얻으면 Batch 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="fd213-120">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="fd213-121">대신 공유 키 인증을 사용 Get-AzBatchAccountKey cmdlet을 사용하여 액세스 키가 채워진 BatchAccountContext 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="fd213-121">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="fd213-122">공유 키 인증을 사용하는 경우 기본 액세스 키는 기본적으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="fd213-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="fd213-123">사용할 키를 변경하기 위해 BatchAccountContext.KeyInUse 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="fd213-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="fd213-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd213-124">-DefaultProfile</span></span>
<span data-ttu-id="fd213-125">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fd213-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd213-126">-Id</span><span class="sxs-lookup"><span data-stu-id="fd213-126">-Id</span></span>
<span data-ttu-id="fd213-127">다시 활성화할 작업의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fd213-127">Specifies the ID of the task to reactivate.</span></span>

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

### <span data-ttu-id="fd213-128">-JobId</span><span class="sxs-lookup"><span data-stu-id="fd213-128">-JobId</span></span>
<span data-ttu-id="fd213-129">작업을 포함하는 작업의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fd213-129">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="fd213-130">-Task</span><span class="sxs-lookup"><span data-stu-id="fd213-130">-Task</span></span>
<span data-ttu-id="fd213-131">이 cmdlet이 다시 활성화하는 작업을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fd213-131">Specifies the task that this cmdlet reactivates.</span></span>
<span data-ttu-id="fd213-132">**PSCloudTask** 개체를 얻은 경우 Get-AzBatchTask cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="fd213-132">To obtain a **PSCloudTask** object, use the Get-AzBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="fd213-133">-확인</span><span class="sxs-lookup"><span data-stu-id="fd213-133">-Confirm</span></span>
<span data-ttu-id="fd213-134">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fd213-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd213-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd213-135">-WhatIf</span></span>
<span data-ttu-id="fd213-136">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="fd213-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd213-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fd213-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd213-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd213-138">CommonParameters</span></span>
<span data-ttu-id="fd213-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fd213-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd213-140">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fd213-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd213-141">입력</span><span class="sxs-lookup"><span data-stu-id="fd213-141">INPUTS</span></span>

### <span data-ttu-id="fd213-142">System.String</span><span class="sxs-lookup"><span data-stu-id="fd213-142">System.String</span></span>

### <span data-ttu-id="fd213-143">Microsoft.Azure.Commands.Bat. Models.PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="fd213-143">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="fd213-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="fd213-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="fd213-145">출력</span><span class="sxs-lookup"><span data-stu-id="fd213-145">OUTPUTS</span></span>

### <span data-ttu-id="fd213-146">System.Void</span><span class="sxs-lookup"><span data-stu-id="fd213-146">System.Void</span></span>

## <span data-ttu-id="fd213-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fd213-147">NOTES</span></span>

## <span data-ttu-id="fd213-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fd213-148">RELATED LINKS</span></span>

[<span data-ttu-id="fd213-149">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="fd213-149">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="fd213-150">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="fd213-150">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="fd213-151">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="fd213-151">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="fd213-152">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="fd213-152">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="fd213-153">Set-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="fd213-153">Set-AzBatchTask</span></span>](./Set-AzBatchTask.md)

[<span data-ttu-id="fd213-154">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="fd213-154">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)


