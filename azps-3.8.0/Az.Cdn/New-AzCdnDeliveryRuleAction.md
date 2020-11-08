---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliveryruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleAction.md
ms.openlocfilehash: d893850105656a9f599870e2ef17a6b195254ad6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042847"
---
# <span data-ttu-id="d35e3-101">New-AzCdnDeliveryRuleAction</span><span class="sxs-lookup"><span data-stu-id="d35e3-101">New-AzCdnDeliveryRuleAction</span></span>

## <span data-ttu-id="d35e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d35e3-102">SYNOPSIS</span></span>
<span data-ttu-id="d35e3-103">배달 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d35e3-103">Creates a delivery action.</span></span>

## <span data-ttu-id="d35e3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d35e3-104">SYNTAX</span></span>

### <span data-ttu-id="d35e3-105">CacheExpirationActionParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="d35e3-105">CacheExpirationActionParameterSet (Default)</span></span>
```
New-AzCdnDeliveryRuleAction -CacheBehavior <String> [-CacheDuration <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d35e3-106">HeaderActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="d35e3-106">HeaderActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -HeaderActionType <String> -Action <String> -HeaderName <String> [-Value <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d35e3-107">UrlRedirectActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="d35e3-107">UrlRedirectActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -RedirectType <String> [-DestinationProtocol <String>] [-CustomPath <String>]
 [-CustomHostname <String>] [-CustomQueryString <String>] [-CustomFragment <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d35e3-108">CacheKeyQueryStringActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="d35e3-108">CacheKeyQueryStringActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -QueryStringBehavior <String> [-QueryParameter <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d35e3-109">UrlRewriteActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="d35e3-109">UrlRewriteActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -SourcePattern <String> -Destination <String> [-PreservePath]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d35e3-110">설명은</span><span class="sxs-lookup"><span data-stu-id="d35e3-110">DESCRIPTION</span></span>
<span data-ttu-id="d35e3-111">**AzCdnDeliveryRule** CMDLET은 CDN 끝점 만들기에 대 한 배달 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d35e3-111">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="d35e3-112">예제의</span><span class="sxs-lookup"><span data-stu-id="d35e3-112">EXAMPLES</span></span>

### <span data-ttu-id="d35e3-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="d35e3-113">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRuleAction -HeaderActionType ModifyRequestHeader -Action Append -HeaderName "Accept-Encoding" -Value "gzip"

HeaderActionType    Action HeaderName      Value
----------------    ------ ----------      -----
ModifyRequestHeader Append Accept-Encoding gzip
```

<span data-ttu-id="d35e3-114">간단한 배달 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d35e3-114">Create a simple delivery rule.</span></span>

## <span data-ttu-id="d35e3-115">변수</span><span class="sxs-lookup"><span data-stu-id="d35e3-115">PARAMETERS</span></span>

### <span data-ttu-id="d35e3-116">-작업</span><span class="sxs-lookup"><span data-stu-id="d35e3-116">-Action</span></span>
<span data-ttu-id="d35e3-117">수행할 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="d35e3-117">Action to perform.</span></span>

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

### <span data-ttu-id="d35e3-118">-CacheBehavior</span><span class="sxs-lookup"><span data-stu-id="d35e3-118">-CacheBehavior</span></span>
<span data-ttu-id="d35e3-119">작업에 대 한 캐싱 동작</span><span class="sxs-lookup"><span data-stu-id="d35e3-119">Caching behavior for the action</span></span>

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

### <span data-ttu-id="d35e3-120">-CacheDuration</span><span class="sxs-lookup"><span data-stu-id="d35e3-120">-CacheDuration</span></span>
<span data-ttu-id="d35e3-121">콘텐츠를 캐시 해야 하는 기간입니다.</span><span class="sxs-lookup"><span data-stu-id="d35e3-121">The duration for which the content needs to be cached.</span></span>
<span data-ttu-id="d35e3-122">허용 되는 형식은 \[ d입니다. \] hh: mm: ss</span><span class="sxs-lookup"><span data-stu-id="d35e3-122">Allowed format is \[d.\]hh:mm:ss</span></span>

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

