---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: A8C6F3BC-EE93-49A4-BF7B-8420967EEB7B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnEndpoint.md
ms.openlocfilehash: 5d2bfdf2bf5f87ccb0213c006de8612b5eaf0730
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533147"
---
# <span data-ttu-id="f5cf3-101">New-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="f5cf3-101">New-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="f5cf3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5cf3-102">SYNOPSIS</span></span>
<span data-ttu-id="f5cf3-103">CDN 끝점을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f5cf3-103">Creates a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5cf3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f5cf3-104">SYNTAX</span></span>

### <span data-ttu-id="f5cf3-105">필드 매개 변수에 대해 설정 되는 매개 변수 (기본값)</span><span class="sxs-lookup"><span data-stu-id="f5cf3-105">Parameter Set for fields parameters (Default)</span></span>
```
New-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -Location <String> [-OriginHostHeader <String>] [-OriginPath <String>] [-ContentTypesToCompress <String[]>]
 [-IsCompressionEnabled <Boolean>] [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-GeoFilters <PSGeoFilter[]>]
 [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5cf3-106">개체 매개 변수에 대해 설정 되는 매개 변수</span><span class="sxs-lookup"><span data-stu-id="f5cf3-106">Parameter Set for object parameters</span></span>
```
New-AzureRmCdnEndpoint -EndpointName <String> -CdnProfile <PSProfile> [-OriginHostHeader <String>]
 [-OriginPath <String>] [-ContentTypesToCompress <String[]>] [-IsCompressionEnabled <Boolean>]
 [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-GeoFilters <PSGeoFilter[]>]
 [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5cf3-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f5cf3-107">DESCRIPTION</span></span>
<span data-ttu-id="f5cf3-108">**AzureRmCdnEndpoint** CMDLET은 CDN (Azure Content Delivery Network) 끝점을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f5cf3-108">The **New-AzureRmCdnEndpoint** cmdlet creates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="f5cf3-109">예제의</span><span class="sxs-lookup"><span data-stu-id="f5cf3-109">EXAMPLES</span></span>

## <span data-ttu-id="f5cf3-110">변수</span><span class="sxs-lookup"><span data-stu-id="f5cf3-110">PARAMETERS</span></span>

### <span data-ttu-id="f5cf3-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="f5cf3-111">-CdnProfile</span></span>
<span data-ttu-id="f5cf3-112">끝점을 추가할 CDN 프로필 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5cf3-112">Specifies the CDN profile object to which the endpoint is added.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f5cf3-113">-ContentTypesToCompress</span><span class="sxs-lookup"><span data-stu-id="f5cf3-113">-ContentTypesToCompress</span></span>
<span data-ttu-id="f5cf3-114">Edge 노드에서 클라이언트로 압축할 콘텐츠 형식의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5cf3-114">Specifies an array of content types to compress from the edge node to the client.</span></span>

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

### <span data-ttu-id="f5cf3-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="f5cf3-115">-EndpointName</span></span>
<span data-ttu-id="f5cf3-116">끝점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5cf3-116">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="f5cf3-117">-GeoFilters</span><span class="sxs-lookup"><span data-stu-id="f5cf3-117">-GeoFilters</span></span>
<span data-ttu-id="f5cf3-118">이 끝점에 적용 되는 지리적 필터 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="f5cf3-118">The list of geo filters that applies to this endpoint.</span></span>

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

### <span data-ttu-id="f5cf3-119">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="f5cf3-119">-HttpPort</span></span>
<span data-ttu-id="f5cf3-120">원본 서버의 HTTP 포트 번호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5cf3-120">Specifies the HTTP port number on the origin server.</span></span>

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

### <span data-ttu-id="f5cf3-121">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="f5cf3-121">-HttpsPort</span></span>
<span data-ttu-id="f5cf3-122">원본 서버의 HTTPS 포트 번호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5cf3-122">Specifies the HTTPS port number on the origin server.</span></span>

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

### <span data-ttu-id="f5cf3-123">-IsCompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="f5cf3-123">-IsCompressionEnabled</span></span>
<span data-ttu-id="f5cf3-124">끝점에 압축을 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f5cf3-124">Indicates whether compression is enabled for the endpoint.</span></span>

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

### <span data-ttu-id="f5cf3-125">-IsHttpAllowed</span><span class="sxs-lookup"><span data-stu-id="f5cf3-125">-IsHttpAllowed</span></span>
<span data-ttu-id="f5cf3-126">끝점에서 HTTP 트래픽을 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f5cf3-126">Indicates whether the endpoint enables HTTP traffic.</span></span>

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

### <span data-ttu-id="f5cf3-127">-IsHttpsAllowed</span><span class="sxs-lookup"><span data-stu-id="f5cf3-127">-IsHttpsAllowed</span></span>
<span data-ttu-id="f5cf3-128">끝점에서 HTTPS 트래픽을 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f5cf3-128">Indicates whether the endpoint enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="f5cf3-129">-위치</span><span class="sxs-lookup"><span data-stu-id="f5cf3-129">-Location</span></span>
<span data-ttu-id="f5cf3-130">끝점의 리소스 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5cf3-130">Specifies the resource location of the endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5cf3-131">-OptimizationType</span><span class="sxs-lookup"><span data-stu-id="f5cf3-131">-OptimizationType</span></span>
<span data-ttu-id="f5cf3-132">이 끝점의 최적화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5cf3-132">Specifies any optimization this endpoint has.</span></span>

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

### <span data-ttu-id="f5cf3-133">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="f5cf3-133">-OriginHostHeader</span></span>
<span data-ttu-id="f5cf3-134">끝점의 원본 호스트 헤드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5cf3-134">Specifies the origin host head of the endpoint.</span></span>

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

### <span data-ttu-id="f5cf3-135">-OriginHostName</span><span class="sxs-lookup"><span data-stu-id="f5cf3-135">-OriginHostName</span></span>
<span data-ttu-id="f5cf3-136">원본 서버의 호스트 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5cf3-136">Specifies the host name of the origin server.</span></span>

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

### <span data-ttu-id="f5cf3-137">-OriginName</span><span class="sxs-lookup"><span data-stu-id="f5cf3-137">-OriginName</span></span>
<span data-ttu-id="f5cf3-138">원본 서버의 리소스 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5cf3-138">Specifies the resource name of the origin server.</span></span>

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

### <span data-ttu-id="f5cf3-139">-OriginPath</span><span class="sxs-lookup"><span data-stu-id="f5cf3-139">-OriginPath</span></span>
<span data-ttu-id="f5cf3-140">원본 서버의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5cf3-140">Specifies the path of the origin server.</span></span>

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

### <span data-ttu-id="f5cf3-141">-/Profile</span><span class="sxs-lookup"><span data-stu-id="f5cf3-141">-ProfileName</span></span>
<span data-ttu-id="f5cf3-142">프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5cf3-142">Specifies the name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5cf3-143">-QueryStringCachingBehavior</span><span class="sxs-lookup"><span data-stu-id="f5cf3-143">-QueryStringCachingBehavior</span></span>
<span data-ttu-id="f5cf3-144">쿼리 문자열이 요청 URL에 있을 때 CDN 끝점의 동작을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5cf3-144">Specifies the behavior of CDN endpoint when a query string is in the request URL.</span></span>

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

### <span data-ttu-id="f5cf3-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5cf3-145">-ResourceGroupName</span></span>
<span data-ttu-id="f5cf3-146">이 끝점이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5cf3-146">Specifies the name of the resource group to which this endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5cf3-147">태그</span><span class="sxs-lookup"><span data-stu-id="f5cf3-147">-Tags</span></span>
<span data-ttu-id="f5cf3-148">이 리소스와 연결 된 태그의 해시 테이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5cf3-148">Specifies a hash table of the tags that associated with this resource.</span></span>

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

### <span data-ttu-id="f5cf3-149">-확인</span><span class="sxs-lookup"><span data-stu-id="f5cf3-149">-Confirm</span></span>
<span data-ttu-id="f5cf3-150">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5cf3-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5cf3-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5cf3-151">-WhatIf</span></span>
<span data-ttu-id="f5cf3-152">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f5cf3-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5cf3-153">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f5cf3-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5cf3-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5cf3-154">-DefaultProfile</span></span>
<span data-ttu-id="f5cf3-155">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f5cf3-155">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5cf3-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5cf3-156">CommonParameters</span></span>
<span data-ttu-id="f5cf3-157">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5cf3-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5cf3-158">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5cf3-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5cf3-159">입력</span><span class="sxs-lookup"><span data-stu-id="f5cf3-159">INPUTS</span></span>

### <span data-ttu-id="f5cf3-160">PSProfile</span><span class="sxs-lookup"><span data-stu-id="f5cf3-160">PSProfile</span></span>
<span data-ttu-id="f5cf3-161">' CdnProfile ' 매개 변수는 파이프라인에서 ' PSProfile ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5cf3-161">Parameter 'CdnProfile' accepts value of type 'PSProfile' from the pipeline</span></span>

## <span data-ttu-id="f5cf3-162">출력</span><span class="sxs-lookup"><span data-stu-id="f5cf3-162">OUTPUTS</span></span>

### <span data-ttu-id="f5cf3-163">Microsoft. Cdn. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="f5cf3-163">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="f5cf3-164">상속자</span><span class="sxs-lookup"><span data-stu-id="f5cf3-164">NOTES</span></span>

## <span data-ttu-id="f5cf3-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f5cf3-165">RELATED LINKS</span></span>

[<span data-ttu-id="f5cf3-166">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="f5cf3-166">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="f5cf3-167">제거-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="f5cf3-167">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="f5cf3-168">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="f5cf3-168">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="f5cf3-169">시작-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="f5cf3-169">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="f5cf3-170">중지-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="f5cf3-170">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


