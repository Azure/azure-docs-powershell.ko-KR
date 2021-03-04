---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: A8C6F3BC-EE93-49A4-BF7B-8420967EEB7B
online version: https://docs.microsoft.com/powershell/module/az.cdn/new-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnEndpoint.md
ms.openlocfilehash: 9c902070ad71048c625115ba2803352a3b1132bd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956011"
---
# <span data-ttu-id="a9e77-101">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="a9e77-101">New-AzCdnEndpoint</span></span>

## <span data-ttu-id="a9e77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9e77-102">SYNOPSIS</span></span>
<span data-ttu-id="a9e77-103">CDN 엔드포인트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a9e77-103">Creates a CDN endpoint.</span></span>

## <span data-ttu-id="a9e77-104">구문</span><span class="sxs-lookup"><span data-stu-id="a9e77-104">SYNTAX</span></span>

### <span data-ttu-id="a9e77-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="a9e77-105">ByFieldsParameterSet (Default)</span></span>
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

### <span data-ttu-id="a9e77-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9e77-106">ByObjectParameterSet</span></span>
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

## <span data-ttu-id="a9e77-107">설명</span><span class="sxs-lookup"><span data-stu-id="a9e77-107">DESCRIPTION</span></span>
<span data-ttu-id="a9e77-108">**New-AzCdnEndpoint** cmdlet은 CDN(Azure Content Delivery Network) 엔드포인트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a9e77-108">The **New-AzCdnEndpoint** cmdlet creates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="a9e77-109">예제</span><span class="sxs-lookup"><span data-stu-id="a9e77-109">EXAMPLES</span></span>

## <span data-ttu-id="a9e77-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a9e77-110">PARAMETERS</span></span>

### <span data-ttu-id="a9e77-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="a9e77-111">-CdnProfile</span></span>
<span data-ttu-id="a9e77-112">엔드포인트가 추가될 CDN 프로필 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a9e77-112">Specifies the CDN profile object to which the endpoint is added.</span></span>

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

### <span data-ttu-id="a9e77-113">-ContentTypesToCompress</span><span class="sxs-lookup"><span data-stu-id="a9e77-113">-ContentTypesToCompress</span></span>
<span data-ttu-id="a9e77-114">에지 노드에서 클라이언트로 압축할 콘텐츠 형식 배열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a9e77-114">Specifies an array of content types to compress from the edge node to the client.</span></span>

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

### <span data-ttu-id="a9e77-115">-DefaultOriginGroup</span><span class="sxs-lookup"><span data-stu-id="a9e77-115">-DefaultOriginGroup</span></span>
<span data-ttu-id="a9e77-116">기본 원본 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="a9e77-116">The default origin group.</span></span>

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

### <span data-ttu-id="a9e77-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9e77-117">-DefaultProfile</span></span>
<span data-ttu-id="a9e77-118">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a9e77-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a9e77-119">-DeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="a9e77-119">-DeliveryPolicy</span></span>
<span data-ttu-id="a9e77-120">이 엔드포인트에 대한 배달 정책입니다.</span><span class="sxs-lookup"><span data-stu-id="a9e77-120">The delivery policy for this endpoint.</span></span>

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

### <span data-ttu-id="a9e77-121">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="a9e77-121">-EndpointName</span></span>
<span data-ttu-id="a9e77-122">엔드포인트의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a9e77-122">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="a9e77-123">-GeoFilters</span><span class="sxs-lookup"><span data-stu-id="a9e77-123">-GeoFilters</span></span>
<span data-ttu-id="a9e77-124">이 엔드포인트에 적용되는 지역 필터 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="a9e77-124">The list of geo filters that applies to this endpoint.</span></span>

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

### <span data-ttu-id="a9e77-125">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="a9e77-125">-HttpPort</span></span>
<span data-ttu-id="a9e77-126">원본 서버에서 HTTP 포트 번호를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a9e77-126">Specifies the HTTP port number on the origin server.</span></span>

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

### <span data-ttu-id="a9e77-127">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="a9e77-127">-HttpsPort</span></span>
<span data-ttu-id="a9e77-128">원본 서버에서 HTTPS 포트 번호를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a9e77-128">Specifies the HTTPS port number on the origin server.</span></span>

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

### <span data-ttu-id="a9e77-129">-IsCompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="a9e77-129">-IsCompressionEnabled</span></span>
<span data-ttu-id="a9e77-130">엔드포인트에 압축을 사용하도록 설정되어 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a9e77-130">Indicates whether compression is enabled for the endpoint.</span></span>

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

