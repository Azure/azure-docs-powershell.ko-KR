---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 622FE9AC-1CC4-489C-BB17-9D6B9D1C151D
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 53963e7672881255cf23df99e53a1471c3c42250
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010331"
---
# <span data-ttu-id="71762-101">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="71762-101">New-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="71762-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71762-102">SYNOPSIS</span></span>
<span data-ttu-id="71762-103">애플리케이션 게이트웨이에 대한 요청 라우팅 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="71762-103">Creates a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="71762-104">구문</span><span class="sxs-lookup"><span data-stu-id="71762-104">SYNTAX</span></span>

### <span data-ttu-id="71762-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="71762-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String> [-Priority <Int32>]
 [-BackendHttpSettingsId <String>] [-HttpListenerId <String>] [-BackendAddressPoolId <String>]
 [-UrlPathMapId <String>] [-RewriteRuleSetId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71762-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="71762-106">SetByResource</span></span>
```
New-AzApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String> [-Priority <Int32>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71762-107">설명</span><span class="sxs-lookup"><span data-stu-id="71762-107">DESCRIPTION</span></span>
<span data-ttu-id="71762-108">**Add-AzApplicationGatewayRequestRoutingRule** cmdlet은 Azure 애플리케이션 게이트웨이에 대한 요청 라우팅 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="71762-108">**The Add-AzApplicationGatewayRequestRoutingRule** cmdlet creates a request routing rule for an Azure application gateway.</span></span>

## <span data-ttu-id="71762-109">예제</span><span class="sxs-lookup"><span data-stu-id="71762-109">EXAMPLES</span></span>

### <span data-ttu-id="71762-110">예제 1: 애플리케이션 게이트웨이에 대한 요청 라우팅 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="71762-110">Example 1: Create a request routing rule for an application gateway</span></span>
```
PS C:\>$Rule = New-AzApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType Basic -Priority 100 -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="71762-111">이 명령은 Rule01이라는 기본 요청 라우팅 규칙을 만들고 결과를 $Rule.</span><span class="sxs-lookup"><span data-stu-id="71762-111">This command creates a basic request routing rule named Rule01 and stores the result in the variable named $Rule.</span></span>

## <span data-ttu-id="71762-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="71762-112">PARAMETERS</span></span>

### <span data-ttu-id="71762-113">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="71762-113">-BackendAddressPool</span></span>
<span data-ttu-id="71762-114">요청 라우팅 규칙을 만들 수 있는 백 엔드 주소 풀을 개체로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="71762-114">Specifies the back-end address pool, as an object, for the request routing rule to create.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71762-115">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="71762-115">-BackendAddressPoolId</span></span>
<span data-ttu-id="71762-116">만들 요청 라우팅 규칙의 백 엔드 주소 풀 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="71762-116">Specifies the back-end address pool ID of the request routing rule to create.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71762-117">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="71762-117">-BackendHttpSettings</span></span>
<span data-ttu-id="71762-118">요청 라우팅 규칙을 만들 수 있는 백 엔드 HTTP 설정을 개체로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="71762-118">Specifies the back-end HTTP settings, as an object, for the request routing rule to create.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71762-119">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="71762-119">-BackendHttpSettingsId</span></span>
<span data-ttu-id="71762-120">만들 요청 라우팅 규칙의 백 엔드 HTTP 설정 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="71762-120">Specifies the back-end HTTP settings ID of the request routing rule to create.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71762-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71762-121">-DefaultProfile</span></span>
<span data-ttu-id="71762-122">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="71762-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71762-123">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="71762-123">-HttpListener</span></span>
<span data-ttu-id="71762-124">만들 요청 라우팅 규칙에 대한 백 엔드 HTTP 수신기를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="71762-124">Specifies the back-end HTTP listener for the request routing rule to create.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71762-125">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="71762-125">-HttpListenerId</span></span>
<span data-ttu-id="71762-126">만들 요청 라우팅 규칙에 대한 백end HTTP 수신기 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="71762-126">Specifies the backend HTTP listener ID for the request routing rule to create.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71762-127">-Name</span><span class="sxs-lookup"><span data-stu-id="71762-127">-Name</span></span>
<span data-ttu-id="71762-128">이 cmdlet에서 만드는 요청 라우팅 규칙의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="71762-128">Specifies the name of the request routing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="71762-129">-Priority</span><span class="sxs-lookup"><span data-stu-id="71762-129">-Priority</span></span>
<span data-ttu-id="71762-130">규칙의 우선 순위</span><span class="sxs-lookup"><span data-stu-id="71762-130">The priority of the rule</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:
Accepted Values: 1-20000

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71762-131">-리디렉션 구성</span><span class="sxs-lookup"><span data-stu-id="71762-131">-RedirectConfiguration</span></span>
<span data-ttu-id="71762-132">애플리케이션 게이트웨이 리디렉션 구성</span><span class="sxs-lookup"><span data-stu-id="71762-132">Application gateway RedirectConfiguration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71762-133">-리디렉션ConfigurationId</span><span class="sxs-lookup"><span data-stu-id="71762-133">-RedirectConfigurationId</span></span>
<span data-ttu-id="71762-134">애플리케이션 게이트웨이 리디렉션 구성의 ID</span><span class="sxs-lookup"><span data-stu-id="71762-134">ID of the application gateway RedirectConfiguration</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71762-135">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="71762-135">-RewriteRuleSet</span></span>
<span data-ttu-id="71762-136">Application gateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="71762-136">Application gateway RewriteRuleSet</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71762-137">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="71762-137">-RewriteRuleSetId</span></span>
<span data-ttu-id="71762-138">애플리케이션 게이트웨이 RewriteRuleSet의 ID</span><span class="sxs-lookup"><span data-stu-id="71762-138">ID of the application gateway RewriteRuleSet</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71762-139">-RuleType</span><span class="sxs-lookup"><span data-stu-id="71762-139">-RuleType</span></span>
<span data-ttu-id="71762-140">요청 라우팅 규칙의 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="71762-140">Specifies type of the request routing rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, PathBasedRouting

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71762-141">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="71762-141">-UrlPathMap</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71762-142">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="71762-142">-UrlPathMapId</span></span>
```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71762-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71762-143">CommonParameters</span></span>
<span data-ttu-id="71762-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="71762-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71762-145">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="71762-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71762-146">입력</span><span class="sxs-lookup"><span data-stu-id="71762-146">INPUTS</span></span>

### <span data-ttu-id="71762-147">없음</span><span class="sxs-lookup"><span data-stu-id="71762-147">None</span></span>

## <span data-ttu-id="71762-148">출력</span><span class="sxs-lookup"><span data-stu-id="71762-148">OUTPUTS</span></span>

### <span data-ttu-id="71762-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="71762-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="71762-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="71762-150">NOTES</span></span>

## <span data-ttu-id="71762-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="71762-151">RELATED LINKS</span></span>

[<span data-ttu-id="71762-152">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="71762-152">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="71762-153">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="71762-153">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="71762-154">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="71762-154">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="71762-155">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="71762-155">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


