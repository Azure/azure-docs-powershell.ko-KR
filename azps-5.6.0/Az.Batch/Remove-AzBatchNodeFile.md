---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: DBA02017-8372-4A91-A4F1-985777DEDAB9
online version: https://docs.microsoft.com/powershell/module/az.batch/remove-azbatchnodefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchNodeFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchNodeFile.md
ms.openlocfilehash: a56b8d0613946b33629fda46cc710cdbeef0814e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010891"
---
# <span data-ttu-id="c2fe8-101">Remove-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="c2fe8-101">Remove-AzBatchNodeFile</span></span>

## <span data-ttu-id="c2fe8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2fe8-102">SYNOPSIS</span></span>
<span data-ttu-id="c2fe8-103">작업 또는 계산 노드에 대한 노드 파일을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="c2fe8-103">Deletes a node file for a task or compute node.</span></span>

## <span data-ttu-id="c2fe8-104">구문</span><span class="sxs-lookup"><span data-stu-id="c2fe8-104">SYNTAX</span></span>

### <span data-ttu-id="c2fe8-105">작업</span><span class="sxs-lookup"><span data-stu-id="c2fe8-105">Task</span></span>
```
Remove-AzBatchNodeFile -JobId <String> -TaskId <String> -Path <String> [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c2fe8-106">ComputeNode</span><span class="sxs-lookup"><span data-stu-id="c2fe8-106">ComputeNode</span></span>
```
Remove-AzBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> -Path <String> [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c2fe8-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="c2fe8-107">InputObject</span></span>
```
Remove-AzBatchNodeFile [[-InputObject] <PSNodeFile>] [-Force] [-Recursive] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2fe8-108">설명</span><span class="sxs-lookup"><span data-stu-id="c2fe8-108">DESCRIPTION</span></span>
<span data-ttu-id="c2fe8-109">**Remove-AzBatchNodeFile** cmdlet은 작업 또는 계산 노드에 대한 Azure Batch 노드 파일을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="c2fe8-109">The **Remove-AzBatchNodeFile** cmdlet deletes an Azure Batch node file for a task or compute node.</span></span>

## <span data-ttu-id="c2fe8-110">예제</span><span class="sxs-lookup"><span data-stu-id="c2fe8-110">EXAMPLES</span></span>

### <span data-ttu-id="c2fe8-111">예제 1: 작업과 연결된 파일 삭제</span><span class="sxs-lookup"><span data-stu-id="c2fe8-111">Example 1: Delete a file associated with a task</span></span>
```
PS C:\>Remove-AzBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Path "wd\testFile.txt" -BatchContext $Context
```

<span data-ttu-id="c2fe8-112">이 명령은 이름의 노드 파일을 wd\testFile.txt.</span><span class="sxs-lookup"><span data-stu-id="c2fe8-112">This command deletes the node file that is named wd\testFile.txt.</span></span>
<span data-ttu-id="c2fe8-113">이 파일은 Job-000001 아래에 ID Task26이 있는 작업과 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2fe8-113">That file is associated with the task that has the ID Task26 under the job Job-000001.</span></span>

### <span data-ttu-id="c2fe8-114">예제 2: 계산 노드에서 파일 삭제</span><span class="sxs-lookup"><span data-stu-id="c2fe8-114">Example 2: Delete a file from a compute node</span></span>
```
PS C:\>Remove-AzBatchNodeFile -PoolId "Pool07" -ComputeNodeId "tvm-2316545714_1-20150725t213220z" -Path "startup\testFile.txt" -BatchContext $Context
```

<span data-ttu-id="c2fe8-115">이 명령은 ID pool07이 startup\testFile.txt 풀의 지정된 계산 노드에서 이름의 노드 파일을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="c2fe8-115">This command deletes the node file that is named startup\testFile.txt from the specified compute node in the pool that has the ID Pool07.</span></span>

### <span data-ttu-id="c2fe8-116">예제 3: 파이프라인을 사용하여 파일 제거</span><span class="sxs-lookup"><span data-stu-id="c2fe8-116">Example 3: Remove a file by using the pipeline</span></span>
```
PS C:\>Get-AzBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Path "wd\testFile2.txt" -BatchContext $Context | Remove-AzBatchNodeFile -Force -BatchContext $Context
```

<span data-ttu-id="c2fe8-117">이 명령은 **Get-AzBatchNodeFile** 을 사용하여 노드 파일을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c2fe8-117">This command gets the node file by using **Get-AzBatchNodeFile**.</span></span>
<span data-ttu-id="c2fe8-118">이 파일은 Job-000001 아래에 ID Task26이 있는 작업과 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2fe8-118">That file is associated with the task that has the ID Task26 under the job Job-000001.</span></span>
<span data-ttu-id="c2fe8-119">명령은 파이프라인을 사용하여 해당 파일을 현재 cmdlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="c2fe8-119">The command passes that file to the current cmdlet by using the pipeline.</span></span>
<span data-ttu-id="c2fe8-120">현재 cmdlet은 노드 파일을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c2fe8-120">The current cmdlet removes the node file.</span></span>
<span data-ttu-id="c2fe8-121">명령은 Force 매개 *변수를 지정합니다.*</span><span class="sxs-lookup"><span data-stu-id="c2fe8-121">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="c2fe8-122">따라서 명령을 확인하라는 메시지가 표시되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c2fe8-122">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="c2fe8-123">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c2fe8-123">PARAMETERS</span></span>

### <span data-ttu-id="c2fe8-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="c2fe8-124">-BatchContext</span></span>
<span data-ttu-id="c2fe8-125">Batch 서비스와 상호 작용하는 데 이 cmdlet이 사용하는 **BatchAccountContext** 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c2fe8-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c2fe8-126">Get-AzBatchAccount cmdlet을 사용하여 BatchAccountContext를 얻으면 Batch 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2fe8-126">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="c2fe8-127">대신 공유 키 인증을 사용 Get-AzBatchAccountKey cmdlet을 사용하여 액세스 키가 채워진 BatchAccountContext 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c2fe8-127">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="c2fe8-128">공유 키 인증을 사용하는 경우 기본 액세스 키는 기본적으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2fe8-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="c2fe8-129">사용할 키를 변경하기 위해 BatchAccountContext.KeyInUse 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="c2fe8-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="c2fe8-130">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="c2fe8-130">-ComputeNodeId</span></span>
<span data-ttu-id="c2fe8-131">이 cmdlet이 삭제하는 Batch 노드 파일이 포함된 계산 노드의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c2fe8-131">Specifies the ID of the compute node that contains the Batch node file that this cmdlet deletes.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2fe8-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2fe8-132">-DefaultProfile</span></span>
<span data-ttu-id="c2fe8-133">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c2fe8-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2fe8-134">-Force</span><span class="sxs-lookup"><span data-stu-id="c2fe8-134">-Force</span></span>
<span data-ttu-id="c2fe8-135">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="c2fe8-135">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c2fe8-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c2fe8-136">-InputObject</span></span>
<span data-ttu-id="c2fe8-137">이 cmdlet이 삭제하는 노드 파일을 나타내는 **PSNodeFile** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c2fe8-137">Specifies **PSNodeFile** object that represent the node file that this cmdlet deletes.</span></span>
<span data-ttu-id="c2fe8-138">**PSNodeFile을 얻은** 경우 Get-AzBatchNodeFile cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2fe8-138">To obtain a **PSNodeFile**, use the Get-AzBatchNodeFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSNodeFile
Parameter Sets: InputObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2fe8-139">-JobId</span><span class="sxs-lookup"><span data-stu-id="c2fe8-139">-JobId</span></span>
<span data-ttu-id="c2fe8-140">작업을 포함하는 작업의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c2fe8-140">Specifies the ID of the job that contains the task.</span></span>

```yaml
Type: System.String
Parameter Sets: Task
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2fe8-141">-Path</span><span class="sxs-lookup"><span data-stu-id="c2fe8-141">-Path</span></span>
<span data-ttu-id="c2fe8-142">삭제할 노드 파일의 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="c2fe8-142">The file path of the node file to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: Task, ComputeNode
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2fe8-143">-PoolId</span><span class="sxs-lookup"><span data-stu-id="c2fe8-143">-PoolId</span></span>
<span data-ttu-id="c2fe8-144">이 cmdlet에서 파일을 제거하는 계산 노드가 포함된 풀의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c2fe8-144">Specifies the ID of the pool that contains the compute nodes for which this cmdlet removes a file.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2fe8-145">-Recursive</span><span class="sxs-lookup"><span data-stu-id="c2fe8-145">-Recursive</span></span>
<span data-ttu-id="c2fe8-146">이 cmdlet은 지정된 경로 아래에 있는 폴더 및 모든 하위 폴더 및 파일을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="c2fe8-146">Indicates that this cmdlet deletes the folder and all subfolders and files under the specified path.</span></span>
<span data-ttu-id="c2fe8-147">이 cmdlet은 경로가 폴더인 경우와 관련이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2fe8-147">This cmdlet is relevant only if the path is a folder.</span></span>

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

### <span data-ttu-id="c2fe8-148">-TaskId</span><span class="sxs-lookup"><span data-stu-id="c2fe8-148">-TaskId</span></span>
<span data-ttu-id="c2fe8-149">작업의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c2fe8-149">Specifies the ID of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: Task
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2fe8-150">-확인</span><span class="sxs-lookup"><span data-stu-id="c2fe8-150">-Confirm</span></span>
<span data-ttu-id="c2fe8-151">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2fe8-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2fe8-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2fe8-152">-WhatIf</span></span>
<span data-ttu-id="c2fe8-153">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="c2fe8-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2fe8-154">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c2fe8-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2fe8-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2fe8-155">CommonParameters</span></span>
<span data-ttu-id="c2fe8-156">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c2fe8-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2fe8-157">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c2fe8-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2fe8-158">입력</span><span class="sxs-lookup"><span data-stu-id="c2fe8-158">INPUTS</span></span>

### <span data-ttu-id="c2fe8-159">System.String</span><span class="sxs-lookup"><span data-stu-id="c2fe8-159">System.String</span></span>

### <span data-ttu-id="c2fe8-160">Microsoft.Azure.Commands.Bat. Models.PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="c2fe8-160">Microsoft.Azure.Commands.Batch.Models.PSNodeFile</span></span>

### <span data-ttu-id="c2fe8-161">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c2fe8-161">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="c2fe8-162">출력</span><span class="sxs-lookup"><span data-stu-id="c2fe8-162">OUTPUTS</span></span>

### <span data-ttu-id="c2fe8-163">System.Void</span><span class="sxs-lookup"><span data-stu-id="c2fe8-163">System.Void</span></span>

## <span data-ttu-id="c2fe8-164">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c2fe8-164">NOTES</span></span>

## <span data-ttu-id="c2fe8-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c2fe8-165">RELATED LINKS</span></span>

[<span data-ttu-id="c2fe8-166">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="c2fe8-166">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="c2fe8-167">Get-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="c2fe8-167">Get-AzBatchNodeFile</span></span>](./Get-AzBatchNodeFile.md)

[<span data-ttu-id="c2fe8-168">Get-AzBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="c2fe8-168">Get-AzBatchNodeFileContent</span></span>](./Get-AzBatchNodeFileContent.md)


