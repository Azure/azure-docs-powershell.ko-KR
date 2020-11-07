---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheLink.md
ms.openlocfilehash: e4f4dd72104b4a57823c54e6cf56f531f48e610d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873442"
---
# <span data-ttu-id="ad2a8-101">Remove-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="ad2a8-101">Remove-AzRedisCacheLink</span></span>

## <span data-ttu-id="ad2a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad2a8-102">SYNOPSIS</span></span>
<span data-ttu-id="ad2a8-103">두 Redis 캐시 간에 지리적 복제 링크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad2a8-103">Remove a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="ad2a8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ad2a8-104">SYNTAX</span></span>

```
Remove-AzRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad2a8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ad2a8-105">DESCRIPTION</span></span>
<span data-ttu-id="ad2a8-106">두 Redis 캐시 간에 지리적 복제 링크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad2a8-106">Remove a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="ad2a8-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ad2a8-107">EXAMPLES</span></span>

### <span data-ttu-id="ad2a8-108">예제 1: 지역 복제 링크 제거</span><span class="sxs-lookup"><span data-stu-id="ad2a8-108">Example 1: Remove a geo replication link</span></span>
```
PS C:\>Remove-AzRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"
```

<span data-ttu-id="ad2a8-109">이 명령은 mycache1 이라는 Redis 캐시가 기본이 고 mycache2 이라는 Redis Cache가 보조 인 지역/복제 링크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad2a8-109">This command removes a geo-replication links where Redis Cache named mycache1 is primary and Redis Cache named mycache2 is secondary.</span></span>

## <span data-ttu-id="ad2a8-110">변수</span><span class="sxs-lookup"><span data-stu-id="ad2a8-110">PARAMETERS</span></span>

### <span data-ttu-id="ad2a8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad2a8-111">-DefaultProfile</span></span>
<span data-ttu-id="ad2a8-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ad2a8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad2a8-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ad2a8-113">-PassThru</span></span>
<span data-ttu-id="ad2a8-114">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="ad2a8-114">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="ad2a8-115">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="ad2a8-115">-PrimaryServerName</span></span>
<span data-ttu-id="ad2a8-116">Link의 기본 redis cache 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ad2a8-116">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="ad2a8-117">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="ad2a8-117">-SecondaryServerName</span></span>
<span data-ttu-id="ad2a8-118">Link의 보조 redis 캐시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ad2a8-118">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="ad2a8-119">-확인</span><span class="sxs-lookup"><span data-stu-id="ad2a8-119">-Confirm</span></span>
<span data-ttu-id="ad2a8-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad2a8-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad2a8-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad2a8-121">-WhatIf</span></span>
<span data-ttu-id="ad2a8-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ad2a8-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad2a8-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ad2a8-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad2a8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad2a8-124">CommonParameters</span></span>
<span data-ttu-id="ad2a8-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad2a8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad2a8-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad2a8-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad2a8-127">입력</span><span class="sxs-lookup"><span data-stu-id="ad2a8-127">INPUTS</span></span>

### <span data-ttu-id="ad2a8-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ad2a8-128">System.String</span></span>

## <span data-ttu-id="ad2a8-129">출력</span><span class="sxs-lookup"><span data-stu-id="ad2a8-129">OUTPUTS</span></span>

### <span data-ttu-id="ad2a8-130">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="ad2a8-130">System.Boolean</span></span>

## <span data-ttu-id="ad2a8-131">상속자</span><span class="sxs-lookup"><span data-stu-id="ad2a8-131">NOTES</span></span>

## <span data-ttu-id="ad2a8-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ad2a8-132">RELATED LINKS</span></span>

[<span data-ttu-id="ad2a8-133">새로운 AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="ad2a8-133">New-AzRedisCacheLink</span></span>](./New-AzRedisCacheLink.md)

[<span data-ttu-id="ad2a8-134">Get-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="ad2a8-134">Get-AzRedisCacheLink</span></span>](./Get-AzRedisCacheLink.md)

[<span data-ttu-id="ad2a8-135">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="ad2a8-135">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="ad2a8-136">새로운 AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="ad2a8-136">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="ad2a8-137">제거-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="ad2a8-137">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="ad2a8-138">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="ad2a8-138">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)