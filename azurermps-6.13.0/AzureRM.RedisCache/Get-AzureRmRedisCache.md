---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 8EF45FCE-5475-4A18-BFB0-C016E239612E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/get-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCache.md
ms.openlocfilehash: ee4d5980743e5a78205c6e1f78cb55fa9b2f6496
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535659"
---
# <span data-ttu-id="f27cd-101">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="f27cd-101">Get-AzureRmRedisCache</span></span>

## <span data-ttu-id="f27cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f27cd-102">SYNOPSIS</span></span>
<span data-ttu-id="f27cd-103">Redis 캐시를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f27cd-103">Gets a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f27cd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f27cd-104">SYNTAX</span></span>

```
Get-AzureRmRedisCache [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f27cd-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f27cd-105">DESCRIPTION</span></span>
<span data-ttu-id="f27cd-106">**AzureRmRedisCache** cmdlet은 지정 된 Azure Redis Cache를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f27cd-106">The **Get-AzureRmRedisCache** cmdlet gets the specified Azure Redis Cache.</span></span>
<span data-ttu-id="f27cd-107">매개 변수를 지정 하지 않으면이 작업은 현재 구독에 대 한 모든 Redis 캐시를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f27cd-107">If you specify no parameters, this operation gets every Redis Cache for the current subscription.</span></span>

## <span data-ttu-id="f27cd-108">예제의</span><span class="sxs-lookup"><span data-stu-id="f27cd-108">EXAMPLES</span></span>

### <span data-ttu-id="f27cd-109">예제 1: 이름으로 Redis 캐시 가져오기</span><span class="sxs-lookup"><span data-stu-id="f27cd-109">Example 1: Get a Redis Cache by name</span></span>
```
PS C:\>Get-AzureRmRedisCache -Name "myexists"

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

<span data-ttu-id="f27cd-110">이 명령은 myexists 라는 Redis 캐시를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f27cd-110">This command gets the Redis Cache named myexists.</span></span>

### <span data-ttu-id="f27cd-111">예제 2: 리소스 그룹의 모든 Redis 캐시 가져오기</span><span class="sxs-lookup"><span data-stu-id="f27cd-111">Example 2: Get every Redis Cache in a resource group</span></span>
```
PS C:\>Get-AzureRmRedisCache -ResourceGroupName "myGroup"

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

<span data-ttu-id="f27cd-112">이 명령은 지정 된 리소스 그룹에 있는 모든 Redis 캐시를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f27cd-112">This command gets every Redis Cache in the specified resource group.</span></span>

### <span data-ttu-id="f27cd-113">예제 3: 현재 구독에서 모든 Redis 캐시 가져오기</span><span class="sxs-lookup"><span data-stu-id="f27cd-113">Example 3: Get every Redis Cache in the current subscription</span></span>
```
PS C:\>Get-AzureRmRedisCache

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

<span data-ttu-id="f27cd-114">이 명령은 현재 구독에 있는 모든 Redis 캐시를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f27cd-114">This command gets every Redis Cache in the current subscription.</span></span>

## <span data-ttu-id="f27cd-115">변수</span><span class="sxs-lookup"><span data-stu-id="f27cd-115">PARAMETERS</span></span>

### <span data-ttu-id="f27cd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f27cd-116">-DefaultProfile</span></span>
<span data-ttu-id="f27cd-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f27cd-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f27cd-118">-이름</span><span class="sxs-lookup"><span data-stu-id="f27cd-118">-Name</span></span>
<span data-ttu-id="f27cd-119">가져올 Redis 캐시의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f27cd-119">Specifies the name of the Redis Cache to get.</span></span>
<span data-ttu-id="f27cd-120">*ResourceGroupName* 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f27cd-120">Use with the *ResourceGroupName* parameter.</span></span>

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

### <span data-ttu-id="f27cd-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f27cd-121">-ResourceGroupName</span></span>
<span data-ttu-id="f27cd-122">가져올 Redis 캐시가 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f27cd-122">Specifies the name of the resource group that contains the Redis Cache to get.</span></span>
<span data-ttu-id="f27cd-123">*ResourceGroupName* 매개 변수만 지정 하는 경우이 작업은 지정 된 리소스 그룹의 모든 Redis 캐시를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f27cd-123">If you specify only the *ResourceGroupName* parameter, this operation gets every Redis Cache in the specified resource group.</span></span>

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

### <span data-ttu-id="f27cd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f27cd-124">CommonParameters</span></span>
<span data-ttu-id="f27cd-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f27cd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f27cd-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f27cd-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f27cd-127">입력</span><span class="sxs-lookup"><span data-stu-id="f27cd-127">INPUTS</span></span>

### <span data-ttu-id="f27cd-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f27cd-128">System.String</span></span>

## <span data-ttu-id="f27cd-129">출력</span><span class="sxs-lookup"><span data-stu-id="f27cd-129">OUTPUTS</span></span>

### <span data-ttu-id="f27cd-130">Microsoft. Azure. 모델을 다시 캐시 합니다. Rediscache특성</span><span class="sxs-lookup"><span data-stu-id="f27cd-130">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span></span>

## <span data-ttu-id="f27cd-131">상속자</span><span class="sxs-lookup"><span data-stu-id="f27cd-131">NOTES</span></span>

## <span data-ttu-id="f27cd-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f27cd-132">RELATED LINKS</span></span>

[<span data-ttu-id="f27cd-133">새로운 AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="f27cd-133">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="f27cd-134">제거-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="f27cd-134">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="f27cd-135">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="f27cd-135">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


