---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/new-azcdndeliveryruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleAction.md
ms.openlocfilehash: 127c73a34b030a991b5875f141ea8dd850a4f0a1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009248"
---
# <span data-ttu-id="d6cda-101">New-AzCdnDeliveryRuleAction</span><span class="sxs-lookup"><span data-stu-id="d6cda-101">New-AzCdnDeliveryRuleAction</span></span>

## <span data-ttu-id="d6cda-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6cda-102">SYNOPSIS</span></span>
<span data-ttu-id="d6cda-103">배달 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d6cda-103">Creates a delivery action.</span></span>

## <span data-ttu-id="d6cda-104">구문</span><span class="sxs-lookup"><span data-stu-id="d6cda-104">SYNTAX</span></span>

### <span data-ttu-id="d6cda-105">CacheExpirationActionParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="d6cda-105">CacheExpirationActionParameterSet (Default)</span></span>
```
New-AzCdnDeliveryRuleAction -CacheBehavior <String> [-CacheDuration <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6cda-106">HeaderActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6cda-106">HeaderActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -HeaderActionType <String> -Action <String> -HeaderName <String> [-Value <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6cda-107">UrlRedirectActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6cda-107">UrlRedirectActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -RedirectType <String> [-DestinationProtocol <String>] [-CustomPath <String>]
 [-CustomHostname <String>] [-CustomQueryString <String>] [-CustomFragment <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6cda-108">CacheKeyQueryStringActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6cda-108">CacheKeyQueryStringActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -QueryStringBehavior <String> [-QueryParameter <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6cda-109">URLRewriteActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6cda-109">UrlRewriteActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -SourcePattern <String> -Destination <String> [-PreservePath]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6cda-110">설명</span><span class="sxs-lookup"><span data-stu-id="d6cda-110">DESCRIPTION</span></span>
<span data-ttu-id="d6cda-111">**New-AzCdnDeliveryRule** cmdlet은 CDN 엔드포인트 만들기에 대한 배달 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d6cda-111">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="d6cda-112">예제</span><span class="sxs-lookup"><span data-stu-id="d6cda-112">EXAMPLES</span></span>

### <span data-ttu-id="d6cda-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="d6cda-113">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRuleAction -HeaderActionType ModifyRequestHeader -Action Append -HeaderName "Accept-Encoding" -Value "gzip"

HeaderActionType    Action HeaderName      Value
----------------    ------ ----------      -----
ModifyRequestHeader Append Accept-Encoding gzip
```

<span data-ttu-id="d6cda-114">간단한 배달 규칙을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d6cda-114">Create a simple delivery rule.</span></span>

## <span data-ttu-id="d6cda-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d6cda-115">PARAMETERS</span></span>

### <span data-ttu-id="d6cda-116">-Action</span><span class="sxs-lookup"><span data-stu-id="d6cda-116">-Action</span></span>
<span data-ttu-id="d6cda-117">수행할 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="d6cda-117">Action to perform.</span></span>

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

### <span data-ttu-id="d6cda-118">-CacheBehavior</span><span class="sxs-lookup"><span data-stu-id="d6cda-118">-CacheBehavior</span></span>
<span data-ttu-id="d6cda-119">작업의 캐싱 동작</span><span class="sxs-lookup"><span data-stu-id="d6cda-119">Caching behavior for the action</span></span>

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

### <span data-ttu-id="d6cda-120">-CacheDuration</span><span class="sxs-lookup"><span data-stu-id="d6cda-120">-CacheDuration</span></span>
<span data-ttu-id="d6cda-121">콘텐츠를 캐시해야 하는 기간입니다.</span><span class="sxs-lookup"><span data-stu-id="d6cda-121">The duration for which the content needs to be cached.</span></span>
<span data-ttu-id="d6cda-122">허용되는 형식은 \[ d입니다. \] hh:mm:ss</span><span class="sxs-lookup"><span data-stu-id="d6cda-122">Allowed format is \[d.\]hh:mm:ss</span></span>

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

