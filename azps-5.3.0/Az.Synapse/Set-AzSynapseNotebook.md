---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseNotebook.md
ms.openlocfilehash: da4907200bef198afa1d57b51069c6379d28c8f1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493260"
---
# <span data-ttu-id="74269-101">Set-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="74269-101">Set-AzSynapseNotebook</span></span>

## <span data-ttu-id="74269-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74269-102">SYNOPSIS</span></span>
<span data-ttu-id="74269-103">작업 영역의 전자 필기장을 생성하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="74269-103">Creates or updates a notebook in a workspace.</span></span>

## <span data-ttu-id="74269-104">구문</span><span class="sxs-lookup"><span data-stu-id="74269-104">SYNTAX</span></span>

### <span data-ttu-id="74269-105">SetByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="74269-105">SetByName (Default)</span></span>
```
Set-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74269-106">SetByNameAndSparkPool</span><span class="sxs-lookup"><span data-stu-id="74269-106">SetByNameAndSparkPool</span></span>
```
Set-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] -SparkPoolName <String> [-ExecutorSize <String>]
 -ExecutorCount <Int32> -DefinitionFile <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74269-107">SetByObject</span><span class="sxs-lookup"><span data-stu-id="74269-107">SetByObject</span></span>
```
Set-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>] -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74269-108">SetByObjectAndSparkPool</span><span class="sxs-lookup"><span data-stu-id="74269-108">SetByObjectAndSparkPool</span></span>
```
Set-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>] -SparkPoolName <String>
 [-ExecutorSize <String>] -ExecutorCount <Int32> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74269-109">설명</span><span class="sxs-lookup"><span data-stu-id="74269-109">DESCRIPTION</span></span>
<span data-ttu-id="74269-110">**Set-AzSynapseNotebook** cmdlet은 작업 영역의 Notebook을 생성하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="74269-110">The **Set-AzSynapseNotebook** cmdlet creates or updates a notebook in a workspace.</span></span>

## <span data-ttu-id="74269-111">예제</span><span class="sxs-lookup"><span data-stu-id="74269-111">EXAMPLES</span></span>

### <span data-ttu-id="74269-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="74269-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseNotebook -WorkspaceName ContosoWorkspace -DefinitionFile "C:\\samples\\notebook.ipynb"

    WorkspaceName : ContosoWorkspace
    Properties    : Microsoft.Azure.Commands.Synapse.Models.PSNotebook
    Name          : notebook
```

<span data-ttu-id="74269-113">이 명령은 ContosoWorkspace라는 작업 영역의 Notebook 파일 notebook.ipynb에서 Notebook을 생성하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="74269-113">This command creates or updates a notebook from notebook file notebook.ipynb in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="74269-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="74269-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapseNotebook -DefinitionFile "C:\\samples\\notebook.ipynb"
```

<span data-ttu-id="74269-115">이 명령은 파이프라인을 통해 ContosoWorkspace라는 작업 영역의 Notebook 파일 notebook.ipynb에서 Notebook을 생성하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="74269-115">This command creates or updates a notebook from notebook file notebook.ipynb in the workspace named ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="74269-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="74269-116">Example 3</span></span>
```powershell
PS C:\> Set-AzSynapseNotebook -WorkspaceName ContosoWorkspace -DefinitionFile "C:\\samples\\notebook.ipynb" -SparkPoolName ContosoSparkPool -ExecutorCount 2
```

<span data-ttu-id="74269-117">이 명령은 Notebook 파일 notebook.ipynb에서 Notebook을 생성하거나 업데이트합니다. Notebook은 ContosoSparkPool에 연결되고 ContosoWorkspace라는 작업 영역의 실행기 2개가 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="74269-117">This command creates or updates a notebook from notebook file notebook.ipynb which attaches to ContosoSparkPool and uses 2 executors in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="74269-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="74269-118">PARAMETERS</span></span>

### <span data-ttu-id="74269-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="74269-119">-AsJob</span></span>
<span data-ttu-id="74269-120">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="74269-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="74269-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74269-121">-DefaultProfile</span></span>
<span data-ttu-id="74269-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="74269-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74269-123">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="74269-123">-DefinitionFile</span></span>
<span data-ttu-id="74269-124">JSON 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="74269-124">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74269-125">-ExecutorCount</span><span class="sxs-lookup"><span data-stu-id="74269-125">-ExecutorCount</span></span>
<span data-ttu-id="74269-126">작업의 지정된 Spark 풀에 할당할 실행기 수입니다.</span><span class="sxs-lookup"><span data-stu-id="74269-126">Number of executors to be allocated in the specified Spark pool for the job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SetByNameAndSparkPool, SetByObjectAndSparkPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74269-127">-ExecutorSize</span><span class="sxs-lookup"><span data-stu-id="74269-127">-ExecutorSize</span></span>
<span data-ttu-id="74269-128">작업의 지정된 Spark 풀에 할당된 실행기에 사용할 코어 및 메모리의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="74269-128">Number of core and memory to be used for executors allocated in the specified Spark pool for the job.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndSparkPool, SetByObjectAndSparkPool
Aliases:
Accepted values: Small, Medium, Large

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74269-129">-Name</span><span class="sxs-lookup"><span data-stu-id="74269-129">-Name</span></span>
<span data-ttu-id="74269-130">전자 필기장 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="74269-130">The notebook name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NotebookName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74269-131">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="74269-131">-SparkPoolName</span></span>
<span data-ttu-id="74269-132">Synapse Spark 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="74269-132">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndSparkPool, SetByObjectAndSparkPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74269-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="74269-133">-WorkspaceName</span></span>
<span data-ttu-id="74269-134">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="74269-134">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByNameAndSparkPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74269-135">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="74269-135">-WorkspaceObject</span></span>
<span data-ttu-id="74269-136">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="74269-136">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByObject, SetByObjectAndSparkPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="74269-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="74269-137">-Confirm</span></span>
<span data-ttu-id="74269-138">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="74269-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74269-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74269-139">-WhatIf</span></span>
<span data-ttu-id="74269-140">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="74269-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74269-141">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="74269-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74269-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74269-142">CommonParameters</span></span>
<span data-ttu-id="74269-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="74269-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74269-144">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="74269-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74269-145">입력</span><span class="sxs-lookup"><span data-stu-id="74269-145">INPUTS</span></span>

### <span data-ttu-id="74269-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="74269-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="74269-147">출력</span><span class="sxs-lookup"><span data-stu-id="74269-147">OUTPUTS</span></span>

### <span data-ttu-id="74269-148">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="74269-148">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="74269-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="74269-149">NOTES</span></span>

## <span data-ttu-id="74269-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="74269-150">RELATED LINKS</span></span>
