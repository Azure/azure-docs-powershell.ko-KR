---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9F5EC8E7-12E9-40E5-B98D-AAFD8F9F3C37
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: d384d1b0db463253052ab7efa53233bdd302f496
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871094"
---
# <span data-ttu-id="36e6d-101">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="36e6d-101">Set-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="36e6d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36e6d-102">SYNOPSIS</span></span>
<span data-ttu-id="36e6d-103">백 엔드 서버 풀에 대 한 URL 경로 매핑 배열의 구성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="36e6d-103">Sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="36e6d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="36e6d-104">SYNTAX</span></span>

### <span data-ttu-id="36e6d-105">BackendSetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="36e6d-105">BackendSetByResource (Default)</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>
 -DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="36e6d-106">BackendSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="36e6d-106">BackendSetByResourceId</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> -DefaultBackendAddressPoolId <String>
 -DefaultBackendHttpSettingsId <String> [-DefaultRewriteRuleSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36e6d-107">RedirectSetByResource</span><span class="sxs-lookup"><span data-stu-id="36e6d-107">RedirectSetByResource</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 -DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36e6d-108">RedirectSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="36e6d-108">RedirectSetByResourceId</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSetId <String>]
 -DefaultRedirectConfigurationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36e6d-109">설명은</span><span class="sxs-lookup"><span data-stu-id="36e6d-109">DESCRIPTION</span></span>
<span data-ttu-id="36e6d-110">**AzApplicationGatewayUrlPathMapConfig** cmdlet은 백 엔드 서버 풀에 대 한 URL 경로 매핑 배열의 구성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="36e6d-110">The **Set-AzApplicationGatewayUrlPathMapConfig** cmdlet sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="36e6d-111">예제의</span><span class="sxs-lookup"><span data-stu-id="36e6d-111">EXAMPLES</span></span>

### <span data-ttu-id="36e6d-112">예제 1: URL 경로 매핑 업데이트</span><span class="sxs-lookup"><span data-stu-id="36e6d-112">Example 1: Update an URL path mapping</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $appgw -Name "map01"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="36e6d-113">첫 번째 명령은 appGwName 이라는 응용 프로그램 게이트웨이를 가져와 결과를 $appgw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="36e6d-113">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="36e6d-114">두 번째 명령은 응용 프로그램 게이트웨이에서 map01 이라는 URL 경로 매핑을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="36e6d-114">The second command updates the URL path mapping named map01 in the application gateway.</span></span>
<span data-ttu-id="36e6d-115">세 번째 명령은 응용 프로그램 게이트웨이를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="36e6d-115">The third command updates the application gateway.</span></span>

## <span data-ttu-id="36e6d-116">변수</span><span class="sxs-lookup"><span data-stu-id="36e6d-116">PARAMETERS</span></span>

### <span data-ttu-id="36e6d-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="36e6d-117">-ApplicationGateway</span></span>
<span data-ttu-id="36e6d-118">이 cmdlet이 URL 경로 맵 구성을 설정 하는 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="36e6d-118">Specifies the application gateway to which this cmdlet sets a URL path map configuration.</span></span>

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

### <span data-ttu-id="36e6d-119">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="36e6d-119">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="36e6d-120">*Pathrules* 매개 변수 일치에 지정 된 규칙이 없는 경우 라우팅할 기본 백 엔드 주소 풀을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="36e6d-120">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="36e6d-121">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="36e6d-121">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="36e6d-122">기본 백 엔드 주소 풀 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="36e6d-122">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="36e6d-123">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="36e6d-123">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="36e6d-124">*Pathrules* 매개 변수 일치에 지정 된 규칙이 없는 경우 사용할 기본 백 엔드 HTTP 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="36e6d-124">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="36e6d-125">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="36e6d-125">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="36e6d-126">기본 백 엔드 HTTP 설정 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="36e6d-126">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="36e6d-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36e6d-127">-DefaultProfile</span></span>
<span data-ttu-id="36e6d-128">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="36e6d-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36e6d-129">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="36e6d-129">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="36e6d-130">Application gateway 기본 RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="36e6d-130">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="36e6d-131">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="36e6d-131">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="36e6d-132">응용 프로그램 게이트웨이 기본 RedirectConfiguration의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="36e6d-132">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="36e6d-133">-DefaultRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="36e6d-133">-DefaultRewriteRuleSet</span></span>
<span data-ttu-id="36e6d-134">Application gateway 기본 재작성 규칙 집합</span><span class="sxs-lookup"><span data-stu-id="36e6d-134">Application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="36e6d-135">-DefaultRewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="36e6d-135">-DefaultRewriteRuleSetId</span></span>
<span data-ttu-id="36e6d-136">응용 프로그램 게이트웨이 기본 재작성 규칙 집합의 ID</span><span class="sxs-lookup"><span data-stu-id="36e6d-136">ID of the application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="36e6d-137">-이름</span><span class="sxs-lookup"><span data-stu-id="36e6d-137">-Name</span></span>
<span data-ttu-id="36e6d-138">이 cmdlet이 구성을 설정 하는 URL 경로 맵 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="36e6d-138">Specifies the URL path map name in which this cmdlet sets configuration for.</span></span>

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

### <span data-ttu-id="36e6d-139">-PathRules</span><span class="sxs-lookup"><span data-stu-id="36e6d-139">-PathRules</span></span>
<span data-ttu-id="36e6d-140">경로 규칙의 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="36e6d-140">Specifies a list of path rules.</span></span>
<span data-ttu-id="36e6d-141">경로 규칙은 주문에 따라 구분 되며 지정 된 순서 대로 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="36e6d-141">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="36e6d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36e6d-142">CommonParameters</span></span>
<span data-ttu-id="36e6d-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="36e6d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36e6d-144">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36e6d-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36e6d-145">입력</span><span class="sxs-lookup"><span data-stu-id="36e6d-145">INPUTS</span></span>

### <span data-ttu-id="36e6d-146">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="36e6d-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="36e6d-147">출력</span><span class="sxs-lookup"><span data-stu-id="36e6d-147">OUTPUTS</span></span>

### <span data-ttu-id="36e6d-148">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="36e6d-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="36e6d-149">상속자</span><span class="sxs-lookup"><span data-stu-id="36e6d-149">NOTES</span></span>

## <span data-ttu-id="36e6d-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="36e6d-150">RELATED LINKS</span></span>

[<span data-ttu-id="36e6d-151">추가-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="36e6d-151">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="36e6d-152">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="36e6d-152">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="36e6d-153">새로운 AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="36e6d-153">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="36e6d-154">제거-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="36e6d-154">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)


