---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliveryruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleAction.md
ms.openlocfilehash: d893850105656a9f599870e2ef17a6b195254ad6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177873"
---
# <span data-ttu-id="9b98e-101">New-AzCdnDeliveryRuleAction</span><span class="sxs-lookup"><span data-stu-id="9b98e-101">New-AzCdnDeliveryRuleAction</span></span>

## <span data-ttu-id="9b98e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b98e-102">SYNOPSIS</span></span>
<span data-ttu-id="9b98e-103">배달 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9b98e-103">Creates a delivery action.</span></span>

## <span data-ttu-id="9b98e-104">구문</span><span class="sxs-lookup"><span data-stu-id="9b98e-104">SYNTAX</span></span>

### <span data-ttu-id="9b98e-105">CacheExpirationActionParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="9b98e-105">CacheExpirationActionParameterSet (Default)</span></span>
```
New-AzCdnDeliveryRuleAction -CacheBehavior <String> [-CacheDuration <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b98e-106">HeaderActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b98e-106">HeaderActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -HeaderActionType <String> -Action <String> -HeaderName <String> [-Value <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b98e-107">UrlRedirectActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b98e-107">UrlRedirectActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -RedirectType <String> [-DestinationProtocol <String>] [-CustomPath <String>]
 [-CustomHostname <String>] [-CustomQueryString <String>] [-CustomFragment <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b98e-108">CacheKeyQueryStringActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b98e-108">CacheKeyQueryStringActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -QueryStringBehavior <String> [-QueryParameter <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b98e-109">UrlRewriteActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b98e-109">UrlRewriteActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -SourcePattern <String> -Destination <String> [-PreservePath]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b98e-110">설명</span><span class="sxs-lookup"><span data-stu-id="9b98e-110">DESCRIPTION</span></span>
<span data-ttu-id="9b98e-111">**New-AzCdnDeliveryRule** cmdlet은 CDN 엔드포인트를 만들기 위한 배달 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9b98e-111">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="9b98e-112">예제</span><span class="sxs-lookup"><span data-stu-id="9b98e-112">EXAMPLES</span></span>

### <span data-ttu-id="9b98e-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="9b98e-113">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRuleAction -HeaderActionType ModifyRequestHeader -Action Append -HeaderName "Accept-Encoding" -Value "gzip"

HeaderActionType    Action HeaderName      Value
----------------    ------ ----------      -----
ModifyRequestHeader Append Accept-Encoding gzip
```

<span data-ttu-id="9b98e-114">간단한 배달 규칙을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9b98e-114">Create a simple delivery rule.</span></span>

## <span data-ttu-id="9b98e-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9b98e-115">PARAMETERS</span></span>

### <span data-ttu-id="9b98e-116">-Action</span><span class="sxs-lookup"><span data-stu-id="9b98e-116">-Action</span></span>
<span data-ttu-id="9b98e-117">수행할 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="9b98e-117">Action to perform.</span></span>

```yaml
Type: System.String
Parameter Sets: HeaderActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b98e-118">-CacheBehavior</span><span class="sxs-lookup"><span data-stu-id="9b98e-118">-CacheBehavior</span></span>
<span data-ttu-id="9b98e-119">동작에 대한 캐싱 동작</span><span class="sxs-lookup"><span data-stu-id="9b98e-119">Caching behavior for the action</span></span>

```yaml
Type: System.String
Parameter Sets: CacheExpirationActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b98e-120">-CacheDuration</span><span class="sxs-lookup"><span data-stu-id="9b98e-120">-CacheDuration</span></span>
<span data-ttu-id="9b98e-121">콘텐츠를 캐시해야 하는 기간입니다.</span><span class="sxs-lookup"><span data-stu-id="9b98e-121">The duration for which the content needs to be cached.</span></span>
<span data-ttu-id="9b98e-122">허용되는 형식은 \[ d입니다. \] hh:mm:ss</span><span class="sxs-lookup"><span data-stu-id="9b98e-122">Allowed format is \[d.\]hh:mm:ss</span></span>

