---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 8EF45FCE-5475-4A18-BFB0-C016E239612E
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCache.md
ms.openlocfilehash: cc8d6ff7e7fb55c5ee71c82a8eca4cc661b98b07
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206176"
---
# <span data-ttu-id="e2263-101">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="e2263-101">Get-AzRedisCache</span></span>

## <span data-ttu-id="e2263-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2263-102">SYNOPSIS</span></span>
<span data-ttu-id="e2263-103">Redis Cache를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e2263-103">Gets a Redis Cache.</span></span>

## <span data-ttu-id="e2263-104">구문</span><span class="sxs-lookup"><span data-stu-id="e2263-104">SYNTAX</span></span>

```
Get-AzRedisCache [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e2263-105">설명</span><span class="sxs-lookup"><span data-stu-id="e2263-105">DESCRIPTION</span></span>
<span data-ttu-id="e2263-106">**Get-AzRedisCache** cmdlet은 지정된 Azure Redis Cache를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e2263-106">The **Get-AzRedisCache** cmdlet gets the specified Azure Redis Cache.</span></span>
<span data-ttu-id="e2263-107">매개 변수를 지정하지 않으면 이 작업은 현재 구독에 대한 모든 Redis Cache를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e2263-107">If you specify no parameters, this operation gets every Redis Cache for the current subscription.</span></span>

## <span data-ttu-id="e2263-108">예제</span><span class="sxs-lookup"><span data-stu-id="e2263-108">EXAMPLES</span></span>

### <span data-ttu-id="e2263-109">예제 1: 이름으로 Redis Cache를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e2263-109">Example 1: Get a Redis Cache by name</span></span>
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

<span data-ttu-id="e2263-110">이 명령은 myexists라는 Redis Cache를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e2263-110">This command gets the Redis Cache named myexists.</span></span>

### <span data-ttu-id="e2263-111">예제 2: 리소스 그룹의 모든 Redis Cache를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e2263-111">Example 2: Get every Redis Cache in a resource group</span></span>
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

<span data-ttu-id="e2263-112">이 명령은 지정된 리소스 그룹에 있는 모든 Redis Cache를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e2263-112">This command gets every Redis Cache in the specified resource group.</span></span>

### <span data-ttu-id="e2263-113">예제 3: 현재 구독의 모든 Redis Cache를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e2263-113">Example 3: Get every Redis Cache in the current subscription</span></span>
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

<span data-ttu-id="e2263-114">이 명령은 현재 구독의 모든 Redis Cache를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e2263-114">This command gets every Redis Cache in the current subscription.</span></span>

## <span data-ttu-id="e2263-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e2263-115">PARAMETERS</span></span>

### <span data-ttu-id="e2263-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2263-116">-DefaultProfile</span></span>
<span data-ttu-id="e2263-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e2263-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2263-118">-Name</span><span class="sxs-lookup"><span data-stu-id="e2263-118">-Name</span></span>
<span data-ttu-id="e2263-119">얻을 Redis Cache의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e2263-119">Specifies the name of the Redis Cache to get.</span></span>
<span data-ttu-id="e2263-120">*ResourceGroupName* 매개 변수와 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="e2263-120">Use with the *ResourceGroupName* parameter.</span></span>

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

### <span data-ttu-id="e2263-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2263-121">-ResourceGroupName</span></span>
<span data-ttu-id="e2263-122">얻을 Redis Cache를 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e2263-122">Specifies the name of the resource group that contains the Redis Cache to get.</span></span>
<span data-ttu-id="e2263-123">*ResourceGroupName* 매개 변수만 지정하면 이 작업은 지정된 리소스 그룹의 모든 Redis Cache를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e2263-123">If you specify only the *ResourceGroupName* parameter, this operation gets every Redis Cache in the specified resource group.</span></span>

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

### <span data-ttu-id="e2263-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2263-124">CommonParameters</span></span>
<span data-ttu-id="e2263-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e2263-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2263-126">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e2263-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2263-127">입력</span><span class="sxs-lookup"><span data-stu-id="e2263-127">INPUTS</span></span>

### <span data-ttu-id="e2263-128">System.String</span><span class="sxs-lookup"><span data-stu-id="e2263-128">System.String</span></span>

## <span data-ttu-id="e2263-129">출력</span><span class="sxs-lookup"><span data-stu-id="e2263-129">OUTPUTS</span></span>

### <span data-ttu-id="e2263-130">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="e2263-130">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span></span>

## <span data-ttu-id="e2263-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e2263-131">NOTES</span></span>

## <span data-ttu-id="e2263-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e2263-132">RELATED LINKS</span></span>

[<span data-ttu-id="e2263-133">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="e2263-133">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="e2263-134">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="e2263-134">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="e2263-135">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="e2263-135">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


