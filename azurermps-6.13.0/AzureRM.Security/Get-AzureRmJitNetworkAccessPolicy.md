---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmJitNetworkAccessPolicy.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmJitNetworkAccessPolicy.md
ms.openlocfilehash: bd366b636a29a08bea9124b3c3f4b9b423dc4deb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526052"
---
# <span data-ttu-id="9e008-101">Get-AzureRmJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="9e008-101">Get-AzureRmJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="9e008-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e008-102">SYNOPSIS</span></span>
<span data-ttu-id="9e008-103">JIT 네트워크 액세스 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9e008-103">Gets the JIT network access policies</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e008-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9e008-104">SYNTAX</span></span>

### <span data-ttu-id="9e008-105">구독 범위 (기본값)</span><span class="sxs-lookup"><span data-stu-id="9e008-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmJitNetworkAccessPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e008-106">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="9e008-106">ResourceGroupScope</span></span>
```
Get-AzureRmJitNetworkAccessPolicy -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9e008-107">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="9e008-107">ResourceGroupLevelResource</span></span>
```
Get-AzureRmJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e008-108">리소스</span><span class="sxs-lookup"><span data-stu-id="9e008-108">ResourceId</span></span>
```
Get-AzureRmJitNetworkAccessPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9e008-109">설명은</span><span class="sxs-lookup"><span data-stu-id="9e008-109">DESCRIPTION</span></span>
<span data-ttu-id="9e008-110">JIT (just-in-time) 네트워크 액세스 정책에서는 간단한 사용자가 VM에 대 한 임시 네트워크 연결을 만들 수 있도록 하는 정책 정의를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e008-110">Just In Time (JIT) network access policies let you define a policy the will allow simple users to create a temporary network connection to a VM.</span></span>
<span data-ttu-id="9e008-111">정책은 연결을 자동으로 닫기 전에 VM에 대 한 연결을 요청할 수 있는 포트, 프로토콜 및 원본 IP 주소와 최대 기간을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e008-111">The policy defines what ports, protocol and source IP addresses can request a connection to a VM and the max duration before the connection will be closed automatically.</span></span>
<span data-ttu-id="9e008-112">또한이 정책에 대 한 연결 요청을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9e008-112">In the policy you can also see the connection request that were made with this policy.</span></span> 

## <span data-ttu-id="9e008-113">예제의</span><span class="sxs-lookup"><span data-stu-id="9e008-113">EXAMPLES</span></span>

### <span data-ttu-id="9e008-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="9e008-114">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmJitNetworkAccessPolicy
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

<span data-ttu-id="9e008-115">구독에 대 한 모든 JIT 네트워크 액세스 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="9e008-115">Get all the JIT network access polices on a subscription</span></span>

### <span data-ttu-id="9e008-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="9e008-116">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmJitNetworkAccessPolicy -ResourceGroupName "myService1"
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

<span data-ttu-id="9e008-117">"MyService1" 리소스 그룹의 모든 JIT 네트워크 액세스 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="9e008-117">Get all the JIT network access polices on the "myService1" resource group</span></span>

### <span data-ttu-id="9e008-118">예제 3</span><span class="sxs-lookup"><span data-stu-id="9e008-118">Example 3</span></span>
```powershell
PS C:\> Get-AzureRmJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default"
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded
```

<span data-ttu-id="9e008-119">특정 JIT 네트워크 액세스 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9e008-119">Gets a specific JIT network access policy</span></span>

## <span data-ttu-id="9e008-120">변수</span><span class="sxs-lookup"><span data-stu-id="9e008-120">PARAMETERS</span></span>

### <span data-ttu-id="9e008-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e008-121">-DefaultProfile</span></span>
<span data-ttu-id="9e008-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9e008-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e008-123">-위치</span><span class="sxs-lookup"><span data-stu-id="9e008-123">-Location</span></span>
<span data-ttu-id="9e008-124">Location.</span><span class="sxs-lookup"><span data-stu-id="9e008-124">Location.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e008-125">-이름</span><span class="sxs-lookup"><span data-stu-id="9e008-125">-Name</span></span>
<span data-ttu-id="9e008-126">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9e008-126">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e008-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e008-127">-ResourceGroupName</span></span>
<span data-ttu-id="9e008-128">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9e008-128">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupScope, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e008-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9e008-129">-ResourceId</span></span>
<span data-ttu-id="9e008-130">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="9e008-130">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e008-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e008-131">CommonParameters</span></span>
<span data-ttu-id="9e008-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e008-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e008-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e008-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e008-134">입력</span><span class="sxs-lookup"><span data-stu-id="9e008-134">INPUTS</span></span>

### <span data-ttu-id="9e008-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9e008-135">System.String</span></span>

## <span data-ttu-id="9e008-136">출력</span><span class="sxs-lookup"><span data-stu-id="9e008-136">OUTPUTS</span></span>

### <span data-ttu-id="9e008-137">JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy에 대 한 Microsoft</span><span class="sxs-lookup"><span data-stu-id="9e008-137">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="9e008-138">상속자</span><span class="sxs-lookup"><span data-stu-id="9e008-138">NOTES</span></span>

## <span data-ttu-id="9e008-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9e008-139">RELATED LINKS</span></span>
