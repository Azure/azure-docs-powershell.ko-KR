---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: A8C6F3BC-EE93-49A4-BF7B-8420967EEB7B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnEndpoint.md
ms.openlocfilehash: ba06dcabe874161c9f801841a5be8b0337614799
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048467"
---
# <span data-ttu-id="cf21f-101">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="cf21f-101">New-AzCdnEndpoint</span></span>

## <span data-ttu-id="cf21f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf21f-102">SYNOPSIS</span></span>
<span data-ttu-id="cf21f-103">CDN 끝점을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cf21f-103">Creates a CDN endpoint.</span></span>

## <span data-ttu-id="cf21f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cf21f-104">SYNTAX</span></span>

### <span data-ttu-id="cf21f-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="cf21f-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> -Location <String>
 [-OriginHostHeader <String>] [-OriginPath <String>] [-ContentTypesToCompress <String[]>]
 [-IsCompressionEnabled <Boolean>] [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-ProbePath <String>]
 [-GeoFilters <PSGeoFilter[]>] [-DeliveryPolicy <PSDeliveryPolicy>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf21f-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf21f-106">ByObjectParameterSet</span></span>
```
New-AzCdnEndpoint -EndpointName <String> -CdnProfile <PSProfile> [-OriginHostHeader <String>]
 [-OriginPath <String>] [-ContentTypesToCompress <String[]>] [-IsCompressionEnabled <Boolean>]
 [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-ProbePath <String>]
 [-GeoFilters <PSGeoFilter[]>] [-DeliveryPolicy <PSDeliveryPolicy>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf21f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="cf21f-107">DESCRIPTION</span></span>
<span data-ttu-id="cf21f-108">**AzCdnEndpoint** CMDLET은 CDN (Azure Content Delivery Network) 끝점을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cf21f-108">The **New-AzCdnEndpoint** cmdlet creates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="cf21f-109">예제의</span><span class="sxs-lookup"><span data-stu-id="cf21f-109">EXAMPLES</span></span>

## <span data-ttu-id="cf21f-110">변수</span><span class="sxs-lookup"><span data-stu-id="cf21f-110">PARAMETERS</span></span>

### <span data-ttu-id="cf21f-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="cf21f-111">-CdnProfile</span></span>
<span data-ttu-id="cf21f-112">끝점을 추가할 CDN 프로필 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf21f-112">Specifies the CDN profile object to which the endpoint is added.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf21f-113">-ContentTypesToCompress</span><span class="sxs-lookup"><span data-stu-id="cf21f-113">-ContentTypesToCompress</span></span>
<span data-ttu-id="cf21f-114">Edge 노드에서 클라이언트로 압축할 콘텐츠 형식의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf21f-114">Specifies an array of content types to compress from the edge node to the client.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf21f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf21f-115">-DefaultProfile</span></span>
<span data-ttu-id="cf21f-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="cf21f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cf21f-117">-배달 Ypolicy</span><span class="sxs-lookup"><span data-stu-id="cf21f-117">-DeliveryPolicy</span></span>
<span data-ttu-id="cf21f-118">이 끝점에 대 한 배달 정책입니다.</span><span class="sxs-lookup"><span data-stu-id="cf21f-118">The delivery policy for this endpoint.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf21f-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="cf21f-119">-EndpointName</span></span>
<span data-ttu-id="cf21f-120">끝점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf21f-120">Specifies the name of the endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf21f-121">-GeoFilters</span><span class="sxs-lookup"><span data-stu-id="cf21f-121">-GeoFilters</span></span>
<span data-ttu-id="cf21f-122">이 끝점에 적용 되는 지리적 필터 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="cf21f-122">The list of geo filters that applies to this endpoint.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSGeoFilter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf21f-123">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="cf21f-123">-HttpPort</span></span>
<span data-ttu-id="cf21f-124">원본 서버의 HTTP 포트 번호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf21f-124">Specifies the HTTP port number on the origin server.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf21f-125">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="cf21f-125">-HttpsPort</span></span>
<span data-ttu-id="cf21f-126">원본 서버의 HTTPS 포트 번호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf21f-126">Specifies the HTTPS port number on the origin server.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf21f-127">-IsCompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="cf21f-127">-IsCompressionEnabled</span></span>
<span data-ttu-id="cf21f-128">끝점에 압축을 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="cf21f-128">Indicates whether compression is enabled for the endpoint.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf21f-129">-IsHttpAllowed</span><span class="sxs-lookup"><span data-stu-id="cf21f-129">-IsHttpAllowed</span></span>
<span data-ttu-id="cf21f-130">끝점에서 HTTP 트래픽을 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="cf21f-130">Indicates whether the endpoint enables HTTP traffic.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf21f-131">-IsHttpsAllowed</span><span class="sxs-lookup"><span data-stu-id="cf21f-131">-IsHttpsAllowed</span></span>
<span data-ttu-id="cf21f-132">끝점에서 HTTPS 트래픽을 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="cf21f-132">Indicates whether the endpoint enables HTTPS traffic.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf21f-133">-위치</span><span class="sxs-lookup"><span data-stu-id="cf21f-133">-Location</span></span>
<span data-ttu-id="cf21f-134">끝점의 리소스 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf21f-134">Specifies the resource location of the endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf21f-135">-OptimizationType</span><span class="sxs-lookup"><span data-stu-id="cf21f-135">-OptimizationType</span></span>
<span data-ttu-id="cf21f-136">이 끝점의 최적화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf21f-136">Specifies any optimization this endpoint has.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf21f-137">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="cf21f-137">-OriginHostHeader</span></span>
<span data-ttu-id="cf21f-138">끝점의 원본 호스트 헤드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf21f-138">Specifies the origin host head of the endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf21f-139">-OriginHostName</span><span class="sxs-lookup"><span data-stu-id="cf21f-139">-OriginHostName</span></span>
<span data-ttu-id="cf21f-140">원본 서버의 호스트 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf21f-140">Specifies the host name of the origin server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf21f-141">-OriginName</span><span class="sxs-lookup"><span data-stu-id="cf21f-141">-OriginName</span></span>
<span data-ttu-id="cf21f-142">원본 서버의 리소스 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf21f-142">Specifies the resource name of the origin server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf21f-143">-OriginPath</span><span class="sxs-lookup"><span data-stu-id="cf21f-143">-OriginPath</span></span>
<span data-ttu-id="cf21f-144">원본 서버의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf21f-144">Specifies the path of the origin server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf21f-145">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="cf21f-145">-ProbePath</span></span>
<span data-ttu-id="cf21f-146">동적 사이트 가속에 대 한 프로브 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf21f-146">Specifies the probe path for Dynamic Site Acceleration</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf21f-147">-/Profile</span><span class="sxs-lookup"><span data-stu-id="cf21f-147">-ProfileName</span></span>
<span data-ttu-id="cf21f-148">프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf21f-148">Specifies the name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf21f-149">-QueryStringCachingBehavior</span><span class="sxs-lookup"><span data-stu-id="cf21f-149">-QueryStringCachingBehavior</span></span>
<span data-ttu-id="cf21f-150">쿼리 문자열이 요청 URL에 있을 때 CDN 끝점의 동작을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf21f-150">Specifies the behavior of CDN endpoint when a query string is in the request URL.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSQueryStringCachingBehavior]
Parameter Sets: (All)
Aliases:
Accepted values: IgnoreQueryString, BypassCaching, UseQueryString, NotSet

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf21f-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf21f-151">-ResourceGroupName</span></span>
<span data-ttu-id="cf21f-152">이 끝점이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf21f-152">Specifies the name of the resource group to which this endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf21f-153">태그</span><span class="sxs-lookup"><span data-stu-id="cf21f-153">-Tag</span></span>
<span data-ttu-id="cf21f-154">Azure CDN 끝점과 연결할 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="cf21f-154">The tags to associate with the Azure CDN endpoint.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf21f-155">-확인</span><span class="sxs-lookup"><span data-stu-id="cf21f-155">-Confirm</span></span>
<span data-ttu-id="cf21f-156">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf21f-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf21f-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf21f-157">-WhatIf</span></span>
<span data-ttu-id="cf21f-158">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="cf21f-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf21f-159">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cf21f-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf21f-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf21f-160">CommonParameters</span></span>
<span data-ttu-id="cf21f-161">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf21f-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf21f-162">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cf21f-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf21f-163">입력</span><span class="sxs-lookup"><span data-stu-id="cf21f-163">INPUTS</span></span>

### <span data-ttu-id="cf21f-164">Microsoft. Cdn. 프로필. PSProfile</span><span class="sxs-lookup"><span data-stu-id="cf21f-164">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="cf21f-165">출력</span><span class="sxs-lookup"><span data-stu-id="cf21f-165">OUTPUTS</span></span>

### <span data-ttu-id="cf21f-166">Microsoft. Cdn. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="cf21f-166">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="cf21f-167">상속자</span><span class="sxs-lookup"><span data-stu-id="cf21f-167">NOTES</span></span>

## <span data-ttu-id="cf21f-168">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cf21f-168">RELATED LINKS</span></span>

[<span data-ttu-id="cf21f-169">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="cf21f-169">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="cf21f-170">제거-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="cf21f-170">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="cf21f-171">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="cf21f-171">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="cf21f-172">시작-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="cf21f-172">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="cf21f-173">중지-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="cf21f-173">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


