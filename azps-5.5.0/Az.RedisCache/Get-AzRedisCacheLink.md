---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheLink.md
ms.openlocfilehash: 58c52e30270af309eb5104bbc0a9308f83df91ea
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189236"
---
# <span data-ttu-id="88f42-101">Get-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="88f42-101">Get-AzRedisCacheLink</span></span>

## <span data-ttu-id="88f42-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88f42-102">SYNOPSIS</span></span>
<span data-ttu-id="88f42-103">Redis Cache에 대한 지역 복제 링크를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="88f42-103">Get geo replication link for Redis Cache.</span></span>

## <span data-ttu-id="88f42-104">구문</span><span class="sxs-lookup"><span data-stu-id="88f42-104">SYNTAX</span></span>

### <span data-ttu-id="88f42-105">AllLinksForCache(기본값)</span><span class="sxs-lookup"><span data-stu-id="88f42-105">AllLinksForCache (Default)</span></span>
```
Get-AzRedisCacheLink -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88f42-106">AllLinksForPrimaryCache</span><span class="sxs-lookup"><span data-stu-id="88f42-106">AllLinksForPrimaryCache</span></span>
```
Get-AzRedisCacheLink -PrimaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="88f42-107">SingleLink</span><span class="sxs-lookup"><span data-stu-id="88f42-107">SingleLink</span></span>
```
Get-AzRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88f42-108">AllLinksForSecondaryCache</span><span class="sxs-lookup"><span data-stu-id="88f42-108">AllLinksForSecondaryCache</span></span>
```
Get-AzRedisCacheLink -SecondaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="88f42-109">설명</span><span class="sxs-lookup"><span data-stu-id="88f42-109">DESCRIPTION</span></span>
<span data-ttu-id="88f42-110">지역 복제 링크 세부 정보를 얻을 수 있는 네 가지 방법이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="88f42-110">There are four different ways to get geo-replication link detail.</span></span> <span data-ttu-id="88f42-111">매개 변수 이름 또는 PrimaryServerName 및/또는 SecondaryServerName을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="88f42-111">Either provide parameter Name or PrimaryServerName and/or SecondaryServerName.</span></span> <span data-ttu-id="88f42-112">이름이 지정된 후 캐시가 있는 모든 링크가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="88f42-112">Name is given then all link where cache exists will be returned.</span></span> <span data-ttu-id="88f42-113">PrimaryServerName만 제공된 경우 캐시가 기본인 모든 링크가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="88f42-113">If only PrimaryServerName is given then all links where cache is primary will be returned.</span></span> <span data-ttu-id="88f42-114">SecondaryServerName만 제공된 경우 캐시가 보조인 모든 링크가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="88f42-114">If only SecondaryServerName is given then all links where cache is secondary will be returned.</span></span> <span data-ttu-id="88f42-115">PrimaryServerName 및 SecondaryServerName이 모두 제공된 경우 올바른 역할의 특정 링크가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="88f42-115">If PrimaryServerName and SecondaryServerName both are given then specific link with correct role will be returned.</span></span> 

## <span data-ttu-id="88f42-116">예제</span><span class="sxs-lookup"><span data-stu-id="88f42-116">EXAMPLES</span></span>

### <span data-ttu-id="88f42-117">예제 1: AllLinksForCache 매개 변수 집합 사용</span><span class="sxs-lookup"><span data-stu-id="88f42-117">Example 1: Get using parameter set AllLinksForCache</span></span>
```
PS C:\>Get-AzRedisCacheLink -Name "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="88f42-118">이 명령은 mycache1이라는 Redis Cache에 대한 모든 지역 복제 링크를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="88f42-118">This command gets all geo-replication links for Redis Cache named mycache1.</span></span>

### <span data-ttu-id="88f42-119">예제 2: AllLinksForPrimaryCache 매개 변수 집합 사용</span><span class="sxs-lookup"><span data-stu-id="88f42-119">Example 2: Get using parameter set AllLinksForPrimaryCache</span></span>
```
PS C:\>Get-AzRedisCacheLink -PrimaryServerName "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="88f42-120">이 명령은 mycache1이라는 Redis Cache가 기본인 지역 복제 링크를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="88f42-120">This command gets geo-replication links where Redis Cache named mycache1 is primary.</span></span>

