---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/powershell/module/az.rediscache/remove-azrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheLink.md
ms.openlocfilehash: 2227f4fc9cd8128018160a3e62d9ba56bd664d8f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953088"
---
# <span data-ttu-id="6151b-101">Remove-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="6151b-101">Remove-AzRedisCacheLink</span></span>

## <span data-ttu-id="6151b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6151b-102">SYNOPSIS</span></span>
<span data-ttu-id="6151b-103">두 Redis Caches 간에 지역 복제 링크를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6151b-103">Remove a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="6151b-104">구문</span><span class="sxs-lookup"><span data-stu-id="6151b-104">SYNTAX</span></span>

```
Remove-AzRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6151b-105">설명</span><span class="sxs-lookup"><span data-stu-id="6151b-105">DESCRIPTION</span></span>
<span data-ttu-id="6151b-106">두 Redis Caches 간에 지역 복제 링크를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6151b-106">Remove a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="6151b-107">예제</span><span class="sxs-lookup"><span data-stu-id="6151b-107">EXAMPLES</span></span>

### <span data-ttu-id="6151b-108">예제 1: 지역 복제 링크 제거</span><span class="sxs-lookup"><span data-stu-id="6151b-108">Example 1: Remove a geo replication link</span></span>
```
PS C:\>Remove-AzRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"
```

<span data-ttu-id="6151b-109">이 명령은 mycache1이라는 Redis Cache가 기본이고 mycache2라는 Redis Cache가 보조인 지역 복제 링크를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6151b-109">This command removes a geo-replication links where Redis Cache named mycache1 is primary and Redis Cache named mycache2 is secondary.</span></span>

## <span data-ttu-id="6151b-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6151b-110">PARAMETERS</span></span>

### <span data-ttu-id="6151b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6151b-111">-DefaultProfile</span></span>
<span data-ttu-id="6151b-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6151b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6151b-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6151b-113">-PassThru</span></span>
<span data-ttu-id="6151b-114">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="6151b-114">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="6151b-115">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="6151b-115">-PrimaryServerName</span></span>
<span data-ttu-id="6151b-116">링크의 기본 redis 캐시의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6151b-116">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="6151b-117">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="6151b-117">-SecondaryServerName</span></span>
<span data-ttu-id="6151b-118">링크의 보조 redis 캐시의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6151b-118">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="6151b-119">-확인</span><span class="sxs-lookup"><span data-stu-id="6151b-119">-Confirm</span></span>
<span data-ttu-id="6151b-120">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6151b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6151b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6151b-121">-WhatIf</span></span>
<span data-ttu-id="6151b-122">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="6151b-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6151b-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6151b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6151b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6151b-124">CommonParameters</span></span>
<span data-ttu-id="6151b-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6151b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6151b-126">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6151b-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6151b-127">입력</span><span class="sxs-lookup"><span data-stu-id="6151b-127">INPUTS</span></span>

### <span data-ttu-id="6151b-128">System.String</span><span class="sxs-lookup"><span data-stu-id="6151b-128">System.String</span></span>

## <span data-ttu-id="6151b-129">출력</span><span class="sxs-lookup"><span data-stu-id="6151b-129">OUTPUTS</span></span>

### <span data-ttu-id="6151b-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6151b-130">System.Boolean</span></span>

## <span data-ttu-id="6151b-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6151b-131">NOTES</span></span>

## <span data-ttu-id="6151b-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6151b-132">RELATED LINKS</span></span>

[<span data-ttu-id="6151b-133">New-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="6151b-133">New-AzRedisCacheLink</span></span>](./New-AzRedisCacheLink.md)

[<span data-ttu-id="6151b-134">Get-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="6151b-134">Get-AzRedisCacheLink</span></span>](./Get-AzRedisCacheLink.md)

[<span data-ttu-id="6151b-135">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="6151b-135">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="6151b-136">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="6151b-136">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="6151b-137">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="6151b-137">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="6151b-138">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="6151b-138">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)