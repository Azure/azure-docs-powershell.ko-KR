---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseintegrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeNode.md
ms.openlocfilehash: 5df58da7ef5fa0829da27f4d6a46372f42bc9dc5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384056"
---
# <span data-ttu-id="a444a-101">Get-AzSynapseIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="a444a-101">Get-AzSynapseIntegrationRuntimeNode</span></span>

## <span data-ttu-id="a444a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a444a-102">SYNOPSIS</span></span>
<span data-ttu-id="a444a-103">통합 런타임 노드 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a444a-103">Gets an integration runtime node information.</span></span>

## <span data-ttu-id="a444a-104">구문</span><span class="sxs-lookup"><span data-stu-id="a444a-104">SYNTAX</span></span>

### <span data-ttu-id="a444a-105">GetByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="a444a-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntimeNode [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> -Name <String> [-IpAddress] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a444a-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a444a-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeNode -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 -Name <String> [-IpAddress] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a444a-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a444a-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeNode -ResourceId <String> -Name <String> [-IpAddress]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a444a-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a444a-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeNode -InputObject <PSIntegrationRuntime> -Name <String> [-IpAddress]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a444a-109">설명</span><span class="sxs-lookup"><span data-stu-id="a444a-109">DESCRIPTION</span></span>
<span data-ttu-id="a444a-110">**Get-AzSynapseIntegrationRuntimeNode** cmdlet은 통합 런타임 노드의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a444a-110">The **Get-AzSynapseIntegrationRuntimeNode** cmdlet gets the detail information of an integration runtime node.</span></span>

## <span data-ttu-id="a444a-111">예제</span><span class="sxs-lookup"><span data-stu-id="a444a-111">EXAMPLES</span></span>

### <span data-ttu-id="a444a-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="a444a-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1'
```

<span data-ttu-id="a444a-113">cmdlet은 작업 영역 ContosoWorkspace의 자체 호스팅 통합 런타임 'test-selfhost-ir'에서 'Node_1'라는 노드의 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a444a-113">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="a444a-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="a444a-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1' -IpAddress
```

<span data-ttu-id="a444a-115">cmdlet은 IP 주소를 포함하여 작업 영역 'test-df-eu2'의 자체 호스팅 통합 런타임 'test-selfhost-ir'에서 'Node_1'라는 노드의 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a444a-115">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in workspace 'test-df-eu2', including the IP address.</span></span>

## <span data-ttu-id="a444a-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a444a-116">PARAMETERS</span></span>

### <span data-ttu-id="a444a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a444a-117">-DefaultProfile</span></span>
<span data-ttu-id="a444a-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a444a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a444a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a444a-119">-InputObject</span></span>
<span data-ttu-id="a444a-120">통합 런타임 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="a444a-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="a444a-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="a444a-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="a444a-122">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a444a-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="a444a-123">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="a444a-123">-IpAddress</span></span>
<span data-ttu-id="a444a-124">통합 런타임 노드의 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="a444a-124">The IP Address of integration runtime node.</span></span>

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

### <span data-ttu-id="a444a-125">-Name</span><span class="sxs-lookup"><span data-stu-id="a444a-125">-Name</span></span>
<span data-ttu-id="a444a-126">통합 런타임 노드 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a444a-126">The integration runtime node name.</span></span>

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

### <span data-ttu-id="a444a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a444a-127">-ResourceGroupName</span></span>
<span data-ttu-id="a444a-128">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a444a-128">Resource group name.</span></span>

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

### <span data-ttu-id="a444a-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a444a-129">-ResourceId</span></span>
<span data-ttu-id="a444a-130">Synapse 통합 런타임의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="a444a-130">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="a444a-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a444a-131">-WorkspaceName</span></span>
<span data-ttu-id="a444a-132">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a444a-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="a444a-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a444a-133">-WorkspaceObject</span></span>
<span data-ttu-id="a444a-134">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="a444a-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a444a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a444a-135">CommonParameters</span></span>
<span data-ttu-id="a444a-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a444a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a444a-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a444a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a444a-138">입력</span><span class="sxs-lookup"><span data-stu-id="a444a-138">INPUTS</span></span>

### <span data-ttu-id="a444a-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a444a-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="a444a-140">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="a444a-140">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="a444a-141">출력</span><span class="sxs-lookup"><span data-stu-id="a444a-141">OUTPUTS</span></span>

### <span data-ttu-id="a444a-142">Microsoft.Azure.Commands.Synapse.Models.PSManagedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="a444a-142">Microsoft.Azure.Commands.Synapse.Models.PSManagedIntegrationRuntimeNode</span></span>

### <span data-ttu-id="a444a-143">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="a444a-143">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeNode</span></span>

## <span data-ttu-id="a444a-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a444a-144">NOTES</span></span>

## <span data-ttu-id="a444a-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a444a-145">RELATED LINKS</span></span>
