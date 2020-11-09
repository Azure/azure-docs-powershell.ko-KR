---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseintegrationruntimemetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeMetric.md
ms.openlocfilehash: 0b6700d11b017f00f10328afae2cc6638087f216
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309846"
---
# <span data-ttu-id="7b73d-101">Get-AzSynapseIntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="7b73d-101">Get-AzSynapseIntegrationRuntimeMetric</span></span>

## <span data-ttu-id="7b73d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b73d-102">SYNOPSIS</span></span>
<span data-ttu-id="7b73d-103">통합 런타임에 대 한 메트릭 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7b73d-103">Gets metric data for an integration runtime.</span></span> 

## <span data-ttu-id="7b73d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7b73d-104">SYNTAX</span></span>

### <span data-ttu-id="7b73d-105">GetByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="7b73d-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b73d-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b73d-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b73d-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b73d-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7b73d-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b73d-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric -InputObject <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b73d-109">설명은</span><span class="sxs-lookup"><span data-stu-id="7b73d-109">DESCRIPTION</span></span>
<span data-ttu-id="7b73d-110">**AzSynapseIntegrationRuntimeMetric** cmdlet은 작업 영역의 통합 런타임에 대 한 메트릭 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7b73d-110">The **Get-AzSynapseIntegrationRuntimeMetric** cmdlet gets metric data about integration runtime in a workspace.</span></span>

## <span data-ttu-id="7b73d-111">예제의</span><span class="sxs-lookup"><span data-stu-id="7b73d-111">EXAMPLES</span></span>

### <span data-ttu-id="7b73d-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="7b73d-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeMetric -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="7b73d-113">이 명령은 ContosoWorkspace 이라는 작업 영역의 ' selfhost-ir ' 이라는 통합 런타임에 대 한 메트릭 데이터를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b73d-113">This command displays metric data about the integration runtime named 'test-selfhost-ir' in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="7b73d-114">변수</span><span class="sxs-lookup"><span data-stu-id="7b73d-114">PARAMETERS</span></span>

### <span data-ttu-id="7b73d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b73d-115">-DefaultProfile</span></span>
<span data-ttu-id="7b73d-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7b73d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b73d-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7b73d-117">-InputObject</span></span>
<span data-ttu-id="7b73d-118">통합 런타임 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="7b73d-118">The integration runtime object.</span></span>

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

### <span data-ttu-id="7b73d-119">-이름</span><span class="sxs-lookup"><span data-stu-id="7b73d-119">-Name</span></span>
<span data-ttu-id="7b73d-120">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7b73d-120">The integration runtime name.</span></span>

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

### <span data-ttu-id="7b73d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b73d-121">-ResourceGroupName</span></span>
<span data-ttu-id="7b73d-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7b73d-122">Resource group name.</span></span>

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

### <span data-ttu-id="7b73d-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7b73d-123">-ResourceId</span></span>
<span data-ttu-id="7b73d-124">Synapse 통합 런타임의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="7b73d-124">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="7b73d-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7b73d-125">-WorkspaceName</span></span>
<span data-ttu-id="7b73d-126">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7b73d-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="7b73d-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="7b73d-127">-WorkspaceObject</span></span>
<span data-ttu-id="7b73d-128">일반적으로 파이프라인을 통해 전달 되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="7b73d-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="7b73d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b73d-129">CommonParameters</span></span>
<span data-ttu-id="7b73d-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b73d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b73d-131">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7b73d-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b73d-132">입력</span><span class="sxs-lookup"><span data-stu-id="7b73d-132">INPUTS</span></span>

### <span data-ttu-id="7b73d-133">Synapse. PSSynapseWorkspace/.</span><span class="sxs-lookup"><span data-stu-id="7b73d-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="7b73d-134">Synapse. PSIntegrationRuntime/.</span><span class="sxs-lookup"><span data-stu-id="7b73d-134">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="7b73d-135">출력</span><span class="sxs-lookup"><span data-stu-id="7b73d-135">OUTPUTS</span></span>

### <span data-ttu-id="7b73d-136">Synapse. PSIntegrationRuntimeMetrics/.</span><span class="sxs-lookup"><span data-stu-id="7b73d-136">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeMetrics</span></span>

## <span data-ttu-id="7b73d-137">상속자</span><span class="sxs-lookup"><span data-stu-id="7b73d-137">NOTES</span></span>

## <span data-ttu-id="7b73d-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7b73d-138">RELATED LINKS</span></span>
