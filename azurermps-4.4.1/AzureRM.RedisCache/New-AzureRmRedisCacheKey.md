---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 1F86CE62-AA01-44FB-A935-484EC51DDE5A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheKey.md
ms.openlocfilehash: b453b47da35addb8a04a19957c148c5ec1929e75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529188"
---
# <span data-ttu-id="01c6a-101">New-AzureRmRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="01c6a-101">New-AzureRmRedisCacheKey</span></span>

## <span data-ttu-id="01c6a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01c6a-102">SYNOPSIS</span></span>
<span data-ttu-id="01c6a-103">Redis 캐시의 선택 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="01c6a-103">Regenerates the access key of a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01c6a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="01c6a-104">SYNTAX</span></span>

```
New-AzureRmRedisCacheKey -ResourceGroupName <String> -Name <String> -KeyType <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01c6a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="01c6a-105">DESCRIPTION</span></span>
<span data-ttu-id="01c6a-106">**AzureRmRedisCacheKey** Cmdlet은 Azure Redis Cache의 선택 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="01c6a-106">The **New-AzureRmRedisCacheKey** cmdlet regenerates the access key of an Azure Redis Cache.</span></span>

## <span data-ttu-id="01c6a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="01c6a-107">EXAMPLES</span></span>

### <span data-ttu-id="01c6a-108">예제 1: 기본 키 다시 생성</span><span class="sxs-lookup"><span data-stu-id="01c6a-108">Example 1: Regenerate a primary key</span></span>
```
PS C:\>New-AzureRmRedisCacheKey -ResourceGroupName "ResourceGroup03" -Name "myCache" -KeyType "Primary" -Force

          PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=

          SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="01c6a-109">이 명령은 Redis Cache의 기본 키를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="01c6a-109">This command regenerates the primary key of a Redis Cache.</span></span>

### <span data-ttu-id="01c6a-110">예제 2: 보조 키 다시 생성</span><span class="sxs-lookup"><span data-stu-id="01c6a-110">Example 2: Regenerate a secondary key</span></span>
```
PS C:\>New-AzureRmRedisCacheKey -ResourceGroupName "ResourceGroup03" -Name "myCache" -KeyType "Secondary" -Force
          PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=

          SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="01c6a-111">이 명령은 Redis Cache의 보조 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="01c6a-111">This command regenerates the secondary key of a Redis Cache.</span></span>

## <span data-ttu-id="01c6a-112">변수</span><span class="sxs-lookup"><span data-stu-id="01c6a-112">PARAMETERS</span></span>

### <span data-ttu-id="01c6a-113">-Force</span><span class="sxs-lookup"><span data-stu-id="01c6a-113">-Force</span></span>
<span data-ttu-id="01c6a-114">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="01c6a-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="01c6a-115">-KeyType</span><span class="sxs-lookup"><span data-stu-id="01c6a-115">-KeyType</span></span>
<span data-ttu-id="01c6a-116">기본 또는 보조 선택 키를 다시 생성할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="01c6a-116">Specifies whether to regenerate the primary or secondary access key.</span></span>
<span data-ttu-id="01c6a-117">유효한 값은 Primary, Secondary입니다.</span><span class="sxs-lookup"><span data-stu-id="01c6a-117">Valid values are: Primary, Secondary.</span></span>

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

### <span data-ttu-id="01c6a-118">-이름</span><span class="sxs-lookup"><span data-stu-id="01c6a-118">-Name</span></span>
<span data-ttu-id="01c6a-119">Redis 캐시의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="01c6a-119">Specifies the name of the Redis Cache.</span></span>

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

### <span data-ttu-id="01c6a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01c6a-120">-ResourceGroupName</span></span>
<span data-ttu-id="01c6a-121">Redis 캐시를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="01c6a-121">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="01c6a-122">-확인</span><span class="sxs-lookup"><span data-stu-id="01c6a-122">-Confirm</span></span>
<span data-ttu-id="01c6a-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="01c6a-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01c6a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01c6a-124">-WhatIf</span></span>
<span data-ttu-id="01c6a-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="01c6a-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01c6a-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="01c6a-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01c6a-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01c6a-127">-DefaultProfile</span></span>
<span data-ttu-id="01c6a-128">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="01c6a-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01c6a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01c6a-129">CommonParameters</span></span>
<span data-ttu-id="01c6a-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="01c6a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01c6a-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01c6a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01c6a-132">입력</span><span class="sxs-lookup"><span data-stu-id="01c6a-132">INPUTS</span></span>

### <span data-ttu-id="01c6a-133">않아야</span><span class="sxs-lookup"><span data-stu-id="01c6a-133">None</span></span>
<span data-ttu-id="01c6a-134">이름으로이 cmdlet에 대 한 입력을 파이프 할 수 있지만 값을 기준으로 하지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="01c6a-134">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="01c6a-135">출력</span><span class="sxs-lookup"><span data-stu-id="01c6a-135">OUTPUTS</span></span>

### <span data-ttu-id="01c6a-136">Redis. RedisAccessKeys.</span><span class="sxs-lookup"><span data-stu-id="01c6a-136">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span></span>
<span data-ttu-id="01c6a-137">이 cmdlet은 Redis Cache의 기본 및 보조 선택 키를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="01c6a-137">This cmdlet returns the primary and secondary access key of a Redis Cache.</span></span>

## <span data-ttu-id="01c6a-138">상속자</span><span class="sxs-lookup"><span data-stu-id="01c6a-138">NOTES</span></span>

## <span data-ttu-id="01c6a-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="01c6a-139">RELATED LINKS</span></span>

[<span data-ttu-id="01c6a-140">Get-AzureRmRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="01c6a-140">Get-AzureRmRedisCacheKey</span></span>](./Get-AzureRmRedisCacheKey.md)


