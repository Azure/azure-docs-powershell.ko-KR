---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: a40fba16bd7d361544ca10867d2c575965447c12
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94041582"
---
# <span data-ttu-id="fb892-101">Set-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="fb892-101">Set-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="fb892-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb892-102">SYNOPSIS</span></span>
<span data-ttu-id="fb892-103">JIT 네트워크 액세스 정책을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb892-103">Updates JIT network access policy.</span></span>

## <span data-ttu-id="fb892-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fb892-104">SYNTAX</span></span>

```
Set-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyVirtualMachine[]> -Kind <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb892-105">설명은</span><span class="sxs-lookup"><span data-stu-id="fb892-105">DESCRIPTION</span></span>
<span data-ttu-id="fb892-106">JIT 네트워크 액세스 정책을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb892-106">Updates JIT network access policy.</span></span>

## <span data-ttu-id="fb892-107">예제의</span><span class="sxs-lookup"><span data-stu-id="fb892-107">EXAMPLES</span></span>

### <span data-ttu-id="fb892-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="fb892-108">Example 1</span></span>
```powershell
PS C:\> Set-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default" -VirtualMachine $vmRules -Kind "Basic"

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="fb892-109">새 VM 규칙을 사용 하 여 JIT 네트워크 액세스 정책을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb892-109">Updates a JIT network access policy with new VM rules.</span></span>

## <span data-ttu-id="fb892-110">변수</span><span class="sxs-lookup"><span data-stu-id="fb892-110">PARAMETERS</span></span>

### <span data-ttu-id="fb892-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb892-111">-DefaultProfile</span></span>
<span data-ttu-id="fb892-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fb892-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb892-113">-종류</span><span class="sxs-lookup"><span data-stu-id="fb892-113">-Kind</span></span>
<span data-ttu-id="fb892-114">형식.</span><span class="sxs-lookup"><span data-stu-id="fb892-114">Kind.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb892-115">-위치</span><span class="sxs-lookup"><span data-stu-id="fb892-115">-Location</span></span>
<span data-ttu-id="fb892-116">Location.</span><span class="sxs-lookup"><span data-stu-id="fb892-116">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb892-117">-이름</span><span class="sxs-lookup"><span data-stu-id="fb892-117">-Name</span></span>
<span data-ttu-id="fb892-118">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fb892-118">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb892-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb892-119">-ResourceGroupName</span></span>
<span data-ttu-id="fb892-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fb892-120">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb892-121">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="fb892-121">-VirtualMachine</span></span>
<span data-ttu-id="fb892-122">가상 컴퓨터.</span><span class="sxs-lookup"><span data-stu-id="fb892-122">Virtual Machines.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyVirtualMachine[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb892-123">-확인</span><span class="sxs-lookup"><span data-stu-id="fb892-123">-Confirm</span></span>
<span data-ttu-id="fb892-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb892-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb892-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb892-125">-WhatIf</span></span>
<span data-ttu-id="fb892-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fb892-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fb892-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fb892-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb892-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb892-128">CommonParameters</span></span>
<span data-ttu-id="fb892-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb892-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb892-130">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb892-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb892-131">입력</span><span class="sxs-lookup"><span data-stu-id="fb892-131">INPUTS</span></span>

### <span data-ttu-id="fb892-132">않아야</span><span class="sxs-lookup"><span data-stu-id="fb892-132">None</span></span>

## <span data-ttu-id="fb892-133">출력</span><span class="sxs-lookup"><span data-stu-id="fb892-133">OUTPUTS</span></span>

### <span data-ttu-id="fb892-134">JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy에 대 한 Microsoft</span><span class="sxs-lookup"><span data-stu-id="fb892-134">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="fb892-135">상속자</span><span class="sxs-lookup"><span data-stu-id="fb892-135">NOTES</span></span>

## <span data-ttu-id="fb892-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fb892-136">RELATED LINKS</span></span>
