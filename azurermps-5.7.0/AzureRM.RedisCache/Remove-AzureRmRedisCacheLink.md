---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/remove-azurermrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCacheLink.md
ms.openlocfilehash: a0532feb24966cfe05b0175080fa2333307f33e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529751"
---
# <span data-ttu-id="cd291-101">Remove-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="cd291-101">Remove-AzureRmRedisCacheLink</span></span>

## <span data-ttu-id="cd291-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd291-102">SYNOPSIS</span></span>
<span data-ttu-id="cd291-103">두 Redis 캐시 간에 지리적 복제 링크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd291-103">Remove a geo replication link between two Redis Caches.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd291-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cd291-104">SYNTAX</span></span>

```
Remove-AzureRmRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd291-105">설명은</span><span class="sxs-lookup"><span data-stu-id="cd291-105">DESCRIPTION</span></span>
<span data-ttu-id="cd291-106">두 Redis 캐시 간에 지리적 복제 링크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd291-106">Remove a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="cd291-107">예제의</span><span class="sxs-lookup"><span data-stu-id="cd291-107">EXAMPLES</span></span>

### <span data-ttu-id="cd291-108">예제 1: 지역 복제 링크 제거</span><span class="sxs-lookup"><span data-stu-id="cd291-108">Example 1: Remove a geo replication link</span></span>
```
PS C:\>Remove-AzureRmRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"
```

<span data-ttu-id="cd291-109">이 명령은 mycache1 이라는 Redis 캐시가 기본이 고 mycache2 이라는 Redis Cache가 보조 인 지역/복제 링크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd291-109">This command removes a geo-replication links where Redis Cache named mycache1 is primary and Redis Cache named mycache2 is secondary.</span></span>

## <span data-ttu-id="cd291-110">변수</span><span class="sxs-lookup"><span data-stu-id="cd291-110">PARAMETERS</span></span>

### <span data-ttu-id="cd291-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd291-111">-DefaultProfile</span></span>
<span data-ttu-id="cd291-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cd291-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd291-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cd291-113">-PassThru</span></span>
<span data-ttu-id="cd291-114">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="cd291-114">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd291-115">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="cd291-115">-PrimaryServerName</span></span>
<span data-ttu-id="cd291-116">Link의 기본 redis cache 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cd291-116">Name of primary redis cache in link.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd291-117">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="cd291-117">-SecondaryServerName</span></span>
<span data-ttu-id="cd291-118">Link의 보조 redis 캐시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cd291-118">Name of secondary redis cache in link.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd291-119">-확인</span><span class="sxs-lookup"><span data-stu-id="cd291-119">-Confirm</span></span>
<span data-ttu-id="cd291-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd291-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd291-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd291-121">-WhatIf</span></span>
<span data-ttu-id="cd291-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="cd291-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd291-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cd291-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd291-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd291-124">CommonParameters</span></span>
<span data-ttu-id="cd291-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd291-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd291-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd291-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd291-127">입력</span><span class="sxs-lookup"><span data-stu-id="cd291-127">INPUTS</span></span>

### <span data-ttu-id="cd291-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="cd291-128">System.String</span></span>

## <span data-ttu-id="cd291-129">출력</span><span class="sxs-lookup"><span data-stu-id="cd291-129">OUTPUTS</span></span>

### <span data-ttu-id="cd291-130">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="cd291-130">System.Boolean</span></span>

## <span data-ttu-id="cd291-131">상속자</span><span class="sxs-lookup"><span data-stu-id="cd291-131">NOTES</span></span>

## <span data-ttu-id="cd291-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cd291-132">RELATED LINKS</span></span>

[<span data-ttu-id="cd291-133">새로운 AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="cd291-133">New-AzureRmRedisCacheLink</span></span>](./New-AzureRmRedisCacheLink.md)

[<span data-ttu-id="cd291-134">Get-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="cd291-134">Get-AzureRmRedisCacheLink</span></span>](./Get-AzureRmRedisCacheLink.md)

[<span data-ttu-id="cd291-135">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="cd291-135">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="cd291-136">새로운 AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="cd291-136">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="cd291-137">제거-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="cd291-137">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="cd291-138">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="cd291-138">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)
