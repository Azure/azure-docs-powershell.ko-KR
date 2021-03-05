---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: F7FAFF52-5E07-4D88-B48F-BC70C43E8691
online version: https://docs.microsoft.com/powershell/module/az.rediscache/new-azrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCachePatchSchedule.md
ms.openlocfilehash: ebc51005bcffdde2ad5f64764e90440e8d1e7583
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961723"
---
# <span data-ttu-id="2e93d-101">New-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="2e93d-101">New-AzRedisCachePatchSchedule</span></span>

## <span data-ttu-id="2e93d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e93d-102">SYNOPSIS</span></span>
<span data-ttu-id="2e93d-103">패치 일정을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="2e93d-103">Adds a patch schedule.</span></span>

## <span data-ttu-id="2e93d-104">구문</span><span class="sxs-lookup"><span data-stu-id="2e93d-104">SYNTAX</span></span>

```
New-AzRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String> -Entries <PSScheduleEntry[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e93d-105">설명</span><span class="sxs-lookup"><span data-stu-id="2e93d-105">DESCRIPTION</span></span>
<span data-ttu-id="2e93d-106">**New-AzRedisCachePatchSchedule** cmdlet은 Azure Redis Cache의 캐시에 패치 일정을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="2e93d-106">The **New-AzRedisCachePatchSchedule** cmdlet adds a patch schedule to a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="2e93d-107">예제</span><span class="sxs-lookup"><span data-stu-id="2e93d-107">EXAMPLES</span></span>

### <span data-ttu-id="2e93d-108">예제 1: 캐시에 패치 일정 만들기 및 추가</span><span class="sxs-lookup"><span data-stu-id="2e93d-108">Example 1: Create and add a patch schedule on a cache</span></span>
```
PS C:\>New-AzRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Entries @(New-AzRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00")
```

<span data-ttu-id="2e93d-109">이 명령은 RedisCache06이라는 캐시에 패치 일정을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="2e93d-109">This command adds a patch schedule to the cache named RedisCache06.</span></span>
<span data-ttu-id="2e93d-110">항목 매개 변수는 **New-AzRedisCacheScheduleEntry를** 사용하여 일정을 만드는 명령의 값으로 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="2e93d-110">The Entries parameter takes as its value a command that uses **New-AzRedisCacheScheduleEntry** to create a schedule.</span></span>

## <span data-ttu-id="2e93d-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="2e93d-111">PARAMETERS</span></span>

### <span data-ttu-id="2e93d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e93d-112">-DefaultProfile</span></span>
<span data-ttu-id="2e93d-113">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2e93d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e93d-114">-항목</span><span class="sxs-lookup"><span data-stu-id="2e93d-114">-Entries</span></span>
<span data-ttu-id="2e93d-115">이 cmdlet이 캐시에 설정하는 일정 배열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2e93d-115">Specifies an array of schedules that this cmdlet sets on a cache.</span></span> <span data-ttu-id="2e93d-116">**PSScheduleEntry** 개체를 얻은 경우 New-AzRedisCacheScheduleEntry cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="2e93d-116">To obtain a **PSScheduleEntry** object, use the New-AzRedisCacheScheduleEntry cmdlet.</span></span>

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

### <span data-ttu-id="2e93d-117">-Name</span><span class="sxs-lookup"><span data-stu-id="2e93d-117">-Name</span></span>
<span data-ttu-id="2e93d-118">캐시의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2e93d-118">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="2e93d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e93d-119">-ResourceGroupName</span></span>
<span data-ttu-id="2e93d-120">캐시를 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2e93d-120">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="2e93d-121">-확인</span><span class="sxs-lookup"><span data-stu-id="2e93d-121">-Confirm</span></span>
<span data-ttu-id="2e93d-122">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2e93d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e93d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e93d-123">-WhatIf</span></span>
<span data-ttu-id="2e93d-124">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="2e93d-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2e93d-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2e93d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e93d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e93d-126">CommonParameters</span></span>
<span data-ttu-id="2e93d-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2e93d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e93d-128">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="2e93d-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e93d-129">입력</span><span class="sxs-lookup"><span data-stu-id="2e93d-129">INPUTS</span></span>

### <span data-ttu-id="2e93d-130">System.String</span><span class="sxs-lookup"><span data-stu-id="2e93d-130">System.String</span></span>

### <span data-ttu-id="2e93d-131">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry[]</span><span class="sxs-lookup"><span data-stu-id="2e93d-131">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry[]</span></span>

## <span data-ttu-id="2e93d-132">출력</span><span class="sxs-lookup"><span data-stu-id="2e93d-132">OUTPUTS</span></span>

### <span data-ttu-id="2e93d-133">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="2e93d-133">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="2e93d-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2e93d-134">NOTES</span></span>
* <span data-ttu-id="2e93d-135">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, redis, 캐시, 웹, 웹앱, 웹 사이트</span><span class="sxs-lookup"><span data-stu-id="2e93d-135">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="2e93d-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2e93d-136">RELATED LINKS</span></span>

[<span data-ttu-id="2e93d-137">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="2e93d-137">Get-AzRedisCachePatchSchedule</span></span>](./Get-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="2e93d-138">New-AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="2e93d-138">New-AzRedisCacheScheduleEntry</span></span>](./New-AzRedisCacheScheduleEntry.md)

[<span data-ttu-id="2e93d-139">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="2e93d-139">Remove-AzRedisCachePatchSchedule</span></span>](./Remove-AzRedisCachePatchSchedule.md)