### <span data-ttu-id="d6cda-123">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="d6cda-123">-CustomFragment</span></span>
<span data-ttu-id="d6cda-124">리디렉션 URL에 추가할 조각입니다.</span><span class="sxs-lookup"><span data-stu-id="d6cda-124">Fragment to add to the redirect URL.</span></span>
<span data-ttu-id="d6cda-125">조각은 #에 나오는 URL의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="d6cda-125">Fragment is the part of the URL that comes after #.</span></span>
<span data-ttu-id="d6cda-126">#을 포함하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d6cda-126">Do not include the #.</span></span>

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

### <span data-ttu-id="d6cda-127">-CustomHostname</span><span class="sxs-lookup"><span data-stu-id="d6cda-127">-CustomHostname</span></span>
<span data-ttu-id="d6cda-128">리디렉션할 호스트입니다.</span><span class="sxs-lookup"><span data-stu-id="d6cda-128">Host to redirect.</span></span>
<span data-ttu-id="d6cda-129">수신 호스트를 대상 호스트로 사용하기 위해 비워 두면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d6cda-129">Leave empty to use the incoming host as the destination host.</span></span>

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

### <span data-ttu-id="d6cda-130">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="d6cda-130">-CustomPath</span></span>
<span data-ttu-id="d6cda-131">리디렉션할 전체 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="d6cda-131">The full path to redirect.</span></span>
<span data-ttu-id="d6cda-132">경로는 비어 있을 수 없습니다. /로 시작해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6cda-132">Path cannot be empty and must start with /.</span></span>
<span data-ttu-id="d6cda-133">들어오는 경로를 대상 경로로 사용하기 위해 비워 두면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d6cda-133">Leave empty to use the incoming path as destination path.</span></span>

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

### <span data-ttu-id="d6cda-134">-CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="d6cda-134">-CustomQueryString</span></span>
<span data-ttu-id="d6cda-135">리디렉션 URL에 배치할 쿼리 문자열 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="d6cda-135">The set of query strings to be placed in the redirect URL.</span></span>
<span data-ttu-id="d6cda-136">이 값을 설정하면 기존 쿼리 문자열이 대체됩니다. 들어오는 쿼리 문자열을 보존하기 위해 비워 두면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d6cda-136">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span>
<span data-ttu-id="d6cda-137">쿼리 문자열은 형식이 있어야 \<key\> = \<value\> 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6cda-137">Query string must be in \<key\>=\<value\> format.</span></span>
<span data-ttu-id="d6cda-138">?</span><span class="sxs-lookup"><span data-stu-id="d6cda-138">?</span></span> <span data-ttu-id="d6cda-139">및 & 자동으로 추가될 수 있으므로 포함하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d6cda-139">and & will be added automatically so do not include them.</span></span>

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

### <span data-ttu-id="d6cda-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6cda-140">-DefaultProfile</span></span>
<span data-ttu-id="d6cda-141">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d6cda-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6cda-142">-대상</span><span class="sxs-lookup"><span data-stu-id="d6cda-142">-Destination</span></span>
<span data-ttu-id="d6cda-143">위의 요청을 다시 입력할 상대 URL을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="d6cda-143">Define the relative URL to which the above requests will be rewritten by.</span></span>

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

### <span data-ttu-id="d6cda-144">-DestinationProtocol</span><span class="sxs-lookup"><span data-stu-id="d6cda-144">-DestinationProtocol</span></span>
<span data-ttu-id="d6cda-145">리디렉션에 사용할 프로토콜입니다.</span><span class="sxs-lookup"><span data-stu-id="d6cda-145">Protocol to use for the redirect.</span></span>
<span data-ttu-id="d6cda-146">기본값은 MatchRequest입니다.</span><span class="sxs-lookup"><span data-stu-id="d6cda-146">The default value is MatchRequest.</span></span>

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

