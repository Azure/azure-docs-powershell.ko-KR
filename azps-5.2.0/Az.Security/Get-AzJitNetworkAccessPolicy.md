---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: c385ca902764d6bf9afa3808d718c2ceb5d1357c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330561"
---
# <span data-ttu-id="f4ec7-101">Get-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f4ec7-101">Get-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="f4ec7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4ec7-102">SYNOPSIS</span></span>
<span data-ttu-id="f4ec7-103">JIT 네트워크 액세스 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f4ec7-103">Gets the JIT network access policies</span></span>

## <span data-ttu-id="f4ec7-104">구문</span><span class="sxs-lookup"><span data-stu-id="f4ec7-104">SYNTAX</span></span>

### <span data-ttu-id="f4ec7-105">SubscriptionScope(기본값)</span><span class="sxs-lookup"><span data-stu-id="f4ec7-105">SubscriptionScope (Default)</span></span>
```
Get-AzJitNetworkAccessPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4ec7-106">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="f4ec7-106">ResourceGroupScope</span></span>
```
Get-AzJitNetworkAccessPolicy -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f4ec7-107">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="f4ec7-107">ResourceGroupLevelResource</span></span>
```
Get-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4ec7-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4ec7-108">ResourceId</span></span>
```
Get-AzJitNetworkAccessPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f4ec7-109">설명</span><span class="sxs-lookup"><span data-stu-id="f4ec7-109">DESCRIPTION</span></span>
<span data-ttu-id="f4ec7-110">JIT(Just-In-Time) 네트워크 액세스 정책을 사용하면 간단한 사용자가 VM에 임시 네트워크 연결을 만들 수 있도록 정책을 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f4ec7-110">Just In Time (JIT) network access policies let you define a policy the will allow simple users to create a temporary network connection to a VM.</span></span>
<span data-ttu-id="f4ec7-111">정책은 VM에 대한 연결을 요청할 수 있는 포트, 프로토콜 및 원본 IP 주소와 연결이 자동으로 닫히기 전의 최대 기간을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="f4ec7-111">The policy defines what ports, protocol and source IP addresses can request a connection to a VM and the max duration before the connection will be closed automatically.</span></span>
<span data-ttu-id="f4ec7-112">정책에서 이 정책을 사용하여 만든 연결 요청을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f4ec7-112">In the policy you can also see the connection request that were made with this policy.</span></span> 

## <span data-ttu-id="f4ec7-113">예제</span><span class="sxs-lookup"><span data-stu-id="f4ec7-113">EXAMPLES</span></span>

### <span data-ttu-id="f4ec7-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="f4ec7-114">Example 1</span></span>
```powershell
PS C:\> Get-AzJitNetworkAccessPolicy
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/northeurope/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded
```

<span data-ttu-id="f4ec7-115">구독에서 모든 JIT 네트워크 액세스 권한을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f4ec7-115">Get all the JIT network access polices on a subscription</span></span>

### <span data-ttu-id="f4ec7-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="f4ec7-116">Example 2</span></span>
```powershell
PS C:\> Get-AzJitNetworkAccessPolicy -ResourceGroupName "myService1"
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/northeurope/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded
```

<span data-ttu-id="f4ec7-117">"myService1" 리소스 그룹의 모든 JIT 네트워크 액세스 권한을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f4ec7-117">Get all the JIT network access polices on the "myService1" resource group</span></span>

### <span data-ttu-id="f4ec7-118">예제 3</span><span class="sxs-lookup"><span data-stu-id="f4ec7-118">Example 3</span></span>
```powershell
PS C:\> Get-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default"
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded
```

<span data-ttu-id="f4ec7-119">특정 JIT 네트워크 액세스 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f4ec7-119">Gets a specific JIT network access policy</span></span>

## <span data-ttu-id="f4ec7-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f4ec7-120">PARAMETERS</span></span>

### <span data-ttu-id="f4ec7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4ec7-121">-DefaultProfile</span></span>
<span data-ttu-id="f4ec7-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f4ec7-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4ec7-123">-Location</span><span class="sxs-lookup"><span data-stu-id="f4ec7-123">-Location</span></span>
<span data-ttu-id="f4ec7-124">위치.</span><span class="sxs-lookup"><span data-stu-id="f4ec7-124">Location.</span></span>

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

### <span data-ttu-id="f4ec7-125">-Name</span><span class="sxs-lookup"><span data-stu-id="f4ec7-125">-Name</span></span>
<span data-ttu-id="f4ec7-126">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f4ec7-126">Resource name.</span></span>

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

### <span data-ttu-id="f4ec7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4ec7-127">-ResourceGroupName</span></span>
<span data-ttu-id="f4ec7-128">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f4ec7-128">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupScope, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4ec7-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4ec7-129">-ResourceId</span></span>
<span data-ttu-id="f4ec7-130">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f4ec7-130">Resource ID.</span></span>

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

### <span data-ttu-id="f4ec7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4ec7-131">CommonParameters</span></span>
<span data-ttu-id="f4ec7-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f4ec7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4ec7-133">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f4ec7-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4ec7-134">입력</span><span class="sxs-lookup"><span data-stu-id="f4ec7-134">INPUTS</span></span>

### <span data-ttu-id="f4ec7-135">System.String</span><span class="sxs-lookup"><span data-stu-id="f4ec7-135">System.String</span></span>

## <span data-ttu-id="f4ec7-136">출력</span><span class="sxs-lookup"><span data-stu-id="f4ec7-136">OUTPUTS</span></span>

### <span data-ttu-id="f4ec7-137">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f4ec7-137">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="f4ec7-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f4ec7-138">NOTES</span></span>

## <span data-ttu-id="f4ec7-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f4ec7-139">RELATED LINKS</span></span>
