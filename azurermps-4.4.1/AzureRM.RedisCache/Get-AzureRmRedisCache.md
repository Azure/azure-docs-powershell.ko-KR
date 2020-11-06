---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 8EF45FCE-5475-4A18-BFB0-C016E239612E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCache.md
ms.openlocfilehash: 4cdd81b0cf9f83482192fbe6f484fb0b0d1beaf6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536200"
---
# <span data-ttu-id="cc6e6-101">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="cc6e6-101">Get-AzureRmRedisCache</span></span>

## <span data-ttu-id="cc6e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc6e6-102">SYNOPSIS</span></span>
<span data-ttu-id="cc6e6-103">Redis 캐시를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cc6e6-103">Gets a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc6e6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cc6e6-104">SYNTAX</span></span>

### <span data-ttu-id="cc6e6-105">모든 구독에서 (기본값)</span><span class="sxs-lookup"><span data-stu-id="cc6e6-105">All In Subscription (Default)</span></span>
```
Get-AzureRmRedisCache [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cc6e6-106">모두 리소스 그룹에서</span><span class="sxs-lookup"><span data-stu-id="cc6e6-106">All In Resource Group</span></span>
```
Get-AzureRmRedisCache -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cc6e6-107">특정 Redis 캐시</span><span class="sxs-lookup"><span data-stu-id="cc6e6-107">Specific Redis Cache</span></span>
```
Get-AzureRmRedisCache -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cc6e6-108">설명은</span><span class="sxs-lookup"><span data-stu-id="cc6e6-108">DESCRIPTION</span></span>
<span data-ttu-id="cc6e6-109">**AzureRmRedisCache** cmdlet은 지정 된 Azure Redis Cache를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cc6e6-109">The **Get-AzureRmRedisCache** cmdlet gets the specified Azure Redis Cache.</span></span>
<span data-ttu-id="cc6e6-110">매개 변수를 지정 하지 않으면이 작업은 현재 구독에 대 한 모든 Redis 캐시를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cc6e6-110">If you specify no parameters, this operation gets every Redis Cache for the current subscription.</span></span>

## <span data-ttu-id="cc6e6-111">예제의</span><span class="sxs-lookup"><span data-stu-id="cc6e6-111">EXAMPLES</span></span>

### <span data-ttu-id="cc6e6-112">예제 1: 이름으로 Redis 캐시 가져오기</span><span class="sxs-lookup"><span data-stu-id="cc6e6-112">Example 1: Get a Redis Cache by name</span></span>
```
PS C:\>Get-AzureRmRedisCache -ResourceGroupName "myGroup" -Name "myexists"

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
```

<span data-ttu-id="cc6e6-113">이 명령은 myexists 라는 Redis 캐시를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cc6e6-113">This command gets the Redis Cache named myexists.</span></span>

### <span data-ttu-id="cc6e6-114">예제 2: 리소스 그룹의 모든 Redis 캐시 가져오기</span><span class="sxs-lookup"><span data-stu-id="cc6e6-114">Example 2: Get every Redis Cache in a resource group</span></span>
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
```

<span data-ttu-id="cc6e6-115">이 명령은 지정 된 리소스 그룹에 있는 모든 Redis 캐시를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cc6e6-115">This command gets every Redis Cache in the specified resource group.</span></span>

### <span data-ttu-id="cc6e6-116">예제 3: 현재 구독에서 모든 Redis 캐시 가져오기</span><span class="sxs-lookup"><span data-stu-id="cc6e6-116">Example 3: Get every Redis Cache in the current subscription</span></span>
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
```

<span data-ttu-id="cc6e6-117">이 명령은 현재 구독에 있는 모든 Redis 캐시를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cc6e6-117">This command gets every Redis Cache in the current subscription.</span></span>

## <span data-ttu-id="cc6e6-118">변수</span><span class="sxs-lookup"><span data-stu-id="cc6e6-118">PARAMETERS</span></span>

### <span data-ttu-id="cc6e6-119">-이름</span><span class="sxs-lookup"><span data-stu-id="cc6e6-119">-Name</span></span>
<span data-ttu-id="cc6e6-120">가져올 Redis 캐시의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc6e6-120">Specifies the name of the Redis Cache to get.</span></span>
<span data-ttu-id="cc6e6-121">*ResourceGroupName* 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc6e6-121">Use with the *ResourceGroupName* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific Redis Cache
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc6e6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc6e6-122">-ResourceGroupName</span></span>
<span data-ttu-id="cc6e6-123">가져올 Redis 캐시가 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc6e6-123">Specifies the name of the resource group that contains the Redis Cache to get.</span></span>

<span data-ttu-id="cc6e6-124">*ResourceGroupName* 매개 변수만 지정 하는 경우이 작업은 지정 된 리소스 그룹의 모든 Redis 캐시를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cc6e6-124">If you specify only the *ResourceGroupName* parameter, this operation gets every Redis Cache in the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: All In Resource Group, Specific Redis Cache
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc6e6-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc6e6-125">-DefaultProfile</span></span>
<span data-ttu-id="cc6e6-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cc6e6-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc6e6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc6e6-127">CommonParameters</span></span>
<span data-ttu-id="cc6e6-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc6e6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc6e6-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc6e6-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc6e6-130">입력</span><span class="sxs-lookup"><span data-stu-id="cc6e6-130">INPUTS</span></span>

### <span data-ttu-id="cc6e6-131">않아야</span><span class="sxs-lookup"><span data-stu-id="cc6e6-131">None</span></span>
<span data-ttu-id="cc6e6-132">이름으로이 cmdlet에 대 한 입력을 파이프 할 수 있지만 값을 기준으로 하지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cc6e6-132">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="cc6e6-133">출력</span><span class="sxs-lookup"><span data-stu-id="cc6e6-133">OUTPUTS</span></span>

### <span data-ttu-id="cc6e6-134">Microsoft. Azure. 모델을 다시 캐시 합니다. Rediscache특성</span><span class="sxs-lookup"><span data-stu-id="cc6e6-134">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span></span>
<span data-ttu-id="cc6e6-135">**Rediscacheattributes** 개체의 배열을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc6e6-135">Returns an array of **RedisCacheAttributes** objects.</span></span>

## <span data-ttu-id="cc6e6-136">상속자</span><span class="sxs-lookup"><span data-stu-id="cc6e6-136">NOTES</span></span>

## <span data-ttu-id="cc6e6-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cc6e6-137">RELATED LINKS</span></span>

[<span data-ttu-id="cc6e6-138">새로운 AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="cc6e6-138">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="cc6e6-139">제거-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="cc6e6-139">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="cc6e6-140">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="cc6e6-140">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


