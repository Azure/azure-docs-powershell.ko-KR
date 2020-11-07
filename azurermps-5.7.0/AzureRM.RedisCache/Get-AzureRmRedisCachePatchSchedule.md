---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: DA180A4A-88B6-4359-94E0-CF72F66D1FE4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/get-azurermrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCachePatchSchedule.md
ms.openlocfilehash: 091d3d52da1319842d221881f03fca2b21353fa9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702146"
---
# <span data-ttu-id="90445-101">Get-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="90445-101">Get-AzureRmRedisCachePatchSchedule</span></span>

## <span data-ttu-id="90445-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90445-102">SYNOPSIS</span></span>
<span data-ttu-id="90445-103">패치 일정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="90445-103">Gets a patch schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90445-104">구문과</span><span class="sxs-lookup"><span data-stu-id="90445-104">SYNTAX</span></span>

```
Get-AzureRmRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90445-105">설명은</span><span class="sxs-lookup"><span data-stu-id="90445-105">DESCRIPTION</span></span>
<span data-ttu-id="90445-106">**AzureRmRedisCachePatchSchedule** Cmdlet은 Azure Redis cache의 캐시에 대 한 패치 일정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="90445-106">The **Get-AzureRmRedisCachePatchSchedule** cmdlet gets a patch schedule for a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="90445-107">예제의</span><span class="sxs-lookup"><span data-stu-id="90445-107">EXAMPLES</span></span>

### <span data-ttu-id="90445-108">예제 1: 패치 일정 가져오기</span><span class="sxs-lookup"><span data-stu-id="90445-108">Example 1: Get the patch schedule</span></span>
```
PS C:\>Get-AzureRmRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="90445-109">이 명령은 RedisCache06 이라는 캐시에서 패치 일정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="90445-109">This command gets the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="90445-110">변수</span><span class="sxs-lookup"><span data-stu-id="90445-110">PARAMETERS</span></span>

### <span data-ttu-id="90445-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90445-111">-DefaultProfile</span></span>
<span data-ttu-id="90445-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="90445-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90445-113">-이름</span><span class="sxs-lookup"><span data-stu-id="90445-113">-Name</span></span>
<span data-ttu-id="90445-114">캐시의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90445-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="90445-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90445-115">-ResourceGroupName</span></span>
<span data-ttu-id="90445-116">캐시를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90445-116">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="90445-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90445-117">CommonParameters</span></span>
<span data-ttu-id="90445-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="90445-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90445-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90445-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90445-120">입력</span><span class="sxs-lookup"><span data-stu-id="90445-120">INPUTS</span></span>

### <span data-ttu-id="90445-121">않아야</span><span class="sxs-lookup"><span data-stu-id="90445-121">None</span></span>
<span data-ttu-id="90445-122">속성 이름으로이 cmdlet에 대 한 입력을 파이프로 지정할 수 있지만 값을 기준으로 하지 않아도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="90445-122">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="90445-123">출력</span><span class="sxs-lookup"><span data-stu-id="90445-123">OUTPUTS</span></span>

### <span data-ttu-id="90445-124">PSScheduleEntry. 모델. m e.</span><span class="sxs-lookup"><span data-stu-id="90445-124">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>
<span data-ttu-id="90445-125">이 cmdlet은 캐시에 설정 된 패치 일정 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="90445-125">This cmdlet returns the of patch schedule entries set on the cache.</span></span>

## <span data-ttu-id="90445-126">상속자</span><span class="sxs-lookup"><span data-stu-id="90445-126">NOTES</span></span>
* <span data-ttu-id="90445-127">키워드: azure, azurerm, arm, resource, 관리, manager, redis, cache, web, web app, 웹 사이트</span><span class="sxs-lookup"><span data-stu-id="90445-127">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="90445-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="90445-128">RELATED LINKS</span></span>

[<span data-ttu-id="90445-129">새로운 AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="90445-129">New-AzureRmRedisCachePatchSchedule</span></span>](./New-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="90445-130">새로운 AzureRmRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="90445-130">New-AzureRmRedisCacheScheduleEntry</span></span>](./New-AzureRmRedisCacheScheduleEntry.md)

[<span data-ttu-id="90445-131">제거-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="90445-131">Remove-AzureRmRedisCachePatchSchedule</span></span>](./Remove-AzureRmRedisCachePatchSchedule.md)


