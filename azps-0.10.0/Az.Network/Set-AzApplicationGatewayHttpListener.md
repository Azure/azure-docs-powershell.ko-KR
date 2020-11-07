---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8068AF1-3380-4E60-B6CF-CC584BD053A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: ea07f3b9f2dd1e79f59b3369f3f8d3a8c1434deb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876607"
---
# <span data-ttu-id="55e76-101">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="55e76-101">Set-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="55e76-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55e76-102">SYNOPSIS</span></span>
<span data-ttu-id="55e76-103">응용 프로그램 게이트웨이에 대 한 HTTP 수신기를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="55e76-103">Modifies an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="55e76-104">구문과</span><span class="sxs-lookup"><span data-stu-id="55e76-104">SYNTAX</span></span>

### <span data-ttu-id="55e76-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="55e76-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55e76-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="55e76-106">SetByResource</span></span>
```
Set-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55e76-107">설명은</span><span class="sxs-lookup"><span data-stu-id="55e76-107">DESCRIPTION</span></span>
<span data-ttu-id="55e76-108">**AzApplicationGatewayHttpListener** Cmdlet은 Azure application gateway에 대 한 HTTP 수신기를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="55e76-108">The **Set-AzApplicationGatewayHttpListener** cmdlet modifies an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="55e76-109">예제의</span><span class="sxs-lookup"><span data-stu-id="55e76-109">EXAMPLES</span></span>

### <span data-ttu-id="55e76-110">예제 1: HTTP 수신기 설정</span><span class="sxs-lookup"><span data-stu-id="55e76-110">Example 1: Set an HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol Http -FrontendIpConfiguration $FIP01 -FrontendPort 80
```

<span data-ttu-id="55e76-111">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에 속하는 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져온 다음이를 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="55e76-111">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="55e76-112">두 번째 명령은 포트 80에서 HTTP 프로토콜을 사용 하 여 $FIP 01에 저장 된 프런트 엔드 구성을 사용 하도록 게이트웨이에 대 한 HTTP 수신기를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="55e76-112">The second command sets the HTTP listener for the gateway to use the front-end configuration stored in $FIP01 with the HTTP protocol on port 80.</span></span>

## <span data-ttu-id="55e76-113">변수</span><span class="sxs-lookup"><span data-stu-id="55e76-113">PARAMETERS</span></span>

### <span data-ttu-id="55e76-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="55e76-114">-ApplicationGateway</span></span>
<span data-ttu-id="55e76-115">이 cmdlet이 HTTP 수신기를 연결 하는 데 사용할 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="55e76-115">Specifies the application gateway with which this cmdlet associates the HTTP listener.</span></span>

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

### <span data-ttu-id="55e76-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55e76-116">-DefaultProfile</span></span>
<span data-ttu-id="55e76-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="55e76-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55e76-118">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="55e76-118">-FrontendIPConfiguration</span></span>
<span data-ttu-id="55e76-119">응용 프로그램 게이트웨이의 프런트 엔드 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="55e76-119">Specifies the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="55e76-120">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="55e76-120">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="55e76-121">응용 프로그램 게이트웨이의 프런트 엔드 IP 주소 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="55e76-121">Specifies the ID of the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="55e76-122">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="55e76-122">-FrontendPort</span></span>
<span data-ttu-id="55e76-123">응용 프로그램 게이트웨이 프런트 엔드 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="55e76-123">Specifies the application gateway front-end port.</span></span>

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

### <span data-ttu-id="55e76-124">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="55e76-124">-FrontendPortId</span></span>
<span data-ttu-id="55e76-125">응용 프로그램 게이트웨이 프런트 엔드 포트 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="55e76-125">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="55e76-126">-HostName</span><span class="sxs-lookup"><span data-stu-id="55e76-126">-HostName</span></span>
<span data-ttu-id="55e76-127">이 cmdlet이 HTTP 수신기를 보내는 호스트 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="55e76-127">Specifies the host name that this cmdlet sends the HTTP listener to.</span></span>

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

### <span data-ttu-id="55e76-128">-이름</span><span class="sxs-lookup"><span data-stu-id="55e76-128">-Name</span></span>
<span data-ttu-id="55e76-129">HTTP 수신기의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="55e76-129">Specifies the name of the HTTP listener.</span></span>

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

### <span data-ttu-id="55e76-130">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="55e76-130">-Protocol</span></span>
<span data-ttu-id="55e76-131">HTTP 수신기가 사용 하는 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="55e76-131">Specifies the protocol that the HTTP listener uses.</span></span>
<span data-ttu-id="55e76-132">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="55e76-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="55e76-133">Http</span><span class="sxs-lookup"><span data-stu-id="55e76-133">Http</span></span>
- <span data-ttu-id="55e76-134">Https</span><span class="sxs-lookup"><span data-stu-id="55e76-134">Https</span></span>

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

### <span data-ttu-id="55e76-135">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="55e76-135">-RequireServerNameIndication</span></span>
<span data-ttu-id="55e76-136">Cmdlet에 서버 이름 표시가 필요한 지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="55e76-136">Specifies whether the cmdlet requires a server name indication.</span></span>
<span data-ttu-id="55e76-137">이 매개 변수에 허용 되는 값은 true 또는 false입니다.</span><span class="sxs-lookup"><span data-stu-id="55e76-137">The acceptable values for this parameter are: true or false.</span></span>

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

### <span data-ttu-id="55e76-138">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="55e76-138">-SslCertificate</span></span>
<span data-ttu-id="55e76-139">HTTP 수신기의 SSL 인증서를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="55e76-139">Specifies the SSL certificate of the HTTP listener.</span></span>

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

### <span data-ttu-id="55e76-140">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="55e76-140">-SslCertificateId</span></span>
<span data-ttu-id="55e76-141">HTTP 수신기의 SSL (Secure Socket Layer) 인증서 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="55e76-141">Specifies the Secure Socket Layer (SSL) certificate ID of the HTTP listener.</span></span>

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

### <span data-ttu-id="55e76-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55e76-142">CommonParameters</span></span>
<span data-ttu-id="55e76-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="55e76-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55e76-144">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55e76-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55e76-145">입력</span><span class="sxs-lookup"><span data-stu-id="55e76-145">INPUTS</span></span>

### <span data-ttu-id="55e76-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="55e76-146">System.String</span></span>

## <span data-ttu-id="55e76-147">출력</span><span class="sxs-lookup"><span data-stu-id="55e76-147">OUTPUTS</span></span>

### <span data-ttu-id="55e76-148">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="55e76-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="55e76-149">상속자</span><span class="sxs-lookup"><span data-stu-id="55e76-149">NOTES</span></span>

## <span data-ttu-id="55e76-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="55e76-150">RELATED LINKS</span></span>

[<span data-ttu-id="55e76-151">추가-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="55e76-151">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="55e76-152">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="55e76-152">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="55e76-153">새로운 AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="55e76-153">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="55e76-154">제거-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="55e76-154">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)


