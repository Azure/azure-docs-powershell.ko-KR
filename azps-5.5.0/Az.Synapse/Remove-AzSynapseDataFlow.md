---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsedataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataFlow.md
ms.openlocfilehash: 2d0bec0c86f51771e971ca2c6b5a22c32f8ee687
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197329"
---
# <span data-ttu-id="146ce-101">Remove-AzSynapseDataFlow</span><span class="sxs-lookup"><span data-stu-id="146ce-101">Remove-AzSynapseDataFlow</span></span>

## <span data-ttu-id="146ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="146ce-102">SYNOPSIS</span></span>
<span data-ttu-id="146ce-103">작업 영역의 데이터 흐름을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="146ce-103">Removes a data flow from workspace.</span></span>

## <span data-ttu-id="146ce-104">구문</span><span class="sxs-lookup"><span data-stu-id="146ce-104">SYNTAX</span></span>

### <span data-ttu-id="146ce-105">RemoveByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="146ce-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseDataFlow -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="146ce-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="146ce-106">RemoveByObject</span></span>
```
Remove-AzSynapseDataFlow -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="146ce-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="146ce-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseDataFlow -InputObject <PSDataFlowResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="146ce-108">설명</span><span class="sxs-lookup"><span data-stu-id="146ce-108">DESCRIPTION</span></span>
<span data-ttu-id="146ce-109">**Remove-AzSynapseDataFlow** cmdlet은 작업 영역의 데이터 흐름을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="146ce-109">The **Remove-AzSynapseDataFlow** cmdlet removes a data flow from workspace.</span></span>

## <span data-ttu-id="146ce-110">예제</span><span class="sxs-lookup"><span data-stu-id="146ce-110">EXAMPLES</span></span>

### <span data-ttu-id="146ce-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="146ce-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseDataFlow -WorkspaceName ContosoWorkspace -Name ContosoDataFlow
```

<span data-ttu-id="146ce-112">이 명령은 ContosoWorkspace라는 작업 영역에서 ContosoDataFlow라는 데이터 흐름을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="146ce-112">This command removes the data flow named ContosoDataFlow from the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="146ce-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="146ce-113">PARAMETERS</span></span>

### <span data-ttu-id="146ce-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="146ce-114">-AsJob</span></span>
<span data-ttu-id="146ce-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="146ce-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="146ce-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="146ce-116">-DefaultProfile</span></span>
<span data-ttu-id="146ce-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="146ce-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="146ce-118">-Force</span><span class="sxs-lookup"><span data-stu-id="146ce-118">-Force</span></span>
<span data-ttu-id="146ce-119">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="146ce-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="146ce-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="146ce-120">-InputObject</span></span>
<span data-ttu-id="146ce-121">데이터 흐름 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="146ce-121">The data flow object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="146ce-122">-Name</span><span class="sxs-lookup"><span data-stu-id="146ce-122">-Name</span></span>
<span data-ttu-id="146ce-123">데이터 흐름 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="146ce-123">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases: DataFlowName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="146ce-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="146ce-124">-PassThru</span></span>
<span data-ttu-id="146ce-125">이 Cmdlet은 기본적으로 개체를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="146ce-125">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="146ce-126">이 스위치를 지정하면 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="146ce-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="146ce-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="146ce-127">-WorkspaceName</span></span>
<span data-ttu-id="146ce-128">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="146ce-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="146ce-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="146ce-129">-WorkspaceObject</span></span>
<span data-ttu-id="146ce-130">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="146ce-130">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="146ce-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="146ce-131">-Confirm</span></span>
<span data-ttu-id="146ce-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="146ce-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="146ce-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="146ce-133">-WhatIf</span></span>
<span data-ttu-id="146ce-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="146ce-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="146ce-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="146ce-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="146ce-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="146ce-136">CommonParameters</span></span>
<span data-ttu-id="146ce-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="146ce-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="146ce-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="146ce-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="146ce-139">입력</span><span class="sxs-lookup"><span data-stu-id="146ce-139">INPUTS</span></span>

### <span data-ttu-id="146ce-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="146ce-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="146ce-141">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span><span class="sxs-lookup"><span data-stu-id="146ce-141">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span></span>

## <span data-ttu-id="146ce-142">출력</span><span class="sxs-lookup"><span data-stu-id="146ce-142">OUTPUTS</span></span>

### <span data-ttu-id="146ce-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="146ce-143">System.Boolean</span></span>

## <span data-ttu-id="146ce-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="146ce-144">NOTES</span></span>

## <span data-ttu-id="146ce-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="146ce-145">RELATED LINKS</span></span>
