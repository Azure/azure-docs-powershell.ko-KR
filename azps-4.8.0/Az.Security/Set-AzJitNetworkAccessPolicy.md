---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: a316a59492034f0effd2d233ce386cbd6a256c75
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204349"
---
# <span data-ttu-id="6cdd4-101">Set-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6cdd4-101">Set-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="6cdd4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6cdd4-102">SYNOPSIS</span></span>
<span data-ttu-id="6cdd4-103">JIT 네트워크 액세스 정책을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6cdd4-103">Updates JIT network access policy.</span></span>

## <span data-ttu-id="6cdd4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6cdd4-104">SYNTAX</span></span>

```
Set-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyVirtualMachine[]> -Kind <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6cdd4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6cdd4-105">DESCRIPTION</span></span>
<span data-ttu-id="6cdd4-106">JIT 네트워크 액세스 정책을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6cdd4-106">Updates JIT network access policy.</span></span>

## <span data-ttu-id="6cdd4-107">예제의</span><span class="sxs-lookup"><span data-stu-id="6cdd4-107">EXAMPLES</span></span>

### <span data-ttu-id="6cdd4-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="6cdd4-108">Example 1</span></span>
```powershell
PS C:\> Set-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default" -VirtualMachine $vmRules -Kind "Basic"

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="6cdd4-109">새 VM 규칙을 사용 하 여 JIT 네트워크 액세스 정책을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6cdd4-109">Updates a JIT network access policy with new VM rules.</span></span>

## <span data-ttu-id="6cdd4-110">변수</span><span class="sxs-lookup"><span data-stu-id="6cdd4-110">PARAMETERS</span></span>

### <span data-ttu-id="6cdd4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cdd4-111">-DefaultProfile</span></span>
<span data-ttu-id="6cdd4-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6cdd4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6cdd4-113">-종류</span><span class="sxs-lookup"><span data-stu-id="6cdd4-113">-Kind</span></span>
<span data-ttu-id="6cdd4-114">형식.</span><span class="sxs-lookup"><span data-stu-id="6cdd4-114">Kind.</span></span>

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

### <span data-ttu-id="6cdd4-115">-위치</span><span class="sxs-lookup"><span data-stu-id="6cdd4-115">-Location</span></span>
<span data-ttu-id="6cdd4-116">Location.</span><span class="sxs-lookup"><span data-stu-id="6cdd4-116">Location.</span></span>

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

### <span data-ttu-id="6cdd4-117">-이름</span><span class="sxs-lookup"><span data-stu-id="6cdd4-117">-Name</span></span>
<span data-ttu-id="6cdd4-118">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6cdd4-118">Resource name.</span></span>

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

### <span data-ttu-id="6cdd4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cdd4-119">-ResourceGroupName</span></span>
<span data-ttu-id="6cdd4-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6cdd4-120">Resource group name.</span></span>

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

### <span data-ttu-id="6cdd4-121">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="6cdd4-121">-VirtualMachine</span></span>
<span data-ttu-id="6cdd4-122">가상 컴퓨터.</span><span class="sxs-lookup"><span data-stu-id="6cdd4-122">Virtual Machines.</span></span>

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

### <span data-ttu-id="6cdd4-123">-확인</span><span class="sxs-lookup"><span data-stu-id="6cdd4-123">-Confirm</span></span>
<span data-ttu-id="6cdd4-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6cdd4-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6cdd4-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cdd4-125">-WhatIf</span></span>
<span data-ttu-id="6cdd4-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6cdd4-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6cdd4-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6cdd4-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6cdd4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cdd4-128">CommonParameters</span></span>
<span data-ttu-id="6cdd4-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6cdd4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cdd4-130">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6cdd4-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cdd4-131">입력</span><span class="sxs-lookup"><span data-stu-id="6cdd4-131">INPUTS</span></span>

### <span data-ttu-id="6cdd4-132">않아야</span><span class="sxs-lookup"><span data-stu-id="6cdd4-132">None</span></span>

## <span data-ttu-id="6cdd4-133">출력</span><span class="sxs-lookup"><span data-stu-id="6cdd4-133">OUTPUTS</span></span>

### <span data-ttu-id="6cdd4-134">JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy에 대 한 Microsoft</span><span class="sxs-lookup"><span data-stu-id="6cdd4-134">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="6cdd4-135">상속자</span><span class="sxs-lookup"><span data-stu-id="6cdd4-135">NOTES</span></span>

## <span data-ttu-id="6cdd4-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6cdd4-136">RELATED LINKS</span></span>
