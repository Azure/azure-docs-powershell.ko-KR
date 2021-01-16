---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheFirewallRule.md
ms.openlocfilehash: c19be1f524519a55a5a95a575e97cfd250952570
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344150"
---
# <span data-ttu-id="d3c1a-101">Remove-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d3c1a-101">Remove-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="d3c1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3c1a-102">SYNOPSIS</span></span>
<span data-ttu-id="d3c1a-103">Redis Cache에서 방화벽 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="d3c1a-103">Remove a firewall rule from a Redis Cache.</span></span>

## <span data-ttu-id="d3c1a-104">구문</span><span class="sxs-lookup"><span data-stu-id="d3c1a-104">SYNTAX</span></span>

### <span data-ttu-id="d3c1a-105">NormalParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="d3c1a-105">NormalParameterSet (Default)</span></span>
```
Remove-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3c1a-106">PSRedisFirewallRuleObject</span><span class="sxs-lookup"><span data-stu-id="d3c1a-106">PSRedisFirewallRuleObject</span></span>
```
Remove-AzRedisCacheFirewallRule -InputObject <PSRedisFirewallRule> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3c1a-107">설명</span><span class="sxs-lookup"><span data-stu-id="d3c1a-107">DESCRIPTION</span></span>
<span data-ttu-id="d3c1a-108">Redis Cache에서 방화벽 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="d3c1a-108">Remove a firewall rule from a Redis Cache.</span></span>

## <span data-ttu-id="d3c1a-109">예제</span><span class="sxs-lookup"><span data-stu-id="d3c1a-109">EXAMPLES</span></span>

### <span data-ttu-id="d3c1a-110">예제 1: 단일 방화벽 규칙 제거</span><span class="sxs-lookup"><span data-stu-id="d3c1a-110">Example 1: Remove a single firewall rule</span></span>
```
PS C:\>Remove-AzRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone" -PassThru
True
```

<span data-ttu-id="d3c1a-111">이 명령은 mycache라는 Redis Cache에서 ruleone이라는 방화벽 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="d3c1a-111">This command removes a firewall rule named ruleone from Redis Cache named mycache.</span></span> 

## <span data-ttu-id="d3c1a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d3c1a-112">PARAMETERS</span></span>

### <span data-ttu-id="d3c1a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3c1a-113">-DefaultProfile</span></span>
<span data-ttu-id="d3c1a-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d3c1a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3c1a-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d3c1a-115">-InputObject</span></span>
<span data-ttu-id="d3c1a-116">PSRedisFirewallRule 형식의 개체</span><span class="sxs-lookup"><span data-stu-id="d3c1a-116">object of type PSRedisFirewallRule</span></span>

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

### <span data-ttu-id="d3c1a-117">-Name</span><span class="sxs-lookup"><span data-stu-id="d3c1a-117">-Name</span></span>
<span data-ttu-id="d3c1a-118">redis Cache의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d3c1a-118">Name of redis cache.</span></span>

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

### <span data-ttu-id="d3c1a-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d3c1a-119">-PassThru</span></span>
<span data-ttu-id="d3c1a-120">{{PassThru 설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="d3c1a-120">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="d3c1a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3c1a-121">-ResourceGroupName</span></span>
<span data-ttu-id="d3c1a-122">캐시가 있는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d3c1a-122">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="d3c1a-123">-RuleName</span><span class="sxs-lookup"><span data-stu-id="d3c1a-123">-RuleName</span></span>
<span data-ttu-id="d3c1a-124">방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d3c1a-124">Name of firewall rule.</span></span>

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

### <span data-ttu-id="d3c1a-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d3c1a-125">-Confirm</span></span>
<span data-ttu-id="d3c1a-126">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d3c1a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3c1a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3c1a-127">-WhatIf</span></span>
<span data-ttu-id="d3c1a-128">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="d3c1a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3c1a-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d3c1a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3c1a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3c1a-130">CommonParameters</span></span>
<span data-ttu-id="d3c1a-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d3c1a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3c1a-132">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d3c1a-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3c1a-133">입력</span><span class="sxs-lookup"><span data-stu-id="d3c1a-133">INPUTS</span></span>

### <span data-ttu-id="d3c1a-134">System.String</span><span class="sxs-lookup"><span data-stu-id="d3c1a-134">System.String</span></span>

### <span data-ttu-id="d3c1a-135">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d3c1a-135">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="d3c1a-136">출력</span><span class="sxs-lookup"><span data-stu-id="d3c1a-136">OUTPUTS</span></span>

### <span data-ttu-id="d3c1a-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d3c1a-137">System.Boolean</span></span>

## <span data-ttu-id="d3c1a-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d3c1a-138">NOTES</span></span>

## <span data-ttu-id="d3c1a-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d3c1a-139">RELATED LINKS</span></span>

[<span data-ttu-id="d3c1a-140">New-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d3c1a-140">New-AzRedisCacheFirewallRule</span></span>](./New-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="d3c1a-141">Get-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d3c1a-141">Get-AzRedisCacheFirewallRule</span></span>](./Get-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="d3c1a-142">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="d3c1a-142">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="d3c1a-143">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="d3c1a-143">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="d3c1a-144">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="d3c1a-144">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="d3c1a-145">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="d3c1a-145">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)