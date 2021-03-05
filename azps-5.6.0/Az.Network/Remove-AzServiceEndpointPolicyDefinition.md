---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 65303db1c76f6e7c6e1323ed0cfc88132e4c1c23
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006128"
---
# <span data-ttu-id="3f074-101">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="3f074-101">Remove-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="3f074-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f074-102">SYNOPSIS</span></span>
<span data-ttu-id="3f074-103">서비스 엔드포인트 정책 정의를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="3f074-103">Removes a service endpoint policy definition.</span></span>

## <span data-ttu-id="3f074-104">구문</span><span class="sxs-lookup"><span data-stu-id="3f074-104">SYNTAX</span></span>

### <span data-ttu-id="3f074-105">RemoveByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="3f074-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzServiceEndpointPolicyDefinition [-Name <String>] -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f074-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f074-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -ResourceId <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f074-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f074-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -InputObject <PSServiceEndpointPolicyDefinition>
 -ServiceEndpointPolicy <PSServiceEndpointPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f074-108">설명</span><span class="sxs-lookup"><span data-stu-id="3f074-108">DESCRIPTION</span></span>
<span data-ttu-id="3f074-109">**Remove-AzServiceEndpointPolicy** cmdlet은 서비스 엔드포인트 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="3f074-109">The **Remove-AzServiceEndpointPolicy** cmdlet removes a service endpoint policy.</span></span>

## <span data-ttu-id="3f074-110">예제</span><span class="sxs-lookup"><span data-stu-id="3f074-110">EXAMPLES</span></span>

### <span data-ttu-id="3f074-111">예제 1: 이름을 사용하여 서비스 엔드포인트 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="3f074-111">Example 1: Removes a service endpoint policy using name</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -Name "PolicyDef1"
```

<span data-ttu-id="3f074-112">이 명령은 PolicyDef1 이름으로 서비스 엔드포인트 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="3f074-112">This command removes a service endpoint policy with name PolicyDef1</span></span>

## <span data-ttu-id="3f074-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="3f074-113">PARAMETERS</span></span>

### <span data-ttu-id="3f074-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f074-114">-DefaultProfile</span></span>
<span data-ttu-id="3f074-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3f074-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f074-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3f074-116">-InputObject</span></span>
<span data-ttu-id="3f074-117">서비스 엔드포인트 정책 정의 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="3f074-117">The service endpoint policy definition object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f074-118">-Name</span><span class="sxs-lookup"><span data-stu-id="3f074-118">-Name</span></span>
<span data-ttu-id="3f074-119">서비스 엔드포인트 정의의 이름</span><span class="sxs-lookup"><span data-stu-id="3f074-119">The name of the service endpoint definition</span></span>

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

### <span data-ttu-id="3f074-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3f074-120">-ResourceId</span></span>
<span data-ttu-id="3f074-121">서비스 엔드포인트 정의의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="3f074-121">The ID of the service endpoint definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f074-122">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="3f074-122">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="3f074-123">The ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="3f074-123">The ServiceEndpointPolicy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f074-124">-확인</span><span class="sxs-lookup"><span data-stu-id="3f074-124">-Confirm</span></span>
<span data-ttu-id="3f074-125">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3f074-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f074-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f074-126">-WhatIf</span></span>
<span data-ttu-id="3f074-127">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="3f074-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3f074-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3f074-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f074-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f074-129">CommonParameters</span></span>
<span data-ttu-id="3f074-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3f074-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f074-131">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="3f074-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f074-132">입력</span><span class="sxs-lookup"><span data-stu-id="3f074-132">INPUTS</span></span>

### <span data-ttu-id="3f074-133">System.String</span><span class="sxs-lookup"><span data-stu-id="3f074-133">System.String</span></span>

### <span data-ttu-id="3f074-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="3f074-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>

### <span data-ttu-id="3f074-135">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="3f074-135">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="3f074-136">출력</span><span class="sxs-lookup"><span data-stu-id="3f074-136">OUTPUTS</span></span>

### <span data-ttu-id="3f074-137">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="3f074-137">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="3f074-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3f074-138">NOTES</span></span>

## <span data-ttu-id="3f074-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3f074-139">RELATED LINKS</span></span>

[<span data-ttu-id="3f074-140">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="3f074-140">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="3f074-141">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="3f074-141">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="3f074-142">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="3f074-142">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="3f074-143">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="3f074-143">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
