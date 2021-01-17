---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: a316a59492034f0effd2d233ce386cbd6a256c75
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335438"
---
# <span data-ttu-id="f2c47-101">Set-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f2c47-101">Set-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="f2c47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2c47-102">SYNOPSIS</span></span>
<span data-ttu-id="f2c47-103">JIT 네트워크 액세스 정책을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="f2c47-103">Updates JIT network access policy.</span></span>

## <span data-ttu-id="f2c47-104">구문</span><span class="sxs-lookup"><span data-stu-id="f2c47-104">SYNTAX</span></span>

```
Set-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyVirtualMachine[]> -Kind <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2c47-105">설명</span><span class="sxs-lookup"><span data-stu-id="f2c47-105">DESCRIPTION</span></span>
<span data-ttu-id="f2c47-106">JIT 네트워크 액세스 정책을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="f2c47-106">Updates JIT network access policy.</span></span>

## <span data-ttu-id="f2c47-107">예제</span><span class="sxs-lookup"><span data-stu-id="f2c47-107">EXAMPLES</span></span>

### <span data-ttu-id="f2c47-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="f2c47-108">Example 1</span></span>
```powershell
PS C:\> Set-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default" -VirtualMachine $vmRules -Kind "Basic"

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="f2c47-109">새 VM 규칙을 사용하여 JIT 네트워크 액세스 정책을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="f2c47-109">Updates a JIT network access policy with new VM rules.</span></span>

## <span data-ttu-id="f2c47-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f2c47-110">PARAMETERS</span></span>

### <span data-ttu-id="f2c47-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2c47-111">-DefaultProfile</span></span>
<span data-ttu-id="f2c47-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f2c47-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2c47-113">-Kind</span><span class="sxs-lookup"><span data-stu-id="f2c47-113">-Kind</span></span>
<span data-ttu-id="f2c47-114">종류.</span><span class="sxs-lookup"><span data-stu-id="f2c47-114">Kind.</span></span>

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

### <span data-ttu-id="f2c47-115">-Location</span><span class="sxs-lookup"><span data-stu-id="f2c47-115">-Location</span></span>
<span data-ttu-id="f2c47-116">위치.</span><span class="sxs-lookup"><span data-stu-id="f2c47-116">Location.</span></span>

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

### <span data-ttu-id="f2c47-117">-Name</span><span class="sxs-lookup"><span data-stu-id="f2c47-117">-Name</span></span>
<span data-ttu-id="f2c47-118">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f2c47-118">Resource name.</span></span>

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

### <span data-ttu-id="f2c47-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2c47-119">-ResourceGroupName</span></span>
<span data-ttu-id="f2c47-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f2c47-120">Resource group name.</span></span>

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

### <span data-ttu-id="f2c47-121">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="f2c47-121">-VirtualMachine</span></span>
<span data-ttu-id="f2c47-122">Virtual Machines.</span><span class="sxs-lookup"><span data-stu-id="f2c47-122">Virtual Machines.</span></span>

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

### <span data-ttu-id="f2c47-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f2c47-123">-Confirm</span></span>
<span data-ttu-id="f2c47-124">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2c47-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2c47-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2c47-125">-WhatIf</span></span>
<span data-ttu-id="f2c47-126">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f2c47-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f2c47-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f2c47-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2c47-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2c47-128">CommonParameters</span></span>
<span data-ttu-id="f2c47-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f2c47-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2c47-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f2c47-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2c47-131">입력</span><span class="sxs-lookup"><span data-stu-id="f2c47-131">INPUTS</span></span>

### <span data-ttu-id="f2c47-132">없음</span><span class="sxs-lookup"><span data-stu-id="f2c47-132">None</span></span>

## <span data-ttu-id="f2c47-133">출력</span><span class="sxs-lookup"><span data-stu-id="f2c47-133">OUTPUTS</span></span>

### <span data-ttu-id="f2c47-134">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f2c47-134">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="f2c47-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f2c47-135">NOTES</span></span>

## <span data-ttu-id="f2c47-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f2c47-136">RELATED LINKS</span></span>
