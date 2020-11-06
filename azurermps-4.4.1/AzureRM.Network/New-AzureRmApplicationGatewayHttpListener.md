---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AF8CC409-2EA7-4EC1-86C9-E7A773DE9201
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayHttpListener.md
ms.openlocfilehash: ea7a140d2dca2a590a8d3bc83e946d122fb8fd31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534904"
---
# <span data-ttu-id="9ced9-101">New-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="9ced9-101">New-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="9ced9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ced9-102">SYNOPSIS</span></span>
<span data-ttu-id="9ced9-103">응용 프로그램 게이트웨이에 대 한 HTTP 수신기를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9ced9-103">Creates an HTTP listener for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ced9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9ced9-104">SYNTAX</span></span>

### <span data-ttu-id="9ced9-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9ced9-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayHttpListener -Name <String> [-FrontendIPConfigurationId <String>]
 [-FrontendPortId <String>] [-SslCertificateId <String>] [-HostName <String>]
 [-RequireServerNameIndication <String>] -Protocol <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9ced9-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="9ced9-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayHttpListener -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ced9-107">설명은</span><span class="sxs-lookup"><span data-stu-id="9ced9-107">DESCRIPTION</span></span>
<span data-ttu-id="9ced9-108">**AzureRmApplicationGatewayHttpListener** Cmdlet은 Azure application gateway에 대 한 HTTP 수신기를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9ced9-108">The **New-AzureRmApplicationGatewayHttpListener** cmdlet creates an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="9ced9-109">예제의</span><span class="sxs-lookup"><span data-stu-id="9ced9-109">EXAMPLES</span></span>

### <span data-ttu-id="9ced9-110">예제 1: HTTP 수신기 만들기</span><span class="sxs-lookup"><span data-stu-id="9ced9-110">Example 1: Create an HTTP listener</span></span>
```
PS C:\>$Listener = New-AzureRmApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01
```

<span data-ttu-id="9ced9-111">이 명령은 Listener01 이라는 HTTP 수신기를 만들고 결과를 명명 된 변수 $Listener에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ced9-111">This command creates an HTTP listener named Listener01 and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="9ced9-112">예제 2: SSL을 사용 하 여 HTTP 수신기 만들기</span><span class="sxs-lookup"><span data-stu-id="9ced9-112">Example 2: Create an HTTP listener with SSL</span></span>
```
PS C:\>$Listener = New-AzureRmApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="9ced9-113">이 명령은 SSL 오프 로드를 사용 하 고 $SSLCert 01 변수에 SSL 인증서를 제공 하는 HTTP 수신기를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9ced9-113">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable.</span></span>
<span data-ttu-id="9ced9-114">이 명령은 $Listener 이라는 변수에 결과를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ced9-114">The command stores the result in the variable named $Listener.</span></span>

## <span data-ttu-id="9ced9-115">변수</span><span class="sxs-lookup"><span data-stu-id="9ced9-115">PARAMETERS</span></span>

### <span data-ttu-id="9ced9-116">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="9ced9-116">-FrontendIPConfiguration</span></span>
<span data-ttu-id="9ced9-117">HTTP 수신기에 대 한 프런트 엔드 IP 구성 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ced9-117">Specifies front-end IP configuration object for the HTTP listener.</span></span>

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

### <span data-ttu-id="9ced9-118">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="9ced9-118">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="9ced9-119">HTTP 수신기에 대 한 프런트 엔드 IP 구성의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ced9-119">Specifies the ID of the front-end IP configuration for the HTTP listener.</span></span>

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

### <span data-ttu-id="9ced9-120">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="9ced9-120">-FrontendPort</span></span>
<span data-ttu-id="9ced9-121">HTTP 수신기에 대 한 프런트 엔드 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ced9-121">Specifies the front-end port for the HTTP listener.</span></span>

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

### <span data-ttu-id="9ced9-122">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="9ced9-122">-FrontendPortId</span></span>
<span data-ttu-id="9ced9-123">HTTP 수신기에 대 한 프런트 엔드 포트 개체의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ced9-123">Specifies the ID of the front-end port object for the HTTP listener.</span></span>

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

### <span data-ttu-id="9ced9-124">-HostName</span><span class="sxs-lookup"><span data-stu-id="9ced9-124">-HostName</span></span>
<span data-ttu-id="9ced9-125">Application gateway HTTP 수신기의 호스트 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ced9-125">Specifies the host name of the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="9ced9-126">-이름</span><span class="sxs-lookup"><span data-stu-id="9ced9-126">-Name</span></span>
<span data-ttu-id="9ced9-127">이 cmdlet이 만드는 HTTP 수신기의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ced9-127">Specifies the name of the HTTP listener that this cmdlet creates.</span></span>

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

### <span data-ttu-id="9ced9-128">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="9ced9-128">-Protocol</span></span>
<span data-ttu-id="9ced9-129">HTTP 수신기가 사용 하는 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ced9-129">Specifies the protocol that the HTTP listener uses.</span></span>

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

### <span data-ttu-id="9ced9-130">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="9ced9-130">-RequireServerNameIndication</span></span>
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

### <span data-ttu-id="9ced9-131">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="9ced9-131">-SslCertificate</span></span>
<span data-ttu-id="9ced9-132">HTTP 수신기에 대 한 SSL 인증서 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ced9-132">Specifies the SSL certificate object for  the HTTP listener.</span></span>

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

### <span data-ttu-id="9ced9-133">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="9ced9-133">-SslCertificateId</span></span>
<span data-ttu-id="9ced9-134">HTTP 수신기에 대 한 SSL 인증서의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ced9-134">Specifies the ID of the SSL certificate for the HTTP listener.</span></span>

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

### <span data-ttu-id="9ced9-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ced9-135">-DefaultProfile</span></span>
<span data-ttu-id="9ced9-136">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9ced9-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ced9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ced9-137">CommonParameters</span></span>
<span data-ttu-id="9ced9-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ced9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ced9-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ced9-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ced9-140">입력</span><span class="sxs-lookup"><span data-stu-id="9ced9-140">INPUTS</span></span>

### <span data-ttu-id="9ced9-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9ced9-141">System.String</span></span>

## <span data-ttu-id="9ced9-142">출력</span><span class="sxs-lookup"><span data-stu-id="9ced9-142">OUTPUTS</span></span>

### <span data-ttu-id="9ced9-143">PSHttpListener에 대 한.</span><span class="sxs-lookup"><span data-stu-id="9ced9-143">Microsoft.Azure.Commands.Network.Models.PSHttpListener</span></span>

## <span data-ttu-id="9ced9-144">상속자</span><span class="sxs-lookup"><span data-stu-id="9ced9-144">NOTES</span></span>

## <span data-ttu-id="9ced9-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9ced9-145">RELATED LINKS</span></span>

[<span data-ttu-id="9ced9-146">추가-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="9ced9-146">Add-AzureRmApplicationGatewayHttpListener</span></span>](./Add-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="9ced9-147">Get-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="9ced9-147">Get-AzureRmApplicationGatewayHttpListener</span></span>](./Get-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="9ced9-148">제거-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="9ced9-148">Remove-AzureRmApplicationGatewayHttpListener</span></span>](./Remove-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="9ced9-149">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="9ced9-149">Set-AzureRmApplicationGatewayHttpListener</span></span>](./Set-AzureRmApplicationGatewayHttpListener.md)


