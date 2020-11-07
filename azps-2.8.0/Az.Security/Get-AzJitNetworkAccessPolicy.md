---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: f25db6e5323646e98b64f972818c422c2a3ff4c0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873210"
---
# <span data-ttu-id="36591-101">Get-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="36591-101">Get-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="36591-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36591-102">SYNOPSIS</span></span>
<span data-ttu-id="36591-103">JIT 네트워크 액세스 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="36591-103">Gets the JIT network access policies</span></span>

## <span data-ttu-id="36591-104">구문과</span><span class="sxs-lookup"><span data-stu-id="36591-104">SYNTAX</span></span>

### <span data-ttu-id="36591-105">구독 범위 (기본값)</span><span class="sxs-lookup"><span data-stu-id="36591-105">SubscriptionScope (Default)</span></span>
```
Get-AzJitNetworkAccessPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36591-106">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="36591-106">ResourceGroupScope</span></span>
```
Get-AzJitNetworkAccessPolicy -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="36591-107">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="36591-107">ResourceGroupLevelResource</span></span>
```
Get-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36591-108">리소스</span><span class="sxs-lookup"><span data-stu-id="36591-108">ResourceId</span></span>
```
Get-AzJitNetworkAccessPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="36591-109">설명은</span><span class="sxs-lookup"><span data-stu-id="36591-109">DESCRIPTION</span></span>
<span data-ttu-id="36591-110">JIT (just-in-time) 네트워크 액세스 정책에서는 간단한 사용자가 VM에 대 한 임시 네트워크 연결을 만들 수 있도록 하는 정책 정의를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="36591-110">Just In Time (JIT) network access policies let you define a policy the will allow simple users to create a temporary network connection to a VM.</span></span>
<span data-ttu-id="36591-111">정책은 연결을 자동으로 닫기 전에 VM에 대 한 연결을 요청할 수 있는 포트, 프로토콜 및 원본 IP 주소와 최대 기간을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="36591-111">The policy defines what ports, protocol and source IP addresses can request a connection to a VM and the max duration before the connection will be closed automatically.</span></span>
<span data-ttu-id="36591-112">또한이 정책에 대 한 연결 요청을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="36591-112">In the policy you can also see the connection request that were made with this policy.</span></span> 

## <span data-ttu-id="36591-113">예제의</span><span class="sxs-lookup"><span data-stu-id="36591-113">EXAMPLES</span></span>

### <span data-ttu-id="36591-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="36591-114">Example 1</span></span>
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

<span data-ttu-id="36591-115">구독에 대 한 모든 JIT 네트워크 액세스 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="36591-115">Get all the JIT network access polices on a subscription</span></span>

### <span data-ttu-id="36591-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="36591-116">Example 2</span></span>
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

<span data-ttu-id="36591-117">"MyService1" 리소스 그룹의 모든 JIT 네트워크 액세스 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="36591-117">Get all the JIT network access polices on the "myService1" resource group</span></span>

### <span data-ttu-id="36591-118">예제 3</span><span class="sxs-lookup"><span data-stu-id="36591-118">Example 3</span></span>
```powershell
PS C:\> Get-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default"
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded
```

<span data-ttu-id="36591-119">특정 JIT 네트워크 액세스 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="36591-119">Gets a specific JIT network access policy</span></span>

## <span data-ttu-id="36591-120">변수</span><span class="sxs-lookup"><span data-stu-id="36591-120">PARAMETERS</span></span>

### <span data-ttu-id="36591-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36591-121">-DefaultProfile</span></span>
<span data-ttu-id="36591-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="36591-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36591-123">-위치</span><span class="sxs-lookup"><span data-stu-id="36591-123">-Location</span></span>
<span data-ttu-id="36591-124">Location.</span><span class="sxs-lookup"><span data-stu-id="36591-124">Location.</span></span>

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

### <span data-ttu-id="36591-125">-이름</span><span class="sxs-lookup"><span data-stu-id="36591-125">-Name</span></span>
<span data-ttu-id="36591-126">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="36591-126">Resource name.</span></span>

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

### <span data-ttu-id="36591-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36591-127">-ResourceGroupName</span></span>
<span data-ttu-id="36591-128">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="36591-128">Resource group name.</span></span>

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

### <span data-ttu-id="36591-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="36591-129">-ResourceId</span></span>
<span data-ttu-id="36591-130">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="36591-130">Resource ID.</span></span>

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

### <span data-ttu-id="36591-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36591-131">CommonParameters</span></span>
<span data-ttu-id="36591-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="36591-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36591-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36591-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36591-134">입력</span><span class="sxs-lookup"><span data-stu-id="36591-134">INPUTS</span></span>

### <span data-ttu-id="36591-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="36591-135">System.String</span></span>

## <span data-ttu-id="36591-136">출력</span><span class="sxs-lookup"><span data-stu-id="36591-136">OUTPUTS</span></span>

### <span data-ttu-id="36591-137">JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy에 대 한 Microsoft</span><span class="sxs-lookup"><span data-stu-id="36591-137">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="36591-138">상속자</span><span class="sxs-lookup"><span data-stu-id="36591-138">NOTES</span></span>

## <span data-ttu-id="36591-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="36591-139">RELATED LINKS</span></span>
