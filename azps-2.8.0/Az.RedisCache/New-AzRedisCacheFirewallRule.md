---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheFirewallRule.md
ms.openlocfilehash: dc52668a7d0f17d9cdbf9221a174228be1fa0f5f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873459"
---
# <span data-ttu-id="99c79-101">New-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="99c79-101">New-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="99c79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99c79-102">SYNOPSIS</span></span>
<span data-ttu-id="99c79-103">Redis Cache에 방화벽 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="99c79-103">Create a firewall rule on a Redis Cache.</span></span>

## <span data-ttu-id="99c79-104">구문과</span><span class="sxs-lookup"><span data-stu-id="99c79-104">SYNTAX</span></span>

### <span data-ttu-id="99c79-105">NormalParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="99c79-105">NormalParameterSet (Default)</span></span>
```
New-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String> -StartIP <String>
 -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99c79-106">RedisCacheAttributesObject</span><span class="sxs-lookup"><span data-stu-id="99c79-106">RedisCacheAttributesObject</span></span>
```
New-AzRedisCacheFirewallRule -InputObject <RedisCacheAttributes> -RuleName <String> -StartIP <String>
 -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99c79-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="99c79-107">ResourceIdParameterSet</span></span>
```
New-AzRedisCacheFirewallRule -ResourceId <String> -RuleName <String> -StartIP <String> -EndIP <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99c79-108">설명은</span><span class="sxs-lookup"><span data-stu-id="99c79-108">DESCRIPTION</span></span>
<span data-ttu-id="99c79-109">Redis Cache에 방화벽 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="99c79-109">Create a firewall rule on a Redis Cache.</span></span>

## <span data-ttu-id="99c79-110">예제의</span><span class="sxs-lookup"><span data-stu-id="99c79-110">EXAMPLES</span></span>

### <span data-ttu-id="99c79-111">예제 1: 방화벽 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="99c79-111">Example 1: Create a firewall rule</span></span>
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

<span data-ttu-id="99c79-112">이 명령은 mycache 라는 Redis Cache에 ruleone 이라는 방화벽 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="99c79-112">This command creates firewall rule named ruleone on Redis Cache named mycache.</span></span>

## <span data-ttu-id="99c79-113">변수</span><span class="sxs-lookup"><span data-stu-id="99c79-113">PARAMETERS</span></span>

### <span data-ttu-id="99c79-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99c79-114">-DefaultProfile</span></span>
<span data-ttu-id="99c79-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="99c79-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99c79-116">-EndIP</span><span class="sxs-lookup"><span data-stu-id="99c79-116">-EndIP</span></span>
<span data-ttu-id="99c79-117">종료 IP 주소</span><span class="sxs-lookup"><span data-stu-id="99c79-117">Ending IP address.</span></span>

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

### <span data-ttu-id="99c79-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="99c79-118">-InputObject</span></span>
<span data-ttu-id="99c79-119">RedisCacheAttributes 유형의 개체</span><span class="sxs-lookup"><span data-stu-id="99c79-119">object of type RedisCacheAttributes</span></span>

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

### <span data-ttu-id="99c79-120">-이름</span><span class="sxs-lookup"><span data-stu-id="99c79-120">-Name</span></span>
<span data-ttu-id="99c79-121">Redis cache의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="99c79-121">Name of redis cache.</span></span>

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

### <span data-ttu-id="99c79-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99c79-122">-ResourceGroupName</span></span>
<span data-ttu-id="99c79-123">캐시가 있는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="99c79-123">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="99c79-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="99c79-124">-ResourceId</span></span>
<span data-ttu-id="99c79-125">Redis Cache의 ARM Id입니다.</span><span class="sxs-lookup"><span data-stu-id="99c79-125">ARM Id of Redis Cache.</span></span>

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

### <span data-ttu-id="99c79-126">-RuleName</span><span class="sxs-lookup"><span data-stu-id="99c79-126">-RuleName</span></span>
<span data-ttu-id="99c79-127">방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="99c79-127">Name of firewall rule.</span></span>

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

### <span data-ttu-id="99c79-128">-StartIP</span><span class="sxs-lookup"><span data-stu-id="99c79-128">-StartIP</span></span>
<span data-ttu-id="99c79-129">시작 IP 주소</span><span class="sxs-lookup"><span data-stu-id="99c79-129">Starting IP address.</span></span>

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

### <span data-ttu-id="99c79-130">-확인</span><span class="sxs-lookup"><span data-stu-id="99c79-130">-Confirm</span></span>
<span data-ttu-id="99c79-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="99c79-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99c79-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99c79-132">-WhatIf</span></span>
<span data-ttu-id="99c79-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="99c79-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99c79-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="99c79-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99c79-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99c79-135">CommonParameters</span></span>
<span data-ttu-id="99c79-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="99c79-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99c79-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99c79-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99c79-138">입력</span><span class="sxs-lookup"><span data-stu-id="99c79-138">INPUTS</span></span>

### <span data-ttu-id="99c79-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="99c79-139">System.String</span></span>

### <span data-ttu-id="99c79-140">Microsoft. Azure. 모델을 다시 캐시 합니다. Rediscache특성</span><span class="sxs-lookup"><span data-stu-id="99c79-140">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span></span>

## <span data-ttu-id="99c79-141">출력</span><span class="sxs-lookup"><span data-stu-id="99c79-141">OUTPUTS</span></span>

### <span data-ttu-id="99c79-142">PSRedisFirewallRule. 모델. m e.</span><span class="sxs-lookup"><span data-stu-id="99c79-142">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="99c79-143">상속자</span><span class="sxs-lookup"><span data-stu-id="99c79-143">NOTES</span></span>

## <span data-ttu-id="99c79-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="99c79-144">RELATED LINKS</span></span>

[<span data-ttu-id="99c79-145">Get-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="99c79-145">Get-AzRedisCacheFirewallRule</span></span>](./Get-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="99c79-146">제거-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="99c79-146">Remove-AzRedisCacheFirewallRule</span></span>](./Remove-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="99c79-147">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="99c79-147">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="99c79-148">새로운 AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="99c79-148">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="99c79-149">제거-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="99c79-149">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="99c79-150">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="99c79-150">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)