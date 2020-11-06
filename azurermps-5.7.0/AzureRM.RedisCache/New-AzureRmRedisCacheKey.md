---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 1F86CE62-AA01-44FB-A935-484EC51DDE5A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscachekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheKey.md
ms.openlocfilehash: 51fff2f79435c6806b126fbc0a9c120ee8b8842e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524980"
---
# <span data-ttu-id="13303-101">New-AzureRmRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="13303-101">New-AzureRmRedisCacheKey</span></span>

## <span data-ttu-id="13303-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13303-102">SYNOPSIS</span></span>
<span data-ttu-id="13303-103">Redis 캐시의 선택 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="13303-103">Regenerates the access key of a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13303-104">구문과</span><span class="sxs-lookup"><span data-stu-id="13303-104">SYNTAX</span></span>

```
New-AzureRmRedisCacheKey [-ResourceGroupName <String>] -Name <String> -KeyType <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13303-105">설명은</span><span class="sxs-lookup"><span data-stu-id="13303-105">DESCRIPTION</span></span>
<span data-ttu-id="13303-106">**AzureRmRedisCacheKey** Cmdlet은 Azure Redis Cache의 선택 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="13303-106">The **New-AzureRmRedisCacheKey** cmdlet regenerates the access key of an Azure Redis Cache.</span></span>

## <span data-ttu-id="13303-107">예제의</span><span class="sxs-lookup"><span data-stu-id="13303-107">EXAMPLES</span></span>

### <span data-ttu-id="13303-108">예제 1: 기본 키 다시 생성</span><span class="sxs-lookup"><span data-stu-id="13303-108">Example 1: Regenerate a primary key</span></span>
```
PS C:\>New-AzureRmRedisCacheKey -ResourceGroupName "ResourceGroup03" -Name "myCache" -KeyType "Primary" -Force

          PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=

          SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="13303-109">이 명령은 Redis Cache의 기본 키를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="13303-109">This command regenerates the primary key of a Redis Cache.</span></span>

### <span data-ttu-id="13303-110">예제 2: 보조 키 다시 생성</span><span class="sxs-lookup"><span data-stu-id="13303-110">Example 2: Regenerate a secondary key</span></span>
```
PS C:\>New-AzureRmRedisCacheKey -ResourceGroupName "ResourceGroup03" -Name "myCache" -KeyType "Secondary" -Force
          PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=

          SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="13303-111">이 명령은 Redis Cache의 보조 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="13303-111">This command regenerates the secondary key of a Redis Cache.</span></span>

## <span data-ttu-id="13303-112">변수</span><span class="sxs-lookup"><span data-stu-id="13303-112">PARAMETERS</span></span>

### <span data-ttu-id="13303-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13303-113">-DefaultProfile</span></span>
<span data-ttu-id="13303-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="13303-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13303-115">-Force</span><span class="sxs-lookup"><span data-stu-id="13303-115">-Force</span></span>
<span data-ttu-id="13303-116">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="13303-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="13303-117">-KeyType</span><span class="sxs-lookup"><span data-stu-id="13303-117">-KeyType</span></span>
<span data-ttu-id="13303-118">기본 또는 보조 선택 키를 다시 생성할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="13303-118">Specifies whether to regenerate the primary or secondary access key.</span></span>
<span data-ttu-id="13303-119">유효한 값은 Primary, Secondary입니다.</span><span class="sxs-lookup"><span data-stu-id="13303-119">Valid values are: Primary, Secondary.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13303-120">-이름</span><span class="sxs-lookup"><span data-stu-id="13303-120">-Name</span></span>
<span data-ttu-id="13303-121">Redis 캐시의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="13303-121">Specifies the name of the Redis Cache.</span></span>

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

### <span data-ttu-id="13303-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13303-122">-ResourceGroupName</span></span>
<span data-ttu-id="13303-123">Redis 캐시를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="13303-123">Specifies the name of the resource group that contains the Redis Cache.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13303-124">-확인</span><span class="sxs-lookup"><span data-stu-id="13303-124">-Confirm</span></span>
<span data-ttu-id="13303-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="13303-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13303-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13303-126">-WhatIf</span></span>
<span data-ttu-id="13303-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="13303-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13303-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="13303-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13303-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13303-129">CommonParameters</span></span>
<span data-ttu-id="13303-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="13303-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13303-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13303-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13303-132">입력</span><span class="sxs-lookup"><span data-stu-id="13303-132">INPUTS</span></span>

### <span data-ttu-id="13303-133">않아야</span><span class="sxs-lookup"><span data-stu-id="13303-133">None</span></span>
<span data-ttu-id="13303-134">이름으로이 cmdlet에 대 한 입력을 파이프 할 수 있지만 값을 기준으로 하지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="13303-134">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="13303-135">출력</span><span class="sxs-lookup"><span data-stu-id="13303-135">OUTPUTS</span></span>

### <span data-ttu-id="13303-136">Redis. RedisAccessKeys.</span><span class="sxs-lookup"><span data-stu-id="13303-136">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span></span>
<span data-ttu-id="13303-137">이 cmdlet은 Redis Cache의 기본 및 보조 선택 키를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="13303-137">This cmdlet returns the primary and secondary access key of a Redis Cache.</span></span>

## <span data-ttu-id="13303-138">상속자</span><span class="sxs-lookup"><span data-stu-id="13303-138">NOTES</span></span>

## <span data-ttu-id="13303-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="13303-139">RELATED LINKS</span></span>

[<span data-ttu-id="13303-140">Get-AzureRmRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="13303-140">Get-AzureRmRedisCacheKey</span></span>](./Get-AzureRmRedisCacheKey.md)


