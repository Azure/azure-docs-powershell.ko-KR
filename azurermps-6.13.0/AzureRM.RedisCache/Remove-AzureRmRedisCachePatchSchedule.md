---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 2EA765B8-D82B-4789-8F10-88F79BDF44D0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/remove-azurermrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCachePatchSchedule.md
ms.openlocfilehash: 7224e83333b281fac849ee9e5d99a0691aba3ccc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703437"
---
# <span data-ttu-id="6d592-101">Remove-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="6d592-101">Remove-AzureRmRedisCachePatchSchedule</span></span>

## <span data-ttu-id="6d592-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d592-102">SYNOPSIS</span></span>
<span data-ttu-id="6d592-103">패치 일정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d592-103">Removes the patch schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d592-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6d592-104">SYNTAX</span></span>

```
Remove-AzureRmRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d592-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6d592-105">DESCRIPTION</span></span>
<span data-ttu-id="6d592-106">**AzureRmRedisCachePatchSchedule** Cmdlet은 Azure Redis cache의 캐시에서 패치 일정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d592-106">The **Remove-AzureRmRedisCachePatchSchedule** cmdlet removes the patch schedule from a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="6d592-107">예제의</span><span class="sxs-lookup"><span data-stu-id="6d592-107">EXAMPLES</span></span>

### <span data-ttu-id="6d592-108">예제 1: 패치 일정 제거</span><span class="sxs-lookup"><span data-stu-id="6d592-108">Example 1: Remove the patch schedule</span></span>
```
PS C:\>Remove-AzureRmRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="6d592-109">이 명령은 RedisCache06 이라는 캐시에서 패치 일정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d592-109">This command removes the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="6d592-110">변수</span><span class="sxs-lookup"><span data-stu-id="6d592-110">PARAMETERS</span></span>

### <span data-ttu-id="6d592-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d592-111">-DefaultProfile</span></span>
<span data-ttu-id="6d592-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6d592-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d592-113">-이름</span><span class="sxs-lookup"><span data-stu-id="6d592-113">-Name</span></span>
<span data-ttu-id="6d592-114">캐시의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d592-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="6d592-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6d592-115">-PassThru</span></span>
<span data-ttu-id="6d592-116">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="6d592-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="6d592-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d592-117">-ResourceGroupName</span></span>
<span data-ttu-id="6d592-118">캐시를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d592-118">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="6d592-119">-확인</span><span class="sxs-lookup"><span data-stu-id="6d592-119">-Confirm</span></span>
<span data-ttu-id="6d592-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d592-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d592-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d592-121">-WhatIf</span></span>
<span data-ttu-id="6d592-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6d592-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d592-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6d592-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d592-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d592-124">CommonParameters</span></span>
<span data-ttu-id="6d592-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d592-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d592-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d592-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d592-127">입력</span><span class="sxs-lookup"><span data-stu-id="6d592-127">INPUTS</span></span>

### <span data-ttu-id="6d592-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6d592-128">System.String</span></span>

## <span data-ttu-id="6d592-129">출력</span><span class="sxs-lookup"><span data-stu-id="6d592-129">OUTPUTS</span></span>

### <span data-ttu-id="6d592-130">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="6d592-130">System.Boolean</span></span>

## <span data-ttu-id="6d592-131">상속자</span><span class="sxs-lookup"><span data-stu-id="6d592-131">NOTES</span></span>
* <span data-ttu-id="6d592-132">키워드: azure, azurerm, arm, resource, 관리, manager, redis, cache, web, web app, 웹 사이트</span><span class="sxs-lookup"><span data-stu-id="6d592-132">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="6d592-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6d592-133">RELATED LINKS</span></span>

[<span data-ttu-id="6d592-134">Get-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="6d592-134">Get-AzureRmRedisCachePatchSchedule</span></span>](./Get-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="6d592-135">새로운 AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="6d592-135">New-AzureRmRedisCachePatchSchedule</span></span>](./New-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="6d592-136">새로운 AzureRmRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="6d592-136">New-AzureRmRedisCacheScheduleEntry</span></span>](./New-AzureRmRedisCacheScheduleEntry.md)


