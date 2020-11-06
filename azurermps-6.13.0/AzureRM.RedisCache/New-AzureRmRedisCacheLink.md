---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheLink.md
ms.openlocfilehash: f625c9180287166b01607c468c44b5e0623c11cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524304"
---
# <span data-ttu-id="eba85-101">New-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="eba85-101">New-AzureRmRedisCacheLink</span></span>

## <span data-ttu-id="eba85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eba85-102">SYNOPSIS</span></span>
<span data-ttu-id="eba85-103">두 Redis 캐시 간에 지역 복제 링크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="eba85-103">Create a geo replication link between two Redis Caches.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eba85-104">구문과</span><span class="sxs-lookup"><span data-stu-id="eba85-104">SYNTAX</span></span>

```
New-AzureRmRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eba85-105">설명은</span><span class="sxs-lookup"><span data-stu-id="eba85-105">DESCRIPTION</span></span>
<span data-ttu-id="eba85-106">두 Redis 캐시 간에 지역 복제 링크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="eba85-106">Create a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="eba85-107">예제의</span><span class="sxs-lookup"><span data-stu-id="eba85-107">EXAMPLES</span></span>

### <span data-ttu-id="eba85-108">예제 1: 두 캐시 간에 링크 만들기</span><span class="sxs-lookup"><span data-stu-id="eba85-108">Example 1: Create a link between two caches</span></span>
```
PS C:\>New-AzureRmRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Creating
```

<span data-ttu-id="eba85-109">이 명령은 Redis Cache mycache1 및 mycache2 간에 지리적 복제 링크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="eba85-109">This command creates geo-replication link between Redis Cache mycache1 and mycache2.</span></span>

## <span data-ttu-id="eba85-110">변수</span><span class="sxs-lookup"><span data-stu-id="eba85-110">PARAMETERS</span></span>

### <span data-ttu-id="eba85-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eba85-111">-DefaultProfile</span></span>
<span data-ttu-id="eba85-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="eba85-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eba85-113">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="eba85-113">-PrimaryServerName</span></span>
<span data-ttu-id="eba85-114">Link의 기본 redis cache 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="eba85-114">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="eba85-115">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="eba85-115">-SecondaryServerName</span></span>
<span data-ttu-id="eba85-116">Link의 보조 redis 캐시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="eba85-116">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="eba85-117">-확인</span><span class="sxs-lookup"><span data-stu-id="eba85-117">-Confirm</span></span>
<span data-ttu-id="eba85-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="eba85-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eba85-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eba85-119">-WhatIf</span></span>
<span data-ttu-id="eba85-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="eba85-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eba85-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eba85-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eba85-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eba85-122">CommonParameters</span></span>
<span data-ttu-id="eba85-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="eba85-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eba85-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eba85-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eba85-125">입력</span><span class="sxs-lookup"><span data-stu-id="eba85-125">INPUTS</span></span>

### <span data-ttu-id="eba85-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="eba85-126">System.String</span></span>

## <span data-ttu-id="eba85-127">출력</span><span class="sxs-lookup"><span data-stu-id="eba85-127">OUTPUTS</span></span>

### <span data-ttu-id="eba85-128">PSRedisLinkedServer. 모델. m e.</span><span class="sxs-lookup"><span data-stu-id="eba85-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span></span>

## <span data-ttu-id="eba85-129">상속자</span><span class="sxs-lookup"><span data-stu-id="eba85-129">NOTES</span></span>

## <span data-ttu-id="eba85-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="eba85-130">RELATED LINKS</span></span>

[<span data-ttu-id="eba85-131">Get-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="eba85-131">Get-AzureRmRedisCacheLink</span></span>](./Get-AzureRmRedisCacheLink.md)

[<span data-ttu-id="eba85-132">제거-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="eba85-132">Remove-AzureRmRedisCacheLink</span></span>](./Remove-AzureRmRedisCacheLink.md)

[<span data-ttu-id="eba85-133">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="eba85-133">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="eba85-134">새로운 AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="eba85-134">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="eba85-135">제거-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="eba85-135">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="eba85-136">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="eba85-136">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)
