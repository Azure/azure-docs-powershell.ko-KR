---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheLink.md
ms.openlocfilehash: 38c72a19e73d87272fb91fb6472a41496658e7d6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183793"
---
# <span data-ttu-id="2f5ce-101">Remove-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="2f5ce-101">Remove-AzRedisCacheLink</span></span>

## <span data-ttu-id="2f5ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f5ce-102">SYNOPSIS</span></span>
<span data-ttu-id="2f5ce-103">두 Redis Cache 간에 지역 복제 링크를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="2f5ce-103">Remove a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="2f5ce-104">구문</span><span class="sxs-lookup"><span data-stu-id="2f5ce-104">SYNTAX</span></span>

```
Remove-AzRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f5ce-105">설명</span><span class="sxs-lookup"><span data-stu-id="2f5ce-105">DESCRIPTION</span></span>
<span data-ttu-id="2f5ce-106">두 Redis Cache 간에 지역 복제 링크를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="2f5ce-106">Remove a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="2f5ce-107">예제</span><span class="sxs-lookup"><span data-stu-id="2f5ce-107">EXAMPLES</span></span>

### <span data-ttu-id="2f5ce-108">예제 1: 지역 복제 링크 제거</span><span class="sxs-lookup"><span data-stu-id="2f5ce-108">Example 1: Remove a geo replication link</span></span>
```
PS C:\>Remove-AzRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"
```

<span data-ttu-id="2f5ce-109">이 명령은 mycache1이라는 Redis Cache가 기본이고 mycache2라는 Redis Cache가 보조인 지역 복제 링크를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="2f5ce-109">This command removes a geo-replication links where Redis Cache named mycache1 is primary and Redis Cache named mycache2 is secondary.</span></span>

## <span data-ttu-id="2f5ce-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2f5ce-110">PARAMETERS</span></span>

### <span data-ttu-id="2f5ce-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f5ce-111">-DefaultProfile</span></span>
<span data-ttu-id="2f5ce-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2f5ce-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f5ce-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2f5ce-113">-PassThru</span></span>
<span data-ttu-id="2f5ce-114">{{PassThru 설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="2f5ce-114">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="2f5ce-115">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="2f5ce-115">-PrimaryServerName</span></span>
<span data-ttu-id="2f5ce-116">링크에 있는 기본 redis Cache의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2f5ce-116">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="2f5ce-117">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="2f5ce-117">-SecondaryServerName</span></span>
<span data-ttu-id="2f5ce-118">링크에 있는 보조 Redis Cache의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2f5ce-118">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="2f5ce-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2f5ce-119">-Confirm</span></span>
<span data-ttu-id="2f5ce-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2f5ce-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f5ce-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f5ce-121">-WhatIf</span></span>
<span data-ttu-id="2f5ce-122">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="2f5ce-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f5ce-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2f5ce-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f5ce-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f5ce-124">CommonParameters</span></span>
<span data-ttu-id="2f5ce-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2f5ce-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f5ce-126">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="2f5ce-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f5ce-127">입력</span><span class="sxs-lookup"><span data-stu-id="2f5ce-127">INPUTS</span></span>

### <span data-ttu-id="2f5ce-128">System.String</span><span class="sxs-lookup"><span data-stu-id="2f5ce-128">System.String</span></span>

## <span data-ttu-id="2f5ce-129">출력</span><span class="sxs-lookup"><span data-stu-id="2f5ce-129">OUTPUTS</span></span>

### <span data-ttu-id="2f5ce-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2f5ce-130">System.Boolean</span></span>

## <span data-ttu-id="2f5ce-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2f5ce-131">NOTES</span></span>

## <span data-ttu-id="2f5ce-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2f5ce-132">RELATED LINKS</span></span>

[<span data-ttu-id="2f5ce-133">New-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="2f5ce-133">New-AzRedisCacheLink</span></span>](./New-AzRedisCacheLink.md)

[<span data-ttu-id="2f5ce-134">Get-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="2f5ce-134">Get-AzRedisCacheLink</span></span>](./Get-AzRedisCacheLink.md)

[<span data-ttu-id="2f5ce-135">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="2f5ce-135">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="2f5ce-136">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="2f5ce-136">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="2f5ce-137">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="2f5ce-137">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="2f5ce-138">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="2f5ce-138">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)