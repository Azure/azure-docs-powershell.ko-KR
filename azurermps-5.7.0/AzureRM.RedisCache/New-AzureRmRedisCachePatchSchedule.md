---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: F7FAFF52-5E07-4D88-B48F-BC70C43E8691
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCachePatchSchedule.md
ms.openlocfilehash: 5c4375b4bb325877ec0520e0641496e8adfafec0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524975"
---
# <span data-ttu-id="70315-101">New-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="70315-101">New-AzureRmRedisCachePatchSchedule</span></span>

## <span data-ttu-id="70315-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70315-102">SYNOPSIS</span></span>
<span data-ttu-id="70315-103">패치 일정을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="70315-103">Adds a patch schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="70315-104">구문과</span><span class="sxs-lookup"><span data-stu-id="70315-104">SYNTAX</span></span>

```
New-AzureRmRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String> -Entries <PSScheduleEntry[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70315-105">설명은</span><span class="sxs-lookup"><span data-stu-id="70315-105">DESCRIPTION</span></span>
<span data-ttu-id="70315-106">**AzureRmRedisCachePatchSchedule** Cmdlet은 Azure Redis cache의 캐시에 패치 일정을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="70315-106">The **New-AzureRmRedisCachePatchSchedule** cmdlet adds a patch schedule to a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="70315-107">예제의</span><span class="sxs-lookup"><span data-stu-id="70315-107">EXAMPLES</span></span>

### <span data-ttu-id="70315-108">예제 1: 캐시에서 패치 일정 만들기 및 추가</span><span class="sxs-lookup"><span data-stu-id="70315-108">Example 1: Create and add a patch schedule on a cache</span></span>
```
PS C:\>New-AzureRmRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Entries @(New-AzureRmRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00")
```

<span data-ttu-id="70315-109">이 명령은 패치 일정을 RedisCache06 이라는 캐시에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="70315-109">This command adds a patch schedule to the cache named RedisCache06.</span></span>
<span data-ttu-id="70315-110">Entries 매개 변수는 **New-AzureRmRedisCacheScheduleEntry** 를 사용 하 여 일정을 만드는 명령 값으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="70315-110">The Entries parameter takes as its value a command that uses **New-AzureRmRedisCacheScheduleEntry** to create a schedule.</span></span>

## <span data-ttu-id="70315-111">변수</span><span class="sxs-lookup"><span data-stu-id="70315-111">PARAMETERS</span></span>

### <span data-ttu-id="70315-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70315-112">-DefaultProfile</span></span>
<span data-ttu-id="70315-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="70315-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70315-114">-항목</span><span class="sxs-lookup"><span data-stu-id="70315-114">-Entries</span></span>
<span data-ttu-id="70315-115">이 cmdlet이 캐시에 설정 하는 일정의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="70315-115">Specifies an array of schedules that this cmdlet sets on a cache.</span></span> <span data-ttu-id="70315-116">**PSScheduleEntry** 개체를 가져오려면 New-AzureRmRedisCacheScheduleEntry cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="70315-116">To obtain a **PSScheduleEntry** object, use the New-AzureRmRedisCacheScheduleEntry cmdlet.</span></span>

```yaml
Type: PSScheduleEntry[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70315-117">-이름</span><span class="sxs-lookup"><span data-stu-id="70315-117">-Name</span></span>
<span data-ttu-id="70315-118">캐시의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="70315-118">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="70315-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70315-119">-ResourceGroupName</span></span>
<span data-ttu-id="70315-120">캐시를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="70315-120">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="70315-121">-확인</span><span class="sxs-lookup"><span data-stu-id="70315-121">-Confirm</span></span>
<span data-ttu-id="70315-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="70315-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70315-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70315-123">-WhatIf</span></span>
<span data-ttu-id="70315-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="70315-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="70315-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="70315-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70315-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70315-126">CommonParameters</span></span>
<span data-ttu-id="70315-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="70315-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70315-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70315-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70315-129">입력</span><span class="sxs-lookup"><span data-stu-id="70315-129">INPUTS</span></span>

### <span data-ttu-id="70315-130">않아야</span><span class="sxs-lookup"><span data-stu-id="70315-130">None</span></span>
<span data-ttu-id="70315-131">속성 이름으로이 cmdlet에 대 한 입력을 파이프로 지정할 수 있지만 값을 기준으로 하지 않아도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="70315-131">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="70315-132">출력</span><span class="sxs-lookup"><span data-stu-id="70315-132">OUTPUTS</span></span>

### <span data-ttu-id="70315-133">PSScheduleEntry. 모델. m e.</span><span class="sxs-lookup"><span data-stu-id="70315-133">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>
<span data-ttu-id="70315-134">이 cmdlet은 캐시에 설정 된 패치 일정 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="70315-134">This cmdlet returns the of patch schedule entries set on the cache.</span></span>

## <span data-ttu-id="70315-135">상속자</span><span class="sxs-lookup"><span data-stu-id="70315-135">NOTES</span></span>
* <span data-ttu-id="70315-136">키워드: azure, azurerm, arm, resource, 관리, manager, redis, cache, web, web app, 웹 사이트</span><span class="sxs-lookup"><span data-stu-id="70315-136">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="70315-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="70315-137">RELATED LINKS</span></span>

[<span data-ttu-id="70315-138">Get-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="70315-138">Get-AzureRmRedisCachePatchSchedule</span></span>](./Get-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="70315-139">새로운 AzureRmRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="70315-139">New-AzureRmRedisCacheScheduleEntry</span></span>](./New-AzureRmRedisCacheScheduleEntry.md)

[<span data-ttu-id="70315-140">제거-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="70315-140">Remove-AzureRmRedisCachePatchSchedule</span></span>](./Remove-AzureRmRedisCachePatchSchedule.md)


