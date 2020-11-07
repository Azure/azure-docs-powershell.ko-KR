---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8068AF1-3380-4E60-B6CF-CC584BD053A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayHttpListener.md
ms.openlocfilehash: 26cf3a0fb3ae118913130a754def47a257aac254
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711138"
---
# <span data-ttu-id="349a0-101">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="349a0-101">Set-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="349a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="349a0-102">SYNOPSIS</span></span>
<span data-ttu-id="349a0-103">응용 프로그램 게이트웨이에 대 한 HTTP 수신기를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="349a0-103">Modifies an HTTP listener for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="349a0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="349a0-104">SYNTAX</span></span>

### <span data-ttu-id="349a0-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="349a0-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="349a0-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="349a0-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="349a0-107">설명은</span><span class="sxs-lookup"><span data-stu-id="349a0-107">DESCRIPTION</span></span>
<span data-ttu-id="349a0-108">**AzureRmApplicationGatewayHttpListener** Cmdlet은 Azure application gateway에 대 한 HTTP 수신기를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="349a0-108">The **Set-AzureRmApplicationGatewayHttpListener** cmdlet modifies an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="349a0-109">예제의</span><span class="sxs-lookup"><span data-stu-id="349a0-109">EXAMPLES</span></span>

### <span data-ttu-id="349a0-110">예제 1: HTTP 수신기 설정</span><span class="sxs-lookup"><span data-stu-id="349a0-110">Example 1: Set an HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol Http -FrontendIpConfiguration $FIP01 -FrontendPort 80
```

<span data-ttu-id="349a0-111">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에 속하는 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져온 다음이를 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="349a0-111">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="349a0-112">두 번째 명령은 포트 80에서 HTTP 프로토콜을 사용 하 여 $FIP 01에 저장 된 프런트 엔드 구성을 사용 하도록 게이트웨이에 대 한 HTTP 수신기를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="349a0-112">The second command sets the HTTP listener for the gateway to use the front-end configuration stored in $FIP01 with the HTTP protocol on port 80.</span></span>

## <span data-ttu-id="349a0-113">변수</span><span class="sxs-lookup"><span data-stu-id="349a0-113">PARAMETERS</span></span>

### <span data-ttu-id="349a0-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="349a0-114">-ApplicationGateway</span></span>
<span data-ttu-id="349a0-115">이 cmdlet이 HTTP 수신기를 연결 하는 데 사용할 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="349a0-115">Specifies the application gateway with which this cmdlet associates the HTTP listener.</span></span>

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

### <span data-ttu-id="349a0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="349a0-116">-DefaultProfile</span></span>
<span data-ttu-id="349a0-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="349a0-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="349a0-118">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="349a0-118">-FrontendIPConfiguration</span></span>
<span data-ttu-id="349a0-119">응용 프로그램 게이트웨이의 프런트 엔드 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="349a0-119">Specifies the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="349a0-120">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="349a0-120">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="349a0-121">응용 프로그램 게이트웨이의 프런트 엔드 IP 주소 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="349a0-121">Specifies the ID of the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="349a0-122">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="349a0-122">-FrontendPort</span></span>
<span data-ttu-id="349a0-123">응용 프로그램 게이트웨이 프런트 엔드 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="349a0-123">Specifies the application gateway front-end port.</span></span>

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

### <span data-ttu-id="349a0-124">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="349a0-124">-FrontendPortId</span></span>
<span data-ttu-id="349a0-125">응용 프로그램 게이트웨이 프런트 엔드 포트 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="349a0-125">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="349a0-126">-HostName</span><span class="sxs-lookup"><span data-stu-id="349a0-126">-HostName</span></span>
<span data-ttu-id="349a0-127">이 cmdlet이 HTTP 수신기를 보내는 호스트 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="349a0-127">Specifies the host name that this cmdlet sends the HTTP listener to.</span></span>

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

### <span data-ttu-id="349a0-128">-이름</span><span class="sxs-lookup"><span data-stu-id="349a0-128">-Name</span></span>
<span data-ttu-id="349a0-129">HTTP 수신기의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="349a0-129">Specifies the name of the HTTP listener.</span></span>

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

### <span data-ttu-id="349a0-130">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="349a0-130">-Protocol</span></span>
<span data-ttu-id="349a0-131">HTTP 수신기가 사용 하는 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="349a0-131">Specifies the protocol that the HTTP listener uses.</span></span>
<span data-ttu-id="349a0-132">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="349a0-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="349a0-133">Http</span><span class="sxs-lookup"><span data-stu-id="349a0-133">Http</span></span>
- <span data-ttu-id="349a0-134">Https</span><span class="sxs-lookup"><span data-stu-id="349a0-134">Https</span></span>

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

### <span data-ttu-id="349a0-135">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="349a0-135">-RequireServerNameIndication</span></span>
<span data-ttu-id="349a0-136">Cmdlet에 서버 이름 표시가 필요한 지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="349a0-136">Specifies whether the cmdlet requires a server name indication.</span></span>
<span data-ttu-id="349a0-137">이 매개 변수에 허용 되는 값은 true 또는 false입니다.</span><span class="sxs-lookup"><span data-stu-id="349a0-137">The acceptable values for this parameter are: true or false.</span></span>

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

### <span data-ttu-id="349a0-138">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="349a0-138">-SslCertificate</span></span>
<span data-ttu-id="349a0-139">HTTP 수신기의 SSL 인증서를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="349a0-139">Specifies the SSL certificate of the HTTP listener.</span></span>

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

### <span data-ttu-id="349a0-140">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="349a0-140">-SslCertificateId</span></span>
<span data-ttu-id="349a0-141">HTTP 수신기의 SSL (Secure Socket Layer) 인증서 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="349a0-141">Specifies the Secure Socket Layer (SSL) certificate ID of the HTTP listener.</span></span>

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

### <span data-ttu-id="349a0-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="349a0-142">CommonParameters</span></span>
<span data-ttu-id="349a0-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="349a0-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="349a0-144">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="349a0-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="349a0-145">입력</span><span class="sxs-lookup"><span data-stu-id="349a0-145">INPUTS</span></span>

### <span data-ttu-id="349a0-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="349a0-146">System.String</span></span>

## <span data-ttu-id="349a0-147">출력</span><span class="sxs-lookup"><span data-stu-id="349a0-147">OUTPUTS</span></span>

### <span data-ttu-id="349a0-148">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="349a0-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="349a0-149">상속자</span><span class="sxs-lookup"><span data-stu-id="349a0-149">NOTES</span></span>

## <span data-ttu-id="349a0-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="349a0-150">RELATED LINKS</span></span>

[<span data-ttu-id="349a0-151">추가-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="349a0-151">Add-AzureRmApplicationGatewayHttpListener</span></span>](./Add-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="349a0-152">Get-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="349a0-152">Get-AzureRmApplicationGatewayHttpListener</span></span>](./Get-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="349a0-153">새로운 AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="349a0-153">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="349a0-154">제거-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="349a0-154">Remove-AzureRmApplicationGatewayHttpListener</span></span>](./Remove-AzureRmApplicationGatewayHttpListener.md)


