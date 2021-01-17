---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapsePipeline.md
ms.openlocfilehash: 747658224703a09f98f232deb865adf4bb084682
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383454"
---
# <span data-ttu-id="1aa7b-101">Remove-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="1aa7b-101">Remove-AzSynapsePipeline</span></span>

## <span data-ttu-id="1aa7b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1aa7b-102">SYNOPSIS</span></span>
<span data-ttu-id="1aa7b-103">작업 영역의 파이프라인을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1aa7b-103">Removes a pipeline from workspace.</span></span>

## <span data-ttu-id="1aa7b-104">구문</span><span class="sxs-lookup"><span data-stu-id="1aa7b-104">SYNTAX</span></span>

### <span data-ttu-id="1aa7b-105">RemoveByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="1aa7b-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapsePipeline -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1aa7b-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="1aa7b-106">RemoveByObject</span></span>
```
Remove-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1aa7b-107">NewByInputObject</span><span class="sxs-lookup"><span data-stu-id="1aa7b-107">NewByInputObject</span></span>
```
Remove-AzSynapsePipeline -Name <String> -InputObject <PSPipelineResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1aa7b-108">설명</span><span class="sxs-lookup"><span data-stu-id="1aa7b-108">DESCRIPTION</span></span>
<span data-ttu-id="1aa7b-109">**Remove-AzSynapsePipeline** cmdlet은 작업 영역의 파이프라인을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1aa7b-109">The **Remove-AzSynapsePipeline** cmdlet removes a pipeline from workspace.</span></span>

## <span data-ttu-id="1aa7b-110">예제</span><span class="sxs-lookup"><span data-stu-id="1aa7b-110">EXAMPLES</span></span>

### <span data-ttu-id="1aa7b-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="1aa7b-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
```

<span data-ttu-id="1aa7b-112">이 cmdlet은 ContosoWorkspace라는 작업 영역에서 ContosoPipeline이라는 파이프라인을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1aa7b-112">This cmdlet removes the pipeline named ContosoPipeline from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="1aa7b-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="1aa7b-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapsePipeline -Name ContosoPipeline
```

<span data-ttu-id="1aa7b-114">이 cmdlet은 파이프라인을 통해 ContosoWorkspace라는 작업 영역에서 ContosoPipeline이라는 파이프라인을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1aa7b-114">This cmdlet removes the pipeline named ContosoPipeline from the workspace named ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="1aa7b-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="1aa7b-115">Example 3</span></span>
```powershell
PS C:\> $pipeline = Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
PS C:\> $pipeline | Remove-AzSynapsePipeline
```

<span data-ttu-id="1aa7b-116">이 cmdlet은 파이프라인을 통해 ContosoWorkspace라는 작업 영역에서 ContosoPipeline이라는 파이프라인을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1aa7b-116">This cmdlet removes the pipeline named ContosoPipeline from the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="1aa7b-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1aa7b-117">PARAMETERS</span></span>

### <span data-ttu-id="1aa7b-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1aa7b-118">-AsJob</span></span>
<span data-ttu-id="1aa7b-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="1aa7b-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1aa7b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1aa7b-120">-DefaultProfile</span></span>
<span data-ttu-id="1aa7b-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1aa7b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1aa7b-122">-Force</span><span class="sxs-lookup"><span data-stu-id="1aa7b-122">-Force</span></span>
<span data-ttu-id="1aa7b-123">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1aa7b-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="1aa7b-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1aa7b-124">-InputObject</span></span>
<span data-ttu-id="1aa7b-125">파이프라인 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="1aa7b-125">The pipeline object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource
Parameter Sets: NewByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1aa7b-126">-Name</span><span class="sxs-lookup"><span data-stu-id="1aa7b-126">-Name</span></span>
<span data-ttu-id="1aa7b-127">파이프라인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1aa7b-127">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PipelineName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1aa7b-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1aa7b-128">-PassThru</span></span>
<span data-ttu-id="1aa7b-129">이 Cmdlet은 기본적으로 개체를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1aa7b-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="1aa7b-130">이 스위치를 지정하면 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="1aa7b-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="1aa7b-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1aa7b-131">-WorkspaceName</span></span>
<span data-ttu-id="1aa7b-132">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1aa7b-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="1aa7b-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="1aa7b-133">-WorkspaceObject</span></span>
<span data-ttu-id="1aa7b-134">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="1aa7b-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="1aa7b-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1aa7b-135">-Confirm</span></span>
<span data-ttu-id="1aa7b-136">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1aa7b-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1aa7b-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1aa7b-137">-WhatIf</span></span>
<span data-ttu-id="1aa7b-138">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="1aa7b-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1aa7b-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1aa7b-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1aa7b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1aa7b-140">CommonParameters</span></span>
<span data-ttu-id="1aa7b-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1aa7b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1aa7b-142">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1aa7b-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1aa7b-143">입력</span><span class="sxs-lookup"><span data-stu-id="1aa7b-143">INPUTS</span></span>

### <span data-ttu-id="1aa7b-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="1aa7b-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="1aa7b-145">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="1aa7b-145">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

## <span data-ttu-id="1aa7b-146">출력</span><span class="sxs-lookup"><span data-stu-id="1aa7b-146">OUTPUTS</span></span>

### <span data-ttu-id="1aa7b-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1aa7b-147">System.Boolean</span></span>

## <span data-ttu-id="1aa7b-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1aa7b-148">NOTES</span></span>

## <span data-ttu-id="1aa7b-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1aa7b-149">RELATED LINKS</span></span>
