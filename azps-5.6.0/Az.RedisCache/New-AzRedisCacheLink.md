---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/powershell/module/az.rediscache/new-azrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheLink.md
ms.openlocfilehash: 41a2172fffdbd83edc8ab72a4fe922d600362731
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972704"
---
# <span data-ttu-id="4efaa-101">New-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="4efaa-101">New-AzRedisCacheLink</span></span>

## <span data-ttu-id="4efaa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4efaa-102">SYNOPSIS</span></span>
<span data-ttu-id="4efaa-103">두 Redis Caches 간에 지역 복제 링크를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="4efaa-103">Create a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="4efaa-104">구문</span><span class="sxs-lookup"><span data-stu-id="4efaa-104">SYNTAX</span></span>

```
New-AzRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4efaa-105">설명</span><span class="sxs-lookup"><span data-stu-id="4efaa-105">DESCRIPTION</span></span>
<span data-ttu-id="4efaa-106">두 Redis Caches 간에 지역 복제 링크를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="4efaa-106">Create a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="4efaa-107">예제</span><span class="sxs-lookup"><span data-stu-id="4efaa-107">EXAMPLES</span></span>

### <span data-ttu-id="4efaa-108">예제 1: 두 캐시 간에 링크 만들기</span><span class="sxs-lookup"><span data-stu-id="4efaa-108">Example 1: Create a link between two caches</span></span>
```
PS C:\>New-AzRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Creating
```

<span data-ttu-id="4efaa-109">이 명령은 Redis Cache mycache1과 mycache2 간에 지역 복제 링크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4efaa-109">This command creates geo-replication link between Redis Cache mycache1 and mycache2.</span></span>

## <span data-ttu-id="4efaa-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="4efaa-110">PARAMETERS</span></span>

### <span data-ttu-id="4efaa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4efaa-111">-DefaultProfile</span></span>
<span data-ttu-id="4efaa-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4efaa-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4efaa-113">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="4efaa-113">-PrimaryServerName</span></span>
<span data-ttu-id="4efaa-114">링크의 기본 redis 캐시의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4efaa-114">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="4efaa-115">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="4efaa-115">-SecondaryServerName</span></span>
<span data-ttu-id="4efaa-116">링크의 보조 redis 캐시의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4efaa-116">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="4efaa-117">-확인</span><span class="sxs-lookup"><span data-stu-id="4efaa-117">-Confirm</span></span>
<span data-ttu-id="4efaa-118">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4efaa-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4efaa-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4efaa-119">-WhatIf</span></span>
<span data-ttu-id="4efaa-120">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="4efaa-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4efaa-121">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4efaa-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4efaa-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4efaa-122">CommonParameters</span></span>
<span data-ttu-id="4efaa-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4efaa-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4efaa-124">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4efaa-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4efaa-125">입력</span><span class="sxs-lookup"><span data-stu-id="4efaa-125">INPUTS</span></span>

### <span data-ttu-id="4efaa-126">System.String</span><span class="sxs-lookup"><span data-stu-id="4efaa-126">System.String</span></span>

## <span data-ttu-id="4efaa-127">출력</span><span class="sxs-lookup"><span data-stu-id="4efaa-127">OUTPUTS</span></span>

### <span data-ttu-id="4efaa-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span><span class="sxs-lookup"><span data-stu-id="4efaa-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span></span>

## <span data-ttu-id="4efaa-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4efaa-129">NOTES</span></span>

## <span data-ttu-id="4efaa-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4efaa-130">RELATED LINKS</span></span>

[<span data-ttu-id="4efaa-131">Get-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="4efaa-131">Get-AzRedisCacheLink</span></span>](./Get-AzRedisCacheLink.md)

[<span data-ttu-id="4efaa-132">Remove-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="4efaa-132">Remove-AzRedisCacheLink</span></span>](./Remove-AzRedisCacheLink.md)

[<span data-ttu-id="4efaa-133">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="4efaa-133">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="4efaa-134">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="4efaa-134">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="4efaa-135">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="4efaa-135">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="4efaa-136">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="4efaa-136">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)