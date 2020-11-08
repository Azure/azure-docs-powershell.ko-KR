---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 57b6c6619a45e515c7aff2e30edc346ff39af9ac
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056631"
---
# <span data-ttu-id="fbcb8-101">Remove-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="fbcb8-101">Remove-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="fbcb8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbcb8-102">SYNOPSIS</span></span>
<span data-ttu-id="fbcb8-103">통합 런타임을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbcb8-103">Removes an integration runtime.</span></span>

## <span data-ttu-id="fbcb8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fbcb8-104">SYNTAX</span></span>

### <span data-ttu-id="fbcb8-105">RemoveByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="fbcb8-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbcb8-106">RemoveByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fbcb8-106">RemoveByParentObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntime -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbcb8-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fbcb8-107">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntime -ResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbcb8-108">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fbcb8-108">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fbcb8-109">설명은</span><span class="sxs-lookup"><span data-stu-id="fbcb8-109">DESCRIPTION</span></span>
<span data-ttu-id="fbcb8-110">**AzSynapseIntegrationRuntime** cmdlet은 통합 런타임을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbcb8-110">The **Remove-AzSynapseIntegrationRuntime** cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="fbcb8-111">예제의</span><span class="sxs-lookup"><span data-stu-id="fbcb8-111">EXAMPLES</span></span>

### <span data-ttu-id="fbcb8-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="fbcb8-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="fbcb8-113">이 명령은 ContosoWorkspace 이라는 작업 영역에서 ' 테스트 예약-ir ' 이라는 이름의 통합 런타임을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbcb8-113">This command removes the integration runtime named 'test-reserved-ir' from the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="fbcb8-114">변수</span><span class="sxs-lookup"><span data-stu-id="fbcb8-114">PARAMETERS</span></span>

### <span data-ttu-id="fbcb8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbcb8-115">-DefaultProfile</span></span>
<span data-ttu-id="fbcb8-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fbcb8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fbcb8-117">-Force</span><span class="sxs-lookup"><span data-stu-id="fbcb8-117">-Force</span></span>
<span data-ttu-id="fbcb8-118">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fbcb8-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="fbcb8-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fbcb8-119">-InputObject</span></span>
<span data-ttu-id="fbcb8-120">통합 런타임 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="fbcb8-120">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fbcb8-121">-이름</span><span class="sxs-lookup"><span data-stu-id="fbcb8-121">-Name</span></span>
<span data-ttu-id="fbcb8-122">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fbcb8-122">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet, RemoveByParentObjectParameterSet
Aliases: IntegrationRuntimeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbcb8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbcb8-123">-ResourceGroupName</span></span>
<span data-ttu-id="fbcb8-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fbcb8-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbcb8-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fbcb8-125">-ResourceId</span></span>
<span data-ttu-id="fbcb8-126">Synapse 통합 런타임의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="fbcb8-126">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbcb8-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="fbcb8-127">-WorkspaceName</span></span>
<span data-ttu-id="fbcb8-128">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fbcb8-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbcb8-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="fbcb8-129">-WorkspaceObject</span></span>
<span data-ttu-id="fbcb8-130">일반적으로 파이프라인을 통해 전달 되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="fbcb8-130">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fbcb8-131">-확인</span><span class="sxs-lookup"><span data-stu-id="fbcb8-131">-Confirm</span></span>
<span data-ttu-id="fbcb8-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbcb8-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbcb8-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbcb8-133">-WhatIf</span></span>
<span data-ttu-id="fbcb8-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fbcb8-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbcb8-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fbcb8-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbcb8-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbcb8-136">CommonParameters</span></span>
<span data-ttu-id="fbcb8-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbcb8-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbcb8-138">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fbcb8-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbcb8-139">입력</span><span class="sxs-lookup"><span data-stu-id="fbcb8-139">INPUTS</span></span>

### <span data-ttu-id="fbcb8-140">Synapse. PSSynapseWorkspace/.</span><span class="sxs-lookup"><span data-stu-id="fbcb8-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="fbcb8-141">Synapse. PSIntegrationRuntime/.</span><span class="sxs-lookup"><span data-stu-id="fbcb8-141">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="fbcb8-142">출력</span><span class="sxs-lookup"><span data-stu-id="fbcb8-142">OUTPUTS</span></span>

### <span data-ttu-id="fbcb8-143">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="fbcb8-143">System.Void</span></span>

## <span data-ttu-id="fbcb8-144">상속자</span><span class="sxs-lookup"><span data-stu-id="fbcb8-144">NOTES</span></span>

## <span data-ttu-id="fbcb8-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fbcb8-145">RELATED LINKS</span></span>
