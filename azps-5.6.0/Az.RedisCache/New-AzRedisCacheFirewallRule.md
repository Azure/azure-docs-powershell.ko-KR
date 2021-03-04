---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/powershell/module/az.rediscache/new-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheFirewallRule.md
ms.openlocfilehash: bd0d6995cae0d32a7fb0ce46d42f87a480c275f8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956672"
---
# <span data-ttu-id="d9eb6-101">New-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d9eb6-101">New-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="d9eb6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9eb6-102">SYNOPSIS</span></span>
<span data-ttu-id="d9eb6-103">Redis Cache에서 방화벽 규칙을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d9eb6-103">Create a firewall rule on a Redis Cache.</span></span>

## <span data-ttu-id="d9eb6-104">구문</span><span class="sxs-lookup"><span data-stu-id="d9eb6-104">SYNTAX</span></span>

### <span data-ttu-id="d9eb6-105">NormalParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="d9eb6-105">NormalParameterSet (Default)</span></span>
```
New-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String> -StartIP <String>
 -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9eb6-106">RedisCacheAttributesObject</span><span class="sxs-lookup"><span data-stu-id="d9eb6-106">RedisCacheAttributesObject</span></span>
```
New-AzRedisCacheFirewallRule -InputObject <RedisCacheAttributes> -RuleName <String> -StartIP <String>
 -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9eb6-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9eb6-107">ResourceIdParameterSet</span></span>
```
New-AzRedisCacheFirewallRule -ResourceId <String> -RuleName <String> -StartIP <String> -EndIP <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9eb6-108">설명</span><span class="sxs-lookup"><span data-stu-id="d9eb6-108">DESCRIPTION</span></span>
<span data-ttu-id="d9eb6-109">Redis Cache에서 방화벽 규칙을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d9eb6-109">Create a firewall rule on a Redis Cache.</span></span>

## <span data-ttu-id="d9eb6-110">예제</span><span class="sxs-lookup"><span data-stu-id="d9eb6-110">EXAMPLES</span></span>

### <span data-ttu-id="d9eb6-111">예제 1: 방화벽 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="d9eb6-111">Example 1: Create a firewall rule</span></span>
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

<span data-ttu-id="d9eb6-112">이 명령은 mycache라는 Redis Cache에서 ruleone이라는 방화벽 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d9eb6-112">This command creates firewall rule named ruleone on Redis Cache named mycache.</span></span>

## <span data-ttu-id="d9eb6-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d9eb6-113">PARAMETERS</span></span>

### <span data-ttu-id="d9eb6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9eb6-114">-DefaultProfile</span></span>
<span data-ttu-id="d9eb6-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d9eb6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9eb6-116">-EndIP</span><span class="sxs-lookup"><span data-stu-id="d9eb6-116">-EndIP</span></span>
<span data-ttu-id="d9eb6-117">종료 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="d9eb6-117">Ending IP address.</span></span>

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

### <span data-ttu-id="d9eb6-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9eb6-118">-InputObject</span></span>
<span data-ttu-id="d9eb6-119">RedisCacheAttributes 형식의 개체</span><span class="sxs-lookup"><span data-stu-id="d9eb6-119">object of type RedisCacheAttributes</span></span>

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

### <span data-ttu-id="d9eb6-120">-Name</span><span class="sxs-lookup"><span data-stu-id="d9eb6-120">-Name</span></span>
<span data-ttu-id="d9eb6-121">redis 캐시의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d9eb6-121">Name of redis cache.</span></span>

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

### <span data-ttu-id="d9eb6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9eb6-122">-ResourceGroupName</span></span>
<span data-ttu-id="d9eb6-123">캐시가 있는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d9eb6-123">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="d9eb6-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d9eb6-124">-ResourceId</span></span>
<span data-ttu-id="d9eb6-125">ARM Id의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="d9eb6-125">ARM Id of Redis Cache.</span></span>

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

### <span data-ttu-id="d9eb6-126">-RuleName</span><span class="sxs-lookup"><span data-stu-id="d9eb6-126">-RuleName</span></span>
<span data-ttu-id="d9eb6-127">방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d9eb6-127">Name of firewall rule.</span></span>

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

### <span data-ttu-id="d9eb6-128">-StartIP</span><span class="sxs-lookup"><span data-stu-id="d9eb6-128">-StartIP</span></span>
<span data-ttu-id="d9eb6-129">IP 주소를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="d9eb6-129">Starting IP address.</span></span>

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

### <span data-ttu-id="d9eb6-130">-확인</span><span class="sxs-lookup"><span data-stu-id="d9eb6-130">-Confirm</span></span>
<span data-ttu-id="d9eb6-131">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d9eb6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9eb6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9eb6-132">-WhatIf</span></span>
<span data-ttu-id="d9eb6-133">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="d9eb6-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9eb6-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d9eb6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9eb6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9eb6-135">CommonParameters</span></span>
<span data-ttu-id="d9eb6-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d9eb6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9eb6-137">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d9eb6-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9eb6-138">입력</span><span class="sxs-lookup"><span data-stu-id="d9eb6-138">INPUTS</span></span>

### <span data-ttu-id="d9eb6-139">System.String</span><span class="sxs-lookup"><span data-stu-id="d9eb6-139">System.String</span></span>

### <span data-ttu-id="d9eb6-140">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="d9eb6-140">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span></span>

## <span data-ttu-id="d9eb6-141">출력</span><span class="sxs-lookup"><span data-stu-id="d9eb6-141">OUTPUTS</span></span>

### <span data-ttu-id="d9eb6-142">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d9eb6-142">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="d9eb6-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d9eb6-143">NOTES</span></span>

## <span data-ttu-id="d9eb6-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d9eb6-144">RELATED LINKS</span></span>

[<span data-ttu-id="d9eb6-145">Get-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d9eb6-145">Get-AzRedisCacheFirewallRule</span></span>](./Get-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="d9eb6-146">Remove-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d9eb6-146">Remove-AzRedisCacheFirewallRule</span></span>](./Remove-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="d9eb6-147">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="d9eb6-147">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="d9eb6-148">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="d9eb6-148">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="d9eb6-149">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="d9eb6-149">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="d9eb6-150">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="d9eb6-150">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)