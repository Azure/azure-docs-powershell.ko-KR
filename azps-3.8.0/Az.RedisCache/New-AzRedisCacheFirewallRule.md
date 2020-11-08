---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheFirewallRule.md
ms.openlocfilehash: 50a2df73d6cfa1e9d34f2c5c4b426f601c9d9309
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034795"
---
# <span data-ttu-id="23f5b-101">New-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="23f5b-101">New-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="23f5b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23f5b-102">SYNOPSIS</span></span>
<span data-ttu-id="23f5b-103">Redis Cache에 방화벽 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="23f5b-103">Create a firewall rule on a Redis Cache.</span></span>

## <span data-ttu-id="23f5b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="23f5b-104">SYNTAX</span></span>

### <span data-ttu-id="23f5b-105">NormalParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="23f5b-105">NormalParameterSet (Default)</span></span>
```
New-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String> -StartIP <String>
 -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23f5b-106">RedisCacheAttributesObject</span><span class="sxs-lookup"><span data-stu-id="23f5b-106">RedisCacheAttributesObject</span></span>
```
New-AzRedisCacheFirewallRule -InputObject <RedisCacheAttributes> -RuleName <String> -StartIP <String>
 -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23f5b-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="23f5b-107">ResourceIdParameterSet</span></span>
```
New-AzRedisCacheFirewallRule -ResourceId <String> -RuleName <String> -StartIP <String> -EndIP <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23f5b-108">설명은</span><span class="sxs-lookup"><span data-stu-id="23f5b-108">DESCRIPTION</span></span>
<span data-ttu-id="23f5b-109">Redis Cache에 방화벽 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="23f5b-109">Create a firewall rule on a Redis Cache.</span></span>

## <span data-ttu-id="23f5b-110">예제의</span><span class="sxs-lookup"><span data-stu-id="23f5b-110">EXAMPLES</span></span>

### <span data-ttu-id="23f5b-111">예제 1: 방화벽 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="23f5b-111">Example 1: Create a firewall rule</span></span>
```
PS C:\>New-AzRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone" -StartIP "10.0.0.1" -EndIP "10.0.0.32"

        ResourceGroupName : myGroup
        Name              : mycache
        FirewallRuleId    : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/mycache/firewallRules/ruleone
        RuleName          : ruleone
        Type              : Microsoft.Cache/Redis/firewallRules
        StartIP           : 10.0.0.1
        EndIP             : 10.0.0.32
```

<span data-ttu-id="23f5b-112">이 명령은 mycache 라는 Redis Cache에 ruleone 이라는 방화벽 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="23f5b-112">This command creates firewall rule named ruleone on Redis Cache named mycache.</span></span>

## <span data-ttu-id="23f5b-113">변수</span><span class="sxs-lookup"><span data-stu-id="23f5b-113">PARAMETERS</span></span>

### <span data-ttu-id="23f5b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23f5b-114">-DefaultProfile</span></span>
<span data-ttu-id="23f5b-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="23f5b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23f5b-116">-EndIP</span><span class="sxs-lookup"><span data-stu-id="23f5b-116">-EndIP</span></span>
<span data-ttu-id="23f5b-117">종료 IP 주소</span><span class="sxs-lookup"><span data-stu-id="23f5b-117">Ending IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23f5b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="23f5b-118">-InputObject</span></span>
<span data-ttu-id="23f5b-119">RedisCacheAttributes 유형의 개체</span><span class="sxs-lookup"><span data-stu-id="23f5b-119">object of type RedisCacheAttributes</span></span>

```yaml
Type: Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes
Parameter Sets: RedisCacheAttributesObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23f5b-120">-이름</span><span class="sxs-lookup"><span data-stu-id="23f5b-120">-Name</span></span>
<span data-ttu-id="23f5b-121">Redis cache의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="23f5b-121">Name of redis cache.</span></span>

```yaml
Type: System.String
Parameter Sets: NormalParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23f5b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23f5b-122">-ResourceGroupName</span></span>
<span data-ttu-id="23f5b-123">캐시가 있는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="23f5b-123">Name of resource group in which cache exists.</span></span>

```yaml
Type: System.String
Parameter Sets: NormalParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23f5b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="23f5b-124">-ResourceId</span></span>
<span data-ttu-id="23f5b-125">Redis Cache의 ARM Id입니다.</span><span class="sxs-lookup"><span data-stu-id="23f5b-125">ARM Id of Redis Cache.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23f5b-126">-RuleName</span><span class="sxs-lookup"><span data-stu-id="23f5b-126">-RuleName</span></span>
<span data-ttu-id="23f5b-127">방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="23f5b-127">Name of firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23f5b-128">-StartIP</span><span class="sxs-lookup"><span data-stu-id="23f5b-128">-StartIP</span></span>
<span data-ttu-id="23f5b-129">시작 IP 주소</span><span class="sxs-lookup"><span data-stu-id="23f5b-129">Starting IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23f5b-130">-확인</span><span class="sxs-lookup"><span data-stu-id="23f5b-130">-Confirm</span></span>
<span data-ttu-id="23f5b-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="23f5b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23f5b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23f5b-132">-WhatIf</span></span>
<span data-ttu-id="23f5b-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="23f5b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23f5b-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="23f5b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23f5b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23f5b-135">CommonParameters</span></span>
<span data-ttu-id="23f5b-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="23f5b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23f5b-137">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23f5b-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23f5b-138">입력</span><span class="sxs-lookup"><span data-stu-id="23f5b-138">INPUTS</span></span>

### <span data-ttu-id="23f5b-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="23f5b-139">System.String</span></span>

### <span data-ttu-id="23f5b-140">Microsoft. Azure. 모델을 다시 캐시 합니다. Rediscache특성</span><span class="sxs-lookup"><span data-stu-id="23f5b-140">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span></span>

## <span data-ttu-id="23f5b-141">출력</span><span class="sxs-lookup"><span data-stu-id="23f5b-141">OUTPUTS</span></span>

### <span data-ttu-id="23f5b-142">PSRedisFirewallRule. 모델. m e.</span><span class="sxs-lookup"><span data-stu-id="23f5b-142">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="23f5b-143">상속자</span><span class="sxs-lookup"><span data-stu-id="23f5b-143">NOTES</span></span>

## <span data-ttu-id="23f5b-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="23f5b-144">RELATED LINKS</span></span>

[<span data-ttu-id="23f5b-145">Get-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="23f5b-145">Get-AzRedisCacheFirewallRule</span></span>](./Get-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="23f5b-146">제거-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="23f5b-146">Remove-AzRedisCacheFirewallRule</span></span>](./Remove-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="23f5b-147">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="23f5b-147">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="23f5b-148">새로운 AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="23f5b-148">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="23f5b-149">제거-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="23f5b-149">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="23f5b-150">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="23f5b-150">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)