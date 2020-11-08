---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: A8C6F3BC-EE93-49A4-BF7B-8420967EEB7B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnEndpoint.md
ms.openlocfilehash: 9e0b8ee74ff89f4a5903df1c73dc7b289b0371c4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216266"
---
# <span data-ttu-id="b0041-101">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b0041-101">New-AzCdnEndpoint</span></span>

## <span data-ttu-id="b0041-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0041-102">SYNOPSIS</span></span>
<span data-ttu-id="b0041-103">CDN 끝점을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b0041-103">Creates a CDN endpoint.</span></span>

## <span data-ttu-id="b0041-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b0041-104">SYNTAX</span></span>

### <span data-ttu-id="b0041-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="b0041-105">ByFieldsParameterSet (Default)</span></span>
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

### <span data-ttu-id="b0041-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0041-106">ByObjectParameterSet</span></span>
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

## <span data-ttu-id="b0041-107">설명은</span><span class="sxs-lookup"><span data-stu-id="b0041-107">DESCRIPTION</span></span>
<span data-ttu-id="b0041-108">**AzCdnEndpoint** CMDLET은 CDN (Azure Content Delivery Network) 끝점을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b0041-108">The **New-AzCdnEndpoint** cmdlet creates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="b0041-109">예제의</span><span class="sxs-lookup"><span data-stu-id="b0041-109">EXAMPLES</span></span>

## <span data-ttu-id="b0041-110">변수</span><span class="sxs-lookup"><span data-stu-id="b0041-110">PARAMETERS</span></span>

### <span data-ttu-id="b0041-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="b0041-111">-CdnProfile</span></span>
<span data-ttu-id="b0041-112">끝점을 추가할 CDN 프로필 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0041-112">Specifies the CDN profile object to which the endpoint is added.</span></span>

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

### <span data-ttu-id="b0041-113">-ContentTypesToCompress</span><span class="sxs-lookup"><span data-stu-id="b0041-113">-ContentTypesToCompress</span></span>
<span data-ttu-id="b0041-114">Edge 노드에서 클라이언트로 압축할 콘텐츠 형식의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0041-114">Specifies an array of content types to compress from the edge node to the client.</span></span>

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

### <span data-ttu-id="b0041-115">-DefaultOriginGroup</span><span class="sxs-lookup"><span data-stu-id="b0041-115">-DefaultOriginGroup</span></span>
<span data-ttu-id="b0041-116">기본 시작 그룹</span><span class="sxs-lookup"><span data-stu-id="b0041-116">The default origin group.</span></span>

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

### <span data-ttu-id="b0041-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0041-117">-DefaultProfile</span></span>
<span data-ttu-id="b0041-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="b0041-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b0041-119">-배달 Ypolicy</span><span class="sxs-lookup"><span data-stu-id="b0041-119">-DeliveryPolicy</span></span>
<span data-ttu-id="b0041-120">이 끝점에 대 한 배달 정책입니다.</span><span class="sxs-lookup"><span data-stu-id="b0041-120">The delivery policy for this endpoint.</span></span>

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

### <span data-ttu-id="b0041-121">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="b0041-121">-EndpointName</span></span>
<span data-ttu-id="b0041-122">끝점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0041-122">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="b0041-123">-GeoFilters</span><span class="sxs-lookup"><span data-stu-id="b0041-123">-GeoFilters</span></span>
<span data-ttu-id="b0041-124">이 끝점에 적용 되는 지리적 필터 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="b0041-124">The list of geo filters that applies to this endpoint.</span></span>

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

### <span data-ttu-id="b0041-125">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="b0041-125">-HttpPort</span></span>
<span data-ttu-id="b0041-126">원본 서버의 HTTP 포트 번호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0041-126">Specifies the HTTP port number on the origin server.</span></span>

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

### <span data-ttu-id="b0041-127">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="b0041-127">-HttpsPort</span></span>
<span data-ttu-id="b0041-128">원본 서버의 HTTPS 포트 번호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0041-128">Specifies the HTTPS port number on the origin server.</span></span>

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

### <span data-ttu-id="b0041-129">-IsCompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="b0041-129">-IsCompressionEnabled</span></span>
<span data-ttu-id="b0041-130">끝점에 압축을 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b0041-130">Indicates whether compression is enabled for the endpoint.</span></span>

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

