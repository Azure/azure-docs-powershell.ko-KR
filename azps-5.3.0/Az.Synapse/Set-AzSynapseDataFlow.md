---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsedataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataFlow.md
ms.openlocfilehash: 4147343b01e53050f88429424ca7a9c70aa445c6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493265"
---
# <span data-ttu-id="cc8be-101">Set-AzSynapseDataFlow</span><span class="sxs-lookup"><span data-stu-id="cc8be-101">Set-AzSynapseDataFlow</span></span>

## <span data-ttu-id="cc8be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc8be-102">SYNOPSIS</span></span>
<span data-ttu-id="cc8be-103">작업 영역의 데이터 흐름을 생성하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="cc8be-103">Creates or updates a data flow in workspace.</span></span>

## <span data-ttu-id="cc8be-104">구문</span><span class="sxs-lookup"><span data-stu-id="cc8be-104">SYNTAX</span></span>

### <span data-ttu-id="cc8be-105">SetByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="cc8be-105">SetByName (Default)</span></span>
```
Set-AzSynapseDataFlow -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc8be-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="cc8be-106">SetByObject</span></span>
```
Set-AzSynapseDataFlow -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc8be-107">설명</span><span class="sxs-lookup"><span data-stu-id="cc8be-107">DESCRIPTION</span></span>
<span data-ttu-id="cc8be-108">**Set-AzSynapseDataFlow** cmdlet은 데이터 흐름을 생성하거나 작업 영역의 기존 데이터 흐름을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="cc8be-108">The **Set-AzSynapseDataFlow** cmdlet creates a data flow or updates an existing data flow in workspace.</span></span>

## <span data-ttu-id="cc8be-109">예제</span><span class="sxs-lookup"><span data-stu-id="cc8be-109">EXAMPLES</span></span>

### <span data-ttu-id="cc8be-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="cc8be-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseDataFlow -WorkspaceName ContosoWorkspace -Name ContosoDataFlow -DefinitionFile "C:\\samples\\DataFlow.json"
```

<span data-ttu-id="cc8be-111">이 명령은 ContosoWorkspace라는 작업 영역의 ContosoDataFlow라는 데이터 흐름을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cc8be-111">This command creates a data flow named ContosoDataFlow in the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="cc8be-112">이 명령은 데이터 흐름을 DataFlow.js기반입니다.</span><span class="sxs-lookup"><span data-stu-id="cc8be-112">The command bases the data flow on information in the DataFlow.json file.</span></span>

## <span data-ttu-id="cc8be-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cc8be-113">PARAMETERS</span></span>

### <span data-ttu-id="cc8be-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cc8be-114">-AsJob</span></span>
<span data-ttu-id="cc8be-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="cc8be-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cc8be-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc8be-116">-DefaultProfile</span></span>
<span data-ttu-id="cc8be-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cc8be-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc8be-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="cc8be-118">-DefinitionFile</span></span>
<span data-ttu-id="cc8be-119">JSON 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="cc8be-119">The JSON file path.</span></span>

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

### <span data-ttu-id="cc8be-120">-Name</span><span class="sxs-lookup"><span data-stu-id="cc8be-120">-Name</span></span>
<span data-ttu-id="cc8be-121">데이터 흐름 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cc8be-121">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DataFlowName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc8be-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="cc8be-122">-WorkspaceName</span></span>
<span data-ttu-id="cc8be-123">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cc8be-123">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc8be-124">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="cc8be-124">-WorkspaceObject</span></span>
<span data-ttu-id="cc8be-125">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="cc8be-125">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cc8be-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cc8be-126">-Confirm</span></span>
<span data-ttu-id="cc8be-127">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="cc8be-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc8be-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc8be-128">-WhatIf</span></span>
<span data-ttu-id="cc8be-129">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="cc8be-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc8be-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cc8be-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc8be-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc8be-131">CommonParameters</span></span>
<span data-ttu-id="cc8be-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cc8be-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc8be-133">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="cc8be-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc8be-134">입력</span><span class="sxs-lookup"><span data-stu-id="cc8be-134">INPUTS</span></span>

### <span data-ttu-id="cc8be-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="cc8be-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="cc8be-136">출력</span><span class="sxs-lookup"><span data-stu-id="cc8be-136">OUTPUTS</span></span>

### <span data-ttu-id="cc8be-137">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span><span class="sxs-lookup"><span data-stu-id="cc8be-137">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span></span>

## <span data-ttu-id="cc8be-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cc8be-138">NOTES</span></span>

## <span data-ttu-id="cc8be-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cc8be-139">RELATED LINKS</span></span>
