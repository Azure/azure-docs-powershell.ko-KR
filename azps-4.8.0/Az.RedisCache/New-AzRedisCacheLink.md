---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheLink.md
ms.openlocfilehash: d27f3ece14e18465fc534bff1a3451eaec2c40a3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204467"
---
# <span data-ttu-id="8b4c8-101">New-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="8b4c8-101">New-AzRedisCacheLink</span></span>

## <span data-ttu-id="8b4c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b4c8-102">SYNOPSIS</span></span>
<span data-ttu-id="8b4c8-103">두 Redis 캐시 간에 지역 복제 링크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8b4c8-103">Create a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="8b4c8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8b4c8-104">SYNTAX</span></span>

```
New-AzRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b4c8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8b4c8-105">DESCRIPTION</span></span>
<span data-ttu-id="8b4c8-106">두 Redis 캐시 간에 지역 복제 링크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8b4c8-106">Create a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="8b4c8-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8b4c8-107">EXAMPLES</span></span>

### <span data-ttu-id="8b4c8-108">예제 1: 두 캐시 간에 링크 만들기</span><span class="sxs-lookup"><span data-stu-id="8b4c8-108">Example 1: Create a link between two caches</span></span>
```
PS C:\>New-AzRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Creating
```

<span data-ttu-id="8b4c8-109">이 명령은 Redis Cache mycache1 및 mycache2 간에 지리적 복제 링크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8b4c8-109">This command creates geo-replication link between Redis Cache mycache1 and mycache2.</span></span>

## <span data-ttu-id="8b4c8-110">변수</span><span class="sxs-lookup"><span data-stu-id="8b4c8-110">PARAMETERS</span></span>

### <span data-ttu-id="8b4c8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b4c8-111">-DefaultProfile</span></span>
<span data-ttu-id="8b4c8-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8b4c8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b4c8-113">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="8b4c8-113">-PrimaryServerName</span></span>
<span data-ttu-id="8b4c8-114">Link의 기본 redis cache 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8b4c8-114">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="8b4c8-115">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="8b4c8-115">-SecondaryServerName</span></span>
<span data-ttu-id="8b4c8-116">Link의 보조 redis 캐시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8b4c8-116">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="8b4c8-117">-확인</span><span class="sxs-lookup"><span data-stu-id="8b4c8-117">-Confirm</span></span>
<span data-ttu-id="8b4c8-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b4c8-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b4c8-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b4c8-119">-WhatIf</span></span>
<span data-ttu-id="8b4c8-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8b4c8-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b4c8-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8b4c8-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b4c8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b4c8-122">CommonParameters</span></span>
<span data-ttu-id="8b4c8-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b4c8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b4c8-124">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b4c8-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b4c8-125">입력</span><span class="sxs-lookup"><span data-stu-id="8b4c8-125">INPUTS</span></span>

### <span data-ttu-id="8b4c8-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8b4c8-126">System.String</span></span>

## <span data-ttu-id="8b4c8-127">출력</span><span class="sxs-lookup"><span data-stu-id="8b4c8-127">OUTPUTS</span></span>

### <span data-ttu-id="8b4c8-128">PSRedisLinkedServer. 모델. m e.</span><span class="sxs-lookup"><span data-stu-id="8b4c8-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span></span>

## <span data-ttu-id="8b4c8-129">상속자</span><span class="sxs-lookup"><span data-stu-id="8b4c8-129">NOTES</span></span>

## <span data-ttu-id="8b4c8-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8b4c8-130">RELATED LINKS</span></span>

[<span data-ttu-id="8b4c8-131">Get-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="8b4c8-131">Get-AzRedisCacheLink</span></span>](./Get-AzRedisCacheLink.md)

[<span data-ttu-id="8b4c8-132">제거-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="8b4c8-132">Remove-AzRedisCacheLink</span></span>](./Remove-AzRedisCacheLink.md)

[<span data-ttu-id="8b4c8-133">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="8b4c8-133">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="8b4c8-134">새로운 AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="8b4c8-134">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="8b4c8-135">제거-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="8b4c8-135">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="8b4c8-136">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="8b4c8-136">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)