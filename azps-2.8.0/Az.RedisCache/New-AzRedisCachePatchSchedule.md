---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: F7FAFF52-5E07-4D88-B48F-BC70C43E8691
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCachePatchSchedule.md
ms.openlocfilehash: 367327e19ff95132b7b7d6bc2d86970892ab6e55
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873456"
---
# <span data-ttu-id="352c2-101">New-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="352c2-101">New-AzRedisCachePatchSchedule</span></span>

## <span data-ttu-id="352c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="352c2-102">SYNOPSIS</span></span>
<span data-ttu-id="352c2-103">패치 일정을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="352c2-103">Adds a patch schedule.</span></span>

## <span data-ttu-id="352c2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="352c2-104">SYNTAX</span></span>

```
New-AzRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String> -Entries <PSScheduleEntry[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="352c2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="352c2-105">DESCRIPTION</span></span>
<span data-ttu-id="352c2-106">**AzRedisCachePatchSchedule** Cmdlet은 Azure Redis cache의 캐시에 패치 일정을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="352c2-106">The **New-AzRedisCachePatchSchedule** cmdlet adds a patch schedule to a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="352c2-107">예제의</span><span class="sxs-lookup"><span data-stu-id="352c2-107">EXAMPLES</span></span>

### <span data-ttu-id="352c2-108">예제 1: 캐시에서 패치 일정 만들기 및 추가</span><span class="sxs-lookup"><span data-stu-id="352c2-108">Example 1: Create and add a patch schedule on a cache</span></span>
```
PS C:\>New-AzRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Entries @(New-AzRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00")
```

<span data-ttu-id="352c2-109">이 명령은 패치 일정을 RedisCache06 이라는 캐시에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="352c2-109">This command adds a patch schedule to the cache named RedisCache06.</span></span>
<span data-ttu-id="352c2-110">Entries 매개 변수는 **New-AzRedisCacheScheduleEntry** 를 사용 하 여 일정을 만드는 명령 값으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="352c2-110">The Entries parameter takes as its value a command that uses **New-AzRedisCacheScheduleEntry** to create a schedule.</span></span>

## <span data-ttu-id="352c2-111">변수</span><span class="sxs-lookup"><span data-stu-id="352c2-111">PARAMETERS</span></span>

### <span data-ttu-id="352c2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="352c2-112">-DefaultProfile</span></span>
<span data-ttu-id="352c2-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="352c2-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="352c2-114">-항목</span><span class="sxs-lookup"><span data-stu-id="352c2-114">-Entries</span></span>
<span data-ttu-id="352c2-115">이 cmdlet이 캐시에 설정 하는 일정의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="352c2-115">Specifies an array of schedules that this cmdlet sets on a cache.</span></span> <span data-ttu-id="352c2-116">**PSScheduleEntry** 개체를 가져오려면 New-AzRedisCacheScheduleEntry cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="352c2-116">To obtain a **PSScheduleEntry** object, use the New-AzRedisCacheScheduleEntry cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="352c2-117">-이름</span><span class="sxs-lookup"><span data-stu-id="352c2-117">-Name</span></span>
<span data-ttu-id="352c2-118">캐시의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="352c2-118">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="352c2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="352c2-119">-ResourceGroupName</span></span>
<span data-ttu-id="352c2-120">캐시를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="352c2-120">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="352c2-121">-확인</span><span class="sxs-lookup"><span data-stu-id="352c2-121">-Confirm</span></span>
<span data-ttu-id="352c2-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="352c2-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="352c2-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="352c2-123">-WhatIf</span></span>
<span data-ttu-id="352c2-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="352c2-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="352c2-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="352c2-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="352c2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="352c2-126">CommonParameters</span></span>
<span data-ttu-id="352c2-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="352c2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="352c2-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="352c2-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="352c2-129">입력</span><span class="sxs-lookup"><span data-stu-id="352c2-129">INPUTS</span></span>

### <span data-ttu-id="352c2-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="352c2-130">System.String</span></span>

### <span data-ttu-id="352c2-131">PSScheduleEntry []을 (를) 다시 캐시 합니다.</span><span class="sxs-lookup"><span data-stu-id="352c2-131">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry[]</span></span>

## <span data-ttu-id="352c2-132">출력</span><span class="sxs-lookup"><span data-stu-id="352c2-132">OUTPUTS</span></span>

### <span data-ttu-id="352c2-133">PSScheduleEntry. 모델. m e.</span><span class="sxs-lookup"><span data-stu-id="352c2-133">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="352c2-134">상속자</span><span class="sxs-lookup"><span data-stu-id="352c2-134">NOTES</span></span>
* <span data-ttu-id="352c2-135">키워드: azure, azurerm, arm, resource, 관리, manager, redis, cache, web, web app, 웹 사이트</span><span class="sxs-lookup"><span data-stu-id="352c2-135">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="352c2-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="352c2-136">RELATED LINKS</span></span>

[<span data-ttu-id="352c2-137">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="352c2-137">Get-AzRedisCachePatchSchedule</span></span>](./Get-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="352c2-138">새로운 AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="352c2-138">New-AzRedisCacheScheduleEntry</span></span>](./New-AzRedisCacheScheduleEntry.md)

[<span data-ttu-id="352c2-139">제거-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="352c2-139">Remove-AzRedisCachePatchSchedule</span></span>](./Remove-AzRedisCachePatchSchedule.md)


