---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliveryruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleAction.md
ms.openlocfilehash: a1ebadb47bbde091ca6b430fab86111b35bf34bc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697587"
---
# <span data-ttu-id="fddbd-101">New-AzCdnDeliveryRuleAction</span><span class="sxs-lookup"><span data-stu-id="fddbd-101">New-AzCdnDeliveryRuleAction</span></span>

## <span data-ttu-id="fddbd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fddbd-102">SYNOPSIS</span></span>
<span data-ttu-id="fddbd-103">배달 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fddbd-103">Creates a delivery action.</span></span>

## <span data-ttu-id="fddbd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fddbd-104">SYNTAX</span></span>

### <span data-ttu-id="fddbd-105">CacheExpirationActionParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="fddbd-105">CacheExpirationActionParameterSet (Default)</span></span>
```
New-AzCdnDeliveryRuleAction -CacheBehavior <String> [-CacheDuration <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fddbd-106">HeaderActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="fddbd-106">HeaderActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -HeaderActionType <String> -Action <String> -HeaderName <String> [-Value <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fddbd-107">UrlRedirectActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="fddbd-107">UrlRedirectActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -RedirectType <String> [-DestinationProtocol <String>] [-CustomPath <String>]
 [-CustomHostname <String>] [-CustomQueryString <String>] [-CustomFragment <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fddbd-108">설명은</span><span class="sxs-lookup"><span data-stu-id="fddbd-108">DESCRIPTION</span></span>
<span data-ttu-id="fddbd-109">**AzCdnDeliveryRule** CMDLET은 CDN 끝점 만들기에 대 한 배달 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fddbd-109">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="fddbd-110">예제의</span><span class="sxs-lookup"><span data-stu-id="fddbd-110">EXAMPLES</span></span>

### <span data-ttu-id="fddbd-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="fddbd-111">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRuleAction -HeaderActionType ModifyRequestHeader -Action Append -HeaderName "Accept-Encoding" -Value "gzip"

HeaderActionType    Action HeaderName      Value
----------------    ------ ----------      -----
ModifyRequestHeader Append Accept-Encoding gzip
```

<span data-ttu-id="fddbd-112">간단한 배달 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fddbd-112">Create a simple delivery rule.</span></span>

## <span data-ttu-id="fddbd-113">변수</span><span class="sxs-lookup"><span data-stu-id="fddbd-113">PARAMETERS</span></span>

### <span data-ttu-id="fddbd-114">-작업</span><span class="sxs-lookup"><span data-stu-id="fddbd-114">-Action</span></span>
<span data-ttu-id="fddbd-115">수행할 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="fddbd-115">Action to perform.</span></span>

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

### <span data-ttu-id="fddbd-116">-CacheBehavior</span><span class="sxs-lookup"><span data-stu-id="fddbd-116">-CacheBehavior</span></span>
<span data-ttu-id="fddbd-117">작업에 대 한 캐싱 동작</span><span class="sxs-lookup"><span data-stu-id="fddbd-117">Caching behavior for the action</span></span>

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

### <span data-ttu-id="fddbd-118">-CacheDuration</span><span class="sxs-lookup"><span data-stu-id="fddbd-118">-CacheDuration</span></span>
<span data-ttu-id="fddbd-119">콘텐츠를 캐시 해야 하는 기간입니다.</span><span class="sxs-lookup"><span data-stu-id="fddbd-119">The duration for which the content needs to be cached.</span></span>
<span data-ttu-id="fddbd-120">허용 되는 형식은 \[ d입니다. \] hh: mm: ss</span><span class="sxs-lookup"><span data-stu-id="fddbd-120">Allowed format is \[d.\]hh:mm:ss</span></span>

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

### <span data-ttu-id="fddbd-121">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="fddbd-121">-CustomFragment</span></span>
<span data-ttu-id="fddbd-122">리디렉션 URL에 추가할 조각입니다.</span><span class="sxs-lookup"><span data-stu-id="fddbd-122">Fragment to add to the redirect URL.</span></span>
<span data-ttu-id="fddbd-123">단편은 # 다음에 오는 URL의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="fddbd-123">Fragment is the part of the URL that comes after #.</span></span>
<span data-ttu-id="fddbd-124"># .를 포함 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="fddbd-124">Do not include the #.</span></span>

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

### <span data-ttu-id="fddbd-125">-CustomHostname</span><span class="sxs-lookup"><span data-stu-id="fddbd-125">-CustomHostname</span></span>
<span data-ttu-id="fddbd-126">리디렉션할 호스트입니다.</span><span class="sxs-lookup"><span data-stu-id="fddbd-126">Host to redirect.</span></span>
<span data-ttu-id="fddbd-127">들어오는 호스트를 대상 호스트로 사용 하려면 비워 두세요.</span><span class="sxs-lookup"><span data-stu-id="fddbd-127">Leave empty to use the incoming host as the destination host.</span></span>

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

