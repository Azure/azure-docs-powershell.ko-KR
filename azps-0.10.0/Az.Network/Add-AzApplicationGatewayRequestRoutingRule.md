---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BBA600C2-4813-4C12-8447-E770A949DA32
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 32695204a153d04643063f4d991b577e619edcea
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875689"
---
# <span data-ttu-id="35f06-101">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="35f06-101">Add-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="35f06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35f06-102">SYNOPSIS</span></span>
<span data-ttu-id="35f06-103">응용 프로그램 게이트웨이에 요청 라우팅 규칙을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="35f06-103">Adds a request routing rule to an application gateway.</span></span>

## <span data-ttu-id="35f06-104">구문과</span><span class="sxs-lookup"><span data-stu-id="35f06-104">SYNTAX</span></span>

### <span data-ttu-id="35f06-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="35f06-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35f06-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="35f06-106">SetByResource</span></span>
```
Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35f06-107">설명은</span><span class="sxs-lookup"><span data-stu-id="35f06-107">DESCRIPTION</span></span>
<span data-ttu-id="35f06-108">**Add-AzApplicationGatewayRequestRoutingRule** cmdlet은 응용 프로그램 게이트웨이에 요청 라우팅 규칙을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="35f06-108">The **Add-AzApplicationGatewayRequestRoutingRule** cmdlet adds a request routing rule to an application gateway.</span></span>

## <span data-ttu-id="35f06-109">예제의</span><span class="sxs-lookup"><span data-stu-id="35f06-109">EXAMPLES</span></span>

### <span data-ttu-id="35f06-110">예제 1: 응용 프로그램 게이트웨이에 요청 라우팅 규칙 추가</span><span class="sxs-lookup"><span data-stu-id="35f06-110">Example 1: Add a request routing rule to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzureApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="35f06-111">첫 번째 명령은 응용 프로그램 게이트웨이를 가져와 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="35f06-111">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="35f06-112">두 번째 명령은 응용 프로그램 게이트웨이에 요청 라우팅 규칙을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="35f06-112">The second command adds the request routing rule to the application gateway.</span></span>

## <span data-ttu-id="35f06-113">변수</span><span class="sxs-lookup"><span data-stu-id="35f06-113">PARAMETERS</span></span>

### <span data-ttu-id="35f06-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="35f06-114">-ApplicationGateway</span></span>
<span data-ttu-id="35f06-115">이 cmdlet이 요청 라우팅 규칙을 추가 하는 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35f06-115">Specifies an application gateway to which this cmdlet adds a request routing rule.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35f06-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="35f06-116">-BackendAddressPool</span></span>
<span data-ttu-id="35f06-117">응용 프로그램 게이트웨이 백 엔드 주소 풀 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35f06-117">Specifies an application gateway back-end address pool object.</span></span>

```yaml
Type: PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35f06-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="35f06-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="35f06-119">응용 프로그램 게이트웨이 백 엔드 주소 풀 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35f06-119">Specifies an application gateway back-end address pool ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35f06-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="35f06-120">-BackendHttpSettings</span></span>
<span data-ttu-id="35f06-121">응용 프로그램 게이트웨이에 대 한 백 엔드 HTTP 설정 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35f06-121">Specifies a back-end HTTP settings object for an application gateway.</span></span>

```yaml
Type: PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35f06-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="35f06-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="35f06-123">응용 프로그램 게이트웨이에 대 한 백 엔드 HTTP 설정 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35f06-123">Specifies a backend HTTP settings ID for an application gateway.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35f06-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35f06-124">-DefaultProfile</span></span>
<span data-ttu-id="35f06-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="35f06-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35f06-126">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="35f06-126">-HttpListener</span></span>
<span data-ttu-id="35f06-127">Application gateway HTTP 수신기 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35f06-127">Specifies application gateway HTTP listener object.</span></span>

```yaml
Type: PSApplicationGatewayHttpListener
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35f06-128">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="35f06-128">-HttpListenerId</span></span>
<span data-ttu-id="35f06-129">Application gateway HTTP 수신기 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35f06-129">Specifies application gateway HTTP listener ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35f06-130">-이름</span><span class="sxs-lookup"><span data-stu-id="35f06-130">-Name</span></span>
<span data-ttu-id="35f06-131">이 cmdlet에 추가 되는 요청 라우팅 규칙의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35f06-131">Specifies the name of request routing rule this cmdlet adds.</span></span>

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

### <span data-ttu-id="35f06-132">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="35f06-132">-RedirectConfiguration</span></span>
<span data-ttu-id="35f06-133">Application gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="35f06-133">Application gateway RedirectConfiguration</span></span>

```yaml
Type: PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35f06-134">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="35f06-134">-RedirectConfigurationId</span></span>
<span data-ttu-id="35f06-135">응용 프로그램 게이트웨이 RedirectConfiguration의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="35f06-135">ID of the application gateway RedirectConfiguration</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35f06-136">-RuleType</span><span class="sxs-lookup"><span data-stu-id="35f06-136">-RuleType</span></span>
<span data-ttu-id="35f06-137">요청 라우팅 규칙 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35f06-137">Specifies the type of request routing rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, PathBasedRouting

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35f06-138">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="35f06-138">-UrlPathMap</span></span>
```yaml
Type: PSApplicationGatewayUrlPathMap
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35f06-139">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="35f06-139">-UrlPathMapId</span></span>
<span data-ttu-id="35f06-140">라우팅 규칙에 대 한 URL 경로 맵 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35f06-140">Specifies the URL path map ID for the routing rule.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35f06-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35f06-141">CommonParameters</span></span>
<span data-ttu-id="35f06-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="35f06-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35f06-143">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35f06-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35f06-144">입력</span><span class="sxs-lookup"><span data-stu-id="35f06-144">INPUTS</span></span>

### <span data-ttu-id="35f06-145">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="35f06-145">System.String</span></span>

## <span data-ttu-id="35f06-146">출력</span><span class="sxs-lookup"><span data-stu-id="35f06-146">OUTPUTS</span></span>

### <span data-ttu-id="35f06-147">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="35f06-147">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="35f06-148">상속자</span><span class="sxs-lookup"><span data-stu-id="35f06-148">NOTES</span></span>

## <span data-ttu-id="35f06-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="35f06-149">RELATED LINKS</span></span>

[<span data-ttu-id="35f06-150">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="35f06-150">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="35f06-151">새로운 AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="35f06-151">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="35f06-152">제거-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="35f06-152">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="35f06-153">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="35f06-153">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


