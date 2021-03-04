---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/set-azsynapsedataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataFlow.md
ms.openlocfilehash: 4254a301e599dac542a099b9c4f2ebace8929ab4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952976"
---
# <span data-ttu-id="2df40-101">Set-AzSynapseDataFlow</span><span class="sxs-lookup"><span data-stu-id="2df40-101">Set-AzSynapseDataFlow</span></span>

## <span data-ttu-id="2df40-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2df40-102">SYNOPSIS</span></span>
<span data-ttu-id="2df40-103">작업 영역의 데이터 흐름을 생성하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="2df40-103">Creates or updates a data flow in workspace.</span></span>

## <span data-ttu-id="2df40-104">구문</span><span class="sxs-lookup"><span data-stu-id="2df40-104">SYNTAX</span></span>

### <span data-ttu-id="2df40-105">SetByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="2df40-105">SetByName (Default)</span></span>
```
Set-AzSynapseDataFlow -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2df40-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="2df40-106">SetByObject</span></span>
```
Set-AzSynapseDataFlow -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2df40-107">설명</span><span class="sxs-lookup"><span data-stu-id="2df40-107">DESCRIPTION</span></span>
<span data-ttu-id="2df40-108">**Set-AzSynapseDataFlow** cmdlet은 데이터 흐름을 생성하거나 작업 영역의 기존 데이터 흐름을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="2df40-108">The **Set-AzSynapseDataFlow** cmdlet creates a data flow or updates an existing data flow in workspace.</span></span>

## <span data-ttu-id="2df40-109">예제</span><span class="sxs-lookup"><span data-stu-id="2df40-109">EXAMPLES</span></span>

### <span data-ttu-id="2df40-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="2df40-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseDataFlow -WorkspaceName ContosoWorkspace -Name ContosoDataFlow -DefinitionFile "C:\\samples\\DataFlow.json"
```

<span data-ttu-id="2df40-111">이 명령은 ContosoWorkspace라는 작업 영역에서 ContosoDataFlow라는 데이터 흐름을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2df40-111">This command creates a data flow named ContosoDataFlow in the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="2df40-112">명령은 파일에서 데이터 흐름을 DataFlow.js기반입니다.</span><span class="sxs-lookup"><span data-stu-id="2df40-112">The command bases the data flow on information in the DataFlow.json file.</span></span>

## <span data-ttu-id="2df40-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="2df40-113">PARAMETERS</span></span>

### <span data-ttu-id="2df40-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2df40-114">-AsJob</span></span>
<span data-ttu-id="2df40-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="2df40-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2df40-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2df40-116">-DefaultProfile</span></span>
<span data-ttu-id="2df40-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2df40-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2df40-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="2df40-118">-DefinitionFile</span></span>
<span data-ttu-id="2df40-119">JSON 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="2df40-119">The JSON file path.</span></span>

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

### <span data-ttu-id="2df40-120">-Name</span><span class="sxs-lookup"><span data-stu-id="2df40-120">-Name</span></span>
<span data-ttu-id="2df40-121">데이터 흐름 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2df40-121">The data flow name.</span></span>

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

### <span data-ttu-id="2df40-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2df40-122">-WorkspaceName</span></span>
<span data-ttu-id="2df40-123">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2df40-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="2df40-124">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="2df40-124">-WorkspaceObject</span></span>
<span data-ttu-id="2df40-125">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="2df40-125">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="2df40-126">-확인</span><span class="sxs-lookup"><span data-stu-id="2df40-126">-Confirm</span></span>
<span data-ttu-id="2df40-127">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2df40-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2df40-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2df40-128">-WhatIf</span></span>
<span data-ttu-id="2df40-129">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="2df40-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2df40-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2df40-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2df40-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2df40-131">CommonParameters</span></span>
<span data-ttu-id="2df40-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2df40-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2df40-133">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2df40-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2df40-134">입력</span><span class="sxs-lookup"><span data-stu-id="2df40-134">INPUTS</span></span>

### <span data-ttu-id="2df40-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="2df40-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="2df40-136">출력</span><span class="sxs-lookup"><span data-stu-id="2df40-136">OUTPUTS</span></span>

### <span data-ttu-id="2df40-137">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span><span class="sxs-lookup"><span data-stu-id="2df40-137">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span></span>

## <span data-ttu-id="2df40-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2df40-138">NOTES</span></span>

## <span data-ttu-id="2df40-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2df40-139">RELATED LINKS</span></span>