### <span data-ttu-id="fddbd-128">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="fddbd-128">-CustomPath</span></span>
<span data-ttu-id="fddbd-129">리디렉션할 전체 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="fddbd-129">The full path to redirect.</span></span>
<span data-ttu-id="fddbd-130">경로는 비워 둘 수 없으며/로 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fddbd-130">Path cannot be empty and must start with /.</span></span>
<span data-ttu-id="fddbd-131">들어오는 경로를 대상 경로로 사용 하려면 비워 두세요.</span><span class="sxs-lookup"><span data-stu-id="fddbd-131">Leave empty to use the incoming path as destination path.</span></span>

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

### <span data-ttu-id="fddbd-132">-CustomQueryString 쿼리</span><span class="sxs-lookup"><span data-stu-id="fddbd-132">-CustomQueryString</span></span>
<span data-ttu-id="fddbd-133">리디렉션 URL에 배치할 쿼리 문자열 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="fddbd-133">The set of query strings to be placed in the redirect URL.</span></span>
<span data-ttu-id="fddbd-134">이 값을 설정 하면 기존 쿼리 문자열이 바뀝니다. 수신 쿼리 문자열을 보존 하려면 비워 둡니다.</span><span class="sxs-lookup"><span data-stu-id="fddbd-134">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span>
<span data-ttu-id="fddbd-135">쿼리 문자열은 \< 키 \> = \< 값 \> 형식 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fddbd-135">Query string must be in \<key\>=\<value\> format.</span></span>
<span data-ttu-id="fddbd-136">?</span><span class="sxs-lookup"><span data-stu-id="fddbd-136">?</span></span> <span data-ttu-id="fddbd-137">및 &는 자동으로 추가 되므로이를 포함 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fddbd-137">and & will be added automatically so do not include them.</span></span>

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

### <span data-ttu-id="fddbd-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fddbd-138">-DefaultProfile</span></span>
<span data-ttu-id="fddbd-139">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fddbd-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fddbd-140">-DestinationProtocol</span><span class="sxs-lookup"><span data-stu-id="fddbd-140">-DestinationProtocol</span></span>
<span data-ttu-id="fddbd-141">리디렉션에 사용할 프로토콜입니다.</span><span class="sxs-lookup"><span data-stu-id="fddbd-141">Protocol to use for the redirect.</span></span>
<span data-ttu-id="fddbd-142">기본 값은 MatchRequest입니다.</span><span class="sxs-lookup"><span data-stu-id="fddbd-142">The default value is MatchRequest.</span></span>

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

### <span data-ttu-id="fddbd-143">-HeaderActionType</span><span class="sxs-lookup"><span data-stu-id="fddbd-143">-HeaderActionType</span></span>
<span data-ttu-id="fddbd-144">요청 헤더 또는 응답 헤더를 수정할지 여부</span><span class="sxs-lookup"><span data-stu-id="fddbd-144">Whether to modify request header or response header</span></span>

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

### <span data-ttu-id="fddbd-145">-인원 Ername</span><span class="sxs-lookup"><span data-stu-id="fddbd-145">-HeaderName</span></span>
<span data-ttu-id="fddbd-146">수정할 머리글의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fddbd-146">Name of the header to modify.</span></span>

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

### <span data-ttu-id="fddbd-147">RedirectType</span><span class="sxs-lookup"><span data-stu-id="fddbd-147">-RedirectType</span></span>
<span data-ttu-id="fddbd-148">트래픽 리디렉션을 위해 규칙이 사용 하는 리디렉션 유형</span><span class="sxs-lookup"><span data-stu-id="fddbd-148">The redirect type the rule will use when redirecting traffic</span></span>

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

### <span data-ttu-id="fddbd-149">-값</span><span class="sxs-lookup"><span data-stu-id="fddbd-149">-Value</span></span>
<span data-ttu-id="fddbd-150">지정 된 작업에 대 한 값입니다.</span><span class="sxs-lookup"><span data-stu-id="fddbd-150">Value for the specified action.</span></span>

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

### <span data-ttu-id="fddbd-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fddbd-151">CommonParameters</span></span>
<span data-ttu-id="fddbd-152">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fddbd-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fddbd-153">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fddbd-153">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fddbd-154">입력</span><span class="sxs-lookup"><span data-stu-id="fddbd-154">INPUTS</span></span>

### <span data-ttu-id="fddbd-155">않아야</span><span class="sxs-lookup"><span data-stu-id="fddbd-155">None</span></span>

## <span data-ttu-id="fddbd-156">출력</span><span class="sxs-lookup"><span data-stu-id="fddbd-156">OUTPUTS</span></span>

### <span data-ttu-id="fddbd-157">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction</span><span class="sxs-lookup"><span data-stu-id="fddbd-157">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction</span></span>

## <span data-ttu-id="fddbd-158">상속자</span><span class="sxs-lookup"><span data-stu-id="fddbd-158">NOTES</span></span>

## <span data-ttu-id="fddbd-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fddbd-159">RELATED LINKS</span></span>
