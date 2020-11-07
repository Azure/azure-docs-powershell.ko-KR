---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 8EF45FCE-5475-4A18-BFB0-C016E239612E
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCache.md
ms.openlocfilehash: 1e7f57ce251c6f95a74b2ca0a55aa1caa92349a7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873461"
---
# <span data-ttu-id="90431-101">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="90431-101">Get-AzRedisCache</span></span>

## <span data-ttu-id="90431-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90431-102">SYNOPSIS</span></span>
<span data-ttu-id="90431-103">Redis 캐시를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="90431-103">Gets a Redis Cache.</span></span>

## <span data-ttu-id="90431-104">구문과</span><span class="sxs-lookup"><span data-stu-id="90431-104">SYNTAX</span></span>

```
Get-AzRedisCache [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="90431-105">설명은</span><span class="sxs-lookup"><span data-stu-id="90431-105">DESCRIPTION</span></span>
<span data-ttu-id="90431-106">**AzRedisCache** cmdlet은 지정 된 Azure Redis Cache를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="90431-106">The **Get-AzRedisCache** cmdlet gets the specified Azure Redis Cache.</span></span>
<span data-ttu-id="90431-107">매개 변수를 지정 하지 않으면이 작업은 현재 구독에 대 한 모든 Redis 캐시를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="90431-107">If you specify no parameters, this operation gets every Redis Cache for the current subscription.</span></span>

## <span data-ttu-id="90431-108">예제의</span><span class="sxs-lookup"><span data-stu-id="90431-108">EXAMPLES</span></span>

### <span data-ttu-id="90431-109">예제 1: 이름으로 Redis 캐시 가져오기</span><span class="sxs-lookup"><span data-stu-id="90431-109">Example 1: Get a Redis Cache by name</span></span>
```
PS C:\>Get-AzRedisCache -Name "myexists"

        ResourceGroupName  : myGroup
        Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/myexists
        Location           : North Central US
        Name               : myexists
        Type               : Microsoft.Cache/Redis
        HostName           : myexists.redis.cache.windows.net
        Port               : 6379
        ProvisioningState  : succeeded
        SslPort            : 6380
        RedisConfiguration : {}
        EnableNonSslPort   : False
        RedisVersion       : 2.8
        Size               : 1GB
        Sku                : Basic
        Tag                : {}
        Zone               : []
```

<span data-ttu-id="90431-110">이 명령은 myexists 라는 Redis 캐시를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="90431-110">This command gets the Redis Cache named myexists.</span></span>

### <span data-ttu-id="90431-111">예제 2: 리소스 그룹의 모든 Redis 캐시 가져오기</span><span class="sxs-lookup"><span data-stu-id="90431-111">Example 2: Get every Redis Cache in a resource group</span></span>
```
PS C:\>Get-AzRedisCache -ResourceGroupName "myGroup"

        ResourceGroupName  : myGroup
        Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/myexists
        Location           : North Central US
        Name               : myexists
        Type               : Microsoft.Cache/Redis
        HostName           : myexists.redis.cache.windows.net
        Port               : 6379
        ProvisioningState  : succeeded
        SslPort            : 6380
        RedisConfiguration : {}
        EnableNonSslPort   : False
        RedisVersion       : 2.8
        Size               : 1GB
        Sku                : Basic
        Tag                : {}
        Zone               : []

        ResourceGroupName  : myGroup
        Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/myearlier
        Location           : North Central US
        Name               : myearlier
        Type               : Microsoft.Cache/Redis
        HostName           : myearlier.redis.cache.windows.net
        Port               : 6379
        ProvisioningState  : succeeded
        SslPort            : 6380
        RedisConfiguration : {}
        EnableNonSslPort   : True
        RedisVersion       : 2.8
        Size               : 250MB
        Sku                : Standard
        Tag                : {}
        Zone               : []
