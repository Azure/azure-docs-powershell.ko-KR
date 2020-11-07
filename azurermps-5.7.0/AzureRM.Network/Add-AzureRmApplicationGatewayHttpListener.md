---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1E192553-61D8-4449-936B-68CF866C710C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayHttpListener.md
ms.openlocfilehash: 34c40e17ca1ae297677c05ffc198c7580ef7c4a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702636"
---
# <span data-ttu-id="14ce4-101">Add-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="14ce4-101">Add-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="14ce4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14ce4-102">SYNOPSIS</span></span>
<span data-ttu-id="14ce4-103">응용 프로그램 게이트웨이에 HTTP 수신기를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="14ce4-103">Adds an HTTP listener to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14ce4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="14ce4-104">SYNTAX</span></span>

### <span data-ttu-id="14ce4-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="14ce4-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14ce4-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="14ce4-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14ce4-107">설명은</span><span class="sxs-lookup"><span data-stu-id="14ce4-107">DESCRIPTION</span></span>
<span data-ttu-id="14ce4-108">**Add-AzureRmApplicationGatewayHttpListener** cmdlet은 응용 프로그램 게이트웨이에 HTTP 수신기를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="14ce4-108">The **Add-AzureRmApplicationGatewayHttpListener** cmdlet adds a HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="14ce4-109">예제의</span><span class="sxs-lookup"><span data-stu-id="14ce4-109">EXAMPLES</span></span>

