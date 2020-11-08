---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheFirewallRule.md
ms.openlocfilehash: c19be1f524519a55a5a95a575e97cfd250952570
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217550"
---
# <span data-ttu-id="b76ec-101">Remove-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b76ec-101">Remove-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="b76ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b76ec-102">SYNOPSIS</span></span>
<span data-ttu-id="b76ec-103">Redis 캐시에서 방화벽 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b76ec-103">Remove a firewall rule from a Redis Cache.</span></span>

## <span data-ttu-id="b76ec-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b76ec-104">SYNTAX</span></span>

### <span data-ttu-id="b76ec-105">NormalParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="b76ec-105">NormalParameterSet (Default)</span></span>
```
Remove-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b76ec-106">PSRedisFirewallRuleObject</span><span class="sxs-lookup"><span data-stu-id="b76ec-106">PSRedisFirewallRuleObject</span></span>
```
Remove-AzRedisCacheFirewallRule -InputObject <PSRedisFirewallRule> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b76ec-107">설명은</span><span class="sxs-lookup"><span data-stu-id="b76ec-107">DESCRIPTION</span></span>
<span data-ttu-id="b76ec-108">Redis 캐시에서 방화벽 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b76ec-108">Remove a firewall rule from a Redis Cache.</span></span>

## <span data-ttu-id="b76ec-109">예제의</span><span class="sxs-lookup"><span data-stu-id="b76ec-109">EXAMPLES</span></span>

### <span data-ttu-id="b76ec-110">예제 1: 단일 방화벽 규칙 제거</span><span class="sxs-lookup"><span data-stu-id="b76ec-110">Example 1: Remove a single firewall rule</span></span>
```
PS C:\>Remove-AzRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone" -PassThru
True
```

<span data-ttu-id="b76ec-111">이 명령은 mycache 라는 Redis Cache에서 ruleone 이라는 방화벽 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b76ec-111">This command removes a firewall rule named ruleone from Redis Cache named mycache.</span></span> 

## <span data-ttu-id="b76ec-112">변수</span><span class="sxs-lookup"><span data-stu-id="b76ec-112">PARAMETERS</span></span>

### <span data-ttu-id="b76ec-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b76ec-113">-DefaultProfile</span></span>
<span data-ttu-id="b76ec-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b76ec-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b76ec-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b76ec-115">-InputObject</span></span>
<span data-ttu-id="b76ec-116">PSRedisFirewallRule 유형의 개체</span><span class="sxs-lookup"><span data-stu-id="b76ec-116">object of type PSRedisFirewallRule</span></span>

```yaml
Type: Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule
Parameter Sets: PSRedisFirewallRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b76ec-117">-이름</span><span class="sxs-lookup"><span data-stu-id="b76ec-117">-Name</span></span>
<span data-ttu-id="b76ec-118">Redis cache의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b76ec-118">Name of redis cache.</span></span>

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

### <span data-ttu-id="b76ec-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b76ec-119">-PassThru</span></span>
<span data-ttu-id="b76ec-120">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="b76ec-120">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b76ec-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b76ec-121">-ResourceGroupName</span></span>
<span data-ttu-id="b76ec-122">캐시가 있는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b76ec-122">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="b76ec-123">-RuleName</span><span class="sxs-lookup"><span data-stu-id="b76ec-123">-RuleName</span></span>
<span data-ttu-id="b76ec-124">방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b76ec-124">Name of firewall rule.</span></span>

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

### <span data-ttu-id="b76ec-125">-확인</span><span class="sxs-lookup"><span data-stu-id="b76ec-125">-Confirm</span></span>
<span data-ttu-id="b76ec-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b76ec-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b76ec-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b76ec-127">-WhatIf</span></span>
<span data-ttu-id="b76ec-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b76ec-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b76ec-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b76ec-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b76ec-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b76ec-130">CommonParameters</span></span>
<span data-ttu-id="b76ec-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b76ec-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b76ec-132">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b76ec-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b76ec-133">입력</span><span class="sxs-lookup"><span data-stu-id="b76ec-133">INPUTS</span></span>

### <span data-ttu-id="b76ec-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b76ec-134">System.String</span></span>

### <span data-ttu-id="b76ec-135">PSRedisFirewallRule. 모델. m e.</span><span class="sxs-lookup"><span data-stu-id="b76ec-135">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="b76ec-136">출력</span><span class="sxs-lookup"><span data-stu-id="b76ec-136">OUTPUTS</span></span>

### <span data-ttu-id="b76ec-137">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="b76ec-137">System.Boolean</span></span>

## <span data-ttu-id="b76ec-138">상속자</span><span class="sxs-lookup"><span data-stu-id="b76ec-138">NOTES</span></span>

## <span data-ttu-id="b76ec-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b76ec-139">RELATED LINKS</span></span>

[<span data-ttu-id="b76ec-140">새로운 AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b76ec-140">New-AzRedisCacheFirewallRule</span></span>](./New-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="b76ec-141">Get-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b76ec-141">Get-AzRedisCacheFirewallRule</span></span>](./Get-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="b76ec-142">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="b76ec-142">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="b76ec-143">새로운 AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="b76ec-143">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="b76ec-144">제거-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="b76ec-144">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="b76ec-145">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="b76ec-145">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)