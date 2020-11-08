---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapsePipeline.md
ms.openlocfilehash: f28abbca41c68ce08e516fb52f69b7de8c54e67a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217926"
---
# <span data-ttu-id="7d0a4-101">Remove-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="7d0a4-101">Remove-AzSynapsePipeline</span></span>

## <span data-ttu-id="7d0a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d0a4-102">SYNOPSIS</span></span>
<span data-ttu-id="7d0a4-103">작업 영역에서 파이프라인을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d0a4-103">Removes a pipeline from workspace.</span></span>

## <span data-ttu-id="7d0a4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7d0a4-104">SYNTAX</span></span>

### <span data-ttu-id="7d0a4-105">RemoveByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="7d0a4-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapsePipeline -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d0a4-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="7d0a4-106">RemoveByObject</span></span>
```
Remove-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d0a4-107">NewByInputObject</span><span class="sxs-lookup"><span data-stu-id="7d0a4-107">NewByInputObject</span></span>
```
Remove-AzSynapsePipeline -Name <String> -InputObject <PSPipelineResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d0a4-108">설명은</span><span class="sxs-lookup"><span data-stu-id="7d0a4-108">DESCRIPTION</span></span>
<span data-ttu-id="7d0a4-109">**Remove-AzSynapsePipeline** cmdlet은 작업 영역에서 파이프라인을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d0a4-109">The **Remove-AzSynapsePipeline** cmdlet removes a pipeline from workspace.</span></span>

## <span data-ttu-id="7d0a4-110">예제의</span><span class="sxs-lookup"><span data-stu-id="7d0a4-110">EXAMPLES</span></span>

### <span data-ttu-id="7d0a4-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="7d0a4-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
```

<span data-ttu-id="7d0a4-112">이 cmdlet은 ContosoWorkspace 이라는 작업 영역에서 ContosoPipeline 이라는 파이프라인을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d0a4-112">This cmdlet removes the pipeline named ContosoPipeline from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="7d0a4-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="7d0a4-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapsePipeline -Name ContosoPipeline
```

<span data-ttu-id="7d0a4-114">이 cmdlet은 ContosoPipeline 이라는 파이프라인을 ContosoWorkspace에서 파이프라인 이라는 작업 영역에서 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d0a4-114">This cmdlet removes the pipeline named ContosoPipeline from the workspace named ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="7d0a4-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="7d0a4-115">Example 3</span></span>
```powershell
PS C:\> $pipeline = Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
PS C:\> $pipeline | Remove-AzSynapsePipeline
```

<span data-ttu-id="7d0a4-116">이 cmdlet은 ContosoPipeline 이라는 파이프라인을 ContosoWorkspace에서 파이프라인 이라는 작업 영역에서 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d0a4-116">This cmdlet removes the pipeline named ContosoPipeline from the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="7d0a4-117">변수</span><span class="sxs-lookup"><span data-stu-id="7d0a4-117">PARAMETERS</span></span>

### <span data-ttu-id="7d0a4-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7d0a4-118">-AsJob</span></span>
<span data-ttu-id="7d0a4-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="7d0a4-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7d0a4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d0a4-120">-DefaultProfile</span></span>
<span data-ttu-id="7d0a4-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7d0a4-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d0a4-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7d0a4-122">-InputObject</span></span>
<span data-ttu-id="7d0a4-123">파이프라인 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="7d0a4-123">The pipeline object.</span></span>

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

### <span data-ttu-id="7d0a4-124">-이름</span><span class="sxs-lookup"><span data-stu-id="7d0a4-124">-Name</span></span>
<span data-ttu-id="7d0a4-125">파이프라인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7d0a4-125">The pipeline name.</span></span>

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

### <span data-ttu-id="7d0a4-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7d0a4-126">-PassThru</span></span>
<span data-ttu-id="7d0a4-127">이 Cmdlet은 기본적으로 개체를 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7d0a4-127">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="7d0a4-128">이 스위치를 지정 하면 성공한 경우 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d0a4-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="7d0a4-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7d0a4-129">-WorkspaceName</span></span>
<span data-ttu-id="7d0a4-130">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7d0a4-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="7d0a4-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="7d0a4-131">-WorkspaceObject</span></span>
<span data-ttu-id="7d0a4-132">일반적으로 파이프라인을 통해 전달 되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="7d0a4-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="7d0a4-133">-확인</span><span class="sxs-lookup"><span data-stu-id="7d0a4-133">-Confirm</span></span>
<span data-ttu-id="7d0a4-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d0a4-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d0a4-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d0a4-135">-WhatIf</span></span>
<span data-ttu-id="7d0a4-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7d0a4-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d0a4-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7d0a4-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d0a4-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d0a4-138">CommonParameters</span></span>
<span data-ttu-id="7d0a4-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d0a4-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d0a4-140">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7d0a4-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d0a4-141">입력</span><span class="sxs-lookup"><span data-stu-id="7d0a4-141">INPUTS</span></span>

### <span data-ttu-id="7d0a4-142">Synapse. PSSynapseWorkspace/.</span><span class="sxs-lookup"><span data-stu-id="7d0a4-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="7d0a4-143">Synapse. PSPipelineResource/.</span><span class="sxs-lookup"><span data-stu-id="7d0a4-143">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

## <span data-ttu-id="7d0a4-144">출력</span><span class="sxs-lookup"><span data-stu-id="7d0a4-144">OUTPUTS</span></span>

### <span data-ttu-id="7d0a4-145">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="7d0a4-145">System.Boolean</span></span>

## <span data-ttu-id="7d0a4-146">상속자</span><span class="sxs-lookup"><span data-stu-id="7d0a4-146">NOTES</span></span>

## <span data-ttu-id="7d0a4-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7d0a4-147">RELATED LINKS</span></span>
