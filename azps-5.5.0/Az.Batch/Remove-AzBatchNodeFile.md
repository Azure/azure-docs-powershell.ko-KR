---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: DBA02017-8372-4A91-A4F1-985777DEDAB9
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchnodefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchNodeFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchNodeFile.md
ms.openlocfilehash: 7e9aeebebfc5720ab006d43071eadeabe6bcf655
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182065"
---
# <span data-ttu-id="bde51-101">Remove-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="bde51-101">Remove-AzBatchNodeFile</span></span>

## <span data-ttu-id="bde51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bde51-102">SYNOPSIS</span></span>
<span data-ttu-id="bde51-103">태스크 또는 계산 노드에 대한 노드 파일을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="bde51-103">Deletes a node file for a task or compute node.</span></span>

## <span data-ttu-id="bde51-104">구문</span><span class="sxs-lookup"><span data-stu-id="bde51-104">SYNTAX</span></span>

### <span data-ttu-id="bde51-105">작업</span><span class="sxs-lookup"><span data-stu-id="bde51-105">Task</span></span>
```
Remove-AzBatchNodeFile -JobId <String> -TaskId <String> -Path <String> [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bde51-106">ComputeNode</span><span class="sxs-lookup"><span data-stu-id="bde51-106">ComputeNode</span></span>
```
Remove-AzBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> -Path <String> [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bde51-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="bde51-107">InputObject</span></span>
```
Remove-AzBatchNodeFile [[-InputObject] <PSNodeFile>] [-Force] [-Recursive] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bde51-108">설명</span><span class="sxs-lookup"><span data-stu-id="bde51-108">DESCRIPTION</span></span>
<span data-ttu-id="bde51-109">**Remove-AzBatchNodeFile** cmdlet은 태스크 또는 계산 노드에 대한 Azure Batch 노드 파일을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="bde51-109">The **Remove-AzBatchNodeFile** cmdlet deletes an Azure Batch node file for a task or compute node.</span></span>

## <span data-ttu-id="bde51-110">예제</span><span class="sxs-lookup"><span data-stu-id="bde51-110">EXAMPLES</span></span>

### <span data-ttu-id="bde51-111">예제 1: 작업과 연결된 파일 삭제</span><span class="sxs-lookup"><span data-stu-id="bde51-111">Example 1: Delete a file associated with a task</span></span>
```
PS C:\>Remove-AzBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Path "wd\testFile.txt" -BatchContext $Context
```

<span data-ttu-id="bde51-112">이 명령은 이름 지정한 노드 파일을 wd\testFile.txt.</span><span class="sxs-lookup"><span data-stu-id="bde51-112">This command deletes the node file that is named wd\testFile.txt.</span></span>
<span data-ttu-id="bde51-113">해당 파일은 Job-000001 작업 아래에 ID Task26이 있는 태스크와 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="bde51-113">That file is associated with the task that has the ID Task26 under the job Job-000001.</span></span>

### <span data-ttu-id="bde51-114">예제 2: 계산 노드에서 파일 삭제</span><span class="sxs-lookup"><span data-stu-id="bde51-114">Example 2: Delete a file from a compute node</span></span>
```
PS C:\>Remove-AzBatchNodeFile -PoolId "Pool07" -ComputeNodeId "tvm-2316545714_1-20150725t213220z" -Path "startup\testFile.txt" -BatchContext $Context
```

<span data-ttu-id="bde51-115">이 명령은 ID Pool07이 startup\testFile.txt 지정된 계산 노드에서 이름이 지정된 노드 파일을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="bde51-115">This command deletes the node file that is named startup\testFile.txt from the specified compute node in the pool that has the ID Pool07.</span></span>

### <span data-ttu-id="bde51-116">예제 3: 파이프라인을 사용하여 파일 제거</span><span class="sxs-lookup"><span data-stu-id="bde51-116">Example 3: Remove a file by using the pipeline</span></span>
```
PS C:\>Get-AzBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Path "wd\testFile2.txt" -BatchContext $Context | Remove-AzBatchNodeFile -Force -BatchContext $Context
```

<span data-ttu-id="bde51-117">이 명령은 **Get-AzBatchNodeFile을** 사용하여 노드 파일을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="bde51-117">This command gets the node file by using **Get-AzBatchNodeFile**.</span></span>
<span data-ttu-id="bde51-118">해당 파일은 Job-000001 작업 아래에 ID Task26이 있는 태스크와 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="bde51-118">That file is associated with the task that has the ID Task26 under the job Job-000001.</span></span>
<span data-ttu-id="bde51-119">이 명령은 파이프라인을 사용하여 해당 파일을 현재 cmdlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="bde51-119">The command passes that file to the current cmdlet by using the pipeline.</span></span>
<span data-ttu-id="bde51-120">현재 cmdlet은 노드 파일을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="bde51-120">The current cmdlet removes the node file.</span></span>
<span data-ttu-id="bde51-121">이 명령은 Force 매개 *변수를 지정합니다.*</span><span class="sxs-lookup"><span data-stu-id="bde51-121">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="bde51-122">따라서 명령은 확인을 요청하는 메시지를 표시하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bde51-122">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="bde51-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bde51-123">PARAMETERS</span></span>

### <span data-ttu-id="bde51-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="bde51-124">-BatchContext</span></span>
<span data-ttu-id="bde51-125">이 cmdlet이 Batch 서비스와 상호 작용하는 데 사용하는 **BatchAccountContext** 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bde51-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="bde51-126">Get-AzBatchAccount cmdlet을 사용하여 BatchAccountContext를 얻을 경우 Batch 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="bde51-126">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="bde51-127">대신 공유 키 인증을 사용 Get-AzBatchAccountKey 키가 채워진 BatchAccountContext 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="bde51-127">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="bde51-128">공유 키 인증을 사용하는 경우 기본 액세스 키가 기본적으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="bde51-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="bde51-129">사용할 키를 변경하기 위해 BatchAccountContext.KeyInUse 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="bde51-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="bde51-130">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="bde51-130">-ComputeNodeId</span></span>
<span data-ttu-id="bde51-131">이 cmdlet에서 삭제하는 Batch 노드 파일을 포함하는 계산 노드의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bde51-131">Specifies the ID of the compute node that contains the Batch node file that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="bde51-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bde51-132">-DefaultProfile</span></span>
<span data-ttu-id="bde51-133">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bde51-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bde51-134">-Force</span><span class="sxs-lookup"><span data-stu-id="bde51-134">-Force</span></span>
<span data-ttu-id="bde51-135">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="bde51-135">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bde51-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bde51-136">-InputObject</span></span>
<span data-ttu-id="bde51-137">이 cmdlet이 삭제하는 노드 파일을 나타내는 **PSNodeFile** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bde51-137">Specifies **PSNodeFile** object that represent the node file that this cmdlet deletes.</span></span>
<span data-ttu-id="bde51-138">**PSNodeFile을 얻습니다.** Get-AzBatchNodeFile cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="bde51-138">To obtain a **PSNodeFile**, use the Get-AzBatchNodeFile cmdlet.</span></span>

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

### <span data-ttu-id="bde51-139">-JobId</span><span class="sxs-lookup"><span data-stu-id="bde51-139">-JobId</span></span>
<span data-ttu-id="bde51-140">태스크를 포함하는 작업의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bde51-140">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="bde51-141">-Path</span><span class="sxs-lookup"><span data-stu-id="bde51-141">-Path</span></span>
<span data-ttu-id="bde51-142">삭제할 노드 파일의 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="bde51-142">The file path of the node file to delete.</span></span>

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

### <span data-ttu-id="bde51-143">-PoolId</span><span class="sxs-lookup"><span data-stu-id="bde51-143">-PoolId</span></span>
<span data-ttu-id="bde51-144">이 cmdlet이 파일을 제거하는 계산 노드를 포함하는 풀의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bde51-144">Specifies the ID of the pool that contains the compute nodes for which this cmdlet removes a file.</span></span>

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

### <span data-ttu-id="bde51-145">-Recursive</span><span class="sxs-lookup"><span data-stu-id="bde51-145">-Recursive</span></span>
<span data-ttu-id="bde51-146">이 cmdlet이 지정된 경로에서 폴더 및 모든 하위 폴더 및 파일을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="bde51-146">Indicates that this cmdlet deletes the folder and all subfolders and files under the specified path.</span></span>
<span data-ttu-id="bde51-147">이 cmdlet은 경로가 폴더인 경우 관련이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bde51-147">This cmdlet is relevant only if the path is a folder.</span></span>

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

### <span data-ttu-id="bde51-148">-TaskId</span><span class="sxs-lookup"><span data-stu-id="bde51-148">-TaskId</span></span>
<span data-ttu-id="bde51-149">작업의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bde51-149">Specifies the ID of the task.</span></span>

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

### <span data-ttu-id="bde51-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bde51-150">-Confirm</span></span>
<span data-ttu-id="bde51-151">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="bde51-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bde51-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bde51-152">-WhatIf</span></span>
<span data-ttu-id="bde51-153">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="bde51-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bde51-154">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bde51-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bde51-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bde51-155">CommonParameters</span></span>
<span data-ttu-id="bde51-156">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bde51-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bde51-157">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bde51-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bde51-158">입력</span><span class="sxs-lookup"><span data-stu-id="bde51-158">INPUTS</span></span>

### <span data-ttu-id="bde51-159">System.String</span><span class="sxs-lookup"><span data-stu-id="bde51-159">System.String</span></span>

### <span data-ttu-id="bde51-160">Microsoft.Azure.Commands.Batch. Models.PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="bde51-160">Microsoft.Azure.Commands.Batch.Models.PSNodeFile</span></span>

### <span data-ttu-id="bde51-161">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="bde51-161">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="bde51-162">출력</span><span class="sxs-lookup"><span data-stu-id="bde51-162">OUTPUTS</span></span>

### <span data-ttu-id="bde51-163">System.Void</span><span class="sxs-lookup"><span data-stu-id="bde51-163">System.Void</span></span>

## <span data-ttu-id="bde51-164">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bde51-164">NOTES</span></span>

## <span data-ttu-id="bde51-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bde51-165">RELATED LINKS</span></span>

[<span data-ttu-id="bde51-166">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="bde51-166">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="bde51-167">Get-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="bde51-167">Get-AzBatchNodeFile</span></span>](./Get-AzBatchNodeFile.md)

[<span data-ttu-id="bde51-168">Get-AzBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="bde51-168">Get-AzBatchNodeFileContent</span></span>](./Get-AzBatchNodeFileContent.md)


