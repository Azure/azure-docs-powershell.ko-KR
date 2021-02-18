---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D79AEF8C-F0DC-40F8-9EEE-A2BB6AE5C4BF
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchTask.md
ms.openlocfilehash: e067eea86e3a4350d08c5c0f9ec34b4af65b07f8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200988"
---
# <span data-ttu-id="40508-101">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="40508-101">Remove-AzBatchTask</span></span>

## <span data-ttu-id="40508-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40508-102">SYNOPSIS</span></span>
<span data-ttu-id="40508-103">Batch 작업을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="40508-103">Deletes a Batch task.</span></span>

## <span data-ttu-id="40508-104">구문</span><span class="sxs-lookup"><span data-stu-id="40508-104">SYNTAX</span></span>

### <span data-ttu-id="40508-105">ID</span><span class="sxs-lookup"><span data-stu-id="40508-105">Id</span></span>
```
Remove-AzBatchTask [-JobId] <String> [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40508-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="40508-106">InputObject</span></span>
```
Remove-AzBatchTask [-InputObject] <PSCloudTask> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40508-107">설명</span><span class="sxs-lookup"><span data-stu-id="40508-107">DESCRIPTION</span></span>
<span data-ttu-id="40508-108">**Remove-AzBatchTask** cmdlet은 Azure Batch 작업을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="40508-108">The **Remove-AzBatchTask** cmdlet deletes an Azure Batch task.</span></span>
<span data-ttu-id="40508-109">이 cmdlet은 Force 매개 변수를 지정하지 않는 한 확인을 *요청하는 메시지를* 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="40508-109">This cmdlet prompts you for confirmation, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="40508-110">예제</span><span class="sxs-lookup"><span data-stu-id="40508-110">EXAMPLES</span></span>

### <span data-ttu-id="40508-111">예제 1: ID로 Batch 작업 삭제</span><span class="sxs-lookup"><span data-stu-id="40508-111">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Remove-AzBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="40508-112">이 명령은 ID Job-000001이 있는 작업 아래에 ID Task23이 있는 태스크를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="40508-112">This command deletes a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="40508-113">이 명령은 확인을 요청하는 메시지를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="40508-113">The command prompts you for confirmation.</span></span>
<span data-ttu-id="40508-114">**Get-AzBatchAccountKey** cmdlet을 사용하여 $Context 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="40508-114">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="40508-115">예제 2: 확인 없이 파이프라인을 사용하여 Batch 작업 삭제</span><span class="sxs-lookup"><span data-stu-id="40508-115">Example 2: Delete a Batch task by using the pipeline without confirmation</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Remove-AzBatchTask -Force -BatchContext $Context
```

<span data-ttu-id="40508-116">이 명령은 **Get-AzBatchTask** cmdlet을 사용하여 ID Job-000001이 있는 작업에 ID Task26이 있는 Batch 태스크를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="40508-116">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the **Get-AzBatchTask** cmdlet.</span></span>
<span data-ttu-id="40508-117">이 명령은 파이프라인 연산자를 사용하여 이 작업을 현재 cmdlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="40508-117">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="40508-118">이 명령은 해당 작업을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="40508-118">The command deletes that task.</span></span>
<span data-ttu-id="40508-119">이 명령은 Force 매개 *변수를 지정합니다.*</span><span class="sxs-lookup"><span data-stu-id="40508-119">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="40508-120">따라서 명령은 확인을 요청하는 메시지를 표시하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="40508-120">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="40508-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="40508-121">PARAMETERS</span></span>

### <span data-ttu-id="40508-122">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="40508-122">-BatchContext</span></span>
<span data-ttu-id="40508-123">이 cmdlet이 Batch 서비스와 상호 작용하는 데 사용하는 **BatchAccountContext** 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="40508-123">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="40508-124">Get-AzBatchAccount cmdlet을 사용하여 BatchAccountContext를 얻으면 Batch 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="40508-124">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="40508-125">대신 공유 키 인증을 사용Get-AzBatchAccountKey cmdlet을 사용하여 액세스 키가 채워진 BatchAccountContext 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="40508-125">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="40508-126">공유 키 인증을 사용하는 경우 기본 액세스 키가 기본적으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="40508-126">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="40508-127">사용할 키를 변경하기 위해 BatchAccountContext.KeyInUse 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="40508-127">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="40508-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40508-128">-DefaultProfile</span></span>
<span data-ttu-id="40508-129">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="40508-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40508-130">-Force</span><span class="sxs-lookup"><span data-stu-id="40508-130">-Force</span></span>
<span data-ttu-id="40508-131">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="40508-131">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40508-132">-Id</span><span class="sxs-lookup"><span data-stu-id="40508-132">-Id</span></span>
<span data-ttu-id="40508-133">이 cmdlet이 삭제하는 작업의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="40508-133">Specifies the ID of the task that this cmdlet deletes.</span></span>
<span data-ttu-id="40508-134">와일드카드 문자는 지정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="40508-134">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="40508-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="40508-135">-InputObject</span></span>
<span data-ttu-id="40508-136">이 cmdlet이 삭제하는 작업을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="40508-136">Specifies the task that this cmdlet deletes.</span></span>
<span data-ttu-id="40508-137">**PSCloudTask** 개체를 얻습니다. Get-AzBatchTask cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="40508-137">To obtain a **PSCloudTask** object, use  the Get-AzBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="40508-138">-JobId</span><span class="sxs-lookup"><span data-stu-id="40508-138">-JobId</span></span>
<span data-ttu-id="40508-139">태스크를 포함하는 작업의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="40508-139">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="40508-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="40508-140">-Confirm</span></span>
<span data-ttu-id="40508-141">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="40508-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40508-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40508-142">-WhatIf</span></span>
<span data-ttu-id="40508-143">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="40508-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40508-144">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="40508-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40508-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40508-145">CommonParameters</span></span>
<span data-ttu-id="40508-146">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="40508-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40508-147">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="40508-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40508-148">입력</span><span class="sxs-lookup"><span data-stu-id="40508-148">INPUTS</span></span>

### <span data-ttu-id="40508-149">System.String</span><span class="sxs-lookup"><span data-stu-id="40508-149">System.String</span></span>

### <span data-ttu-id="40508-150">Microsoft.Azure.Commands.Batch. Models.PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="40508-150">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="40508-151">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="40508-151">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="40508-152">출력</span><span class="sxs-lookup"><span data-stu-id="40508-152">OUTPUTS</span></span>

### <span data-ttu-id="40508-153">System.Void</span><span class="sxs-lookup"><span data-stu-id="40508-153">System.Void</span></span>

## <span data-ttu-id="40508-154">참고 사항</span><span class="sxs-lookup"><span data-stu-id="40508-154">NOTES</span></span>

## <span data-ttu-id="40508-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="40508-155">RELATED LINKS</span></span>

[<span data-ttu-id="40508-156">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="40508-156">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="40508-157">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="40508-157">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="40508-158">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="40508-158">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="40508-159">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="40508-159">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="40508-160">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="40508-160">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="40508-161">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="40508-161">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
