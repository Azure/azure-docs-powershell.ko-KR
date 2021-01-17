---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Start-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Start-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Start-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: b992f3a41278ba66c54eeefc0b548eef76b50980
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368033"
---
# <span data-ttu-id="98df1-101">Start-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="98df1-101">Start-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="98df1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98df1-102">SYNOPSIS</span></span>
<span data-ttu-id="98df1-103">임시 네트워크 액세스 요청을 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="98df1-103">Invokes a temporary network access request.</span></span>

## <span data-ttu-id="98df1-104">구문</span><span class="sxs-lookup"><span data-stu-id="98df1-104">SYNTAX</span></span>

### <span data-ttu-id="98df1-105">ResourceGroupLevelResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="98df1-105">ResourceGroupLevelResource (Default)</span></span>
```
Start-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98df1-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="98df1-106">ResourceId</span></span>
```
Start-AzJitNetworkAccessPolicy -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98df1-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="98df1-107">InputObject</span></span>
```
Start-AzJitNetworkAccessPolicy -InputObject <PSSecurityJitNetworkAccessPolicyInitiateInputObject>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98df1-108">설명</span><span class="sxs-lookup"><span data-stu-id="98df1-108">DESCRIPTION</span></span>
<span data-ttu-id="98df1-109">임시 네트워크 액세스 요청을 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="98df1-109">Invokes a temporary network access request.</span></span>
<span data-ttu-id="98df1-110">구성된 JIT 네트워크 액세스 정책에 대해 요청의 유효성을 검사하고, 허용되는 경우 사용자의 요청에 따라 네트워크 연결을 개설합니다.</span><span class="sxs-lookup"><span data-stu-id="98df1-110">The request is validated against the configured JIT network access policy and if permitted, opens up a network connection according to the user's request.</span></span>
<span data-ttu-id="98df1-111">요청은 이후 검토를 위해 정책에 기록되고 지정된 기간을 초과하면 종료됩니다.</span><span class="sxs-lookup"><span data-stu-id="98df1-111">The request will be logged in the policy for later review and will be terminated when the specified duration will be exceeded.</span></span>

## <span data-ttu-id="98df1-112">예제</span><span class="sxs-lookup"><span data-stu-id="98df1-112">EXAMPLES</span></span>

### <span data-ttu-id="98df1-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="98df1-113">Example 1</span></span>
```powershell
PS C:\> Set-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default" -Kind "Basic" -VirtualMachine $vms

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.S
                    ecurity/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.
                    Compute/virtualMachines/testService}
Requests          : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="98df1-114">지정된 연결 요청 데이터에 따라 네트워크 연결이 열립니다.</span><span class="sxs-lookup"><span data-stu-id="98df1-114">Opens up a network connection according to the specified connection request data.</span></span>

## <span data-ttu-id="98df1-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="98df1-115">PARAMETERS</span></span>

### <span data-ttu-id="98df1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98df1-116">-DefaultProfile</span></span>
<span data-ttu-id="98df1-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="98df1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98df1-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="98df1-118">-InputObject</span></span>
<span data-ttu-id="98df1-119">입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="98df1-119">Input Object.</span></span>

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

### <span data-ttu-id="98df1-120">-Location</span><span class="sxs-lookup"><span data-stu-id="98df1-120">-Location</span></span>
<span data-ttu-id="98df1-121">위치.</span><span class="sxs-lookup"><span data-stu-id="98df1-121">Location.</span></span>

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

### <span data-ttu-id="98df1-122">-Name</span><span class="sxs-lookup"><span data-stu-id="98df1-122">-Name</span></span>
<span data-ttu-id="98df1-123">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="98df1-123">Resource name.</span></span>

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

### <span data-ttu-id="98df1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98df1-124">-ResourceGroupName</span></span>
<span data-ttu-id="98df1-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="98df1-125">Resource group name.</span></span>

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

### <span data-ttu-id="98df1-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="98df1-126">-ResourceId</span></span>
<span data-ttu-id="98df1-127">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="98df1-127">Resource ID.</span></span>

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

### <span data-ttu-id="98df1-128">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="98df1-128">-VirtualMachine</span></span>
<span data-ttu-id="98df1-129">자동 프로비전.</span><span class="sxs-lookup"><span data-stu-id="98df1-129">Automatic Provisioning.</span></span>

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

### <span data-ttu-id="98df1-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="98df1-130">-Confirm</span></span>
<span data-ttu-id="98df1-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="98df1-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98df1-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98df1-132">-WhatIf</span></span>
<span data-ttu-id="98df1-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="98df1-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="98df1-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="98df1-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98df1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98df1-135">CommonParameters</span></span>
<span data-ttu-id="98df1-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="98df1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98df1-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="98df1-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98df1-138">입력</span><span class="sxs-lookup"><span data-stu-id="98df1-138">INPUTS</span></span>

### <span data-ttu-id="98df1-139">System.String</span><span class="sxs-lookup"><span data-stu-id="98df1-139">System.String</span></span>

### <span data-ttu-id="98df1-140">Microsoft.Azure.Commands.Security.Cmdlets.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyInitiateInputObject</span><span class="sxs-lookup"><span data-stu-id="98df1-140">Microsoft.Azure.Commands.Security.Cmdlets.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyInitiateInputObject</span></span>

## <span data-ttu-id="98df1-141">출력</span><span class="sxs-lookup"><span data-stu-id="98df1-141">OUTPUTS</span></span>

### <span data-ttu-id="98df1-142">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="98df1-142">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="98df1-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="98df1-143">NOTES</span></span>

## <span data-ttu-id="98df1-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="98df1-144">RELATED LINKS</span></span>