```yaml
Type: System.String
Parameter Sets: CacheExpirationActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b98e-123">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="9b98e-123">-CustomFragment</span></span>
<span data-ttu-id="9b98e-124">리디렉션 URL에 추가할 조각입니다.</span><span class="sxs-lookup"><span data-stu-id="9b98e-124">Fragment to add to the redirect URL.</span></span>
<span data-ttu-id="9b98e-125">조각은 #다음에 오는 URL의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="9b98e-125">Fragment is the part of the URL that comes after #.</span></span>
<span data-ttu-id="9b98e-126">#을 포함하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9b98e-126">Do not include the #.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b98e-127">-CustomHostname</span><span class="sxs-lookup"><span data-stu-id="9b98e-127">-CustomHostname</span></span>
<span data-ttu-id="9b98e-128">리디렉션할 호스트입니다.</span><span class="sxs-lookup"><span data-stu-id="9b98e-128">Host to redirect.</span></span>
<span data-ttu-id="9b98e-129">들어오는 호스트를 대상 호스트로 사용하길 빈 채로 하세요.</span><span class="sxs-lookup"><span data-stu-id="9b98e-129">Leave empty to use the incoming host as the destination host.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b98e-130">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="9b98e-130">-CustomPath</span></span>
<span data-ttu-id="9b98e-131">리디렉션할 전체 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="9b98e-131">The full path to redirect.</span></span>
<span data-ttu-id="9b98e-132">경로는 비어 있을 수 없습니다. /로 시작해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b98e-132">Path cannot be empty and must start with /.</span></span>
<span data-ttu-id="9b98e-133">들어오는 경로를 대상 경로로 사용하길 빈 채로 하세요.</span><span class="sxs-lookup"><span data-stu-id="9b98e-133">Leave empty to use the incoming path as destination path.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b98e-134">-CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="9b98e-134">-CustomQueryString</span></span>
<span data-ttu-id="9b98e-135">리디렉션 URL에 배치할 쿼리 문자열 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="9b98e-135">The set of query strings to be placed in the redirect URL.</span></span>
<span data-ttu-id="9b98e-136">이 값을 설정하면 기존 쿼리 문자열이 대체됩니다. 들어오는 쿼리 문자열을 보존하기 위해 비워 두기</span><span class="sxs-lookup"><span data-stu-id="9b98e-136">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span>
<span data-ttu-id="9b98e-137">쿼리 문자열은 형식이 있어야 \<key\> = \<value\> 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b98e-137">Query string must be in \<key\>=\<value\> format.</span></span>
<span data-ttu-id="9b98e-138">?</span><span class="sxs-lookup"><span data-stu-id="9b98e-138">?</span></span> <span data-ttu-id="9b98e-139">를 & 자동으로 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="9b98e-139">and & will be added automatically so do not include them.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b98e-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b98e-140">-DefaultProfile</span></span>
<span data-ttu-id="9b98e-141">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9b98e-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b98e-142">-Destination</span><span class="sxs-lookup"><span data-stu-id="9b98e-142">-Destination</span></span>
<span data-ttu-id="9b98e-143">위의 요청이 다시 덮어질 상대 URL을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="9b98e-143">Define the relative URL to which the above requests will be rewritten by.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRewriteActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b98e-144">-DestinationProtocol</span><span class="sxs-lookup"><span data-stu-id="9b98e-144">-DestinationProtocol</span></span>
<span data-ttu-id="9b98e-145">리디렉션에 사용할 프로토콜입니다.</span><span class="sxs-lookup"><span data-stu-id="9b98e-145">Protocol to use for the redirect.</span></span>
<span data-ttu-id="9b98e-146">기본값은 MatchRequest입니다.</span><span class="sxs-lookup"><span data-stu-id="9b98e-146">The default value is MatchRequest.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b98e-147">-HeaderActionType</span><span class="sxs-lookup"><span data-stu-id="9b98e-147">-HeaderActionType</span></span>
<span data-ttu-id="9b98e-148">요청 헤더 또는 응답 헤더를 수정할지 여부</span><span class="sxs-lookup"><span data-stu-id="9b98e-148">Whether to modify request header or response header</span></span>

```yaml
Type: System.String
Parameter Sets: HeaderActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b98e-149">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="9b98e-149">-HeaderName</span></span>
<span data-ttu-id="9b98e-150">수정할 헤더의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9b98e-150">Name of the header to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: HeaderActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b98e-151">-PreservePath</span><span class="sxs-lookup"><span data-stu-id="9b98e-151">-PreservePath</span></span>
<span data-ttu-id="9b98e-152">불일치 경로를 보존할지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="9b98e-152">Whether to preserve unmatched path.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UrlRewriteActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b98e-153">-QueryParameter</span><span class="sxs-lookup"><span data-stu-id="9b98e-153">-QueryParameter</span></span>
<span data-ttu-id="9b98e-154">포함하거나 제외할 쿼리 매개 변수입니다(콤마로 구분).</span><span class="sxs-lookup"><span data-stu-id="9b98e-154">Query parameters to include or exclude (comma separated).</span></span>

