---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: A8C6F3BC-EE93-49A4-BF7B-8420967EEB7B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnEndpoint.md
ms.openlocfilehash: 9d8704abaeb5fd320a871b7b15720af3bbb0c472
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869221"
---
# <span data-ttu-id="352e2-101">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="352e2-101">New-AzCdnEndpoint</span></span>

## <span data-ttu-id="352e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="352e2-102">SYNOPSIS</span></span>
<span data-ttu-id="352e2-103">CDN 끝점을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="352e2-103">Creates a CDN endpoint.</span></span>

## <span data-ttu-id="352e2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="352e2-104">SYNTAX</span></span>

### <span data-ttu-id="352e2-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="352e2-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> -Location <String>
 [-OriginHostHeader <String>] [-OriginPath <String>] [-ContentTypesToCompress <String[]>]
 [-IsCompressionEnabled <Boolean>] [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-ProbePath <String>]
 [-GeoFilters <PSGeoFilter[]>] [-DeliveryPolicy <PSDeliveryPolicy>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="352e2-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="352e2-106">ByObjectParameterSet</span></span>
```
New-AzCdnEndpoint -EndpointName <String> -CdnProfile <PSProfile> [-OriginHostHeader <String>]
 [-OriginPath <String>] [-ContentTypesToCompress <String[]>] [-IsCompressionEnabled <Boolean>]
 [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-ProbePath <String>]
 [-GeoFilters <PSGeoFilter[]>] [-DeliveryPolicy <PSDeliveryPolicy>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="352e2-107">설명은</span><span class="sxs-lookup"><span data-stu-id="352e2-107">DESCRIPTION</span></span>
<span data-ttu-id="352e2-108">**AzCdnEndpoint** CMDLET은 CDN (Azure Content Delivery Network) 끝점을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="352e2-108">The **New-AzCdnEndpoint** cmdlet creates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="352e2-109">예제의</span><span class="sxs-lookup"><span data-stu-id="352e2-109">EXAMPLES</span></span>

## <span data-ttu-id="352e2-110">변수</span><span class="sxs-lookup"><span data-stu-id="352e2-110">PARAMETERS</span></span>

### <span data-ttu-id="352e2-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="352e2-111">-CdnProfile</span></span>
<span data-ttu-id="352e2-112">끝점을 추가할 CDN 프로필 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="352e2-112">Specifies the CDN profile object to which the endpoint is added.</span></span>

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

### <span data-ttu-id="352e2-113">-ContentTypesToCompress</span><span class="sxs-lookup"><span data-stu-id="352e2-113">-ContentTypesToCompress</span></span>
<span data-ttu-id="352e2-114">Edge 노드에서 클라이언트로 압축할 콘텐츠 형식의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="352e2-114">Specifies an array of content types to compress from the edge node to the client.</span></span>

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

### <span data-ttu-id="352e2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="352e2-115">-DefaultProfile</span></span>
<span data-ttu-id="352e2-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="352e2-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="352e2-117">-배달 Ypolicy</span><span class="sxs-lookup"><span data-stu-id="352e2-117">-DeliveryPolicy</span></span>
<span data-ttu-id="352e2-118">이 끝점에 대 한 배달 정책입니다.</span><span class="sxs-lookup"><span data-stu-id="352e2-118">The delivery policy for this endpoint.</span></span>

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

### <span data-ttu-id="352e2-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="352e2-119">-EndpointName</span></span>
<span data-ttu-id="352e2-120">끝점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="352e2-120">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="352e2-121">-GeoFilters</span><span class="sxs-lookup"><span data-stu-id="352e2-121">-GeoFilters</span></span>
<span data-ttu-id="352e2-122">이 끝점에 적용 되는 지리적 필터 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="352e2-122">The list of geo filters that applies to this endpoint.</span></span>

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

### <span data-ttu-id="352e2-123">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="352e2-123">-HttpPort</span></span>
<span data-ttu-id="352e2-124">원본 서버의 HTTP 포트 번호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="352e2-124">Specifies the HTTP port number on the origin server.</span></span>

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

### <span data-ttu-id="352e2-125">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="352e2-125">-HttpsPort</span></span>
<span data-ttu-id="352e2-126">원본 서버의 HTTPS 포트 번호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="352e2-126">Specifies the HTTPS port number on the origin server.</span></span>

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

### <span data-ttu-id="352e2-127">-IsCompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="352e2-127">-IsCompressionEnabled</span></span>
<span data-ttu-id="352e2-128">끝점에 압축을 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="352e2-128">Indicates whether compression is enabled for the endpoint.</span></span>

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

### <span data-ttu-id="352e2-129">-IsHttpAllowed</span><span class="sxs-lookup"><span data-stu-id="352e2-129">-IsHttpAllowed</span></span>
<span data-ttu-id="352e2-130">끝점에서 HTTP 트래픽을 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="352e2-130">Indicates whether the endpoint enables HTTP traffic.</span></span>

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

### <span data-ttu-id="352e2-131">-IsHttpsAllowed</span><span class="sxs-lookup"><span data-stu-id="352e2-131">-IsHttpsAllowed</span></span>
<span data-ttu-id="352e2-132">끝점에서 HTTPS 트래픽을 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="352e2-132">Indicates whether the endpoint enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="352e2-133">-위치</span><span class="sxs-lookup"><span data-stu-id="352e2-133">-Location</span></span>
<span data-ttu-id="352e2-134">끝점의 리소스 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="352e2-134">Specifies the resource location of the endpoint.</span></span>

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

### <span data-ttu-id="352e2-135">-OptimizationType</span><span class="sxs-lookup"><span data-stu-id="352e2-135">-OptimizationType</span></span>
<span data-ttu-id="352e2-136">이 끝점의 최적화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="352e2-136">Specifies any optimization this endpoint has.</span></span>

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

### <span data-ttu-id="352e2-137">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="352e2-137">-OriginHostHeader</span></span>
<span data-ttu-id="352e2-138">끝점의 원본 호스트 헤드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="352e2-138">Specifies the origin host head of the endpoint.</span></span>

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

### <span data-ttu-id="352e2-139">-OriginHostName</span><span class="sxs-lookup"><span data-stu-id="352e2-139">-OriginHostName</span></span>
<span data-ttu-id="352e2-140">원본 서버의 호스트 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="352e2-140">Specifies the host name of the origin server.</span></span>

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

### <span data-ttu-id="352e2-141">-OriginName</span><span class="sxs-lookup"><span data-stu-id="352e2-141">-OriginName</span></span>
<span data-ttu-id="352e2-142">원본 서버의 리소스 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="352e2-142">Specifies the resource name of the origin server.</span></span>

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

### <span data-ttu-id="352e2-143">-OriginPath</span><span class="sxs-lookup"><span data-stu-id="352e2-143">-OriginPath</span></span>
<span data-ttu-id="352e2-144">원본 서버의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="352e2-144">Specifies the path of the origin server.</span></span>

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

### <span data-ttu-id="352e2-145">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="352e2-145">-ProbePath</span></span>
<span data-ttu-id="352e2-146">동적 사이트 가속에 대 한 프로브 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="352e2-146">Specifies the probe path for Dynamic Site Acceleration</span></span>

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

### <span data-ttu-id="352e2-147">-/Profile</span><span class="sxs-lookup"><span data-stu-id="352e2-147">-ProfileName</span></span>
<span data-ttu-id="352e2-148">프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="352e2-148">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="352e2-149">-QueryStringCachingBehavior</span><span class="sxs-lookup"><span data-stu-id="352e2-149">-QueryStringCachingBehavior</span></span>
<span data-ttu-id="352e2-150">쿼리 문자열이 요청 URL에 있을 때 CDN 끝점의 동작을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="352e2-150">Specifies the behavior of CDN endpoint when a query string is in the request URL.</span></span>

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

### <span data-ttu-id="352e2-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="352e2-151">-ResourceGroupName</span></span>
<span data-ttu-id="352e2-152">이 끝점이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="352e2-152">Specifies the name of the resource group to which this endpoint belongs.</span></span>

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

### <span data-ttu-id="352e2-153">태그</span><span class="sxs-lookup"><span data-stu-id="352e2-153">-Tag</span></span>
<span data-ttu-id="352e2-154">Azure CDN 끝점과 연결할 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="352e2-154">The tags to associate with the Azure CDN endpoint.</span></span>

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

### <span data-ttu-id="352e2-155">-확인</span><span class="sxs-lookup"><span data-stu-id="352e2-155">-Confirm</span></span>
<span data-ttu-id="352e2-156">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="352e2-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="352e2-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="352e2-157">-WhatIf</span></span>
<span data-ttu-id="352e2-158">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="352e2-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="352e2-159">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="352e2-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="352e2-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="352e2-160">CommonParameters</span></span>
<span data-ttu-id="352e2-161">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="352e2-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="352e2-162">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="352e2-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="352e2-163">입력</span><span class="sxs-lookup"><span data-stu-id="352e2-163">INPUTS</span></span>

### <span data-ttu-id="352e2-164">Microsoft. Cdn. 프로필. PSProfile</span><span class="sxs-lookup"><span data-stu-id="352e2-164">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="352e2-165">출력</span><span class="sxs-lookup"><span data-stu-id="352e2-165">OUTPUTS</span></span>

### <span data-ttu-id="352e2-166">Microsoft. Cdn. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="352e2-166">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="352e2-167">상속자</span><span class="sxs-lookup"><span data-stu-id="352e2-167">NOTES</span></span>

## <span data-ttu-id="352e2-168">관련 링크</span><span class="sxs-lookup"><span data-stu-id="352e2-168">RELATED LINKS</span></span>

[<span data-ttu-id="352e2-169">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="352e2-169">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="352e2-170">제거-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="352e2-170">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="352e2-171">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="352e2-171">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="352e2-172">시작-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="352e2-172">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="352e2-173">중지-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="352e2-173">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


