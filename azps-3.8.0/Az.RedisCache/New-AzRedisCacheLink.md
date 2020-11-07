---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheLink.md
ms.openlocfilehash: d27f3ece14e18465fc534bff1a3451eaec2c40a3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93879189"
---
# <span data-ttu-id="b05ed-101">New-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="b05ed-101">New-AzRedisCacheLink</span></span>

## <span data-ttu-id="b05ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b05ed-102">SYNOPSIS</span></span>
<span data-ttu-id="b05ed-103">두 Redis 캐시 간에 지역 복제 링크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b05ed-103">Create a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="b05ed-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b05ed-104">SYNTAX</span></span>

```
New-AzRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b05ed-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b05ed-105">DESCRIPTION</span></span>
<span data-ttu-id="b05ed-106">두 Redis 캐시 간에 지역 복제 링크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b05ed-106">Create a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="b05ed-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b05ed-107">EXAMPLES</span></span>

### <span data-ttu-id="b05ed-108">예제 1: 두 캐시 간에 링크 만들기</span><span class="sxs-lookup"><span data-stu-id="b05ed-108">Example 1: Create a link between two caches</span></span>
```
PS C:\>New-AzRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Creating
```

<span data-ttu-id="b05ed-109">이 명령은 Redis Cache mycache1 및 mycache2 간에 지리적 복제 링크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b05ed-109">This command creates geo-replication link between Redis Cache mycache1 and mycache2.</span></span>

## <span data-ttu-id="b05ed-110">변수</span><span class="sxs-lookup"><span data-stu-id="b05ed-110">PARAMETERS</span></span>

### <span data-ttu-id="b05ed-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b05ed-111">-DefaultProfile</span></span>
<span data-ttu-id="b05ed-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b05ed-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b05ed-113">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="b05ed-113">-PrimaryServerName</span></span>
<span data-ttu-id="b05ed-114">Link의 기본 redis cache 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b05ed-114">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="b05ed-115">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="b05ed-115">-SecondaryServerName</span></span>
<span data-ttu-id="b05ed-116">Link의 보조 redis 캐시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b05ed-116">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="b05ed-117">-확인</span><span class="sxs-lookup"><span data-stu-id="b05ed-117">-Confirm</span></span>
<span data-ttu-id="b05ed-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b05ed-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b05ed-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b05ed-119">-WhatIf</span></span>
<span data-ttu-id="b05ed-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b05ed-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b05ed-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b05ed-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b05ed-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b05ed-122">CommonParameters</span></span>
<span data-ttu-id="b05ed-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b05ed-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b05ed-124">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b05ed-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b05ed-125">입력</span><span class="sxs-lookup"><span data-stu-id="b05ed-125">INPUTS</span></span>

### <span data-ttu-id="b05ed-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b05ed-126">System.String</span></span>

## <span data-ttu-id="b05ed-127">출력</span><span class="sxs-lookup"><span data-stu-id="b05ed-127">OUTPUTS</span></span>

### <span data-ttu-id="b05ed-128">PSRedisLinkedServer. 모델. m e.</span><span class="sxs-lookup"><span data-stu-id="b05ed-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span></span>

## <span data-ttu-id="b05ed-129">상속자</span><span class="sxs-lookup"><span data-stu-id="b05ed-129">NOTES</span></span>

## <span data-ttu-id="b05ed-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b05ed-130">RELATED LINKS</span></span>

[<span data-ttu-id="b05ed-131">Get-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="b05ed-131">Get-AzRedisCacheLink</span></span>](./Get-AzRedisCacheLink.md)

[<span data-ttu-id="b05ed-132">제거-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="b05ed-132">Remove-AzRedisCacheLink</span></span>](./Remove-AzRedisCacheLink.md)

[<span data-ttu-id="b05ed-133">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="b05ed-133">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="b05ed-134">새로운 AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="b05ed-134">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="b05ed-135">제거-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="b05ed-135">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="b05ed-136">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="b05ed-136">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)