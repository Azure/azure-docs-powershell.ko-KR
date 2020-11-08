---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/sync-azsynapseintegrationruntimecredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Sync-AzSynapseIntegrationRuntimeCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Sync-AzSynapseIntegrationRuntimeCredential.md
ms.openlocfilehash: feb9d74cf49dfa8ae5455b303ee78f443a08e942
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215160"
---
# <span data-ttu-id="d7934-101">Sync-AzSynapseIntegrationRuntimeCredential</span><span class="sxs-lookup"><span data-stu-id="d7934-101">Sync-AzSynapseIntegrationRuntimeCredential</span></span>

## <span data-ttu-id="d7934-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7934-102">SYNOPSIS</span></span>
<span data-ttu-id="d7934-103">통합 런타임 노드 간에 자격 증명을 동기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7934-103">Synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="d7934-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d7934-104">SYNTAX</span></span>

### <span data-ttu-id="d7934-105">StopByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="d7934-105">StopByNameParameterSet (Default)</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d7934-106">StopByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7934-106">StopByParentObjectParameterSet</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential -IntegrationRuntimeName <String>
 -WorkspaceObject <PSSynapseWorkspace> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d7934-107">StopByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7934-107">StopByResourceIdParameterSet</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential -ResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7934-108">StopByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7934-108">StopByInputObjectParameterSet</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential -InputObject <PSIntegrationRuntime> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7934-109">설명은</span><span class="sxs-lookup"><span data-stu-id="d7934-109">DESCRIPTION</span></span>
<span data-ttu-id="d7934-110">**AzSynapseIntegrationRuntimeCredential** cmdlet은 통합 런타임 노드 간에 온-프레미스 자격 증명을 동기화 하므로 모든 노드에서 자격 증명을 동일 하 게 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d7934-110">The **Sync-AzSynapseIntegrationRuntimeCredential** cmdlet synchronizes on-premises credentials among integration runtime nodes, which forces the credentials to be identical in all nodes.</span></span>

## <span data-ttu-id="d7934-111">예제의</span><span class="sxs-lookup"><span data-stu-id="d7934-111">EXAMPLES</span></span>

### <span data-ttu-id="d7934-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="d7934-112">Example 1</span></span>
```powershell
PS C:\> Sync-AzSynapseIntegrationRuntimeCredential -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir'
```

<span data-ttu-id="d7934-113">통합 런타임 노드 간에 자격 증명을 동기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7934-113">Synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="d7934-114">변수</span><span class="sxs-lookup"><span data-stu-id="d7934-114">PARAMETERS</span></span>

### <span data-ttu-id="d7934-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7934-115">-DefaultProfile</span></span>
<span data-ttu-id="d7934-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d7934-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7934-117">-Force</span><span class="sxs-lookup"><span data-stu-id="d7934-117">-Force</span></span>
<span data-ttu-id="d7934-118">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d7934-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="d7934-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d7934-119">-InputObject</span></span>
<span data-ttu-id="d7934-120">통합 런타임 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d7934-120">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: StopByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d7934-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="d7934-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="d7934-122">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d7934-122">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameParameterSet, StopByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7934-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7934-123">-ResourceGroupName</span></span>
<span data-ttu-id="d7934-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d7934-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7934-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d7934-125">-ResourceId</span></span>
<span data-ttu-id="d7934-126">Synapse 통합 런타임의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="d7934-126">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7934-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d7934-127">-WorkspaceName</span></span>
<span data-ttu-id="d7934-128">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d7934-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7934-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d7934-129">-WorkspaceObject</span></span>
<span data-ttu-id="d7934-130">일반적으로 파이프라인을 통해 전달 되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d7934-130">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: StopByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d7934-131">-확인</span><span class="sxs-lookup"><span data-stu-id="d7934-131">-Confirm</span></span>
<span data-ttu-id="d7934-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7934-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7934-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7934-133">-WhatIf</span></span>
<span data-ttu-id="d7934-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d7934-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7934-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d7934-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7934-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7934-136">CommonParameters</span></span>
<span data-ttu-id="d7934-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7934-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7934-138">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d7934-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7934-139">입력</span><span class="sxs-lookup"><span data-stu-id="d7934-139">INPUTS</span></span>

### <span data-ttu-id="d7934-140">Synapse. PSSynapseWorkspace/.</span><span class="sxs-lookup"><span data-stu-id="d7934-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="d7934-141">Synapse. PSIntegrationRuntime/.</span><span class="sxs-lookup"><span data-stu-id="d7934-141">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="d7934-142">출력</span><span class="sxs-lookup"><span data-stu-id="d7934-142">OUTPUTS</span></span>

### <span data-ttu-id="d7934-143">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="d7934-143">System.Void</span></span>

## <span data-ttu-id="d7934-144">상속자</span><span class="sxs-lookup"><span data-stu-id="d7934-144">NOTES</span></span>

## <span data-ttu-id="d7934-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d7934-145">RELATED LINKS</span></span>
