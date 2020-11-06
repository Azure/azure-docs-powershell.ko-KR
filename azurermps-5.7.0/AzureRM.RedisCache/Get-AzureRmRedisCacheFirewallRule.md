---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/get-azurermrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheFirewallRule.md
ms.openlocfilehash: 231787f57061ff4e118510c3dc166915b39da436
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529756"
---
# <span data-ttu-id="854ce-101">Get-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="854ce-101">Get-AzureRmRedisCacheFirewallRule</span></span>

## <span data-ttu-id="854ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="854ce-102">SYNOPSIS</span></span>
<span data-ttu-id="854ce-103">Redis Cache에 설정 되는 방화벽 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="854ce-103">Get firewall rules set on Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="854ce-104">구문과</span><span class="sxs-lookup"><span data-stu-id="854ce-104">SYNTAX</span></span>

```
Get-AzureRmRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> [-RuleName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="854ce-105">설명은</span><span class="sxs-lookup"><span data-stu-id="854ce-105">DESCRIPTION</span></span>
<span data-ttu-id="854ce-106">**RuleName** 매개 변수를 제공 하는 경우 **AzureRmRedisCacheFirewallRule** Cmdlet은 Azure Redis Cache에서 지정 된 방화벽 규칙에 대 한 자세한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="854ce-106">If **RuleName** parameter if provided, **Get-AzureRmRedisCacheFirewallRule** cmdlet gets detail about the specified firewall rule on Azure Redis Cache.</span></span> <span data-ttu-id="854ce-107">**이름만** 지정 된 경우이 작업은 해당 Redis 캐시에서 사용할 수 있는 모든 방화벽 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="854ce-107">If only **Name** is specified this operation gets all firewall rules available on that Redis Cache.</span></span>

## <span data-ttu-id="854ce-108">예제의</span><span class="sxs-lookup"><span data-stu-id="854ce-108">EXAMPLES</span></span>

### <span data-ttu-id="854ce-109">예제 1: 단일 방화벽 규칙 가져오기</span><span class="sxs-lookup"><span data-stu-id="854ce-109">Example 1: Get a single firewall rule</span></span>
```
PS C:\>Get-AzureRmRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone"

        ResourceGroupName : myGroup
        Name              : mycache
        FirewallRuleId    : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/mycache/firewallRules/ruleone
        RuleName          : ruleone
        Type              : Microsoft.Cache/Redis/firewallRules
        StartIP           : 10.0.0.1
        EndIP             : 10.0.0.32
```

<span data-ttu-id="854ce-110">이 명령은 mycache 라는 Redis Cache에서 ruleone 이라는 방화벽 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="854ce-110">This command gets firewall rule named ruleone from Redis Cache named mycache.</span></span>

### <span data-ttu-id="854ce-111">예제 2: 모든 방화벽 규칙 가져오기</span><span class="sxs-lookup"><span data-stu-id="854ce-111">Example 2: Get all firewall rules</span></span>
```
PS C:\>Get-AzureRmRedisCacheFirewallRule -Name "mycache"

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

<span data-ttu-id="854ce-112">이 명령은 Redis Cache 이라는 mycache의 모든 방화벽 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="854ce-112">This command gets all firewall rules from Redis Cache named mycache.</span></span>

## <span data-ttu-id="854ce-113">변수</span><span class="sxs-lookup"><span data-stu-id="854ce-113">PARAMETERS</span></span>

### <span data-ttu-id="854ce-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="854ce-114">-DefaultProfile</span></span>
<span data-ttu-id="854ce-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="854ce-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="854ce-116">-이름</span><span class="sxs-lookup"><span data-stu-id="854ce-116">-Name</span></span>
<span data-ttu-id="854ce-117">Redis cache의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="854ce-117">Name of redis cache.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="854ce-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="854ce-118">-ResourceGroupName</span></span>
<span data-ttu-id="854ce-119">캐시가 있는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="854ce-119">Name of resource group in which cache exists.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="854ce-120">-RuleName</span><span class="sxs-lookup"><span data-stu-id="854ce-120">-RuleName</span></span>
<span data-ttu-id="854ce-121">방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="854ce-121">Name of firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="854ce-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="854ce-122">CommonParameters</span></span>
<span data-ttu-id="854ce-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="854ce-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="854ce-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="854ce-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="854ce-125">입력</span><span class="sxs-lookup"><span data-stu-id="854ce-125">INPUTS</span></span>

### <span data-ttu-id="854ce-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="854ce-126">System.String</span></span>
<span data-ttu-id="854ce-127">이름으로이 cmdlet에 대 한 입력을 파이프 할 수 있지만 값을 기준으로 하지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="854ce-127">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="854ce-128">출력</span><span class="sxs-lookup"><span data-stu-id="854ce-128">OUTPUTS</span></span>

### <span data-ttu-id="854ce-129">System.webserver. List ' 1 [[PSRedisFirewallRule, Microsoft azure. r e.]. 4.0.1.0, Version =, Culture = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="854ce-129">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule, Microsoft.Azure.Commands.RedisCache, Version=4.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="854ce-130">상속자</span><span class="sxs-lookup"><span data-stu-id="854ce-130">NOTES</span></span>

## <span data-ttu-id="854ce-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="854ce-131">RELATED LINKS</span></span>

[<span data-ttu-id="854ce-132">새로운 AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="854ce-132">New-AzureRmRedisCacheFirewallRule</span></span>](./New-AzureRmRedisCacheFirewallRule.md)

[<span data-ttu-id="854ce-133">제거-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="854ce-133">Remove-AzureRmRedisCacheFirewallRule</span></span>](./Remove-AzureRmRedisCacheFirewallRule.md)

[<span data-ttu-id="854ce-134">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="854ce-134">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="854ce-135">새로운 AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="854ce-135">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="854ce-136">제거-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="854ce-136">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="854ce-137">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="854ce-137">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)
