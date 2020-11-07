---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1E192553-61D8-4449-936B-68CF866C710C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 5648bb1cb7497517afb5ff461674294e426c0131
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870901"
---
# <span data-ttu-id="95d13-101">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="95d13-101">Add-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="95d13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95d13-102">SYNOPSIS</span></span>
<span data-ttu-id="95d13-103">응용 프로그램 게이트웨이에 HTTP 수신기를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="95d13-103">Adds an HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="95d13-104">구문과</span><span class="sxs-lookup"><span data-stu-id="95d13-104">SYNTAX</span></span>

### <span data-ttu-id="95d13-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="95d13-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="95d13-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="95d13-106">SetByResource</span></span>
```
Add-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="95d13-107">설명은</span><span class="sxs-lookup"><span data-stu-id="95d13-107">DESCRIPTION</span></span>
<span data-ttu-id="95d13-108">**Add-AzApplicationGatewayHttpListener** cmdlet은 응용 프로그램 게이트웨이에 HTTP 수신기를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="95d13-108">The **Add-AzApplicationGatewayHttpListener** cmdlet adds a HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="95d13-109">예제의</span><span class="sxs-lookup"><span data-stu-id="95d13-109">EXAMPLES</span></span>

### <span data-ttu-id="95d13-110">예제 1: HTTP 수신기 추가</span><span class="sxs-lookup"><span data-stu-id="95d13-110">Example 1: Add a HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "listener01" -Protocol "Http" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01
```

<span data-ttu-id="95d13-111">첫 번째 명령은 응용 프로그램 게이트웨이를 가져와 $AppGw 변수에 저장 합니다. 두 번째 명령은 HTTP 수신기를 응용 프로그램 게이트웨이에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="95d13-111">The first command gets the application gateway and stores it in the $AppGw variable.The second command adds the HTTP listener to the application gateway.</span></span>

### <span data-ttu-id="95d13-112">예제 2: SSL을 사용 하 여 HTTPS 수신기 추가</span><span class="sxs-lookup"><span data-stu-id="95d13-112">Example 2: Add a HTTPS listener with SSL</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="95d13-113">첫 번째 명령은 응용 프로그램 게이트웨이를 가져와 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="95d13-113">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="95d13-114">두 번째 명령은 HTTPS 프로토콜을 사용 하는 수신기를 응용 프로그램 게이트웨이에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="95d13-114">The second command adds the listener, which uses the HTTPS protocol, to the application gateway.</span></span>

## <span data-ttu-id="95d13-115">변수</span><span class="sxs-lookup"><span data-stu-id="95d13-115">PARAMETERS</span></span>

### <span data-ttu-id="95d13-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="95d13-116">-ApplicationGateway</span></span>
<span data-ttu-id="95d13-117">이 cmdlet이 HTTP 수신기를 추가 하는 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="95d13-117">Specifies the application gateway to which this cmdlet adds an HTTP listener.</span></span>

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

### <span data-ttu-id="95d13-118">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="95d13-118">-CustomErrorConfiguration</span></span>
<span data-ttu-id="95d13-119">Application gateway의 고객 오류</span><span class="sxs-lookup"><span data-stu-id="95d13-119">Customer error of an application gateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95d13-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95d13-120">-DefaultProfile</span></span>
<span data-ttu-id="95d13-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="95d13-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95d13-122">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="95d13-122">-FrontendIPConfiguration</span></span>
<span data-ttu-id="95d13-123">응용 프로그램 게이트웨이 프런트 엔드 IP 리소스 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="95d13-123">Specifies the application gateway front-end IP resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95d13-124">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="95d13-124">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="95d13-125">응용 프로그램 게이트웨이 프런트 엔드 IP ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="95d13-125">Specifies the application gateway front-end IP ID.</span></span>

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

### <span data-ttu-id="95d13-126">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="95d13-126">-FrontendPort</span></span>
<span data-ttu-id="95d13-127">응용 프로그램 게이트웨이 프런트 엔드 포트 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="95d13-127">Specifies the application gateway front-end port object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95d13-128">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="95d13-128">-FrontendPortId</span></span>
<span data-ttu-id="95d13-129">응용 프로그램 게이트웨이 프런트 엔드 포트 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="95d13-129">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="95d13-130">-HostName</span><span class="sxs-lookup"><span data-stu-id="95d13-130">-HostName</span></span>
<span data-ttu-id="95d13-131">이 cmdlet이 HTTP 수신기를 추가 하는 호스트 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="95d13-131">Specifies the host name that this cmdlet adds a HTTP listener to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95d13-132">-이름</span><span class="sxs-lookup"><span data-stu-id="95d13-132">-Name</span></span>
<span data-ttu-id="95d13-133">이 명령이 추가 하는 프런트 엔드 포트의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="95d13-133">Specifies the name of the front-end port that this command adds.</span></span>

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

### <span data-ttu-id="95d13-134">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="95d13-134">-Protocol</span></span>
<span data-ttu-id="95d13-135">HTTP 수신기의 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="95d13-135">Specifies the protocol of the HTTP listener.</span></span>
<span data-ttu-id="95d13-136">HTTP와 HTTPS 모두 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="95d13-136">Both HTTP and HTTPS are supported.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95d13-137">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="95d13-137">-RequireServerNameIndication</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: true, false

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95d13-138">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="95d13-138">-SslCertificate</span></span>
<span data-ttu-id="95d13-139">HTTP 수신기의 SSL 인증서를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="95d13-139">Specifies the SSL certificate of the HTTP listener.</span></span>
<span data-ttu-id="95d13-140">HTTPS가 수신기 프로토콜로 선택 된 경우에는 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="95d13-140">Must be specified if HTTPS is chosen as listener protocol.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95d13-141">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="95d13-141">-SslCertificateId</span></span>
<span data-ttu-id="95d13-142">HTTP 수신기의 SSL 인증서 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="95d13-142">Specifies the SSL certificate ID of the HTTP listener.</span></span>
<span data-ttu-id="95d13-143">HTTPS가 수신기 프로토콜로 선택 된 경우에는 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="95d13-143">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="95d13-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95d13-144">CommonParameters</span></span>
<span data-ttu-id="95d13-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="95d13-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95d13-146">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95d13-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95d13-147">입력</span><span class="sxs-lookup"><span data-stu-id="95d13-147">INPUTS</span></span>

### <span data-ttu-id="95d13-148">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="95d13-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="95d13-149">출력</span><span class="sxs-lookup"><span data-stu-id="95d13-149">OUTPUTS</span></span>

### <span data-ttu-id="95d13-150">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="95d13-150">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="95d13-151">상속자</span><span class="sxs-lookup"><span data-stu-id="95d13-151">NOTES</span></span>

## <span data-ttu-id="95d13-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="95d13-152">RELATED LINKS</span></span>

[<span data-ttu-id="95d13-153">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="95d13-153">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="95d13-154">새로운 AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="95d13-154">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="95d13-155">제거-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="95d13-155">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="95d13-156">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="95d13-156">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


