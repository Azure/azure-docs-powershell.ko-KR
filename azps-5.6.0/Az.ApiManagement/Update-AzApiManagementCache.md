---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/update-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementCache.md
ms.openlocfilehash: 8c7b423090de10ea1573d268dcc3c301ec4b206d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001947"
---
# <span data-ttu-id="c327b-101">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="c327b-101">Update-AzApiManagementCache</span></span>

## <span data-ttu-id="c327b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c327b-102">SYNOPSIS</span></span>
<span data-ttu-id="c327b-103">Api Management 서비스의 캐시를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c327b-103">updates a cache in Api Management service.</span></span>

## <span data-ttu-id="c327b-104">구문</span><span class="sxs-lookup"><span data-stu-id="c327b-104">SYNTAX</span></span>

### <span data-ttu-id="c327b-105">ExpandedParameter(기본값)</span><span class="sxs-lookup"><span data-stu-id="c327b-105">ExpandedParameter (Default)</span></span>
```
Update-AzApiManagementCache -Context <PsApiManagementContext> -CacheId <String> [-ConnectionString <String>]
 [-AzureRedisResourceId <String>] [-Description <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c327b-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c327b-106">ByInputObject</span></span>
```
Update-AzApiManagementCache -InputObject <PsApiManagementCache> [-ConnectionString <String>]
 [-AzureRedisResourceId <String>] [-Description <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c327b-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c327b-107">ByResourceId</span></span>
```
Update-AzApiManagementCache -ResourceId <String> [-ConnectionString <String>] [-AzureRedisResourceId <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c327b-108">설명</span><span class="sxs-lookup"><span data-stu-id="c327b-108">DESCRIPTION</span></span>
<span data-ttu-id="c327b-109">cmdlet **Update-AzApiManagementCache는 ApiManagement** 서비스의 캐시를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c327b-109">The cmdlet **Update-AzApiManagementCache** updates a cache in the ApiManagement service.</span></span>

## <span data-ttu-id="c327b-110">예제</span><span class="sxs-lookup"><span data-stu-id="c327b-110">EXAMPLES</span></span>

### <span data-ttu-id="c327b-111">예제 1: 중앙에서 캐시 설명 업데이트</span><span class="sxs-lookup"><span data-stu-id="c327b-111">Example 1 : Updates the Description of the Cache in centralus</span></span>
```powershell
PS D:\github\azure-powershell> $context=New-AzApiManagementContext -ResourceGroupName Api-Default-Central-US -ServiceName contoso
PS D:\github\azure-powershell> Update-AzApiManagementCache -Context $context -CacheId centralus -Description "Team new cache" -PassThru


CacheId              : centralus
Description          : Team new cache
ConnectionString     : {{5cc19889e6ed3b0524c3f7d3}}
AzureRedisResourceId :
Id                   : /subscriptions/subid/resourceGroups/Api-Default-Central-US/providers/M
                       icrosoft.ApiManagement/service/contoso/caches/centralus
ResourceGroupName    : Api-Default-Central-US
ServiceName          : contoso
```

<span data-ttu-id="c327b-112">미국 중부의 캐시에 대한 설명을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c327b-112">Updates the description of the Cache in Central US.</span></span>

## <span data-ttu-id="c327b-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c327b-113">PARAMETERS</span></span>

### <span data-ttu-id="c327b-114">-AzureRedisResourceId</span><span class="sxs-lookup"><span data-stu-id="c327b-114">-AzureRedisResourceId</span></span>
<span data-ttu-id="c327b-115">Azure Redis Cache 인스턴스의 Arm ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="c327b-115">Arm ResourceId of the Azure Redis Cache instance.</span></span>
<span data-ttu-id="c327b-116">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="c327b-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="c327b-117">-CacheId</span><span class="sxs-lookup"><span data-stu-id="c327b-117">-CacheId</span></span>
<span data-ttu-id="c327b-118">새 캐시의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="c327b-118">Identifier of new cache.</span></span>
<span data-ttu-id="c327b-119">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="c327b-119">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c327b-120">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="c327b-120">-ConnectionString</span></span>
<span data-ttu-id="c327b-121">Redis 연결 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="c327b-121">Redis Connection String.</span></span>
<span data-ttu-id="c327b-122">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="c327b-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="c327b-123">-Context</span><span class="sxs-lookup"><span data-stu-id="c327b-123">-Context</span></span>
<span data-ttu-id="c327b-124">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="c327b-124">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="c327b-125">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="c327b-125">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c327b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c327b-126">-DefaultProfile</span></span>
<span data-ttu-id="c327b-127">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c327b-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c327b-128">-Description</span><span class="sxs-lookup"><span data-stu-id="c327b-128">-Description</span></span>
<span data-ttu-id="c327b-129">캐시 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="c327b-129">Cache Description.</span></span>
<span data-ttu-id="c327b-130">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="c327b-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="c327b-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c327b-131">-InputObject</span></span>
<span data-ttu-id="c327b-132">PsApiManagementCache의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="c327b-132">Instance of PsApiManagementCache.</span></span>
<span data-ttu-id="c327b-133">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="c327b-133">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c327b-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c327b-134">-PassThru</span></span>
<span data-ttu-id="c327b-135">지정된 경우 Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache 형식의 인스턴스를 출력에 기록합니다.</span><span class="sxs-lookup"><span data-stu-id="c327b-135">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache type  representing the modified cache will be written to output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c327b-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c327b-136">-ResourceId</span></span>
<span data-ttu-id="c327b-137">Cache의 Arm ResourceId.</span><span class="sxs-lookup"><span data-stu-id="c327b-137">Arm ResourceId of Cache.</span></span>
<span data-ttu-id="c327b-138">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="c327b-138">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c327b-139">-확인</span><span class="sxs-lookup"><span data-stu-id="c327b-139">-Confirm</span></span>
<span data-ttu-id="c327b-140">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c327b-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c327b-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c327b-141">-WhatIf</span></span>
<span data-ttu-id="c327b-142">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="c327b-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c327b-143">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c327b-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c327b-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c327b-144">CommonParameters</span></span>
<span data-ttu-id="c327b-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c327b-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c327b-146">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c327b-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c327b-147">입력</span><span class="sxs-lookup"><span data-stu-id="c327b-147">INPUTS</span></span>

### <span data-ttu-id="c327b-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c327b-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c327b-149">System.String</span><span class="sxs-lookup"><span data-stu-id="c327b-149">System.String</span></span>

### <span data-ttu-id="c327b-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="c327b-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

### <span data-ttu-id="c327b-151">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c327b-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c327b-152">출력</span><span class="sxs-lookup"><span data-stu-id="c327b-152">OUTPUTS</span></span>

### <span data-ttu-id="c327b-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="c327b-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

## <span data-ttu-id="c327b-154">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c327b-154">NOTES</span></span>

## <span data-ttu-id="c327b-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c327b-155">RELATED LINKS</span></span>

[<span data-ttu-id="c327b-156">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="c327b-156">New-AzApiManagementCache</span></span>](./New-AzApiManagementCache.md)

[<span data-ttu-id="c327b-157">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="c327b-157">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache.md)

[<span data-ttu-id="c327b-158">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="c327b-158">Remove-AzApiManagementCache</span></span>](./Remove-AzApiManagementCache.md)