```yaml
Type: System.String[]
Parameter Sets: CacheKeyQueryStringActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b98e-155">-QueryStringBehavior</span><span class="sxs-lookup"><span data-stu-id="9b98e-155">-QueryStringBehavior</span></span>
<span data-ttu-id="9b98e-156">요청에 대한 QueryString 동작</span><span class="sxs-lookup"><span data-stu-id="9b98e-156">QueryString behavior for the requests</span></span>

```yaml
Type: System.String
Parameter Sets: CacheKeyQueryStringActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b98e-157">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="9b98e-157">-RedirectType</span></span>
<span data-ttu-id="9b98e-158">트래픽을 리디렉션할 때 규칙이 사용할 리디렉션 유형</span><span class="sxs-lookup"><span data-stu-id="9b98e-158">The redirect type the rule will use when redirecting traffic</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b98e-159">-SourcePattern</span><span class="sxs-lookup"><span data-stu-id="9b98e-159">-SourcePattern</span></span>
<span data-ttu-id="9b98e-160">다시 입력할 수 있는 요청 유형을 식별하는 요청 URI 패턴을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="9b98e-160">Define a request URI pattern that identifies the type of requests that may be rewritten.</span></span> <span data-ttu-id="9b98e-161">값이 비어 있는 경우 모든 문자열이 일치합니다.</span><span class="sxs-lookup"><span data-stu-id="9b98e-161">If value is blank, all strings are matched.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRewriteActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b98e-162">-Value</span><span class="sxs-lookup"><span data-stu-id="9b98e-162">-Value</span></span>
<span data-ttu-id="9b98e-163">지정된 작업의 값입니다.</span><span class="sxs-lookup"><span data-stu-id="9b98e-163">Value for the specified action.</span></span>

```yaml
Type: System.String
Parameter Sets: HeaderActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b98e-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b98e-164">CommonParameters</span></span>
<span data-ttu-id="9b98e-165">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9b98e-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b98e-166">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9b98e-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b98e-167">입력</span><span class="sxs-lookup"><span data-stu-id="9b98e-167">INPUTS</span></span>

### <span data-ttu-id="9b98e-168">없음</span><span class="sxs-lookup"><span data-stu-id="9b98e-168">None</span></span>

## <span data-ttu-id="9b98e-169">출력</span><span class="sxs-lookup"><span data-stu-id="9b98e-169">OUTPUTS</span></span>

### <span data-ttu-id="9b98e-170">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction</span><span class="sxs-lookup"><span data-stu-id="9b98e-170">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction</span></span>

## <span data-ttu-id="9b98e-171">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9b98e-171">NOTES</span></span>

## <span data-ttu-id="9b98e-172">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9b98e-172">RELATED LINKS</span></span>