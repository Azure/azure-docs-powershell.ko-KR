---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 75A4826A-7A5F-4742-9DC4-DC728CED63D0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayrequestroutingrule
schema: 2.0.0
ms.openlocfilehash: e3b52040090ace745f58e8c3dd56ac59bb5d9b73
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881325"
---
# <span data-ttu-id="8e94f-101">Set-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="8e94f-101">Set-AzureRmApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="8e94f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e94f-102">SYNOPSIS</span></span>
<span data-ttu-id="8e94f-103">Application gateway에 대 한 요청 라우팅 규칙을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e94f-103">Modifies a request routing rule for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e94f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8e94f-104">SYNTAX</span></span>

### <span data-ttu-id="8e94f-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="8e94f-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e94f-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="8e94f-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e94f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="8e94f-107">DESCRIPTION</span></span>
<span data-ttu-id="8e94f-108">**Set-AzureRmApplicationGatewayRequestRoutingRule** cmdlet은 요청 라우팅 규칙을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e94f-108">The **Set-AzureRmApplicationGatewayRequestRoutingRule** cmdlet modifies a request routing rule.</span></span>

## <span data-ttu-id="8e94f-109">예제의</span><span class="sxs-lookup"><span data-stu-id="8e94f-109">EXAMPLES</span></span>

### <span data-ttu-id="8e94f-110">예제 1: 요청 라우팅 규칙 업데이트</span><span class="sxs-lookup"><span data-stu-id="8e94f-110">Example 1: Update a request routing rule</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="8e94f-111">첫 번째 명령은 ApplicationGateway01 이라는 응용 프로그램 게이트웨이를 가져와이를 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e94f-111">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="8e94f-112">두 번째 명령은 $Setting 변수에 지정 된 백 엔드 HTTP 설정, $Listener 변수에 지정 된 HTTP 수신기 및 $Pool 변수에 지정 된 백 엔드 주소 풀을 사용 하도록 응용 프로그램 게이트웨이에 대 한 요청 라우팅 규칙을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e94f-112">The second command modifies the request routing rule for the application gateway to use back-end HTTP settings specified in the $Setting variable, an HTTP listener specified in the $Listener variable, and a back-end address pool specified in the $Pool variable.</span></span>

## <span data-ttu-id="8e94f-113">변수</span><span class="sxs-lookup"><span data-stu-id="8e94f-113">PARAMETERS</span></span>

### <span data-ttu-id="8e94f-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8e94f-114">-ApplicationGateway</span></span>
<span data-ttu-id="8e94f-115">이 cmdlet이 요청 라우팅 규칙을 연결 하는 응용 프로그램 게이트웨이 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e94f-115">Specifies the application gateway object with which this cmdlet associates a request routing rule.</span></span>

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

### <span data-ttu-id="8e94f-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="8e94f-116">-BackendAddressPool</span></span>
<span data-ttu-id="8e94f-117">응용 프로그램 게이트웨이 백 엔드 주소 풀을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e94f-117">Specifies the application gateway back-end address pool.</span></span>

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

### <span data-ttu-id="8e94f-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="8e94f-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="8e94f-119">응용 프로그램 게이트웨이 백 엔드 주소 풀 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e94f-119">Specifies the application gateway back-end address pool ID.</span></span>

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

### <span data-ttu-id="8e94f-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="8e94f-120">-BackendHttpSettings</span></span>
<span data-ttu-id="8e94f-121">응용 프로그램 게이트웨이 백 엔드 HTTP 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e94f-121">Specifies the application gateway backend HTTP settings.</span></span>

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

### <span data-ttu-id="8e94f-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="8e94f-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="8e94f-123">응용 프로그램 게이트웨이 백 엔드 HTTP 설정 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e94f-123">Specifies the application gateway back-end HTTP settings ID.</span></span>

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

### <span data-ttu-id="8e94f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e94f-124">-DefaultProfile</span></span>
<span data-ttu-id="8e94f-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8e94f-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e94f-126">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="8e94f-126">-HttpListener</span></span>
<span data-ttu-id="8e94f-127">응용 프로그램 게이트웨이 HTTP 수신기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e94f-127">Specifies the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="8e94f-128">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="8e94f-128">-HttpListenerId</span></span>
<span data-ttu-id="8e94f-129">응용 프로그램 게이트웨이 HTTP 수신기 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e94f-129">Specifies the application gateway HTTP listener ID.</span></span>

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

### <span data-ttu-id="8e94f-130">-이름</span><span class="sxs-lookup"><span data-stu-id="8e94f-130">-Name</span></span>
<span data-ttu-id="8e94f-131">이 cmdlet이 수정 하는 요청 라우팅 규칙의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e94f-131">Specifies the name of the request routing rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="8e94f-132">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="8e94f-132">-RedirectConfiguration</span></span>
<span data-ttu-id="8e94f-133">Application gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="8e94f-133">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="8e94f-134">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="8e94f-134">-RedirectConfigurationId</span></span>
<span data-ttu-id="8e94f-135">응용 프로그램 게이트웨이 RedirectConfiguration의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8e94f-135">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="8e94f-136">-RuleType</span><span class="sxs-lookup"><span data-stu-id="8e94f-136">-RuleType</span></span>
<span data-ttu-id="8e94f-137">요청 라우팅 규칙 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e94f-137">Specifies the type of request routing rule.</span></span>

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

### <span data-ttu-id="8e94f-138">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="8e94f-138">-UrlPathMap</span></span>
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

### <span data-ttu-id="8e94f-139">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="8e94f-139">-UrlPathMapId</span></span>
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

### <span data-ttu-id="8e94f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e94f-140">CommonParameters</span></span>
<span data-ttu-id="8e94f-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e94f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e94f-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e94f-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e94f-143">입력</span><span class="sxs-lookup"><span data-stu-id="8e94f-143">INPUTS</span></span>

### <span data-ttu-id="8e94f-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8e94f-144">System.String</span></span>

## <span data-ttu-id="8e94f-145">출력</span><span class="sxs-lookup"><span data-stu-id="8e94f-145">OUTPUTS</span></span>

### <span data-ttu-id="8e94f-146">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8e94f-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8e94f-147">상속자</span><span class="sxs-lookup"><span data-stu-id="8e94f-147">NOTES</span></span>

## <span data-ttu-id="8e94f-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8e94f-148">RELATED LINKS</span></span>

[<span data-ttu-id="8e94f-149">추가-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="8e94f-149">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Add-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="8e94f-150">Get-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="8e94f-150">Get-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Get-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="8e94f-151">새로운 AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="8e94f-151">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="8e94f-152">제거-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="8e94f-152">Remove-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzureRmApplicationGatewayRequestRoutingRule.md)


