---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/remove-azurermrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCacheFirewallRule.md
ms.openlocfilehash: 7f2e9a3bb54aab9def9eba7bdc2a84680fe121c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524968"
---
# <span data-ttu-id="24421-101">Remove-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="24421-101">Remove-AzureRmRedisCacheFirewallRule</span></span>

## <span data-ttu-id="24421-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24421-102">SYNOPSIS</span></span>
<span data-ttu-id="24421-103">Redis 캐시에서 방화벽 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="24421-103">Remove a firewall rule from a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24421-104">구문과</span><span class="sxs-lookup"><span data-stu-id="24421-104">SYNTAX</span></span>

### <span data-ttu-id="24421-105">NormalParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="24421-105">NormalParameterSet (Default)</span></span>
```
Remove-AzureRmRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24421-106">PSRedisFirewallRuleObject</span><span class="sxs-lookup"><span data-stu-id="24421-106">PSRedisFirewallRuleObject</span></span>
```
Remove-AzureRmRedisCacheFirewallRule -InputObject <PSRedisFirewallRule> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24421-107">설명은</span><span class="sxs-lookup"><span data-stu-id="24421-107">DESCRIPTION</span></span>
<span data-ttu-id="24421-108">Redis 캐시에서 방화벽 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="24421-108">Remove a firewall rule from a Redis Cache.</span></span>

## <span data-ttu-id="24421-109">예제의</span><span class="sxs-lookup"><span data-stu-id="24421-109">EXAMPLES</span></span>

### <span data-ttu-id="24421-110">예제 1: 단일 방화벽 규칙 제거</span><span class="sxs-lookup"><span data-stu-id="24421-110">Example 1: Remove a single firewall rule</span></span>
```
PS C:\>Remove-AzureRmRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone" -PassThru
True
```

<span data-ttu-id="24421-111">이 명령은 mycache 라는 Redis Cache에서 ruleone 이라는 방화벽 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="24421-111">This command removes a firewall rule named ruleone from Redis Cache named mycache.</span></span> 

## <span data-ttu-id="24421-112">변수</span><span class="sxs-lookup"><span data-stu-id="24421-112">PARAMETERS</span></span>

### <span data-ttu-id="24421-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24421-113">-DefaultProfile</span></span>
<span data-ttu-id="24421-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="24421-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24421-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="24421-115">-InputObject</span></span>
<span data-ttu-id="24421-116">PSRedisFirewallRule 유형의 개체</span><span class="sxs-lookup"><span data-stu-id="24421-116">object of type PSRedisFirewallRule</span></span>

```yaml
Type: PSRedisFirewallRule
Parameter Sets: PSRedisFirewallRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="24421-117">-이름</span><span class="sxs-lookup"><span data-stu-id="24421-117">-Name</span></span>
<span data-ttu-id="24421-118">Redis cache의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24421-118">Name of redis cache.</span></span>

```yaml
Type: String
Parameter Sets: NormalParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24421-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="24421-119">-PassThru</span></span>
<span data-ttu-id="24421-120">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="24421-120">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24421-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24421-121">-ResourceGroupName</span></span>
<span data-ttu-id="24421-122">캐시가 있는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24421-122">Name of resource group in which cache exists.</span></span>

```yaml
Type: String
Parameter Sets: NormalParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24421-123">-RuleName</span><span class="sxs-lookup"><span data-stu-id="24421-123">-RuleName</span></span>
<span data-ttu-id="24421-124">방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24421-124">Name of firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: NormalParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24421-125">-확인</span><span class="sxs-lookup"><span data-stu-id="24421-125">-Confirm</span></span>
<span data-ttu-id="24421-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="24421-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24421-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24421-127">-WhatIf</span></span>
<span data-ttu-id="24421-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="24421-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24421-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="24421-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24421-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24421-130">CommonParameters</span></span>
<span data-ttu-id="24421-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="24421-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24421-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24421-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24421-133">입력</span><span class="sxs-lookup"><span data-stu-id="24421-133">INPUTS</span></span>

### <span data-ttu-id="24421-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="24421-134">System.String</span></span>

## <span data-ttu-id="24421-135">출력</span><span class="sxs-lookup"><span data-stu-id="24421-135">OUTPUTS</span></span>

### <span data-ttu-id="24421-136">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="24421-136">System.Boolean</span></span>

## <span data-ttu-id="24421-137">상속자</span><span class="sxs-lookup"><span data-stu-id="24421-137">NOTES</span></span>

## <span data-ttu-id="24421-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="24421-138">RELATED LINKS</span></span>

[<span data-ttu-id="24421-139">새로운 AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="24421-139">New-AzureRmRedisCacheFirewallRule</span></span>](./New-AzureRmRedisCacheFirewallRule.md)

[<span data-ttu-id="24421-140">Get-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="24421-140">Get-AzureRmRedisCacheFirewallRule</span></span>](./Get-AzureRmRedisCacheFirewallRule.md)

[<span data-ttu-id="24421-141">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="24421-141">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="24421-142">새로운 AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="24421-142">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="24421-143">제거-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="24421-143">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="24421-144">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="24421-144">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)
