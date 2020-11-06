---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: DBA02017-8372-4A91-A4F1-985777DEDAB9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchNodeFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchNodeFile.md
ms.openlocfilehash: 5b8797cf2f6068098d1ca407f0f97283dd171af5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531185"
---
# <span data-ttu-id="aff47-101">Remove-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="aff47-101">Remove-AzureBatchNodeFile</span></span>

## <span data-ttu-id="aff47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aff47-102">SYNOPSIS</span></span>
<span data-ttu-id="aff47-103">작업 또는 계산 노드에 대 한 노드 파일을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="aff47-103">Deletes a node file for a task or compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aff47-104">구문과</span><span class="sxs-lookup"><span data-stu-id="aff47-104">SYNTAX</span></span>

### <span data-ttu-id="aff47-105">작업</span><span class="sxs-lookup"><span data-stu-id="aff47-105">Task</span></span>
```
Remove-AzureBatchNodeFile -JobId <String> -TaskId <String> -Name <String> [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="aff47-106">ComputeNode</span><span class="sxs-lookup"><span data-stu-id="aff47-106">ComputeNode</span></span>
```
Remove-AzureBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> -Name <String> [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="aff47-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="aff47-107">InputObject</span></span>
```
Remove-AzureBatchNodeFile [[-InputObject] <PSNodeFile>] [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="aff47-108">설명은</span><span class="sxs-lookup"><span data-stu-id="aff47-108">DESCRIPTION</span></span>
<span data-ttu-id="aff47-109">**Remove-AzureBatchNodeFile** cmdlet은 작업 또는 계산 노드에 대 한 Azure Batch 노드 파일을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="aff47-109">The **Remove-AzureBatchNodeFile** cmdlet deletes an Azure Batch node file for a task or compute node.</span></span>

## <span data-ttu-id="aff47-110">예제의</span><span class="sxs-lookup"><span data-stu-id="aff47-110">EXAMPLES</span></span>

### <span data-ttu-id="aff47-111">예제 1: 작업을 사용 하 여 assocated 파일 삭제</span><span class="sxs-lookup"><span data-stu-id="aff47-111">Example 1: Delete a file assocated with a task</span></span>
```
PS C:\>Remove-AzureBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Name "wd\testFile.txt" -BatchContext $Context
```

<span data-ttu-id="aff47-112">이 명령은 wd\testFile.txt 라는 노드 파일을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="aff47-112">This command deletes the node file that is named wd\testFile.txt.</span></span>
<span data-ttu-id="aff47-113">이 파일은 작업 작업-000001에서 ID Task26를 가진 작업과 연결 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aff47-113">That file is associated with the task that has the ID Task26 under the job Job-000001.</span></span>

### <span data-ttu-id="aff47-114">예제 2: 계산 노드에서 파일 삭제</span><span class="sxs-lookup"><span data-stu-id="aff47-114">Example 2: Delete a file from a compute node</span></span>
```
PS C:\>Remove-AzureBatchNodeFile -PoolId "Pool07" -ComputeNodeId "tvm-2316545714_1-20150725t213220z" -Name "startup\testFile.txt" -BatchContext $Context
```

<span data-ttu-id="aff47-115">이 명령은 ID Pool07를 가진 풀의 지정 된 계산 노드에서 startup\testFile.txt 이라는 이름의 노드 파일을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="aff47-115">This command deletes the node file that is named startup\testFile.txt from the specified compute node in the pool that has the ID Pool07.</span></span>

### <span data-ttu-id="aff47-116">예제 3: 파이프라인을 사용 하 여 파일 제거</span><span class="sxs-lookup"><span data-stu-id="aff47-116">Example 3: Remove a file by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Name "wd\testFile2.txt" -BatchContext $Context | Remove-AzureBatchNodeFile -Force -BatchContext $Context
```

<span data-ttu-id="aff47-117">이 명령은 **가져오기-AzureBatchNodeFile** 을 사용 하 여 노드 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="aff47-117">This command gets the node file by using **Get-AzureBatchNodeFile**.</span></span>
<span data-ttu-id="aff47-118">이 파일은 작업 작업-000001에서 ID Task26를 가진 작업과 연결 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aff47-118">That file is associated with the task that has the ID Task26 under the job Job-000001.</span></span>
<span data-ttu-id="aff47-119">이 명령은 파이프라인을 사용 하 여 해당 파일을 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="aff47-119">The command passes that file to the current cmdlet by using the pipeline.</span></span>
<span data-ttu-id="aff47-120">현재 cmdlet은 노드 파일을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="aff47-120">The current cmdlet removes the node file.</span></span>
<span data-ttu-id="aff47-121">명령에서 *Force* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aff47-121">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="aff47-122">따라서 명령에 확인 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aff47-122">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="aff47-123">변수</span><span class="sxs-lookup"><span data-stu-id="aff47-123">PARAMETERS</span></span>

### <span data-ttu-id="aff47-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="aff47-124">-BatchContext</span></span>
<span data-ttu-id="aff47-125">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aff47-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="aff47-126">구독에 대 한 선택 키를 포함 하는 **Batchaccountcontext** 개체를 가져오려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="aff47-126">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="aff47-127">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="aff47-127">-ComputeNodeId</span></span>
<span data-ttu-id="aff47-128">이 cmdlet이 삭제 하는 일괄 처리 노드 파일을 포함 하는 계산 노드의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aff47-128">Specifies the ID of the compute node that contains the Batch node file that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="aff47-129">-Force</span><span class="sxs-lookup"><span data-stu-id="aff47-129">-Force</span></span>
<span data-ttu-id="aff47-130">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="aff47-130">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="aff47-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aff47-131">-InputObject</span></span>
<span data-ttu-id="aff47-132">이 cmdlet이 삭제 하는 노드 파일을 나타내는 **Psnodefile** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aff47-132">Specifies **PSNodeFile** object that represent the node file that this cmdlet deletes.</span></span>
<span data-ttu-id="aff47-133">**Psnodefile** 을 얻으려면 Get-AzureBatchNodeFile cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="aff47-133">To obtain a **PSNodeFile** , use the Get-AzureBatchNodeFile cmdlet.</span></span>

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

### <span data-ttu-id="aff47-134">-JobId</span><span class="sxs-lookup"><span data-stu-id="aff47-134">-JobId</span></span>
<span data-ttu-id="aff47-135">작업을 포함 하는 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aff47-135">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="aff47-136">-이름</span><span class="sxs-lookup"><span data-stu-id="aff47-136">-Name</span></span>
<span data-ttu-id="aff47-137">이 cmdlet이 삭제 하는 노드 파일의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aff47-137">Specifies the name of the node file that this cmdlet deletes.</span></span>

```yaml
Type: System.String
Parameter Sets: Task, ComputeNode
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aff47-138">-PoolId</span><span class="sxs-lookup"><span data-stu-id="aff47-138">-PoolId</span></span>
<span data-ttu-id="aff47-139">이 cmdlet이 파일을 제거 하는 계산 노드를 포함 하는 풀의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aff47-139">Specifies the ID of the pool that contains the compute nodes for which this cmdlet removes a file.</span></span>

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

### <span data-ttu-id="aff47-140">-Recursive</span><span class="sxs-lookup"><span data-stu-id="aff47-140">-Recursive</span></span>
<span data-ttu-id="aff47-141">이 cmdlet이 지정 된 경로 아래에 있는 폴더 및 모든 하위 폴더 및 파일을 삭제 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="aff47-141">Indicates that this cmdlet deletes the folder and all subfolders and files under the specified path.</span></span>
<span data-ttu-id="aff47-142">이 cmdlet은 경로가 폴더인 경우에만 관련이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aff47-142">This cmdlet is relevant only if the path is a folder.</span></span>

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

### <span data-ttu-id="aff47-143">-TaskId</span><span class="sxs-lookup"><span data-stu-id="aff47-143">-TaskId</span></span>
<span data-ttu-id="aff47-144">작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aff47-144">Specifies the ID of the task.</span></span>

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

### <span data-ttu-id="aff47-145">-확인</span><span class="sxs-lookup"><span data-stu-id="aff47-145">-Confirm</span></span>
<span data-ttu-id="aff47-146">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="aff47-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aff47-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aff47-147">-WhatIf</span></span>
<span data-ttu-id="aff47-148">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="aff47-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aff47-149">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aff47-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aff47-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aff47-150">-DefaultProfile</span></span>
<span data-ttu-id="aff47-151">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aff47-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aff47-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aff47-152">CommonParameters</span></span>
<span data-ttu-id="aff47-153">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="aff47-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aff47-154">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aff47-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aff47-155">입력</span><span class="sxs-lookup"><span data-stu-id="aff47-155">INPUTS</span></span>

### <span data-ttu-id="aff47-156">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="aff47-156">BatchAccountContext</span></span>
<span data-ttu-id="aff47-157">' BatchContext ' 매개 변수는 파이프라인에서 ' BatchAccountContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="aff47-157">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="aff47-158">PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="aff47-158">PSNodeFile</span></span>
<span data-ttu-id="aff47-159">' InputObject ' 매개 변수는 파이프라인에서 ' PSNodeFile ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="aff47-159">Parameter 'InputObject' accepts value of type 'PSNodeFile' from the pipeline</span></span>

## <span data-ttu-id="aff47-160">출력</span><span class="sxs-lookup"><span data-stu-id="aff47-160">OUTPUTS</span></span>

## <span data-ttu-id="aff47-161">상속자</span><span class="sxs-lookup"><span data-stu-id="aff47-161">NOTES</span></span>

## <span data-ttu-id="aff47-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aff47-162">RELATED LINKS</span></span>

[<span data-ttu-id="aff47-163">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="aff47-163">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="aff47-164">Get-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="aff47-164">Get-AzureBatchNodeFile</span></span>](./Get-AzureBatchNodeFile.md)

[<span data-ttu-id="aff47-165">Get-AzureBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="aff47-165">Get-AzureBatchNodeFileContent</span></span>](./Get-AzureBatchNodeFileContent.md)


