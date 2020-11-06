---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 1F86CE62-AA01-44FB-A935-484EC51DDE5A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscachekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheKey.md
ms.openlocfilehash: d54bc01e7a5aa23206037d4eb1d99e5d9e5deb0d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533335"
---
# <span data-ttu-id="df7d5-101">New-AzureRmRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="df7d5-101">New-AzureRmRedisCacheKey</span></span>

## <span data-ttu-id="df7d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df7d5-102">SYNOPSIS</span></span>
<span data-ttu-id="df7d5-103">Redis 캐시의 선택 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="df7d5-103">Regenerates the access key of a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df7d5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="df7d5-104">SYNTAX</span></span>

```
New-AzureRmRedisCacheKey [-ResourceGroupName <String>] -Name <String> -KeyType <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df7d5-105">설명은</span><span class="sxs-lookup"><span data-stu-id="df7d5-105">DESCRIPTION</span></span>
<span data-ttu-id="df7d5-106">**AzureRmRedisCacheKey** Cmdlet은 Azure Redis Cache의 선택 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="df7d5-106">The **New-AzureRmRedisCacheKey** cmdlet regenerates the access key of an Azure Redis Cache.</span></span>

## <span data-ttu-id="df7d5-107">예제의</span><span class="sxs-lookup"><span data-stu-id="df7d5-107">EXAMPLES</span></span>

### <span data-ttu-id="df7d5-108">예제 1: 기본 키 다시 생성</span><span class="sxs-lookup"><span data-stu-id="df7d5-108">Example 1: Regenerate a primary key</span></span>
```
PS C:\>New-AzureRmRedisCacheKey -ResourceGroupName "ResourceGroup03" -Name "myCache" -KeyType "Primary" -Force

          PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=

          SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="df7d5-109">이 명령은 Redis Cache의 기본 키를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="df7d5-109">This command regenerates the primary key of a Redis Cache.</span></span>

### <span data-ttu-id="df7d5-110">예제 2: 보조 키 다시 생성</span><span class="sxs-lookup"><span data-stu-id="df7d5-110">Example 2: Regenerate a secondary key</span></span>
```
PS C:\>New-AzureRmRedisCacheKey -ResourceGroupName "ResourceGroup03" -Name "myCache" -KeyType "Secondary" -Force
          PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=

          SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="df7d5-111">이 명령은 Redis Cache의 보조 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="df7d5-111">This command regenerates the secondary key of a Redis Cache.</span></span>

## <span data-ttu-id="df7d5-112">변수</span><span class="sxs-lookup"><span data-stu-id="df7d5-112">PARAMETERS</span></span>

### <span data-ttu-id="df7d5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df7d5-113">-DefaultProfile</span></span>
<span data-ttu-id="df7d5-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="df7d5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df7d5-115">-Force</span><span class="sxs-lookup"><span data-stu-id="df7d5-115">-Force</span></span>
<span data-ttu-id="df7d5-116">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="df7d5-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="df7d5-117">-KeyType</span><span class="sxs-lookup"><span data-stu-id="df7d5-117">-KeyType</span></span>
<span data-ttu-id="df7d5-118">기본 또는 보조 선택 키를 다시 생성할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="df7d5-118">Specifies whether to regenerate the primary or secondary access key.</span></span>
<span data-ttu-id="df7d5-119">유효한 값은 Primary, Secondary입니다.</span><span class="sxs-lookup"><span data-stu-id="df7d5-119">Valid values are: Primary, Secondary.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df7d5-120">-이름</span><span class="sxs-lookup"><span data-stu-id="df7d5-120">-Name</span></span>
<span data-ttu-id="df7d5-121">Redis 캐시의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="df7d5-121">Specifies the name of the Redis Cache.</span></span>

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

### <span data-ttu-id="df7d5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df7d5-122">-ResourceGroupName</span></span>
<span data-ttu-id="df7d5-123">Redis 캐시를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="df7d5-123">Specifies the name of the resource group that contains the Redis Cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df7d5-124">-확인</span><span class="sxs-lookup"><span data-stu-id="df7d5-124">-Confirm</span></span>
<span data-ttu-id="df7d5-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="df7d5-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df7d5-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df7d5-126">-WhatIf</span></span>
<span data-ttu-id="df7d5-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="df7d5-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df7d5-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="df7d5-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df7d5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df7d5-129">CommonParameters</span></span>
<span data-ttu-id="df7d5-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="df7d5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df7d5-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df7d5-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df7d5-132">입력</span><span class="sxs-lookup"><span data-stu-id="df7d5-132">INPUTS</span></span>

### <span data-ttu-id="df7d5-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="df7d5-133">System.String</span></span>

## <span data-ttu-id="df7d5-134">출력</span><span class="sxs-lookup"><span data-stu-id="df7d5-134">OUTPUTS</span></span>

### <span data-ttu-id="df7d5-135">Redis. RedisAccessKeys.</span><span class="sxs-lookup"><span data-stu-id="df7d5-135">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span></span>

## <span data-ttu-id="df7d5-136">상속자</span><span class="sxs-lookup"><span data-stu-id="df7d5-136">NOTES</span></span>

## <span data-ttu-id="df7d5-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="df7d5-137">RELATED LINKS</span></span>

[<span data-ttu-id="df7d5-138">Get-AzureRmRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="df7d5-138">Get-AzureRmRedisCacheKey</span></span>](./Get-AzureRmRedisCacheKey.md)


