---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Start-AzureRmJitNetworkAccessPolicy.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Start-AzureRmJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Start-AzureRmJitNetworkAccessPolicy.md
ms.openlocfilehash: 62dccdc3b55caa5d63036ed3298caa5a01514342
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533300"
---
# <span data-ttu-id="d770a-101">Start-AzureRmJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d770a-101">Start-AzureRmJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="d770a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d770a-102">SYNOPSIS</span></span>
<span data-ttu-id="d770a-103">임시 네트워크 액세스 요청을 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="d770a-103">Invokes a temporary network access request.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d770a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d770a-104">SYNTAX</span></span>

### <span data-ttu-id="d770a-105">ResourceGroupLevelResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="d770a-105">ResourceGroupLevelResource (Default)</span></span>
```
Start-AzureRmJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d770a-106">리소스</span><span class="sxs-lookup"><span data-stu-id="d770a-106">ResourceId</span></span>
```
Start-AzureRmJitNetworkAccessPolicy -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d770a-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="d770a-107">InputObject</span></span>
```
Start-AzureRmJitNetworkAccessPolicy -InputObject <PSSecurityJitNetworkAccessPolicyInitiateInputObject>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d770a-108">설명은</span><span class="sxs-lookup"><span data-stu-id="d770a-108">DESCRIPTION</span></span>
<span data-ttu-id="d770a-109">임시 네트워크 액세스 요청을 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="d770a-109">Invokes a temporary network access request.</span></span>
<span data-ttu-id="d770a-110">구성 된 JIT 네트워크 액세스 정책에 대해 요청 유효성을 검사 하 고 permittet 인 경우 사용자의 요청에 따라 네트워크 연결을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="d770a-110">The request is validated against the configured JIT network access policy and if permittet, opens up a network connection according to the user's request.</span></span>
<span data-ttu-id="d770a-111">요청은 나중에 검토를 위해 정책에서 로그에 승인 되며 지정 된 기간을 초과할 경우 종료 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d770a-111">The request will be loged in the policy for later review and will be terminated when the specified duration will be exceeded.</span></span>

## <span data-ttu-id="d770a-112">예제의</span><span class="sxs-lookup"><span data-stu-id="d770a-112">EXAMPLES</span></span>

### <span data-ttu-id="d770a-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="d770a-113">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default" -Kind "Basic" -VirtualMachine $vms

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.S
                    ecurity/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.
                    Compute/virtualMachines/testService}
Requests          : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="d770a-114">지정 된 연결 요청 데이터에 따라 네트워크 연결을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="d770a-114">Opens up a network connection according to the specified connection request data.</span></span>

## <span data-ttu-id="d770a-115">변수</span><span class="sxs-lookup"><span data-stu-id="d770a-115">PARAMETERS</span></span>

### <span data-ttu-id="d770a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d770a-116">-DefaultProfile</span></span>
<span data-ttu-id="d770a-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d770a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d770a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d770a-118">-InputObject</span></span>
<span data-ttu-id="d770a-119">입력 개체</span><span class="sxs-lookup"><span data-stu-id="d770a-119">Input Object.</span></span>

```yaml
Type: PSSecurityJitNetworkAccessPolicyInitiateInputObject
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d770a-120">-위치</span><span class="sxs-lookup"><span data-stu-id="d770a-120">-Location</span></span>
<span data-ttu-id="d770a-121">Location.</span><span class="sxs-lookup"><span data-stu-id="d770a-121">Location.</span></span>

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

### <span data-ttu-id="d770a-122">-이름</span><span class="sxs-lookup"><span data-stu-id="d770a-122">-Name</span></span>
<span data-ttu-id="d770a-123">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d770a-123">Resource name.</span></span>

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

### <span data-ttu-id="d770a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d770a-124">-ResourceGroupName</span></span>
<span data-ttu-id="d770a-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d770a-125">Resource group name.</span></span>

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

### <span data-ttu-id="d770a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d770a-126">-ResourceId</span></span>
<span data-ttu-id="d770a-127">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d770a-127">Resource ID.</span></span>

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

### <span data-ttu-id="d770a-128">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="d770a-128">-VirtualMachine</span></span>
<span data-ttu-id="d770a-129">자동 프로비저닝.</span><span class="sxs-lookup"><span data-stu-id="d770a-129">Automatic Provisioning.</span></span>

```yaml
Type: PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d770a-130">-확인</span><span class="sxs-lookup"><span data-stu-id="d770a-130">-Confirm</span></span>
<span data-ttu-id="d770a-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d770a-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d770a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d770a-132">-WhatIf</span></span>
<span data-ttu-id="d770a-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d770a-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d770a-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d770a-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d770a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d770a-135">CommonParameters</span></span>
<span data-ttu-id="d770a-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d770a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d770a-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d770a-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d770a-138">입력</span><span class="sxs-lookup"><span data-stu-id="d770a-138">INPUTS</span></span>

### <span data-ttu-id="d770a-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d770a-139">System.String</span></span>
<span data-ttu-id="d770a-140">Microsoft. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine [])</span><span class="sxs-lookup"><span data-stu-id="d770a-140">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]</span></span>

## <span data-ttu-id="d770a-141">출력</span><span class="sxs-lookup"><span data-stu-id="d770a-141">OUTPUTS</span></span>

### <span data-ttu-id="d770a-142">JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy에 대 한 Microsoft</span><span class="sxs-lookup"><span data-stu-id="d770a-142">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="d770a-143">상속자</span><span class="sxs-lookup"><span data-stu-id="d770a-143">NOTES</span></span>

## <span data-ttu-id="d770a-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d770a-144">RELATED LINKS</span></span>
