---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCache.md
ms.openlocfilehash: 4ae5bdd5dc9c15ab72b2f35f5d67eeaa732296bd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042246"
---
# <span data-ttu-id="665ff-101">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="665ff-101">New-AzApiManagementCache</span></span>

## <span data-ttu-id="665ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="665ff-102">SYNOPSIS</span></span>
<span data-ttu-id="665ff-103">새 캐시 엔터티를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="665ff-103">Creates a new Cache entity</span></span>

## <span data-ttu-id="665ff-104">구문과</span><span class="sxs-lookup"><span data-stu-id="665ff-104">SYNTAX</span></span>

```
New-AzApiManagementCache -Context <PsApiManagementContext> [-CacheId <String>] -ConnectionString <String>
 [-AzureRedisResourceId <String>] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="665ff-105">설명은</span><span class="sxs-lookup"><span data-stu-id="665ff-105">DESCRIPTION</span></span>
<span data-ttu-id="665ff-106">Cmdlet **AzApiManagementCache** 는 Api Management 서비스에 새 캐시 엔터티를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="665ff-106">The cmdlet **New-AzApiManagementCache** creates a new cache entity in Api Management service.</span></span>

## <span data-ttu-id="665ff-107">예제의</span><span class="sxs-lookup"><span data-stu-id="665ff-107">EXAMPLES</span></span>

### <span data-ttu-id="665ff-108">예제 1: 새 캐시 엔터티 만들기</span><span class="sxs-lookup"><span data-stu-id="665ff-108">Example 1 : Create a new Cache entity</span></span>
```powershell
PS c:\> New-AzApiManagementCache -Context $context -ConnectionString "teamdemo.redis.cache.windows.net:6380,password=xxxxxx+xxxxx=,ssl=True,abortConnect=False" -Description "Team Cache"

CacheId           : centralus
Description       : Team Cache
ConnectionString  : {{5cc19889e6ed3b0524c3f7d3}}
ResourceId        :
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsof
                    t.ApiManagement/service/contoso/caches/centralus
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="665ff-109">Cmdlet은 Api Management 서비스의 마스터 위치에 새 캐시 엔터티를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="665ff-109">The cmdlets creates a new cache entity in the master location of the Api Management service.</span></span>

## <span data-ttu-id="665ff-110">변수</span><span class="sxs-lookup"><span data-stu-id="665ff-110">PARAMETERS</span></span>

### <span data-ttu-id="665ff-111">-AzureRedisResourceId</span><span class="sxs-lookup"><span data-stu-id="665ff-111">-AzureRedisResourceId</span></span>
<span data-ttu-id="665ff-112">Azure Redis Cache 인스턴스의 Arm ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="665ff-112">Arm ResourceId of the Azure Redis Cache instance.</span></span> <span data-ttu-id="665ff-113">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="665ff-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="665ff-114">-CacheId</span><span class="sxs-lookup"><span data-stu-id="665ff-114">-CacheId</span></span>
<span data-ttu-id="665ff-115">새 캐시의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="665ff-115">Identifier of new cache.</span></span>
<span data-ttu-id="665ff-116">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="665ff-116">This parameter is optional.</span></span>
<span data-ttu-id="665ff-117">지정 하지 않으면가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="665ff-117">If not specified will be generated.</span></span>

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

### <span data-ttu-id="665ff-118">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="665ff-118">-ConnectionString</span></span>
<span data-ttu-id="665ff-119">Redis 연결 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="665ff-119">Redis Connection String.</span></span>
<span data-ttu-id="665ff-120">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="665ff-120">This parameter is required.</span></span>

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

### <span data-ttu-id="665ff-121">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="665ff-121">-Context</span></span>
<span data-ttu-id="665ff-122">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="665ff-122">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="665ff-123">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="665ff-123">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="665ff-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="665ff-124">-DefaultProfile</span></span>
<span data-ttu-id="665ff-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="665ff-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="665ff-126">-설명</span><span class="sxs-lookup"><span data-stu-id="665ff-126">-Description</span></span>
<span data-ttu-id="665ff-127">캐시 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="665ff-127">Cache Description.</span></span>
<span data-ttu-id="665ff-128">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="665ff-128">This parameter is optional.</span></span>

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

### <span data-ttu-id="665ff-129">-확인</span><span class="sxs-lookup"><span data-stu-id="665ff-129">-Confirm</span></span>
<span data-ttu-id="665ff-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="665ff-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="665ff-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="665ff-131">-WhatIf</span></span>
<span data-ttu-id="665ff-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="665ff-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="665ff-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="665ff-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="665ff-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="665ff-134">CommonParameters</span></span>
<span data-ttu-id="665ff-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="665ff-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="665ff-136">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="665ff-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="665ff-137">입력</span><span class="sxs-lookup"><span data-stu-id="665ff-137">INPUTS</span></span>

### <span data-ttu-id="665ff-138">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="665ff-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="665ff-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="665ff-139">System.String</span></span>

## <span data-ttu-id="665ff-140">출력</span><span class="sxs-lookup"><span data-stu-id="665ff-140">OUTPUTS</span></span>

### <span data-ttu-id="665ff-141">ApiManagement. ServiceManagement. \ PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="665ff-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

## <span data-ttu-id="665ff-142">상속자</span><span class="sxs-lookup"><span data-stu-id="665ff-142">NOTES</span></span>

## <span data-ttu-id="665ff-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="665ff-143">RELATED LINKS</span></span>

[<span data-ttu-id="665ff-144">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="665ff-144">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache)

[<span data-ttu-id="665ff-145">Set-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="665ff-145">Set-AzApiManagementCache</span></span>](./Set-AzApiManagementCache.md)

[<span data-ttu-id="665ff-146">제거-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="665ff-146">Remove-AzApiManagementCache</span></span>](./Remove-AzApiManagementCache.md)
