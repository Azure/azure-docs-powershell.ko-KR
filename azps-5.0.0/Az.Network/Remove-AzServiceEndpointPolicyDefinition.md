---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 146e43ce5f1816994a1d408e215e4b3e27c2bbca
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216392"
---
# <span data-ttu-id="5cbe6-101">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="5cbe6-101">Remove-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="5cbe6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5cbe6-102">SYNOPSIS</span></span>
<span data-ttu-id="5cbe6-103">서비스 끝점 정책 정의를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cbe6-103">Removes a service endpoint policy definition.</span></span>

## <span data-ttu-id="5cbe6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5cbe6-104">SYNTAX</span></span>

### <span data-ttu-id="5cbe6-105">RemoveByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="5cbe6-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzServiceEndpointPolicyDefinition [-Name <String>] -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cbe6-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5cbe6-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -ResourceId <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cbe6-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5cbe6-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -InputObject <PSServiceEndpointPolicyDefinition>
 -ServiceEndpointPolicy <PSServiceEndpointPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5cbe6-108">설명은</span><span class="sxs-lookup"><span data-stu-id="5cbe6-108">DESCRIPTION</span></span>
<span data-ttu-id="5cbe6-109">**AzServiceEndpointPolicy** cmdlet은 서비스 끝점 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cbe6-109">The **Remove-AzServiceEndpointPolicy** cmdlet removes a service endpoint policy.</span></span>

## <span data-ttu-id="5cbe6-110">예제의</span><span class="sxs-lookup"><span data-stu-id="5cbe6-110">EXAMPLES</span></span>

### <span data-ttu-id="5cbe6-111">예제 1: 이름을 사용 하 여 서비스 끝점 정책 제거</span><span class="sxs-lookup"><span data-stu-id="5cbe6-111">Example 1: Removes a service endpoint policy using name</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -Name "PolicyDef1"
```

<span data-ttu-id="5cbe6-112">이 명령은 이름이 PolicyDef1 인 서비스 끝점 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cbe6-112">This command removes a service endpoint policy with name PolicyDef1</span></span>

## <span data-ttu-id="5cbe6-113">변수</span><span class="sxs-lookup"><span data-stu-id="5cbe6-113">PARAMETERS</span></span>

### <span data-ttu-id="5cbe6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cbe6-114">-DefaultProfile</span></span>
<span data-ttu-id="5cbe6-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5cbe6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5cbe6-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5cbe6-116">-InputObject</span></span>
<span data-ttu-id="5cbe6-117">서비스 끝점 정책 정의 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="5cbe6-117">The service endpoint policy definition object.</span></span>

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

### <span data-ttu-id="5cbe6-118">-이름</span><span class="sxs-lookup"><span data-stu-id="5cbe6-118">-Name</span></span>
<span data-ttu-id="5cbe6-119">서비스 끝점 정의의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5cbe6-119">The name of the service endpoint definition</span></span>

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

### <span data-ttu-id="5cbe6-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5cbe6-120">-ResourceId</span></span>
<span data-ttu-id="5cbe6-121">서비스 끝점 정의의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5cbe6-121">The ID of the service endpoint definition.</span></span>

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

### <span data-ttu-id="5cbe6-122">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="5cbe6-122">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="5cbe6-123">ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="5cbe6-123">The ServiceEndpointPolicy</span></span>

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

### <span data-ttu-id="5cbe6-124">-확인</span><span class="sxs-lookup"><span data-stu-id="5cbe6-124">-Confirm</span></span>
<span data-ttu-id="5cbe6-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cbe6-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cbe6-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cbe6-126">-WhatIf</span></span>
<span data-ttu-id="5cbe6-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5cbe6-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5cbe6-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5cbe6-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cbe6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cbe6-129">CommonParameters</span></span>
<span data-ttu-id="5cbe6-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cbe6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cbe6-131">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cbe6-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cbe6-132">입력</span><span class="sxs-lookup"><span data-stu-id="5cbe6-132">INPUTS</span></span>

### <span data-ttu-id="5cbe6-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5cbe6-133">System.String</span></span>

### <span data-ttu-id="5cbe6-134">Microsoft. m a w. PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="5cbe6-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>

### <span data-ttu-id="5cbe6-135">Microsoft. 네트워크. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="5cbe6-135">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="5cbe6-136">출력</span><span class="sxs-lookup"><span data-stu-id="5cbe6-136">OUTPUTS</span></span>

### <span data-ttu-id="5cbe6-137">Microsoft. 네트워크. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="5cbe6-137">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="5cbe6-138">상속자</span><span class="sxs-lookup"><span data-stu-id="5cbe6-138">NOTES</span></span>

## <span data-ttu-id="5cbe6-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5cbe6-139">RELATED LINKS</span></span>

[<span data-ttu-id="5cbe6-140">추가-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="5cbe6-140">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="5cbe6-141">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="5cbe6-141">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="5cbe6-142">새로운 AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="5cbe6-142">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="5cbe6-143">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="5cbe6-143">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
