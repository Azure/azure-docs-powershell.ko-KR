---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 285c0877441cabf51c723a472208cc002867fa7a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195636"
---
# <span data-ttu-id="e51c2-101">Get-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="e51c2-101">Get-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="e51c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e51c2-102">SYNOPSIS</span></span>
<span data-ttu-id="e51c2-103">통합 런타임 리소스에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e51c2-103">Gets information about integration runtime resources.</span></span>

## <span data-ttu-id="e51c2-104">구문</span><span class="sxs-lookup"><span data-stu-id="e51c2-104">SYNTAX</span></span>

### <span data-ttu-id="e51c2-105">GetByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="e51c2-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e51c2-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e51c2-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntime [-Name <String>] -WorkspaceObject <PSSynapseWorkspace> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e51c2-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e51c2-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntime -ResourceId <String> [-Status] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e51c2-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e51c2-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e51c2-109">설명</span><span class="sxs-lookup"><span data-stu-id="e51c2-109">DESCRIPTION</span></span>
<span data-ttu-id="e51c2-110">**Get-AzSynapseIntegrationRuntime** cmdlet은 작업 영역의 통합 런타임에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e51c2-110">The **Get-AzSynapseIntegrationRuntime** cmdlet gets information about integration runtimes in a workspace.</span></span>
<span data-ttu-id="e51c2-111">통합 런타임의 이름을 지정하면 이 cmdlet은 해당 통합 런타임에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e51c2-111">If you specify the name of an integration runtime, this cmdlet gets information about that integration runtime.</span></span>
<span data-ttu-id="e51c2-112">이름을 지정하지 않으면 이 cmdlet은 작업 영역의 모든 통합 런타임에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e51c2-112">If you do not specify a name, this cmdlet gets information about all of the integration runtimes in a workspace.</span></span>

## <span data-ttu-id="e51c2-113">예제</span><span class="sxs-lookup"><span data-stu-id="e51c2-113">EXAMPLES</span></span>

### <span data-ttu-id="e51c2-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="e51c2-114">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="e51c2-115">ContosoWorkspace라는 작업 영역의 모든 통합 런타임 나열</span><span class="sxs-lookup"><span data-stu-id="e51c2-115">List all integration runtimes in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="e51c2-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="e51c2-116">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="e51c2-117">이 명령은 ContosoWorkspace라는 작업 영역의 'test-selfhost-ir'이라는 통합 런타임에 대한 정보를 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e51c2-117">This command displays information about the integration runtime named 'test-selfhost-ir' in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="e51c2-118">예제 3</span><span class="sxs-lookup"><span data-stu-id="e51c2-118">Example 3</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -Status
```

<span data-ttu-id="e51c2-119">이 명령은 ContosoWorkspace라는 작업 영역의 'test-selfhost-ir'이라는 통합 런타임에 대한 세부 상태를 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e51c2-119">This command displays detail status about the integration runtime named 'test-selfhost-ir' in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="e51c2-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e51c2-120">PARAMETERS</span></span>

### <span data-ttu-id="e51c2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e51c2-121">-DefaultProfile</span></span>
<span data-ttu-id="e51c2-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e51c2-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e51c2-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e51c2-123">-InputObject</span></span>
<span data-ttu-id="e51c2-124">통합 런타임 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="e51c2-124">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e51c2-125">-Name</span><span class="sxs-lookup"><span data-stu-id="e51c2-125">-Name</span></span>
<span data-ttu-id="e51c2-126">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e51c2-126">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases: IntegrationRuntimeName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e51c2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e51c2-127">-ResourceGroupName</span></span>
<span data-ttu-id="e51c2-128">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e51c2-128">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e51c2-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e51c2-129">-ResourceId</span></span>
<span data-ttu-id="e51c2-130">Synapse 통합 런타임의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="e51c2-130">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e51c2-131">-Status</span><span class="sxs-lookup"><span data-stu-id="e51c2-131">-Status</span></span>
<span data-ttu-id="e51c2-132">통합 런타임 세부 정보 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="e51c2-132">The integration runtime detail status.</span></span>

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

### <span data-ttu-id="e51c2-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e51c2-133">-WorkspaceName</span></span>
<span data-ttu-id="e51c2-134">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e51c2-134">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e51c2-135">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e51c2-135">-WorkspaceObject</span></span>
<span data-ttu-id="e51c2-136">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="e51c2-136">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e51c2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e51c2-137">CommonParameters</span></span>
<span data-ttu-id="e51c2-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e51c2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e51c2-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e51c2-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e51c2-140">입력</span><span class="sxs-lookup"><span data-stu-id="e51c2-140">INPUTS</span></span>

### <span data-ttu-id="e51c2-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e51c2-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="e51c2-142">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="e51c2-142">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="e51c2-143">출력</span><span class="sxs-lookup"><span data-stu-id="e51c2-143">OUTPUTS</span></span>

### <span data-ttu-id="e51c2-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="e51c2-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="e51c2-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e51c2-145">NOTES</span></span>

## <span data-ttu-id="e51c2-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e51c2-146">RELATED LINKS</span></span>
