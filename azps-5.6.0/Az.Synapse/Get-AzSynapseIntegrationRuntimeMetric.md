---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapseintegrationruntimemetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeMetric.md
ms.openlocfilehash: 158d4a54cdbeec0dd8cf756a3c685aede97f5bed
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994742"
---
# <span data-ttu-id="62c3b-101">Get-AzSynapseIntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="62c3b-101">Get-AzSynapseIntegrationRuntimeMetric</span></span>

## <span data-ttu-id="62c3b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62c3b-102">SYNOPSIS</span></span>
<span data-ttu-id="62c3b-103">통합 런타임에 대한 메트릭 데이터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="62c3b-103">Gets metric data for an integration runtime.</span></span> 

## <span data-ttu-id="62c3b-104">구문</span><span class="sxs-lookup"><span data-stu-id="62c3b-104">SYNTAX</span></span>

### <span data-ttu-id="62c3b-105">GetByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="62c3b-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62c3b-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="62c3b-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62c3b-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="62c3b-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="62c3b-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="62c3b-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric -InputObject <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62c3b-109">설명</span><span class="sxs-lookup"><span data-stu-id="62c3b-109">DESCRIPTION</span></span>
<span data-ttu-id="62c3b-110">**Get-AzSynapseIntegrationRuntimeMetric** cmdlet은 작업 영역의 통합 런타임에 대한 메트릭 데이터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="62c3b-110">The **Get-AzSynapseIntegrationRuntimeMetric** cmdlet gets metric data about integration runtime in a workspace.</span></span>

## <span data-ttu-id="62c3b-111">예제</span><span class="sxs-lookup"><span data-stu-id="62c3b-111">EXAMPLES</span></span>

### <span data-ttu-id="62c3b-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="62c3b-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeMetric -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="62c3b-113">이 명령은 ContosoWorkspace라는 작업 영역의 'test-selfhost-ir'이라는 통합 런타임에 대한 메트릭 데이터를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="62c3b-113">This command displays metric data about the integration runtime named 'test-selfhost-ir' in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="62c3b-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="62c3b-114">PARAMETERS</span></span>

### <span data-ttu-id="62c3b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62c3b-115">-DefaultProfile</span></span>
<span data-ttu-id="62c3b-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="62c3b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62c3b-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="62c3b-117">-InputObject</span></span>
<span data-ttu-id="62c3b-118">통합 런타임 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="62c3b-118">The integration runtime object.</span></span>

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

### <span data-ttu-id="62c3b-119">-Name</span><span class="sxs-lookup"><span data-stu-id="62c3b-119">-Name</span></span>
<span data-ttu-id="62c3b-120">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="62c3b-120">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases: IntegrationRuntimeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62c3b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62c3b-121">-ResourceGroupName</span></span>
<span data-ttu-id="62c3b-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="62c3b-122">Resource group name.</span></span>

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

### <span data-ttu-id="62c3b-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="62c3b-123">-ResourceId</span></span>
<span data-ttu-id="62c3b-124">Synapse 통합 런타임의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="62c3b-124">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="62c3b-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="62c3b-125">-WorkspaceName</span></span>
<span data-ttu-id="62c3b-126">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="62c3b-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="62c3b-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="62c3b-127">-WorkspaceObject</span></span>
<span data-ttu-id="62c3b-128">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="62c3b-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="62c3b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62c3b-129">CommonParameters</span></span>
<span data-ttu-id="62c3b-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="62c3b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62c3b-131">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="62c3b-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62c3b-132">입력</span><span class="sxs-lookup"><span data-stu-id="62c3b-132">INPUTS</span></span>

### <span data-ttu-id="62c3b-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="62c3b-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="62c3b-134">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="62c3b-134">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="62c3b-135">출력</span><span class="sxs-lookup"><span data-stu-id="62c3b-135">OUTPUTS</span></span>

### <span data-ttu-id="62c3b-136">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeMetrics</span><span class="sxs-lookup"><span data-stu-id="62c3b-136">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeMetrics</span></span>

## <span data-ttu-id="62c3b-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="62c3b-137">NOTES</span></span>

## <span data-ttu-id="62c3b-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="62c3b-138">RELATED LINKS</span></span>
