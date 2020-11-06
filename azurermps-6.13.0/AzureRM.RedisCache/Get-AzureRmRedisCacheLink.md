---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/get-azurermrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheLink.md
ms.openlocfilehash: a45407fc7f25e2c7bee5c591ab3110b0620a2c0f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530109"
---
# <span data-ttu-id="91a48-101">Get-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="91a48-101">Get-AzureRmRedisCacheLink</span></span>

## <span data-ttu-id="91a48-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91a48-102">SYNOPSIS</span></span>
<span data-ttu-id="91a48-103">Redis Cache에 대 한 지역 복제 링크를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="91a48-103">Get geo replication link for Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91a48-104">구문과</span><span class="sxs-lookup"><span data-stu-id="91a48-104">SYNTAX</span></span>

### <span data-ttu-id="91a48-105">All링크 Forcache (기본값)</span><span class="sxs-lookup"><span data-stu-id="91a48-105">AllLinksForCache (Default)</span></span>
```
Get-AzureRmRedisCacheLink -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91a48-106">All링크 Forprimarycache</span><span class="sxs-lookup"><span data-stu-id="91a48-106">AllLinksForPrimaryCache</span></span>
```
Get-AzureRmRedisCacheLink -PrimaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="91a48-107">SingleLink</span><span class="sxs-lookup"><span data-stu-id="91a48-107">SingleLink</span></span>
```
Get-AzureRmRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91a48-108">All링크 Forsecondarycache</span><span class="sxs-lookup"><span data-stu-id="91a48-108">AllLinksForSecondaryCache</span></span>
```
Get-AzureRmRedisCacheLink -SecondaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="91a48-109">설명은</span><span class="sxs-lookup"><span data-stu-id="91a48-109">DESCRIPTION</span></span>
<span data-ttu-id="91a48-110">지리적 복제 링크 세부 정보는 네 가지 방법으로 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91a48-110">There are four different ways to get geo-replication link detail.</span></span> <span data-ttu-id="91a48-111">매개 변수 이름 또는 PrimaryServerName 및/또는 SecondaryServerName을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="91a48-111">Either provide parameter Name or PrimaryServerName and/or SecondaryServerName.</span></span> <span data-ttu-id="91a48-112">Name이 지정 되 면 캐시가 존재 하는 모든 링크가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="91a48-112">Name is given then all link where cache exists will be returned.</span></span> <span data-ttu-id="91a48-113">PrimaryServerName만 지정 하는 경우 캐시가 기본으로 있는 모든 링크는 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="91a48-113">If only PrimaryServerName is given then all links where cache is primary will be returned.</span></span> <span data-ttu-id="91a48-114">SecondaryServerName만 지정 하는 경우 캐시가 보조 인 모든 링크는 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="91a48-114">If only SecondaryServerName is given then all links where cache is secondary will be returned.</span></span> <span data-ttu-id="91a48-115">PrimaryServerName 및 SecondaryServerName이 모두 지정 된 경우 올바른 역할의 특정 링크가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="91a48-115">If PrimaryServerName and SecondaryServerName both are given then specific link with correct role will be returned.</span></span> 

## <span data-ttu-id="91a48-116">예제의</span><span class="sxs-lookup"><span data-stu-id="91a48-116">EXAMPLES</span></span>

### <span data-ttu-id="91a48-117">예제 1: using 매개 변수 설정 가져오기 All링크 Forcache</span><span class="sxs-lookup"><span data-stu-id="91a48-117">Example 1: Get using parameter set AllLinksForCache</span></span>
```
PS C:\>Get-AzureRmRedisCacheLink -Name "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="91a48-118">이 명령은 mycache1 이라는 Redis Cache에 대 한 모든 지역/복제 링크를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="91a48-118">This command gets all geo-replication links for Redis Cache named mycache1.</span></span>

### <span data-ttu-id="91a48-119">예제 2: using 매개 변수 설정 가져오기 All링크 Forprimarycache</span><span class="sxs-lookup"><span data-stu-id="91a48-119">Example 2: Get using parameter set AllLinksForPrimaryCache</span></span>
```
PS C:\>Get-AzureRmRedisCacheLink -PrimaryServerName "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="91a48-120">이 명령은 mycache1 이라는 Redis 캐시가 기본 인 지역 복제 링크를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="91a48-120">This command gets geo-replication links where Redis Cache named mycache1 is primary.</span></span>

