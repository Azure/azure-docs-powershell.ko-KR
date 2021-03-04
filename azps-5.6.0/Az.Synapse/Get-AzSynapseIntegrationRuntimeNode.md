---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapseintegrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeNode.md
ms.openlocfilehash: dbd791b3ab77889e8c78279b576b614c4d86b4b9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994737"
---
# <span data-ttu-id="a3f1f-101">Get-AzSynapseIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="a3f1f-101">Get-AzSynapseIntegrationRuntimeNode</span></span>

## <span data-ttu-id="a3f1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3f1f-102">SYNOPSIS</span></span>
<span data-ttu-id="a3f1f-103">통합 런타임 노드 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a3f1f-103">Gets an integration runtime node information.</span></span>

## <span data-ttu-id="a3f1f-104">구문</span><span class="sxs-lookup"><span data-stu-id="a3f1f-104">SYNTAX</span></span>

### <span data-ttu-id="a3f1f-105">GetByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="a3f1f-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntimeNode [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> -Name <String> [-IpAddress] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a3f1f-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3f1f-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeNode -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 -Name <String> [-IpAddress] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a3f1f-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3f1f-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeNode -ResourceId <String> -Name <String> [-IpAddress]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a3f1f-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3f1f-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeNode -InputObject <PSIntegrationRuntime> -Name <String> [-IpAddress]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3f1f-109">설명</span><span class="sxs-lookup"><span data-stu-id="a3f1f-109">DESCRIPTION</span></span>
<span data-ttu-id="a3f1f-110">**Get-AzSynapseIntegrationRuntimeNode** cmdlet은 통합 런타임 노드의 세부 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="a3f1f-110">The **Get-AzSynapseIntegrationRuntimeNode** cmdlet gets the detail information of an integration runtime node.</span></span>

## <span data-ttu-id="a3f1f-111">예제</span><span class="sxs-lookup"><span data-stu-id="a3f1f-111">EXAMPLES</span></span>

### <span data-ttu-id="a3f1f-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="a3f1f-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1'
```

<span data-ttu-id="a3f1f-113">cmdlet은 작업 영역 ContosoWorkspace의 자체 호스팅 통합 Node_1 'test-selfhost-ir'에서 'Node_1'라는 노드 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a3f1f-113">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="a3f1f-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="a3f1f-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1' -IpAddress
```

<span data-ttu-id="a3f1f-115">cmdlet은 IP 주소를 포함하여 작업 영역 'test-df-eu2'Node_1 자체 호스팅 통합 런타임 'test-selfhost-ir'에서 'Node_1'라는 노드 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a3f1f-115">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in workspace 'test-df-eu2', including the IP address.</span></span>

## <span data-ttu-id="a3f1f-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a3f1f-116">PARAMETERS</span></span>

### <span data-ttu-id="a3f1f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3f1f-117">-DefaultProfile</span></span>
<span data-ttu-id="a3f1f-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a3f1f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3f1f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a3f1f-119">-InputObject</span></span>
<span data-ttu-id="a3f1f-120">통합 런타임 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="a3f1f-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="a3f1f-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="a3f1f-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="a3f1f-122">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a3f1f-122">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3f1f-123">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="a3f1f-123">-IpAddress</span></span>
<span data-ttu-id="a3f1f-124">통합 런타임 노드의 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="a3f1f-124">The IP Address of integration runtime node.</span></span>

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

### <span data-ttu-id="a3f1f-125">-Name</span><span class="sxs-lookup"><span data-stu-id="a3f1f-125">-Name</span></span>
<span data-ttu-id="a3f1f-126">통합 런타임 노드 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a3f1f-126">The integration runtime node name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3f1f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3f1f-127">-ResourceGroupName</span></span>
<span data-ttu-id="a3f1f-128">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a3f1f-128">Resource group name.</span></span>

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

### <span data-ttu-id="a3f1f-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a3f1f-129">-ResourceId</span></span>
<span data-ttu-id="a3f1f-130">Synapse 통합 런타임의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="a3f1f-130">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="a3f1f-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a3f1f-131">-WorkspaceName</span></span>
<span data-ttu-id="a3f1f-132">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a3f1f-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="a3f1f-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a3f1f-133">-WorkspaceObject</span></span>
<span data-ttu-id="a3f1f-134">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="a3f1f-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a3f1f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3f1f-135">CommonParameters</span></span>
<span data-ttu-id="a3f1f-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a3f1f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3f1f-137">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a3f1f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3f1f-138">입력</span><span class="sxs-lookup"><span data-stu-id="a3f1f-138">INPUTS</span></span>

### <span data-ttu-id="a3f1f-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a3f1f-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="a3f1f-140">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="a3f1f-140">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="a3f1f-141">출력</span><span class="sxs-lookup"><span data-stu-id="a3f1f-141">OUTPUTS</span></span>

### <span data-ttu-id="a3f1f-142">Microsoft.Azure.Commands.Synapse.Models.PSManagedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="a3f1f-142">Microsoft.Azure.Commands.Synapse.Models.PSManagedIntegrationRuntimeNode</span></span>

### <span data-ttu-id="a3f1f-143">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="a3f1f-143">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeNode</span></span>

## <span data-ttu-id="a3f1f-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a3f1f-144">NOTES</span></span>

## <span data-ttu-id="a3f1f-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a3f1f-145">RELATED LINKS</span></span>
