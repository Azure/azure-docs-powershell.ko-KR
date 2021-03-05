---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Start-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Start-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Start-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: 674f88a30ea036fc496cd6931b3d856a20a25c0a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986482"
---
# <span data-ttu-id="ca715-101">Start-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ca715-101">Start-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="ca715-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca715-102">SYNOPSIS</span></span>
<span data-ttu-id="ca715-103">임시 네트워크 액세스 요청을 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="ca715-103">Invokes a temporary network access request.</span></span>

## <span data-ttu-id="ca715-104">구문</span><span class="sxs-lookup"><span data-stu-id="ca715-104">SYNTAX</span></span>

### <span data-ttu-id="ca715-105">ResourceGroupLevelResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="ca715-105">ResourceGroupLevelResource (Default)</span></span>
```
Start-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca715-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ca715-106">ResourceId</span></span>
```
Start-AzJitNetworkAccessPolicy -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca715-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="ca715-107">InputObject</span></span>
```
Start-AzJitNetworkAccessPolicy -InputObject <PSSecurityJitNetworkAccessPolicyInitiateInputObject>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca715-108">설명</span><span class="sxs-lookup"><span data-stu-id="ca715-108">DESCRIPTION</span></span>
<span data-ttu-id="ca715-109">임시 네트워크 액세스 요청을 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="ca715-109">Invokes a temporary network access request.</span></span>
<span data-ttu-id="ca715-110">요청은 구성된 JIT 네트워크 액세스 정책에 대해 유효성을 검사하며, 허용되는 경우 사용자의 요청에 따라 네트워크 연결을 오픈합니다.</span><span class="sxs-lookup"><span data-stu-id="ca715-110">The request is validated against the configured JIT network access policy and if permitted, opens up a network connection according to the user's request.</span></span>
<span data-ttu-id="ca715-111">요청은 나중에 검토하기 위해 정책에 기록되고 지정된 기간을 초과하면 종료됩니다.</span><span class="sxs-lookup"><span data-stu-id="ca715-111">The request will be logged in the policy for later review and will be terminated when the specified duration will be exceeded.</span></span>

## <span data-ttu-id="ca715-112">예제</span><span class="sxs-lookup"><span data-stu-id="ca715-112">EXAMPLES</span></span>

### <span data-ttu-id="ca715-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="ca715-113">Example 1</span></span>
```powershell
$MyResource = Get-AzResource -Id /subscriptions/xxxxxxx-xxxxx-xxxxx-xxxxxxx/resourceGroups/PolicyDemo/providers/Microsoft.Compute/virtualMachines/PolicyDemoVM1
$JitPolicy = (@{
        id    = $MyResource.ResourceId; 
        ports = (@{
                number                     = 22
                endTimeUtc                 = Get-Date (Get-Date -AsUTC).AddHours(1) -Format O
                allowedSourceAddressPrefix = @($MyPublicIP) 
            })
    })
$ActivationVM = @($JitPolicy)
Start-AzJitNetworkAccessPolicy -ResourceGroupName $($MyResource.ResourceGroupName) -Location $MyResource.Location -Name "default" -VirtualMachine $ActivationVM

```

<span data-ttu-id="ca715-114">내 공용 IP에서 포트 22를 통해 1시간 동안 네트워크 연결을 갖습니다(표시되지 않습니다).</span><span class="sxs-lookup"><span data-stu-id="ca715-114">Opens up a network connection for 1 hour over port 22 from my public IP (not shown).</span></span>

## <span data-ttu-id="ca715-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ca715-115">PARAMETERS</span></span>

### <span data-ttu-id="ca715-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca715-116">-DefaultProfile</span></span>
<span data-ttu-id="ca715-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ca715-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca715-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ca715-118">-InputObject</span></span>
<span data-ttu-id="ca715-119">입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ca715-119">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Cmdlets.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyInitiateInputObject
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca715-120">-Location</span><span class="sxs-lookup"><span data-stu-id="ca715-120">-Location</span></span>
<span data-ttu-id="ca715-121">위치입니다.</span><span class="sxs-lookup"><span data-stu-id="ca715-121">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca715-122">-Name</span><span class="sxs-lookup"><span data-stu-id="ca715-122">-Name</span></span>
<span data-ttu-id="ca715-123">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ca715-123">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca715-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca715-124">-ResourceGroupName</span></span>
<span data-ttu-id="ca715-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ca715-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca715-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ca715-126">-ResourceId</span></span>
<span data-ttu-id="ca715-127">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ca715-127">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca715-128">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="ca715-128">-VirtualMachine</span></span>
<span data-ttu-id="ca715-129">자동 프로비전.</span><span class="sxs-lookup"><span data-stu-id="ca715-129">Automatic Provisioning.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca715-130">-확인</span><span class="sxs-lookup"><span data-stu-id="ca715-130">-Confirm</span></span>
<span data-ttu-id="ca715-131">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ca715-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca715-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca715-132">-WhatIf</span></span>
<span data-ttu-id="ca715-133">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ca715-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ca715-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ca715-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca715-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca715-135">CommonParameters</span></span>
<span data-ttu-id="ca715-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ca715-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca715-137">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ca715-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca715-138">입력</span><span class="sxs-lookup"><span data-stu-id="ca715-138">INPUTS</span></span>

### <span data-ttu-id="ca715-139">System.String</span><span class="sxs-lookup"><span data-stu-id="ca715-139">System.String</span></span>

### <span data-ttu-id="ca715-140">Microsoft.Azure.Commands.Security.Cmdlets.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyInitiateInputObject</span><span class="sxs-lookup"><span data-stu-id="ca715-140">Microsoft.Azure.Commands.Security.Cmdlets.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyInitiateInputObject</span></span>

## <span data-ttu-id="ca715-141">출력</span><span class="sxs-lookup"><span data-stu-id="ca715-141">OUTPUTS</span></span>

### <span data-ttu-id="ca715-142">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ca715-142">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="ca715-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ca715-143">NOTES</span></span>

## <span data-ttu-id="ca715-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ca715-144">RELATED LINKS</span></span>