### <span data-ttu-id="d35e3-123">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="d35e3-123">-CustomFragment</span></span>
<span data-ttu-id="d35e3-124">리디렉션 URL에 추가할 조각입니다.</span><span class="sxs-lookup"><span data-stu-id="d35e3-124">Fragment to add to the redirect URL.</span></span>
<span data-ttu-id="d35e3-125">단편은 # 다음에 오는 URL의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="d35e3-125">Fragment is the part of the URL that comes after #.</span></span>
<span data-ttu-id="d35e3-126"># .를 포함 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="d35e3-126">Do not include the #.</span></span>

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

### <span data-ttu-id="d35e3-127">-CustomHostname</span><span class="sxs-lookup"><span data-stu-id="d35e3-127">-CustomHostname</span></span>
<span data-ttu-id="d35e3-128">리디렉션할 호스트입니다.</span><span class="sxs-lookup"><span data-stu-id="d35e3-128">Host to redirect.</span></span>
<span data-ttu-id="d35e3-129">들어오는 호스트를 대상 호스트로 사용 하려면 비워 두세요.</span><span class="sxs-lookup"><span data-stu-id="d35e3-129">Leave empty to use the incoming host as the destination host.</span></span>

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

### <span data-ttu-id="d35e3-130">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="d35e3-130">-CustomPath</span></span>
<span data-ttu-id="d35e3-131">리디렉션할 전체 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="d35e3-131">The full path to redirect.</span></span>
<span data-ttu-id="d35e3-132">경로는 비워 둘 수 없으며/로 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d35e3-132">Path cannot be empty and must start with /.</span></span>
<span data-ttu-id="d35e3-133">들어오는 경로를 대상 경로로 사용 하려면 비워 두세요.</span><span class="sxs-lookup"><span data-stu-id="d35e3-133">Leave empty to use the incoming path as destination path.</span></span>

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

### <span data-ttu-id="d35e3-134">-CustomQueryString 쿼리</span><span class="sxs-lookup"><span data-stu-id="d35e3-134">-CustomQueryString</span></span>
<span data-ttu-id="d35e3-135">리디렉션 URL에 배치할 쿼리 문자열 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="d35e3-135">The set of query strings to be placed in the redirect URL.</span></span>
<span data-ttu-id="d35e3-136">이 값을 설정 하면 기존 쿼리 문자열이 바뀝니다. 수신 쿼리 문자열을 보존 하려면 비워 둡니다.</span><span class="sxs-lookup"><span data-stu-id="d35e3-136">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span>
<span data-ttu-id="d35e3-137">쿼리 문자열은 \< 키 \> = \< 값 \> 형식 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d35e3-137">Query string must be in \<key\>=\<value\> format.</span></span>
<span data-ttu-id="d35e3-138">?</span><span class="sxs-lookup"><span data-stu-id="d35e3-138">?</span></span> <span data-ttu-id="d35e3-139">및 &는 자동으로 추가 되므로이를 포함 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d35e3-139">and & will be added automatically so do not include them.</span></span>

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

### <span data-ttu-id="d35e3-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d35e3-140">-DefaultProfile</span></span>
<span data-ttu-id="d35e3-141">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d35e3-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d35e3-142">-대상</span><span class="sxs-lookup"><span data-stu-id="d35e3-142">-Destination</span></span>
<span data-ttu-id="d35e3-143">위의 요청이 다시 작성 될 상대 URL을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="d35e3-143">Define the relative URL to which the above requests will be rewritten by.</span></span>

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

### <span data-ttu-id="d35e3-144">-DestinationProtocol</span><span class="sxs-lookup"><span data-stu-id="d35e3-144">-DestinationProtocol</span></span>
<span data-ttu-id="d35e3-145">리디렉션에 사용할 프로토콜입니다.</span><span class="sxs-lookup"><span data-stu-id="d35e3-145">Protocol to use for the redirect.</span></span>
<span data-ttu-id="d35e3-146">기본 값은 MatchRequest입니다.</span><span class="sxs-lookup"><span data-stu-id="d35e3-146">The default value is MatchRequest.</span></span>

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

