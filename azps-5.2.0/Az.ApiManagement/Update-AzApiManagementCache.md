---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/update-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementCache.md
ms.openlocfilehash: 2ac2eb7cb40cb7df4324aff276137527d4b148a5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98323098"
---
# <span data-ttu-id="ff372-101">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="ff372-101">Update-AzApiManagementCache</span></span>

## <span data-ttu-id="ff372-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff372-102">SYNOPSIS</span></span>
<span data-ttu-id="ff372-103">Api Management 서비스에서 캐시를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ff372-103">updates a cache in Api Management service.</span></span>

## <span data-ttu-id="ff372-104">구문</span><span class="sxs-lookup"><span data-stu-id="ff372-104">SYNTAX</span></span>

### <span data-ttu-id="ff372-105">ExpandedParameter(기본값)</span><span class="sxs-lookup"><span data-stu-id="ff372-105">ExpandedParameter (Default)</span></span>
```
Update-AzApiManagementCache -Context <PsApiManagementContext> -CacheId <String> [-ConnectionString <String>]
 [-AzureRedisResourceId <String>] [-Description <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff372-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ff372-106">ByInputObject</span></span>
```
Update-AzApiManagementCache -InputObject <PsApiManagementCache> [-ConnectionString <String>]
 [-AzureRedisResourceId <String>] [-Description <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff372-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ff372-107">ByResourceId</span></span>
```
Update-AzApiManagementCache -ResourceId <String> [-ConnectionString <String>] [-AzureRedisResourceId <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ff372-108">설명</span><span class="sxs-lookup"><span data-stu-id="ff372-108">DESCRIPTION</span></span>
<span data-ttu-id="ff372-109">Cmdlet **Update-AzApiManagementCache는** ApiManagement 서비스의 캐시를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ff372-109">The cmdlet **Update-AzApiManagementCache** updates a cache in the ApiManagement service.</span></span>

## <span data-ttu-id="ff372-110">예제</span><span class="sxs-lookup"><span data-stu-id="ff372-110">EXAMPLES</span></span>

### <span data-ttu-id="ff372-111">예제 1: 중앙에서 캐시에 대한 설명 업데이트</span><span class="sxs-lookup"><span data-stu-id="ff372-111">Example 1 : Updates the Description of the Cache in centralus</span></span>
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

<span data-ttu-id="ff372-112">미국 중부의 캐시에 대한 설명을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ff372-112">Updates the description of the Cache in Central US.</span></span>

## <span data-ttu-id="ff372-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ff372-113">PARAMETERS</span></span>

### <span data-ttu-id="ff372-114">-AzureRedisResourceId</span><span class="sxs-lookup"><span data-stu-id="ff372-114">-AzureRedisResourceId</span></span>
<span data-ttu-id="ff372-115">Azure Redis Cache 인스턴스의 Arm ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="ff372-115">Arm ResourceId of the Azure Redis Cache instance.</span></span>
<span data-ttu-id="ff372-116">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="ff372-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="ff372-117">-CacheId</span><span class="sxs-lookup"><span data-stu-id="ff372-117">-CacheId</span></span>
<span data-ttu-id="ff372-118">새 캐시의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="ff372-118">Identifier of new cache.</span></span>
<span data-ttu-id="ff372-119">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="ff372-119">This parameter is required.</span></span>

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

### <span data-ttu-id="ff372-120">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="ff372-120">-ConnectionString</span></span>
<span data-ttu-id="ff372-121">Redis 연결 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="ff372-121">Redis Connection String.</span></span>
<span data-ttu-id="ff372-122">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="ff372-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="ff372-123">-Context</span><span class="sxs-lookup"><span data-stu-id="ff372-123">-Context</span></span>
<span data-ttu-id="ff372-124">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="ff372-124">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="ff372-125">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="ff372-125">This parameter is required.</span></span>

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

### <span data-ttu-id="ff372-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff372-126">-DefaultProfile</span></span>
<span data-ttu-id="ff372-127">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ff372-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff372-128">-Description</span><span class="sxs-lookup"><span data-stu-id="ff372-128">-Description</span></span>
<span data-ttu-id="ff372-129">캐시 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="ff372-129">Cache Description.</span></span>
<span data-ttu-id="ff372-130">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="ff372-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="ff372-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ff372-131">-InputObject</span></span>
<span data-ttu-id="ff372-132">PsApiManagementCache의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="ff372-132">Instance of PsApiManagementCache.</span></span>
<span data-ttu-id="ff372-133">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="ff372-133">This parameter is required.</span></span>

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

### <span data-ttu-id="ff372-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ff372-134">-PassThru</span></span>
<span data-ttu-id="ff372-135">지정된 경우 수정된 캐시를 나타내는 Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache 형식의 인스턴스가 출력에 기록됩니다.</span><span class="sxs-lookup"><span data-stu-id="ff372-135">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache type  representing the modified cache will be written to output.</span></span>

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

### <span data-ttu-id="ff372-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ff372-136">-ResourceId</span></span>
<span data-ttu-id="ff372-137">캐시의 Arm ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="ff372-137">Arm ResourceId of Cache.</span></span>
<span data-ttu-id="ff372-138">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="ff372-138">This parameter is required.</span></span>

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

### <span data-ttu-id="ff372-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ff372-139">-Confirm</span></span>
<span data-ttu-id="ff372-140">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ff372-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff372-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff372-141">-WhatIf</span></span>
<span data-ttu-id="ff372-142">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="ff372-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff372-143">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ff372-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff372-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff372-144">CommonParameters</span></span>
<span data-ttu-id="ff372-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ff372-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff372-146">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ff372-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff372-147">입력</span><span class="sxs-lookup"><span data-stu-id="ff372-147">INPUTS</span></span>

### <span data-ttu-id="ff372-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ff372-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ff372-149">System.String</span><span class="sxs-lookup"><span data-stu-id="ff372-149">System.String</span></span>

### <span data-ttu-id="ff372-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="ff372-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

### <span data-ttu-id="ff372-151">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ff372-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ff372-152">출력</span><span class="sxs-lookup"><span data-stu-id="ff372-152">OUTPUTS</span></span>

### <span data-ttu-id="ff372-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="ff372-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

## <span data-ttu-id="ff372-154">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ff372-154">NOTES</span></span>

## <span data-ttu-id="ff372-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ff372-155">RELATED LINKS</span></span>

[<span data-ttu-id="ff372-156">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="ff372-156">New-AzApiManagementCache</span></span>](./New-AzApiManagementCache.md)

[<span data-ttu-id="ff372-157">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="ff372-157">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache.md)

[<span data-ttu-id="ff372-158">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="ff372-158">Remove-AzApiManagementCache</span></span>](./Remove-AzApiManagementCache.md)
