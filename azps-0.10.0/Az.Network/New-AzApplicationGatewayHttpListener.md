---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF8CC409-2EA7-4EC1-86C9-E7A773DE9201
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 104a5e022d89421ac960d699c7391db660c0dd6b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875468"
---
# <span data-ttu-id="06c15-101">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="06c15-101">New-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="06c15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06c15-102">SYNOPSIS</span></span>
<span data-ttu-id="06c15-103">응용 프로그램 게이트웨이에 대 한 HTTP 수신기를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="06c15-103">Creates an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="06c15-104">구문과</span><span class="sxs-lookup"><span data-stu-id="06c15-104">SYNTAX</span></span>

### <span data-ttu-id="06c15-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="06c15-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String> [-FrontendIPConfigurationId <String>]
 [-FrontendPortId <String>] [-SslCertificateId <String>] [-HostName <String>]
 [-RequireServerNameIndication <String>] -Protocol <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="06c15-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="06c15-106">SetByResource</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06c15-107">설명은</span><span class="sxs-lookup"><span data-stu-id="06c15-107">DESCRIPTION</span></span>
<span data-ttu-id="06c15-108">**AzApplicationGatewayHttpListener** Cmdlet은 Azure application gateway에 대 한 HTTP 수신기를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="06c15-108">The **New-AzApplicationGatewayHttpListener** cmdlet creates an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="06c15-109">예제의</span><span class="sxs-lookup"><span data-stu-id="06c15-109">EXAMPLES</span></span>

### <span data-ttu-id="06c15-110">예제 1: HTTP 수신기 만들기</span><span class="sxs-lookup"><span data-stu-id="06c15-110">Example 1: Create an HTTP listener</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01
```

<span data-ttu-id="06c15-111">이 명령은 Listener01 이라는 HTTP 수신기를 만들고 결과를 명명 된 변수 $Listener에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c15-111">This command creates an HTTP listener named Listener01 and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="06c15-112">예제 2: SSL을 사용 하 여 HTTP 수신기 만들기</span><span class="sxs-lookup"><span data-stu-id="06c15-112">Example 2: Create an HTTP listener with SSL</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="06c15-113">이 명령은 SSL 오프 로드를 사용 하 고 $SSLCert 01 변수에 SSL 인증서를 제공 하는 HTTP 수신기를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="06c15-113">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable.</span></span>
<span data-ttu-id="06c15-114">이 명령은 $Listener 이라는 변수에 결과를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c15-114">The command stores the result in the variable named $Listener.</span></span>

## <span data-ttu-id="06c15-115">변수</span><span class="sxs-lookup"><span data-stu-id="06c15-115">PARAMETERS</span></span>

### <span data-ttu-id="06c15-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06c15-116">-DefaultProfile</span></span>
<span data-ttu-id="06c15-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="06c15-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06c15-118">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="06c15-118">-FrontendIPConfiguration</span></span>
<span data-ttu-id="06c15-119">HTTP 수신기에 대 한 프런트 엔드 IP 구성 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c15-119">Specifies front-end IP configuration object for the HTTP listener.</span></span>

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

### <span data-ttu-id="06c15-120">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="06c15-120">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="06c15-121">HTTP 수신기에 대 한 프런트 엔드 IP 구성의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c15-121">Specifies the ID of the front-end IP configuration for the HTTP listener.</span></span>

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

### <span data-ttu-id="06c15-122">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="06c15-122">-FrontendPort</span></span>
<span data-ttu-id="06c15-123">HTTP 수신기에 대 한 프런트 엔드 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c15-123">Specifies the front-end port for the HTTP listener.</span></span>

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

### <span data-ttu-id="06c15-124">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="06c15-124">-FrontendPortId</span></span>
<span data-ttu-id="06c15-125">HTTP 수신기에 대 한 프런트 엔드 포트 개체의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c15-125">Specifies the ID of the front-end port object for the HTTP listener.</span></span>

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

### <span data-ttu-id="06c15-126">-HostName</span><span class="sxs-lookup"><span data-stu-id="06c15-126">-HostName</span></span>
<span data-ttu-id="06c15-127">Application gateway HTTP 수신기의 호스트 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c15-127">Specifies the host name of the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="06c15-128">-이름</span><span class="sxs-lookup"><span data-stu-id="06c15-128">-Name</span></span>
<span data-ttu-id="06c15-129">이 cmdlet이 만드는 HTTP 수신기의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c15-129">Specifies the name of the HTTP listener that this cmdlet creates.</span></span>

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

### <span data-ttu-id="06c15-130">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="06c15-130">-Protocol</span></span>
<span data-ttu-id="06c15-131">HTTP 수신기가 사용 하는 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c15-131">Specifies the protocol that the HTTP listener uses.</span></span>

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

### <span data-ttu-id="06c15-132">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="06c15-132">-RequireServerNameIndication</span></span>
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

### <span data-ttu-id="06c15-133">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="06c15-133">-SslCertificate</span></span>
<span data-ttu-id="06c15-134">HTTP 수신기에 대 한 SSL 인증서 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c15-134">Specifies the SSL certificate object for  the HTTP listener.</span></span>

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

### <span data-ttu-id="06c15-135">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="06c15-135">-SslCertificateId</span></span>
<span data-ttu-id="06c15-136">HTTP 수신기에 대 한 SSL 인증서의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c15-136">Specifies the ID of the SSL certificate for the HTTP listener.</span></span>

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

### <span data-ttu-id="06c15-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06c15-137">CommonParameters</span></span>
<span data-ttu-id="06c15-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c15-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06c15-139">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06c15-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06c15-140">입력</span><span class="sxs-lookup"><span data-stu-id="06c15-140">INPUTS</span></span>

### <span data-ttu-id="06c15-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="06c15-141">System.String</span></span>

## <span data-ttu-id="06c15-142">출력</span><span class="sxs-lookup"><span data-stu-id="06c15-142">OUTPUTS</span></span>

### <span data-ttu-id="06c15-143">PSHttpListener에 대 한.</span><span class="sxs-lookup"><span data-stu-id="06c15-143">Microsoft.Azure.Commands.Network.Models.PSHttpListener</span></span>

## <span data-ttu-id="06c15-144">상속자</span><span class="sxs-lookup"><span data-stu-id="06c15-144">NOTES</span></span>

## <span data-ttu-id="06c15-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="06c15-145">RELATED LINKS</span></span>

[<span data-ttu-id="06c15-146">추가-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="06c15-146">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="06c15-147">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="06c15-147">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="06c15-148">제거-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="06c15-148">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="06c15-149">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="06c15-149">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


