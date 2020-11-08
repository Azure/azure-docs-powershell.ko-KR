---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: DA180A4A-88B6-4359-94E0-CF72F66D1FE4
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCachePatchSchedule.md
ms.openlocfilehash: 0e63f8e5f427a251db13c76f915dc615f259defc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212904"
---
# <span data-ttu-id="4176c-101">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="4176c-101">Get-AzRedisCachePatchSchedule</span></span>

## <span data-ttu-id="4176c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4176c-102">SYNOPSIS</span></span>
<span data-ttu-id="4176c-103">패치 일정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4176c-103">Gets a patch schedule.</span></span>

## <span data-ttu-id="4176c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4176c-104">SYNTAX</span></span>

```
Get-AzRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4176c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4176c-105">DESCRIPTION</span></span>
<span data-ttu-id="4176c-106">**AzRedisCachePatchSchedule** Cmdlet은 Azure Redis cache의 캐시에 대 한 패치 일정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4176c-106">The **Get-AzRedisCachePatchSchedule** cmdlet gets a patch schedule for a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="4176c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4176c-107">EXAMPLES</span></span>

### <span data-ttu-id="4176c-108">예제 1: 패치 일정 가져오기</span><span class="sxs-lookup"><span data-stu-id="4176c-108">Example 1: Get the patch schedule</span></span>
```
PS C:\>Get-AzRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="4176c-109">이 명령은 RedisCache06 이라는 캐시에서 패치 일정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4176c-109">This command gets the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="4176c-110">변수</span><span class="sxs-lookup"><span data-stu-id="4176c-110">PARAMETERS</span></span>

### <span data-ttu-id="4176c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4176c-111">-DefaultProfile</span></span>
<span data-ttu-id="4176c-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4176c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4176c-113">-이름</span><span class="sxs-lookup"><span data-stu-id="4176c-113">-Name</span></span>
<span data-ttu-id="4176c-114">캐시의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4176c-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="4176c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4176c-115">-ResourceGroupName</span></span>
<span data-ttu-id="4176c-116">캐시를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4176c-116">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="4176c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4176c-117">CommonParameters</span></span>
<span data-ttu-id="4176c-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4176c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4176c-119">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4176c-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4176c-120">입력</span><span class="sxs-lookup"><span data-stu-id="4176c-120">INPUTS</span></span>

### <span data-ttu-id="4176c-121">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4176c-121">System.String</span></span>

## <span data-ttu-id="4176c-122">출력</span><span class="sxs-lookup"><span data-stu-id="4176c-122">OUTPUTS</span></span>

### <span data-ttu-id="4176c-123">PSScheduleEntry. 모델. m e.</span><span class="sxs-lookup"><span data-stu-id="4176c-123">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="4176c-124">상속자</span><span class="sxs-lookup"><span data-stu-id="4176c-124">NOTES</span></span>
* <span data-ttu-id="4176c-125">키워드: azure, azurerm, arm, resource, 관리, manager, redis, cache, web, web app, 웹 사이트</span><span class="sxs-lookup"><span data-stu-id="4176c-125">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="4176c-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4176c-126">RELATED LINKS</span></span>

[<span data-ttu-id="4176c-127">새로운 AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="4176c-127">New-AzRedisCachePatchSchedule</span></span>](./New-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="4176c-128">새로운 AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="4176c-128">New-AzRedisCacheScheduleEntry</span></span>](./New-AzRedisCacheScheduleEntry.md)

[<span data-ttu-id="4176c-129">제거-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="4176c-129">Remove-AzRedisCachePatchSchedule</span></span>](./Remove-AzRedisCachePatchSchedule.md)