### <span data-ttu-id="91a48-121">예제 3: 사용 하는 매개 변수 설정 Get Allindex Forsecondarycache</span><span class="sxs-lookup"><span data-stu-id="91a48-121">Example 3: Get using parameter set AllLinksForSecondaryCache</span></span>
```
PS C:\>Get-AzureRmRedisCacheLink -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="91a48-122">이 명령은 mycache2 이라는 Redis 캐시가 보조 인 지역 복제 링크를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="91a48-122">This command gets geo-replication links where Redis Cache named mycache2 is secondary.</span></span>

### <span data-ttu-id="91a48-123">예제 4: SingleLink set 매개 변수를 사용 하 여 가져오기</span><span class="sxs-lookup"><span data-stu-id="91a48-123">Example 4: Get using parameter set SingleLink</span></span>
```
PS C:\>Get-AzureRmRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="91a48-124">이 명령은 mycache1 이라는 Redis 캐시가 기본 인 단일 지역 복제 링크와 mycache2 이라는 Redis Cache를 보조로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="91a48-124">This command gets a single geo-replication links where Redis Cache named mycache1 is primary and Redis Cache named mycache2 is secondary.</span></span>

## <span data-ttu-id="91a48-125">변수</span><span class="sxs-lookup"><span data-stu-id="91a48-125">PARAMETERS</span></span>

### <span data-ttu-id="91a48-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91a48-126">-DefaultProfile</span></span>
<span data-ttu-id="91a48-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="91a48-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91a48-128">-이름</span><span class="sxs-lookup"><span data-stu-id="91a48-128">-Name</span></span>
<span data-ttu-id="91a48-129">Redis cache의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="91a48-129">Name of redis cache.</span></span>

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

### <span data-ttu-id="91a48-130">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="91a48-130">-PrimaryServerName</span></span>
<span data-ttu-id="91a48-131">Link의 기본 redis cache 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="91a48-131">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="91a48-132">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="91a48-132">-SecondaryServerName</span></span>
<span data-ttu-id="91a48-133">Link의 보조 redis 캐시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="91a48-133">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="91a48-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91a48-134">CommonParameters</span></span>
<span data-ttu-id="91a48-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="91a48-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91a48-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91a48-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91a48-137">입력</span><span class="sxs-lookup"><span data-stu-id="91a48-137">INPUTS</span></span>

### <span data-ttu-id="91a48-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="91a48-138">System.String</span></span>

## <span data-ttu-id="91a48-139">출력</span><span class="sxs-lookup"><span data-stu-id="91a48-139">OUTPUTS</span></span>

### <span data-ttu-id="91a48-140">PSRedisLinkedServer. 모델. m e.</span><span class="sxs-lookup"><span data-stu-id="91a48-140">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span></span>

## <span data-ttu-id="91a48-141">상속자</span><span class="sxs-lookup"><span data-stu-id="91a48-141">NOTES</span></span>

## <span data-ttu-id="91a48-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="91a48-142">RELATED LINKS</span></span>

[<span data-ttu-id="91a48-143">새로운 AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="91a48-143">New-AzureRmRedisCacheLink</span></span>](./New-AzureRmRedisCacheLink.md)

[<span data-ttu-id="91a48-144">제거-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="91a48-144">Remove-AzureRmRedisCacheLink</span></span>](./Remove-AzureRmRedisCacheLink.md)

[<span data-ttu-id="91a48-145">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="91a48-145">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="91a48-146">새로운 AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="91a48-146">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="91a48-147">제거-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="91a48-147">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="91a48-148">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="91a48-148">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)
