---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 2EA765B8-D82B-4789-8F10-88F79BDF44D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCachePatchSchedule.md
ms.openlocfilehash: 8e66391ff613578d1306543c626908763a932d06
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98352521"
---
# <span data-ttu-id="76bca-101">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="76bca-101">Remove-AzRedisCachePatchSchedule</span></span>

## <span data-ttu-id="76bca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76bca-102">SYNOPSIS</span></span>
<span data-ttu-id="76bca-103">패치 일정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="76bca-103">Removes the patch schedule.</span></span>

## <span data-ttu-id="76bca-104">구문</span><span class="sxs-lookup"><span data-stu-id="76bca-104">SYNTAX</span></span>

```
Remove-AzRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76bca-105">설명</span><span class="sxs-lookup"><span data-stu-id="76bca-105">DESCRIPTION</span></span>
<span data-ttu-id="76bca-106">**Remove-AzRedisCachePatchSchedule** cmdlet은 Azure Redis Cache의 캐시에서 패치 일정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="76bca-106">The **Remove-AzRedisCachePatchSchedule** cmdlet removes the patch schedule from a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="76bca-107">예제</span><span class="sxs-lookup"><span data-stu-id="76bca-107">EXAMPLES</span></span>

### <span data-ttu-id="76bca-108">예제 1: 패치 일정 제거</span><span class="sxs-lookup"><span data-stu-id="76bca-108">Example 1: Remove the patch schedule</span></span>
```
PS C:\>Remove-AzRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="76bca-109">이 명령은 RedisCache06이라는 캐시에서 패치 일정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="76bca-109">This command removes the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="76bca-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="76bca-110">PARAMETERS</span></span>

### <span data-ttu-id="76bca-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76bca-111">-DefaultProfile</span></span>
<span data-ttu-id="76bca-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="76bca-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76bca-113">-Name</span><span class="sxs-lookup"><span data-stu-id="76bca-113">-Name</span></span>
<span data-ttu-id="76bca-114">캐시의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="76bca-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="76bca-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="76bca-115">-PassThru</span></span>
<span data-ttu-id="76bca-116">{{PassThru 설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="76bca-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="76bca-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76bca-117">-ResourceGroupName</span></span>
<span data-ttu-id="76bca-118">캐시를 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="76bca-118">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="76bca-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="76bca-119">-Confirm</span></span>
<span data-ttu-id="76bca-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="76bca-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76bca-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76bca-121">-WhatIf</span></span>
<span data-ttu-id="76bca-122">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="76bca-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76bca-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="76bca-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76bca-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76bca-124">CommonParameters</span></span>
<span data-ttu-id="76bca-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="76bca-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76bca-126">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="76bca-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76bca-127">입력</span><span class="sxs-lookup"><span data-stu-id="76bca-127">INPUTS</span></span>

### <span data-ttu-id="76bca-128">System.String</span><span class="sxs-lookup"><span data-stu-id="76bca-128">System.String</span></span>

## <span data-ttu-id="76bca-129">출력</span><span class="sxs-lookup"><span data-stu-id="76bca-129">OUTPUTS</span></span>

### <span data-ttu-id="76bca-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="76bca-130">System.Boolean</span></span>

## <span data-ttu-id="76bca-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="76bca-131">NOTES</span></span>
* <span data-ttu-id="76bca-132">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, redis, 캐시, 웹, 웹앱, 웹 사이트</span><span class="sxs-lookup"><span data-stu-id="76bca-132">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="76bca-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="76bca-133">RELATED LINKS</span></span>

[<span data-ttu-id="76bca-134">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="76bca-134">Get-AzRedisCachePatchSchedule</span></span>](./Get-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="76bca-135">New-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="76bca-135">New-AzRedisCachePatchSchedule</span></span>](./New-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="76bca-136">New-AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="76bca-136">New-AzRedisCacheScheduleEntry</span></span>](./New-AzRedisCacheScheduleEntry.md)