```

<span data-ttu-id="90431-112">이 명령은 지정 된 리소스 그룹에 있는 모든 Redis 캐시를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="90431-112">This command gets every Redis Cache in the specified resource group.</span></span>

### <span data-ttu-id="90431-113">예제 3: 현재 구독에서 모든 Redis 캐시 가져오기</span><span class="sxs-lookup"><span data-stu-id="90431-113">Example 3: Get every Redis Cache in the current subscription</span></span>
```
PS C:\>Get-AzRedisCache

        ResourceGroupName  : myGroup
        Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/myexists
        Location           : North Central US
        Name               : myexists
        Type               : Microsoft.Cache/Redis
        HostName           : myexists.redis.cache.windows.net
        Port               : 6379
        ProvisioningState  : succeeded
        SslPort            : 6380
        RedisConfiguration : {}
        EnableNonSslPort   : False
        RedisVersion       : 2.8
        Size               : 1GB
        Sku                : Basic
        Tag                : {}
        Zone               : []

        ResourceGroupName  : myGroup
        Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/myearlier
        Location           : North Central US
        Name               : myearlier
        Type               : Microsoft.Cache/Redis
        HostName           : myearlier.redis.cache.windows.net
        Port               : 6379
        ProvisioningState  : succeeded
        SslPort            : 6380
        RedisConfiguration : {}
        EnableNonSslPort   : True
        RedisVersion       : 2.8
        Size               : 250MB
        Sku                : Standard
        Tag                : {}
        Zone               : []

        ResourceGroupName  : myGroup2
        Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup2/providers/Microsoft.Cache/Redis/myearlier2
        Location           : North Central US
        Name               : myearlier2
        Type               : Microsoft.Cache/Redis
        HostName           : myearlier2.redis.cache.windows.net
        Port               : 6379
        ProvisioningState  : succeeded
        SslPort            : 6380
        RedisConfiguration : {}
        EnableNonSslPort   : False
        RedisVersion       : 2.8
        Size               : 250MB
        Sku                : Basic
        Tag                : {}
        Zone               : []
```

<span data-ttu-id="90431-114">이 명령은 현재 구독에 있는 모든 Redis 캐시를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="90431-114">This command gets every Redis Cache in the current subscription.</span></span>

## <span data-ttu-id="90431-115">변수</span><span class="sxs-lookup"><span data-stu-id="90431-115">PARAMETERS</span></span>

### <span data-ttu-id="90431-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90431-116">-DefaultProfile</span></span>
<span data-ttu-id="90431-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="90431-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90431-118">-이름</span><span class="sxs-lookup"><span data-stu-id="90431-118">-Name</span></span>
<span data-ttu-id="90431-119">가져올 Redis 캐시의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90431-119">Specifies the name of the Redis Cache to get.</span></span>
<span data-ttu-id="90431-120">*ResourceGroupName* 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="90431-120">Use with the *ResourceGroupName* parameter.</span></span>

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

### <span data-ttu-id="90431-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90431-121">-ResourceGroupName</span></span>
<span data-ttu-id="90431-122">가져올 Redis 캐시가 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90431-122">Specifies the name of the resource group that contains the Redis Cache to get.</span></span>
<span data-ttu-id="90431-123">*ResourceGroupName* 매개 변수만 지정 하는 경우이 작업은 지정 된 리소스 그룹의 모든 Redis 캐시를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="90431-123">If you specify only the *ResourceGroupName* parameter, this operation gets every Redis Cache in the specified resource group.</span></span>

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

### <span data-ttu-id="90431-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90431-124">CommonParameters</span></span>
<span data-ttu-id="90431-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="90431-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90431-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90431-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90431-127">입력</span><span class="sxs-lookup"><span data-stu-id="90431-127">INPUTS</span></span>

### <span data-ttu-id="90431-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="90431-128">System.String</span></span>

## <span data-ttu-id="90431-129">출력</span><span class="sxs-lookup"><span data-stu-id="90431-129">OUTPUTS</span></span>

### <span data-ttu-id="90431-130">Microsoft. Azure. 모델을 다시 캐시 합니다. Rediscache특성</span><span class="sxs-lookup"><span data-stu-id="90431-130">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span></span>

## <span data-ttu-id="90431-131">상속자</span><span class="sxs-lookup"><span data-stu-id="90431-131">NOTES</span></span>

## <span data-ttu-id="90431-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="90431-132">RELATED LINKS</span></span>

[<span data-ttu-id="90431-133">새로운 AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="90431-133">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="90431-134">제거-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="90431-134">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="90431-135">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="90431-135">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


