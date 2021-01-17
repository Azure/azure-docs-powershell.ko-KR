---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9F5EC8E7-12E9-40E5-B98D-AAFD8F9F3C37
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: ec2eede30b6aef81210582b95b775200c8145943
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98371309"
---
# <span data-ttu-id="cbe4e-101">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="cbe4e-101">Set-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="cbe4e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cbe4e-102">SYNOPSIS</span></span>
<span data-ttu-id="cbe4e-103">백end 서버 풀에 대한 URL 경로 매핑 배열에 대한 구성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-103">Sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="cbe4e-104">구문</span><span class="sxs-lookup"><span data-stu-id="cbe4e-104">SYNTAX</span></span>

### <span data-ttu-id="cbe4e-105">BackendSetByResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="cbe4e-105">BackendSetByResource (Default)</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>
 -DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cbe4e-106">BackendSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="cbe4e-106">BackendSetByResourceId</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> -DefaultBackendAddressPoolId <String>
 -DefaultBackendHttpSettingsId <String> [-DefaultRewriteRuleSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cbe4e-107">RedirectSetByResource</span><span class="sxs-lookup"><span data-stu-id="cbe4e-107">RedirectSetByResource</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 -DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cbe4e-108">RedirectSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="cbe4e-108">RedirectSetByResourceId</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSetId <String>]
 -DefaultRedirectConfigurationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cbe4e-109">설명</span><span class="sxs-lookup"><span data-stu-id="cbe4e-109">DESCRIPTION</span></span>
<span data-ttu-id="cbe4e-110">**Set-AzApplicationGatewayUrlPathMapConfig** cmdlet은 백end 서버 풀에 대한 URL 경로 매핑 배열에 대한 구성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-110">The **Set-AzApplicationGatewayUrlPathMapConfig** cmdlet sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="cbe4e-111">예제</span><span class="sxs-lookup"><span data-stu-id="cbe4e-111">EXAMPLES</span></span>

### <span data-ttu-id="cbe4e-112">예제 1: URL 경로 매핑 업데이트</span><span class="sxs-lookup"><span data-stu-id="cbe4e-112">Example 1: Update an URL path mapping</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $appgw -Name "map01"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="cbe4e-113">첫 번째 명령은 appGwName이라는 애플리케이션 게이트웨이를 다운로드하고 결과를 $appgw 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-113">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="cbe4e-114">두 번째 명령은 애플리케이션 게이트웨이에서 map01이라는 URL 경로 매핑을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-114">The second command updates the URL path mapping named map01 in the application gateway.</span></span>
<span data-ttu-id="cbe4e-115">세 번째 명령은 애플리케이션 게이트웨이를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-115">The third command updates the application gateway.</span></span>

## <span data-ttu-id="cbe4e-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cbe4e-116">PARAMETERS</span></span>

### <span data-ttu-id="cbe4e-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cbe4e-117">-ApplicationGateway</span></span>
<span data-ttu-id="cbe4e-118">이 cmdlet이 URL 경로 맵 구성을 설정하는 애플리케이션 게이트웨이를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-118">Specifies the application gateway to which this cmdlet sets a URL path map configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cbe4e-119">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="cbe4e-119">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="cbe4e-120">*pathRules* 매개 변수에 지정된 규칙이 일치하지 않는 경우 라우팅할 기본 백end 주소 풀을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-120">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool
Parameter Sets: BackendSetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbe4e-121">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="cbe4e-121">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="cbe4e-122">기본 백end 주소 풀 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-122">Specifies the default backend address pool ID.</span></span>

```yaml
Type: System.String
Parameter Sets: BackendSetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbe4e-123">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="cbe4e-123">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="cbe4e-124">*pathRules* 매개 변수에 지정된 규칙이 일치하지 않는 경우 사용할 기본 백end HTTP 설정을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-124">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: BackendSetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbe4e-125">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="cbe4e-125">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="cbe4e-126">기본 백end HTTP 설정 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-126">Specifies the default backend HTTP settings ID.</span></span>

```yaml
Type: System.String
Parameter Sets: BackendSetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbe4e-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbe4e-127">-DefaultProfile</span></span>
<span data-ttu-id="cbe4e-128">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cbe4e-129">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="cbe4e-129">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="cbe4e-130">Application Gateway 기본 RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="cbe4e-130">Application gateway default RedirectConfiguration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration
Parameter Sets: RedirectSetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbe4e-131">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="cbe4e-131">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="cbe4e-132">Application Gateway 기본 RedirectConfiguration의 ID</span><span class="sxs-lookup"><span data-stu-id="cbe4e-132">ID of the application gateway default RedirectConfiguration</span></span>

```yaml
Type: System.String
Parameter Sets: RedirectSetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbe4e-133">-DefaultRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cbe4e-133">-DefaultRewriteRuleSet</span></span>
<span data-ttu-id="cbe4e-134">Application Gateway 기본 다시 필기 규칙 집합</span><span class="sxs-lookup"><span data-stu-id="cbe4e-134">Application gateway default rewrite rule set</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet
Parameter Sets: BackendSetByResource, RedirectSetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbe4e-135">-DefaultRewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="cbe4e-135">-DefaultRewriteRuleSetId</span></span>
<span data-ttu-id="cbe4e-136">애플리케이션 게이트웨이 기본 다시 덮기 규칙 집합의 ID</span><span class="sxs-lookup"><span data-stu-id="cbe4e-136">ID of the application gateway default rewrite rule set</span></span>

```yaml
Type: System.String
Parameter Sets: BackendSetByResourceId, RedirectSetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbe4e-137">-Name</span><span class="sxs-lookup"><span data-stu-id="cbe4e-137">-Name</span></span>
<span data-ttu-id="cbe4e-138">이 cmdlet이 구성을 설정하는 URL 경로 맵 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-138">Specifies the URL path map name in which this cmdlet sets configuration for.</span></span>

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

### <span data-ttu-id="cbe4e-139">-PathRules</span><span class="sxs-lookup"><span data-stu-id="cbe4e-139">-PathRules</span></span>
<span data-ttu-id="cbe4e-140">경로 규칙 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-140">Specifies a list of path rules.</span></span>
<span data-ttu-id="cbe4e-141">경로 규칙은 순서에 민감하고 지정된 순서대로 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-141">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbe4e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbe4e-142">CommonParameters</span></span>
<span data-ttu-id="cbe4e-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbe4e-144">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbe4e-145">입력</span><span class="sxs-lookup"><span data-stu-id="cbe4e-145">INPUTS</span></span>

### <span data-ttu-id="cbe4e-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cbe4e-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="cbe4e-147">출력</span><span class="sxs-lookup"><span data-stu-id="cbe4e-147">OUTPUTS</span></span>

### <span data-ttu-id="cbe4e-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cbe4e-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="cbe4e-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cbe4e-149">NOTES</span></span>

## <span data-ttu-id="cbe4e-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cbe4e-150">RELATED LINKS</span></span>

[<span data-ttu-id="cbe4e-151">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="cbe4e-151">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="cbe4e-152">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="cbe4e-152">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="cbe4e-153">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="cbe4e-153">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="cbe4e-154">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="cbe4e-154">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)