### <span data-ttu-id="b0041-131">-IsHttpAllowed</span><span class="sxs-lookup"><span data-stu-id="b0041-131">-IsHttpAllowed</span></span>
<span data-ttu-id="b0041-132">끝점에서 HTTP 트래픽을 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b0041-132">Indicates whether the endpoint enables HTTP traffic.</span></span>

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

### <span data-ttu-id="b0041-133">-IsHttpsAllowed</span><span class="sxs-lookup"><span data-stu-id="b0041-133">-IsHttpsAllowed</span></span>
<span data-ttu-id="b0041-134">끝점에서 HTTPS 트래픽을 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b0041-134">Indicates whether the endpoint enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="b0041-135">-위치</span><span class="sxs-lookup"><span data-stu-id="b0041-135">-Location</span></span>
<span data-ttu-id="b0041-136">끝점의 리소스 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0041-136">Specifies the resource location of the endpoint.</span></span>

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

### <span data-ttu-id="b0041-137">-OptimizationType</span><span class="sxs-lookup"><span data-stu-id="b0041-137">-OptimizationType</span></span>
<span data-ttu-id="b0041-138">이 끝점의 최적화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0041-138">Specifies any optimization this endpoint has.</span></span>

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

### <span data-ttu-id="b0041-139">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="b0041-139">-OriginGroupName</span></span>
<span data-ttu-id="b0041-140">원본 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b0041-140">The name of the origin group.</span></span>

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

### <span data-ttu-id="b0041-141">-OriginGroupProbeIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="b0041-141">-OriginGroupProbeIntervalInSeconds</span></span>
<span data-ttu-id="b0041-142">상태 프로브 사이의 초 수입니다.</span><span class="sxs-lookup"><span data-stu-id="b0041-142">The number of seconds between health probes.</span></span>

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

### <span data-ttu-id="b0041-143">-OriginGroupProbePath</span><span class="sxs-lookup"><span data-stu-id="b0041-143">-OriginGroupProbePath</span></span>
<span data-ttu-id="b0041-144">원점의 상태를 확인 하는 데 사용 되는 원점을 기준으로 하는 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="b0041-144">The path relative to the origin that is used to determine the health of the origin.</span></span>

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

### <span data-ttu-id="b0041-145">-OriginGroupProbeProtocol</span><span class="sxs-lookup"><span data-stu-id="b0041-145">-OriginGroupProbeProtocol</span></span>
<span data-ttu-id="b0041-146">상태 프로브에 사용 하는 프로토콜입니다.</span><span class="sxs-lookup"><span data-stu-id="b0041-146">Protocol to use for health probe.</span></span>

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

### <span data-ttu-id="b0041-147">-OriginGroupProbeRequestType</span><span class="sxs-lookup"><span data-stu-id="b0041-147">-OriginGroupProbeRequestType</span></span>
<span data-ttu-id="b0041-148">적용 되는 상태 프로브 요청의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="b0041-148">The type of health probe request that is made.</span></span>

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

### <span data-ttu-id="b0041-149">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="b0041-149">-OriginHostHeader</span></span>
<span data-ttu-id="b0041-150">끝점의 원본 호스트 헤드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0041-150">Specifies the origin host head of the endpoint.</span></span>

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

### <span data-ttu-id="b0041-151">-OriginHostName</span><span class="sxs-lookup"><span data-stu-id="b0041-151">-OriginHostName</span></span>
<span data-ttu-id="b0041-152">원본 서버의 호스트 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0041-152">Specifies the host name of the origin server.</span></span>

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

### <span data-ttu-id="b0041-153">-OriginId</span><span class="sxs-lookup"><span data-stu-id="b0041-153">-OriginId</span></span>
<span data-ttu-id="b0041-154">Azure CDN 원본 그룹 id입니다.</span><span class="sxs-lookup"><span data-stu-id="b0041-154">Azure CDN origin group ids.</span></span>

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

### <span data-ttu-id="b0041-155">-OriginName</span><span class="sxs-lookup"><span data-stu-id="b0041-155">-OriginName</span></span>
<span data-ttu-id="b0041-156">원본 서버의 리소스 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0041-156">Specifies the resource name of the origin server.</span></span>

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

### <span data-ttu-id="b0041-157">-OriginPath</span><span class="sxs-lookup"><span data-stu-id="b0041-157">-OriginPath</span></span>
<span data-ttu-id="b0041-158">원본 서버의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0041-158">Specifies the path of the origin server.</span></span>

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