### <span data-ttu-id="14ce4-110">예제 1: HTTP 수신기 추가</span><span class="sxs-lookup"><span data-stu-id="14ce4-110">Example 1: Add a HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzureRmApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "listener01" -Protocol "Http" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01
```

<span data-ttu-id="14ce4-111">첫 번째 명령은 응용 프로그램 게이트웨이를 가져와 $AppGw 변수에 저장 합니다. 두 번째 명령은 HTTP 수신기를 응용 프로그램 게이트웨이에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="14ce4-111">The first command gets the application gateway and stores it in the $AppGw variable.The second command adds the HTTP listener to the application gateway.</span></span>

### <span data-ttu-id="14ce4-112">예제 2: SSL을 사용 하 여 HTTPS 수신기 추가</span><span class="sxs-lookup"><span data-stu-id="14ce4-112">Example 2: Add a HTTPS listener with SSL</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="14ce4-113">첫 번째 명령은 응용 프로그램 게이트웨이를 가져와 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="14ce4-113">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="14ce4-114">두 번째 명령은 HTTPS 프로토콜을 사용 하는 수신기를 응용 프로그램 게이트웨이에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="14ce4-114">The second command adds the listener, which uses the HTTPS protocol, to the application gateway.</span></span>

## <span data-ttu-id="14ce4-115">변수</span><span class="sxs-lookup"><span data-stu-id="14ce4-115">PARAMETERS</span></span>

### <span data-ttu-id="14ce4-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="14ce4-116">-ApplicationGateway</span></span>
<span data-ttu-id="14ce4-117">이 cmdlet이 HTTP 수신기를 추가 하는 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="14ce4-117">Specifies the application gateway to which this cmdlet adds an HTTP listener.</span></span>

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

### <span data-ttu-id="14ce4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14ce4-118">-DefaultProfile</span></span>
<span data-ttu-id="14ce4-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="14ce4-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14ce4-120">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="14ce4-120">-FrontendIPConfiguration</span></span>
<span data-ttu-id="14ce4-121">응용 프로그램 게이트웨이 프런트 엔드 IP 리소스 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="14ce4-121">Specifies the application gateway front-end IP resource object.</span></span>

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

### <span data-ttu-id="14ce4-122">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="14ce4-122">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="14ce4-123">응용 프로그램 게이트웨이 프런트 엔드 IP ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="14ce4-123">Specifies the application gateway front-end IP ID.</span></span>

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

### <span data-ttu-id="14ce4-124">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="14ce4-124">-FrontendPort</span></span>
<span data-ttu-id="14ce4-125">응용 프로그램 게이트웨이 프런트 엔드 포트 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="14ce4-125">Specifies the application gateway front-end port object.</span></span>

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

### <span data-ttu-id="14ce4-126">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="14ce4-126">-FrontendPortId</span></span>
<span data-ttu-id="14ce4-127">응용 프로그램 게이트웨이 프런트 엔드 포트 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="14ce4-127">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="14ce4-128">-HostName</span><span class="sxs-lookup"><span data-stu-id="14ce4-128">-HostName</span></span>
<span data-ttu-id="14ce4-129">이 cmdlet이 HTTP 수신기를 추가 하는 호스트 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="14ce4-129">Specifies the host name that this cmdlet adds a HTTP listener to.</span></span>

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

### <span data-ttu-id="14ce4-130">-이름</span><span class="sxs-lookup"><span data-stu-id="14ce4-130">-Name</span></span>
<span data-ttu-id="14ce4-131">이 명령이 추가 하는 프런트 엔드 포트의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="14ce4-131">Specifies the name of the front-end port that this command adds.</span></span>

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

### <span data-ttu-id="14ce4-132">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="14ce4-132">-Protocol</span></span>
<span data-ttu-id="14ce4-133">HTTP 수신기의 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="14ce4-133">Specifies the protocol of the HTTP listener.</span></span>
<span data-ttu-id="14ce4-134">HTTP와 HTTPS 모두 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="14ce4-134">Both HTTP and HTTPS are supported.</span></span>

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

### <span data-ttu-id="14ce4-135">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="14ce4-135">-RequireServerNameIndication</span></span>
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

### <span data-ttu-id="14ce4-136">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="14ce4-136">-SslCertificate</span></span>
<span data-ttu-id="14ce4-137">HTTP 수신기의 SSL 인증서를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="14ce4-137">Specifies the SSL certificate of the HTTP listener.</span></span>
<span data-ttu-id="14ce4-138">HTTPS가 수신기 프로토콜로 선택 된 경우에는 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="14ce4-138">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="14ce4-139">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="14ce4-139">-SslCertificateId</span></span>
<span data-ttu-id="14ce4-140">HTTP 수신기의 SSL 인증서 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="14ce4-140">Specifies the SSL certificate ID of the HTTP listener.</span></span>
<span data-ttu-id="14ce4-141">HTTPS가 수신기 프로토콜로 선택 된 경우에는 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="14ce4-141">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="14ce4-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14ce4-142">CommonParameters</span></span>
<span data-ttu-id="14ce4-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="14ce4-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14ce4-144">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14ce4-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14ce4-145">입력</span><span class="sxs-lookup"><span data-stu-id="14ce4-145">INPUTS</span></span>

### <span data-ttu-id="14ce4-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="14ce4-146">System.String</span></span>

## <span data-ttu-id="14ce4-147">출력</span><span class="sxs-lookup"><span data-stu-id="14ce4-147">OUTPUTS</span></span>

### <span data-ttu-id="14ce4-148">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="14ce4-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="14ce4-149">상속자</span><span class="sxs-lookup"><span data-stu-id="14ce4-149">NOTES</span></span>

## <span data-ttu-id="14ce4-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="14ce4-150">RELATED LINKS</span></span>

[<span data-ttu-id="14ce4-151">Get-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="14ce4-151">Get-AzureRmApplicationGatewayHttpListener</span></span>](./Get-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="14ce4-152">새로운 AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="14ce4-152">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="14ce4-153">제거-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="14ce4-153">Remove-AzureRmApplicationGatewayHttpListener</span></span>](./Remove-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="14ce4-154">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="14ce4-154">Set-AzureRmApplicationGatewayHttpListener</span></span>](./Set-AzureRmApplicationGatewayHttpListener.md)


