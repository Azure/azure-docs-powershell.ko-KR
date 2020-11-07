---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheLink.md
ms.openlocfilehash: 157490da6abeae7e947c22e88301d29043722a86
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873458"
---
# <span data-ttu-id="1f72d-101">New-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="1f72d-101">New-AzRedisCacheLink</span></span>

## <span data-ttu-id="1f72d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f72d-102">SYNOPSIS</span></span>
<span data-ttu-id="1f72d-103">두 Redis 캐시 간에 지역 복제 링크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1f72d-103">Create a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="1f72d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1f72d-104">SYNTAX</span></span>

```
New-AzRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f72d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1f72d-105">DESCRIPTION</span></span>
<span data-ttu-id="1f72d-106">두 Redis 캐시 간에 지역 복제 링크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1f72d-106">Create a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="1f72d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1f72d-107">EXAMPLES</span></span>

### <span data-ttu-id="1f72d-108">예제 1: 두 캐시 간에 링크 만들기</span><span class="sxs-lookup"><span data-stu-id="1f72d-108">Example 1: Create a link between two caches</span></span>
```
PS C:\>New-AzRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Creating
```

<span data-ttu-id="1f72d-109">이 명령은 Redis Cache mycache1 및 mycache2 간에 지리적 복제 링크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1f72d-109">This command creates geo-replication link between Redis Cache mycache1 and mycache2.</span></span>

## <span data-ttu-id="1f72d-110">변수</span><span class="sxs-lookup"><span data-stu-id="1f72d-110">PARAMETERS</span></span>

### <span data-ttu-id="1f72d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f72d-111">-DefaultProfile</span></span>
<span data-ttu-id="1f72d-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1f72d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f72d-113">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="1f72d-113">-PrimaryServerName</span></span>
<span data-ttu-id="1f72d-114">Link의 기본 redis cache 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1f72d-114">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="1f72d-115">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="1f72d-115">-SecondaryServerName</span></span>
<span data-ttu-id="1f72d-116">Link의 보조 redis 캐시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1f72d-116">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="1f72d-117">-확인</span><span class="sxs-lookup"><span data-stu-id="1f72d-117">-Confirm</span></span>
<span data-ttu-id="1f72d-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f72d-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f72d-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f72d-119">-WhatIf</span></span>
<span data-ttu-id="1f72d-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1f72d-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f72d-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1f72d-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f72d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f72d-122">CommonParameters</span></span>
<span data-ttu-id="1f72d-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f72d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f72d-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f72d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f72d-125">입력</span><span class="sxs-lookup"><span data-stu-id="1f72d-125">INPUTS</span></span>

### <span data-ttu-id="1f72d-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1f72d-126">System.String</span></span>

## <span data-ttu-id="1f72d-127">출력</span><span class="sxs-lookup"><span data-stu-id="1f72d-127">OUTPUTS</span></span>

### <span data-ttu-id="1f72d-128">PSRedisLinkedServer. 모델. m e.</span><span class="sxs-lookup"><span data-stu-id="1f72d-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span></span>

## <span data-ttu-id="1f72d-129">상속자</span><span class="sxs-lookup"><span data-stu-id="1f72d-129">NOTES</span></span>

## <span data-ttu-id="1f72d-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1f72d-130">RELATED LINKS</span></span>

[<span data-ttu-id="1f72d-131">Get-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="1f72d-131">Get-AzRedisCacheLink</span></span>](./Get-AzRedisCacheLink.md)

[<span data-ttu-id="1f72d-132">제거-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="1f72d-132">Remove-AzRedisCacheLink</span></span>](./Remove-AzRedisCacheLink.md)

[<span data-ttu-id="1f72d-133">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="1f72d-133">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="1f72d-134">새로운 AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="1f72d-134">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="1f72d-135">제거-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="1f72d-135">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="1f72d-136">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="1f72d-136">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)