### <span data-ttu-id="b0041-159">-우선 순위</span><span class="sxs-lookup"><span data-stu-id="b0041-159">-Priority</span></span>
<span data-ttu-id="b0041-160">Azure CDN 원본 우선 순위입니다.</span><span class="sxs-lookup"><span data-stu-id="b0041-160">Azure CDN origin priority.</span></span>

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

### <span data-ttu-id="b0041-161">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="b0041-161">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="b0041-162">개인 링크에 연결 하기 위해 승인 요청에 포함할 사용자 지정 메시지입니다.</span><span class="sxs-lookup"><span data-stu-id="b0041-162">A custom message to be included in the approval request to connect to the Private Link.</span></span>

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

### <span data-ttu-id="b0041-163">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="b0041-163">-PrivateLinkLocation</span></span>
<span data-ttu-id="b0041-164">Azure CDN 원본 개인 링크 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="b0041-164">Azure CDN origin private link location.</span></span>

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

### <span data-ttu-id="b0041-165">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="b0041-165">-PrivateLinkResourceId</span></span>
<span data-ttu-id="b0041-166">Azure CDN 원본 개인 링크 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="b0041-166">Azure CDN origin private link resource id.</span></span>

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

### <span data-ttu-id="b0041-167">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="b0041-167">-ProbePath</span></span>
<span data-ttu-id="b0041-168">동적 사이트 가속에 대 한 프로브 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0041-168">Specifies the probe path for Dynamic Site Acceleration</span></span>

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

### <span data-ttu-id="b0041-169">-/Profile</span><span class="sxs-lookup"><span data-stu-id="b0041-169">-ProfileName</span></span>
<span data-ttu-id="b0041-170">프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0041-170">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="b0041-171">-QueryStringCachingBehavior</span><span class="sxs-lookup"><span data-stu-id="b0041-171">-QueryStringCachingBehavior</span></span>
<span data-ttu-id="b0041-172">쿼리 문자열이 요청 URL에 있을 때 CDN 끝점의 동작을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0041-172">Specifies the behavior of CDN endpoint when a query string is in the request URL.</span></span>

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

### <span data-ttu-id="b0041-173">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0041-173">-ResourceGroupName</span></span>
<span data-ttu-id="b0041-174">이 끝점이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0041-174">Specifies the name of the resource group to which this endpoint belongs.</span></span>

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

### <span data-ttu-id="b0041-175">태그</span><span class="sxs-lookup"><span data-stu-id="b0041-175">-Tag</span></span>
<span data-ttu-id="b0041-176">Azure CDN 끝점과 연결할 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="b0041-176">The tags to associate with the Azure CDN endpoint.</span></span>

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

### <span data-ttu-id="b0041-177">-중량</span><span class="sxs-lookup"><span data-stu-id="b0041-177">-Weight</span></span>
<span data-ttu-id="b0041-178">Azure CDN 원본 가중치.</span><span class="sxs-lookup"><span data-stu-id="b0041-178">Azure CDN origin weight.</span></span>

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

### <span data-ttu-id="b0041-179">-확인</span><span class="sxs-lookup"><span data-stu-id="b0041-179">-Confirm</span></span>
<span data-ttu-id="b0041-180">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0041-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0041-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0041-181">-WhatIf</span></span>
<span data-ttu-id="b0041-182">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b0041-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0041-183">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b0041-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0041-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0041-184">CommonParameters</span></span>
<span data-ttu-id="b0041-185">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0041-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0041-186">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b0041-186">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0041-187">입력</span><span class="sxs-lookup"><span data-stu-id="b0041-187">INPUTS</span></span>

### <span data-ttu-id="b0041-188">Microsoft. Cdn. 프로필. PSProfile</span><span class="sxs-lookup"><span data-stu-id="b0041-188">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="b0041-189">출력</span><span class="sxs-lookup"><span data-stu-id="b0041-189">OUTPUTS</span></span>

### <span data-ttu-id="b0041-190">Microsoft. Cdn. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="b0041-190">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="b0041-191">상속자</span><span class="sxs-lookup"><span data-stu-id="b0041-191">NOTES</span></span>

## <span data-ttu-id="b0041-192">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b0041-192">RELATED LINKS</span></span>

[<span data-ttu-id="b0041-193">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b0041-193">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="b0041-194">제거-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b0041-194">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="b0041-195">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b0041-195">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="b0041-196">시작-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b0041-196">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="b0041-197">중지-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b0041-197">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