### <span data-ttu-id="a9e77-131">-IsHttpAllowed</span><span class="sxs-lookup"><span data-stu-id="a9e77-131">-IsHttpAllowed</span></span>
<span data-ttu-id="a9e77-132">엔드포인트가 HTTP 트래픽을 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a9e77-132">Indicates whether the endpoint enables HTTP traffic.</span></span>

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

### <span data-ttu-id="a9e77-133">-IsHttpsAllowed</span><span class="sxs-lookup"><span data-stu-id="a9e77-133">-IsHttpsAllowed</span></span>
<span data-ttu-id="a9e77-134">엔드포인트가 HTTPS 트래픽을 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a9e77-134">Indicates whether the endpoint enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="a9e77-135">-Location</span><span class="sxs-lookup"><span data-stu-id="a9e77-135">-Location</span></span>
<span data-ttu-id="a9e77-136">엔드포인트의 리소스 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a9e77-136">Specifies the resource location of the endpoint.</span></span>

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

### <span data-ttu-id="a9e77-137">-OptimizationType</span><span class="sxs-lookup"><span data-stu-id="a9e77-137">-OptimizationType</span></span>
<span data-ttu-id="a9e77-138">이 엔드포인트가 가지는 최적화를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a9e77-138">Specifies any optimization this endpoint has.</span></span>

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

### <span data-ttu-id="a9e77-139">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="a9e77-139">-OriginGroupName</span></span>
<span data-ttu-id="a9e77-140">원본 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a9e77-140">The name of the origin group.</span></span>

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

### <span data-ttu-id="a9e77-141">-OriginGroupProbeIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="a9e77-141">-OriginGroupProbeIntervalInSeconds</span></span>
<span data-ttu-id="a9e77-142">상태 프로브 사이의 초 수입니다.</span><span class="sxs-lookup"><span data-stu-id="a9e77-142">The number of seconds between health probes.</span></span>

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

### <span data-ttu-id="a9e77-143">-OriginGroupProbePath</span><span class="sxs-lookup"><span data-stu-id="a9e77-143">-OriginGroupProbePath</span></span>
<span data-ttu-id="a9e77-144">원본의 상태 확인에 사용되는 원본을 상대로 하는 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="a9e77-144">The path relative to the origin that is used to determine the health of the origin.</span></span>

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

### <span data-ttu-id="a9e77-145">-OriginGroupProbeProtocol</span><span class="sxs-lookup"><span data-stu-id="a9e77-145">-OriginGroupProbeProtocol</span></span>
<span data-ttu-id="a9e77-146">상태 프로브에 사용할 프로토콜입니다.</span><span class="sxs-lookup"><span data-stu-id="a9e77-146">Protocol to use for health probe.</span></span>

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

### <span data-ttu-id="a9e77-147">-OriginGroupProbeRequestType</span><span class="sxs-lookup"><span data-stu-id="a9e77-147">-OriginGroupProbeRequestType</span></span>
<span data-ttu-id="a9e77-148">만든 상태 프로브 요청의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="a9e77-148">The type of health probe request that is made.</span></span>

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

### <span data-ttu-id="a9e77-149">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="a9e77-149">-OriginHostHeader</span></span>
<span data-ttu-id="a9e77-150">엔드포인트의 원본 호스트 헤드를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a9e77-150">Specifies the origin host head of the endpoint.</span></span>

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

### <span data-ttu-id="a9e77-151">-OriginHostName</span><span class="sxs-lookup"><span data-stu-id="a9e77-151">-OriginHostName</span></span>
<span data-ttu-id="a9e77-152">원본 서버의 호스트 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a9e77-152">Specifies the host name of the origin server.</span></span>

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

### <span data-ttu-id="a9e77-153">-OriginId</span><span class="sxs-lookup"><span data-stu-id="a9e77-153">-OriginId</span></span>
<span data-ttu-id="a9e77-154">Azure CDN 원본 그룹 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a9e77-154">Azure CDN origin group ids.</span></span>

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

### <span data-ttu-id="a9e77-155">-OriginName</span><span class="sxs-lookup"><span data-stu-id="a9e77-155">-OriginName</span></span>
<span data-ttu-id="a9e77-156">원본 서버의 리소스 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a9e77-156">Specifies the resource name of the origin server.</span></span>

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

### <span data-ttu-id="a9e77-157">-OriginPath</span><span class="sxs-lookup"><span data-stu-id="a9e77-157">-OriginPath</span></span>
<span data-ttu-id="a9e77-158">원본 서버의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a9e77-158">Specifies the path of the origin server.</span></span>

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

