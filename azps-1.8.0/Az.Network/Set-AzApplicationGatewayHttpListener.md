---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8068AF1-3380-4E60-B6CF-CC584BD053A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 11a416e237ff4a12dc3aafbd161e1ae77faab732
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700054"
---
# <span data-ttu-id="6990e-101">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="6990e-101">Set-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="6990e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6990e-102">SYNOPSIS</span></span>
<span data-ttu-id="6990e-103">응용 프로그램 게이트웨이에 대 한 HTTP 수신기를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6990e-103">Modifies an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="6990e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6990e-104">SYNTAX</span></span>

### <span data-ttu-id="6990e-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="6990e-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6990e-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="6990e-106">SetByResource</span></span>
```
Set-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6990e-107">설명은</span><span class="sxs-lookup"><span data-stu-id="6990e-107">DESCRIPTION</span></span>
<span data-ttu-id="6990e-108">**AzApplicationGatewayHttpListener** Cmdlet은 Azure application gateway에 대 한 HTTP 수신기를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6990e-108">The **Set-AzApplicationGatewayHttpListener** cmdlet modifies an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="6990e-109">예제의</span><span class="sxs-lookup"><span data-stu-id="6990e-109">EXAMPLES</span></span>

### <span data-ttu-id="6990e-110">예제 1: HTTP 수신기 설정</span><span class="sxs-lookup"><span data-stu-id="6990e-110">Example 1: Set an HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol Http -FrontendIpConfiguration $FIP01 -FrontendPort 80
```

<span data-ttu-id="6990e-111">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에 속하는 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져온 다음이를 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="6990e-111">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="6990e-112">두 번째 명령은 포트 80에서 HTTP 프로토콜을 사용 하 여 $FIP 01에 저장 된 프런트 엔드 구성을 사용 하도록 게이트웨이에 대 한 HTTP 수신기를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6990e-112">The second command sets the HTTP listener for the gateway to use the front-end configuration stored in $FIP01 with the HTTP protocol on port 80.</span></span>

## <span data-ttu-id="6990e-113">변수</span><span class="sxs-lookup"><span data-stu-id="6990e-113">PARAMETERS</span></span>

### <span data-ttu-id="6990e-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6990e-114">-ApplicationGateway</span></span>
<span data-ttu-id="6990e-115">이 cmdlet이 HTTP 수신기를 연결 하는 데 사용할 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6990e-115">Specifies the application gateway with which this cmdlet associates the HTTP listener.</span></span>

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

### <span data-ttu-id="6990e-116">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="6990e-116">-CustomErrorConfiguration</span></span>
<span data-ttu-id="6990e-117">Application gateway의 고객 오류</span><span class="sxs-lookup"><span data-stu-id="6990e-117">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="6990e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6990e-118">-DefaultProfile</span></span>
<span data-ttu-id="6990e-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6990e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6990e-120">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="6990e-120">-FrontendIPConfiguration</span></span>
<span data-ttu-id="6990e-121">응용 프로그램 게이트웨이의 프런트 엔드 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6990e-121">Specifies the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="6990e-122">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="6990e-122">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="6990e-123">응용 프로그램 게이트웨이의 프런트 엔드 IP 주소 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6990e-123">Specifies the ID of the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="6990e-124">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="6990e-124">-FrontendPort</span></span>
<span data-ttu-id="6990e-125">응용 프로그램 게이트웨이 프런트 엔드 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6990e-125">Specifies the application gateway front-end port.</span></span>

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

### <span data-ttu-id="6990e-126">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="6990e-126">-FrontendPortId</span></span>
<span data-ttu-id="6990e-127">응용 프로그램 게이트웨이 프런트 엔드 포트 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6990e-127">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="6990e-128">-HostName</span><span class="sxs-lookup"><span data-stu-id="6990e-128">-HostName</span></span>
<span data-ttu-id="6990e-129">이 cmdlet이 HTTP 수신기를 보내는 호스트 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6990e-129">Specifies the host name that this cmdlet sends the HTTP listener to.</span></span>

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

### <span data-ttu-id="6990e-130">-이름</span><span class="sxs-lookup"><span data-stu-id="6990e-130">-Name</span></span>
<span data-ttu-id="6990e-131">HTTP 수신기의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6990e-131">Specifies the name of the HTTP listener.</span></span>

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

### <span data-ttu-id="6990e-132">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="6990e-132">-Protocol</span></span>
<span data-ttu-id="6990e-133">HTTP 수신기가 사용 하는 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6990e-133">Specifies the protocol that the HTTP listener uses.</span></span>
<span data-ttu-id="6990e-134">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6990e-134">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6990e-135">Http</span><span class="sxs-lookup"><span data-stu-id="6990e-135">Http</span></span>
- <span data-ttu-id="6990e-136">Https</span><span class="sxs-lookup"><span data-stu-id="6990e-136">Https</span></span>

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

### <span data-ttu-id="6990e-137">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="6990e-137">-RequireServerNameIndication</span></span>
<span data-ttu-id="6990e-138">Cmdlet에 서버 이름 표시가 필요한 지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6990e-138">Specifies whether the cmdlet requires a server name indication.</span></span>
<span data-ttu-id="6990e-139">이 매개 변수에 허용 되는 값은 true 또는 false입니다.</span><span class="sxs-lookup"><span data-stu-id="6990e-139">The acceptable values for this parameter are: true or false.</span></span>

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

### <span data-ttu-id="6990e-140">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="6990e-140">-SslCertificate</span></span>
<span data-ttu-id="6990e-141">HTTP 수신기의 SSL 인증서를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6990e-141">Specifies the SSL certificate of the HTTP listener.</span></span>

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

### <span data-ttu-id="6990e-142">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="6990e-142">-SslCertificateId</span></span>
<span data-ttu-id="6990e-143">HTTP 수신기의 SSL (Secure Socket Layer) 인증서 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6990e-143">Specifies the Secure Socket Layer (SSL) certificate ID of the HTTP listener.</span></span>

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

### <span data-ttu-id="6990e-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6990e-144">CommonParameters</span></span>
<span data-ttu-id="6990e-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6990e-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6990e-146">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6990e-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6990e-147">입력</span><span class="sxs-lookup"><span data-stu-id="6990e-147">INPUTS</span></span>

### <span data-ttu-id="6990e-148">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6990e-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6990e-149">출력</span><span class="sxs-lookup"><span data-stu-id="6990e-149">OUTPUTS</span></span>

### <span data-ttu-id="6990e-150">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6990e-150">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6990e-151">상속자</span><span class="sxs-lookup"><span data-stu-id="6990e-151">NOTES</span></span>

## <span data-ttu-id="6990e-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6990e-152">RELATED LINKS</span></span>

[<span data-ttu-id="6990e-153">추가-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="6990e-153">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="6990e-154">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="6990e-154">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="6990e-155">새로운 AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="6990e-155">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="6990e-156">제거-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="6990e-156">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)


