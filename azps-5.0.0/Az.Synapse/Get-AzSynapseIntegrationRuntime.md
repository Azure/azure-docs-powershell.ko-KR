---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 285c0877441cabf51c723a472208cc002867fa7a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217964"
---
# <span data-ttu-id="a3e61-101">Get-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="a3e61-101">Get-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="a3e61-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3e61-102">SYNOPSIS</span></span>
<span data-ttu-id="a3e61-103">통합 런타임 리소스에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a3e61-103">Gets information about integration runtime resources.</span></span>

## <span data-ttu-id="a3e61-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a3e61-104">SYNTAX</span></span>

### <span data-ttu-id="a3e61-105">GetByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="a3e61-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a3e61-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3e61-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntime [-Name <String>] -WorkspaceObject <PSSynapseWorkspace> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a3e61-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3e61-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntime -ResourceId <String> [-Status] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a3e61-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3e61-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3e61-109">설명은</span><span class="sxs-lookup"><span data-stu-id="a3e61-109">DESCRIPTION</span></span>
<span data-ttu-id="a3e61-110">**AzSynapseIntegrationRuntime** cmdlet은 작업 영역의 통합 런타임에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a3e61-110">The **Get-AzSynapseIntegrationRuntime** cmdlet gets information about integration runtimes in a workspace.</span></span>
<span data-ttu-id="a3e61-111">통합 런타임의 이름을 지정 하면이 cmdlet은 해당 통합 런타임에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a3e61-111">If you specify the name of an integration runtime, this cmdlet gets information about that integration runtime.</span></span>
<span data-ttu-id="a3e61-112">이름을 지정 하지 않으면이 cmdlet은 작업 영역의 모든 통합 런타임에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a3e61-112">If you do not specify a name, this cmdlet gets information about all of the integration runtimes in a workspace.</span></span>

## <span data-ttu-id="a3e61-113">예제의</span><span class="sxs-lookup"><span data-stu-id="a3e61-113">EXAMPLES</span></span>

### <span data-ttu-id="a3e61-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="a3e61-114">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="a3e61-115">ContosoWorkspace 이라는 작업 영역의 모든 통합 런타임을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3e61-115">List all integration runtimes in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="a3e61-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="a3e61-116">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="a3e61-117">이 명령은 ContosoWorkspace 이라는 작업 영역의 ' selfhost-ir ' 이라는 통합 런타임에 대 한 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3e61-117">This command displays information about the integration runtime named 'test-selfhost-ir' in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="a3e61-118">예제 3</span><span class="sxs-lookup"><span data-stu-id="a3e61-118">Example 3</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -Status
```

<span data-ttu-id="a3e61-119">이 명령은 ContosoWorkspace 이라는 작업 영역의 ' selfhost-ir ' 이라는 통합 런타임에 대 한 세부 정보 상태를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3e61-119">This command displays detail status about the integration runtime named 'test-selfhost-ir' in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="a3e61-120">변수</span><span class="sxs-lookup"><span data-stu-id="a3e61-120">PARAMETERS</span></span>

### <span data-ttu-id="a3e61-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3e61-121">-DefaultProfile</span></span>
<span data-ttu-id="a3e61-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a3e61-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3e61-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a3e61-123">-InputObject</span></span>
<span data-ttu-id="a3e61-124">통합 런타임 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="a3e61-124">The integration runtime object.</span></span>

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

### <span data-ttu-id="a3e61-125">-이름</span><span class="sxs-lookup"><span data-stu-id="a3e61-125">-Name</span></span>
<span data-ttu-id="a3e61-126">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a3e61-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="a3e61-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3e61-127">-ResourceGroupName</span></span>
<span data-ttu-id="a3e61-128">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a3e61-128">Resource group name.</span></span>

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

### <span data-ttu-id="a3e61-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a3e61-129">-ResourceId</span></span>
<span data-ttu-id="a3e61-130">Synapse 통합 런타임의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="a3e61-130">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="a3e61-131">-상태</span><span class="sxs-lookup"><span data-stu-id="a3e61-131">-Status</span></span>
<span data-ttu-id="a3e61-132">통합 런타임 세부 정보 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="a3e61-132">The integration runtime detail status.</span></span>

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

### <span data-ttu-id="a3e61-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a3e61-133">-WorkspaceName</span></span>
<span data-ttu-id="a3e61-134">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a3e61-134">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="a3e61-135">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a3e61-135">-WorkspaceObject</span></span>
<span data-ttu-id="a3e61-136">일반적으로 파이프라인을 통해 전달 되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="a3e61-136">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a3e61-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3e61-137">CommonParameters</span></span>
<span data-ttu-id="a3e61-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3e61-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3e61-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a3e61-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3e61-140">입력</span><span class="sxs-lookup"><span data-stu-id="a3e61-140">INPUTS</span></span>

### <span data-ttu-id="a3e61-141">Synapse. PSSynapseWorkspace/.</span><span class="sxs-lookup"><span data-stu-id="a3e61-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="a3e61-142">Synapse. PSIntegrationRuntime/.</span><span class="sxs-lookup"><span data-stu-id="a3e61-142">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="a3e61-143">출력</span><span class="sxs-lookup"><span data-stu-id="a3e61-143">OUTPUTS</span></span>

### <span data-ttu-id="a3e61-144">Synapse. PSIntegrationRuntime/.</span><span class="sxs-lookup"><span data-stu-id="a3e61-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="a3e61-145">상속자</span><span class="sxs-lookup"><span data-stu-id="a3e61-145">NOTES</span></span>

## <span data-ttu-id="a3e61-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a3e61-146">RELATED LINKS</span></span>
