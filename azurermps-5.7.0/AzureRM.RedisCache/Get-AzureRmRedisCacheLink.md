---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/get-azurermrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheLink.md
ms.openlocfilehash: dff5f565e27f89360465ede3eb8fbe2c3d5620a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528859"
---
# <span data-ttu-id="00bf7-101">Get-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="00bf7-101">Get-AzureRmRedisCacheLink</span></span>

## <span data-ttu-id="00bf7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00bf7-102">SYNOPSIS</span></span>
<span data-ttu-id="00bf7-103">Redis Cache에 대 한 지역 복제 링크를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="00bf7-103">Get geo replication link for Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00bf7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="00bf7-104">SYNTAX</span></span>

### <span data-ttu-id="00bf7-105">All링크 Forcache (기본값)</span><span class="sxs-lookup"><span data-stu-id="00bf7-105">AllLinksForCache (Default)</span></span>
```
Get-AzureRmRedisCacheLink -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00bf7-106">All링크 Forprimarycache</span><span class="sxs-lookup"><span data-stu-id="00bf7-106">AllLinksForPrimaryCache</span></span>
```
Get-AzureRmRedisCacheLink -PrimaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="00bf7-107">SingleLink</span><span class="sxs-lookup"><span data-stu-id="00bf7-107">SingleLink</span></span>
```
Get-AzureRmRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00bf7-108">All링크 Forsecondarycache</span><span class="sxs-lookup"><span data-stu-id="00bf7-108">AllLinksForSecondaryCache</span></span>
```
Get-AzureRmRedisCacheLink -SecondaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="00bf7-109">설명은</span><span class="sxs-lookup"><span data-stu-id="00bf7-109">DESCRIPTION</span></span>
<span data-ttu-id="00bf7-110">지리적 복제 링크 세부 정보는 네 가지 방법으로 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00bf7-110">There are four different ways to get geo-replication link detail.</span></span> <span data-ttu-id="00bf7-111">매개 변수 이름 또는 PrimaryServerName 및/또는 SecondaryServerName을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="00bf7-111">Either provide parameter Name or PrimaryServerName and/or SecondaryServerName.</span></span> <span data-ttu-id="00bf7-112">Name이 지정 되 면 캐시가 존재 하는 모든 링크가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="00bf7-112">Name is given then all link where cache exists will be returned.</span></span> <span data-ttu-id="00bf7-113">PrimaryServerName만 지정 하는 경우 캐시가 기본으로 있는 모든 링크는 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="00bf7-113">If only PrimaryServerName is given then all links where cache is primary will be returned.</span></span> <span data-ttu-id="00bf7-114">SecondaryServerName만 지정 하는 경우 캐시가 보조 인 모든 링크는 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="00bf7-114">If only SecondaryServerName is given then all links where cache is secondary will be returned.</span></span> <span data-ttu-id="00bf7-115">PrimaryServerName 및 SecondaryServerName이 모두 지정 된 경우 올바른 역할의 특정 링크가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="00bf7-115">If PrimaryServerName and SecondaryServerName both are given then specific link with correct role will be returned.</span></span> 

## <span data-ttu-id="00bf7-116">예제의</span><span class="sxs-lookup"><span data-stu-id="00bf7-116">EXAMPLES</span></span>

### <span data-ttu-id="00bf7-117">예제 1: using 매개 변수 설정 가져오기 All링크 Forcache</span><span class="sxs-lookup"><span data-stu-id="00bf7-117">Example 1: Get using parameter set AllLinksForCache</span></span>
```
PS C:\>Get-AzureRmRedisCacheLink -Name "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="00bf7-118">이 명령은 mycache1 이라는 Redis Cache에 대 한 모든 지역/복제 링크를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="00bf7-118">This command gets all geo-replication links for Redis Cache named mycache1.</span></span>

### <span data-ttu-id="00bf7-119">예제 2: using 매개 변수 설정 가져오기 All링크 Forprimarycache</span><span class="sxs-lookup"><span data-stu-id="00bf7-119">Example 2: Get using parameter set AllLinksForPrimaryCache</span></span>
```
PS C:\>Get-AzureRmRedisCacheLink -PrimaryServerName "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="00bf7-120">이 명령은 mycache1 이라는 Redis 캐시가 기본 인 지역 복제 링크를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="00bf7-120">This command gets geo-replication links where Redis Cache named mycache1 is primary.</span></span>