### <span data-ttu-id="d35e3-147">-HeaderActionType</span><span class="sxs-lookup"><span data-stu-id="d35e3-147">-HeaderActionType</span></span>
<span data-ttu-id="d35e3-148">요청 헤더 또는 응답 헤더를 수정할지 여부</span><span class="sxs-lookup"><span data-stu-id="d35e3-148">Whether to modify request header or response header</span></span>

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

### <span data-ttu-id="d35e3-149">-인원 Ername</span><span class="sxs-lookup"><span data-stu-id="d35e3-149">-HeaderName</span></span>
<span data-ttu-id="d35e3-150">수정할 머리글의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d35e3-150">Name of the header to modify.</span></span>

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

### <span data-ttu-id="d35e3-151">-PreservePath</span><span class="sxs-lookup"><span data-stu-id="d35e3-151">-PreservePath</span></span>
<span data-ttu-id="d35e3-152">일치 하지 않는 경로를 유지할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d35e3-152">Whether to preserve unmatched path.</span></span>

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

### <span data-ttu-id="d35e3-153">-QueryParameter</span><span class="sxs-lookup"><span data-stu-id="d35e3-153">-QueryParameter</span></span>
<span data-ttu-id="d35e3-154">포함 하거나 제외할 쿼리 매개 변수 (쉼표 구분)</span><span class="sxs-lookup"><span data-stu-id="d35e3-154">Query parameters to include or exclude (comma separated).</span></span>

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

### <span data-ttu-id="d35e3-155">-QueryStringBehavior</span><span class="sxs-lookup"><span data-stu-id="d35e3-155">-QueryStringBehavior</span></span>
<span data-ttu-id="d35e3-156">요청에 대 한 QueryString 동작</span><span class="sxs-lookup"><span data-stu-id="d35e3-156">QueryString behavior for the requests</span></span>

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

### <span data-ttu-id="d35e3-157">RedirectType</span><span class="sxs-lookup"><span data-stu-id="d35e3-157">-RedirectType</span></span>
<span data-ttu-id="d35e3-158">트래픽 리디렉션을 위해 규칙이 사용 하는 리디렉션 유형</span><span class="sxs-lookup"><span data-stu-id="d35e3-158">The redirect type the rule will use when redirecting traffic</span></span>

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

### <span data-ttu-id="d35e3-159">-SourcePattern</span><span class="sxs-lookup"><span data-stu-id="d35e3-159">-SourcePattern</span></span>
<span data-ttu-id="d35e3-160">다시 작성할 수 있는 요청 유형을 식별 하는 요청 URI 패턴을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="d35e3-160">Define a request URI pattern that identifies the type of requests that may be rewritten.</span></span> <span data-ttu-id="d35e3-161">값이 비어 있으면 모든 문자열이 일치 합니다.</span><span class="sxs-lookup"><span data-stu-id="d35e3-161">If value is blank, all strings are matched.</span></span>

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

### <span data-ttu-id="d35e3-162">-값</span><span class="sxs-lookup"><span data-stu-id="d35e3-162">-Value</span></span>
<span data-ttu-id="d35e3-163">지정 된 작업에 대 한 값입니다.</span><span class="sxs-lookup"><span data-stu-id="d35e3-163">Value for the specified action.</span></span>

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

### <span data-ttu-id="d35e3-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d35e3-164">CommonParameters</span></span>
<span data-ttu-id="d35e3-165">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d35e3-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d35e3-166">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d35e3-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d35e3-167">입력</span><span class="sxs-lookup"><span data-stu-id="d35e3-167">INPUTS</span></span>

### <span data-ttu-id="d35e3-168">않아야</span><span class="sxs-lookup"><span data-stu-id="d35e3-168">None</span></span>

## <span data-ttu-id="d35e3-169">출력</span><span class="sxs-lookup"><span data-stu-id="d35e3-169">OUTPUTS</span></span>

### <span data-ttu-id="d35e3-170">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction</span><span class="sxs-lookup"><span data-stu-id="d35e3-170">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction</span></span>

## <span data-ttu-id="d35e3-171">상속자</span><span class="sxs-lookup"><span data-stu-id="d35e3-171">NOTES</span></span>

## <span data-ttu-id="d35e3-172">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d35e3-172">RELATED LINKS</span></span>