### <span data-ttu-id="88f42-121">예제 3: AllLinksForSecondaryCache 매개 변수 집합 사용</span><span class="sxs-lookup"><span data-stu-id="88f42-121">Example 3: Get using parameter set AllLinksForSecondaryCache</span></span>
```
PS C:\>Get-AzRedisCacheLink -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="88f42-122">이 명령은 mycache2라는 Redis Cache가 보조인 지역 복제 링크를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="88f42-122">This command gets geo-replication links where Redis Cache named mycache2 is secondary.</span></span>

### <span data-ttu-id="88f42-123">예제 4: 매개 변수 집합 SingleLink 사용</span><span class="sxs-lookup"><span data-stu-id="88f42-123">Example 4: Get using parameter set SingleLink</span></span>
```
PS C:\>Get-AzRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="88f42-124">이 명령은 mycache1이라는 Redis Cache가 기본이고 mycache2라는 Redis Cache가 보조인 단일 지역 복제 링크를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="88f42-124">This command gets a single geo-replication links where Redis Cache named mycache1 is primary and Redis Cache named mycache2 is secondary.</span></span>

## <span data-ttu-id="88f42-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="88f42-125">PARAMETERS</span></span>

### <span data-ttu-id="88f42-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88f42-126">-DefaultProfile</span></span>
<span data-ttu-id="88f42-127">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="88f42-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88f42-128">-Name</span><span class="sxs-lookup"><span data-stu-id="88f42-128">-Name</span></span>
<span data-ttu-id="88f42-129">redis Cache의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="88f42-129">Name of redis cache.</span></span>

```yaml
Type: System.String
Parameter Sets: AllLinksForCache
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88f42-130">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="88f42-130">-PrimaryServerName</span></span>
<span data-ttu-id="88f42-131">링크에 있는 기본 redis Cache의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="88f42-131">Name of primary redis cache in link.</span></span>

```yaml
Type: System.String
Parameter Sets: AllLinksForPrimaryCache, SingleLink
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88f42-132">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="88f42-132">-SecondaryServerName</span></span>
<span data-ttu-id="88f42-133">링크에 있는 보조 Redis Cache의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="88f42-133">Name of secondary redis cache in link.</span></span>

```yaml
Type: System.String
Parameter Sets: SingleLink, AllLinksForSecondaryCache
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88f42-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88f42-134">CommonParameters</span></span>
<span data-ttu-id="88f42-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="88f42-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88f42-136">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="88f42-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88f42-137">입력</span><span class="sxs-lookup"><span data-stu-id="88f42-137">INPUTS</span></span>

### <span data-ttu-id="88f42-138">System.String</span><span class="sxs-lookup"><span data-stu-id="88f42-138">System.String</span></span>

## <span data-ttu-id="88f42-139">출력</span><span class="sxs-lookup"><span data-stu-id="88f42-139">OUTPUTS</span></span>

### <span data-ttu-id="88f42-140">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span><span class="sxs-lookup"><span data-stu-id="88f42-140">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span></span>

## <span data-ttu-id="88f42-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="88f42-141">NOTES</span></span>

## <span data-ttu-id="88f42-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="88f42-142">RELATED LINKS</span></span>

[<span data-ttu-id="88f42-143">New-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="88f42-143">New-AzRedisCacheLink</span></span>](./New-AzRedisCacheLink.md)

[<span data-ttu-id="88f42-144">Remove-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="88f42-144">Remove-AzRedisCacheLink</span></span>](./Remove-AzRedisCacheLink.md)

[<span data-ttu-id="88f42-145">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="88f42-145">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="88f42-146">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="88f42-146">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="88f42-147">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="88f42-147">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="88f42-148">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="88f42-148">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)