---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AF8CC409-2EA7-4EC1-86C9-E7A773DE9201
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayhttplistener
schema: 2.0.0
ms.openlocfilehash: f6b8e2a869ba6c59011241c5ebb7b1fe46ac2bc7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93880669"
---
# <span data-ttu-id="a409c-101">New-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="a409c-101">New-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="a409c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a409c-102">SYNOPSIS</span></span>
<span data-ttu-id="a409c-103">응용 프로그램 게이트웨이에 대 한 HTTP 수신기를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a409c-103">Creates an HTTP listener for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a409c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a409c-104">SYNTAX</span></span>

### <span data-ttu-id="a409c-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a409c-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayHttpListener -Name <String> [-FrontendIPConfigurationId <String>]
 [-FrontendPortId <String>] [-SslCertificateId <String>] [-HostName <String>]
 [-RequireServerNameIndication <String>] -Protocol <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a409c-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="a409c-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayHttpListener -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a409c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="a409c-107">DESCRIPTION</span></span>
<span data-ttu-id="a409c-108">**AzureRmApplicationGatewayHttpListener** Cmdlet은 Azure application gateway에 대 한 HTTP 수신기를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a409c-108">The **New-AzureRmApplicationGatewayHttpListener** cmdlet creates an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="a409c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="a409c-109">EXAMPLES</span></span>

### <span data-ttu-id="a409c-110">예제 1: HTTP 수신기 만들기</span><span class="sxs-lookup"><span data-stu-id="a409c-110">Example 1: Create an HTTP listener</span></span>
```
PS C:\>$Listener = New-AzureRmApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01
```

<span data-ttu-id="a409c-111">이 명령은 Listener01 이라는 HTTP 수신기를 만들고 결과를 명명 된 변수 $Listener에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a409c-111">This command creates an HTTP listener named Listener01 and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="a409c-112">예제 2: SSL을 사용 하 여 HTTP 수신기 만들기</span><span class="sxs-lookup"><span data-stu-id="a409c-112">Example 2: Create an HTTP listener with SSL</span></span>
```
PS C:\>$Listener = New-AzureRmApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="a409c-113">이 명령은 SSL 오프 로드를 사용 하 고 $SSLCert 01 변수에 SSL 인증서를 제공 하는 HTTP 수신기를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a409c-113">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable.</span></span>
<span data-ttu-id="a409c-114">이 명령은 $Listener 이라는 변수에 결과를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a409c-114">The command stores the result in the variable named $Listener.</span></span>

## <span data-ttu-id="a409c-115">변수</span><span class="sxs-lookup"><span data-stu-id="a409c-115">PARAMETERS</span></span>

### <span data-ttu-id="a409c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a409c-116">-DefaultProfile</span></span>
<span data-ttu-id="a409c-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a409c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a409c-118">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="a409c-118">-FrontendIPConfiguration</span></span>
<span data-ttu-id="a409c-119">HTTP 수신기에 대 한 프런트 엔드 IP 구성 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a409c-119">Specifies front-end IP configuration object for the HTTP listener.</span></span>

```yaml
Type: PSApplicationGatewayFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a409c-120">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="a409c-120">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="a409c-121">HTTP 수신기에 대 한 프런트 엔드 IP 구성의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a409c-121">Specifies the ID of the front-end IP configuration for the HTTP listener.</span></span>

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

### <span data-ttu-id="a409c-122">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="a409c-122">-FrontendPort</span></span>
<span data-ttu-id="a409c-123">HTTP 수신기에 대 한 프런트 엔드 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a409c-123">Specifies the front-end port for the HTTP listener.</span></span>

```yaml
Type: PSApplicationGatewayFrontendPort
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a409c-124">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="a409c-124">-FrontendPortId</span></span>
<span data-ttu-id="a409c-125">HTTP 수신기에 대 한 프런트 엔드 포트 개체의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a409c-125">Specifies the ID of the front-end port object for the HTTP listener.</span></span>

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

### <span data-ttu-id="a409c-126">-HostName</span><span class="sxs-lookup"><span data-stu-id="a409c-126">-HostName</span></span>
<span data-ttu-id="a409c-127">Application gateway HTTP 수신기의 호스트 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a409c-127">Specifies the host name of the application gateway HTTP listener.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a409c-128">-이름</span><span class="sxs-lookup"><span data-stu-id="a409c-128">-Name</span></span>
<span data-ttu-id="a409c-129">이 cmdlet이 만드는 HTTP 수신기의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a409c-129">Specifies the name of the HTTP listener that this cmdlet creates.</span></span>

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

### <span data-ttu-id="a409c-130">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="a409c-130">-Protocol</span></span>
<span data-ttu-id="a409c-131">HTTP 수신기가 사용 하는 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a409c-131">Specifies the protocol that the HTTP listener uses.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a409c-132">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="a409c-132">-RequireServerNameIndication</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: true, false

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a409c-133">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="a409c-133">-SslCertificate</span></span>
<span data-ttu-id="a409c-134">HTTP 수신기에 대 한 SSL 인증서 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a409c-134">Specifies the SSL certificate object for  the HTTP listener.</span></span>

```yaml
Type: PSApplicationGatewaySslCertificate
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a409c-135">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="a409c-135">-SslCertificateId</span></span>
<span data-ttu-id="a409c-136">HTTP 수신기에 대 한 SSL 인증서의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a409c-136">Specifies the ID of the SSL certificate for the HTTP listener.</span></span>

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

### <span data-ttu-id="a409c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a409c-137">CommonParameters</span></span>
<span data-ttu-id="a409c-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a409c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a409c-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a409c-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a409c-140">입력</span><span class="sxs-lookup"><span data-stu-id="a409c-140">INPUTS</span></span>

### <span data-ttu-id="a409c-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a409c-141">System.String</span></span>

## <span data-ttu-id="a409c-142">출력</span><span class="sxs-lookup"><span data-stu-id="a409c-142">OUTPUTS</span></span>

### <span data-ttu-id="a409c-143">PSHttpListener에 대 한.</span><span class="sxs-lookup"><span data-stu-id="a409c-143">Microsoft.Azure.Commands.Network.Models.PSHttpListener</span></span>

## <span data-ttu-id="a409c-144">상속자</span><span class="sxs-lookup"><span data-stu-id="a409c-144">NOTES</span></span>

## <span data-ttu-id="a409c-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a409c-145">RELATED LINKS</span></span>

[<span data-ttu-id="a409c-146">추가-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="a409c-146">Add-AzureRmApplicationGatewayHttpListener</span></span>](./Add-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="a409c-147">Get-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="a409c-147">Get-AzureRmApplicationGatewayHttpListener</span></span>](./Get-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="a409c-148">제거-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="a409c-148">Remove-AzureRmApplicationGatewayHttpListener</span></span>](./Remove-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="a409c-149">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="a409c-149">Set-AzureRmApplicationGatewayHttpListener</span></span>](./Set-AzureRmApplicationGatewayHttpListener.md)


