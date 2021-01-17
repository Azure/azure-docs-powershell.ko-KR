---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: A8C6F3BC-EE93-49A4-BF7B-8420967EEB7B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnEndpoint.md
ms.openlocfilehash: 9e0b8ee74ff89f4a5903df1c73dc7b289b0371c4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361817"
---
# <span data-ttu-id="af16f-101">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="af16f-101">New-AzCdnEndpoint</span></span>

## <span data-ttu-id="af16f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af16f-102">SYNOPSIS</span></span>
<span data-ttu-id="af16f-103">CDN 엔드포인트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="af16f-103">Creates a CDN endpoint.</span></span>

## <span data-ttu-id="af16f-104">구문</span><span class="sxs-lookup"><span data-stu-id="af16f-104">SYNTAX</span></span>

### <span data-ttu-id="af16f-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="af16f-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> -Location <String>
 [-OriginHostHeader <String>] [-OriginPath <String>] [-ContentTypesToCompress <String[]>]
 [-IsCompressionEnabled <Boolean>] [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-ProbePath <String>]
 [-GeoFilters <PSGeoFilter[]>] [-DeliveryPolicy <PSDeliveryPolicy>] [-Tag <Hashtable>]
 [-DefaultOriginGroup <String>] [-Priority <Int32>] [-Weight <Int32>] [-PrivateLinkApprovalMessage <String>]
 [-PrivateLinkLocation <String>] [-PrivateLinkResourceId <String>]
 [-OriginId <System.Collections.Generic.List`1[System.String]>] [-OriginGroupName <String>]
 [-OriginGroupProbeIntervalInSeconds <Int32>] [-OriginGroupProbePath <String>]
 [-OriginGroupProbeProtocol <String>] [-OriginGroupProbeRequestType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af16f-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="af16f-106">ByObjectParameterSet</span></span>
```
New-AzCdnEndpoint -EndpointName <String> -CdnProfile <PSProfile> [-OriginHostHeader <String>]
 [-OriginPath <String>] [-ContentTypesToCompress <String[]>] [-IsCompressionEnabled <Boolean>]
 [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-ProbePath <String>]
 [-GeoFilters <PSGeoFilter[]>] [-DeliveryPolicy <PSDeliveryPolicy>] [-Tag <Hashtable>]
 [-DefaultOriginGroup <String>] [-Priority <Int32>] [-Weight <Int32>] [-PrivateLinkApprovalMessage <String>]
 [-PrivateLinkLocation <String>] [-PrivateLinkResourceId <String>]
 [-OriginId <System.Collections.Generic.List`1[System.String]>] [-OriginGroupName <String>]
 [-OriginGroupProbeIntervalInSeconds <Int32>] [-OriginGroupProbePath <String>]
 [-OriginGroupProbeProtocol <String>] [-OriginGroupProbeRequestType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af16f-107">설명</span><span class="sxs-lookup"><span data-stu-id="af16f-107">DESCRIPTION</span></span>
<span data-ttu-id="af16f-108">**New-AzCdnEndpoint** cmdlet은 Azure CDN(Content Delivery Network) 엔드포인트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="af16f-108">The **New-AzCdnEndpoint** cmdlet creates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="af16f-109">예제</span><span class="sxs-lookup"><span data-stu-id="af16f-109">EXAMPLES</span></span>

## <span data-ttu-id="af16f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="af16f-110">PARAMETERS</span></span>

### <span data-ttu-id="af16f-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="af16f-111">-CdnProfile</span></span>
<span data-ttu-id="af16f-112">엔드포인트가 추가될 CDN 프로필 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="af16f-112">Specifies the CDN profile object to which the endpoint is added.</span></span>

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

### <span data-ttu-id="af16f-113">-ContentTypesToCompress</span><span class="sxs-lookup"><span data-stu-id="af16f-113">-ContentTypesToCompress</span></span>
<span data-ttu-id="af16f-114">에지 노드에서 클라이언트로 압축할 콘텐츠 형식의 배열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="af16f-114">Specifies an array of content types to compress from the edge node to the client.</span></span>

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

### <span data-ttu-id="af16f-115">-DefaultOriginGroup</span><span class="sxs-lookup"><span data-stu-id="af16f-115">-DefaultOriginGroup</span></span>
<span data-ttu-id="af16f-116">기본 원본 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="af16f-116">The default origin group.</span></span>

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

### <span data-ttu-id="af16f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af16f-117">-DefaultProfile</span></span>
<span data-ttu-id="af16f-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="af16f-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="af16f-119">-DeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="af16f-119">-DeliveryPolicy</span></span>
<span data-ttu-id="af16f-120">이 엔드포인트에 대한 배달 정책입니다.</span><span class="sxs-lookup"><span data-stu-id="af16f-120">The delivery policy for this endpoint.</span></span>

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

### <span data-ttu-id="af16f-121">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="af16f-121">-EndpointName</span></span>
<span data-ttu-id="af16f-122">엔드포인트의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="af16f-122">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="af16f-123">-GeoFilters</span><span class="sxs-lookup"><span data-stu-id="af16f-123">-GeoFilters</span></span>
<span data-ttu-id="af16f-124">이 엔드포인트에 적용되는 지역 필터 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="af16f-124">The list of geo filters that applies to this endpoint.</span></span>

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

### <span data-ttu-id="af16f-125">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="af16f-125">-HttpPort</span></span>
<span data-ttu-id="af16f-126">원본 서버의 HTTP 포트 번호를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="af16f-126">Specifies the HTTP port number on the origin server.</span></span>

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

### <span data-ttu-id="af16f-127">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="af16f-127">-HttpsPort</span></span>
<span data-ttu-id="af16f-128">원본 서버의 HTTPS 포트 번호를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="af16f-128">Specifies the HTTPS port number on the origin server.</span></span>

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

### <span data-ttu-id="af16f-129">-IsCompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="af16f-129">-IsCompressionEnabled</span></span>
<span data-ttu-id="af16f-130">엔드포인트에 대해 압축을 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="af16f-130">Indicates whether compression is enabled for the endpoint.</span></span>

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

### <span data-ttu-id="af16f-131">-IsHttpAllowed</span><span class="sxs-lookup"><span data-stu-id="af16f-131">-IsHttpAllowed</span></span>
<span data-ttu-id="af16f-132">엔드포인트가 HTTP 트래픽을 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="af16f-132">Indicates whether the endpoint enables HTTP traffic.</span></span>

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

### <span data-ttu-id="af16f-133">-IsHttpsAllowed</span><span class="sxs-lookup"><span data-stu-id="af16f-133">-IsHttpsAllowed</span></span>
<span data-ttu-id="af16f-134">엔드포인트가 HTTPS 트래픽을 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="af16f-134">Indicates whether the endpoint enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="af16f-135">-Location</span><span class="sxs-lookup"><span data-stu-id="af16f-135">-Location</span></span>
<span data-ttu-id="af16f-136">엔드포인트의 리소스 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="af16f-136">Specifies the resource location of the endpoint.</span></span>

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

### <span data-ttu-id="af16f-137">-OptimizationType</span><span class="sxs-lookup"><span data-stu-id="af16f-137">-OptimizationType</span></span>
<span data-ttu-id="af16f-138">이 엔드포인트가 가지는 최적화를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="af16f-138">Specifies any optimization this endpoint has.</span></span>

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

### <span data-ttu-id="af16f-139">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="af16f-139">-OriginGroupName</span></span>
<span data-ttu-id="af16f-140">원본 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="af16f-140">The name of the origin group.</span></span>

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

### <span data-ttu-id="af16f-141">-OriginGroupProbeIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="af16f-141">-OriginGroupProbeIntervalInSeconds</span></span>
<span data-ttu-id="af16f-142">상태 프로브 사이의 시간(초)입니다.</span><span class="sxs-lookup"><span data-stu-id="af16f-142">The number of seconds between health probes.</span></span>

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

### <span data-ttu-id="af16f-143">-OriginGroupProbePath</span><span class="sxs-lookup"><span data-stu-id="af16f-143">-OriginGroupProbePath</span></span>
<span data-ttu-id="af16f-144">원본의 상태 확인에 사용되는 원본에 대한 상대 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="af16f-144">The path relative to the origin that is used to determine the health of the origin.</span></span>

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

### <span data-ttu-id="af16f-145">-OriginGroupProbeProtocol</span><span class="sxs-lookup"><span data-stu-id="af16f-145">-OriginGroupProbeProtocol</span></span>
<span data-ttu-id="af16f-146">상태 프로브에 사용할 프로토콜입니다.</span><span class="sxs-lookup"><span data-stu-id="af16f-146">Protocol to use for health probe.</span></span>

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

### <span data-ttu-id="af16f-147">-OriginGroupProbeRequestType</span><span class="sxs-lookup"><span data-stu-id="af16f-147">-OriginGroupProbeRequestType</span></span>
<span data-ttu-id="af16f-148">만들어진 상태 프로브 요청의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="af16f-148">The type of health probe request that is made.</span></span>

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

### <span data-ttu-id="af16f-149">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="af16f-149">-OriginHostHeader</span></span>
<span data-ttu-id="af16f-150">엔드포인트의 원본 호스트 헤드를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="af16f-150">Specifies the origin host head of the endpoint.</span></span>

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

### <span data-ttu-id="af16f-151">-OriginHostName</span><span class="sxs-lookup"><span data-stu-id="af16f-151">-OriginHostName</span></span>
<span data-ttu-id="af16f-152">원본 서버의 호스트 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="af16f-152">Specifies the host name of the origin server.</span></span>

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

### <span data-ttu-id="af16f-153">-OriginId</span><span class="sxs-lookup"><span data-stu-id="af16f-153">-OriginId</span></span>
<span data-ttu-id="af16f-154">Azure CDN 원본 그룹 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="af16f-154">Azure CDN origin group ids.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af16f-155">-OriginName</span><span class="sxs-lookup"><span data-stu-id="af16f-155">-OriginName</span></span>
<span data-ttu-id="af16f-156">원본 서버의 리소스 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="af16f-156">Specifies the resource name of the origin server.</span></span>

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

### <span data-ttu-id="af16f-157">-OriginPath</span><span class="sxs-lookup"><span data-stu-id="af16f-157">-OriginPath</span></span>
<span data-ttu-id="af16f-158">원본 서버의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="af16f-158">Specifies the path of the origin server.</span></span>

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

### <span data-ttu-id="af16f-159">-Priority</span><span class="sxs-lookup"><span data-stu-id="af16f-159">-Priority</span></span>
<span data-ttu-id="af16f-160">Azure CDN 원본 우선 순위입니다.</span><span class="sxs-lookup"><span data-stu-id="af16f-160">Azure CDN origin priority.</span></span>

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

### <span data-ttu-id="af16f-161">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="af16f-161">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="af16f-162">개인 링크에 연결하기 위한 승인 요청에 포함될 사용자 지정 메시지입니다.</span><span class="sxs-lookup"><span data-stu-id="af16f-162">A custom message to be included in the approval request to connect to the Private Link.</span></span>

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

### <span data-ttu-id="af16f-163">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="af16f-163">-PrivateLinkLocation</span></span>
<span data-ttu-id="af16f-164">Azure CDN 원본 개인 링크 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="af16f-164">Azure CDN origin private link location.</span></span>

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

### <span data-ttu-id="af16f-165">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="af16f-165">-PrivateLinkResourceId</span></span>
<span data-ttu-id="af16f-166">Azure CDN 원본 개인 링크 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="af16f-166">Azure CDN origin private link resource id.</span></span>

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

### <span data-ttu-id="af16f-167">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="af16f-167">-ProbePath</span></span>
<span data-ttu-id="af16f-168">동적 사이트 가속에 대한 프로브 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="af16f-168">Specifies the probe path for Dynamic Site Acceleration</span></span>

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

### <span data-ttu-id="af16f-169">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="af16f-169">-ProfileName</span></span>
<span data-ttu-id="af16f-170">프로필의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="af16f-170">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="af16f-171">-QueryStringCachingBehavior</span><span class="sxs-lookup"><span data-stu-id="af16f-171">-QueryStringCachingBehavior</span></span>
<span data-ttu-id="af16f-172">쿼리 문자열이 요청 URL에 있을 때 CDN 엔드포인트의 동작을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="af16f-172">Specifies the behavior of CDN endpoint when a query string is in the request URL.</span></span>

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

### <span data-ttu-id="af16f-173">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af16f-173">-ResourceGroupName</span></span>
<span data-ttu-id="af16f-174">이 엔드포인트가 속한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="af16f-174">Specifies the name of the resource group to which this endpoint belongs.</span></span>

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

### <span data-ttu-id="af16f-175">-Tag</span><span class="sxs-lookup"><span data-stu-id="af16f-175">-Tag</span></span>
<span data-ttu-id="af16f-176">Azure CDN 엔드포인트와 연결되는 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="af16f-176">The tags to associate with the Azure CDN endpoint.</span></span>

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

### <span data-ttu-id="af16f-177">-Weight</span><span class="sxs-lookup"><span data-stu-id="af16f-177">-Weight</span></span>
<span data-ttu-id="af16f-178">Azure CDN 원본 가중치입니다.</span><span class="sxs-lookup"><span data-stu-id="af16f-178">Azure CDN origin weight.</span></span>

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

### <span data-ttu-id="af16f-179">-Confirm</span><span class="sxs-lookup"><span data-stu-id="af16f-179">-Confirm</span></span>
<span data-ttu-id="af16f-180">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="af16f-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af16f-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af16f-181">-WhatIf</span></span>
<span data-ttu-id="af16f-182">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="af16f-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af16f-183">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="af16f-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af16f-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af16f-184">CommonParameters</span></span>
<span data-ttu-id="af16f-185">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="af16f-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af16f-186">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="af16f-186">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af16f-187">입력</span><span class="sxs-lookup"><span data-stu-id="af16f-187">INPUTS</span></span>

### <span data-ttu-id="af16f-188">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="af16f-188">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="af16f-189">출력</span><span class="sxs-lookup"><span data-stu-id="af16f-189">OUTPUTS</span></span>

### <span data-ttu-id="af16f-190">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="af16f-190">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="af16f-191">참고 사항</span><span class="sxs-lookup"><span data-stu-id="af16f-191">NOTES</span></span>

## <span data-ttu-id="af16f-192">관련 링크</span><span class="sxs-lookup"><span data-stu-id="af16f-192">RELATED LINKS</span></span>

[<span data-ttu-id="af16f-193">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="af16f-193">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="af16f-194">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="af16f-194">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="af16f-195">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="af16f-195">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="af16f-196">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="af16f-196">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="af16f-197">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="af16f-197">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