### <span data-ttu-id="a9e77-159">-Priority</span><span class="sxs-lookup"><span data-stu-id="a9e77-159">-Priority</span></span>
<span data-ttu-id="a9e77-160">Azure CDN 원본 우선 순위입니다.</span><span class="sxs-lookup"><span data-stu-id="a9e77-160">Azure CDN origin priority.</span></span>

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

### <span data-ttu-id="a9e77-161">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="a9e77-161">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="a9e77-162">개인 링크에 연결하는 승인 요청에 포함될 사용자 지정 메시지입니다.</span><span class="sxs-lookup"><span data-stu-id="a9e77-162">A custom message to be included in the approval request to connect to the Private Link.</span></span>

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

### <span data-ttu-id="a9e77-163">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="a9e77-163">-PrivateLinkLocation</span></span>
<span data-ttu-id="a9e77-164">Azure CDN 원본 개인 링크 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="a9e77-164">Azure CDN origin private link location.</span></span>

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

### <span data-ttu-id="a9e77-165">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="a9e77-165">-PrivateLinkResourceId</span></span>
<span data-ttu-id="a9e77-166">Azure CDN 원본 개인 링크 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a9e77-166">Azure CDN origin private link resource id.</span></span>

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

### <span data-ttu-id="a9e77-167">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="a9e77-167">-ProbePath</span></span>
<span data-ttu-id="a9e77-168">동적 사이트 가속에 대한 프로브 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a9e77-168">Specifies the probe path for Dynamic Site Acceleration</span></span>

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

### <span data-ttu-id="a9e77-169">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="a9e77-169">-ProfileName</span></span>
<span data-ttu-id="a9e77-170">프로필의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a9e77-170">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="a9e77-171">-QueryStringCachingBehavior</span><span class="sxs-lookup"><span data-stu-id="a9e77-171">-QueryStringCachingBehavior</span></span>
<span data-ttu-id="a9e77-172">쿼리 문자열이 요청 URL에 있을 때 CDN 엔드포인트의 동작을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a9e77-172">Specifies the behavior of CDN endpoint when a query string is in the request URL.</span></span>

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

### <span data-ttu-id="a9e77-173">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9e77-173">-ResourceGroupName</span></span>
<span data-ttu-id="a9e77-174">이 엔드포인트가 속한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a9e77-174">Specifies the name of the resource group to which this endpoint belongs.</span></span>

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

### <span data-ttu-id="a9e77-175">-Tag</span><span class="sxs-lookup"><span data-stu-id="a9e77-175">-Tag</span></span>
<span data-ttu-id="a9e77-176">Azure CDN 엔드포인트와 연결되는 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="a9e77-176">The tags to associate with the Azure CDN endpoint.</span></span>

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

### <span data-ttu-id="a9e77-177">-Weight</span><span class="sxs-lookup"><span data-stu-id="a9e77-177">-Weight</span></span>
<span data-ttu-id="a9e77-178">Azure CDN 원본 가중치입니다.</span><span class="sxs-lookup"><span data-stu-id="a9e77-178">Azure CDN origin weight.</span></span>

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

### <span data-ttu-id="a9e77-179">-확인</span><span class="sxs-lookup"><span data-stu-id="a9e77-179">-Confirm</span></span>
<span data-ttu-id="a9e77-180">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9e77-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9e77-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9e77-181">-WhatIf</span></span>
<span data-ttu-id="a9e77-182">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="a9e77-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9e77-183">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a9e77-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9e77-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9e77-184">CommonParameters</span></span>
<span data-ttu-id="a9e77-185">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a9e77-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9e77-186">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a9e77-186">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9e77-187">입력</span><span class="sxs-lookup"><span data-stu-id="a9e77-187">INPUTS</span></span>

### <span data-ttu-id="a9e77-188">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="a9e77-188">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="a9e77-189">출력</span><span class="sxs-lookup"><span data-stu-id="a9e77-189">OUTPUTS</span></span>

### <span data-ttu-id="a9e77-190">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="a9e77-190">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="a9e77-191">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a9e77-191">NOTES</span></span>

## <span data-ttu-id="a9e77-192">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a9e77-192">RELATED LINKS</span></span>

[<span data-ttu-id="a9e77-193">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="a9e77-193">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="a9e77-194">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="a9e77-194">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="a9e77-195">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="a9e77-195">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="a9e77-196">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="a9e77-196">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="a9e77-197">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="a9e77-197">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


