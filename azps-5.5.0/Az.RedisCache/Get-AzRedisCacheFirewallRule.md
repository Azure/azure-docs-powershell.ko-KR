---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheFirewallRule.md
ms.openlocfilehash: 8e28951f826c5a049f345bb3182bda10e7de82fb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191241"
---
# <span data-ttu-id="32cf8-101">Get-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="32cf8-101">Get-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="32cf8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32cf8-102">SYNOPSIS</span></span>
<span data-ttu-id="32cf8-103">Redis Cache에 설정된 방화벽 규칙을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="32cf8-103">Get firewall rules set on Redis Cache.</span></span>

## <span data-ttu-id="32cf8-104">구문</span><span class="sxs-lookup"><span data-stu-id="32cf8-104">SYNTAX</span></span>

```
Get-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> [-RuleName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32cf8-105">설명</span><span class="sxs-lookup"><span data-stu-id="32cf8-105">DESCRIPTION</span></span>
<span data-ttu-id="32cf8-106">**RuleName** 매개 변수가 제공된 경우 **Get-AzRedisCacheFirewallRule** cmdlet은 Azure Redis Cache에서 지정된 방화벽 규칙에 대한 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="32cf8-106">If **RuleName** parameter if provided, **Get-AzRedisCacheFirewallRule** cmdlet gets detail about the specified firewall rule on Azure Redis Cache.</span></span> <span data-ttu-id="32cf8-107">Name만  지정하면 이 작업은 Redis Cache에서 사용할 수 있는 모든 방화벽 규칙을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="32cf8-107">If only **Name** is specified this operation gets all firewall rules available on that Redis Cache.</span></span>

## <span data-ttu-id="32cf8-108">예제</span><span class="sxs-lookup"><span data-stu-id="32cf8-108">EXAMPLES</span></span>

### <span data-ttu-id="32cf8-109">예제 1: 단일 방화벽 규칙 얻기</span><span class="sxs-lookup"><span data-stu-id="32cf8-109">Example 1: Get a single firewall rule</span></span>
```
PS C:\>Get-AzRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone"

        ResourceGroupName : myGroup
        Name              : mycache
        FirewallRuleId    : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/mycache/firewallRules/ruleone
        RuleName          : ruleone
        Type              : Microsoft.Cache/Redis/firewallRules
        StartIP           : 10.0.0.1
        EndIP             : 10.0.0.32
```

<span data-ttu-id="32cf8-110">이 명령은 mycache라는 Redis Cache에서 ruleone이라는 방화벽 규칙을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="32cf8-110">This command gets firewall rule named ruleone from Redis Cache named mycache.</span></span>

### <span data-ttu-id="32cf8-111">예제 2: 모든 방화벽 규칙 얻기</span><span class="sxs-lookup"><span data-stu-id="32cf8-111">Example 2: Get all firewall rules</span></span>
```
PS C:\>Get-AzRedisCacheFirewallRule -Name "mycache"

        ResourceGroupName : myGroup
        Name              : mycache
        FirewallRuleId    : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/mycache/firewallRules/ruleone
        RuleName          : ruleone
        Type              : Microsoft.Cache/Redis/firewallRules
        StartIP           : 10.0.0.1
        EndIP             : 10.0.0.32

        ResourceGroupName : myGroup
        Name              : mycache
        FirewallRuleId    : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/mycache/firewallRules/ruletwo
        RuleName          : ruletwo
        Type              : Microsoft.Cache/Redis/firewallRules
        StartIP           : 10.0.0.33
        EndIP             : 10.0.0.64
```

<span data-ttu-id="32cf8-112">이 명령은 mycache라는 Redis Cache에서 모든 방화벽 규칙을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="32cf8-112">This command gets all firewall rules from Redis Cache named mycache.</span></span>

## <span data-ttu-id="32cf8-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="32cf8-113">PARAMETERS</span></span>

### <span data-ttu-id="32cf8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32cf8-114">-DefaultProfile</span></span>
<span data-ttu-id="32cf8-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="32cf8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32cf8-116">-Name</span><span class="sxs-lookup"><span data-stu-id="32cf8-116">-Name</span></span>
<span data-ttu-id="32cf8-117">redis Cache의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="32cf8-117">Name of redis cache.</span></span>

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

### <span data-ttu-id="32cf8-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32cf8-118">-ResourceGroupName</span></span>
<span data-ttu-id="32cf8-119">캐시가 있는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="32cf8-119">Name of resource group in which cache exists.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32cf8-120">-RuleName</span><span class="sxs-lookup"><span data-stu-id="32cf8-120">-RuleName</span></span>
<span data-ttu-id="32cf8-121">방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="32cf8-121">Name of firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32cf8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32cf8-122">CommonParameters</span></span>
<span data-ttu-id="32cf8-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="32cf8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32cf8-124">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="32cf8-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32cf8-125">입력</span><span class="sxs-lookup"><span data-stu-id="32cf8-125">INPUTS</span></span>

### <span data-ttu-id="32cf8-126">System.String</span><span class="sxs-lookup"><span data-stu-id="32cf8-126">System.String</span></span>

## <span data-ttu-id="32cf8-127">출력</span><span class="sxs-lookup"><span data-stu-id="32cf8-127">OUTPUTS</span></span>

### <span data-ttu-id="32cf8-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="32cf8-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="32cf8-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="32cf8-129">NOTES</span></span>

## <span data-ttu-id="32cf8-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="32cf8-130">RELATED LINKS</span></span>

[<span data-ttu-id="32cf8-131">New-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="32cf8-131">New-AzRedisCacheFirewallRule</span></span>](./New-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="32cf8-132">Remove-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="32cf8-132">Remove-AzRedisCacheFirewallRule</span></span>](./Remove-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="32cf8-133">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="32cf8-133">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="32cf8-134">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="32cf8-134">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="32cf8-135">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="32cf8-135">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="32cf8-136">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="32cf8-136">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)