### <span data-ttu-id="d6cda-147">-HeaderActionType</span><span class="sxs-lookup"><span data-stu-id="d6cda-147">-HeaderActionType</span></span>
<span data-ttu-id="d6cda-148">요청 헤더 또는 응답 헤더를 수정할지 여부</span><span class="sxs-lookup"><span data-stu-id="d6cda-148">Whether to modify request header or response header</span></span>

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

### <span data-ttu-id="d6cda-149">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="d6cda-149">-HeaderName</span></span>
<span data-ttu-id="d6cda-150">수정할 헤더의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d6cda-150">Name of the header to modify.</span></span>

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

### <span data-ttu-id="d6cda-151">-PreservePath</span><span class="sxs-lookup"><span data-stu-id="d6cda-151">-PreservePath</span></span>
<span data-ttu-id="d6cda-152">비할 데 없는 경로를 보존할지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="d6cda-152">Whether to preserve unmatched path.</span></span>

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

### <span data-ttu-id="d6cda-153">-QueryParameter</span><span class="sxs-lookup"><span data-stu-id="d6cda-153">-QueryParameter</span></span>
<span data-ttu-id="d6cda-154">포함하거나 제외할 쿼리 매개 변수(콤마 분리).</span><span class="sxs-lookup"><span data-stu-id="d6cda-154">Query parameters to include or exclude (comma separated).</span></span>

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

### <span data-ttu-id="d6cda-155">-QueryStringBehavior</span><span class="sxs-lookup"><span data-stu-id="d6cda-155">-QueryStringBehavior</span></span>
<span data-ttu-id="d6cda-156">요청에 대한 QueryString 동작</span><span class="sxs-lookup"><span data-stu-id="d6cda-156">QueryString behavior for the requests</span></span>

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

### <span data-ttu-id="d6cda-157">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="d6cda-157">-RedirectType</span></span>
<span data-ttu-id="d6cda-158">트래픽을 리디렉션할 때 규칙이 사용할 리디렉션 유형</span><span class="sxs-lookup"><span data-stu-id="d6cda-158">The redirect type the rule will use when redirecting traffic</span></span>

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

### <span data-ttu-id="d6cda-159">-SourcePattern</span><span class="sxs-lookup"><span data-stu-id="d6cda-159">-SourcePattern</span></span>
<span data-ttu-id="d6cda-160">다시 입력할 수 있는 요청 유형을 식별하는 요청 URI 패턴을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="d6cda-160">Define a request URI pattern that identifies the type of requests that may be rewritten.</span></span> <span data-ttu-id="d6cda-161">값이 비어 있는 경우 모든 문자열이 일치합니다.</span><span class="sxs-lookup"><span data-stu-id="d6cda-161">If value is blank, all strings are matched.</span></span>

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

### <span data-ttu-id="d6cda-162">-Value</span><span class="sxs-lookup"><span data-stu-id="d6cda-162">-Value</span></span>
<span data-ttu-id="d6cda-163">지정된 작업의 값입니다.</span><span class="sxs-lookup"><span data-stu-id="d6cda-163">Value for the specified action.</span></span>

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

### <span data-ttu-id="d6cda-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6cda-164">CommonParameters</span></span>
<span data-ttu-id="d6cda-165">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d6cda-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6cda-166">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d6cda-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6cda-167">입력</span><span class="sxs-lookup"><span data-stu-id="d6cda-167">INPUTS</span></span>

### <span data-ttu-id="d6cda-168">없음</span><span class="sxs-lookup"><span data-stu-id="d6cda-168">None</span></span>

## <span data-ttu-id="d6cda-169">출력</span><span class="sxs-lookup"><span data-stu-id="d6cda-169">OUTPUTS</span></span>

### <span data-ttu-id="d6cda-170">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction</span><span class="sxs-lookup"><span data-stu-id="d6cda-170">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction</span></span>

## <span data-ttu-id="d6cda-171">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d6cda-171">NOTES</span></span>

## <span data-ttu-id="d6cda-172">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d6cda-172">RELATED LINKS</span></span>
