---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF8CC409-2EA7-4EC1-86C9-E7A773DE9201
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: e5593ae97692813cc36f14942edb21768517f317
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700407"
---
# <span data-ttu-id="07084-101">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="07084-101">New-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="07084-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07084-102">SYNOPSIS</span></span>
<span data-ttu-id="07084-103">응용 프로그램 게이트웨이에 대 한 HTTP 수신기를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="07084-103">Creates an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="07084-104">구문과</span><span class="sxs-lookup"><span data-stu-id="07084-104">SYNTAX</span></span>

### <span data-ttu-id="07084-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="07084-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String> [-FrontendIPConfigurationId <String>]
 [-FrontendPortId <String>] [-SslCertificateId <String>] [-HostName <String>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="07084-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="07084-106">SetByResource</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="07084-107">설명은</span><span class="sxs-lookup"><span data-stu-id="07084-107">DESCRIPTION</span></span>
<span data-ttu-id="07084-108">**AzApplicationGatewayHttpListener** Cmdlet은 Azure application gateway에 대 한 HTTP 수신기를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="07084-108">The **New-AzApplicationGatewayHttpListener** cmdlet creates an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="07084-109">예제의</span><span class="sxs-lookup"><span data-stu-id="07084-109">EXAMPLES</span></span>

### <span data-ttu-id="07084-110">예제 1: HTTP 수신기 만들기</span><span class="sxs-lookup"><span data-stu-id="07084-110">Example 1: Create an HTTP listener</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01
```

<span data-ttu-id="07084-111">이 명령은 Listener01 이라는 HTTP 수신기를 만들고 결과를 명명 된 변수 $Listener에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="07084-111">This command creates an HTTP listener named Listener01 and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="07084-112">예제 2: SSL을 사용 하 여 HTTP 수신기 만들기</span><span class="sxs-lookup"><span data-stu-id="07084-112">Example 2: Create an HTTP listener with SSL</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="07084-113">이 명령은 SSL 오프 로드를 사용 하 고 $SSLCert 01 변수에 SSL 인증서를 제공 하는 HTTP 수신기를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="07084-113">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable.</span></span>
<span data-ttu-id="07084-114">이 명령은 $Listener 이라는 변수에 결과를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="07084-114">The command stores the result in the variable named $Listener.</span></span>

## <span data-ttu-id="07084-115">변수</span><span class="sxs-lookup"><span data-stu-id="07084-115">PARAMETERS</span></span>

### <span data-ttu-id="07084-116">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="07084-116">-CustomErrorConfiguration</span></span>
<span data-ttu-id="07084-117">Application gateway의 고객 오류</span><span class="sxs-lookup"><span data-stu-id="07084-117">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="07084-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07084-118">-DefaultProfile</span></span>
<span data-ttu-id="07084-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="07084-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07084-120">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="07084-120">-FrontendIPConfiguration</span></span>
<span data-ttu-id="07084-121">HTTP 수신기에 대 한 프런트 엔드 IP 구성 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="07084-121">Specifies front-end IP configuration object for the HTTP listener.</span></span>

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

### <span data-ttu-id="07084-122">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="07084-122">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="07084-123">HTTP 수신기에 대 한 프런트 엔드 IP 구성의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="07084-123">Specifies the ID of the front-end IP configuration for the HTTP listener.</span></span>

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

### <span data-ttu-id="07084-124">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="07084-124">-FrontendPort</span></span>
<span data-ttu-id="07084-125">HTTP 수신기에 대 한 프런트 엔드 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="07084-125">Specifies the front-end port for the HTTP listener.</span></span>

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

### <span data-ttu-id="07084-126">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="07084-126">-FrontendPortId</span></span>
<span data-ttu-id="07084-127">HTTP 수신기에 대 한 프런트 엔드 포트 개체의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="07084-127">Specifies the ID of the front-end port object for the HTTP listener.</span></span>

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

### <span data-ttu-id="07084-128">-HostName</span><span class="sxs-lookup"><span data-stu-id="07084-128">-HostName</span></span>
<span data-ttu-id="07084-129">Application gateway HTTP 수신기의 호스트 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="07084-129">Specifies the host name of the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="07084-130">-이름</span><span class="sxs-lookup"><span data-stu-id="07084-130">-Name</span></span>
<span data-ttu-id="07084-131">이 cmdlet이 만드는 HTTP 수신기의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="07084-131">Specifies the name of the HTTP listener that this cmdlet creates.</span></span>

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

### <span data-ttu-id="07084-132">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="07084-132">-Protocol</span></span>
<span data-ttu-id="07084-133">HTTP 수신기가 사용 하는 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="07084-133">Specifies the protocol that the HTTP listener uses.</span></span>

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

### <span data-ttu-id="07084-134">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="07084-134">-RequireServerNameIndication</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: true, false

Required: False
Position: Named
Default value: true
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07084-135">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="07084-135">-SslCertificate</span></span>
<span data-ttu-id="07084-136">HTTP 수신기에 대 한 SSL 인증서 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="07084-136">Specifies the SSL certificate object for the HTTP listener.</span></span>

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

### <span data-ttu-id="07084-137">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="07084-137">-SslCertificateId</span></span>
<span data-ttu-id="07084-138">HTTP 수신기에 대 한 SSL 인증서의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="07084-138">Specifies the ID of the SSL certificate for the HTTP listener.</span></span>

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

### <span data-ttu-id="07084-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07084-139">CommonParameters</span></span>
<span data-ttu-id="07084-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="07084-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07084-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07084-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07084-142">입력</span><span class="sxs-lookup"><span data-stu-id="07084-142">INPUTS</span></span>

### <span data-ttu-id="07084-143">않아야</span><span class="sxs-lookup"><span data-stu-id="07084-143">None</span></span>

## <span data-ttu-id="07084-144">출력</span><span class="sxs-lookup"><span data-stu-id="07084-144">OUTPUTS</span></span>

### <span data-ttu-id="07084-145">PSApplicationGatewayHttpListener에 대 한.</span><span class="sxs-lookup"><span data-stu-id="07084-145">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="07084-146">상속자</span><span class="sxs-lookup"><span data-stu-id="07084-146">NOTES</span></span>

## <span data-ttu-id="07084-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="07084-147">RELATED LINKS</span></span>

[<span data-ttu-id="07084-148">추가-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="07084-148">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="07084-149">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="07084-149">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="07084-150">제거-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="07084-150">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="07084-151">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="07084-151">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


