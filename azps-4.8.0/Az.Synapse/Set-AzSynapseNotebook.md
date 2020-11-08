---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseNotebook.md
ms.openlocfilehash: da4907200bef198afa1d57b51069c6379d28c8f1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213154"
---
# <span data-ttu-id="8b29e-101">Set-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="8b29e-101">Set-AzSynapseNotebook</span></span>

## <span data-ttu-id="8b29e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b29e-102">SYNOPSIS</span></span>
<span data-ttu-id="8b29e-103">작업 영역에서 전자 필기장을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b29e-103">Creates or updates a notebook in a workspace.</span></span>

## <span data-ttu-id="8b29e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8b29e-104">SYNTAX</span></span>

### <span data-ttu-id="8b29e-105">SetByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="8b29e-105">SetByName (Default)</span></span>
```
Set-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b29e-106">SetByNameAndSparkPool</span><span class="sxs-lookup"><span data-stu-id="8b29e-106">SetByNameAndSparkPool</span></span>
```
Set-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] -SparkPoolName <String> [-ExecutorSize <String>]
 -ExecutorCount <Int32> -DefinitionFile <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b29e-107">SetByObject</span><span class="sxs-lookup"><span data-stu-id="8b29e-107">SetByObject</span></span>
```
Set-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>] -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b29e-108">SetByObjectAndSparkPool</span><span class="sxs-lookup"><span data-stu-id="8b29e-108">SetByObjectAndSparkPool</span></span>
```
Set-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>] -SparkPoolName <String>
 [-ExecutorSize <String>] -ExecutorCount <Int32> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b29e-109">설명은</span><span class="sxs-lookup"><span data-stu-id="8b29e-109">DESCRIPTION</span></span>
<span data-ttu-id="8b29e-110">**Set-AzSynapseNotebook** cmdlet은 작업 영역에서 전자 필기장을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b29e-110">The **Set-AzSynapseNotebook** cmdlet creates or updates a notebook in a workspace.</span></span>

## <span data-ttu-id="8b29e-111">예제의</span><span class="sxs-lookup"><span data-stu-id="8b29e-111">EXAMPLES</span></span>

### <span data-ttu-id="8b29e-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="8b29e-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseNotebook -WorkspaceName ContosoWorkspace -DefinitionFile "C:\\samples\\notebook.ipynb"

    WorkspaceName : ContosoWorkspace
    Properties    : Microsoft.Azure.Commands.Synapse.Models.PSNotebook
    Name          : notebook
```

<span data-ttu-id="8b29e-113">이 명령은 ContosoWorkspace 이라는 작업 영역의 전자 필기장 파일 전자 필기장에서 전자 필기장을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b29e-113">This command creates or updates a notebook from notebook file notebook.ipynb in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="8b29e-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="8b29e-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapseNotebook -DefinitionFile "C:\\samples\\notebook.ipynb"
```

<span data-ttu-id="8b29e-115">이 명령은 ContosoWorkspace에서 파이프라인 이라는 이름의 작업 영역에 있는 전자 필기장 파일 전자 필기장에서 전자 필기장을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b29e-115">This command creates or updates a notebook from notebook file notebook.ipynb in the workspace named ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="8b29e-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="8b29e-116">Example 3</span></span>
```powershell
PS C:\> Set-AzSynapseNotebook -WorkspaceName ContosoWorkspace -DefinitionFile "C:\\samples\\notebook.ipynb" -SparkPoolName ContosoSparkPool -ExecutorCount 2
```

<span data-ttu-id="8b29e-117">이 명령은 ContosoSparkPool에 연결 되 고 ContosoWorkspace 이라는 작업 영역에서 2 실행자를 사용 하는 전자 필기장 파일 전자 필기장에서 전자 필기장을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b29e-117">This command creates or updates a notebook from notebook file notebook.ipynb which attaches to ContosoSparkPool and uses 2 executors in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="8b29e-118">변수</span><span class="sxs-lookup"><span data-stu-id="8b29e-118">PARAMETERS</span></span>

### <span data-ttu-id="8b29e-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8b29e-119">-AsJob</span></span>
<span data-ttu-id="8b29e-120">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="8b29e-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8b29e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b29e-121">-DefaultProfile</span></span>
<span data-ttu-id="8b29e-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8b29e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b29e-123">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="8b29e-123">-DefinitionFile</span></span>
<span data-ttu-id="8b29e-124">JSON 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="8b29e-124">The JSON file path.</span></span>

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

### <span data-ttu-id="8b29e-125">-ExecutorCount</span><span class="sxs-lookup"><span data-stu-id="8b29e-125">-ExecutorCount</span></span>
<span data-ttu-id="8b29e-126">작업에 대해 지정 된 Spark 풀에 할당할 실행자 수입니다.</span><span class="sxs-lookup"><span data-stu-id="8b29e-126">Number of executors to be allocated in the specified Spark pool for the job.</span></span>

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

### <span data-ttu-id="8b29e-127">-ExecutorSize</span><span class="sxs-lookup"><span data-stu-id="8b29e-127">-ExecutorSize</span></span>
<span data-ttu-id="8b29e-128">작업에 대해 지정 된 Spark 풀에 할당 된 실행자에 사용 되는 코어 및 메모리의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="8b29e-128">Number of core and memory to be used for executors allocated in the specified Spark pool for the job.</span></span>

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

### <span data-ttu-id="8b29e-129">-이름</span><span class="sxs-lookup"><span data-stu-id="8b29e-129">-Name</span></span>
<span data-ttu-id="8b29e-130">전자 필기장 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8b29e-130">The notebook name.</span></span>

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

### <span data-ttu-id="8b29e-131">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="8b29e-131">-SparkPoolName</span></span>
<span data-ttu-id="8b29e-132">Synapse Spark 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8b29e-132">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="8b29e-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8b29e-133">-WorkspaceName</span></span>
<span data-ttu-id="8b29e-134">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8b29e-134">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="8b29e-135">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="8b29e-135">-WorkspaceObject</span></span>
<span data-ttu-id="8b29e-136">일반적으로 파이프라인을 통해 전달 되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="8b29e-136">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="8b29e-137">-확인</span><span class="sxs-lookup"><span data-stu-id="8b29e-137">-Confirm</span></span>
<span data-ttu-id="8b29e-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b29e-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b29e-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b29e-139">-WhatIf</span></span>
<span data-ttu-id="8b29e-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8b29e-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b29e-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8b29e-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b29e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b29e-142">CommonParameters</span></span>
<span data-ttu-id="8b29e-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b29e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b29e-144">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8b29e-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b29e-145">입력</span><span class="sxs-lookup"><span data-stu-id="8b29e-145">INPUTS</span></span>

### <span data-ttu-id="8b29e-146">Synapse. PSSynapseWorkspace/.</span><span class="sxs-lookup"><span data-stu-id="8b29e-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="8b29e-147">출력</span><span class="sxs-lookup"><span data-stu-id="8b29e-147">OUTPUTS</span></span>

### <span data-ttu-id="8b29e-148">Synapse. PSNotebookResource/.</span><span class="sxs-lookup"><span data-stu-id="8b29e-148">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="8b29e-149">상속자</span><span class="sxs-lookup"><span data-stu-id="8b29e-149">NOTES</span></span>

## <span data-ttu-id="8b29e-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8b29e-150">RELATED LINKS</span></span>