### <span data-ttu-id="00bf7-121">예제 3: 사용 하는 매개 변수 설정 Get Allindex Forsecondarycache</span><span class="sxs-lookup"><span data-stu-id="00bf7-121">Example 3: Get using parameter set AllLinksForSecondaryCache</span></span>
```
PS C:\>Get-AzureRmRedisCacheLink -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="00bf7-122">이 명령은 mycache2 이라는 Redis 캐시가 보조 인 지역 복제 링크를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="00bf7-122">This command gets geo-replication links where Redis Cache named mycache2 is secondary.</span></span>

### <span data-ttu-id="00bf7-123">예제 4: SingleLink set 매개 변수를 사용 하 여 가져오기</span><span class="sxs-lookup"><span data-stu-id="00bf7-123">Example 4: Get using parameter set SingleLink</span></span>
```
PS C:\>Get-AzureRmRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="00bf7-124">이 명령은 mycache1 이라는 Redis 캐시가 기본 인 단일 지역 복제 링크와 mycache2 이라는 Redis Cache를 보조로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="00bf7-124">This command gets a single geo-replication links where Redis Cache named mycache1 is primary and Redis Cache named mycache2 is secondary.</span></span>

## <span data-ttu-id="00bf7-125">변수</span><span class="sxs-lookup"><span data-stu-id="00bf7-125">PARAMETERS</span></span>

### <span data-ttu-id="00bf7-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00bf7-126">-DefaultProfile</span></span>
<span data-ttu-id="00bf7-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="00bf7-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00bf7-128">-이름</span><span class="sxs-lookup"><span data-stu-id="00bf7-128">-Name</span></span>
<span data-ttu-id="00bf7-129">Redis cache의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="00bf7-129">Name of redis cache.</span></span>

```yaml
Type: String
Parameter Sets: AllLinksForCache
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00bf7-130">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="00bf7-130">-PrimaryServerName</span></span>
<span data-ttu-id="00bf7-131">Link의 기본 redis cache 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="00bf7-131">Name of primary redis cache in link.</span></span>

```yaml
Type: String
Parameter Sets: AllLinksForPrimaryCache, SingleLink
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00bf7-132">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="00bf7-132">-SecondaryServerName</span></span>
<span data-ttu-id="00bf7-133">Link의 보조 redis 캐시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="00bf7-133">Name of secondary redis cache in link.</span></span>

```yaml
Type: String
Parameter Sets: SingleLink, AllLinksForSecondaryCache
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00bf7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00bf7-134">CommonParameters</span></span>
<span data-ttu-id="00bf7-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="00bf7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00bf7-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00bf7-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00bf7-137">입력</span><span class="sxs-lookup"><span data-stu-id="00bf7-137">INPUTS</span></span>

### <span data-ttu-id="00bf7-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="00bf7-138">System.String</span></span>
<span data-ttu-id="00bf7-139">이름으로이 cmdlet에 대 한 입력을 파이프 할 수 있지만 값을 기준으로 하지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="00bf7-139">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="00bf7-140">출력</span><span class="sxs-lookup"><span data-stu-id="00bf7-140">OUTPUTS</span></span>

### <span data-ttu-id="00bf7-141">System.webserver. List ' 1 [[PSRedisLinkedServer, Microsoft azure. r e.]. 4.0.1.0, Version =, Culture = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="00bf7-141">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer, Microsoft.Azure.Commands.RedisCache, Version=4.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="00bf7-142">상속자</span><span class="sxs-lookup"><span data-stu-id="00bf7-142">NOTES</span></span>

## <span data-ttu-id="00bf7-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="00bf7-143">RELATED LINKS</span></span>

[<span data-ttu-id="00bf7-144">새로운 AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="00bf7-144">New-AzureRmRedisCacheLink</span></span>](./New-AzureRmRedisCacheLink.md)

[<span data-ttu-id="00bf7-145">제거-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="00bf7-145">Remove-AzureRmRedisCacheLink</span></span>](./Remove-AzureRmRedisCacheLink.md)

[<span data-ttu-id="00bf7-146">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="00bf7-146">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="00bf7-147">새로운 AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="00bf7-147">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="00bf7-148">제거-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="00bf7-148">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="00bf7-149">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="00bf7-149">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)
