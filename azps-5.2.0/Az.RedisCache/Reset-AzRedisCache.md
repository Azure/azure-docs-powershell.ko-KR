---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: A73D4DDD-387A-4468-AC6E-F15BF473527E
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/reset-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Reset-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Reset-AzRedisCache.md
ms.openlocfilehash: c2373bb4ef093a35abc12b14f55f4c977fc54d64
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98352514"
---
# <span data-ttu-id="5dc9c-101">Reset-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="5dc9c-101">Reset-AzRedisCache</span></span>

## <span data-ttu-id="5dc9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5dc9c-102">SYNOPSIS</span></span>
<span data-ttu-id="5dc9c-103">캐시의 노드를 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="5dc9c-103">Restarts nodes of a cache.</span></span>

## <span data-ttu-id="5dc9c-104">구문</span><span class="sxs-lookup"><span data-stu-id="5dc9c-104">SYNTAX</span></span>

```
Reset-AzRedisCache [-ResourceGroupName <String>] -Name <String> -RebootType <String> [-ShardId <Int32>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5dc9c-105">설명</span><span class="sxs-lookup"><span data-stu-id="5dc9c-105">DESCRIPTION</span></span>
<span data-ttu-id="5dc9c-106">**Reset-AzRedisCache** cmdlet은 Azure Redis Cache 인스턴스의 노드를 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="5dc9c-106">The **Reset-AzRedisCache** cmdlet restarts nodes of an Azure Redis Cache instance.</span></span>

## <span data-ttu-id="5dc9c-107">예제</span><span class="sxs-lookup"><span data-stu-id="5dc9c-107">EXAMPLES</span></span>

### <span data-ttu-id="5dc9c-108">예제 1: 두 노드 다시 시작</span><span class="sxs-lookup"><span data-stu-id="5dc9c-108">Example 1: Restart both nodes</span></span>
```
PS C:\>Reset-AzRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -RebootType "AllNodes" -Force
```

<span data-ttu-id="5dc9c-109">이 명령은 RedisCache06이라는 캐시에 대해 두 노드를 모두 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="5dc9c-109">This command restarts both nodes for the cache named RedisCache06.</span></span>

## <span data-ttu-id="5dc9c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5dc9c-110">PARAMETERS</span></span>

### <span data-ttu-id="5dc9c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5dc9c-111">-DefaultProfile</span></span>
<span data-ttu-id="5dc9c-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5dc9c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5dc9c-113">-Force</span><span class="sxs-lookup"><span data-stu-id="5dc9c-113">-Force</span></span>
<span data-ttu-id="5dc9c-114">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="5dc9c-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5dc9c-115">-Name</span><span class="sxs-lookup"><span data-stu-id="5dc9c-115">-Name</span></span>
<span data-ttu-id="5dc9c-116">캐시의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5dc9c-116">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="5dc9c-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5dc9c-117">-PassThru</span></span>
<span data-ttu-id="5dc9c-118">이 cmdlet은 작업이 성공하는지 여부를 나타내는 부울을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="5dc9c-118">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="5dc9c-119">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5dc9c-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5dc9c-120">-RebootType</span><span class="sxs-lookup"><span data-stu-id="5dc9c-120">-RebootType</span></span>
<span data-ttu-id="5dc9c-121">다시 시작할 노드 또는 노드를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5dc9c-121">Specifies which node or nodes to restart.</span></span>
<span data-ttu-id="5dc9c-122">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="5dc9c-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5dc9c-123">PrimaryNode</span><span class="sxs-lookup"><span data-stu-id="5dc9c-123">PrimaryNode</span></span> 
- <span data-ttu-id="5dc9c-124">SecondaryNode</span><span class="sxs-lookup"><span data-stu-id="5dc9c-124">SecondaryNode</span></span> 
- <span data-ttu-id="5dc9c-125">AllNodes</span><span class="sxs-lookup"><span data-stu-id="5dc9c-125">AllNodes</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryNode, SecondaryNode, AllNodes

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5dc9c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5dc9c-126">-ResourceGroupName</span></span>
<span data-ttu-id="5dc9c-127">캐시를 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5dc9c-127">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="5dc9c-128">-ShardId</span><span class="sxs-lookup"><span data-stu-id="5dc9c-128">-ShardId</span></span>
<span data-ttu-id="5dc9c-129">클러스터링이 활성화된 프리미엄 캐시에 대해 이 cmdlet이 다시 시작하는 shard의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5dc9c-129">Specifies the ID of the shard that this cmdlet restarts for a premium cache with clustering enabled.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5dc9c-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5dc9c-130">-Confirm</span></span>
<span data-ttu-id="5dc9c-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5dc9c-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dc9c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5dc9c-132">-WhatIf</span></span>
<span data-ttu-id="5dc9c-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="5dc9c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5dc9c-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5dc9c-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dc9c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dc9c-135">CommonParameters</span></span>
<span data-ttu-id="5dc9c-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5dc9c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dc9c-137">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5dc9c-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dc9c-138">입력</span><span class="sxs-lookup"><span data-stu-id="5dc9c-138">INPUTS</span></span>

### <span data-ttu-id="5dc9c-139">System.String</span><span class="sxs-lookup"><span data-stu-id="5dc9c-139">System.String</span></span>

### <span data-ttu-id="5dc9c-140">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="5dc9c-140">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="5dc9c-141">출력</span><span class="sxs-lookup"><span data-stu-id="5dc9c-141">OUTPUTS</span></span>

### <span data-ttu-id="5dc9c-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5dc9c-142">System.Boolean</span></span>

## <span data-ttu-id="5dc9c-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5dc9c-143">NOTES</span></span>
* <span data-ttu-id="5dc9c-144">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, redis, 캐시, 웹, 웹앱, 웹 사이트</span><span class="sxs-lookup"><span data-stu-id="5dc9c-144">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="5dc9c-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5dc9c-145">RELATED LINKS</span></span>

[<span data-ttu-id="5dc9c-146">Export-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="5dc9c-146">Export-AzRedisCache</span></span>](./Export-AzRedisCache.md)

[<span data-ttu-id="5dc9c-147">Import-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="5dc9c-147">Import-AzRedisCache</span></span>](./Import-AzRedisCache.md)

[<span data-ttu-id="5dc9c-148">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="5dc9c-148">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="5dc9c-149">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="5dc9c-149">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="5dc9c-150">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="5dc9c-150">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


