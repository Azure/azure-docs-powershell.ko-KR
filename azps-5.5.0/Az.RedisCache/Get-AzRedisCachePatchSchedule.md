---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: DA180A4A-88B6-4359-94E0-CF72F66D1FE4
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCachePatchSchedule.md
ms.openlocfilehash: 0e63f8e5f427a251db13c76f915dc615f259defc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178937"
---
# <span data-ttu-id="90317-101">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="90317-101">Get-AzRedisCachePatchSchedule</span></span>

## <span data-ttu-id="90317-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90317-102">SYNOPSIS</span></span>
<span data-ttu-id="90317-103">패치 일정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="90317-103">Gets a patch schedule.</span></span>

## <span data-ttu-id="90317-104">구문</span><span class="sxs-lookup"><span data-stu-id="90317-104">SYNTAX</span></span>

```
Get-AzRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90317-105">설명</span><span class="sxs-lookup"><span data-stu-id="90317-105">DESCRIPTION</span></span>
<span data-ttu-id="90317-106">**Get-AzRedisCachePatchSchedule** cmdlet은 Azure Redis Cache의 캐시에 대한 패치 일정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="90317-106">The **Get-AzRedisCachePatchSchedule** cmdlet gets a patch schedule for a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="90317-107">예제</span><span class="sxs-lookup"><span data-stu-id="90317-107">EXAMPLES</span></span>

### <span data-ttu-id="90317-108">예제 1: 패치 일정 확인</span><span class="sxs-lookup"><span data-stu-id="90317-108">Example 1: Get the patch schedule</span></span>
```
PS C:\>Get-AzRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="90317-109">이 명령은 RedisCache06이라는 캐시에서 패치 일정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="90317-109">This command gets the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="90317-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="90317-110">PARAMETERS</span></span>

### <span data-ttu-id="90317-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90317-111">-DefaultProfile</span></span>
<span data-ttu-id="90317-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="90317-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90317-113">-Name</span><span class="sxs-lookup"><span data-stu-id="90317-113">-Name</span></span>
<span data-ttu-id="90317-114">캐시의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="90317-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="90317-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90317-115">-ResourceGroupName</span></span>
<span data-ttu-id="90317-116">캐시를 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="90317-116">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="90317-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90317-117">CommonParameters</span></span>
<span data-ttu-id="90317-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="90317-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90317-119">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="90317-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90317-120">입력</span><span class="sxs-lookup"><span data-stu-id="90317-120">INPUTS</span></span>

### <span data-ttu-id="90317-121">System.String</span><span class="sxs-lookup"><span data-stu-id="90317-121">System.String</span></span>

## <span data-ttu-id="90317-122">출력</span><span class="sxs-lookup"><span data-stu-id="90317-122">OUTPUTS</span></span>

### <span data-ttu-id="90317-123">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="90317-123">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="90317-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="90317-124">NOTES</span></span>
* <span data-ttu-id="90317-125">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, redis, 캐시, 웹, 웹앱, 웹 사이트</span><span class="sxs-lookup"><span data-stu-id="90317-125">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="90317-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="90317-126">RELATED LINKS</span></span>

[<span data-ttu-id="90317-127">New-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="90317-127">New-AzRedisCachePatchSchedule</span></span>](./New-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="90317-128">New-AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="90317-128">New-AzRedisCacheScheduleEntry</span></span>](./New-AzRedisCacheScheduleEntry.md)

[<span data-ttu-id="90317-129">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="90317-129">Remove-AzRedisCachePatchSchedule</span></span>](./Remove-AzRedisCachePatchSchedule.md)


