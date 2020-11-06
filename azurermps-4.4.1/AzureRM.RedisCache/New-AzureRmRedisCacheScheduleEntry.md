---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: ACB53C23-99E0-4A0A-A44E-0D3FDB12450B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheScheduleEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheScheduleEntry.md
ms.openlocfilehash: 07bfc520cfabc33ed4f72f1d0d4c46c9104a5253
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527340"
---
# <span data-ttu-id="0b3e3-101">New-AzureRmRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="0b3e3-101">New-AzureRmRedisCacheScheduleEntry</span></span>

## <span data-ttu-id="0b3e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b3e3-102">SYNOPSIS</span></span>
<span data-ttu-id="0b3e3-103">일정 항목을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0b3e3-103">Creates a schedule entry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b3e3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0b3e3-104">SYNTAX</span></span>

```
New-AzureRmRedisCacheScheduleEntry -DayOfWeek <String> -StartHourUtc <Int32> [-MaintenanceWindow <TimeSpan>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b3e3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0b3e3-105">DESCRIPTION</span></span>
<span data-ttu-id="0b3e3-106">**AzureRmRedisCacheScheduleEntry** Cmdlet은 **PSScheduleEntry** 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0b3e3-106">The **New-AzureRmRedisCacheScheduleEntry** cmdlet creates a **PSScheduleEntry** object.</span></span>
<span data-ttu-id="0b3e3-107">Azure Redis 캐시 패치 예약 cmdlet (예: New-AzureRmRedisCachePatchSchedule cmdlet)에는 일정 항목 개체가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b3e3-107">Azure Redis Cache patch schedule cmdlets, such as the New-AzureRmRedisCachePatchSchedule cmdlet, require schedule entry objects.</span></span>

## <span data-ttu-id="0b3e3-108">예제의</span><span class="sxs-lookup"><span data-stu-id="0b3e3-108">EXAMPLES</span></span>

### <span data-ttu-id="0b3e3-109">예제 1: 주말 일정 항목 만들기</span><span class="sxs-lookup"><span data-stu-id="0b3e3-109">Example 1: Create a schedule entry for weekends</span></span>
```
PS C:\>New-AzureRmRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00"
```

<span data-ttu-id="0b3e3-110">이 명령은 지정 된 시작 시간 및 윈도를 포함 하는 주말 일정을 나타내는 **PSScheduleEntry** 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0b3e3-110">This command creates a **PSScheduleEntry** object that represents a weekend schedule that has the specified start time and window.</span></span>

## <span data-ttu-id="0b3e3-111">변수</span><span class="sxs-lookup"><span data-stu-id="0b3e3-111">PARAMETERS</span></span>

### <span data-ttu-id="0b3e3-112">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="0b3e3-112">-DayOfWeek</span></span>
<span data-ttu-id="0b3e3-113">일정 항목에 대 한 요일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b3e3-113">Specifies the day of the week for the schedule entry.</span></span>
<span data-ttu-id="0b3e3-114">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0b3e3-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0b3e3-115">매일</span><span class="sxs-lookup"><span data-stu-id="0b3e3-115">Everyday</span></span> 
- <span data-ttu-id="0b3e3-116">주말을</span><span class="sxs-lookup"><span data-stu-id="0b3e3-116">Weekend</span></span> 
- <span data-ttu-id="0b3e3-117">월요일</span><span class="sxs-lookup"><span data-stu-id="0b3e3-117">Monday</span></span> 
- <span data-ttu-id="0b3e3-118">시간은</span><span class="sxs-lookup"><span data-stu-id="0b3e3-118">Tuesday</span></span> 
- <span data-ttu-id="0b3e3-119">일</span><span class="sxs-lookup"><span data-stu-id="0b3e3-119">Wednesday</span></span> 
- <span data-ttu-id="0b3e3-120">목요일</span><span class="sxs-lookup"><span data-stu-id="0b3e3-120">Thursday</span></span> 
- <span data-ttu-id="0b3e3-121">금요일</span><span class="sxs-lookup"><span data-stu-id="0b3e3-121">Friday</span></span> 
- <span data-ttu-id="0b3e3-122">토요일</span><span class="sxs-lookup"><span data-stu-id="0b3e3-122">Saturday</span></span> 
- <span data-ttu-id="0b3e3-123">나타내고</span><span class="sxs-lookup"><span data-stu-id="0b3e3-123">Sunday</span></span>

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

### <span data-ttu-id="0b3e3-124">-MaintenanceWindow</span><span class="sxs-lookup"><span data-stu-id="0b3e3-124">-MaintenanceWindow</span></span>
<span data-ttu-id="0b3e3-125">업데이트에 허용 되는 시간 창 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b3e3-125">Specifies the amount of time window allowed for updates.</span></span>

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

### <span data-ttu-id="0b3e3-126">-StartHourUtc</span><span class="sxs-lookup"><span data-stu-id="0b3e3-126">-StartHourUtc</span></span>
<span data-ttu-id="0b3e3-127">일정이 시작 되는 시간 (일)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b3e3-127">Specifies an hour of the day when the schedule starts.</span></span>

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

### <span data-ttu-id="0b3e3-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b3e3-128">-DefaultProfile</span></span>
<span data-ttu-id="0b3e3-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0b3e3-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b3e3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b3e3-130">CommonParameters</span></span>
<span data-ttu-id="0b3e3-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b3e3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b3e3-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b3e3-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b3e3-133">입력</span><span class="sxs-lookup"><span data-stu-id="0b3e3-133">INPUTS</span></span>

### <span data-ttu-id="0b3e3-134">않아야</span><span class="sxs-lookup"><span data-stu-id="0b3e3-134">None</span></span>
<span data-ttu-id="0b3e3-135">속성 이름으로이 cmdlet에 대 한 입력을 파이프로 지정할 수 있지만 값을 기준으로 하지 않아도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0b3e3-135">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="0b3e3-136">출력</span><span class="sxs-lookup"><span data-stu-id="0b3e3-136">OUTPUTS</span></span>

### <span data-ttu-id="0b3e3-137">PSScheduleEntry. 모델. m e.</span><span class="sxs-lookup"><span data-stu-id="0b3e3-137">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>
<span data-ttu-id="0b3e3-138">이 cmdlet은 일정 항목 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b3e3-138">This cmdlet returns a schedule entry object.</span></span>

## <span data-ttu-id="0b3e3-139">상속자</span><span class="sxs-lookup"><span data-stu-id="0b3e3-139">NOTES</span></span>
* <span data-ttu-id="0b3e3-140">키워드: azure, azurerm, arm, resource, 관리, manager, redis, cache, web, web app, 웹 사이트</span><span class="sxs-lookup"><span data-stu-id="0b3e3-140">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="0b3e3-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0b3e3-141">RELATED LINKS</span></span>

[<span data-ttu-id="0b3e3-142">Get-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="0b3e3-142">Get-AzureRmRedisCachePatchSchedule</span></span>](./Get-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="0b3e3-143">새로운 AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="0b3e3-143">New-AzureRmRedisCachePatchSchedule</span></span>](./New-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="0b3e3-144">제거-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="0b3e3-144">Remove-AzureRmRedisCachePatchSchedule</span></span>](./Remove-AzureRmRedisCachePatchSchedule.md)


