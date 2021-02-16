---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCache.md
ms.openlocfilehash: cfa2024064256b780121aeb489a3e8988b0a688e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195409"
---
# <span data-ttu-id="5fac1-101">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="5fac1-101">New-AzApiManagementCache</span></span>

## <span data-ttu-id="5fac1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5fac1-102">SYNOPSIS</span></span>
<span data-ttu-id="5fac1-103">새 캐시 엔터티를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5fac1-103">Creates a new Cache entity</span></span>

## <span data-ttu-id="5fac1-104">구문</span><span class="sxs-lookup"><span data-stu-id="5fac1-104">SYNTAX</span></span>

```
New-AzApiManagementCache -Context <PsApiManagementContext> [-CacheId <String>] -ConnectionString <String>
 [-AzureRedisResourceId <String>] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5fac1-105">설명</span><span class="sxs-lookup"><span data-stu-id="5fac1-105">DESCRIPTION</span></span>
<span data-ttu-id="5fac1-106">**New-AzApiManagementCache** cmdlet은 Api Management 서비스에 새 캐시 엔터티를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5fac1-106">The cmdlet **New-AzApiManagementCache** creates a new cache entity in Api Management service.</span></span>

## <span data-ttu-id="5fac1-107">예제</span><span class="sxs-lookup"><span data-stu-id="5fac1-107">EXAMPLES</span></span>

### <span data-ttu-id="5fac1-108">예제 1: 새 캐시 엔터티 만들기</span><span class="sxs-lookup"><span data-stu-id="5fac1-108">Example 1 : Create a new Cache entity</span></span>
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

<span data-ttu-id="5fac1-109">cmdlet은 Api Management 서비스의 마스터 위치에 새 캐시 엔터티를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5fac1-109">The cmdlets creates a new cache entity in the master location of the Api Management service.</span></span>

## <span data-ttu-id="5fac1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5fac1-110">PARAMETERS</span></span>

### <span data-ttu-id="5fac1-111">-AzureRedisResourceId</span><span class="sxs-lookup"><span data-stu-id="5fac1-111">-AzureRedisResourceId</span></span>
<span data-ttu-id="5fac1-112">Azure Redis Cache 인스턴스의 Arm ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="5fac1-112">Arm ResourceId of the Azure Redis Cache instance.</span></span> <span data-ttu-id="5fac1-113">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="5fac1-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="5fac1-114">-CacheId</span><span class="sxs-lookup"><span data-stu-id="5fac1-114">-CacheId</span></span>
<span data-ttu-id="5fac1-115">새 캐시의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="5fac1-115">Identifier of new cache.</span></span>
<span data-ttu-id="5fac1-116">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="5fac1-116">This parameter is optional.</span></span>
<span data-ttu-id="5fac1-117">지정하지 않으면 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="5fac1-117">If not specified will be generated.</span></span>

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

### <span data-ttu-id="5fac1-118">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="5fac1-118">-ConnectionString</span></span>
<span data-ttu-id="5fac1-119">Redis 연결 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="5fac1-119">Redis Connection String.</span></span>
<span data-ttu-id="5fac1-120">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="5fac1-120">This parameter is required.</span></span>

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

### <span data-ttu-id="5fac1-121">-Context</span><span class="sxs-lookup"><span data-stu-id="5fac1-121">-Context</span></span>
<span data-ttu-id="5fac1-122">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="5fac1-122">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="5fac1-123">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="5fac1-123">This parameter is required.</span></span>

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

### <span data-ttu-id="5fac1-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fac1-124">-DefaultProfile</span></span>
<span data-ttu-id="5fac1-125">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5fac1-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5fac1-126">-Description</span><span class="sxs-lookup"><span data-stu-id="5fac1-126">-Description</span></span>
<span data-ttu-id="5fac1-127">캐시 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="5fac1-127">Cache Description.</span></span>
<span data-ttu-id="5fac1-128">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="5fac1-128">This parameter is optional.</span></span>

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

### <span data-ttu-id="5fac1-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5fac1-129">-Confirm</span></span>
<span data-ttu-id="5fac1-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5fac1-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5fac1-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fac1-131">-WhatIf</span></span>
<span data-ttu-id="5fac1-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="5fac1-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5fac1-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5fac1-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5fac1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fac1-134">CommonParameters</span></span>
<span data-ttu-id="5fac1-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5fac1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fac1-136">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5fac1-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fac1-137">입력</span><span class="sxs-lookup"><span data-stu-id="5fac1-137">INPUTS</span></span>

### <span data-ttu-id="5fac1-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="5fac1-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="5fac1-139">System.String</span><span class="sxs-lookup"><span data-stu-id="5fac1-139">System.String</span></span>

## <span data-ttu-id="5fac1-140">출력</span><span class="sxs-lookup"><span data-stu-id="5fac1-140">OUTPUTS</span></span>

### <span data-ttu-id="5fac1-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="5fac1-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

## <span data-ttu-id="5fac1-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5fac1-142">NOTES</span></span>

## <span data-ttu-id="5fac1-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5fac1-143">RELATED LINKS</span></span>

[<span data-ttu-id="5fac1-144">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="5fac1-144">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache.md)

[<span data-ttu-id="5fac1-145">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="5fac1-145">Remove-AzApiManagementCache</span></span>](./Remove-AzApiManagementCache.md)

[<span data-ttu-id="5fac1-146">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="5fac1-146">Update-AzApiManagementCache</span></span>](./Update-AzApiManagementCache.md)