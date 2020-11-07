---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: ACB53C23-99E0-4A0A-A44E-0D3FDB12450B
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachescheduleentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheScheduleEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheScheduleEntry.md
ms.openlocfilehash: e3976c1008388c85a04715541d0d88e164a422e9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93879169"
---
# <span data-ttu-id="87b56-101">New-AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="87b56-101">New-AzRedisCacheScheduleEntry</span></span>

## <span data-ttu-id="87b56-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87b56-102">SYNOPSIS</span></span>
<span data-ttu-id="87b56-103">일정 항목을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="87b56-103">Creates a schedule entry.</span></span>

## <span data-ttu-id="87b56-104">구문과</span><span class="sxs-lookup"><span data-stu-id="87b56-104">SYNTAX</span></span>

```
New-AzRedisCacheScheduleEntry -DayOfWeek <String> -StartHourUtc <Int32> [-MaintenanceWindow <TimeSpan>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87b56-105">설명은</span><span class="sxs-lookup"><span data-stu-id="87b56-105">DESCRIPTION</span></span>
<span data-ttu-id="87b56-106">**AzRedisCacheScheduleEntry** Cmdlet은 **PSScheduleEntry** 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="87b56-106">The **New-AzRedisCacheScheduleEntry** cmdlet creates a **PSScheduleEntry** object.</span></span>
<span data-ttu-id="87b56-107">Azure Redis 캐시 패치 예약 cmdlet (예: New-AzRedisCachePatchSchedule cmdlet)에는 일정 항목 개체가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="87b56-107">Azure Redis Cache patch schedule cmdlets, such as the New-AzRedisCachePatchSchedule cmdlet, require schedule entry objects.</span></span>

## <span data-ttu-id="87b56-108">예제의</span><span class="sxs-lookup"><span data-stu-id="87b56-108">EXAMPLES</span></span>

### <span data-ttu-id="87b56-109">예제 1: 주말 일정 항목 만들기</span><span class="sxs-lookup"><span data-stu-id="87b56-109">Example 1: Create a schedule entry for weekends</span></span>
```
PS C:\>New-AzRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00"
```

<span data-ttu-id="87b56-110">이 명령은 지정 된 시작 시간 및 윈도를 포함 하는 주말 일정을 나타내는 **PSScheduleEntry** 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="87b56-110">This command creates a **PSScheduleEntry** object that represents a weekend schedule that has the specified start time and window.</span></span>

## <span data-ttu-id="87b56-111">변수</span><span class="sxs-lookup"><span data-stu-id="87b56-111">PARAMETERS</span></span>

### <span data-ttu-id="87b56-112">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="87b56-112">-DayOfWeek</span></span>
<span data-ttu-id="87b56-113">일정 항목에 대 한 요일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="87b56-113">Specifies the day of the week for the schedule entry.</span></span>
<span data-ttu-id="87b56-114">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="87b56-114">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="87b56-115">매일</span><span class="sxs-lookup"><span data-stu-id="87b56-115">Everyday</span></span> 
- <span data-ttu-id="87b56-116">주말을</span><span class="sxs-lookup"><span data-stu-id="87b56-116">Weekend</span></span> 
- <span data-ttu-id="87b56-117">월요일</span><span class="sxs-lookup"><span data-stu-id="87b56-117">Monday</span></span> 
- <span data-ttu-id="87b56-118">시간은</span><span class="sxs-lookup"><span data-stu-id="87b56-118">Tuesday</span></span> 
- <span data-ttu-id="87b56-119">일</span><span class="sxs-lookup"><span data-stu-id="87b56-119">Wednesday</span></span> 
- <span data-ttu-id="87b56-120">목요일</span><span class="sxs-lookup"><span data-stu-id="87b56-120">Thursday</span></span> 
- <span data-ttu-id="87b56-121">금요일</span><span class="sxs-lookup"><span data-stu-id="87b56-121">Friday</span></span> 
- <span data-ttu-id="87b56-122">토요일</span><span class="sxs-lookup"><span data-stu-id="87b56-122">Saturday</span></span> 
- <span data-ttu-id="87b56-123">나타내고</span><span class="sxs-lookup"><span data-stu-id="87b56-123">Sunday</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Everyday, Weekend, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87b56-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87b56-124">-DefaultProfile</span></span>
<span data-ttu-id="87b56-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="87b56-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87b56-126">-MaintenanceWindow</span><span class="sxs-lookup"><span data-stu-id="87b56-126">-MaintenanceWindow</span></span>
<span data-ttu-id="87b56-127">업데이트에 허용 되는 시간 창 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="87b56-127">Specifies the amount of time window allowed for updates.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87b56-128">-StartHourUtc</span><span class="sxs-lookup"><span data-stu-id="87b56-128">-StartHourUtc</span></span>
<span data-ttu-id="87b56-129">일정이 시작 되는 시간 (일)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="87b56-129">Specifies an hour of the day when the schedule starts.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87b56-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87b56-130">CommonParameters</span></span>
<span data-ttu-id="87b56-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="87b56-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87b56-132">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87b56-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87b56-133">입력</span><span class="sxs-lookup"><span data-stu-id="87b56-133">INPUTS</span></span>

### <span data-ttu-id="87b56-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="87b56-134">System.String</span></span>

### <span data-ttu-id="87b56-135">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="87b56-135">System.Int32</span></span>

### <span data-ttu-id="87b56-136">시스템 Null 허용 ' 1 [[System. TimeSpan, CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="87b56-136">System.Nullable\`1[[System.TimeSpan, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="87b56-137">출력</span><span class="sxs-lookup"><span data-stu-id="87b56-137">OUTPUTS</span></span>

### <span data-ttu-id="87b56-138">PSScheduleEntry. 모델. m e.</span><span class="sxs-lookup"><span data-stu-id="87b56-138">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="87b56-139">상속자</span><span class="sxs-lookup"><span data-stu-id="87b56-139">NOTES</span></span>
* <span data-ttu-id="87b56-140">키워드: azure, azurerm, arm, resource, 관리, manager, redis, cache, web, web app, 웹 사이트</span><span class="sxs-lookup"><span data-stu-id="87b56-140">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="87b56-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="87b56-141">RELATED LINKS</span></span>

[<span data-ttu-id="87b56-142">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="87b56-142">Get-AzRedisCachePatchSchedule</span></span>](./Get-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="87b56-143">새로운 AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="87b56-143">New-AzRedisCachePatchSchedule</span></span>](./New-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="87b56-144">제거-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="87b56-144">Remove-AzRedisCachePatchSchedule</span></span>](./Remove-AzRedisCachePatchSchedule.md)


