---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapseintegrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseIntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseIntegrationRuntimeKey.md
ms.openlocfilehash: 836dcabaa190b66daf5a4f3f2fdaf300fe47ccdf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339825"
---
# <span data-ttu-id="419f2-101">New-AzSynapseIntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="419f2-101">New-AzSynapseIntegrationRuntimeKey</span></span>

## <span data-ttu-id="419f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="419f2-102">SYNOPSIS</span></span>
<span data-ttu-id="419f2-103">자체 호스팅 통합 런타임 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="419f2-103">Regenerate self-hosted integration runtime key.</span></span>

## <span data-ttu-id="419f2-104">구문</span><span class="sxs-lookup"><span data-stu-id="419f2-104">SYNTAX</span></span>

### <span data-ttu-id="419f2-105">NewByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="419f2-105">NewByNameParameterSet (Default)</span></span>
```
New-AzSynapseIntegrationRuntimeKey [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -KeyName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="419f2-106">NewByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="419f2-106">NewByParentObjectParameterSet</span></span>
```
New-AzSynapseIntegrationRuntimeKey -Name <String> -WorkspaceObject <PSSynapseWorkspace> -KeyName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="419f2-107">NewByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="419f2-107">NewByResourceIdParameterSet</span></span>
```
New-AzSynapseIntegrationRuntimeKey -ResourceId <String> -KeyName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="419f2-108">NewByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="419f2-108">NewByInputObjectParameterSet</span></span>
```
New-AzSynapseIntegrationRuntimeKey -InputObject <PSIntegrationRuntime> -KeyName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="419f2-109">설명</span><span class="sxs-lookup"><span data-stu-id="419f2-109">DESCRIPTION</span></span>
<span data-ttu-id="419f2-110">**New-AzSynapseIntegrationRuntimeKey** cmdlet은 'KeyName' 매개 변수에 지정된 키 이름으로 통합 런타임 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="419f2-110">The cmdlet **New-AzSynapseIntegrationRuntimeKey** regenerates the integration runtime key with the key name specified by 'KeyName' parameter.</span></span> <span data-ttu-id="419f2-111">이전 키가 잘못되었습니다.</span><span class="sxs-lookup"><span data-stu-id="419f2-111">The previous key will is invalid.</span></span>

## <span data-ttu-id="419f2-112">예제</span><span class="sxs-lookup"><span data-stu-id="419f2-112">EXAMPLES</span></span>

### <span data-ttu-id="419f2-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="419f2-113">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseIntegrationRuntimeKey -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -KeyName authKey2
```

<span data-ttu-id="419f2-114">cmdlet은 'test-selfhost-ir'이라는 통합 런타임에 대한 키 'authKey2'를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="419f2-114">The cmdlet regenerates key 'authKey2' for integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="419f2-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="419f2-115">PARAMETERS</span></span>

### <span data-ttu-id="419f2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="419f2-116">-DefaultProfile</span></span>
<span data-ttu-id="419f2-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="419f2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="419f2-118">-Force</span><span class="sxs-lookup"><span data-stu-id="419f2-118">-Force</span></span>
<span data-ttu-id="419f2-119">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="419f2-119">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="419f2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="419f2-120">-InputObject</span></span>
<span data-ttu-id="419f2-121">통합 런타임 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="419f2-121">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: NewByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="419f2-122">-KeyName</span><span class="sxs-lookup"><span data-stu-id="419f2-122">-KeyName</span></span>
<span data-ttu-id="419f2-123">자체 호스팅 통합 런타임의 인증 키 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="419f2-123">The authentication key name of the self-hosted integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AuthKey1, AuthKey2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="419f2-124">-Name</span><span class="sxs-lookup"><span data-stu-id="419f2-124">-Name</span></span>
<span data-ttu-id="419f2-125">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="419f2-125">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByNameParameterSet, NewByParentObjectParameterSet
Aliases: IntegrationRuntimeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="419f2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="419f2-126">-ResourceGroupName</span></span>
<span data-ttu-id="419f2-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="419f2-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="419f2-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="419f2-128">-ResourceId</span></span>
<span data-ttu-id="419f2-129">Synapse 통합 런타임의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="419f2-129">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="419f2-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="419f2-130">-WorkspaceName</span></span>
<span data-ttu-id="419f2-131">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="419f2-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="419f2-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="419f2-132">-WorkspaceObject</span></span>
<span data-ttu-id="419f2-133">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="419f2-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: NewByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="419f2-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="419f2-134">-Confirm</span></span>
<span data-ttu-id="419f2-135">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="419f2-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="419f2-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="419f2-136">-WhatIf</span></span>
<span data-ttu-id="419f2-137">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="419f2-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="419f2-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="419f2-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="419f2-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="419f2-139">CommonParameters</span></span>
<span data-ttu-id="419f2-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="419f2-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="419f2-141">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="419f2-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="419f2-142">입력</span><span class="sxs-lookup"><span data-stu-id="419f2-142">INPUTS</span></span>

### <span data-ttu-id="419f2-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="419f2-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="419f2-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="419f2-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="419f2-145">출력</span><span class="sxs-lookup"><span data-stu-id="419f2-145">OUTPUTS</span></span>

### <span data-ttu-id="419f2-146">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="419f2-146">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="419f2-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="419f2-147">NOTES</span></span>

## <span data-ttu-id="419f2-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="419f2-148">RELATED LINKS</span></span>
