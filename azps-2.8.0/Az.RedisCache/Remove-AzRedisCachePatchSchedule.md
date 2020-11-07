---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 2EA765B8-D82B-4789-8F10-88F79BDF44D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCachePatchSchedule.md
ms.openlocfilehash: 83fab07a44dd85e000e86597881341cad6c641e8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871974"
---
# <span data-ttu-id="b460a-101">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="b460a-101">Remove-AzRedisCachePatchSchedule</span></span>

## <span data-ttu-id="b460a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b460a-102">SYNOPSIS</span></span>
<span data-ttu-id="b460a-103">패치 일정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b460a-103">Removes the patch schedule.</span></span>

## <span data-ttu-id="b460a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b460a-104">SYNTAX</span></span>

```
Remove-AzRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b460a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b460a-105">DESCRIPTION</span></span>
<span data-ttu-id="b460a-106">**AzRedisCachePatchSchedule** Cmdlet은 Azure Redis cache의 캐시에서 패치 일정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b460a-106">The **Remove-AzRedisCachePatchSchedule** cmdlet removes the patch schedule from a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="b460a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b460a-107">EXAMPLES</span></span>

### <span data-ttu-id="b460a-108">예제 1: 패치 일정 제거</span><span class="sxs-lookup"><span data-stu-id="b460a-108">Example 1: Remove the patch schedule</span></span>
```
PS C:\>Remove-AzRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="b460a-109">이 명령은 RedisCache06 이라는 캐시에서 패치 일정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b460a-109">This command removes the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="b460a-110">변수</span><span class="sxs-lookup"><span data-stu-id="b460a-110">PARAMETERS</span></span>

### <span data-ttu-id="b460a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b460a-111">-DefaultProfile</span></span>
<span data-ttu-id="b460a-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b460a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b460a-113">-이름</span><span class="sxs-lookup"><span data-stu-id="b460a-113">-Name</span></span>
<span data-ttu-id="b460a-114">캐시의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b460a-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="b460a-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b460a-115">-PassThru</span></span>
<span data-ttu-id="b460a-116">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="b460a-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="b460a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b460a-117">-ResourceGroupName</span></span>
<span data-ttu-id="b460a-118">캐시를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b460a-118">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="b460a-119">-확인</span><span class="sxs-lookup"><span data-stu-id="b460a-119">-Confirm</span></span>
<span data-ttu-id="b460a-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b460a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b460a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b460a-121">-WhatIf</span></span>
<span data-ttu-id="b460a-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b460a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b460a-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b460a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b460a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b460a-124">CommonParameters</span></span>
<span data-ttu-id="b460a-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b460a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b460a-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b460a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b460a-127">입력</span><span class="sxs-lookup"><span data-stu-id="b460a-127">INPUTS</span></span>

### <span data-ttu-id="b460a-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b460a-128">System.String</span></span>

## <span data-ttu-id="b460a-129">출력</span><span class="sxs-lookup"><span data-stu-id="b460a-129">OUTPUTS</span></span>

### <span data-ttu-id="b460a-130">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="b460a-130">System.Boolean</span></span>

## <span data-ttu-id="b460a-131">상속자</span><span class="sxs-lookup"><span data-stu-id="b460a-131">NOTES</span></span>
* <span data-ttu-id="b460a-132">키워드: azure, azurerm, arm, resource, 관리, manager, redis, cache, web, web app, 웹 사이트</span><span class="sxs-lookup"><span data-stu-id="b460a-132">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="b460a-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b460a-133">RELATED LINKS</span></span>

[<span data-ttu-id="b460a-134">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="b460a-134">Get-AzRedisCachePatchSchedule</span></span>](./Get-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="b460a-135">새로운 AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="b460a-135">New-AzRedisCachePatchSchedule</span></span>](./New-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="b460a-136">새로운 AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="b460a-136">New-AzRedisCacheScheduleEntry</span></span>](./New-AzRedisCacheScheduleEntry.md)


