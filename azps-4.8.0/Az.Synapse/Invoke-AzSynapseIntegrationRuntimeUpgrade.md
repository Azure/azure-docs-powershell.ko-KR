---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/invoke-azsynapseintegrationruntimeupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseIntegrationRuntimeUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseIntegrationRuntimeUpgrade.md
ms.openlocfilehash: 59630bd0ffcf5bebfc68f647cff444466727a990
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204185"
---
# <span data-ttu-id="8486d-101">Invoke-AzSynapseIntegrationRuntimeUpgrade</span><span class="sxs-lookup"><span data-stu-id="8486d-101">Invoke-AzSynapseIntegrationRuntimeUpgrade</span></span>

## <span data-ttu-id="8486d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8486d-102">SYNOPSIS</span></span>
<span data-ttu-id="8486d-103">자체 호스팅 통합 런타임을 업그레이드 합니다.</span><span class="sxs-lookup"><span data-stu-id="8486d-103">Upgrades self-hosted integration runtime.</span></span>

## <span data-ttu-id="8486d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8486d-104">SYNTAX</span></span>

### <span data-ttu-id="8486d-105">InvokeByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="8486d-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8486d-106">InvokeByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8486d-106">InvokeByParentObjectParameterSet</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8486d-107">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8486d-107">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8486d-108">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8486d-108">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade -InputObject <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8486d-109">설명은</span><span class="sxs-lookup"><span data-stu-id="8486d-109">DESCRIPTION</span></span>
<span data-ttu-id="8486d-110">새 버전을 사용할 수 있는 경우 **AzSynapseIntegrationRuntimeUpgrade** cmdlet은 자체 호스트 된 통합 런타임을 업그레이드 합니다.</span><span class="sxs-lookup"><span data-stu-id="8486d-110">The **Invoke-AzSynapseIntegrationRuntimeUpgrade** cmdlet upgrades self-hosted integration runtime if the new version is available.</span></span>

## <span data-ttu-id="8486d-111">예제의</span><span class="sxs-lookup"><span data-stu-id="8486d-111">EXAMPLES</span></span>

### <span data-ttu-id="8486d-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="8486d-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSynapseIntegrationRuntimeUpgrade -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="8486d-113">Cmdlet이 "selfhost-ir ' 이라는 자체 호스팅 통합 런타임을 작업 영역 ContosoWorkspace에서 업그레이드 합니다.</span><span class="sxs-lookup"><span data-stu-id="8486d-113">The cmdlet upgrades self-hosted integration runtime named 'test-selfhost-ir' in workspace ContosoWorkspace.</span></span>

## <span data-ttu-id="8486d-114">변수</span><span class="sxs-lookup"><span data-stu-id="8486d-114">PARAMETERS</span></span>

### <span data-ttu-id="8486d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8486d-115">-DefaultProfile</span></span>
<span data-ttu-id="8486d-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8486d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8486d-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8486d-117">-InputObject</span></span>
<span data-ttu-id="8486d-118">통합 런타임 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="8486d-118">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: InvokeByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8486d-119">-이름</span><span class="sxs-lookup"><span data-stu-id="8486d-119">-Name</span></span>
<span data-ttu-id="8486d-120">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8486d-120">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet, InvokeByParentObjectParameterSet
Aliases: IntegrationRuntimeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8486d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8486d-121">-ResourceGroupName</span></span>
<span data-ttu-id="8486d-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8486d-122">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8486d-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8486d-123">-ResourceId</span></span>
<span data-ttu-id="8486d-124">Synapse 통합 런타임의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="8486d-124">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8486d-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8486d-125">-WorkspaceName</span></span>
<span data-ttu-id="8486d-126">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8486d-126">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8486d-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="8486d-127">-WorkspaceObject</span></span>
<span data-ttu-id="8486d-128">일반적으로 파이프라인을 통해 전달 되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="8486d-128">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: InvokeByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8486d-129">-확인</span><span class="sxs-lookup"><span data-stu-id="8486d-129">-Confirm</span></span>
<span data-ttu-id="8486d-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8486d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8486d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8486d-131">-WhatIf</span></span>
<span data-ttu-id="8486d-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8486d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8486d-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8486d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8486d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8486d-134">CommonParameters</span></span>
<span data-ttu-id="8486d-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8486d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8486d-136">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8486d-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8486d-137">입력</span><span class="sxs-lookup"><span data-stu-id="8486d-137">INPUTS</span></span>

### <span data-ttu-id="8486d-138">Synapse. PSSynapseWorkspace/.</span><span class="sxs-lookup"><span data-stu-id="8486d-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="8486d-139">Synapse. PSIntegrationRuntime/.</span><span class="sxs-lookup"><span data-stu-id="8486d-139">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="8486d-140">출력</span><span class="sxs-lookup"><span data-stu-id="8486d-140">OUTPUTS</span></span>

### <span data-ttu-id="8486d-141">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="8486d-141">System.Void</span></span>

## <span data-ttu-id="8486d-142">상속자</span><span class="sxs-lookup"><span data-stu-id="8486d-142">NOTES</span></span>

## <span data-ttu-id="8486d-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8486d-143">RELATED LINKS</span></span>
