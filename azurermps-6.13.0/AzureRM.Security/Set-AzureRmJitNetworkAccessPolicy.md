---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmJitNetworkAccessPolicy.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmJitNetworkAccessPolicy.md
ms.openlocfilehash: 72e3cf48f112c5e9bb07a8f7eb57dfe3d4c9ee07
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529381"
---
# <span data-ttu-id="3b8a9-101">Set-AzureRmJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3b8a9-101">Set-AzureRmJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="3b8a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b8a9-102">SYNOPSIS</span></span>
<span data-ttu-id="3b8a9-103">JIT 네트워크 액세스 정책을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b8a9-103">Updates JIT network access policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b8a9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3b8a9-104">SYNTAX</span></span>

```
Set-AzureRmJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyVirtualMachine[]> -Kind <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b8a9-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3b8a9-105">DESCRIPTION</span></span>
<span data-ttu-id="3b8a9-106">JIT 네트워크 액세스 정책을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b8a9-106">Updates JIT network access policy.</span></span>

## <span data-ttu-id="3b8a9-107">예제의</span><span class="sxs-lookup"><span data-stu-id="3b8a9-107">EXAMPLES</span></span>

### <span data-ttu-id="3b8a9-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="3b8a9-108">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default" -VirtualMachine $vmRules -Kind "Basic"

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="3b8a9-109">새 VM 규칙을 사용 하 여 JIT 네트워크 액세스 정책을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b8a9-109">Updates a JIT network access policy with new VM rules.</span></span>

## <span data-ttu-id="3b8a9-110">변수</span><span class="sxs-lookup"><span data-stu-id="3b8a9-110">PARAMETERS</span></span>

### <span data-ttu-id="3b8a9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b8a9-111">-DefaultProfile</span></span>
<span data-ttu-id="3b8a9-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3b8a9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b8a9-113">-종류</span><span class="sxs-lookup"><span data-stu-id="3b8a9-113">-Kind</span></span>
<span data-ttu-id="3b8a9-114">형식.</span><span class="sxs-lookup"><span data-stu-id="3b8a9-114">Kind.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b8a9-115">-위치</span><span class="sxs-lookup"><span data-stu-id="3b8a9-115">-Location</span></span>
<span data-ttu-id="3b8a9-116">Location.</span><span class="sxs-lookup"><span data-stu-id="3b8a9-116">Location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b8a9-117">-이름</span><span class="sxs-lookup"><span data-stu-id="3b8a9-117">-Name</span></span>
<span data-ttu-id="3b8a9-118">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3b8a9-118">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b8a9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b8a9-119">-ResourceGroupName</span></span>
<span data-ttu-id="3b8a9-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3b8a9-120">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b8a9-121">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="3b8a9-121">-VirtualMachine</span></span>
<span data-ttu-id="3b8a9-122">Virutal 컴퓨터.</span><span class="sxs-lookup"><span data-stu-id="3b8a9-122">Virutal Machines.</span></span>

```yaml
Type: PSSecurityJitNetworkAccessPolicyVirtualMachine[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b8a9-123">-확인</span><span class="sxs-lookup"><span data-stu-id="3b8a9-123">-Confirm</span></span>
<span data-ttu-id="3b8a9-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b8a9-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b8a9-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b8a9-125">-WhatIf</span></span>
<span data-ttu-id="3b8a9-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3b8a9-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3b8a9-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3b8a9-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b8a9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b8a9-128">CommonParameters</span></span>
<span data-ttu-id="3b8a9-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b8a9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b8a9-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b8a9-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b8a9-131">입력</span><span class="sxs-lookup"><span data-stu-id="3b8a9-131">INPUTS</span></span>

### <span data-ttu-id="3b8a9-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3b8a9-132">System.String</span></span>
<span data-ttu-id="3b8a9-133">Microsoft. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicyVirtualMachine [])</span><span class="sxs-lookup"><span data-stu-id="3b8a9-133">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyVirtualMachine[]</span></span>

## <span data-ttu-id="3b8a9-134">출력</span><span class="sxs-lookup"><span data-stu-id="3b8a9-134">OUTPUTS</span></span>

### <span data-ttu-id="3b8a9-135">JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy에 대 한 Microsoft</span><span class="sxs-lookup"><span data-stu-id="3b8a9-135">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="3b8a9-136">상속자</span><span class="sxs-lookup"><span data-stu-id="3b8a9-136">NOTES</span></span>

## <span data-ttu-id="3b8a9-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3b8a9-137">RELATED LINKS</span></span>
