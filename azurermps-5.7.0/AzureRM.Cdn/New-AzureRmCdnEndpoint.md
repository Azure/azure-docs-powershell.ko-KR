---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: A8C6F3BC-EE93-49A4-BF7B-8420967EEB7B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/new-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnEndpoint.md
ms.openlocfilehash: 682c12270608f9c75e86cea742fd411e0eb657a7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527016"
---
# <span data-ttu-id="51e7b-101">New-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="51e7b-101">New-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="51e7b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51e7b-102">SYNOPSIS</span></span>
<span data-ttu-id="51e7b-103">CDN 끝점을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="51e7b-103">Creates a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51e7b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="51e7b-104">SYNTAX</span></span>

### <span data-ttu-id="51e7b-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="51e7b-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -Location <String> [-OriginHostHeader <String>] [-OriginPath <String>] [-ContentTypesToCompress <String[]>]
 [-IsCompressionEnabled <Boolean>] [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-GeoFilters <PSGeoFilter[]>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51e7b-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="51e7b-106">ByObjectParameterSet</span></span>
```
New-AzureRmCdnEndpoint -EndpointName <String> -CdnProfile <PSProfile> [-OriginHostHeader <String>]
 [-OriginPath <String>] [-ContentTypesToCompress <String[]>] [-IsCompressionEnabled <Boolean>]
 [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-GeoFilters <PSGeoFilter[]>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51e7b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="51e7b-107">DESCRIPTION</span></span>
<span data-ttu-id="51e7b-108">**AzureRmCdnEndpoint** CMDLET은 CDN (Azure Content Delivery Network) 끝점을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="51e7b-108">The **New-AzureRmCdnEndpoint** cmdlet creates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="51e7b-109">예제의</span><span class="sxs-lookup"><span data-stu-id="51e7b-109">EXAMPLES</span></span>

## <span data-ttu-id="51e7b-110">변수</span><span class="sxs-lookup"><span data-stu-id="51e7b-110">PARAMETERS</span></span>

### <span data-ttu-id="51e7b-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="51e7b-111">-CdnProfile</span></span>
<span data-ttu-id="51e7b-112">끝점을 추가할 CDN 프로필 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51e7b-112">Specifies the CDN profile object to which the endpoint is added.</span></span>

```yaml
Type: PSProfile
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51e7b-113">-ContentTypesToCompress</span><span class="sxs-lookup"><span data-stu-id="51e7b-113">-ContentTypesToCompress</span></span>
<span data-ttu-id="51e7b-114">Edge 노드에서 클라이언트로 압축할 콘텐츠 형식의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51e7b-114">Specifies an array of content types to compress from the edge node to the client.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51e7b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51e7b-115">-DefaultProfile</span></span>
<span data-ttu-id="51e7b-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="51e7b-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51e7b-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="51e7b-117">-EndpointName</span></span>
<span data-ttu-id="51e7b-118">끝점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51e7b-118">Specifies the name of the endpoint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51e7b-119">-GeoFilters</span><span class="sxs-lookup"><span data-stu-id="51e7b-119">-GeoFilters</span></span>
<span data-ttu-id="51e7b-120">이 끝점에 적용 되는 지리적 필터 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="51e7b-120">The list of geo filters that applies to this endpoint.</span></span>

```yaml
Type: PSGeoFilter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51e7b-121">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="51e7b-121">-HttpPort</span></span>
<span data-ttu-id="51e7b-122">원본 서버의 HTTP 포트 번호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51e7b-122">Specifies the HTTP port number on the origin server.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51e7b-123">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="51e7b-123">-HttpsPort</span></span>
<span data-ttu-id="51e7b-124">원본 서버의 HTTPS 포트 번호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51e7b-124">Specifies the HTTPS port number on the origin server.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51e7b-125">-IsCompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="51e7b-125">-IsCompressionEnabled</span></span>
<span data-ttu-id="51e7b-126">끝점에 압축을 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="51e7b-126">Indicates whether compression is enabled for the endpoint.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51e7b-127">-IsHttpAllowed</span><span class="sxs-lookup"><span data-stu-id="51e7b-127">-IsHttpAllowed</span></span>
<span data-ttu-id="51e7b-128">끝점에서 HTTP 트래픽을 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="51e7b-128">Indicates whether the endpoint enables HTTP traffic.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51e7b-129">-IsHttpsAllowed</span><span class="sxs-lookup"><span data-stu-id="51e7b-129">-IsHttpsAllowed</span></span>
<span data-ttu-id="51e7b-130">끝점에서 HTTPS 트래픽을 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="51e7b-130">Indicates whether the endpoint enables HTTPS traffic.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51e7b-131">-위치</span><span class="sxs-lookup"><span data-stu-id="51e7b-131">-Location</span></span>
<span data-ttu-id="51e7b-132">끝점의 리소스 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51e7b-132">Specifies the resource location of the endpoint.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51e7b-133">-OptimizationType</span><span class="sxs-lookup"><span data-stu-id="51e7b-133">-OptimizationType</span></span>
<span data-ttu-id="51e7b-134">이 끝점의 최적화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51e7b-134">Specifies any optimization this endpoint has.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51e7b-135">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="51e7b-135">-OriginHostHeader</span></span>
<span data-ttu-id="51e7b-136">끝점의 원본 호스트 헤드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51e7b-136">Specifies the origin host head of the endpoint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51e7b-137">-OriginHostName</span><span class="sxs-lookup"><span data-stu-id="51e7b-137">-OriginHostName</span></span>
<span data-ttu-id="51e7b-138">원본 서버의 호스트 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51e7b-138">Specifies the host name of the origin server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51e7b-139">-OriginName</span><span class="sxs-lookup"><span data-stu-id="51e7b-139">-OriginName</span></span>
<span data-ttu-id="51e7b-140">원본 서버의 리소스 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51e7b-140">Specifies the resource name of the origin server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51e7b-141">-OriginPath</span><span class="sxs-lookup"><span data-stu-id="51e7b-141">-OriginPath</span></span>
<span data-ttu-id="51e7b-142">원본 서버의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51e7b-142">Specifies the path of the origin server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51e7b-143">-/Profile</span><span class="sxs-lookup"><span data-stu-id="51e7b-143">-ProfileName</span></span>
<span data-ttu-id="51e7b-144">프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51e7b-144">Specifies the name of the profile.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51e7b-145">-QueryStringCachingBehavior</span><span class="sxs-lookup"><span data-stu-id="51e7b-145">-QueryStringCachingBehavior</span></span>
<span data-ttu-id="51e7b-146">쿼리 문자열이 요청 URL에 있을 때 CDN 끝점의 동작을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51e7b-146">Specifies the behavior of CDN endpoint when a query string is in the request URL.</span></span>

```yaml
Type: PSQueryStringCachingBehavior
Parameter Sets: (All)
Aliases:
Accepted values: IgnoreQueryString, BypassCaching, UseQueryString, NotSet

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51e7b-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51e7b-147">-ResourceGroupName</span></span>
<span data-ttu-id="51e7b-148">이 끝점이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51e7b-148">Specifies the name of the resource group to which this endpoint belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51e7b-149">태그</span><span class="sxs-lookup"><span data-stu-id="51e7b-149">-Tag</span></span>
<span data-ttu-id="51e7b-150">Azure CDN 끝점과 연결할 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="51e7b-150">The tags to associate with the Azure CDN endpoint.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51e7b-151">-확인</span><span class="sxs-lookup"><span data-stu-id="51e7b-151">-Confirm</span></span>
<span data-ttu-id="51e7b-152">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="51e7b-152">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51e7b-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51e7b-153">-WhatIf</span></span>
<span data-ttu-id="51e7b-154">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="51e7b-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51e7b-155">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="51e7b-155">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51e7b-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51e7b-156">CommonParameters</span></span>
<span data-ttu-id="51e7b-157">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="51e7b-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51e7b-158">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51e7b-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51e7b-159">입력</span><span class="sxs-lookup"><span data-stu-id="51e7b-159">INPUTS</span></span>

### <span data-ttu-id="51e7b-160">PSProfile</span><span class="sxs-lookup"><span data-stu-id="51e7b-160">PSProfile</span></span>
<span data-ttu-id="51e7b-161">' CdnProfile ' 매개 변수는 파이프라인에서 ' PSProfile ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="51e7b-161">Parameter 'CdnProfile' accepts value of type 'PSProfile' from the pipeline</span></span>

## <span data-ttu-id="51e7b-162">출력</span><span class="sxs-lookup"><span data-stu-id="51e7b-162">OUTPUTS</span></span>

### <span data-ttu-id="51e7b-163">Microsoft. Cdn. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="51e7b-163">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="51e7b-164">상속자</span><span class="sxs-lookup"><span data-stu-id="51e7b-164">NOTES</span></span>

## <span data-ttu-id="51e7b-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="51e7b-165">RELATED LINKS</span></span>

[<span data-ttu-id="51e7b-166">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="51e7b-166">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="51e7b-167">제거-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="51e7b-167">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="51e7b-168">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="51e7b-168">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="51e7b-169">시작-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="51e7b-169">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="51e7b-170">중지-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="51e7b-170">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


