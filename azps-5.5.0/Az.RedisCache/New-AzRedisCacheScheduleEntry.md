---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: ACB53C23-99E0-4A0A-A44E-0D3FDB12450B
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachescheduleentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheScheduleEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheScheduleEntry.md
ms.openlocfilehash: e3976c1008388c85a04715541d0d88e164a422e9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206128"
---
# <span data-ttu-id="7c2e5-101">New-AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="7c2e5-101">New-AzRedisCacheScheduleEntry</span></span>

## <span data-ttu-id="7c2e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c2e5-102">SYNOPSIS</span></span>
<span data-ttu-id="7c2e5-103">일정 항목을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7c2e5-103">Creates a schedule entry.</span></span>

## <span data-ttu-id="7c2e5-104">구문</span><span class="sxs-lookup"><span data-stu-id="7c2e5-104">SYNTAX</span></span>

```
New-AzRedisCacheScheduleEntry -DayOfWeek <String> -StartHourUtc <Int32> [-MaintenanceWindow <TimeSpan>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c2e5-105">설명</span><span class="sxs-lookup"><span data-stu-id="7c2e5-105">DESCRIPTION</span></span>
<span data-ttu-id="7c2e5-106">**New-AzRedisCacheScheduleEntry** cmdlet은 **PSScheduleEntry 개체를** 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7c2e5-106">The **New-AzRedisCacheScheduleEntry** cmdlet creates a **PSScheduleEntry** object.</span></span>
<span data-ttu-id="7c2e5-107">Azure Redis Cache 패치 일정 cmdlet(예: New-AzRedisCachePatchSchedule cmdlet)에는 일정 항목 개체가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c2e5-107">Azure Redis Cache patch schedule cmdlets, such as the New-AzRedisCachePatchSchedule cmdlet, require schedule entry objects.</span></span>

## <span data-ttu-id="7c2e5-108">예제</span><span class="sxs-lookup"><span data-stu-id="7c2e5-108">EXAMPLES</span></span>

### <span data-ttu-id="7c2e5-109">예제 1: 주말에 대한 일정 항목 만들기</span><span class="sxs-lookup"><span data-stu-id="7c2e5-109">Example 1: Create a schedule entry for weekends</span></span>
```
PS C:\>New-AzRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00"
```

<span data-ttu-id="7c2e5-110">이 명령은 지정된 시작 시간 및 창이 있는 주말 일정을 나타내는 **PSScheduleEntry** 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7c2e5-110">This command creates a **PSScheduleEntry** object that represents a weekend schedule that has the specified start time and window.</span></span>

## <span data-ttu-id="7c2e5-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7c2e5-111">PARAMETERS</span></span>

### <span data-ttu-id="7c2e5-112">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="7c2e5-112">-DayOfWeek</span></span>
<span data-ttu-id="7c2e5-113">일정 항목에 대한 주중 날을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7c2e5-113">Specifies the day of the week for the schedule entry.</span></span>
<span data-ttu-id="7c2e5-114">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="7c2e5-114">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7c2e5-115">매일</span><span class="sxs-lookup"><span data-stu-id="7c2e5-115">Everyday</span></span> 
- <span data-ttu-id="7c2e5-116">주말</span><span class="sxs-lookup"><span data-stu-id="7c2e5-116">Weekend</span></span> 
- <span data-ttu-id="7c2e5-117">월요일</span><span class="sxs-lookup"><span data-stu-id="7c2e5-117">Monday</span></span> 
- <span data-ttu-id="7c2e5-118">화요일</span><span class="sxs-lookup"><span data-stu-id="7c2e5-118">Tuesday</span></span> 
- <span data-ttu-id="7c2e5-119">수요일</span><span class="sxs-lookup"><span data-stu-id="7c2e5-119">Wednesday</span></span> 
- <span data-ttu-id="7c2e5-120">목요일</span><span class="sxs-lookup"><span data-stu-id="7c2e5-120">Thursday</span></span> 
- <span data-ttu-id="7c2e5-121">금요일</span><span class="sxs-lookup"><span data-stu-id="7c2e5-121">Friday</span></span> 
- <span data-ttu-id="7c2e5-122">토요일</span><span class="sxs-lookup"><span data-stu-id="7c2e5-122">Saturday</span></span> 
- <span data-ttu-id="7c2e5-123">일요일</span><span class="sxs-lookup"><span data-stu-id="7c2e5-123">Sunday</span></span>

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

### <span data-ttu-id="7c2e5-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c2e5-124">-DefaultProfile</span></span>
<span data-ttu-id="7c2e5-125">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7c2e5-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c2e5-126">-MaintenanceWindow</span><span class="sxs-lookup"><span data-stu-id="7c2e5-126">-MaintenanceWindow</span></span>
<span data-ttu-id="7c2e5-127">업데이트에 허용되는 기간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7c2e5-127">Specifies the amount of time window allowed for updates.</span></span>

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

### <span data-ttu-id="7c2e5-128">-StartHourUtc</span><span class="sxs-lookup"><span data-stu-id="7c2e5-128">-StartHourUtc</span></span>
<span data-ttu-id="7c2e5-129">일정이 시작되는 하루의 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7c2e5-129">Specifies an hour of the day when the schedule starts.</span></span>

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

### <span data-ttu-id="7c2e5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c2e5-130">CommonParameters</span></span>
<span data-ttu-id="7c2e5-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7c2e5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c2e5-132">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7c2e5-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c2e5-133">입력</span><span class="sxs-lookup"><span data-stu-id="7c2e5-133">INPUTS</span></span>

### <span data-ttu-id="7c2e5-134">System.String</span><span class="sxs-lookup"><span data-stu-id="7c2e5-134">System.String</span></span>

### <span data-ttu-id="7c2e5-135">System.Int32</span><span class="sxs-lookup"><span data-stu-id="7c2e5-135">System.Int32</span></span>

### <span data-ttu-id="7c2e5-136">System.Nullable'1[[System.TimeSpan, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7c2e5-136">System.Nullable\`1[[System.TimeSpan, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="7c2e5-137">출력</span><span class="sxs-lookup"><span data-stu-id="7c2e5-137">OUTPUTS</span></span>

### <span data-ttu-id="7c2e5-138">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="7c2e5-138">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="7c2e5-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7c2e5-139">NOTES</span></span>
* <span data-ttu-id="7c2e5-140">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, redis, 캐시, 웹, 웹앱, 웹 사이트</span><span class="sxs-lookup"><span data-stu-id="7c2e5-140">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="7c2e5-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7c2e5-141">RELATED LINKS</span></span>

[<span data-ttu-id="7c2e5-142">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="7c2e5-142">Get-AzRedisCachePatchSchedule</span></span>](./Get-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="7c2e5-143">New-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="7c2e5-143">New-AzRedisCachePatchSchedule</span></span>](./New-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="7c2e5-144">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="7c2e5-144">Remove-AzRedisCachePatchSchedule</span></span>](./Remove-AzRedisCachePatchSchedule.md)


