---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseintegrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeKey.md
ms.openlocfilehash: 08ce91d6d9a942dd20078e0c3b5b537360aac9fc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339242"
---
# <span data-ttu-id="11e00-101">Get-AzSynapseIntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="11e00-101">Get-AzSynapseIntegrationRuntimeKey</span></span>

## <span data-ttu-id="11e00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11e00-102">SYNOPSIS</span></span>
<span data-ttu-id="11e00-103">자체 호스팅 통합 런타임에 대한 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="11e00-103">Gets keys for a self-hosted integration runtime.</span></span>

## <span data-ttu-id="11e00-104">구문</span><span class="sxs-lookup"><span data-stu-id="11e00-104">SYNTAX</span></span>

### <span data-ttu-id="11e00-105">GetByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="11e00-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntimeKey [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11e00-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="11e00-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeKey -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11e00-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="11e00-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="11e00-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="11e00-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeKey -InputObject <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11e00-109">설명</span><span class="sxs-lookup"><span data-stu-id="11e00-109">DESCRIPTION</span></span>
<span data-ttu-id="11e00-110">**Get-AzSynapseIntegrationRuntimeKey** cmdlet은 통합 런타임에 대한 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="11e00-110">The **Get-AzSynapseIntegrationRuntimeKey** cmdlet gets keys for an integration runtime.</span></span> <span data-ttu-id="11e00-111">키는 통합 런타임 노드를 등록하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="11e00-111">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="11e00-112">예제</span><span class="sxs-lookup"><span data-stu-id="11e00-112">EXAMPLES</span></span>

### <span data-ttu-id="11e00-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="11e00-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeKey -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="11e00-114">cmdlet은 'test-selfhost-ir'이라는 통합 런타임에 대한 키를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="11e00-114">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="11e00-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="11e00-115">PARAMETERS</span></span>

### <span data-ttu-id="11e00-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11e00-116">-DefaultProfile</span></span>
<span data-ttu-id="11e00-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="11e00-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11e00-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11e00-118">-InputObject</span></span>
<span data-ttu-id="11e00-119">통합 런타임 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="11e00-119">The integration runtime object.</span></span>

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

### <span data-ttu-id="11e00-120">-Name</span><span class="sxs-lookup"><span data-stu-id="11e00-120">-Name</span></span>
<span data-ttu-id="11e00-121">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="11e00-121">The integration runtime name.</span></span>

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

### <span data-ttu-id="11e00-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11e00-122">-ResourceGroupName</span></span>
<span data-ttu-id="11e00-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="11e00-123">Resource group name.</span></span>

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

### <span data-ttu-id="11e00-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="11e00-124">-ResourceId</span></span>
<span data-ttu-id="11e00-125">Synapse 통합 런타임의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="11e00-125">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="11e00-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="11e00-126">-WorkspaceName</span></span>
<span data-ttu-id="11e00-127">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="11e00-127">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="11e00-128">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="11e00-128">-WorkspaceObject</span></span>
<span data-ttu-id="11e00-129">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="11e00-129">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="11e00-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11e00-130">CommonParameters</span></span>
<span data-ttu-id="11e00-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="11e00-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11e00-132">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="11e00-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11e00-133">입력</span><span class="sxs-lookup"><span data-stu-id="11e00-133">INPUTS</span></span>

### <span data-ttu-id="11e00-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="11e00-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="11e00-135">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="11e00-135">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="11e00-136">출력</span><span class="sxs-lookup"><span data-stu-id="11e00-136">OUTPUTS</span></span>

### <span data-ttu-id="11e00-137">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="11e00-137">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="11e00-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="11e00-138">NOTES</span></span>

## <span data-ttu-id="11e00-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="11e00-139">RELATED LINKS</span></span>
