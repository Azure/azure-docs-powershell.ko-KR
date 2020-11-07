---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheFirewallRule.md
ms.openlocfilehash: c89589d966c03614255751bf13769689ff875332
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702516"
---
# <span data-ttu-id="1434f-101">New-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="1434f-101">New-AzureRmRedisCacheFirewallRule</span></span>

## <span data-ttu-id="1434f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1434f-102">SYNOPSIS</span></span>
<span data-ttu-id="1434f-103">Redis Cache에 방화벽 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1434f-103">Create a firewall rule on a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1434f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1434f-104">SYNTAX</span></span>

### <span data-ttu-id="1434f-105">NormalParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="1434f-105">NormalParameterSet (Default)</span></span>
```
New-AzureRmRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String>
 -StartIP <String> -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1434f-106">RedisCacheAttributesObject</span><span class="sxs-lookup"><span data-stu-id="1434f-106">RedisCacheAttributesObject</span></span>
```
New-AzureRmRedisCacheFirewallRule -InputObject <RedisCacheAttributes> -RuleName <String> -StartIP <String>
 -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1434f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1434f-107">ResourceIdParameterSet</span></span>
```
New-AzureRmRedisCacheFirewallRule -ResourceId <String> -RuleName <String> -StartIP <String> -EndIP <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1434f-108">설명은</span><span class="sxs-lookup"><span data-stu-id="1434f-108">DESCRIPTION</span></span>
<span data-ttu-id="1434f-109">Redis Cache에 방화벽 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1434f-109">Create a firewall rule on a Redis Cache.</span></span>

## <span data-ttu-id="1434f-110">예제의</span><span class="sxs-lookup"><span data-stu-id="1434f-110">EXAMPLES</span></span>

### <span data-ttu-id="1434f-111">예제 1: 방화벽 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="1434f-111">Example 1: Create a firewall rule</span></span>
```
PS C:\>New-AzureRmRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone" -StartIP "10.0.0.1" -EndIP "10.0.0.32"

        ResourceGroupName : myGroup
        Name              : mycache
        FirewallRuleId    : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/mycache/firewallRules/ruleone
        RuleName          : ruleone
        Type              : Microsoft.Cache/Redis/firewallRules
        StartIP           : 10.0.0.1
        EndIP             : 10.0.0.32
```

<span data-ttu-id="1434f-112">이 명령은 mycache 라는 Redis Cache에 ruleone 이라는 방화벽 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1434f-112">This command creates firewall rule named ruleone on Redis Cache named mycache.</span></span>

## <span data-ttu-id="1434f-113">변수</span><span class="sxs-lookup"><span data-stu-id="1434f-113">PARAMETERS</span></span>

### <span data-ttu-id="1434f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1434f-114">-DefaultProfile</span></span>
<span data-ttu-id="1434f-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1434f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1434f-116">-EndIP</span><span class="sxs-lookup"><span data-stu-id="1434f-116">-EndIP</span></span>
<span data-ttu-id="1434f-117">종료 IP 주소</span><span class="sxs-lookup"><span data-stu-id="1434f-117">Ending IP address.</span></span>

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

### <span data-ttu-id="1434f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1434f-118">-InputObject</span></span>
<span data-ttu-id="1434f-119">RedisCacheAttributes 유형의 개체</span><span class="sxs-lookup"><span data-stu-id="1434f-119">object of type RedisCacheAttributes</span></span>

```yaml
Type: RedisCacheAttributes
Parameter Sets: RedisCacheAttributesObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1434f-120">-이름</span><span class="sxs-lookup"><span data-stu-id="1434f-120">-Name</span></span>
<span data-ttu-id="1434f-121">Redis cache의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1434f-121">Name of redis cache.</span></span>

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

### <span data-ttu-id="1434f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1434f-122">-ResourceGroupName</span></span>
<span data-ttu-id="1434f-123">캐시가 있는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1434f-123">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="1434f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1434f-124">-ResourceId</span></span>
<span data-ttu-id="1434f-125">Redis Cache의 ARM Id입니다.</span><span class="sxs-lookup"><span data-stu-id="1434f-125">ARM Id of Redis Cache.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1434f-126">-RuleName</span><span class="sxs-lookup"><span data-stu-id="1434f-126">-RuleName</span></span>
<span data-ttu-id="1434f-127">방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1434f-127">Name of firewall rule.</span></span>

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

### <span data-ttu-id="1434f-128">-StartIP</span><span class="sxs-lookup"><span data-stu-id="1434f-128">-StartIP</span></span>
<span data-ttu-id="1434f-129">시작 IP 주소</span><span class="sxs-lookup"><span data-stu-id="1434f-129">Starting IP address.</span></span>

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

### <span data-ttu-id="1434f-130">-확인</span><span class="sxs-lookup"><span data-stu-id="1434f-130">-Confirm</span></span>
<span data-ttu-id="1434f-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1434f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1434f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1434f-132">-WhatIf</span></span>
<span data-ttu-id="1434f-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1434f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1434f-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1434f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1434f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1434f-135">CommonParameters</span></span>
<span data-ttu-id="1434f-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1434f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1434f-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1434f-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1434f-138">입력</span><span class="sxs-lookup"><span data-stu-id="1434f-138">INPUTS</span></span>

### <span data-ttu-id="1434f-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1434f-139">System.String</span></span>

## <span data-ttu-id="1434f-140">출력</span><span class="sxs-lookup"><span data-stu-id="1434f-140">OUTPUTS</span></span>

### <span data-ttu-id="1434f-141">PSRedisFirewallRule. 모델. m e.</span><span class="sxs-lookup"><span data-stu-id="1434f-141">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="1434f-142">상속자</span><span class="sxs-lookup"><span data-stu-id="1434f-142">NOTES</span></span>

## <span data-ttu-id="1434f-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1434f-143">RELATED LINKS</span></span>

[<span data-ttu-id="1434f-144">Get-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="1434f-144">Get-AzureRmRedisCacheFirewallRule</span></span>](./Get-AzureRmRedisCacheFirewallRule.md)

[<span data-ttu-id="1434f-145">제거-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="1434f-145">Remove-AzureRmRedisCacheFirewallRule</span></span>](./Remove-AzureRmRedisCacheFirewallRule.md)

[<span data-ttu-id="1434f-146">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="1434f-146">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="1434f-147">새로운 AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="1434f-147">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="1434f-148">제거-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="1434f-148">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="1434f-149">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="1434f-149">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)
